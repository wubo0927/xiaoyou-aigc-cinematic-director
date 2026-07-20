# Module 1 — Character DNA（人物 DNA）

## 职责

定义人物是谁。回答的核心问题不是"她长什么样"，而是：

> **观众第一眼为什么愿意看她？**

## 字段规范

每个人物 DNA 覆盖以下字段：

```
年龄 / 五官 / 脸型 / 体型 / 比例 / 肤色 / 发型 / 气质 / 服装 / 姿态
```

## 设计原则

### 1. 反差感靠气质与五官的反差，不靠妆容

```text
Cool temperament with unexpectedly soft facial features.
Clear almond-shaped eyes that appear gentle rather than cold.
She appears distant, but never arrogant.
The contrast between her calm expression and gentle features creates quiet fascination.
```

这比"高冷脸"高级得多。

### 2. 辨识度 > 完美脸

商业吸引力来自"让人一眼记住"，不是"毫无瑕疵"：

```text
A striking young woman with highly recognizable facial features.
Natural asymmetry. Expressive eyes. Elegant facial structure. Healthy skin texture.
Her appearance immediately attracts attention without feeling artificial.
Her beauty feels effortless rather than glamorous, memorable because of quiet individuality instead of perfection.
```

禁止：perfect face、flawless、doll face——这些直接把模型推向 AI 脸。

### 3. 比例真实

```text
Her proportions are realistic, athletic and balanced from years of martial arts practice.
Normal, athletic proportions.
```

禁止：tiny waist、exaggerated breasts、oversized eyes（这些进负向）。

### 4. 服装讲功能与设计感，不讲华丽

```text
A simple flowing white martial robe with elegant practical tailoring, elegant rather than luxurious.
```

## 好 / 坏对比

| 坏（Object List / AI 脸） | 好（DNA 式） |
|---|---|
| beautiful girl, perfect face, beautiful eyes | Gentle almond-shaped eyes that appear soft rather than cold |
| 23岁、清冷 | 清冷气质 × 柔和五官的反差，让人产生安静的好奇 |
| slim, long legs | Realistic athletic proportions developed through years of practice |

## 人物原型库（可持续扩展）

每种原型给出：气质关键词、五官方向、反差设计、默认摄影策略倾向。使用时以原型为底，按用户需求微调。

### 甜妹（Sweet Girl）

- 气质：治愈、干净、温柔
- 五官：柔和圆润，笑眼，自然唇色
- 反差设计：干净甜美 × 眼神里有一点倔强
- 摄影倾向：柔——85mm 中近景、自然逆光、风吹头发、树叶前景、眼神不直视镜头、光先照头发

### 御姐（Cool Elegance）

- 气质：高冷、克制、有掌控感
- 五官：轮廓利落，眼神冷静，短发或利落束发
- 反差设计：冷峻外表 × 极偶然的一丝疲惫或柔软
- 摄影倾向：硬——85mm 低角度、街灯冷暖对比、建筑压迫感、人物站画面边缘、大量负空间

### 侠女（Swordswoman）

- 气质：清冷、江湖、克制的锋利
- 五官：清冷气质 × 柔和五官的反差（标准案例见 `docs/examples.md` 案例一）
- 反差设计：佩剑的锋利 × 看剑时的温柔
- 摄影倾向：静——85mm Eye Level、环境人像、月光/自然光、人物占1/3

### 女帝（Empress）

- 气质：威仪、孤高、不怒自威
- 五官：端庄大气，眉眼有距离感
- 反差设计：万人之上的威仪 × 独处时的孤独
- 摄影倾向：尺度——低机位仰拍克制使用、大殿/天阶纵深、人物在巨大空间中显小

### 小师妹（Junior Disciple）

- 气质：灵动、天真、未经世事
- 五官：幼态、明亮的眼睛
- 反差设计：天真烂漫 × 某个瞬间的早熟安静
- 摄影倾向：轻——自然光、跟拍感、构图松弛、动作进行中（奔跑回头、踮脚张望）

### 魔女（Enchantress）

- 气质：危险、慵懒、亦正亦邪
- 五官：眼型偏媚，唇色略深
- 反差设计：危险气场 × 漫不经心的优雅
- 摄影倾向：暗——低照度、单一光源、阴影里保留细节、颜色深沉

### 剑仙（Sword Immortal）

- 气质：出尘、萧疏、人剑合一
- 五官：清瘦、眉目疏朗
- 反差设计：仙气 × 风霜感（衣袂陈旧、鬓角微乱）
- 摄影倾向：远——35mm 大远景、人物占比 <5%、云海山巅、Landscape First

### 龙女（Dragon Maiden）

- 气质：神性、疏离、非人感
- 五官：极淡的表情，异色细节点到为止
- 反差设计：神性疏离 × 对人间烟火的一瞬凝视
- 摄影倾向：静水深流——水面/雾气环境、对称打破一角、冷色板

> 扩展方式：新原型直接按上述格式追加。原型只是底稿，具体人物 DNA 必须结合场景重新写成完整英文段落。

## 输出格式（英文段落）

```text
A 23-year-old wandering swordswoman.
Cool temperament with unexpectedly soft facial features.
Clear almond-shaped eyes that appear gentle rather than cold.
A refined oval face with subtle youthful softness.
Porcelain-toned skin illuminated by moonlight.
Long black hair loosely tied, with a few strands moved by the breeze.
A simple white martial robe with practical tailoring, elegant rather than luxurious.
Normal, athletic proportions developed through years of martial arts practice.
She appears distant, but never arrogant.
The contrast between her calm expression and gentle features creates quiet fascination.
```
