---
---
name: signal-pack
name: create-editorial-visual-pack
description: 把 URL、文件或知识点转化为可发布的内容套件，交付 publish-info、可独立发布的 article-draft，以及逐图自包含、可直接生图的 figure-spec。用户要求生成公众号图文、多图轮播、学习笔记、技术解读、工具推荐、开源工具文章、深度项目推荐文章及配图规格时使用。支持可选 Article Evolution，把项目基础文章升级为面向采用决策的推荐文章，并在用户明确要求动态物料时安全交接给 HyperFrames Motion Director。支持手绘卡通信息图与 Halftone Paper-Collage Editorial Assembly System v2，可服从用户指定或自动路由。
description: 把 URL、文件或知识点转化为可发布的内容套件，交付 publish-info、可独立发布的 article-draft，以及逐图自包含、可直接生图的 figure-spec。用户要求生成公众号图文、多图轮播、学习笔记、技术解读、工具推荐、开源工具文章、深度项目推荐文章及配图规格时使用。支持可选 Article Evolution，把项目基础文章升级为面向采用决策的推荐文章，并在用户明确要求动态物料时安全交接给 HyperFrames Motion Director。支持手绘卡通信息图与 Halftone Paper-Collage Editorial Assembly System v2，可服从用户指定或自动路由。
---
---


# Signal Pack
# Editorial Visual Pack


把输入转化为文章、发布信息和可逐张生图的配图任务包。
把输入转化为文章、发布信息和可逐张生图的配图任务包。


## 输入
## 输入


- URL、文件或文字知识点；
- URL、文件或文字知识点；
- 内容类型，可选：学习笔记型 / 工具推荐型 / 教程或报告型；未指定时自动判断；
- 内容类型，可选：学习笔记型 / 工具推荐型 / 教程或报告型；未指定时自动判断；
- 发布平台或场景，可选；
- 发布平台或场景，可选；
- Style，可选：手绘卡通信息图 / Halftone Paper-Collage Editorial Assembly System v2；
- Style，可选：手绘卡通信息图 / Halftone Paper-Collage Editorial Assembly System v2；
- 画幅、语言、图数或覆盖要求，可选。
- 画幅、语言、图数或覆盖要求，可选。


## 开始前必须读取
## 开始前必须读取


1. 读取 [references/output-contract.md](references/output-contract.md)，严格按三产物契约交付。
1. 读取 [references/output-contract.md](references/output-contract.md)，严格按三产物契约交付。
2. 读取 [references/style-router.md](references/style-router.md)，确定覆盖、画幅和 Style。
2. 读取 [references/style-router.md](references/style-router.md)，确定覆盖、画幅和 Style。
3. 只读取所选 Style 的 Profile：
3. 只读取所选 Style 的 Profile：
   - [references/hand-drawn-infographic.md](references/hand-drawn-infographic.md)
   - [references/hand-drawn-infographic.md](references/hand-drawn-infographic.md)
   - [references/halftone-paper-collage.md](references/halftone-paper-collage.md)
   - [references/halftone-paper-collage.md](references/halftone-paper-collage.md)
4. 生成 `figure-spec` 前读取 [references/figure-spec-qa.md](references/figure-spec-qa.md)。
4. 生成 `figure-spec` 前读取 [references/figure-spec-qa.md](references/figure-spec-qa.md)。
5. 处理项目/工具内容时读取 [references/article-evolution-gate.md](references/article-evolution-gate.md)；只有进入升级路径才读取：
5. 处理项目/工具内容时读取 [references/article-evolution-gate.md](references/article-evolution-gate.md)；只有进入升级路径才读取：
   - [references/project-recommendation-article.md](references/project-recommendation-article.md)
   - [references/project-recommendation-article.md](references/project-recommendation-article.md)
   - [references/project-recommendation-qa.md](references/project-recommendation-qa.md)
   - [references/project-recommendation-qa.md](references/project-recommendation-qa.md)
6. 只有用户明确要求动态物料时，才读取 [references/hyperframes-motion-handoff.md](references/hyperframes-motion-handoff.md)。
6. 只有用户明确要求动态物料时，才读取 [references/hyperframes-motion-handoff.md](references/hyperframes-motion-handoff.md)。


## 硬约束
## 硬约束


