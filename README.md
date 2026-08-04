<div align="center">

# Folio

**Turn sources into publish-ready copy and production-ready visual briefs.**

[中文](README.zh-CN.md) · [Showcase](#showcase) · [Install](#install)

<img src="assets/folio-demo.jpg" alt="Folio: source material becomes a publishable editorial package" width="960" />

</div>

Folio — Source-to-Publish Editorial Skill — turns a URL, file, or knowledge point into coherent copy and visual production briefs.

## Why Folio

The hard part is rarely finding information. It is turning fragmented sources into something that holds together:

- facts drift away from the story;
- an article does not give the visuals a clear job;
- visual prompts look polished but introduce claims the source never made.

Folio treats those as one editorial problem. It builds a traceable path from **evidence** to **narrative** to **visual direction**—so the finished content has a single point of view instead of three disconnected deliverables.

## What you get

| Layer | Deliverable | Purpose |
| --- | --- | --- |
| Evidence | Internal fact checking | Keeps claims, numbers, limitations, and evidence boundaries grounded in the source. |
| Narrative | `article-draft` | A standalone article with a real argument—not a list of image captions. |
| Visual direction | `figure-spec` | One self-contained, production-ready brief per visual: copy, layout, visual mechanism, and factual limits. |
| Publishing | `publish-info` | A title, summary, and tags ready for the chosen publishing context. |

Folio creates publish-ready copy and visual production briefs. It does not generate final images or publish anything automatically.

A complete package contains three deliverables:

1. `publish-info`
2. `article-draft`
3. `figure-spec`

When a user explicitly narrows the scope, deliver only the requested artifacts.

## Showcase

Selected editorial packages made with Folio. Each example is evidence of a different reading job—not just a style sample.

<table width="100%">
  <tr>
    <th width="33.33%" align="center"><a href="https://github.com/KKenny0/Clipplane">Clipplane</a></th>
    <th width="33.33%" align="center"><a href="https://github.com/RealKai42/qwerty-learner">Qwerty Learner</a></th>
    <th width="33.33%" align="center"><a href="https://x.com/cerebras/article/2081828128952095022">GPT-5.6 model routing ↗</a></th>
  </tr>
  <tr>
    <td width="33.33%" align="center" valign="top"><a href="assets/showcase/clipplane.jpg"><img src="assets/showcase/clipplane.jpg" alt="Clipplane editorial card" width="180" height="240" /></a></td>
    <td width="33.33%" align="center" valign="top"><a href="assets/showcase/qwerty-learner.jpg"><img src="assets/showcase/qwerty-learner.jpg" alt="Qwerty Learner editorial card" width="180" height="240" /></a><br />Figure 1 preview<br /><a href="examples/qwerty-learner.md">View full package</a></td>
    <td width="33.33%" align="center" valign="top"><a href="assets/showcase/gpt-5-6-routing.jpg"><img src="assets/showcase/gpt-5-6-routing.jpg" alt="GPT-5.6 model routing editorial card" width="180" height="240" /></a></td>
  </tr>
  <tr>
    <td width="33.33%" valign="top"><strong>Open-source tool recommendation</strong><br />Chinese social carousel<br />Makes the local-first clipping workflow and its current availability legible at a glance.</td>
    <td width="33.33%" valign="top"><strong>Open-source tool recommendation</strong><br />Chinese social carousel<br />Turns a feature list into a clear “who is this for?” decision.</td>
    <td width="33.33%" valign="top"><strong>Technical explainer</strong><br />Chinese social carousel<br />Based on <a href="https://x.com/cerebras/article/2081828128952095022">Cerebras’ GPT-5.6 source post</a>; separates agent roles by information horizon and task boundary, rather than treating multi-agent as headcount.</td>
  </tr>
</table>

## How it stays coherent

Folio has a taste, not a fixed template.

- **Evidence boundaries** keep the article and visuals from overstating the source.
- **Editorial structure** gives every visual one cognitive responsibility, rather than asking every card to say everything.
- **Style routing** chooses between hand-drawn infographic and halftone paper-collage systems based on the information relationship.
- **Figure-spec QA** checks legibility, hierarchy, safe areas, visual-text collisions, and factual limits before the specification is delivered.

That makes a series feel authored while leaving room for the source, audience, and content type to change.

## Install

```bash
npx skills add https://github.com/KKenny0/folio-skill
```

## Use

```
$folio https://github.com/owner/repo
```

You can also provide a file or topic directly. Optionally specify the platform, language, aspect ratio, number of visuals, or one of the two supported styles: `Hand-Drawn Cartoon Infographic` or `Halftone Paper-Collage Editorial Assembly System v2`. For a summary or a single article, ask for it directly; Folio is not needed.

## License

MIT
