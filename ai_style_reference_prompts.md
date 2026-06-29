# AI风格参考图生成提示词 — 三选一IP置换

## 概述

共需生成 **10张风格参考图**，分两组AI工具各5张：

| 工具 | 角色×3 | UI主界面×1 | 场景×1 | 合计 |
|---|---|---|---|---|
| GPT最新版 | 悟空/赵云/哪吒 | 主界面 | 场景 | 5张 |
| 香蕉最新版 | 悟空/赵云/哪吒 | 主界面 | 场景 | 5张 |
| **总计** | | | | **10张** |

## 原游戏美术风格分析（参考图依据）

### 参考图1：卡牌立绘 `ImgCard0292_FA.png`
- **风格**：高精度半写实二次元插画（Arknights/Honkai级别）
- **技法**：柔渐变阴影（非硬塞璐璐线），柔和喷枪过渡
- **色彩**：互补色方案——紫/蓝背景 vs 粉/橙光源
- **光影**：强背光rim light，体积雾，高光 specular highlights
- **构图**：中心角色+动态pose，背景bokeh虚化

### 参考图2：角色立绘 `Img_headV_01.png`
- **风格**：Cel-shaded anime，魔法少女/idol美学
- **特征**：大眼+宝石高光，华丽装饰，金色配件
- **乐器武器**：奇幻电吉他——半透明蓝色魔法能量+金边框架
- **色彩**：白色+粉色+金色+蓝色

### 参考图3：Loading图 `ImgLoading001.png`
- **风格**：照片级电影3D渲染
- **色彩**：Teal & Orange互补色（冷青蓝 vs 暖橙红）
- **氛围**：史诗科幻战场，体积光，爆炸光效

### 参考图4：战斗场景 `ImgPvp001.png`
- **风格**：科幻技术奇幻，3D场景
- **色彩**：单色蓝色调——从深海军蓝到电光青色
- **元素**：悬浮几何结构，发光能量纹，体积光束，粒子特效
- **氛围**：空灵、神秘、庄严

---

## GPT提示词（5张）

### GPT-1：悟空（西游·侠客·人类化）

```
Create a high-fidelity semi-realistic anime character illustration in the style of premium gacha games like Arknights and Honkai Impact 3rd.

Character: Sun Wukong (Monkey King), humanized warrior form — NOT a literal monkey face, but a handsome young male warrior with monkey-inspired aesthetic features.

Design details:
- Human face with golden irises, subtle golden facial markings/lines on cheeks
- Forehead band (golden circlet) with glowing orange gem
- Pointed monkey-ear decorations on headband (not actual animal ears)
- Spiky golden-brown hair, anime-style
- Muscular lean build, agile stance
- Wearing golden armor plates over a dark navy-blue bodysuit
- Red flowing scarf/cape behind
- Holding a golden staff (Ruyi Jingu Bang) diagonally across body
- Monkey tail visible behind, wrapped around waist

Art style:
- Painterly soft shading with airbrush transitions (NOT flat cel-shading)
- Strong rim lighting from behind (warm orange/pink backlight)
- Crisp outlines on character edges
- Background: blurred misty mountain landscape with bokeh (deep purple/blue tones)
- Floating particle effects (golden sparks)
- Complementary color scheme: warm gold/orange character vs cool purple/blue background
- Dynamic three-quarter action pose
- High detail on armor textures (brushed metal), fabric, and skin
- Resolution: portrait orientation, full body

Mood: heroic, determined, slightly mischievous expression
```

### GPT-2：赵云（三国·富豪·魔幻觉醒）

```
Create a high-fidelity semi-realistic anime character illustration in the style of premium gacha games like Arknights and Honkai Impact 3rd.

Character: Zhao Yun (赵云), awakened warrior form — a noble young Chinese general with dragon-soul awakening power.

Design details:
- Handsome masculine face, determined expression, sharp features
- Silver eyes with faint dragon-pattern iris glow
- Long silver-white hair tied in a warrior's topknot ( Samurai-style ponytail) with loose strands
- Wearing silver and white plate armor with blue dragon-scale patterns
- White flowing battle cape with golden dragon embroidery
- Holding a gleaming silver longsword (dragon胆 sword) with blue energy aura
- Dragon energy aura: translucent blue dragon silhouette coiling around the blade
- Small floating dragon-shaped energy particles around body

Art style:
- Painterly soft shading with airbrush transitions
- Strong rim lighting from behind (cool cyan/blue backlight)
- Crisp outlines on character edges
- Background: blurred ancient Chinese battlefield at dawn, misty, bokeh (warm gold/orange sunrise tones)
- Complementary color scheme: cool silver/blue character vs warm gold/orange background
- Dynamic confident pose, sword pointed forward
- High detail on armor (polished silver metal), cape fabric texture
- Resolution: portrait orientation, full body

Mood: noble, resolute, heroic guardian
```

