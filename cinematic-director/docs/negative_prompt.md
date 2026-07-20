# Negative Prompt 规范 — 排除一切"像 AI"的特征

负向提示词的思路与正向一致：**不是一味排除低质量，而是排除一切会让画面变得像 AI、CG、插画、游戏宣传图的特征。**

核心思想一句话：

> 排除一切"像 AI 绘画、像游戏宣传图、像 CG 海报"的视觉特征。

## 一、四大类组织法

按**问题来源**组织负向提示词，而不是无限堆砌单词。

### ① AI 味（Artificial Look）

```text
HDR, oversharpened, overprocessed, CGI, game render, digital painting,
plastic skin, wax skin, artificial lighting, glossy materials,
Unreal Engine render, octane render, 3D render, concept art, illustration, anime, matte painting
```

### ② 电影摄影禁忌（Non-cinematic）

```text
centered composition, character filling frame, poster composition,
flat perspective, no foreground, no atmosphere, empty background,
close-up portrait（远景场景时）, symmetrical composition, hero shot, hero pose,
obvious focal point, subject dominating frame, forced cinematic angle
```

### ③ 光影问题（Lighting）

```text
multiple light sources, fake rim light, harsh shadows, overexposed,
blown highlights, crushed blacks, over bloom, fake god rays,
fake volumetric light, theatrical lighting, studio flash, beauty lighting, ring light
```

### ④ 色彩问题（Color）

```text
oversaturated, neon colors, rainbow colors, high contrast,
extreme color grading, vivid colors, artificial color grading
```

## 二、通用模板（Cinematic Negative Prompt 完整版）

```text
HDR, extreme HDR, overprocessed, oversharpened, ultra sharp, excessive clarity, hyper detailed skin, crispy details, artificial details, overexposed, underexposed, blown highlights, crushed blacks, harsh contrast, excessive saturation, oversaturated, neon colors, vibrant colors, glowing edges, bloom overload, lens flare overload, fake volumetric light, unrealistic lighting, flat lighting, studio lighting, beauty lighting, inconsistent light source, multiple light directions, washed out colors, plastic skin, wax skin, CGI look, game render, unreal engine look, 3D render, octane render, concept art, digital painting, illustration, anime, comic, matte painting, poster composition, centered composition, symmetrical composition, character filling the frame, floating subject, floating objects, no foreground, no background separation, shallow environment, cluttered composition, busy background, visual chaos, no haze, no depth, flat perspective, unrealistic scale, giant character, oversized subject, perfect symmetry, excessive glow, excessive particles, overdone effects, energy overload, overdesigned costume, glossy materials, plastic fabric, fake reflections, artificial textures, unrealistic shadows, noisy image, low quality, blurry, watermark, text, logo, duplicate objects, extra limbs, bad anatomy, deformed hands, malformed fingers, cropped body
```

## 三、精简版（Midjourney / Flux / SDXL）

```text
HDR, oversharpened, overprocessed, excessive contrast, oversaturated, artificial lighting, CGI, game render, digital painting, illustration, poster, centered composition, close-up portrait, character filling frame, flat lighting, no atmosphere, no depth, fake volumetric light, plastic skin, glossy materials, unrealistic shadows, cluttered composition, excessive particles, glowing edges, neon colors, blurry, watermark, text, logo, bad anatomy, extra limbs
```

Midjourney 写法：`--no HDR, oversharpened, CGI, game render, digital painting, poster, centered composition, ...`

## 四、按题材追加块

### 修仙/武侠专用（排除"游戏海报风"）

```text
overpowered aura, excessive energy effects, too many particles, explosion everywhere,
floating magic circles, over glowing weapon, super bright spiritual energy, flashy effects,
rainbow colors, neon lighting, fantasy wallpaper, mobile game splash art,
MMORPG loading screen, poster art, key visual, cover illustration,
character occupying entire frame, hero pose, dynamic action pose,
flying toward camera, camera facing character directly, perfect centered framing
```

### 人像专用（排除"写真糖水片"）

```text
beauty advertisement, fashion campaign, glamour photography, magazine cover,
commercial portrait, influencer style, instagram aesthetic, selfie,
beauty pose, model pose, exaggerated expression, forced smile, direct eye contact,
seductive pose, beauty filter, skin smoothing, flawless face, AI face, doll face,
heavy makeup, exaggerated eyelashes, glossy lips,
unrealistic anatomy, extra arms, extra hands, missing fingers, fused fingers,
duplicated limbs, oversized eyes, tiny waist, exaggerated breasts, unrealistic proportions
```

### 场景一致性追加（按用户硬性设定动态生成）

用户设定"看不到天空" → 追加：

```text
visible sky, visible stars, visible clouds, visible moon disc
```

用户设定"没有战斗" → 追加：

```text
action pose, fighting pose, sword attack, martial arts choreography, exaggerated movement, flying pose, jumping
```

## 五、自然语言概括句（放在负向末尾）

对支持自然语言理解的模型（Flux、GPT Image、部分 SDXL），在负向末尾加一句概括，比堆几十个同义词更有效：

```text
non-cinematic, artificial AI aesthetics, game splash art, promotional poster style, exaggerated visual effects, unrealistic composition, synthetic digital look
```

## 六、模型适配

| 模型 | 负向支持 | 用法 |
|---|---|---|
| SDXL / SD 系 / ComfyUI | 独立 Negative 字段 | 用完整版四类模板 + 题材追加块 |
| Flux | 部分支持（视工作流） | 完整版或精简版；支持自然语言概括句 |
| Midjourney | `--no` 参数 | 精简版，去掉空格敏感的长短语 |
| 即梦 / 豆包 / 可灵 | 多数不支持独立负向 | 见下方"融入正向"写法 |
| GPT Image / Gemini | 不支持独立负向 | 见下方"融入正向"写法 |

### 不支持负向提示词的模型：把"避免项"融入正向

把负向核心压缩成 2~4 句自然语言，接在正向 Prompt 结尾：

```text
The image must not look like CGI, game art, digital painting or a promotional poster. Avoid HDR, oversaturated colors, plastic skin, theatrical lighting and centered heroic composition. The result should feel like restrained cinematic photography captured on real film, with soft highlights, low contrast and natural atmosphere. No text, no watermark.
```

正向 Prompt 中的 Restraints 层（Avoid spectacle... Trust the landscape...）本身已经承担了大部分负向职能，这也是本体系对这类模型天然兼容的原因。
