---
name: primary-market-quick-look
description: Use when a primary-market investor needs a disciplined quick-look judgment from limited project materials without turning company claims into verified facts.
---

# 一级市场项目初判

## Skill 目标

在资料有限条件下形成有观点、有反方、有证据边界的项目初判，覆盖项目本质、一句话判断、投资逻辑、亮点、反方假设、核心风险、资料缺口和下一步建议。

## 适用场景

- BP-only 或少量资料阶段的首次内部讨论。
- 决定下一轮尽调资源投入前，需要识别真正的核心命题。
- 为 quick look memo 或项目研判简报形成结构化初稿。

## 不适用场景

- 不用于替代完整投资备忘录、估值、法律意见或投委会结论。
- 不用于在没有证据时输出强确定性增长、客户或技术判断。
- 不用于自动决定是否投资、是否进入下一阶段或是否解锁输出。

## 输入要求

资料分诊结果、项目上下文、证据摘录、已知限制和投资团队关注点；输入应尽量带 evidence_id 或材料引用。

执行前必须确认：资料授权范围、敏感等级、版本、提供方、已知缺口，以及哪些内容不能发送给外部系统。

## 输出要求

输出开头应包含 **Executive Snapshot / 5-minute brief**：一句话项目本质、`workflow_status`、当前材料成熟度、3 个初步亮点、3 个关键风险/反方假设、3 个下一步验证重点，以及推荐的下一步 skill。`workflow_status` 只能描述工作流状态，例如 `source-limited quick look`、`ready for risk radar`、`needs more materials before DD question map` 或 `ready for evidence audit before circulation`，不能表达投资建议。

项目本质、一句话判断、投资逻辑、项目亮点、反方假设、核心风险、证据缺口、判断边界和下一步验证优先级。

输出必须区分：事实、公司单方口径、访谈陈述、分析推断、投资观点和信息缺口。

## 证据标签规则

| 标签 | 含义 | 使用要求 |
| --- | --- | --- |
| `user_provided` | 用户直接提供的资料或说明 | 记录材料名称，不自动视为已核验事实 |
| `company_claim` | 公司、创始人或 BP 的单方口径 | 必须标明“公司口径，待交叉验证” |
| `interview_note` | 访谈纪要中的陈述 | 标明访谈对象、日期或版本；不能替代底层材料 |
| `financial_snapshot` | 财务快照、管理报表或模型摘录 | 标明是否审计、口径和期间 |
| `third_party_unverified` | 第三方材料但尚未复核 | 说明来源与未核验状态 |
| `inferred` | 基于现有材料形成的分析推断 | 给出推断链和可能改变判断的条件 |
| `missing_evidence` | 关键证据缺失 | 转化为材料请求或尽调问题 |
| `needs_human_review` | 需要投资团队确认 | 不得自动升级为确定性结论 |


同一陈述可以使用多个标签，但不得以 `needs_human_review` 掩盖缺失证据。

## 禁止性表述

- 不得输出确定性投资推荐、绝对增长判断、验证完成声明或风险清零结论。
- 不得把 `company_claim`、`interview_note` 或 `third_party_unverified` 改写为已核验事实。
- 不得编造客户、收入、融资、财务、估值、技术性能、团队履历或交易条款。
- 不得生成法律、财务、税务或投资决策意见；可提出需专业机构核验的事项。
- 不得替代人工尽调、投资经理判断、投委会决策或项目状态路由。
- 信息不足时必须写明“信息不足，需进一步尽调”，并给出下一步验证动作。


## 处理流程

1. 先解释项目卖的是什么、客户为何购买、价值如何实现。
2. 区分公司叙事与分析者判断，给每条判断绑定证据标签。
3. 提出项目特异的投资逻辑和亮点，不使用空泛行业形容词。
4. 为每条亮点提出反方假设和可能改变判断的条件。
5. 将证据缺口转成下一步材料、访谈或数据验证。
6. 以 judgment boundary 收口，不输出投资决策。

## 输出格式

Markdown memo 或结构化 JSON；默认先给一句话判断，再展开逻辑、亮点、反方、风险和 DD next steps。

优先使用短标题、表格和可执行 bullet；每个重要观点应包含证据边界和可能改变判断的条件。

## 人工复核要求

投资经理必须复核项目本质是否准确、逻辑是否项目特异、证据引用是否越界、反方是否有杀伤力，以及哪些观点可进入正式母稿。

## 与 AI InvestOS 系统模块的对应关系

项目本质研判 → 投资逻辑分析 → 项目亮点分析 → 反方假设 / 核心挑战 → 证据缺口。


## Source References / 来源引用

如条件允许，可用轻量 `source_id` 标注来源，例如文件名、页码、章节、访谈日期或表格 tab。若无法确认来源位置，不得编造 source_id。
