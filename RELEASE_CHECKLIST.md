# Release Checklist

发布公开仓库前，逐项确认：

## 数据与敏感信息

- [ ] 不包含任何真实项目名称或可识别项目代号。
- [ ] 不包含真实客户名称、联系人、合同、使用数据或客户清单。
- [ ] 不包含真实融资金额、估值、投资人、股权结构或交易条款。
- [ ] 不包含 API key、访问令牌、Authorization 值、密码或本地绝对路径。
- [ ] 不包含 `data/private/` 或其他私有资料目录内容。

## 投资与专业边界

- [ ] 不存在确定性投资推荐、自动决策或项目状态路由。
- [ ] 不存在绝对增长、验证完成或风险清零式表述。
- [ ] 不提供法律、财务、税务或投委会意见。
- [ ] 明确保留人工尽调、人工复核和投资团队判断。

## 示例与证据纪律

- [ ] 所有案例均明确标注为虚构或脱敏样例。
- [ ] 所有样例数字均标注为虚构样例。
- [ ] 公司单方口径未被改写为已核验事实。
- [ ] 八类证据标签完整：
  - `user_provided`
  - `company_claim`
  - `interview_note`
  - `financial_snapshot`
  - `third_party_unverified`
  - `inferred`
  - `missing_evidence`
  - `needs_human_review`

## 仓库结构

- [ ] 仅包含当前 6 个 workflow skills。
- [ ] 每个 skill 的输入合同、输出 schema、示例和质量检查均存在。
- [ ] `README.md` 中的相对链接可用。
- [ ] `LICENSE` 存在。
- [ ] `CONTRIBUTING.md` 和 `CHANGELOG.md` 存在。
- [ ] Mermaid workflow diagram 可在 GitHub 正常渲染。

