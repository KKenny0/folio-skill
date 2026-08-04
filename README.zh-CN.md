<div align="center">

# Folio

**把来源变成可发布文稿和可直接进入视觉生产的配图规格。**

[English](README.md) · [案例](#showcase) · [安装](#安装)

<img src="assets/folio-demo.jpg" alt="Folio：将来源材料变成可发布的编辑内容套件" width="960" />

</div>

Folio — Source-to-Publish Editorial Skill — 将 URL、文件或一个知识点整理为彼此一致的文稿和配图制作单。

## 为什么需要 Folio

难的通常不是找到信息，而是把零散来源变成一个真正成立的成品：

- 事实与叙事彼此脱节；
- 文章没有给配图分配清晰任务；
- 图片提示词看起来精致，却加入了来源并未支持的主张。

Folio 将它们视为同一个编辑问题：从 **evidence（证据）** 到 **narrative（叙事）**，再到 **visual direction（视觉方向）**。最终的文章、发布信息和配图规格共享同一个事实边界与观点，而不是三份互不相干的交付物。

## 你会得到什么

| 层次 | 对应内容 | 作用 |
| --- | --- | --- |
| 证据 | 内部事实核查 | 让主张、数字、限制与证据边界始终以来源为准。 |
| 叙事 | `article-draft` | 一篇可独立发布、具有完整论证的文章，而不是图片文案的拼接。 |
| 视觉方向 | `figure-spec` | 每张图一份自包含的配图制作单：图上文案、构图、视觉机制与事实限制。 |
| 发布 | `publish-info` | 面向发布场景的标题、简介和标签。 |

Folio 交付可发布文稿和配图制作规格，不生成最终图片，也不自动发布。

完整内容套件包含三份产物：

1. `publish-info`
2. `article-draft`
3. `figure-spec`

用户明确缩小范围时，只交付所请求的产物。

## Showcase

以下案例展示的不是单纯的风格样本，而是 Folio 如何分别解决不同的阅读任务。

<table width="100%">
  <tr>
    <th width="33.33%" align="center"><a href="https://github.com/KKenny0/Clipplane">Clipplane</a></th>
    <th width="33.33%" align="center"><a href="https://github.com/RealKai42/qwerty-learner">Qwerty Learner</a></th>
    <th width="33.33%" align="center"><a href="https://x.com/cerebras/article/2081828128952095022">GPT-5.6 模型路由 ↗</a></th>
  </tr>
  <tr>
    <td width="33.33%" align="center" valign="top"><a href="assets/showcase/clipplane.jpg"><img src="assets/showcase/clipplane.jpg" alt="Clipplane 内容卡片" width="180" height="240" /></a></td>
    <td width="33.33%" align="center" valign="top"><a href="assets/showcase/qwerty-learner.jpg"><img src="assets/showcase/qwerty-learner.jpg" alt="Qwerty Learner 内容卡片" width="180" height="240" /></a><br />图 1 预览<br /><a href="examples/qwerty-learner.md">查看完整套件</a></td>
    <td width="33.33%" align="center" valign="top"><a href="assets/showcase/gpt-5-6-routing.jpg"><img src="assets/showcase/gpt-5-6-routing.jpg" alt="GPT-5.6 模型路由内容卡片" width="180" height="240" /></a></td>
  </tr>
  <tr>
    <td width="33.33%" valign="top"><strong>开源工具推荐</strong><br />中文社媒多图轮播<br />将本地优先的网页剪藏工作流与当前可用方式清楚地呈现出来。</td>
    <td width="33.33%" valign="top"><strong>开源工具推荐</strong><br />中文社媒多图轮播<br />把功能列表转换为“它适合谁”的明确判断。</td>
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

## 使用

```
$folio https://github.com/owner/repo
```

也可以直接提供文件或知识点。可选指定发布平台、语言、画幅、图数，或两种受支持 Style 之一：`Hand-Drawn Cartoon Infographic`、`Halftone Paper-Collage Editorial Assembly System v2`。只需摘要或单篇文章时，直接提出请求即可，不需要调用 Folio。

## 协议

MIT
