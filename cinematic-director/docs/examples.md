# 完整案例库 — 已验证的端到端示例

每个案例展示完整流水线：用户输入 → Creative Meeting → 模块产出 → FINAL PROMPT → NEGATIVE PROMPT。
两个案例是本体系的标准参照。

---

# 案例一：月下竹林女侠（Environmental Portrait + Attention）

## 用户输入

> 23岁女侠，气质比较清冷，五官和脸型却不同于气质，有种反差感，比例正常、肤色冷白，右手拿着把剑。女侠看着手中横拿的剑，在竹林中一根竹子10m高的位置踩着（竹林中部高度），天色是暗的但月亮很亮，在这个位置看不到天空，只看得到月亮撒下来的月光。

## 关键判断

- 摄影类型：**Environmental Portrait（环境人像）**——不是拍风景也不是拍人，而是"人物与环境共同构成一个情绪"（《卧虎藏龙》式镜头）
- 这张照片真正拍的是：**人与剑之间那两秒钟的沉默**
- 最大亮点不是"女侠站在竹子上"，而是"月光落在剑身，她低头看剑"——整个 Prompt 围绕 **Attention** 构建
- 摄影目标定位：王家卫 × 李安《卧虎藏龙》× Roger Deakins，而不是国风插画/CG海报/游戏宣传图
- 硬性设定推论：看不到天空 → 月亮不能出现，只能出现月光

## Creative Meeting

```text
Director        这一幕真正拍的是：回忆。她在看剑，不是看镜头。
Story           她刚刚停下脚步。她不是在检查武器，她像是想起了什么。
Cinematographer 85mm，Eye Level，摄影机留在竹林内部。人物占约1/3。不拍天空。
Art Director    颜色限制：jade green, deep emerald, cool moonlit silver, muted charcoal, soft white。
Visual Hook     第一眼：剑（画面最亮处）。第二眼：眼神。第三眼：竹林。
Attention       她的注意力完全属于剑。她从未注意到摄影机。
Mood            安静。压抑。孤独。
```

## 模块要点

**Character DNA**（反差感设计——气质与五官的反差，不是妆容）：

```text
Cool temperament with unexpectedly soft facial features.
Clear almond-shaped eyes that appear gentle rather than cold.
Porcelain-toned skin illuminated by moonlight.
She appears distant, but never arrogant.
The contrast between her calm expression and gentle features creates quiet fascination.
```

**Attention**（本案例的灵魂）：她看剑 = 回忆。若看远方 = 等待；看天空 = 向往。

**Story Moment**（观众大脑自动补故事）：

```text
She has just stopped walking. Her eyes quietly follow the blade instead of looking into the distance.
She is not inspecting the weapon. She seems to be remembering something.
The sword catches a faint strip of moonlight. Time appears suspended.
```

**Photography Strategy**（人物气质"静"→ 摄影策略"静"）：85mm / Eye Level / 摄影机在竹林内部 / 月亮永不出现 / 人物约占1/3。

**Visual Hook**：月光不照脸，照剑——剑成为视觉锚点，画面最亮的物体。

## FINAL PROMPT

