# Template — City（城市）

## 最高原则

> **城市是有态度的环境，不是背景板。**
> 城市人像 = 人物与城市空间的关系（压迫/庇护/疏离/归属），城市风景 = 城市本身的呼吸。

## 两个子类型

### A. 城市夜景人像（御姐原型的主场）

```
焦段：85mm
机位：低角度
人物占比：20~30%，站在画面边缘
光源：街灯/橱窗光/霓虹反光——全部是 practical lighting（画面内真实光源）
构图：建筑体量制造压迫感，大量负空间
色板：冷暖对比（钠灯暖橙 × 夜色冷蓝），但饱和度克制，不是赛博朋克
情绪：疏离、清醒、独自与城市对视
```

Hook 参考：黑白反差、冷眼神、城市灯光、轮廓光（克制）。

### B. 城市街头/风景（Street）

```
焦段：35mm / 50mm
机位：Eye Level，旁观者位置
人物占比：行人作为城市的比例尺与生命迹象
光源：自然光/雨后反光/清晨斜光
构图：街道纵深、建筑韵律、偶然感
情绪：城市在人到来之前就存在，在人离开之后继续
```

## Prompt 骨架（夜景人像）

```text
This image is approached as a quiet cinematic night portrait rather than a fashion editorial.

[Intent] The relationship between the woman and the city is the true subject. The city carries the emotional weight of distance and solitude. The portrait observes rather than glamorizes.

[Character DNA — 辨识度设计，见 modules/character_dna.md 御姐原型]

[Attention] She watches the passing traffic lights, not the camera. Her thoughts belong to somewhere else.

[Story Moment] She has just stepped out of a late meeting. The street has gone quiet. She pauses under the streetlight for a moment before walking on.

[Photography Strategy] 85mm cinema lens from a slightly low angle. She stands near the edge of the frame, occupying about one quarter of it. The architecture rises above her, creating gentle pressure. Large negative space dominates the composition.

[Light] All light comes from real sources within the scene: streetlights, shop windows, distant traffic. Warm sodium light meets the cool blue of the night. Highlights remain restrained. Shadows keep their texture.

[Color] A restrained palette of warm amber, deep blue night tones and neutral grays. No neon excess. Color belongs to the light sources, not to decoration.

[Restraints] Avoid fashion posing. Avoid glamour lighting. Avoid cyberpunk saturation. Nothing feels staged. The city remains slightly indifferent to her presence.

[Scene 五要素 + Director's Observation]
```

## 负向要点

基础通用块 + 人像专用块 + 城市特有：

```text
cyberpunk, neon overload, oversaturated neon colors, blade runner aesthetics,
fashion editorial, glamour lighting, studio flash, beauty lighting,
empty sterile street, fake wet ground reflections everywhere,
lens flare overload, bokeh overload,
modern fantasy effects, light trails everywhere
```

（古装/年代感城市另加：`modern vehicles, contemporary clothing, plastic signage` 的镜像调整）

## 示例（雨后清晨街头 · Street 子类型）

Scene 五要素：

```text
Location: A narrow old street lined with low buildings and tangled overhead wires.
Time: Just after sunrise.
Weather: The rain has stopped; the pavement is still dark and reflective.
Moment: The first shopkeeper rolls up the metal shutter while steam rises from a breakfast stall.
Human Scale: A girl with an umbrella still folded walks slowly through the long shadows.
```

Director's Observation：

```text
The street is waking up slowly.
Steam drifts across the morning light.
The city does not perform for anyone.
She walks through it as if through her own memory.
Nothing dramatic happens.
The morning continues with or without being seen.
```
