# Prompt 语法规范 — 摄影笔记式英文写作

最终 Prompt 一律用英文书写。本文档定义句式、结构、组装顺序和禁用词。

## 一、文体：散文式摄影笔记，不是关键词堆叠

**不要**逗号分隔的关键词流（那是 Object List）：

```text
beautiful girl, bamboo forest, moonlight, sword, masterpiece, 8k, cinematic
```

**要**完整句子构成的摄影笔记，每句都是一个摄影决策或观察：

```text
This image is approached as a quiet cinematic observation rather than a fantasy illustration.
The bamboo forest is the true protagonist.
She quietly watches the reflection upon the blade, completely absorbed in her own thoughts.
```

例外：面向 Midjourney/SDXL 短提示词场景时可压缩为短语流，但语义仍来自模块产出（见 `docs/negative_prompt.md` 的模型适配部分）。

## 二、组装顺序

```
1. Intent              摄影意图（这是什么、不是什么）
2. Hierarchy           视觉层级（谁是主角、占比多少）
3. Attention           人物注意力（有人物时）
4. Photography Strategy 镜头/机位/占比/构图
5. Visual Hook         视觉锚点（最亮处、第一眼）
6. Photographer's Notes 摄影哲学句式（Observe/Trust/Leave）
7. Director's Observation 导演观察（收尾情绪段）
8. Scene Details       场景五要素
9. Rendering Constraints 渲染约束（低对比/克制高光/自然色彩过渡）
```

## 三、开头句式（Intent 定调）

每段 Prompt 的第一句必须先声明"这是什么、不是什么"：

```text
This image is approached as a quiet cinematic observation rather than a fantasy illustration or character artwork.
This image is approached as a cinematic observation of stillness before motion rather than an action illustration.
This image is approached as a quiet cinematic portrait rather than a beauty illustration.
```

## 四、Scene 五要素

场景部分必须拆成五句，不写成一团：

```text
Location    A vast snow-covered alpine basin.
Time        Early winter morning.
Weather     Thin fog drifting between frozen ridges.
Moment      The first sunlight slowly reaches the valley floor.
Human Scale A lone traveler walks across the frozen river.
```

Scene 写"世界正在发生什么"，不写"世界里有什么"：

| Object List（禁止） | Photographer's Notes（要求） |
|---|---|
| A cultivator standing on a cliff. | A mountain ridge disappears into morning fog while a lone cultivator slowly walks along the crest. |
| Snow mountain. | The first sunlight slowly reaches the frozen valley floor. |

## 五、可替换模块设计

Prompt 尾部预留三个可替换模块，摄影语言层（前 90%）永远不变：

```text
=========================
Scene
=========================
Dense moonlit bamboo forest in early summer.

=========================
Moment
=========================
She quietly studies the reflection on her sword before continuing her journey.

=========================
Emotion
=========================
Loneliness, restraint, quiet determination, unspoken memories.
```

换场景只改 Scene 一句：`Snow-covered mountain ridge beneath a pale winter moon.` / `Rocky coastline beneath drifting sea mist before dawn.` / `Floating bamboo islands suspended above a sea of clouds.`

## 六、灵魂句式库

### Observe 句式（分配观众注意力，放在 Prompt 后段）

```text
Observe her attention before observing her beauty.
Observe the moonlight before observing the sword.
Observe the silence before observing the character.
Observe the bamboo before observing the people.
Observe the movement of the bamboo before observing the duel.
```

### 偶然目击感（对抗摆拍）

```text
The portrait feels like the camera has accidentally witnessed a private moment that was never meant to be seen.
She does not notice the camera.
The composition feels discovered rather than staged.
Nothing feels posed. Nothing feels performative.
```

### 环境拟人（建立情绪，不加物体）

```text
The entire forest seems to hold its breath.
The landscape remains indifferent to human presence.
The bamboo remembers the wind.
The surrounding environment quietly embraces the subject rather than framing her.
```

这类句子不增加任何"物体"，却会强烈影响模型的构图倾向、主体比例、情绪和镜头选择。

### Restraints 句式（结尾约束）

```text
Avoid visual spectacle. Avoid heroic presentation. Avoid obvious focal points. Avoid forced drama.
Leave empty space. Leave ambiguity. Leave silence.
Trust the landscape. Trust natural light. Trust quiet observation.
Let the viewer slowly discover the image.
Nothing feels theatrical. Nothing feels staged.
```

## 七、禁用词清单

正向 Prompt 中一律不得出现：

```text
8K, 4K, masterpiece, best quality, ultra detailed, hyper detailed, ultra realistic,
HDR, epic, amazing, stunning, breathtaking, award winning, trending on artstation,
sharp focus, insane detail, extremely detailed, high resolution,
volumetric lighting（作为炫技标签时）, god rays（作为炫技标签时）
```

这些词把模型推向 CG 宣传图数据集。电影感需要的是把画面"压下来"，不是"拉上去"。

## 八、量化表达

占比和距离要具体，不要形容词：

```text
The subject occupies roughly one third of the frame.（环境人像）
The figures occupy less than five percent of the frame.（武侠远景）
The human occupies less than 2% of the frame.（风景）
The camera watches quietly from a distant elevated position.
nearly ten meters above the forest floor
```

## 九、通用 Prompt 骨架（Photographer's Notes Version）

风景/大场景通用模板，实际使用时由模块产出填充：

```text
This image is approached as a quiet cinematic observation rather than a fantasy illustration.

The landscape is the true protagonist. The environment carries the emotional weight. Human presence exists only as a subtle scale reference, never as the visual focus.

The terrain dominates the composition. The sky remains calm and spacious. The subject occupies only a tiny portion of the frame and is discovered gradually instead of presented immediately.

Large uninterrupted shapes define the image. Wide negative space allows the scene to breathe. Visual weight is distributed naturally across the landscape. The composition feels observed rather than designed.

Foreground elements exist naturally without becoming frames. The middle distance carries the narrative. Background forms dissolve softly into atmospheric perspective. Depth emerges through air, haze and distance instead of exaggerated blur.

Natural light gently reveals the terrain before revealing the subject. Clouds soften the sunlight. Highlights remain restrained. Shadows preserve detail and texture. Light belongs to the environment rather than the character.

The color palette is intentionally restrained. Few dominant hues. Muted earth tones. Atmospheric desaturation. Color transitions are gradual and governed by distance and light rather than local object color.

Nothing feels theatrical. Nothing feels staged. The camera quietly witnesses the world. Silence, patience and stillness define the emotional atmosphere. Grandeur emerges from natural scale instead of visual excess.

Avoid visual spectacle. Avoid heroic presentation. Avoid obvious focal points. Avoid forced drama. Leave empty space. Leave ambiguity. Trust the landscape. Let the viewer slowly discover the image.

[Scene — 五要素，唯一变化的部分]
```
