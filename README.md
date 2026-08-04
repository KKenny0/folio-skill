<div align="center">

# Folio

**Turn sources into publish-ready copy and production-ready visual briefs.**

[中文](README.zh-CN.md) · [Showcase](#showcase) · [Install](#install) · [FAQ](#faq)

<img src="assets/folio-demo.jpg" alt="Folio: source material becomes a publishable editorial package with article draft, publish-info, and figure-spec" width="960" />

</div>

**Folio** is an [Agent Skill](https://github.com/KKenny0/folio-skill) for source-to-publish editorial packaging. Given a **URL**, **file**, or **knowledge point**, it produces a coherent content suite: a standalone article, social/publishing metadata, and self-contained figure production briefs—without generating final images or auto-publishing.

| | |
| --- | --- |
| **Category** | Agent Skill · editorial content pipeline |
| **Input** | URL, local file, or topic text |
| **Default output** | `publish-info` · `article-draft` · `figure-spec` |
| **Supported styles** | Hand-Drawn Cartoon Infographic · Halftone Paper-Collage Editorial Assembly System v2 |
| **Install** | `npx skills add https://github.com/KKenny0/folio-skill` |
| **License** | MIT |

## Why Folio

The hard part is rarely finding information. It is turning fragmented sources into something that holds together:

- facts drift away from the story;
- an article does not give the visuals a clear job;
- visual prompts look polished but introduce claims the source never made.

Folio treats those as one editorial problem. It builds a traceable path from **evidence** → **narrative** → **visual direction**, so the finished content shares one point of view instead of three disconnected deliverables.

## What you get

| Layer | Deliverable | Purpose |
| --- | --- | --- |
| Evidence | Internal fact checking | Keeps claims, numbers, limitations, and evidence boundaries grounded in the source. |
| Narrative | `article-draft` | A standalone article with a real argument—not a list of image captions. |
| Visual direction | `figure-spec` | One self-contained, production-ready brief per visual: on-image copy, layout, visual mechanism, and factual limits. |
| Publishing | `publish-info` | Title, summary, and tags ready for the chosen publishing context. |

A full package is delivered in this order:

1. `publish-info`
2. `article-draft`
3. `figure-spec`

Narrow the scope only with explicit limits (“only the article”, “no figure-spec”). Listing desired items does not drop the rest of the default suite.

**Folio does not** generate final images, auto-publish, or produce motion/video assets. Each `figure-spec` is self-contained: paste its production brief (or the full image-generation instruction) into Codex `imagegen`, ChatGPT image generation, or any other image tool you already use.

## When to use Folio

| Use Folio when… | Skip Folio when… |
| --- | --- |
| You need an article **and** visual production briefs that stay fact-aligned | You only want a summary, notes, or a single article draft |
| You are packaging a project/tool recommendation for adoption decisions | You need final rendered images or auto-posting |
| You want social carousel / WeChat-style editorial packages with clear per-card jobs | You need unsupported visual styles or motion media |

Typical inputs: open-source repo URLs, technical posts, research notes, product pages, or a pasted knowledge point.

## Showcase

Selected packages made with Folio. Each example solves a different reading job—not just a style sample.

<table width="100%">
  <tr>
    <th width="33.33%" align="center"><a href="https://github.com/KKenny0/Clipplane">Clipplane</a></th>
    <th width="33.33%" align="center"><a href="https://github.com/RealKai42/qwerty-learner">Qwerty Learner</a></th>
    <th width="33.33%" align="center"><a href="https://x.com/cerebras/article/2081828128952095022">GPT-5.6 model routing ↗</a></th>
  </tr>
  <tr>
    <td width="33.33%" align="center" valign="top"><a href="assets/showcase/clipplane.jpg"><img src="assets/showcase/clipplane.jpg" alt="Clipplane: open-source tool recommendation carousel card generated via Folio figure-spec" width="180" height="240" /></a></td>
    <td width="33.33%" align="center" valign="top"><a href="assets/showcase/qwerty-learner.jpg"><img src="assets/showcase/qwerty-learner.jpg" alt="Qwerty Learner: adoption-oriented editorial card from a full Folio package" width="180" height="240" /></a><br />Figure 1 preview<br /><a href="examples/qwerty-learner.md">View full package</a></td>
    <td width="33.33%" align="center" valign="top"><a href="assets/showcase/gpt-5-6-routing.jpg"><img src="assets/showcase/gpt-5-6-routing.jpg" alt="GPT-5.6 model routing: technical explainer card from Folio editorial package" width="180" height="240" /></a></td>
  </tr>
  <tr>
    <td width="33.33%" valign="top"><strong>Open-source tool recommendation</strong><br />Chinese social carousel<br />Makes the local-first clipping workflow and its current availability legible at a glance.</td>
    <td width="33.33%" valign="top"><strong>Open-source tool recommendation</strong><br />Chinese social carousel<br />Turns a feature list into a clear “who is this for?” decision.<br /><a href="examples/qwerty-learner.md">Full publish-info + article + figure-spec</a></td>
    <td width="33.33%" valign="top"><strong>Technical explainer</strong><br />Chinese social carousel<br />Based on <a href="https://x.com/cerebras/article/2081828128952095022">Cerebras’ GPT-5.6 source post</a>; separates agent roles by information horizon and task boundary, rather than treating multi-agent as headcount.</td>
  </tr>
</table>

## How it stays coherent

Folio has a taste, not a fixed template.

- **Evidence boundaries** keep the article and visuals from overstating the source.
- **Editorial structure** gives every visual one cognitive responsibility, rather than asking every card to say everything.
- **Style routing** chooses between hand-drawn infographic and halftone paper-collage systems based on the information relationship.
- **Figure-spec QA** checks legibility, hierarchy, safe areas, visual-text collisions, and factual limits before the specification is delivered.

That makes a series feel authored while still following the source, audience, and content type.

## Install

```bash
npx skills add https://github.com/KKenny0/folio-skill
```

Works with agent runtimes that support the Skills format (for example Claude Code / compatible `skills add` hosts).

## Use

```text
$folio https://github.com/owner/repo
```

Other useful shapes:

```text
$folio ./notes/meeting.md
$folio "prefix caching for long agent contexts"
$folio https://example.com/post -- platform: WeChat language: zh figures: 4
```

Optional controls: publishing platform, language, aspect ratio, number of visuals, and style (`Hand-Drawn Cartoon Infographic` or `Halftone Paper-Collage Editorial Assembly System v2`).

For a plain summary or a single article, ask the agent directly—Folio is not required.

## FAQ

**What is Folio?**  
An Agent Skill that turns a URL, file, or topic into a publish-ready editorial package: `publish-info`, `article-draft`, and per-image `figure-spec` briefs.

**What problem does it solve?**  
It keeps evidence, narrative, and visual direction on one factual boundary, so image prompts do not invent claims the source never made.

**What are the three deliverables?**  
`publish-info` (title, summary, tags), `article-draft` (standalone article), and `figure-spec` (self-contained visual production briefs).

**Does Folio generate images?**  
No. It writes production-ready `figure-spec` briefs. You generate finals yourself—e.g. with Codex `imagegen`, ChatGPT image generation, or another image tool—by feeding each brief (or its full image-generation instruction) into that tool.

**Which visual styles are supported?**  
Two: Hand-Drawn Cartoon Infographic, and Halftone Paper-Collage Editorial Assembly System v2. Other styles are not silently simulated.

**When should I not use Folio?**  
When you only need a summary, learning notes, or a single article—or when you need motion/video production.

**Where can I see a full package?**  
See [examples/qwerty-learner.md](examples/qwerty-learner.md).

## License

MIT