### GPT-3：哪吒（封神·侠客·火莲觉醒）

```
Create a high-fidelity semi-realistic anime character illustration in the style of premium gacha games like Arknights and Honkai Impact 3rd.

Character: Nezha (哪吒), fire-lotus awakened form — a young fierce warrior with divine fire abilities.

Design details:
- Youthful androgynous face, fierce determined expression, sharp eyes
- Crimson red eyes with flame-like iris patterns
- Black hair in twin-tops (twin bun style) with red ribbons, some hair strands flaming at tips
- Wearing red and gold armor with lotus-flower motifs (chestplate shaped like lotus petals)
- Arm guards with fire patterns, dark red legwraps
- Two red arm rings (乾坤圈/Universe Rings) floating near shoulders, glowing
- Holding a flaming spear (Fire-Tipped Spear/火尖枪) with orange-red fire trails
- Red sash (红绫/Red Armillary Sash) flowing dynamically around body like ribbons
- Lotus flower energy platform beneath feet, glowing pink-orange

Art style:
- Painterly soft shading with airbrush transitions
- Strong rim lighting (warm orange/gold backlight)
- Crisp outlines on character edges
- Background: blurred lotus pond with fire and embers floating, bokeh (deep red/purple tones)
- Floating fire particles and lotus petal effects
- Complementary color scheme: warm red/orange character vs deep purple/dark background
- Dynamic action pose, mid-leap with spear thrust
- High detail on armor (gold filigree), fire effects
- Resolution: portrait orientation, full body

Mood: fierce, youthful, divine warrior energy
```

### GPT-4：UI主界面

```
Create a mobile card game main UI screen design in the style of premium anime gacha games (like Million Arthur, Arknights, Granblue Fantasy).

Layout:
- Top bar: player info (avatar, level, name), currency icons (gold, gems) with semi-transparent dark blue background
- Left sidebar: vertical icon buttons (Home, Story, Cards, Shop, Settings) with golden frame and blue glow
- Right sidebar: notification bell, friend list, mail icon
- Bottom center: large circular "BATTLE" button in gold with blue energy ring
- Bottom: card deck preview showing 5 card backs in a fan layout

Center: Main character display area showing a full-body character (anime style, standing on a glowing platform)

Background art:
- Mystical floating island or ancient temple ruins with blue energy veins
- Glowing geometric structures floating in background (cyan glow)
- Volumetric light beams from above
- Particle effects: floating blue energy motes
- Color palette: deep navy blue background, cyan/blue energy accents, gold UI elements
- UI frame style: ornate gold borders with blue gem inlays, semi-transparent dark panels
- Overall mood: premium, mystical, inviting

Resolution: 9:16 vertical (mobile portrait), 1080x1920
```

### GPT-5：场景

```
Create a 3D game scene background art in the style of sci-fi fantasy card games.

Scene: An ancient mystical battlefield arena floating in a void — blending Chinese fantasy temple architecture with glowing energy technology.

Elements:
- Central platform: circular tiered stone stage with glowing blue energy lines etched into surface
- Floating geometric structures: fragmented cubes and pyramids suspended in air, with cyan energy veins
- Background: massive ancient stone pillars (Chinese temple style) with glowing energy cracks
- Sky/vault: deep purple-blue gradient void with floating debris and energy particles
- Light source: volumetric god rays from above, illuminating center platform
- Water/energy effect: a stream of glowing blue pixels cascading from floating structures
- Fog: atmospheric volumetric haze at bottom, glowing cyan

Color palette:
- Dominant: deep navy blue (#0a1a3a) to indigo (#1a0a3a)
- Accent: electric cyan (#00ffff) and turquoise (#40e0d0)
- Warm accent: small gold/orange light sources for contrast
- Overall temperature: cool, mysterious, sacred

Style: 3D rendered, stylized realism, slightly painterly post-processing
Resolution: 16:9 landscape, 1920x1080
Mood: epic, vast, otherworldly, ancient power
```

