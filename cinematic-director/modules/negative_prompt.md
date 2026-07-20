# Module 8 — Negative Prompt 组装规则

## 职责

根据本次的摄影类型、题材和用户硬性设定，组装 Negative Prompt。

详细词库和模型适配见 `docs/negative_prompt.md`，本文件只定义**组装流程**。

## 组装公式

```
NEGATIVE PROMPT =
    基础通用块（四大类：AI味 / 非电影构图 / 光影 / 色彩）
  + 题材追加块（武侠修仙 / 人像 / …）
  + 场景一致性块（由用户硬性设定动态生成）
  + 解剖学基础块（有人物时）
  + 收尾（watermark, text, logo）
```

## 组装步骤

1. **起底**：放入基础通用块（见 `docs/negative_prompt.md` 通用模板，或按目标模型选精简版）
2. **查题材**：武侠/修仙 → 追加"游戏海报风"块；人像 → 追加"写真糖水片"块
3. **翻设定**：逐条检查用户硬性设定和 Creative Meeting 决议，生成一致性负向：
   - "看不到天空" → `visible sky, visible stars, visible clouds, visible moon disc`
   - "没有战斗/对峙前一秒" → `action pose, fighting pose, sword attack, weapon collision, martial arts choreography`
   - "古代场景" → `urban elements, modern clothing`
   - "人物极小" → `character filling frame, close-up portrait, oversized characters, giant character`
   - "低对比静谧" → `harsh contrast, dramatic rim light, theatrical lighting`
4. **解剖学**（有人物时必加）：`extra limbs, extra hands, missing fingers, fused fingers, malformed hands, deformed anatomy, unrealistic proportions, duplicated characters`
5. **收尾**：`watermark, text, logo`
6. **去重**：合并后删除重复词

## 与正向的镜像关系

负向不是独立创作，而是正向决策的镜像。每个重要的正向决策都应有负向保险：

| 正向决策 | 负向镜像 |
|---|---|
| The figures occupy less than 5% of the frame | character filling frame, oversized characters |
| No obvious focal point | centered composition, obvious focal point |
| Highlights remain restrained | blown highlights, HDR, over bloom |
| Restrained palette of layered greens | oversaturated colors, neon colors, rainbow colors |
| Their swords remain lowered | sword clash, action pose, dramatic combat |
| Only moonlight enters the forest | visible moon disc, multiple light sources |

## 输出检查

- [ ] 覆盖四大类（AI味 / 非电影 / 光影 / 色彩）
- [ ] 含题材追加块
- [ ] 用户每条硬性设定都有对应负向
- [ ] 有人物时含解剖学块
- [ ] 无重复词
- [ ] 目标模型不支持负向时，已按 `docs/negative_prompt.md` 转成正向融入句
