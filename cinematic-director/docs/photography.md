# 七维摄影语言 — 电影感的构成

电影感不是"画质"，而是"摄影语言"。本文档定义构成电影感的七个维度，以及每个维度的英文词汇库。

## 电影感黄金公式

写 Prompt 时的注意力分配权重：

```text
20% Camera（摄影机）
25% Composition（构图）
20% Lighting（灯光）
15% Atmosphere（空气感）
10% Color（色彩控制）
 5% Emotion（情绪）
 5% Detail（细节）
```

电影感的决定因素来自镜头语言、构图、光线和空间——而不是分辨率或锐度。

## 一、Camera（摄影机）— 20%

电影首先不是人物，而是摄影机。Prompt 首先描述的不是 `beautiful girl standing`，而是 `low-angle medium-wide shot`。

```text
low-angle shot / eye-level shot / high-angle shot / over-the-shoulder shot
35mm cinema lens / 50mm anamorphic lens / 85mm cinema lens / telephoto compression
wide establishing shot / medium shot / close-up / extreme close-up / extreme long shot
foreground framing / off-center composition / negative space
```

机位选择即叙事立场：

- 拍人像 → 85mm、Eye Level、摄影机在环境内部（intimate cinematic perspective）
- 拍武侠/风景 → 35mm、距离拉远、人物占比压到 10% 以下（the camera watches quietly from a distance）

## 二、Composition（构图）— 25%

电影不会把角色放满整个画面。AI 喜欢人物占 80%；电影通常人物占 20~40%（环境人像）甚至 1~5%（风景/武侠），大量环境。

```text
small character against a vast landscape
off-center composition / rule of thirds
foreground rocks / midground character / background mountains
layered composition / deep spatial composition
leading lines / framed by ruins
environment dominates the frame
large uninterrupted negative space
no obvious focal point
visual weight distributed across the frame
the viewer discovers the subject instead of immediately seeing it
the composition feels observed rather than designed
```

避免：centered composition、perfect symmetry、character filling frame。

## 三、Depth（空间）— 融入构图

电影一定有空间。AI 最容易犯的错误是所有东西贴在一起。

```text
foreground branches / foreground mist
middle-distance character
background mountains
multiple depth layers
strong atmospheric perspective
soft distant silhouettes
depth comes from air rather than blur
the scene breathes through layered space
distance feels physically believable
```

关键原则：**深度来自空气（air），不来自模糊（blur）**。空间比细节重要。

## 四、Lighting（灯光）— 20%

真正电影灯光不是"亮"，而是**有来源**（motivated lighting）。光先照空间，再照人。

```text
motivated lighting / moonlight / sunset backlight / window light / firelight
soft bounce light / diffused skylight / cloud-diffused sunlight
practical lighting / subtle rim light / ambient haze / soft shadow transition
light reveals terrain before revealing people
the brightest area is not necessarily the subject
highlights remain restrained / shadows preserve detail and texture
```

避免：HDR、extreme contrast、overexposed、dramatic rim light、fake god rays、beauty lighting。

光源逻辑必须自洽：说了"看不到天空"，月亮就不能出现，只能出现"月光透过竹叶过滤下来"（soft silver light filters naturally through countless layers of bamboo leaves, gently wrapping the scene without revealing its source）。

## 五、Atmosphere（空气感）— 15%

电影摄影永远有空气。**空气就是电影滤镜。**

```text
thin atmospheric haze / soft fog / mist layers / air particles
dust / humidity / light diffusion / subtle bloom
low visibility in distance / fog layers
atmospheric perspective gradually dissolves the mountains into pale blue haze
thin mist gently separates distant layers
```

## 六、Color（色彩）— 10%

电影不会五颜六色，而是**限制色彩**。一张图的主导色控制在 3~5 种。

```text
muted colors / restricted color palette / restrained palette
cold blue tones / warm highlights / earth tones / subtle teal shadows
desaturated greens / soft neutral colors
natural color transition
Kodak Vision3 color science / ARRI Alexa color response
color follows distance / color follows light rather than objects
colors transition naturally through atmosphere rather than saturation
```

关键原则：**颜色来自空气和光，不来自物体。** 避免：蓝衣服红披风金光紫光各种灵气堆在一起。

示例色板：

- 月下竹林：jade green, deep emerald, cool moonlit silver, muted charcoal, soft white
- 竹海对决：layered greens, soft jade, muted cyan, warm bamboo tones
- 山谷晨光：灰蓝、灰绿、土黄

## 七、Emotion（情绪）— 5%

电影不是动作，而是**动作之前**。

```text
the calm before the storm / quiet tension / pregnant silence
heavy atmosphere / imminent confrontation / restrained emotion
subtle anticipation / loneliness / stillness / weight / dignified presence
quiet / patient / unhurried / observational / silent
heavy without spectacle / immense without exaggeration
stillness becomes the emotion
```

## Detail（细节）— 5%

细节权重最低。不追求"清晰"，追求"真实"：

```text
physically plausible lighting / natural material response
subtle imperfections / filmic exposure / cinematic realism
natural optical depth / realistic spatial compression
fine texture remains inside the shadows
nothing feels artificial or overprocessed
```

## 三个常见误区（本体系的起点）

1. **别再执着 8K。** 越堆 8K/锐度/masterpiece/HDR，图越假。电影感来自把画面"压下来"：低对比、柔和高光、真实薄雾、逻辑自洽的空间关系。
2. **压迫感/史诗感来自构图**，不来自标签：低机位、前后景深度、人物位置、空气雾、阴影里的细节、压低的天空、克制的灯光、大战前的静默。
3. **放下"高清"和 HDR。** 电影感 = 有限色板 + 柔和高光 + 低对比阴影 + 大气深度 + 更小的人物比例 + 空间压缩感。
