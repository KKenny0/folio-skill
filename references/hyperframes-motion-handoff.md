# HyperFrames Motion Handoff

只有用户明确要求视频、动态物料或 Motion Director 时才使用。HyperFrames 是下游传播媒体生产器，不是事实来源。

## 1. 先建立内部媒体地图

只保留值得动态化且可追溯的内容：

- `source phrase`：文章中的原句、名词、动词、数字或张力；
- `mechanism`：值得通过动作解释的真实机制；
- `real product surface`：真实命令、界面、截图、输出、模块或状态；
- `proof artifact`：能够支持判断的第一方资产或可复现产物；
- `CTA`：低成本下一步；
- `forbidden reading`：素材不得暗示的更强结论。

生成场景、概念隐喻和模拟外壳只能承担解释或传播作用。不得用它们证明产品能力、性能、兼容性、界面状态、输出结果或采用数据。

## 2. 标准 handoff

内部 handoff 至少包含：

```yaml
motion_handoff:
  source:
    urls:
    revision:
    researched_at:
  audience:
  recommendation_thesis:
  claim_ids:
    - id:
      class:
      safe_wording:
      required_attribution:
      prohibited_upgrade:
  article_draft:
  source_phrase_map:
  real_assets:
    - asset:
      role: explanation | proof | identity | action
      claim_ids:
      treatment_boundary:
  forbidden_fabrications:
  platform:
  language:
  aspect_ratio:
  candidate_motion_arc:
  cta:
```

`forbidden_fabrications` 至少覆盖：虚构命令、UI、数字、版本、状态、结果、截图、benchmark、stars、兼容性与作者体验。真实资产缺失时明确缺失，不生成“看起来真实”的替代证据。

## 3. 调用边界

1. 调用时读取 `hyperframes-motion-director` 的当前版本，不复制其完整规则到本 Skill。
2. 将 handoff 作为输入，并说明项目事实以 Claim IDs 与 source revision 为准。
3. 首个用户可见的动态产物必须是 Motion Director 的 `BRIEF_DESIGN_PROPOSAL`。
4. 停下等待用户确认；确认前不得生成资产、搭建 composition、snapshot 或 render。
5. 用户确认后，后续生产、验证与交付服从 Motion Director 当前协议。
6. Skill 或连接不可用时明确报告，不自行模拟 Motion Director，也不声称已制作或渲染。

## 4. 一致性检查

- 每个主要动态组件都能指向 source phrase、机制、Claim ID、真实资产或 CTA；
- 动态表达没有强化为 Claim Ledger 禁止的读法；
- proof 角色只由真实、可追溯资产承担；
- handoff 中的文章、平台、语言和比例与三产物一致；
- 未收到用户明确动态请求时，不生成 handoff。
