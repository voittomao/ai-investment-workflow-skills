# Contributing

感谢你改进 AI Investment Workflow Skills。

## 新增 Skill 的最低标准

新增 skill 应解决可跨项目复用的投研工作流问题，而不是单个项目提示词。提交前请说明：

1. 触发场景是什么。
2. 输入边界和敏感信息边界是什么。
3. 输出如何进入投资分析母稿或后续尽调。
4. 哪些内容必须人工复核。
5. 如何检查证据越界、编造和过度确定性。

## 目录结构

```text
skills/<skill-name>/
├── README.md
├── skill.md
├── input_contract.md
├── output_schema.md
├── example_input.md
├── example_output.md
└── quality_checklist.md
```

`skill-name` 使用小写字母、数字和连字符。

## `skill.md` 必需内容

- Skill 目标
- 适用场景与不适用场景
- 输入与输出要求
- 证据标签规则
- 禁止性表述
- 处理流程
- 输出格式
- 人工复核要求
- 与 AI InvestOS 模块或投资分析母稿的关系

## 示例规则

- 只使用完全虚构或充分脱敏的数据。
- 不使用真实公司、客户、融资、估值、投资人或交易信息。
- 所有业务数字明确标注为虚构样例。
- 示例要体现投资判断、反方假设、信息缺口和下一步验证。
- 不输出确定性投资推荐或自动决策结论。

## 提交前检查

请完成 [RELEASE_CHECKLIST.md](RELEASE_CHECKLIST.md)，并确认新增内容不会把证据纪律变成空心 checklist，也不会用格式替代投资判断。