```text
This image is approached as a quiet cinematic observation rather than a fantasy illustration or character artwork.

The portrait captures a fleeting moment of contemplation instead of action. Nothing dramatic is happening. The emotional center comes entirely from stillness, silence and attention.

A 23-year-old wandering Chinese swordswoman stands lightly upon a single flexible bamboo stalk nearly ten meters above the forest floor, surrounded completely by an endless sea of towering emerald bamboo. She is suspended within the middle layers of the bamboo forest, where dense bamboo trunks and leaves completely obscure the sky.

Her temperament is calm, distant and restrained, yet her facial features create an unexpected contrast. She possesses gentle almond-shaped eyes, a naturally soft oval face, delicate youthful features and porcelain-cool skin illuminated by moonlight. Her beauty feels effortless rather than glamorous, memorable because of quiet individuality instead of perfection.

She wears a simple flowing white martial robe with elegant practical tailoring. Long black hair is loosely tied, with several strands softly lifted by the mountain breeze. Her proportions are realistic, athletic and balanced from years of martial arts practice.

Her right hand holds a straight Chinese sword horizontally before her chest. The blade catches a single narrow ribbon of cold moonlight. She is not preparing to attack. She quietly watches the reflection upon the blade, completely absorbed in her own thoughts. Her attention belongs entirely to the sword. She never notices the camera.

Only the moonlight enters the forest. The moon itself remains completely hidden above the bamboo canopy. Soft silver light filters naturally through countless layers of bamboo leaves, gently wrapping the scene without revealing its source.

The bamboo forest becomes an enormous natural cathedral of vertical lines. Thousands of bamboo trunks disappear upward into darkness while soft mist separates distant layers. The surrounding environment quietly embraces the subject rather than framing her.

The camera remains inside the bamboo forest using an intimate cinematic perspective with an 85mm lens at eye level. The composition feels discovered rather than staged. The swordswoman occupies roughly one third of the frame while the bamboo continues to dominate the visual rhythm. Negative space and layered depth allow the image to breathe.

Natural atmospheric perspective gently softens distant bamboo. Fine texture remains inside the shadows. Highlights stay restrained. Contrast remains low. Nothing feels artificial or overprocessed.

The color palette is intentionally limited to jade green, deep emerald, cool moonlit silver, muted charcoal and soft white. Colors transition naturally through atmosphere rather than saturation.

Observe her attention before observing her beauty.

Observe the moonlight before observing the sword.

Observe the silence before observing the character.

The portrait feels like the camera has accidentally witnessed a private moment that was never meant to be seen.
```

## NEGATIVE PROMPT

```text
anime, illustration, digital painting, concept art, game splash art, fantasy poster, promotional artwork, wuxia illustration, CGI, Unreal Engine render, overly stylized, beauty advertisement, fashion campaign, glamour photography, magazine cover, influencer aesthetic, selfie, studio portrait, commercial beauty lighting, centered composition, perfect symmetry, hero pose, action pose, fighting pose, sword attack, martial arts choreography, exaggerated movement, flying pose, jumping, energy effects, magical aura, glowing sword, lightning, particles, bloom, lens flare, HDR, oversharpened, excessive clarity, high contrast, oversaturated colors, neon colors, plastic skin, porcelain doll skin, heavy makeup, beauty filter, exaggerated eyelashes, glossy lips, unrealistic anatomy, extra arms, extra hands, missing fingers, fused fingers, duplicated limbs, malformed hands, deformed body, oversized eyes, tiny waist, exaggerated breasts, unrealistic proportions, floating objects, messy bamboo, chaotic composition, visible sky, visible stars, visible clouds, visible moon disc, urban elements, modern clothing, text, watermark, logo
```

注意负向末尾的场景一致性块：`visible sky, visible stars, visible clouds, visible moon disc` 直接来自用户硬性设定"看不到天空"。

## 可替换模块（摄影语言层不变，只换尾部）

```text
Scene    Dense moonlit bamboo forest in early summer.
Moment   She quietly studies the reflection on her sword before continuing her journey.
Emotion  Loneliness, restraint, quiet determination, unspoken memories.
```

换雪山：`Scene: Snow-covered mountain ridge beneath a pale winter moon.`
换海边：`Scene: Rocky coastline beneath drifting sea mist before dawn.`
换修仙：`Scene: Floating bamboo islands suspended above a sea of clouds.`

---

# 案例二：竹海对决（Moment Before + Landscape First）

## 用户输入

> 站在弯曲竹梢上的女侠与一位身着黑衣蓑帽的刺客在苍翠竹海上对峙。两人施展绝顶轻功，在随风弯曲的翠竹顶端追逐交锋，凌空飞舞的身影宛如白鹤掠过竹梢。设计一套摄影团队工作流，找出观众最喜爱的瞬间。

## 关键判断

- 直接写"女侠 VS 刺客在竹林上飞"，AI 99% 会生成：两人飞在空中 + 武器碰撞 + 灵气特效 + 动作 POSE = 游戏宣传图
- 导演决策：不拍"打斗"，拍**"一触即发"**——Anticipation is stronger than Action
- 摄影类型：**Landscape First 的武侠场景**——竹海是主角，对决只是被短暂目击的人类事件
- 最有张力的一帧：两根竹梢被压弯到极限、即将回弹、两人即将交错——**Moment Before（前一秒美学）**

## Creative Meeting