- 最终只交付 `publish-info`、`article-draft`、`figure-spec`。
- 最终只交付 `publish-info`、`article-draft`、`figure-spec`。
- `article-draft` 是可独立发布的文章和内容事实源，不按图片顺序组织。
- `article-draft` 是可独立发布的文章和内容事实源，不按图片顺序组织。
- `figure-spec` 的每张图都同时包含「参考图片内容」与「配图规格」，且完全自包含。
- `figure-spec` 的每张图都同时包含「参考图片内容」与「配图规格」，且完全自包含。
- 用户指定 Style 时直接服从；未指定时按认知目标与信息关系自动选择并说明理由。
- 用户指定 Style 时直接服从；未指定时按认知目标与信息关系自动选择并说明理由。
- 同一套图默认保持同一 Style 和比例。
- 同一套图默认保持同一 Style 和比例。
- 规格可以压缩、重组文章，但不能新增文章或来源中没有的事实。
- 规格可以压缩、重组文章，但不能新增文章或来源中没有的事实。
- Card Responsibility Brief、事实核查和 Figure Spec QA 都是内部过程，不得作为第四份用户产物。
- Card Responsibility Brief、事实核查和 Figure Spec QA 都是内部过程，不得作为第四份用户产物。
- Article Evolution 只原地升级三产物；Recommendation Brief、Claim Ledger、媒体地图、handoff 与升级 QA 都是内部过程。
- Article Evolution 只原地升级三产物；Recommendation Brief、Claim Ledger、媒体地图、handoff 与升级 QA 都是内部过程。
- 不伪造第一人称体验；只有用户明确提供的真实体验、笔记或结果才能写成作者体验。
- 不伪造第一人称体验；只有用户明确提供的真实体验、笔记或结果才能写成作者体验。
- HyperFrames 不是事实来源。只有用户明确要求动态物料时才建立 handoff，并服从 Motion Director 先 Brief、确认后制作的协议。
- HyperFrames 不是事实来源。只有用户明确要求动态物料时才建立 handoff，并服从 Motion Director 先 Brief、确认后制作的协议。


## 标签体系
## 标签体系


从下列维度选 2–3 个，输出为 `标签：工具推荐 · 开源项目 · 入门友好`：
从下列维度选 2–3 个，输出为 `标签：工具推荐 · 开源项目 · 入门友好`：


- 内容类型：工具推荐 / 学习笔记 / 技术解读 / 行业速递 / 实操教程 / 概念拆解；
- 内容类型：工具推荐 / 学习笔记 / 技术解读 / 行业速递 / 实操教程 / 概念拆解；
- 领域：AI Agent / LLM / 开源项目 / 编程工具 / 开发者生态 / 模型动态；
- 领域：AI Agent / LLM / 开源项目 / 编程工具 / 开发者生态 / 模型动态；
- 受众：入门友好 / 进阶干货 / 开发者必看；
- 受众：入门友好 / 进阶干货 / 开发者必看；
- 格式：多图轮播 / 单图速览 / 系列连载。
- 格式：多图轮播 / 单图速览 / 系列连载。


## 流程
## 流程


### Step 1：消化来源
### Step 1：消化来源


1. 获取 URL 或文件内容；知识点直接处理。
1. 获取 URL 或文件内容；知识点直接处理。
2. 区分来源事实、可验证引用、用户观点与推断。
2. 区分来源事实、可验证引用、用户观点与推断。
3. 提取核心问题、关键主张、数字/公式/限制、适用对象、行动信息和来源链接。
3. 提取核心问题、关键主张、数字/公式/限制、适用对象、行动信息和来源链接。
4. 判断内容类型与发布场景；缺省发布场景按社交媒体多图轮播处理。
4. 判断内容类型与发布场景；缺省发布场景按社交媒体多图轮播处理。


### Step 2：生成 article-draft
### Step 2：生成 article-draft


先写完整文章，再做配图。按主题自然组织为导语、若干章节和必要结尾：
先写完整文章，再做配图。按主题自然组织为导语、若干章节和必要结尾：


