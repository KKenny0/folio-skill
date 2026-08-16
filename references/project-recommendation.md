# Project Recommendation

把已核实的项目资料整理成帮助特定读者做采用决策的内容核心，而不是扩写 README。内部 Project Snapshot、Recommendation Brief 与 Claim Ledger 用于派生和核查，不作为用户产物。

## 先建立事实与推荐基础

记录仓库、官网或文档与研究时间；branch、tag、commit、version 或 dated revision；项目形态；第一方来源、真实资产、安装或使用前提、许可和时间敏感状态。

围绕采用决策整理：具体读者及其当前工作流、现状替代方案、`reader pain → credible mechanism → observable outcome`、最强证据、best-fit、not-fit、setup cost、prerequisites、limitations 和最低成本下一步。核心论点必须连接具体处境、可信机制和可观察结果；不要把“强大的 Y 工具”当推荐理由。

为每条决策相关主张建立内部证据分类：

```yaml
- statement:
  class: verified-fact | attributed-source-claim | editorial-judgment
  source:
  revision:
  safe-wording:
  required-attribution:
```

- `verified-fact` 由第一方来源、已检查产物或可复现结果直接支持。
- `attributed-source-claim` 在项目内容中指项目方的说法，发布时保留归因。
- `editorial-judgment` 是基于已列事实的推荐、解释或适配判断。

缺失证据时缩窄或删除主张。不得把重复推断升级为事实，也不得把生成媒体、模拟 UI、虚构命令或示意图当作产品证据。

## 写出真实 walkthrough

内容核心至少包含一个来源支持的真实使用流程：起始输入或用户情境、实际操作或界面路径、项目处理机制、输出形式或可观察变化，以及环境、版本、前置条件和可复现边界。来源只展示拟议流程、局部示例或项目方描述时，明确记录该边界。没有亲自运行，不要写成“我试了”。

## 内容核心要支持的判断

所有派生产物合起来必须帮助读者完成：

1. **Relevance**：它解决谁在什么工作流里的哪种摩擦？
2. **Comprehension**：它通过什么可信机制改变现状，实际使用是什么样？
3. **Trust**：哪些是事实、项目方说法和编辑判断？证据与边界是什么？
4. **Action**：采用成本、前置条件、限制、best-fit、not-fit 和最低成本下一步是什么？

根据项目和读者决策自然组织以下内容，可合并或省略：当前处境、项目定位、可信机制、真实 walkthrough、可观察结果和证据、采用成本、限制、best-fit/not-fit，以及有边界的推荐结论。代表性能力放在真实场景中讲；比较必须说明现状方案，且差异可追溯到来源。

默认社媒套件不要求在单张图或发布正文中完整重复所有组件，但不得省略会改变采用判断的前置条件、成本或限制。整套 `figure-spec` 与 `publish-info` 应共同覆盖 relevance、comprehension、trust 和 action；明确请求文章时，`article-draft` 必须独立完成这四项判断。

## 派生与同步边界

- 不伪造第一人称体验、版本、兼容性、隐私、安全、性能、排名、stars、价格、命令、输出或比较。
- 时间敏感信息记录核查日期或 revision；项目方的性能或效果声明保留归因。
- 推荐结论是有事实基础的编辑判断，不冒充项目事实。
- 明确采用成本、权限、依赖、迁移、许可或时间成本；没有相关成本时说明核查范围，不凭空写“零成本”。
- 内容核心必须记录限制、前置条件、best-fit 与 not-fit，不能只记录优点。
- `publish-info`、可选的 `article-draft` 与 `figure-spec` 都从同一内容核心派生；任一产物不得出现内容核心之外的事实。
- `publish-info` 的来源说明承载对发布判断必要的来源、revision、核查日期和关键不确定性；文章存在时仍保留自己的自然尾注。

## 交付前检查

确认内容核心足以支持 relevance、comprehension、trust、action；包含真实 walkthrough；关键主张有证据分类和安全措辞；成本与边界完整；没有退化为 README 功能清单。再逐项检查用户请求的每个派生产物没有撤回、增强或新增主张。任一项不满足，修订内容核心后重新派生并复检。