---

## 香蕉提示词（5张）

### 香蕉-1：悟空（西游·侠客·人类化）

```
A high-quality anime game character illustration of Sun Wukong (Monkey King) in humanized warrior form. He is a handsome young male warrior with golden irises, subtle golden facial markings, a golden forehead circlet with orange gem, spiky golden-brown hair, and pointed monkey-ear decorations. He wears golden armor over a dark navy bodysuit with a red flowing scarf. He holds a golden staff diagonally. A monkey tail wraps around his waist. The art style is semi-realistic anime with painterly shading, strong rim lighting in warm orange, and a blurred purple-blue mountain background with floating golden sparks. Dynamic three-quarter action pose, full body, portrait orientation. Premium gacha game art quality.
```

### 香蕉-2：赵云（三国·富豪·魔幻觉醒）

```
A high-quality anime game character illustration of Zhao Yun, a noble Chinese general with dragon-soul awakening. He has silver eyes with dragon-pattern iris glow, silver-white hair in a warrior topknot, wearing silver and white plate armor with blue dragon-scale patterns, and a white cape with golden dragon embroidery. He holds a silver longsword with blue dragon energy aura coiling around it. Floating dragon-shaped energy particles surround him. Semi-realistic anime style with painterly shading, strong cyan rim lighting, blurred ancient battlefield at dawn with warm gold sunrise bokeh. Complementary silver/blue vs gold/orange color scheme. Confident heroic pose, full body, portrait orientation. Premium gacha game art quality.
```

### 香蕉-3：哪吒（封神·侠客·火莲觉醒）

```
A high-quality anime game character illustration of Nezha as a fierce young divine warrior with fire abilities. He has crimson red eyes with flame patterns, black hair in twin buns with red ribbons and flaming tips. He wears red and gold armor with lotus-flower motifs, fire-pattern arm guards, and holds a flaming fire-tipped spear. Two glowing red arm rings float near his shoulders. A red sash flows dynamically around his body like ribbons. A lotus energy platform glows beneath his feet. Semi-realistic anime style with painterly shading, warm orange rim lighting, blurred lotus pond background with floating embers, deep red-purple tones. Dynamic mid-leap action pose with spear thrust, full body, portrait orientation. Premium gacha game art quality.
```

### 香蕉-4：UI主界面

```
A mobile card game main UI screen, vertical 9:16 format, in premium anime gacha game style. Top bar with player avatar, level, and currency icons (gold, gems) on dark blue semi-transparent background. Left sidebar with vertical golden-framed icon buttons. Bottom center has a large gold BATTLE button with blue energy ring. Center shows a full-body anime character on a glowing platform. Background is a mystical floating island with ancient temple ruins, glowing blue energy veins, floating geometric structures, volumetric light beams, and blue energy particles. Color palette: deep navy blue, cyan accents, gold UI elements. Ornate gold borders with blue gem inlays. Mood: premium, mystical, inviting.
```

### 香蕉-5：场景

```
A 3D game scene background of an ancient mystical battlefield arena floating in a void, blending Chinese fantasy temple architecture with glowing energy technology. Central circular tiered stone stage with glowing blue energy lines. Floating fragmented cubes and pyramids with cyan energy veins. Massive ancient Chinese temple stone pillars with glowing energy cracks. Deep purple-blue gradient void sky with floating debris. Volumetric god rays from above. Glowing blue pixel stream cascading. Atmospheric cyan fog at bottom. Color palette: deep navy to indigo, electric cyan and turquoise accents, small warm gold light sources. 3D rendered stylized realism, 16:9 landscape. Mood: epic, vast, otherworldly, ancient power.
```

---

## 换蒙皮技术要点（附注）

| 角色 | 原武器骨骼 | 骨骼数 | 动画引用率 | 新武器处理 |
|---|---|---|---|---|
| 侠客(双匕首+鞘) | swordRoot+scabbardRoot+Bone100+Bone065 | 5 | 100% | 保留骨骼名 |
| 佣兵(大刀) | SwordRoot+Bone001~011+weaponRoot1 | 14 | 98% | 保留骨骼名 |
| 歌姬(吉他) | guitarRoot+weapon1_01~04+weapon2_1~23 | 17 | 82% | 吉他→琵琶换贴图 |
| 富豪(剑) | weaponRoot+gunRoot+bone52~71 | 9 | 100% | 保留骨骼名 |