- 学习笔记型：问题背景 → 核心概念 → 关键机制 → 理解与连接 → 实践建议；
- 学习笔记型：问题背景 → 核心概念 → 关键机制 → 理解与连接 → 实践建议；
- 工具推荐型：痛点 → 工具定位 → 核心机制/功能 → 差异与限制 → 适用对象与获取方式；
- 工具推荐型：痛点 → 工具定位 → 核心机制/功能 → 差异与限制 → 适用对象与获取方式；
- 教程/报告型：目标与范围 → 主要章节 → 限制/风险 → 结论或步骤。
- 教程/报告型：目标与范围 → 主要章节 → 限制/风险 → 结论或步骤。


文章必须脱离图片独立成立。不得写总图数、图号、逐图文字、构图、色彩或材质。
文章必须脱离图片独立成立。不得写总图数、图号、逐图文字、构图、色彩或材质。


若用户一开始明确要求深度项目推荐文章，直接按 `article-evolution-gate.md` 进入 Article Evolution：补做项目研究与 Claim Ledger，按 `project-recommendation-article.md` 写升级版文章，不先生成基础版。
若用户一开始明确要求深度项目推荐文章，直接按 `article-evolution-gate.md` 进入 Article Evolution：补做项目研究与 Claim Ledger，按 `project-recommendation-article.md` 写升级版文章，不先生成基础版。


### Step 3：规划配图叙事
### Step 3：规划配图叙事


按 `style-router.md` 决定覆盖：
按 `style-router.md` 决定覆盖：


- 社交媒体选择性提炼 4–6 个最值得视觉化的信息点；
- 社交媒体选择性提炼 4–6 个最值得视觉化的信息点；
- 教程或报告覆盖全部主要章节。
- 教程或报告覆盖全部主要章节。


为每张图在内部形成 Card Responsibility Brief：
为每张图在内部形成 Card Responsibility Brief：


- 唯一认知目标；
- 唯一认知目标；
- 核心主张；
- 核心主张；
- 信息关系；
- 信息关系；
- 必需文字；
- 必需文字；
- 主题或项目原生锚点；
- 主题或项目原生锚点；
- 事实与证据边界；
- 事实与证据边界；
- 空白责任。
- 空白责任。


不要把 Brief 输出为独立文件。
不要把 Brief 输出为独立文件。


### Step 4：选择 Style 与画幅
### Step 4：选择 Style 与画幅


1. 用户明确指定时直接采用。
1. 用户明确指定时直接采用。
2. 未指定时按 `style-router.md` 自动选择；理由必须包含认知目标与信息关系。
2. 未指定时按 `style-router.md` 自动选择；理由必须包含认知目标与信息关系。
3. 画幅优先级：用户指定 > 平台要求 > Style 默认。
3. 画幅优先级：用户指定 > 平台要求 > Style 默认。
4. 同一套图默认使用一个 Style 和统一比例。
4. 同一套图默认使用一个 Style 和统一比例。


### Step 5：生成 figure-spec
### Step 5：生成 figure-spec


按 `output-contract.md` 生成。文件开头写明 Style、选择方式、路由理由、发布场景、覆盖策略和统一比例。
按 `output-contract.md` 生成。文件开头写明 Style、选择方式、路由理由、发布场景、覆盖策略和统一比例。


每张图必须重复：
每张图必须重复：


- 实际图上文字；
- 实际图上文字；
- Style 完整名称与版本；
- Style 完整名称与版本；
- 比例和方向；
- 比例和方向；
- 语言；
- 语言；
- 认知目标、核心主张和信息关系；
- 认知目标、核心主张和信息关系；
- 构图机制、视觉锚点、色彩、材质与氛围；
- 构图机制、视觉锚点、色彩、材质与氛围；
- 文字层级、安全区、禁区和事实边界；
- 文字层级、安全区、禁区和事实边界；
- 合并所有约束的完整生图指令。
- 合并所有约束的完整生图指令。


禁止使用“同上”“保持前图风格”“沿用全局设置”等依赖上下文的写法。
禁止使用“同上”“保持前图风格”“沿用全局设置”等依赖上下文的写法。


### Step 6：事实核查
### Step 6：事实核查


有明确原文来源时必须执行严格核查；无来源的知识点也要标记不确定内容，不能把推断写成来源事实。
有明确原文来源时必须执行严格核查；无来源的知识点也要标记不确定内容，不能把推断写成来源事实。


可启动独立 Subagent 读取原文、`article-draft`、`publish-info` 与 `figure-spec`，逐项检查：
可启动独立 Subagent 读取原文、`article-draft`、`publish-info` 与 `figure-spec`，逐项检查：


