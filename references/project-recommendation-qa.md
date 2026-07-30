# Project Recommendation QA

升级路径交付前逐项检查。任一硬门槛失败即为 `FAIL`；修复后重新检查，最终必须为 `PASS`。

## 硬门槛

1. **路由正确**：非项目内容无升级提示；项目基础包恰好一次；明确深度文章直接升级；拒绝或不回应不追问。
2. **仍是三产物**：只交付 `publish-info`、`article-draft`、`figure-spec`；升级提示、Brief、Claim Ledger、媒体地图、handoff 与 QA 记录都不是第四份正式产物。
3. **采用判断完整**：文章能回答 relevance、comprehension、trust、action。
4. **真实 walkthrough**：输入、操作、输出形式、环境/版本或可复现边界齐全；没有虚构体验或结果。
5. **证据分类**：关键主张可区分 `verified-fact`、`attributed-project-claim`、`editorial-judgment`，并保留来源、revision、安全措辞和必要归因。
6. **采用成本**：设置成本、权限、依赖、迁移、许可或时间成本按项目实际情况说明；无相关成本时说明核查范围，不凭空宣称“零成本”。
7. **边界完整**：限制、前置条件、best-fit 与 not-fit 明确；不得只写优点。
8. **不是 README 摘要**：文章按读者决策和真实工作流组织，不是功能、安装、受众清单的扩写。
9. **依赖产物同步**：`publish-info` 与升级文章一致；`figure-spec` 没有保留已撤回主张，也没有新增文章/来源之外的事实。
10. **HyperFrames 安全**：只有用户明确要求动态物料才生成 handoff；生成媒体不被当作事实、证明或真实产品状态；未确认 Motion Director Brief 前不进入资产或渲染。

## 质量评分

每项 0–2 分：

| 维度 | 0 | 1 | 2 |
| --- | --- | --- | --- |
| Relevance | 读者处境不明 | 泛化痛点 | 具体工作流与 status quo 清楚 |
| Comprehension | 只有功能 | 知道类别 | 机制、walkthrough 与结果形式清楚 |
| Trust | 宣传断言无证据 | 部分有边界 | 证据等级、归因、限制完整 |
| Action | 没有下一步 | 只有链接/命令 | 成本、适配与低成本下一步清楚 |
| Editorial value | README 改写 | 有少量判断 | 有边界的推荐论点贯穿全文 |

总分低于 8/10 必须修订；Relevance、Comprehension 或 Trust 为 0 时直接失败。

## FAIL→PASS 反向测试

复制一份已通过样例：

1. 删除限制与 not-fit；
2. 删除或混淆证据分类；
3. 运行本清单，必须因硬门槛 5、7 失败；
4. 还原内容，再检必须 PASS；
5. 保存失败原因、修复项与复检结果。
