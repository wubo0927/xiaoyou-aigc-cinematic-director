# Template — Portrait（人像）

## 最高原则

> **The person is not the subject. The moment is.**
> 人物不是主体，瞬间才是主体。

人像比风景更需要摄影师思维——AI 太容易把人像做成"美女CG""时尚海报""写真糖水片"。人像 Prompt 不从"人物长什么样"开始，而从**摄影师如何观察这个人**开始。

## 视觉层级（人像版 Hierarchy）

```
Emotion → Light → Environment → Person → Face Detail
```

脸的细节在最后，不在最前。

## 默认摄影策略

```
焦段：85mm
机位：Eye Level
人物占比：30~50%，周围保留呼吸空间
光源：自然窗光 / 阴天漫射光 / 柔和反射光；光先塑空间再照人；最亮处不一定是脸
构图：避免对称、避免居中、负空间有意义、"被发现"而不是"被摆放"
色板：柔和自然色调，颜色跟随光而不是妆容
情绪：安静、亲密但不煽情、克制
姿态：eyes 不直视镜头，姿态自然进行中
```

## 双层结构提醒（商业 × 电影）

单纯的"清水照"没有第一眼吸引力。人物设计要有**辨识度**（见 `modules/character_dna.md`），同时保持电影摄影语言：

```text
A striking young woman with highly recognizable facial features.
Natural asymmetry. Expressive eyes. Elegant facial structure. Healthy skin texture. Graceful posture.
Her appearance immediately attracts attention without feeling artificial.
The portrait is approached as quiet cinematic photography rather than commercial beauty advertising.
The environment and light remain equally important.
```

## Prompt 骨架（Portrait Photographer's Notes）

```text
This image is approached as a quiet cinematic portrait rather than a beauty illustration.

[Intent] The emotional atmosphere carries more importance than physical appearance. The portrait quietly observes the subject instead of presenting perfection. The camera witnesses a fleeting human moment rather than constructing an idealized image.

[Character DNA — 按 modules/character_dna.md 产出填入，含辨识度与反差设计]

[Attention — 她此刻看哪里、为什么]

[Story Moment — 这一秒刚刚发生什么]

[Environment] The subject exists naturally within the surrounding environment. The space gently supports the portrait without disappearing into the background. Negative space remains meaningful, allowing the image to breathe.

[Light] Natural light shapes the portrait before revealing facial features. Soft window light, cloud-diffused daylight, and gentle reflected light create subtle transitions between highlights and shadows. Texture is preserved without harsh contrast or artificial clarity.

[Color] The color palette remains restrained, composed of muted natural tones with soft transitions. Color follows light rather than makeup. Nothing feels overly saturated or visually aggressive.

[Expression] The expression is understated. The posture feels effortless. Hair, clothing and movement respond naturally to the environment. The portrait captures presence rather than performance.

[Composition] The composition feels observed rather than arranged. The subject is not placed as a visual icon but discovered within the frame. Silence, stillness and authenticity become the emotional center of the image.

[Restraints] Avoid spectacle. Avoid glamour. Avoid theatrical beauty. Leave room for ambiguity. Trust natural light. Trust natural posture. Trust quiet observation.
```

## 负向要点

基础通用块 + 人像专用块（重点）：

```text
beauty advertisement, fashion campaign, glamour photography, magazine cover, commercial portrait,
influencer style, instagram aesthetic, selfie, perfect symmetry, centered composition,
beauty pose, model pose, exaggerated expression, forced smile, direct eye contact, seductive pose,
beauty filter, skin smoothing, plastic skin, wax skin, porcelain skin, flawless face, AI face, doll face,
anime face, heavy makeup, exaggerated eyelashes, glossy lips,
dramatic rim light, studio flash, beauty lighting, ring light,
artificial background blur, unrealistic bokeh,
extra limbs, extra hands, missing fingers, fused fingers, malformed hands, unrealistic proportions
```

## 示例（夏日树林 · 甜妹原型）

```text
Attention: She watches the light moving between the leaves, unaware of being seen.
Story Moment: A breeze has just lifted a few strands of her hair. She smiles slightly at nothing in particular.
Photography Strategy: 85mm, eye level, backlit by soft afternoon sun, leaves as natural foreground,
                      she stands slightly off-center, occupying one third of the frame.
Visual Hook: 第一眼——逆光发丝的金边；第二眼——温柔眼神；第三眼——夏日绿色。
```
