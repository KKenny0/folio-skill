<div align="center">

# Folio

**把来源变成可发布文稿和可直接进入视觉生产的配图规格。**

[English](README.md) · [案例](#showcase) · [安装](#安装) · [常见问题](#常见问题)

<img src="assets/folio-demo.jpg" alt="Folio：将来源材料变成可发布的编辑内容套件，含文章草稿、发布信息与配图规格" width="960" />

</div>

**Folio** 是一个 [Agent Skill](https://github.com/KKenny0/folio-skill)，面向「来源 → 可发布内容套件」的编辑流程。输入 **URL**、**文件** 或 **知识点**，输出彼此一致的文稿、发布元数据和自包含配图制作单——不生成最终图片，也不自动发布。

| | |
| --- | --- |
| **类别** | Agent Skill · 编辑内容流水线 |
| **输入** | URL、本地文件或知识点文本 |
| **默认输出** | `publish-info` · `article-draft` · `figure-spec` |
| **支持的 Style** | Hand-Drawn Cartoon Infographic · Halftone Paper-Collage Editorial Assembly System v2 |
| **安装** | `npx skills add https://github.com/KKenny0/folio-skill` |
| **协议** | MIT |

## 为什么需要 Folio

难的通常不是找到信息，而是把零散来源变成一个真正成立的成品：

- 事实与叙事彼此脱节；
- 文章没有给配图分配清晰任务；
- 图片提示词看起来精致，却加入了来源并未支持的主张。

Folio 把它们当作同一个编辑问题：从 **evidence（证据）** → **narrative（叙事）** → **visual direction（视觉方向）**。最终的文章、发布信息和配图规格共享同一事实边界与观点，而不是三份互不相干的交付物。

## 你会得到什么

| 层次 | 对应内容 | 作用 |
| --- | --- | --- |
| 证据 | 内部事实核查 | 让主张、数字、限制与证据边界始终以来源为准。 |
| 叙事 | `article-draft` | 一篇可独立发布、具有完整论证的文章，而不是图片文案的拼接。 |
| 视觉方向 | `figure-spec` | 每张图一份自包含的配图制作单：图上文案、构图、视觉机制与事实限制。 |
| 发布 | `publish-info` | 面向发布场景的标题、简介和标签。 |

完整内容套件默认按此顺序交付：

1. `publish-info`
2. `article-draft`
3. `figure-spec`

只有用户用「只要 / 不要 / 无需 / 仅输出」等明确限定时，才缩小交付范围；仅列出想要的内容，不视为排除未点名的默认产物。

**Folio 不负责**：生成最终图片、自动发布，或编排动态/视频资产。每份 `figure-spec` 都是自包含的：把其中的配图规格（或完整生图指令）贴进 Codex 的 `imagegen`、ChatGPT 的配图能力，或你常用的其他生图工具，即可得到最终图片。

## 什么时候用 Folio

| 适合用 Folio | 不必用 Folio |
| --- | --- |
| 需要文章 **和** 与事实对齐的配图制作规格 | 只要摘要、学习笔记或单篇文章 |
| 要把项目/工具整理成面向采用决策的推荐 | 需要最终成图或自动发帖 |
| 要做社媒多图轮播 / 公众号图文套件，且每张图任务清晰 | 需要未支持的视觉风格，或动态媒体 |

常见输入：开源仓库 URL、技术帖、研究笔记、产品页，或直接粘贴的知识点。

## Showcase

以下案例展示的不是单纯的风格样本，而是 Folio 如何分别解决不同的阅读任务。

<table width="100%">
  <tr>
    <th width="33.33%" align="center"><a href="https://github.com/KKenny0/Clipplane">Clipplane</a></th>
    <th width="33.33%" align="center"><a href="https://github.com/RealKai42/qwerty-learner">Qwerty Learner</a></th>
    <th width="33.33%" align="center"><a href="https://x.com/cerebras/article/2081828128952095022">GPT-5.6 模型路由 ↗</a></th>
  </tr>
  <tr>
    <td width="33.33%" align="center" valign="top"><a href="assets/showcase/clipplane.jpg"><img src="assets/showcase/clipplane.jpg" alt="Clipplane：Folio figure-spec 驱动的开源工具推荐轮播卡" width="180" height="240" /></a></td>
    <td width="33.33%" align="center" valign="top"><a href="assets/showcase/qwerty-learner.jpg"><img src="assets/showcase/qwerty-learner.jpg" alt="Qwerty Learner：完整 Folio 套件中的采用决策型内容卡" width="180" height="240" /></a><br />图 1 预览<br /><a href="examples/qwerty-learner.md">查看完整套件</a></td>
    <td width="33.33%" align="center" valign="top"><a href="assets/showcase/gpt-5-6-routing.jpg"><img src="assets/showcase/gpt-5-6-routing.jpg" alt="GPT-5.6 模型路由：Folio 技术解读套件中的内容卡" width="180" height="240" /></a></td>
  </tr>
  <tr>
    <td width="33.33%" valign="top"><strong>开源工具推荐</strong><br />中文社媒多图轮播<br />将本地优先的网页剪藏工作流与当前可用方式清楚地呈现出来。</td>
    <td width="33.33%" valign="top"><strong>开源工具推荐</strong><br />中文社媒多图轮播<br />把功能列表转换为「它适合谁」的明确判断。<br /><a href="examples/qwerty-learner.md">完整 publish-info + 文章 + figure-spec</a></td>
    <td width="33.33%" valign="top"><strong>技术解读</strong><br />中文社媒多图轮播<br />基于 <a href="https://x.com/cerebras/article/2081828128952095022">Cerebras 的 GPT-5.6 原始帖文</a>；按信息视野与任务边界区分 Agent 角色，而不是把多 Agent 简化为人头叠加。</td>
  </tr>
</table>

## 如何保持一致性

Folio 有统一的 taste，但不是固定模板。

- **事实边界**：避免文章与图像夸大或改写来源。
- **编辑结构**：每张图只承担一个认知任务，而不是试图在一张卡里塞进全部信息。
- **风格路由**：按信息关系，在手绘信息图和纸张拼贴编辑系统之间选择。
- **Figure Spec QA**：在交付前检查可读性、层级、安全区、图文碰撞与事实限制。

这让系列内容有连续的作者感，同时仍然能随来源、受众与内容类型而变化。

## 安装

```bash
npx skills add https://github.com/KKenny0/folio-skill
```

适用于支持 Skills 格式的 Agent 运行时（例如 Claude Code / 兼容 `skills add` 的宿主）。

## 使用

```text
$folio https://github.com/owner/repo
```

其他常见写法：

```text
$folio ./notes/meeting.md
$folio "长上下文里的 prefix cache"
$folio https://example.com/post -- 平台: 公众号 语言: 中文 图数: 4
```

可选：发布平台、语言、画幅、图数，以及两种受支持 Style 之一：`Hand-Drawn Cartoon Infographic`、`Halftone Paper-Collage Editorial Assembly System v2`。

只需摘要或单篇文章时，直接向 Agent 提要求即可，不必调用 Folio。

## 常见问题

**Folio 是什么？**  
一个 Agent Skill：把 URL、文件或知识点整理成可发布的编辑内容套件——`publish-info`、`article-draft`，以及逐图 `figure-spec`。

**它解决什么问题？**  
让证据、叙事和视觉方向落在同一条事实边界上，避免配图提示词编造来源没有的主张。

**三份默认产物分别是什么？**  
`publish-info`（标题、简介、标签）、`article-draft`（可独立发布的文章）、`figure-spec`（自包含的配图制作规格）。

**Folio 会生成图片吗？**  
不会。它交付可直接进入视觉生产的 `figure-spec`。最终成图由你完成——例如把每张图的规格（或完整生图指令）交给 Codex 的 `imagegen`、ChatGPT 的配图，或其他生图工具。

**支持哪些视觉风格？**  
两种：Hand-Drawn Cartoon Infographic，以及 Halftone Paper-Collage Editorial Assembly System v2。其他风格不会被静默模拟。

**什么时候不该用 Folio？**  
只要摘要、学习笔记或单篇文章时；或者需要动态/视频生产时。

**完整套件长什么样？**  
见 [examples/qwerty-learner.md](examples/qwerty-learner.md)。

## 协议

MIT