## 人类化原则

- 悟空：人脸+金色瞳孔+面部金纹+额带。**不做猴脸**
- 八戒：人脸+络腮胡+大耳装饰。**不做猪脸**
- 唐僧/沙僧：纯人形，直接换贴图
- 面部BlendShape保留，只换贴图

## 三方案4主角

| 方案 | 侠客 | 佣兵 | 歌姬 | 富豪 | 工期 |
|---|---|---|---|---|---|
| 封神 | 哪吒(火尖枪) | 杨戬(三尖刀) | 妲己(琵琶) | 姜子牙(打神鞭) | 4周 |
| 西游 | 悟空(金箍棒) | 八戒(钉耙) | 唐僧(锡杖) | 沙僧(宝杖) | 7.5周 |
| 三国 | 张辽(双匕首不改) | 孙策(大刀不改) | 貂蝉(琵琶) | 赵云(剑不改) | 4周 |

---

## 三方案十维度加权评分

| 维度 | 权重 | 封神 | 西游 | 三国 |
|---|---|---|---|---|
| 剧情匹配度 | 15% | 88 | 90 | 85 |
| 角色丰富度 | 10% | 85 | 85 | 95 |
| 超自然元素 | 10% | 100 | 100 | 80 |
| 试炼/关卡感 | 10% | 85 | 95 | 85 |
| 四职业适配 | 5% | 95 | 85 | 95 |
| 国内认知度 | 5% | 90 | 95 | 98 |
| 美术复用率 | 15% | 82 | 80 | 85 |
| 特效适配 | 10% | 85 | 85 | 80 |
| 卡牌适配 | 10% | 85 | 85 | 95 |
| 版权安全性 | 10% | 100 | 100 | 100 |
| **加权总分** | 100% | **89** | **89** | **88** |

---

## 核心概念映射（原IP→三方案）

| 原IP元素 | 封神演义 | 西游人类化 | 魔幻三国 |
|---|---|---|---|
| 环系统 | 封神榜 — 天庭选拔365正神 | 如来佛祖 — 设计取经路线 | 觉醒石系统 — 天降觉醒石选中武将 |
| 巴德尔（希望） | 封神之力/法宝 | 大乘佛法/真经 | 龙魂之力 |
| 霍德尔（绝望） | 妲己/九尾狐 — 迷惑纣王 | 六耳猕猴/心魔 | 魔魂觉醒者 — 被黑暗觉醒石侵蚀 |
| 文明覆灭 | 商朝覆灭 — 纣王无道 | 大唐遭劫/妖魔横行 | 黄巾妖乱 — 张角妖术引发 |
| 法莎莉雅 | 妲己 — 美丽致命，背负使命 | 女儿国国王 | 貂蝉（双重身份）— 表面美人实为守护者 |
| 奥丁 | 元始天尊/鸿钧老祖 | 如来佛祖 | 左慈/于吉 — 神秘仙人旁观嘲讽 |
| 诗嘉古尔 | 申公豹/女娲 | 观音/太上老君 | 南华老仙 — 授张角天书 |
| 帝国 | 商朝+截教 | 天庭/妖王 | 曹魏+妖兽军团 |
| 试炼 | 破阵闯关 — 十绝阵/诛仙阵/万仙阵 | 八十一难 | 战役试炼 — 八阵图=幻境 |
| 文明重启 | 武王伐纣，封神榜完成 | 取得真经 | 三分归晋+觉醒石碎裂 |

---

## 逐章剧情映射

