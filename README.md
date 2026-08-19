<div align="center">

# Social Content Kit

**Turn sources into social-ready copy and production-ready visual briefs.**

[中文](README.zh-CN.md) · [Showcase](#showcase) · [Install](#install) · [FAQ](#faq)

</div>

**Social Content Kit** is an [Agent Skill](https://github.com/KKenny0/social-content-kit-skill) for source-to-social editorial packaging. Given a **URL**, **file**, or **knowledge point**, it produces platform-ready publishing copy and self-contained visual production briefs that share one verified content boundary. A standalone article is generated only when explicitly requested.

| | |
| --- | --- |
| **Category** | Agent Skill · social editorial pipeline |
| **Input** | URL, local file, or topic text |
| **Default output** | `publish-info` · `figure-spec` |
| **Article, on request** | `article-draft` |
| **Visual identity** | Folio Editorial Sketch · one fixed house style |
| **Install** | `npx skills add https://github.com/KKenny0/social-content-kit-skill` |
| **License** | MIT |

## Why Social Content Kit

The hard part is rarely finding information. It is turning fragmented sources into social content without letting the copy and visuals drift apart:

- publishing copy loses the limitations that make a recommendation credible;
- each card repeats information instead of having one clear cognitive job;
- visual prompts look polished but introduce claims the source never made.

Social Content Kit treats those as one editorial problem. It builds an internal verified content core, then derives publishing copy and visual briefs from that same source of truth. An article is optional instead of a mandatory intermediate deliverable; long, short, and very short only control its length.

## What you get

| Layer | Deliverable | Purpose |
| --- | --- | --- |
| Evidence | Internal verified content core | Tracks sources, claims, exact values, limitations, and uncertainty. It is never emitted as another deliverable. |
| Publishing | `publish-info` | Platform-ready title, post copy, source note, and tags. |
| Visual direction | `figure-spec` | One self-contained production brief per visual: on-image copy, layout, visual mechanism, and factual limits. |
| Article, on request | `article-draft` | A standalone article organized independently of the cards, at the requested length. |

Default social package:

1. `publish-info`
2. `figure-spec`

Ask for a “full content package,” “article and visuals,” or a WeChat long-form package to receive:

1. `publish-info`
2. `article-draft`
3. `figure-spec`

Explicit limits such as “only,” “without,” or “do not include” are followed exactly.

**Social Content Kit does not automatically** generate final images, auto-publish, or produce motion/video assets. Each `figure-spec` is self-contained. When the current session exposes a callable image-generation tool, the Skill may offer—after delivering and checking the briefs—to continue generating the images. It never infers that capability from a platform name, and it waits for confirmation before calling the tool.

## When to use Social Content Kit

| Use Social Content Kit when… | Skip Social Content Kit when… |
| --- | --- |
| You want a social carousel or image-card series with platform-ready post copy | You only want a summary, notes, or a plain single article |
| You are packaging a project/tool recommendation for adoption decisions | You only need rendered images, without social copy or visual briefs |
| You need an article and fact-aligned visuals as one explicitly requested package | You need unsupported visual styles or motion media |

Typical inputs: open-source repository URLs, technical posts, research notes, product pages, or pasted knowledge points.

## Showcase

One validated social suite made from the real [srt-whiteboard-animation](https://github.com/geeklee/srt-whiteboard-animation) repository. The four cards change reading jobs without changing visual identity.

<table width="100%">
  <tr>
    <th colspan="4" align="center"><a href="https://github.com/geeklee/srt-whiteboard-animation">srt-whiteboard-animation ↗</a></th>
  </tr>
  <tr>
    <td width="25%" align="center" valign="top"><a href="assets/showcase/srt-whiteboard-01.jpg"><img src="assets/showcase/srt-whiteboard-01.jpg" alt="Cover card: SRT subtitles become a hand-drawn animation" width="180" height="240" /></a></td>
    <td width="25%" align="center" valign="top"><a href="assets/showcase/srt-whiteboard-02.jpg"><img src="assets/showcase/srt-whiteboard-02.jpg" alt="Process card: split subtitles into 25–35 second scenes" width="180" height="240" /></a></td>
    <td width="25%" align="center" valign="top"><a href="assets/showcase/srt-whiteboard-03.jpg"><img src="assets/showcase/srt-whiteboard-03.jpg" alt="Mechanism card: masks control order and strokes control drawing" width="180" height="240" /></a></td>
    <td width="25%" align="center" valign="top"><a href="assets/showcase/srt-whiteboard-04.jpg"><img src="assets/showcase/srt-whiteboard-04.jpg" alt="Decision card: suitable content and lowest-cost next step" width="180" height="240" /></a></td>
  </tr>
  <tr>
    <td width="25%" valign="top"><strong>Entry</strong><br />Source and value</td>
    <td width="25%" valign="top"><strong>Process</strong><br />Exact timing and grouping</td>
    <td width="25%" valign="top"><strong>Mechanism</strong><br />What each control system is responsible for</td>
    <td width="25%" valign="top"><strong>Decision</strong><br />Best fit and next step<br /><a href="examples/srt-whiteboard-animation.md">View publish-info + figure-spec</a></td>
  </tr>
</table>

## How it stays coherent

Social Content Kit has a taste, not a fixed template.

- **Evidence boundaries** keep publishing copy and visuals from overstating the source.
- **Editorial structure** gives every visual one cognitive responsibility instead of asking every card to say everything.
- **Plain language first** makes the title, responsibility labels, and main relationship carry the conclusion; fields and parameters stay local supporting evidence.
- **One house style** keeps the warm gray-white paper, navy ink, cobalt structure, terracotta emphasis, typography, and drawing grammar stable across posts.
- **Mechanism routing** varies the hand-drawn relation, semantic paper operation, composition, and accent area according to what each card must explain.
- **Figure-spec QA** checks legibility, hierarchy, safe areas, visual-text collisions, and factual limits before the specification is delivered.

That makes a series feel authored while still following the source, audience, and publishing context.

## Install

```bash
npx skills add https://github.com/KKenny0/social-content-kit-skill
```

Works with agent runtimes that support the Skills format, such as Claude Code and compatible `skills add` hosts.

## Use

```text
$social-content-kit https://github.com/owner/repo
```

This default invocation produces `publish-info` and `figure-spec`. Other useful shapes:

```text
$social-content-kit ./notes/meeting.md
$social-content-kit "prefix caching for long agent contexts"
$social-content-kit https://example.com/post -- platform: WeChat language: zh figures: 4
$social-content-kit https://example.com/post -- full package with article and 4 visuals
```

Optional controls: publishing platform, language, aspect ratio, number of visuals, and requested deliverables. Visual style is intentionally not a control.

If neither you nor the publishing platform specifies an aspect ratio, Social Content Kit defaults to a `3:4` portrait canvas (`1536×2048 px`).

For a plain summary or single article, ask the agent directly—Social Content Kit is not required.

## FAQ

**What is Social Content Kit?**

An Agent Skill that turns a URL, file, or topic into platform-ready publishing copy and self-contained visual production briefs.

**Was this Skill previously called Folio?**

Yes. Starting with v0.9.0, the public Skill ID is `$social-content-kit` and the repository is `social-content-kit-skill`. Reinstall the Skill to update the invocation name. Folio Editorial Sketch remains the fixed visual identity.

**What is generated by default?**

`publish-info` (title, post copy, source note, tags) and `figure-spec` (one self-contained visual brief per card).

**Can Social Content Kit still write a standalone article?**

Yes. In an explicit `$social-content-kit` request, asking for a standalone article returns `article-draft` only. Ask for an article-and-visual, full-content, or WeChat long-form package when you want all three deliverables.

**What keeps the deliverables fact-aligned without a visible article?**

Social Content Kit first builds an internal verified content core containing sources, claims, exact values, limitations, and uncertainty. Every requested deliverable is derived from it.

**Does Social Content Kit generate images?**

Not automatically. It first delivers production-ready `figure-spec` briefs. If the current session has a callable image-generation tool—and you did not request briefs-only output—it can then ask, in the output language, whether to generate the images as a confirmed downstream step. Image generation and bitmap inspection are detected separately: if the session cannot inspect generated pixels, the offer discloses that limitation and the results remain marked as awaiting Bitmap QA. A successful tool call is not an approval.

**Which visual style is used?**

One: Folio Editorial Sketch. It uses editorial hierarchy and a dominant hand-drawn relationship, adds paper only when it explains a boundary or transformation, and keeps halftone local. The fixed identity is deliberate so separate posts still look like one social account.

**Where can I see a complete default package?**

See [examples/srt-whiteboard-animation.md](examples/srt-whiteboard-animation.md).

## License

MIT