```text
Director        拍"一触即发"，不拍碰撞。刀还没砍出去，比砍出去更有力量。
Story           女侠站在弯曲到极限的竹梢。刺客刚踏上另一根竹子。两竹缓慢回弹。
                下一秒必然相撞。但这一秒，整个世界静止。
Cinematographer 机位距离至少100米，35mm，俯视高位。人物占比 <5%，竹海占90%。
                摄影机不追人物，摄影机观察竹林。
Art Director    颜色：layered greens, soft jade, muted cyan, warm bamboo tones。
Visual Hook     第一眼：一整片绿色竹海。然后才发现：两个极小的人站在两根弯成弓形的竹子顶端（＼○ ○／）。
Mood            全片屏息。寂静比景观重要。
```

## 模块要点

**Photography Strategy**（机位即叙事立场）：

```text
The bamboo forest is the protagonist.
The duel is only briefly witnessed.
The camera quietly observes from a distance.
Human movement should feel weightless against the immense sea of bamboo.
The viewer first notices the bamboo. Only later discovers the duel.
```

**Photographer's Notes**：

```text
Observe the movement of the bamboo before observing the duel.
The bamboo bends more dramatically than the people.
The characters should appear light enough to belong to the wind.
Silence is more important than spectacle.
The moment before impact is the emotional peak.
```

**Director's Observation**：

```text
Nothing has happened yet. The bamboo remembers the wind.
The entire forest seems to hold its breath.
Two lives balance on the last inch before movement.
The silence carries more violence than the coming strike.
```

## FINAL PROMPT

```text
This image is approached as a cinematic observation of stillness before motion rather than an action illustration.

The bamboo forest is the true protagonist. Endless layers of emerald bamboo stretch across the landscape like a living ocean. The duel exists only as a fleeting human event inside an immense natural world.

The emotional center of the image is anticipation rather than combat. Nothing has happened yet. Everything is about to happen.

Two martial artists stand separately upon the flexible tips of two towering bamboo stalks bent deeply by their weight. One is a graceful swordswoman dressed in flowing white robes. The other is a mysterious assassin wearing weathered black garments and a traditional straw hat. Their swords remain lowered. Their bodies remain perfectly balanced. The distance between them is only a few meters.

A gentle mountain wind flows through the bamboo sea. Thousands of bamboo leaves ripple like waves. The bent bamboo slowly rebounds toward one another. The entire forest appears to hold its breath.

The camera watches quietly from a distant elevated position using a natural 35mm cinematic perspective. The figures occupy less than five percent of the frame. The audience first experiences the endless bamboo landscape, then gradually discovers the duel suspended above it.

Large uninterrupted green forms dominate the composition. The curved bamboo creates elegant visual rhythm across the frame. The environment overwhelms the characters. Air, distance and silence become the true subjects.

Natural overcast daylight softly wraps the bamboo canopy. Thin mist gently separates distant layers. Atmospheric perspective gradually dissolves the mountains into pale blue haze. Light belongs to the landscape before touching the characters.

The color palette remains restrained with layered greens, soft jade, muted cyan and warm bamboo tones. Highlights stay delicate. Shadows preserve detail. Nothing feels theatrical.

Observe the bamboo before observing the people. Let the landscape carry the tension. Let silence become the action. The moment before collision is more powerful than the collision itself.
```

## NEGATIVE PROMPT

```text
action pose, sword clash, weapon collision, explosion, energy blast, magical aura, fantasy effects, glowing sword, lightning, excessive particles, flying debris, dramatic combat, exaggerated martial arts pose, superhero pose, game splash art, MMORPG loading screen, promotional poster, concept art, centered composition, character filling frame, close-up portrait, oversized characters, obvious focal point, spectacle, overdesigned scene, HDR, oversharpened, excessive clarity, oversaturated colors, harsh contrast, artificial lighting, dramatic rim light, fake volumetric light, CGI look, digital painting aesthetics, plastic fabric, glossy materials, impossible bamboo geometry, chaotic bamboo density, visual clutter, excessive motion blur, unrealistic perspective, artificial symmetry, busy composition, watermark, logo, text, extra limbs, extra hands, deformed anatomy, malformed fingers, duplicated characters
```

---

# 新案例沉淀格式

生成效果好的案例按以下结构追加到本文件：

```markdown
# 案例N：标题（摄影类型 + 核心原则）
## 用户输入
## 关键判断
## Creative Meeting
## 模块要点
## FINAL PROMPT
## NEGATIVE PROMPT
## 生成验证（使用的模型、效果评价、迭代记录）
```
