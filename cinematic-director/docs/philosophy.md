# 摄影哲学 — 从"描述画面"到"记录摄影"

这份文档是整个体系的思想根基。所有模块规则、模板、Prompt 语法都从这里推导出来。

## 一、为什么大多数 Prompt 生成的是游戏 CG，不是电影摄影

很多人写 Prompt 的习惯是不断往里面添加内容：

```
8K, masterpiece, best quality, HDR, ultra detailed, cinematic, volumetric lighting
城堡、飞龙、仙人、雷电、灵气、粒子、神光
```

最后得到一张信息量很大的图片——但它像游戏宣传图、概念设计、CG 海报，不像电影摄影。

原因很简单：这些 Prompt 一直在描述**画面里有什么**。

而真正的摄影师思考的是：

> 为什么站在这里拍？为什么不用另一个角度？为什么人物这么小？为什么这里没有任何炫技？

摄影从来不是不断增加元素，而是不断做选择。真正优秀的电影摄影（Roger Deakins、Greig Fraser、Hoyte van Hoytema），大量时间都在决定：**什么不拍。**

## 二、Object List vs Photographer's Notes

**物体清单（Object List）**——AI 最容易收敛成 CG 的写法：

```
一个修仙者
站在悬崖
背后巨大的山
云海
金色阳光
HDR
8K
```

**摄影师笔记（Photographer's Notes）**——本体系的写法：

```
山应该比人物更重要。
人物最好很难第一眼发现。
光应该先照亮地形，而不是人物。
留更多空气。
不要把主体放在画面中心。
不需要强调英雄感。
保持安静。
```

第二种写法里几乎没有任何"物体"，全部都是**摄影决策**。它约束的不是画面元素，而是模型做视觉决策的方式。

> **Prompt 不应该告诉 AI 画什么，而应该告诉 AI 如何看这个世界。电影感恰恰诞生于这种观察方式。**

## 三、三层结构：Intent / Hierarchy / Restraints

Prompt 最核心的结构只有三层。

### 第一层：Intent（摄影意图）

摄影师今天到底想拍什么。不是"有什么"，而是"为什么拍"。

```text
The landscape is the protagonist.
The environment carries the emotion.
The human exists only as a scale reference.
The camera quietly observes rather than glorifies.
```

### 第二层：Hierarchy（视觉层级）

什么重要，什么不重要。谁才是主角。

```text
The mountain dominates the frame.
The sky remains soft and quiet.
The human occupies less than 2% of the frame.
The environment overwhelms the subject.
```

### 第三层：Restraints（摄影限制）

真正电影摄影的大部分工作是"删"：删掉炫技、英雄感、HDR、夸张灯光、中心构图、一眼看懂。留下：留白、空气、沉默、等待。

```text
Do not chase spectacle.
Do not exaggerate scale.
Do not place the subject in the center.
Do not explain everything immediately.
Leave ambiguity. Leave silence. Leave empty space.
Trust the landscape.
```

## 四、拍的是 Moment，不是 Object

Scene 不应该描述物体，而应该描述**世界正在发生什么**：

| 不要写 | 而要写 |
|---|---|
| 一个女孩 | 一个女孩正在等待日出 |
| 一座桥 | 清晨第一缕光照到桥面 |
| 一座山 | 暴雨结束后，云层缓慢翻过山脊 |

人像摄影的最高原则：

> **The person is not the subject. The moment is.**
> 人物不是主体，瞬间才是主体。

风景摄影的最高原则：

> **Landscape is the protagonist.**
> 风景才是主角，人物只是比例尺。

## 五、去中心化（Decentralization）：Discover, not Present

AI 的默认习惯是制造视觉中心：最亮的地方、最大的人物、最清晰的位置。这会自动形成英雄海报。

电影摄影经常反过来：没有明显视觉中心，观众需要慢慢寻找人物、慢慢阅读画面、慢慢理解空间。

所以 Prompt 不应该强调"主体在哪里"，而应该强调**观众如何发现主体**：

```text
The viewer discovers the subject instead of immediately seeing it.
The composition feels observed rather than designed.
No obvious focal point.
Visual weight is distributed naturally across the frame.
```

## 六、Attention（注意力）理论 ★ 本体系独有

电影摄影不是拍"状态"，而是拍**注意力**。摄影师真正记录的，是人物把注意力放在哪里。

同一个女侠拿剑站在竹林里，仅仅改变视线方向，整个故事都会变：

| 她看哪里 | 画面就是 |
|---|---|
| 看远方 | 等待 |
| 看天空 | 向往 |
| 看竹林 | 观察 |
| 看剑 | **回忆** |

注意力直接决定：眼神、构图、光线、视觉锚点，以及观众对这张图的解读方向。这是大多数 AI 生图 Prompt 缺失的一环，也是电影摄影区别于普通插画描述的关键。

典型句式：

```text
Her attention belongs entirely to the sword. She never notices the camera.
Observe her attention before observing her beauty.
```

## 七、Moment Before（前一秒美学）

> **Anticipation is stronger than Action.** 期待，比动作本身更有力量。

不要寻找**最激烈的一帧**，而要寻找**最有张力的一帧**：箭还没射出、剑还没相撞、人物还没转身、暴雨还没落下。观众的大脑会自动补全下一秒，这种参与感比直接展示高潮更强。

竹海对决的例子：不拍两把剑撞在一起，而拍——

```text
女侠站在已经弯曲到极限的竹梢。
刺客刚刚踏上另一根竹子。
两根竹子缓慢向彼此回弹。
下一秒他们一定会相撞。
但是这一秒，整个世界都静止了。
```

```text
The silence carries more violence than the coming strike.
The moment before collision is more powerful than the collision itself.
```

## 八、双层目标：商业吸引 × 电影质感

只有电影质感 → 很舒服，但没有第一眼吸引力（"清水照"）。
只有商业吸引 → 美女 + HDR + 神光 + 大长腿 → 手游海报。

正确做法是两层同时成立：

- **第一层（Hook）**：用户会不会停下来——辨识度、色彩关系、有故事感的姿态、视觉反差
- **第二层（Cinematic）**：停下来以后觉得"这张图为什么这么舒服"——摄影语言

关键区分：**吸引力来自"辨识度"，不是"完美脸"；来自"视觉反差"，不是"感官刺激"。**

```text
A striking young woman with highly recognizable facial features.
Her appearance immediately attracts attention without feeling artificial.
The portrait is approached as quiet cinematic photography rather than commercial beauty advertising.
```

## 九、固定 90% + 变化 10%

整套 Prompt 是一种"摄影风格 DSL"：**摄影语言层永远固定，真正变化的只有最后的场景描述。**

```
① Photography Philosophy（永远固定）
② Camera Language（永远固定）
③ Visual Restraints（永远固定）
④ Scene / Director's Observation（唯一变化）
```

竹林换成雪山，只改一句：

```
Scene: Snow-covered mountain ridge beneath a pale winter moon.
```

整张图的电影语言依然成立。这样既保持统一的摄影语言，又能快速产出大量风格一致但内容丰富的作品。

## 十、一句话总结

> **电影感不是"画质"，而是"摄影语言"。**
> 当 Prompt 从"描述物体"转向"约束决策"，它就不再是在告诉 AI 画什么，而是在告诉 AI 如何看这个世界。
