# 多语言 (i18n) 实现方案文档

## 概述

本项目使用 **TinaX I18N** 框架实现多语言支持。当前项目配置为简体中文 (`cmn-hans`) 作为默认语言区域。

---

## 系统架构

### 1. 配置层 — `I18NConfig.asset`

**路径:** `Assets/Resources/XConfig/TinaX/I18NConfig.asset`

TinaX I18N 的核心配置文件，定义语言区域与翻译文件的映射关系。

```yaml
EnableI18N: 1                          # 启用 i18n
DefaultRegion: cmn-hans                 # 默认语言区域（简体中文）
AutomaticMatchingBySystemLanaguage: 1   # 根据系统语言自动匹配
Regions:
  - Name: cmn-hans                      # 区域名称
    BindLanguage: 0600000028000000      # 绑定的系统语言代码
    JsonDicts:                          # JSON 翻译字典列表
      - LoadPath: Assets/App/Data/lang/hans/hans_common.json
        GroupName: common               # 分组名
      - LoadPath: Assets/App/Data/lang/hans/hans_explorestory.json
        GroupName: explorestory
    AssetDicts: []                     # Asset 类型字典（当前为空）
```

**当前仅注册了一个区域 `cmn-hans`**，包含两个翻译文件分组：
| 分组名 | 文件 | 用途 |
|---|---|---|
| `common` | `hans_common.json` (211K行) | 通用 UI 文本（按钮、提示、系统名称等） |
| `explorestory` | `hans_explorestory.json` (63K行) | 探索剧情文本（角色名、对话、旁白等） |

### 2. 运行时翻译层 — Lua 端

**路径:** `Assets/App/Lua/Common/I18N.lua.bytes`

Lua 端通过 `CS.TinaX.I18N.XI18N.That` 调用 C# 侧的 TinaX I18N 管理器。

```lua
local i18NManager = CS.TinaX.I18N.XI18N.That

-- 通过 key 获取本地化文本
function i18N:GetText(key, groupName, defaultText)

-- 获取当前语言
function i18N:GetCurrentLanguages()

-- 获取并格式化含多个 %s 占位符的本地化字符串
function i18N:GetFormatText(key, ...)
```

**关键特性:**
- `GetText(key, groupName, defaultText)` — 按 key 和分组获取翻译文本
- `GetFormatText(key, ...)` — 支持 `%s` 占位符的格式化文本，通过 `order` 字段解决 Lua `string.format` 无法指定 `%s` 顺序的问题
- 所有文本会经过 `Color.FormatI18NColor()` 处理颜色标签

### 3. 运行时翻译层 — C# 端

#### 3a. 游戏内 i18n — `InGameI18N.cs`

**路径:** `Assets/App/Scripts/InGameI18N.cs`

独立于 TinaX I18N 的轻量级翻译系统，专门用于**资源更新阶段**的 UI 文本（在 TinaX 完全初始化之前可用）。

```csharp
public static class InGameI18N
{
    // 从 VFS 虚拟磁盘或 StreamingAssets 读取 download_common.json
    public static async void UseRegion()

    // 通过 key 获取翻译文本
    public static string GetText(string key)
}
```

**加载优先级:**
1. `VFS_VDisk/download_common.json` （虚拟磁盘缓存，热更后使用）
2. `StreamingAssets/Update/download_common.json` （安装包内原始文件）

**数据格式:**
```json
{
  "data": [
    { "k": "Download_Text_001", "v": "资源档下载中", "order": [] }
  ]
}
```

#### 3b. UI 组件 — `InGameLocalizedText.cs`

**路径:** `Assets/App/Scripts/UI/InGameLocalizedText.cs`

挂载在 GameObject 上的 MonoBehaviour 组件，自动通过 `InGameI18N` 获取翻译文本并设置到 `Text` 或 `TextMeshProUGUI` 组件。

```csharp
public class InGameLocalizedText : MonoBehaviour
{
    public string InGameKey;  // 在 Inspector 中设置的翻译 key
    // Start() 时自动调用 InGameI18N.GetText(InGameKey) 并赋值
}
```

### 4. SDK 层 — GSDK 独立 i18n

**路径:** `Assets/StreamingAssets/gsdk.json`

游戏 SDK（登录、支付等）有自己的独立多语言配置，不经过 TinaX I18N 系统。包含 `zh-Hans`、`zh-Hant`、`en`、`ja`、`ko` 等多个语言。

---

## 翻译文件格式

### TinaX I18N JSON 格式 (hans_common.json / hans_explorestory.json)

```json
{
  "data": [
    {
      "k": "Common_btn001",       // 翻译 key
      "v": "确定",                 // 翻译值
      "order": []                  // %s 占位符顺序（空数组表示无占位符）
    }
  ]
}
```