| 原剧情 | 封神演义 | 西游人类化 | 魔幻三国 |
|---|---|---|---|
| 开篇：环之墟 | 女娲降封神令，鸿钧告知此前多次失败 | 观音奉佛旨找取经人，此前多次失败 | 南华老仙铸造觉醒石，此前多次失败 |
| 序章：环的试炼 | 哪吒莲花化身觉醒，太乙真人赐火尖枪 | 悟空五行山解封，观音赐紧箍 | 张辽古战场发现觉醒石，注入龙魂 |
| 第一章：汇合的四人 | 哪吒陆续遇杨戬/妲己/姜子牙，遇土行孙(丹蒂)，第一战破十绝阵 | 悟空收八戒/沙僧，遇土地公(丹蒂)，第一难黑熊精 | 张辽遇孙策/貂蝉/赵云，遇鲁肃(丹蒂)，第一战黄巾妖兵 |
| 第二章：愤怒的巨龙 | 妲己出现妖气弥漫，封神榜触发，元始天尊注意 | 观音现身指引真经，石板触发，元始天尊苏醒 | 貂蝉觉醒倾国之力，传国玉玺触发天命，左慈感知 |
| 第三章：重逢与分别 | 元始天尊vs通天教主，万仙阵爆发，妲己被封印 | 元始天尊vs通天教主，万仙阵爆发 | 左慈vs曹操(魔魂)，妖兽化吕布吞噬貂蝉 |
| 第四章：钢铁的要塞 | 潜入朝歌/截教巢穴，窃听申公豹阴谋，二郎神救援 | 潜入朝歌/截教巢穴，窃听申公豹 | 潜入许昌魏国要塞，窃听南华老仙阴谋，周瑜救援 |
| 第五章：海底迷踪 | 潜入东海/碧游宫，通天教主苏醒，四人被万仙阵吞入 | 潜入东海龙宫，通天教主苏醒 | 潜入赤壁水寨暗道，妖兽化吕布苏醒 |
| 第六章：蛇腹之旅 | 万仙阵幻境：截教门人被屠杀/妖族内斗/百姓灾难。申公豹夺走妲己 | 万仙阵幻境，申公豹夺走妲己 | 八阵图幻境：魏将思乡/黄巾绝望/百姓流离。南华老仙夺走貂蝉 |
| 第七章：猩红之地 | 坠入万妖谷，袁洪(技巧之场)称哪吒为"轮回不知悔改的杀神" | 坠入狮驼岭，大鹏金翅雕称悟空为"轮回不知悔改的妖猴" | 坠入南蛮之地，兀突骨称张辽为"轮回不知悔改的伪善者" |

---

## 全角色映射

### 主角团队

| 原IP角色 | 定位 | 封神 | 西游 | 三国 |
|---|---|---|---|---|
| 侠客 | 敏捷/暗杀 | 哪吒（火尖枪+乾坤圈） | 悟空（金箍棒） | 张辽（双匕首不改） |
| 佣兵 | 力量/近战 | 杨戬（三尖两刃刀） | 八戒（九齿钉耙） | 孙策（大刀不改） |
| 歌姬 | 辅助/治疗 | 妲己（琵琶=吉他换贴图） | 唐僧（锡杖⚠️违和） | 貂蝉（琵琶=吉他换贴图） |
| 富豪 | 防御/财富 | 姜子牙（打神鞭） | 沙僧（降妖宝杖） | 赵云（剑不改） |
| 技巧之场 | 盔甲武士/神秘 | 袁洪 | 大鹏金翅雕 | 兀突骨/祝融 |

### 核心NPC

| 原IP角色 | 定位 | 封神 | 西游 | 三国 |
|---|---|---|---|---|
| 法莎莉雅 | 毁灭妖精/守护者 | 妲己 | 女儿国国王 | 貂蝉（双重身份） |
| 丹蒂 | 工匠/话痨 | 土行孙 | 土地公 | 鲁肃 |
| 斯卡哈 | 导师/严厉 | 太乙真人 | 菩提祖师 | 卢植/水镜先生 |
| 卡拉丁 | 舰船长/豪爽 | 二郎神 | 二郎神 | 周瑜 |
| 乌莎哈 | 助手/认真 | 哮天犬 | 哮天犬 | 吕蒙 |

### 反派阵营

