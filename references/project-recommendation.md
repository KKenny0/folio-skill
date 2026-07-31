# Project Recommendation

把已核实的项目资料写成帮助特定读者做采用决策的文章，而不是扩写 README。内部 Project Snapshot、Recommendation Brief 与 Claim Ledger 用于写作和核查，不作为第四份正式产物。

## 先建立事实与推荐基础

记录仓库、官网或文档与研究时间；branch、tag、commit、version 或 dated revision；项目形态；第一方来源、真实资产、安装或使用前提、许可和时间敏感状态。

围绕采用决策整理：具体读者及其当前工作流、现状替代方案、`reader pain → credible mechanism → observable outcome`、最强证据、best-fit、not-fit、setup cost、prerequisites、limitations 和最低成本下一步。核心论点必须连接具体处境、可信机制和可观察结果；不要把“强大的 Y 工具”当推荐理由。

为每条决策相关主张建立内部证据分类：

```yaml
- statement:
  class: verified-fact | attributed-project-claim | editorial-judgment
  source:
  revision:
  safe-wording:
  required-attribution:
```

- `verified-fact` 由第一方来源、已检查产物或可复现结果直接支持。
- `attributed-project-claim` 是项目方的说法，发布时保留归因。
- `editorial-judgment` 是基于已列事实的推荐、解释或适配判断。

缺失证据时缩窄或删除主张。不得把重复推断升级为事实，也不得把生成媒体、模拟 UI、虚构命令或示意图当作产品证据。

## 写出真实 walkthrough

至少包含一个来源支持的真实使用流程：起始输入或用户情境、实际操作或界面路径、项目处理机制、输出形式或可观察变化，以及环境、版本、前置条件和可复现边界。来源只展示拟议流程、局部示例或项目方描述时，明确写出该边界。没有亲自运行，不要写成“我试了”。

## 文章要帮读者完成的判断

文章整体必须回答：

1. **Relevance**：它解决谁在什么工作流里的哪种摩擦？
2. **Comprehension**：它通过什么可信机制改变现状，实际使用是什么样？
3. **Trust**：哪些是事实、项目方说法和编辑判断？证据与边界是什么？
4. **Action**：采用成本、前置条件、限制、best-fit、not-fit 和最低成本下一步是什么？

根据项目和读者决策自然组织以下组件，可合并或省略：当前处境、项目定位、可信机制、真实 walkthrough、可观察结果和证据、采用成本、限制、best-fit/not-fit，以及有边界的推荐结论。代表性能力放在真实场景中讲；比较必须说明现状方案，且差异可追溯到来源。不要把证据类别或内部术语当成机械章节标题。

## 写作与同步边界

- 不伪造第一人称体验、版本、兼容性、隐私、安全、性能、排名、stars、价格、命令、输出或比较。
- 时间敏感信息附核查日期或 revision；项目方的性能或效果声明保留归因。
- 推荐结论是有事实基础的编辑判断，不冒充项目事实。
- 明确采用成本、权限、依赖、迁移、许可或时间成本；没有相关成本时说明核查范围，不凭空写“零成本”。
- 文章必须明确限制、前置条件、best-fit 与 not-fit，不能只写优点。
- `publish-info` 与 `figure-spec` 从完成的文章派生并保持同步；后两者不得出现文章外的事实。

## 交付前检查

确认文章完成 relevance、comprehension、trust、action；有真实 walkthrough；关键主张有证据分类和安全措辞；成本与边界完整；文章不是 README 摘要；派生的元数据和配图规格没有撤回或新增的主张。任一项不满足，修订后再交付。