### InGameI18N JSON 格式 (download_common.json)

```json
{
  "data": [
    {
      "k": "Download_Text_001",
      "v": "资源档下载中",
      "order": []
    }
  ]
}
```

---

## 语言文件目录结构

```
Assets/App/Data/lang/
├── hans/                  # 简体中文 (cmn-hans) — 当前激活
│   ├── hans_common.json       ✓ 已转换为简体
│   └── hans_explorestory.json ✓ 已转换为简体
├── tw/                     # 繁体中文(台湾) — 未在 I18NConfig 中注册
│   ├── tw_common.json         实际内容为简体（标签与内容不符）
│   ├── tw_explorestory.json   实际内容为简体
│   └── tw_task.json            实际内容为简体
├── hk/                     # 繁体中文(香港) — 未在 I18NConfig 中注册
│   ├── hk_common.json         实际内容为简体（标签与内容不符）
│   ├── hk_explorestory.json   实际内容为简体
│   └── hk_task.json            实际内容为简体
├── en_us/                  # 英语 — 未在 I18NConfig 中注册
│   └── en_us_common.json
├── jp/                     # 日语 — 未在 I18NConfig 中注册
│   └── jp_common.json
└── kr/                     # 韩语 — 未在 I18NConfig 中注册
    └── kr_common.json
```

> **注意:** `tw` 和 `hk` 文件夹中的文件实际内容已是简体中文，与文件夹标签不符。只有 `hans` 文件夹在 `I18NConfig.asset` 中注册并被游戏使用。

---

## 繁简转换记录

### 已转换的文件

| 文件 | 转换方式 | 词组替换 | 字符替换 |
|---|---|---|---|
| `hans/hans_common.json` | OpenCC 映射表 + C# 脚本 | 14 | 146,401 |
| `hans/hans_explorestory.json` | OpenCC 映射表 + C# 脚本 | 15 | 85,313 |
| `StreamingAssets/Update/download_common.json` | OpenCC 映射表 + C# 脚本 | 0 | 183 |
| `Lua/Data/PlotAnimation.lua.bytes` | OpenCC 映射表 + C# 脚本 | — | (角色名繁→简) |
| `Lua/Data/StageTypeConfig.lua.bytes` | OpenCC 映射表 + C# 脚本 | — | (注释繁→简) |

### 转换工具

使用 [OpenCC (Open Chinese Convert)](https://github.com/BYVoid/OpenCC) 的字符和词组映射表：
- `TSCharacters.txt` — 单字级繁→简映射（2961 条）
- `TSPhrases.txt` — 词组级繁→简映射（361 条，上下文感知）

转换流程：先应用词组替换（避免歧义），再逐字符替换。

### 未转换（设计如此）

| 文件 | 原因 |
|---|---|
| `gsdk.json` 的 `zh-Hant` 部分 | GSDK 独立多语言，繁体部分为设计保留 |
| `Assets/CRIMW/` (CriWare SDK) | 第三方音频 SDK，不涉及游戏文本 |
| `Assets/ThirdPartys/` | 第三方库 |
| `Packages/` (TinaX, Zeus) | 第三方框架代码 |

---

## 使用方式

### Lua 中获取翻译文本

```lua
local I18N = require "Common.I18N"

-- 基本用法
local text = I18N:GetText("Common_btn001")  -- 返回 "确定"

-- 指定分组
local text = I18N:GetText("SomeKey", "explorestory")

-- 格式化文本（含占位符）
local text = I18N:GetFormatText("Download_Text_002", "5", "30")
-- 返回 "剩余时间：5分钟30秒"
```

### Unity Inspector 中绑定翻译

在 GameObject 上添加 `InGameLocalizedText` 组件，设置 `InGameKey` 为对应的翻译 key，运行时自动获取并显示翻译文本。

---

## 注意事项

1. **`hans` 文件夹是唯一激活的语言区域**，其他语言文件夹（`tw`、`hk`、`en_us`、`jp`、`kr`）存在但未在 `I18NConfig.asset` 中注册。
2. **`tw` 和 `hk` 文件夹内容实际为简体中文**，与文件夹标签不符。如需启用繁体支持，需要重新制作繁体翻译文件。
3. **`hans` 文件夹缺少 `hans_task.json`**（`tw` 和 `hk` 有对应的 task 文件），可能表示任务文本不通过 i18n 系统处理。
4. **Lua 脚本中的硬编码中文** — `PlotAnimation.lua.bytes` 中有角色名等硬编码中文字符串，不经过 i18n 系统，修改语言时需同步更新。
5. **GSDK 独立 i18n** — `gsdk.json` 有自己的多语言配置，与 TinaX I18N 系统独立。
