# Template — Wuxia（武侠）

## 最高原则

> **写意，不写实打斗。** 武侠的电影感来自 Moment Before（前一秒美学）+ Landscape First。
>
> **Anticipation is stronger than Action.** 期待，比动作本身更有力量。

直接写"两人交锋"，AI 99% 会生成：飞在空中 + 武器碰撞 + 灵气特效 + 动作 POSE = 游戏宣传图。

## 核心决策

1. **不拍碰撞，拍一触即发**：刀还没砍出去比砍出去更有力量。最有张力的一帧：竹梢弯到极限、即将回弹、两人即将交错——这一秒整个世界静止
2. **环境是主角**：竹海/雪原/大漠是主体，对决只是被短暂目击的人类事件
3. **人物如白鹤**：轻功的写意感 = 人物轻得属于风，不是肌肉与特效

## 默认摄影策略

```
焦段：35mm natural cinematic perspective
机位：距离≥100米，俯视高位（elevated distant position）
人物占比：<5%（两人对峙）；单人环境人像场景转用 environmental_portrait 模板
光源：自然阴天光/月光，光属于风景先于人物
构图：大面积不间断的绿色/单色块，弯曲竹梢形成优雅视觉韵律，环境压倒人物
色板：layered greens, soft jade, muted cyan, warm bamboo tones（竹海）
情绪：全片屏息、静默比景观重要
```

## Prompt 骨架

```text
This image is approached as a cinematic observation of stillness before motion rather than an action illustration.

[Intent] The [bamboo forest/snowfield/desert] is the true protagonist. The duel exists only as a fleeting human event inside an immense natural world. The emotional center of the image is anticipation rather than combat. Nothing has happened yet. Everything is about to happen.

[Characters — 两个剪影级的人物描述，武器 remain lowered]

[Moment Before] A gentle wind flows through the [environment]. The bent [bamboo] slowly rebounds toward one another. The entire [forest] appears to hold its breath.

[Photography Strategy] The camera watches quietly from a distant elevated position using a natural 35mm cinematic perspective. The figures occupy less than five percent of the frame. The audience first experiences the endless landscape, then gradually discovers the duel suspended above it.

[Composition] Large uninterrupted [green] forms dominate the composition. The environment overwhelms the characters. Air, distance and silence become the true subjects.

[Light] Natural overcast daylight softly wraps the [canopy]. Thin mist gently separates distant layers. Light belongs to the landscape before touching the characters.

[Color] The color palette remains restrained with [layered greens, soft jade, muted cyan]. Highlights stay delicate. Shadows preserve detail. Nothing feels theatrical.

[Observe 收尾] Observe the [bamboo] before observing the people. Let the landscape carry the tension. Let silence become the action. The moment before collision is more powerful than the collision itself.
```

## 负向要点

基础通用块 + 武侠专用块（关键——排除游戏海报风）：

```text
action pose, sword clash, weapon collision, explosion, energy blast, magical aura,
fantasy effects, glowing sword, lightning, excessive particles, flying debris,
dramatic combat, exaggerated martial arts pose, superhero pose,
game splash art, MMORPG loading screen, promotional poster,
centered composition, character filling frame, close-up portrait, oversized characters,
obvious focal point, spectacle, dramatic rim light,
impossible bamboo geometry, chaotic bamboo density,
excessive motion blur, duplicated characters
```

## 完整标准示例

见 `docs/examples.md` 案例二（竹海对决）——本模板的全部规则来自该案例。

## Moment Before 时刻库（武侠场景选帧参考）

```text
两根竹梢被压弯到极限，即将回弹相撞的前一秒
剑已出鞘三寸，尚未完全拔出
两人擦肩而过后背对静止，胜负未明
斗笠边缘刚刚抬起，眼神即将相遇
落叶停在剑锋上方一寸
雨滴悬在屋檐，追逐刚刚停住
```
