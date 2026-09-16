# AI Investment Workflow Skills

> 六个可独立使用的投资研究工作流，帮助你从“读材料”走到“形成可被验证、也可被推翻的判断”。

## 30 秒看懂

把商业计划书（BP）、访谈纪要或经营数据交给普通 AI 助手，很容易得到一份看似完整的总结，却不一定知道哪些是事实、哪些只是公司口径，真正的投资逻辑又最可能错在哪里。

这套仓库提供六个 Skills（可复用工作步骤），分别处理资料分诊、项目初判、风险、尽调、判断更新和证据审计。它们不替你作出投资决定；人仍负责定义问题、判断证据是否足够、接受什么风险，以及是否采纳最终判断。

适合一级市场投资、产业投资、战略、FA 和公司研究场景。所有示例均为虚构数据。

[从“我该用哪个 Skill”开始](#我该用哪个-skill) · [查看 NovaCompute 中文案例](examples/nova_compute_end_to_end.zh-CN.md) · [查看英文主页](README.md)

## 我该用哪个 Skill？

| 如果你现在遇到的问题是 | 先用哪个 Skill | 它帮你得到什么 |
| --- | --- | --- |
| 材料很多很乱，不知道能信什么 | [资料分诊](skills/source-material-triage/zh-CN/README.md) | 哪些材料能支持什么、彼此是否冲突、还缺什么 |
| 有一份 BP，想快速看懂项目真正赌什么 | [项目初判](skills/primary-market-quick-look/zh-CN/README.md) | 项目本质、投资逻辑候选、最强反方、证伪条件和下一步验证 |
| 已有初判，想知道最可能错在哪里 | [风险雷达](skills/investment-risk-radar/zh-CN/README.md) | 逻辑如何失效、最快验证什么、哪些风险最可能改变判断 |
| 马上要尽调或访谈，不知道问什么最值钱 | [尽调问题地图](skills/dd-question-map/zh-CN/README.md) | 少而关键的问题、材料请求，以及什么答案会改变判断 |
| 新材料来了，想知道判断是否真的改变 | [版本化更新](skills/versioned-investment-update/zh-CN/README.md) | 材料变化、证据变化、判断变化及候选更新 |
| 报告准备流转，担心把推断写成事实 | [证据审计](skills/investment-evidence-audit/zh-CN/README.md) | 证据不足、过度结论、时效冲突和最小改写建议 |

## 第一次怎么用

不需要先理解 AI InvestOS，也不需要安装运行时。

1. **判断手里有什么。** 如果只有一份 BP，先用“资料分诊”标明它是公司口径，再进入“项目初判”；如果来源和边界已经整理清楚，可以直接进入对应 Skill。
2. **把四个文件交给 AI。** 打开对应目录，将 `skill.md`、`input_contract.md`、`output_schema.md`、`quality_checklist.md` 与脱敏材料一起提供给 AI 助手。
3. **要求保留边界。** 输出必须区分事实、公司口径、推断、冲突和未知项，并写清下一步需要验证什么。
4. **由人确认。** AI 可以形成候选判断，但证据是否足够、判断是否采纳，仍由专业人员决定。

一条常见路径是：

```text
资料分诊 → 项目初判 → 风险雷达 → 尽调问题地图
        → 新材料到来后的版本化更新 → 流转前证据审计
```

这不是必须每次完整跑一遍的流水线。你可以只运行当前最需要的 Skill。想看完整示范，可阅读 [NovaCompute 中文教学案例](examples/nova_compute_end_to_end.zh-CN.md)。

## 为什么不能直接让 AI 写“亮点”？

因为投资研究不仅要形成答案，还要管理答案的证据边界。六个 Skills 共同遵循 [统一证据语义](EVIDENCE_SEMANTICS.md)：

1. 公司口径不等于已核验事实。
2. AI 生成的分析不等于来源证据。
3. 文件更新不代表其中说法自动成为当前事实。
4. 不知道的内容要明确保留为“未知”，不能补写。
5. 冲突、例外和是否采纳判断，必须经过人工复核（Human Review）。

## 四种研究状态（Research Modes）

研究状态只帮助你判断从哪里开始，不是四个新 Skills，也不要求先理解某个系统。

| 研究状态 | 你手里的信息 | 怎么开始 |
| --- | --- | --- |
| **无内部材料（Greenfield）** | 基本没有可用内部材料 | 先建立第一版公开证据，再交给资料分诊和项目初判 |
| **已有材料（Material-led）** | 已有 BP、访谈、财务或经营材料 | 从已有材料出发，只围绕关键判断补证或找反证 |
| **深入尽调（Deep DD）** | 已有初判和关键假设或风险 | 用风险雷达和尽调问题地图验证最可能改变判断的证据 |
| **增量更新（Incremental Update）** | 已有历史判断，又收到新材料或新事件 | 用版本化更新区分材料、证据和判断分别发生了什么变化 |

## 专业使用边界

- 每个 Skill 都提供任务说明、输入要求、输出结构和质量检查清单；需要时可继续阅读这些专业文件。
- 人工复核不是免责声明：人要决定证据是否足够、例外是否合理、候选判断是否采纳，以及风险是否可以接受。
- 本仓库提供工作方法，不提供生产级命令行工具、模型接口、自动审批或最终投资决策。

## 两项仍在验证的候选能力

“候选”表示仍需真实场景验证，尚未成为正式 Skill：

- **外部研究与证据构建（External Research & Evidence Build）**：从研究问题出发，寻找并交叉验证公开来源，直到证据足够或应当停止。
- **后续轮与交易研判（Follow-on / Transaction Review）**：区分“公司是否仍值得看好”和“当前交易条件是否值得参与”。

因此正式 Skill 仍然只有 6 个，本仓库也不声称已经具备完整的自动外部研究能力。

## 与 AI InvestOS 的关系

本仓库来自 AI InvestOS 实践，但可以独立使用；它只保留可公开的方法，不包含私有业务代码、模型配置、真实项目资料或项目状态。

## 公开边界

- 所有示例均为虚构或脱敏样例，不对应真实公司、客户、融资、收入、估值或交易。
- 这些 skills 帮助组织资料、判断、风险、DD 问题、版本变化和证据边界。
- 不构成投资建议、证券交易建议、法律、财务或税务意见。
- 不替代专业尽调、人工判断、投委会决策或公司经营决策。
- 不应默认把完整敏感项目资料发送给外部模型。
- 公司口径、访谈纪要和未核验第三方资料必须保留来源标签。
- 任何输出进入正式材料或经营讨论前，都需要适当的人工复核。

## 仓库结构

```text
.
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── CHANGELOG.md
├── RELEASE_CHECKLIST.md
├── EVIDENCE_SEMANTICS.md
├── examples/
│   ├── nova_compute_end_to_end.md
│   └── nova_compute_end_to_end.zh-CN.md
└── skills/
    ├── source-material-triage/
    ├── primary-market-quick-look/
    ├── investment-risk-radar/
    ├── dd-question-map/
    ├── versioned-investment-update/
    └── investment-evidence-audit/
```

每个 Skill 均提供 `skill.md`、输入要求、输出结构（schema）、示例和质量检查清单。

## 引用方式 / How to Reference

推荐使用以下中性引用：

> AI Investment Workflow Skills v0.2.0：一套以一级市场投资研究为主线，用于公司研究、尽调组织、风险映射、版本化更新与证据审计的开源工作流。

引用时应同时说明：

1. 仓库示例全部为虚构数据。
2. skills 用于辅助研究与组织判断，不形成真实投资结论。
3. 核心价值在于工作流、证据纪律和人工复核，而非单次模型回答。

## License

[MIT License](LICENSE)
