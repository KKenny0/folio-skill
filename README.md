# Signal Pack

![Signal Pack demo banner](assets/signal-pack-demo.jpg)

Turn a URL, file, or knowledge point into a publish-ready editorial package:

- `publish-info`: title, summary, and tags
- `article-draft`: a standalone article grounded in the source material
- `figure-spec`: self-contained prompts and layout specifications for each visual

It is designed for Chinese social-media carousels, learning notes, technical explainers, and open-source project recommendations. It includes source fact checking, figure-spec QA, two visual-language routes, and an optional project-recommendation evolution path.

## Install

```bash
npx skills add https://github.com/KKenny0/signal-pack
```

## Use

```
@Signal Pack https://github.com/owner/repo
```

You can also provide a file or a topic directly. Optionally specify the platform, language, aspect ratio, number of visuals, or one of the supported visual styles.

## Output

The skill intentionally returns only three user-facing artifacts, in this order:

1. `publish-info`
2. `article-draft`
3. `figure-spec`

Internal fact-checking and QA records are used to improve the result, not emitted as extra deliverables.

## Showcase

Selected examples generated with Signal Pack.

| [Clipplane](https://github.com/KKenny0/Clipplane) | [Qwerty Learner](https://github.com/RealKai42/qwerty-learner) | [Bento](https://github.com/warpstreamlabs/bento) | GPT-5.6 model routing |
| --- | --- | --- | --- |
| <a href="assets/showcase/clipplane.jpg"><img src="assets/showcase/clipplane.jpg" alt="Clipplane showcase" width="180" /></a> | <a href="assets/showcase/qwerty-learner.jpg"><img src="assets/showcase/qwerty-learner.jpg" alt="Qwerty Learner showcase" width="180" /></a> | <a href="assets/showcase/bento.jpg"><img src="assets/showcase/bento.jpg" alt="Bento showcase" width="180" /></a> | <a href="assets/showcase/gpt-5-6-routing.jpg"><img src="assets/showcase/gpt-5-6-routing.jpg" alt="GPT-5.6 model routing showcase" width="180" /></a> |

## License

MIT
