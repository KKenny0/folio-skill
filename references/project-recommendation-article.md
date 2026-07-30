# Project Recommendation Article Contract

把已核实的项目资料写成帮助特定读者做采用决策的文章，而不是扩写 README。内部记录不作为第四份正式产物。

## 1. 先建立事实与推荐基础

### Project Snapshot

至少记录：

- 仓库/官网/文档与研究时间；
- branch、tag、commit、version 或 dated revision；
- 项目形态：Agent Skill、CLI、库/框架、终端产品、服务、基础设施或内容仓库；
- 第一方来源、真实资产、安装/使用前提、许可与时间敏感状态。

### Recommendation Brief

围绕采用决策记录：

- 具体读者及其当前工作流；
- 真实痛点与现状替代方案；
- reader pain → credible mechanism → observable outcome；
- 核心推荐论点与最强证据；
- best-fit、not-fit、setup cost、prerequisites、limitations、next action。

核心论点必须连接“具体处境—可信机制—可观察结果”。拒绝“X 是一个强大的 Y 工具”式定义。

### Claim Ledger

每条决策相关主张记录：

```yaml
- id:
  statement:
  class: verified-fact | attributed-project-claim | editorial-judgment
  source:
  revision:
  safe-wording:
  required-attribution:
  prohibited-upgrade:
```

- `verified-fact`：第一方来源、已检查产物或可复现结果直接支持；
- `attributed-project-claim`：项目方声称但未独立验证，发布时保留必要归因；
- `editorial-judgment`：基于已列事实的推荐、解释或适配判断。

缺失证据时缩窄或删除主张。不得把重复出现的推断升级为事实，不得把生成媒体、模拟 UI、虚构命令或漂亮示意图当作产品证据。

## 2. 写出真实 walkthrough

至少包含一个来源支持的真实使用流程：

- 起始输入或用户情境；
- 实际操作、命令、界面路径或方法；
- 项目处理机制；
- 输出形式或可观察变化；
- 环境、版本、前置条件和可复现边界。

若来源只展示拟议流程、局部示例或项目方描述，应明确边界。没有亲自运行就不要写成“我试了”；没有真实结果就不要写成成功案例。

## 3. 文章必须完成的读者判断

文章整体必须回答：

1. **Relevance**：它解决谁在什么工作流里的哪种摩擦？
2. **Comprehension**：它通过什么可信机制改变现状，实际使用是什么样？
3. **Trust**：哪些是事实、项目方说法和编辑判断？证据与边界是什么？
4. **Action**：采用成本、前置条件、限制、best-fit、not-fit 和最低成本下一步是什么？

代表性能力应放在真实场景中讲，不写成功能清单。比较必须说明参照的现状方案；差异必须能追溯到来源。

## 4. 自然组织文章

根据项目和读者决策组织章节，不套固定标题。常见叙事组件可按需排序、合并或省略：

- 读者当前处境与 status quo；
- 项目定位与值得关注的转变；
- 可信机制；
- 真实 walkthrough；
- 可观察结果与证据；
- 采用成本、权限、依赖、许可或迁移代价；
- 限制、风险、best-fit 与 not-fit；
- 有边界的推荐结论和低成本下一步。

章节标题必须是自然、可发布的表达，不把 `verified fact`、`not-fit` 或 `Claim Ledger` 当成机械模板标题。证据分类可以在正文中用自然语言显式表达，也可通过引用与措辞区分。

## 5. 写作边界

- 第一人称体验只来自用户明确提供的真实体验、笔记或结果；
- 不编造版本、兼容性、隐私、安全、性能、排名、stars、价格、命令、输出或比较；
- 时间敏感信息附核查日期或 revision；
- 项目方的性能或效果声明保留归因；
- 推荐结论是有事实基础的编辑判断，不冒充项目事实；
- `figure-spec` 只能使用升级文章或原始来源支持的事实。