| 原IP角色 | 定位 | 封神 | 西游 | 三国 |
|---|---|---|---|---|
| 奥丁 | 神王/旁白 | 元始天尊/鸿钧老祖 | 如来佛祖 | 左慈/于吉 |
| 诗嘉古尔 | 幕后黑手 | 申公豹/女娲 | 观音/太上老君 | 南华老仙 |
| 冯·阿什 | 副指挥/激进 | 闻仲 | 黄袍怪 | 夏侯惇/张郃 |
| 冯·德·坦恩 | 指挥/骑士精神 | 纣王/通天教主 | 牛魔王 | 曹操（魔魂觉醒） |
| 耶梦加得 | 机械巨蛇/Boss | 蟒蛇精/万仙阵 | 蟒蛇精/万仙阵 | 妖兽化吕布 |
| 魔神 | 终极Boss | 无天佛祖/通天教主 | 无天佛祖 | 黑暗觉醒石本身 |
| 布道队 | 杂兵/烦人 | 截教门人/小妖 | 截教门人/小妖 | 黄巾妖兵/魏国斥候 |

### 怪物体系

| 原怪物 | 封神 | 西游 | 三国 |
|---|---|---|---|
| 巨狼 | 妖狼 | 妖狼/哮天犬野生种 | 妖化战马/妖狼 |
| 巨人 | 巨妖/山神 | 巨妖/山神 | 妖化蛮族巨汉 |
| 机械蛇(耶梦加得) | 蟒蛇精/万仙阵 | 蟒蛇精/万仙阵 | 妖兽化吕布 |
| 黑泥怪物(庇斯特) | 妖气/瘴气怪物 | 妖气/瘴气怪物 | 黄巾妖兵 |
| 机械巨人 | 机关巨人(鲁班术) | 机关巨人 | 妖化战象 |
| 海底怪物 | 水妖/蛟龙 | 水妖/蛟龙 | 赤壁水妖 |

---

## 美术资源盘点

| 资产分类 | 数量 | 路径 |
|---|---|---|
| Player 3D模型 | 36 FBX / 993 anim / 278 tga | Characters\Player |
| Monster 3D | 112 FBX / 1,339 anim / 488 tga | Characters\Monster |
| NPC 3D | 74 FBX / 202 anim / 430 tga(含emotion) | Characters\Npc |
| Boss 3D | 36 FBX / 506 anim / 206 tga | Characters\Boss |
| Qban(Q版) | 27 FBX / 81 anim | Characters\Qban |
| 剧情角色动画 | 5,365 anim / 103角色文件夹 | Characters\Plot |
| 卡牌立绘 | 1,052 PNG | UI\Texture\ImgCard |
| 图标素材 | 964 PNG | UI\Texture\ImgIcon |
| Sprite图集 | 112 | UI\Sprite |
| Spine动画 | 47组 | UI\Spine |
| 场景环境 | 2,105 FBX / 2,025 tga | Environment |
| 特效 | 807 FBX / 1,647 PNG | Effect |
| 过场动画 | 597预制体 | DialogPrefabs |
| 音频 | 1,342文件 | StreamingAssets\Criware |
| 字体 | 56+108文件 | UI\Font |

---

## 美术复用率对比

| 资产分类 | 封神 | 西游 | 三国 |
|---|---|---|---|
| UI系统图集(112) | 90%复用 | 90%复用 | 85%复用 |
| 4主角3D(36) | 纯换贴图 | 换蒙皮(悟空/八戒) | 纯换贴图(武器不改) |
| Monster(112) | 60%复用(改贴图) | 60%复用 | 50%复用 |
| NPC(74) | 改贴图 | 改贴图 | 改贴图 |
| Boss(36) | 改贴图+部分模型 | 改贴图+部分模型 | 改贴图+部分模型 |
| 卡牌立绘(1052) | 重画50% | 重画50% | 重画85% |
| 场景(2105) | 复用60% | 复用60% | 复用30%+改25% |
| 特效(807+1647) | 复用70% | 复用70% | 复用80%(觉醒系统) |
| Spine(47) | 换贴图,骨架留 | 换贴图,骨架留 | 换贴图,骨架留 |
| 过场(597) | 复用70%(改角色引用) | 复用70% | 复用55%+改25% |
| 音频(1342) | 复用50% | 复用50% | 复用45% |
| 字体 | 完全复用 | 完全复用 | 完全复用 |

---

## 歌姬吉他→琵琶兼容性分析

原武器骨骼（实测）：guitarRoot(49/60动画) + weapon1_01~04(48/60) + weapon2_1~23(48/60) + swordRoot(49/60) = **17根骨骼，82%动画引用**