1. 核心论点是否改变、夸大或弱化；
1. 核心论点是否改变、夸大或弱化；
2. 定理、概念名称和前提是否完整；
2. 定理、概念名称和前提是否完整；
3. 所有数字、范围、上下界与常数是否一致；
3. 所有数字、范围、上下界与常数是否一致；
4. 公式逐字符比对：完全一致为通过，等价变形仍警告，错误为失败；
4. 公式逐字符比对：完全一致为通过，等价变形仍警告，错误为失败；
5. 来源重要论点是否遗漏或误述；
5. 来源重要论点是否遗漏或误述；
6. 三产物是否增加来源没有的主张；
6. 三产物是否增加来源没有的主张；
7. `figure-spec` 的图上文字、视觉关系和证据形态是否造成新误读。
7. `figure-spec` 的图上文字、视觉关系和证据形态是否造成新误读。


每项判断都要附来源证据与终稿对应文本。核查记录可写入临时文件供修订使用，但不得作为第四份用户交付物。修复全部失败项，并明确处理警告项；不得降低公式、数字或事实边界的严格度。
每项判断都要附来源证据与终稿对应文本。核查记录可写入临时文件供修订使用，但不得作为第四份用户交付物。修复全部失败项，并明确处理警告项；不得降低公式、数字或事实边界的严格度。


### Step 7：规格 QA
### Step 7：规格 QA


按 `figure-spec-qa.md` 做逐图和整套检查。发现 `FAIL` 时修正后重检；最终内部结果必须为 `PASS`。这一步只做生图前规格 QA，不生成图片，也不声称完成 Bitmap QA。
按 `figure-spec-qa.md` 做逐图和整套检查。发现 `FAIL` 时修正后重检；最终内部结果必须为 `PASS`。这一步只做生图前规格 QA，不生成图片，也不声称完成 Bitmap QA。


### Step 8：交付
### Step 8：交付


按以下顺序输出且只输出：
按以下顺序输出且只输出：


1. `publish-info`
1. `publish-info`
2. `article-draft`
2. `article-draft`
3. `figure-spec`
3. `figure-spec`


### Step 9：Article Evolution（仅项目/工具内容）
### Step 9：Article Evolution（仅项目/工具内容）


按 `article-evolution-gate.md` 路由：
按 `article-evolution-gate.md` 路由：


- 非项目内容：交付后结束，不出现升级提示；
- 非项目内容：交付后结束，不出现升级提示；
- 项目/工具基础包：三产物交付后只询问一次是否升级；
- 项目/工具基础包：三产物交付后只询问一次是否升级；
- 用户接受：补做研究，原地重写 `article-draft`，同步更新受影响的 `publish-info` 与 `figure-spec`，按 `project-recommendation-qa.md` 修复至 PASS，不再询问；
- 用户接受：补做研究，原地重写 `article-draft`，同步更新受影响的 `publish-info` 与 `figure-spec`，按 `project-recommendation-qa.md` 修复至 PASS，不再询问；
- 用户拒绝或不回应：结束，不追问。
- 用户拒绝或不回应：结束，不追问。


升级文章必须围绕真实读者处境、status quo、可信机制、真实 walkthrough、可观察结果、证据等级、采用成本、前置条件、限制、best-fit、not-fit 与低成本下一步形成自然论证，禁止退化为 README 功能清单。
升级文章必须围绕真实读者处境、status quo、可信机制、真实 walkthrough、可观察结果、证据等级、采用成本、前置条件、限制、best-fit、not-fit 与低成本下一步形成自然论证，禁止退化为 README 功能清单。


只有用户明确要求视频或动态物料时，才按 `hyperframes-motion-handoff.md` 建立媒体地图与标准 handoff，并调用当前可用的 `hyperframes-motion-director`。首次只向用户交付其 `BRIEF_DESIGN_PROPOSAL`；确认前不得生成资产或渲染。能力不可用时报告阻塞，不自行冒充。
只有用户明确要求视频或动态物料时，才按 `hyperframes-motion-handoff.md` 建立媒体地图与标准 handoff，并调用当前可用的 `hyperframes-motion-director`。首次只向用户交付其 `BRIEF_DESIGN_PROPOSAL`；确认前不得生成资产或渲染。能力不可用时报告阻塞，不自行冒充。


