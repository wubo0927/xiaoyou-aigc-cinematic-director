# Template — Environmental Portrait（环境人像）

## 定位

电影摄影里完全独立的类别——不是拍风景，也不是拍人，而是：

> **人物与环境共同构成一个情绪。**

《卧虎藏龙》《英雄》《十面埋伏》的许多镜头都属于这一类。当用户输入"人物 + 明确的环境 + 中景"时，大概率是这个类型（不要误判为 Landscape 或 Portrait）。

## 与相邻类型的区分

| | Landscape | Environmental Portrait | Portrait |
|---|---|---|---|
| 主体 | 环境 | 人物与环境共构情绪 | 瞬间（人物承载） |
| 人物占比 | ≤2% | ~1/3（30~40%） | 30~50% |
| 环境角色 | 主角 | 与人物等重 | 有意义的衬托 |

## 默认摄影策略

```
焦段：85mm cinema lens
机位：Eye Level，摄影机在环境内部（intimate cinematic perspective）
人物占比：约1/3，环境保持同等重要
光源：环境的自然光（月光/晨光），光先照注意力对象，光源本体常隐藏
构图："被发现"感，环境"拥抱"人物而不是"框住"人物
深度：浅但可信，背景溶解为分层的环境
色板：3~5种，由环境决定（竹林=玉绿/墨绿/银灰）
情绪：由人物 Attention 与环境共同决定
```

## 核心决策链（标准案例的推导过程）

1. 这张照片真正拍的是什么？→ 不是女侠、不是竹林、不是月亮，而是**人与剑之间那两秒钟的沉默**
2. Attention 是灵魂 → 她看剑（=回忆），月光照剑不照脸，剑成为视觉锚点
3. 遵守空间设定 → 看不到天空，则月亮永不出现，只有被竹叶过滤的月光
4. 环境策略 → 竹林成为"垂直线条的天然大教堂"，环境拥抱人物

## Prompt 骨架

```text
This image is approached as a quiet cinematic observation rather than a fantasy illustration or character artwork.

[Intent] The portrait captures a fleeting moment of [contemplation/waiting/...] instead of action. Nothing dramatic is happening. The emotional center comes entirely from stillness, silence and attention.

[Scene anchor — 人物在环境中的物理位置，具体量化]

[Character DNA — 反差感 + 辨识度，见 modules/character_dna.md]

[Attention — 她看什么、为什么，She never notices the camera]

[Light] Only the [moonlight/morning light] enters the [forest/space]. The [light source] itself remains completely hidden. Soft light filters naturally through [medium], gently wrapping the scene without revealing its source.

[Environment] The [environment] becomes [an enormous natural cathedral of vertical lines / ...]. The surrounding environment quietly embraces the subject rather than framing her.

[Photography Strategy] The camera remains inside the [environment] using an intimate cinematic perspective with an 85mm lens at eye level. The composition feels discovered rather than staged. The subject occupies roughly one third of the frame while the [environment] continues to dominate the visual rhythm.

[Rendering] Natural atmospheric perspective gently softens the distance. Fine texture remains inside the shadows. Highlights stay restrained. Contrast remains low. Nothing feels artificial or overprocessed.

[Color] The color palette is intentionally limited to [3~5 colors]. Colors transition naturally through atmosphere rather than saturation.

[Observe 收尾]
Observe her attention before observing her beauty.
Observe the [light] before observing the [anchor object].
Observe the silence before observing the character.
The portrait feels like the camera has accidentally witnessed a private moment that was never meant to be seen.
```

## 负向要点

基础通用块 + 人像专用块 + 场景一致性块。标准示例（含"看不到天空"设定）：

```text
visible sky, visible stars, visible clouds, visible moon disc,
action pose, fighting pose, sword attack, hero pose,
energy effects, magical aura, glowing sword, lightning, particles,
wuxia illustration, fantasy poster, game splash art,
urban elements, modern clothing
```

## 完整标准示例

见 `docs/examples.md` 案例一（月下竹林女侠）——本模板的全部规则都来自该案例的推导。

## 可替换模块

摄影语言层不变，只换尾部三块：

```text
Scene:   Dense moonlit bamboo forest in early summer.
Moment:  She quietly studies the reflection on her sword before continuing her journey.
Emotion: Loneliness, restraint, quiet determination, unspoken memories.
```
