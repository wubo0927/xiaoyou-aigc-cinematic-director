# Template — Still-Life（静物 / 物品）

## 最高原则

> **电影静物 ≠ 电商产品图。** 拍的是一件物在光里的存在感，不是货架上待售的商品。
>
> **The object is the protagonist, light is the story.** 物是主角，光是叙事。
>
> **仍然拍 Moment，不拍 catalog。** 光刚照到刃、尘埃刚落定、一件旧物被搁下的那一刻——静物也有它的"前一秒"。

直接写"一把剑的产品图"，AI 99% 会生成：白底 + 均匀柔光 + 居中摆正 + 高光锃亮 = 电商 packshot。那是**技术参考板**要的东西（走 libtv-storyboard 的技术配方，不走本 skill）；本模板拍的是**有氛围的电影静物**。

> ⚠ 分流提醒：若目标是"多物件分格、中性背景、均匀布光、形制精确的一致性参考板"（如三视图、道具板），**不要用本模板**——那是技术一致性资产，由 libtv-storyboard 的 reference-assets 直接出 prompt。本模板只管单件（或极少数）物品的电影级静物。

## 核心决策

1. **单一 hero object**：一件物占据情绪中心，其余（案面、器物、背景）只是它的语境。不铺满、不并列展销。
2. **光讲述材质**：侧光/低角掠光起纹理——木的哑、铁的沉、丝的旧、玉的润，靠光的方向说，不靠"高清材质"堆词。
3. **大量暗部与留白**：暗部不必填满，让物从暗里浮出来（discover, not present）。
4. **一种氛围，一个光源**：单一可信光源（窗光/烛光/天光从一侧来），不多打灯。
5. **悬置瞬间**：光刚触到物体的那一秒、尘埃刚落、物刚被搁下——"什么都没发生"本身就是静物的强瞬间。

## 默认摄影策略

```
焦段：85–100mm（近距，轻微压缩，不畸变）
机位：平视或微俯，贴近物体；单件特写或小景
物体占比：hero object 占画面约 1/3–1/2，其余是光、影、留白
光源：单一自然光（窗光/天光/烛光），低角侧光或掠光；光先落在物的一条边/一个面
构图：离心（物不居中）、大面积暗部或空案面、负空间承重
色板：3~5 种，来自物的材质与光色（哑炭灰/旧木褐/冷银/暖烛橘），不靠饱和度
情绪：安静、克制、被时间浸过的物感；不锃亮、不崭新（除非剧情要"新"）
```

## Prompt 骨架

```text
This image is approached as a quiet still-life observation rather than a product shot or e-commerce packshot.

[Intent] A single object is the true protagonist. The image is about how light rests on the object and what the object remembers, not about displaying merchandise. The emotional weight comes from stillness, material and shadow.

[Object Identity — 物的材质身份，非卖点：形制、材质、新旧、岁月痕迹。例：An old straight sword in a matte black lacquered scabbard, its brass fittings darkened with age, entirely without ornament.]

[Light & Material] A single low side light rakes across the object, revealing the grain of the wood, the dull weight of the iron, the faded thread. Light reaches one edge first; the rest falls into soft shadow. Highlights stay restrained — nothing glossy, nothing sparkling.

[Moment] The light has just reached the blade. Dust has just settled. Nothing moves. Time appears suspended.

[Photography Strategy] The camera observes closely with an 85–100mm perspective at eye level, slightly off-center. The object occupies roughly one third to one half of the frame; the surrounding surface, air and shadow carry the rest.

[Composition] Off-center placement. Large areas of quiet surface and untouched darkness. Negative space lets the object breathe. The composition feels discovered on a table, not arranged for sale.

[Color] A restrained palette drawn from the material itself — muted charcoal, aged wood, cold silver, warm candle. Colors come from light and surface, not saturation.

[Observe 收尾] Observe the light before observing the object. Observe the shadow before observing the shape. Let the object sit in silence. Leave the darkness untouched.
```

## 负向要点

基础通用块 + 静物专用块（关键——排除电商/产品目录风）：

```text
product catalog, e-commerce packshot, product photography, white seamless background,
studio softbox, evenly lit, catalog lighting, ring light, glossy reflection, sparkling highlight,
floating object, object centered, hero product shot, advertising, price tag, brand new pristine,
3D render, CGI, game item icon, inventory icon, glossy CG, oversharpened, HDR,
oversaturated colors, multiple objects arranged in grid, orthographic reference sheet
```

> 注：`white seamless background / evenly lit / orthographic reference sheet / multiple objects in grid` 之所以进负向，是因为那些是**技术参考板**的特征——正是本模板要避开的另一条路。

## 示例（祖师剑·窗光木案）

Object Identity + Scene：

```text
An old straight sword rests horizontally on a worn wooden table. The scabbard is matte black lacquer, its brass fittings darkened with age, the hilt wrapped in dark aged cord — heavy, plain, clearly old.

Location: A dim ancestral hall, a corner of a wooden altar table.
Time: Late night.
Light: A single narrow band of cold moonlight falls from a lattice window onto the scabbard, catching one edge; the rest of the table sinks into shadow.
Moment: The moonlight has just crept onto the blade. Dust has settled. Nothing moves.
```

Director's Observation：

```text
The hall is completely still.
Cold light rests on the old scabbard and touches nothing else.
The sword has lain here untouched for a long time.
Nothing dramatic happens.
The object seems to hold a history no one is left to tell.
```

要点回顾：单件剑占画面约 1/3，其余是暗案面与留白；光只从窗棂一侧来，先落剑鞘一条边；色板只有哑黑/旧木褐/冷银月光；拍的是"这把剑在黑暗里被月光碰到的一刻"，不是产品展示。
