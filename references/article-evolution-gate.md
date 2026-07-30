# Article Evolution Gate

在基础三产物完成后，用本 Gate 判断是否把项目/工具内容升级为采用决策型推荐文章。升级只改变三产物的内容深度，不增加第四份正式产物。

## 路由

| 输入情形 | 行为 |
| --- | --- |
| 非项目/工具内容 | 正常交付三产物；不出现升级提示 |
| 项目/工具内容，用户未要求深度文章 | 正常交付三产物；交付后只询问一次是否升级 |
| 用户接受升级 | 补做项目研究，原地重写 `article-draft`，同步更新受影响的 `publish-info` 与 `figure-spec`；不再询问 |
| 用户拒绝或不回应 | 流程结束；不追问 |
| 用户一开始明确要求深度项目推荐文章/开源工具文章 | 直接进入升级路径；不先生成基础版 |

唯一允许的升级提示：

> 如果你愿意，我可以把这篇基础文章继续升级为面向采用决策的项目推荐文章：补充真实使用流程、证据等级、采用成本、限制与不适用对象，并同步更新配图规格。

这句一次性交互提示不是正式产物。不得换名保存、附加为第四份文件或在用户拒绝后重复出现。

## 升级步骤

1. 读取 [project-recommendation-article.md](project-recommendation-article.md)。
2. 建立内部 Project Snapshot、Recommendation Brief 与 Claim Ledger。
3. 补齐真实 walkthrough、采用成本、前置条件、限制、best-fit、not-fit 与低成本下一步。
4. 原地重写 `article-draft`，保留自然文章结构。
5. 重新检查 `publish-info`；凡标题、简介或标签不再准确，立即更新。
6. 重新生成受影响的 `figure-spec`；只使用升级文章或原始来源支持的事实。
7. 读取 [project-recommendation-qa.md](project-recommendation-qa.md)，修复至 PASS。
8. 仅在用户明确要求动态物料时，读取 [hyperframes-motion-handoff.md](hyperframes-motion-handoff.md)。

## 不升级的情形

- 主题不是具体项目、工具、Skill、CLI、库、框架、产品、服务或基础设施；
- 来源不足以支持采用判断，且无法继续核实；
- 用户只需要摘要、学习笔记、技术解释或当前三产物；
- 用户已经拒绝，或没有回应唯一一次升级提示。

来源不足时保留基础文章，明确事实边界；不得用推断、生成画面或宣传措辞填补证据空缺。