## 最小格式示例
## 最小格式示例


```markdown
```markdown
### 📋 publish-info
### 📋 publish-info


**标题**：RAG：让模型先查再答
**标题**：RAG：让模型先查再答
**简介**：从问题、检索到生成，理解 RAG 如何用外部资料减少知识过时与无依据回答。
**简介**：从问题、检索到生成，理解 RAG 如何用外部资料减少知识过时与无依据回答。
**标签**：学习笔记 · LLM · 入门友好
**标签**：学习笔记 · LLM · 入门友好


### 📝 article-draft
### 📝 article-draft


# RAG：让模型先查再答
# RAG：让模型先查再答


RAG 把外部资料引入生成过程……
RAG 把外部资料引入生成过程……


## 为什么需要它
## 为什么需要它
……
……


## 它如何工作
## 它如何工作
……
……


### 🎨 figure-spec
### 🎨 figure-spec


**所选 Style**：Hand-Drawn Cartoon Infographic
**所选 Style**：Hand-Drawn Cartoon Infographic
**选择方式**：自动路由
**选择方式**：自动路由
**路由理由**：因为需要让读者快速理解 RAG 的概念与三步机制，核心信息关系是顺序与概念解释，所以选择手绘卡通信息图。
**路由理由**：因为需要让读者快速理解 RAG 的概念与三步机制，核心信息关系是顺序与概念解释，所以选择手绘卡通信息图。
**发布场景**：公众号多图轮播
**发布场景**：公众号多图轮播
**覆盖策略**：选择性提炼
**覆盖策略**：选择性提炼
**统一比例**：16:9 横版
**统一比例**：16:9 横版


## 图 1
## 图 1


### 参考图片内容
### 参考图片内容
- 主标题：RAG：让模型先查再答
- 主标题：RAG：让模型先查再答
- 副标题：检索增强生成
- 副标题：检索增强生成
- 正文 / 列表：问题 → 检索资料 → 基于资料回答
- 正文 / 列表：问题 → 检索资料 → 基于资料回答
- 强调词 / 数字：先查，再答
- 强调词 / 数字：先查，再答
- 必要署名 / 限制：无
- 必要署名 / 限制：无


### 配图规格
### 配图规格
- Style：Hand-Drawn Cartoon Infographic
- Style：Hand-Drawn Cartoon Infographic
- 画幅：16:9 横版
- 画幅：16:9 横版
- 语言：中文
- 语言：中文
- 本图认知目标：读者理解 RAG 会在回答前查找外部资料。
- 本图认知目标：读者理解 RAG 会在回答前查找外部资料。
- 核心主张：RAG 将检索结果作为生成时的参考。
- 核心主张：RAG 将检索结果作为生成时的参考。
- 信息关系：顺序与概念解释。
- 信息关系：顺序与概念解释。
- 构图与视觉机制：手绘角色先从资料柜取出文档，再递给对话气泡；三步从左到右。
- 构图与视觉机制：手绘角色先从资料柜取出文档，再递给对话气泡；三步从左到右。
- 视觉锚点：资料柜、文档、对话气泡。
- 视觉锚点：资料柜、文档、对话气泡。
- 色彩、材质与氛围：蓝绿主色，轻微纸感，清楚、亲切。
- 色彩、材质与氛围：蓝绿主色，轻微纸感，清楚、亲切。
- 文字规则与安全区：标题独立可读，正文分三段，四周保留 8% 安全区。
- 文字规则与安全区：标题独立可读，正文分三段，四周保留 8% 安全区。
- 禁区与事实边界：不画未经来源支持的准确率数字，不伪造产品截图。
- 禁区与事实边界：不画未经来源支持的准确率数字，不伪造产品截图。
- 完整生图指令：[合并本图全部文字与视觉约束的完整指令]
- 完整生图指令：[合并本图全部文字与视觉约束的完整指令]
```
```


## 用户手动发布
## 用户手动发布


只有用户发回图片并明确要求发布时，才调用已配置的公众号发布能力；发布前向用户展示标题、简介、图片顺序和提交范围。生成三产物本身不授权发布。
只有用户发回图片并明确要求发布时，才调用已配置的公众号发布能力；发布前向用户展示标题、简介、图片顺序和提交范围。生成三产物本身不授权发布。