| 方案 | 歌姬角色 | 吉他17骨处理 | 语义兼容 | 违和感 |
|---|---|---|---|---|
| 封神 | 妲己 | 全保留，换武器贴图成琵琶外观 | ✅ 弹琵琶=弹吉他 | 低 |
| 西游 | 唐僧 | 全保留(空骨)，换模型成锡杖 | ❌ 弹锡杖≠弹吉他 | 高 |
| 三国 | 貂蝉 | 全保留，换武器贴图成琵琶外观 | ✅ 弹琵琶=弹吉他 | 低 |

**结论：** 封神和三国都是"吉他→琵琶"，天然完美兼容。琵琶就是乐器，weapon1=琴身，weapon2=琴弦，guitarRoot=琴根。0动画改动。西游的"吉他→锡杖"有语义违和。

---

## 人类化代价对比

| 做法 | 面部表情(430贴图) | 口型同步 | Spine(47组) | 过场(597个) | Q版(27个) |
|---|---|---|---|---|---|
| 人类化(推荐) | ✅保留换贴图 | ✅保留 | ✅保留换贴图 | ✅保留 | ✅保留 |
| 做动物脸(不推荐) | ❌全部废弃 | ❌全部重做 | ❌47组重做 | ❌597个重调 | ❌27个重做 |

**人类化省60-75%工作量。**

---

## 封神影视参考

| 作品 | 年份 | 角色 | 票房/热度 |
|---|---|---|---|
| 《封神第一部：朝歌风云》 | 2023 | 哪吒/杨戬/姜子牙/妲己全员 | 乌尔善导演，大热 |
| 《哪吒之魔童降世》 | 2019 | 哪吒 | 票房50亿+ |
| 《姜子牙》 | 2020 | 姜子牙 | 票房16亿 |
| 《新神榜：杨戬》 | 2022 | 杨戬 | 动画电影 |

---

## 数据来源

### 原始设计文档
- 总梗概：`D:\MA2020\Design\剧情共享文档\2梗概+脚本\5梗概\2023调整后梗概（最初版）序~7章.docx`
- 各章大纲：`D:\MA2020\Design\剧情共享文档\2梗概+脚本\5梗概\23456章剧情梗概（会议讨论基本确定版）\`
- 主线校对版台词：`D:\MA2020\Design\剧情共享文档\2梗概+脚本\1主线\主线校对版\`
- 支线剧情：`D:\MA2020\Design\剧情共享文档\2梗概+脚本\2支线\`

### 游戏内数据
- 剧情文本：`Assets\App\Data\lang\hans\hans_explorestory.json`（63,124行）
- 剧情结构：`Assets\App\Lua\Data\Plot.lua.bytes`（15,702行）
- 皮肤配置：`Assets\App\Lua\Data\Skin.lua.bytes`（weaponPrefab/bodyPrefab映射）
- 模型配置：`Assets\App\Lua\Data\AssetsModel.lua.bytes`（武器预制体路径映射）
- 过场动画：`Assets\DialogPrefabs\`（597个）

### 武器骨骼实测数据
- 侠客(FH01)：`Prefabs\Characters\FH01\FH01_Weapon01_M.prefab` — swordRoot(47/47), scabbardRoot(44/47), Bone100(47/47), Bone065(44/47)
- 佣兵(YB01)：`Prefabs\Characters\YB01\YB01_Weapon01_M.prefab` — SwordRoot(55/59), weaponRoot1(58/59), Bone001~011(58/59), reRoot(58/59)
- 歌姬(GJ01)：`Prefabs\Characters\GJ01\GJ01_Weapon01_M.prefab` — guitarRoot(49/60), weapon1_01~04(48/60), weapon2_1~23(48/60), swordRoot(49/60)
- 富豪(DZ01)：`Prefabs\Characters\DZ01\DZ01_Weapon01_M.prefab` — weaponRoot(60/60), gunRoot(59/60), weapon(60/60), bone52~71(50~58/60)

### 公有领域IP确认
- 封神演义 — 许仲琳·明代·公有领域
- 西游记 — 吴承恩(约1500-1582)·明代·公有领域
- 三国演义 — 罗贯中(约1330-1400)·元末明初·公有领域
- 注意：原著文本/角色名/设定/剧情可自由商用。各现代改编版（影视/动漫/游戏）的美术设计仍有独立版权，使用时需基于原著而非改编版。
