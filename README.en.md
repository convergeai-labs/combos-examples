# combos-examples

![Games built by AI agents — 7 games · 21 versions · 0 hand-written lines](docs/assets/hero.png)

[中文](README.md) | **English**

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Games: 5](https://img.shields.io/badge/games-7-blueviolet)](https://github.com/convergeai-labs/combos-examples#play-online)
[![Hand-written code: 0 lines](https://img.shields.io/badge/hand--written%20code-0%20lines-orange)](docs/how-built-with-agent.md)

Games created on [Combos](https://combos.converge.ai) **entirely by an AI coding agent driving the platform's Boo editor agent** — no hand-written game code. Each example ships with its full creation spec, delivery report, version (hash) chain, and verification evidence.

> Batch 1: two games built in one day (pixel fighting + terminal quiz). Batch 2 (2026-08-25): a style-diversity trio — ink-wash, synthwave, watercolor — each **one-shot built, zero fix turns**.

## Latest: the AAA batch (gpt-6-astra × max reasoning)

| 灰烬王座 Ash Throne |
|---|
| ![Ash Throne gameplay: challenge → dodge-and-strike → death card](docs/assets/demo-ashthrone.gif) |
| A three-phase souls-like boss duel: ruined throne hall, telegraphed wind-ups, i-frame dodges, dual victory/defeat cards |
| [▶ Challenge the Ash King](https://combos.game/play/aa231fec03a4e477ba35bb49b25025bc) `29769` · [docs](examples/ash-throne/) |

The heaviest game in the collection: gpt-6-astra at max reasoning effort, one build, zero fix turns; ships a built-in e2e hook (`__combosGameplayTest`) with snapshots and outcome callbacks. A dash-spam bot survives only 23 seconds — the difficulty is the design goal.

## The 3D showcase (gpt-6-astra)

| 崩塌实验室 Crash Lab |
|---|
| ![Crash Lab gameplay: aim → launch → slow-mo collapse → result](docs/assets/demo-crashlab.gif) |
| Blender-grade 3D physics destruction: drag to aim, one shot, 0.25× slow-mo collapse, destruction-% rank card |
| [▶ Start smashing](https://combos.game/play/9b198fca47ea7195ca115dc396b85b7b) `94401` · [docs](examples/crash-lab/) |

First 3D game in the collection, built in one shot by **gpt-6-astra** with zero fix turns; seeded physics — identical drags measured ±0% across runs.

## The style-diversity batch

Three games with zero overlap in visual style, input mechanic, and distribution structure:

| 一笔签 One Stroke Fortune | 毫秒反应局 Millisecond Reaction | 灵魂汤底 Soul Soup |
|---|---|---|
| ![One Stroke Fortune gameplay](docs/assets/demo-one-stroke-fortune.gif) | ![Millisecond Reaction gameplay](docs/assets/demo-ms-reflex.gif) | ![Soul Soup gameplay](docs/assets/demo-soul-soup.gif) |
| Ink-wash · draw one stroke for your fortune poster | Synthwave · tap the instant the light turns green | Watercolor storybook · three choices reveal your soul soup |
| Input: continuous stroke (draw) | Input: single-shot timing (ms) | Input: discrete choices (narrative) |
| [▶ Play](https://combos.game/play/f21f5d3fc39ed46e571279e28e995ce8) `96120` · [docs](examples/one-stroke-fortune/) | [▶ Play](https://combos.game/play/28185913e918a376b139ff0c511b9ff9) `94840` · [docs](examples/ms-reflex/) | [▶ Play](https://combos.game/play/1040f4909f4dc83398a9739ea27bd384) `47205` · [docs](examples/soul-soup/) |

All three passed the full independent-verification gate (state machine, dual viewport, zero console errors, permanent honesty disclaimers), plus distribution invariants: 100 random-stroke draws covering 12/12 fortunes, all 27 narrative paths covering 6/6 soups, and correct false-start judgment on the fake-flash round.

## Batch 1 (published)

No install — opens in a mobile browser, anonymous play supported:

| 模型大乱斗 Model Brawl | 模型盲测 Model Blind Test |
|---|---|
| ![Model Brawl gameplay: pick fighter → fight → KO report](docs/assets/demo-brawl.gif) | ![Model Blind Test gameplay: read → guess → reveal](docs/assets/demo-blindtest.gif) |
| One-button AI-model fighting, 20s rounds, meme KO cards | Guess which AI model wrote the answer; face-cam + selfie score poster |
| [▶ Fight now](https://combos.game/play/8dd0941ae0543fcccd0fc565a6ecaf3c) · share code `58283` | [▶ Start the test](https://combos.game/play/ae82cf8ef3e7931e0008b02a2a7cebae) · share code `89524` |

## The creation pipeline

![Creation pipeline: viral design → spec → Boo creation → independent browser verification → bounded fixes → delivery report](docs/assets/creation-pipeline.png)

Every deployed hash is independently verified in a real browser; failures go back for a bounded fix turn and the new hash is verified again. Seven games, 21 deployed hashes, zero hand-written code.

## Examples

| Game | One-liner | Play | Hashes | Key lessons inside |
|---|---|---|---|---|
| [模型大乱斗 Model Brawl](examples/model-brawl/) | One-button AI-model fighting, 20s rounds, meme KO cards | [▶ play](https://combos.game/play/8dd0941ae0543fcccd0fc565a6ecaf3c) | 9 | Slate message fragmentation incident; desktop input-mapping bug invisible to Boo's own smoke test |
| [模型盲测 Model Blind Test](examples/model-blind-test/) | Guess which AI model wrote the answer; face-cam + selfie score poster | [▶ play](https://combos.game/play/ae82cf8ef3e7931e0008b02a2a7cebae) | 7 | Broken question-bank distribution; getUserMedia pending-forever ("clicked, nothing happened") root cause & fix |
| [一笔签 One Stroke Fortune](examples/one-stroke-fortune/) | Draw one stroke on rice paper, get your 2026 ink fortune poster | [▶ play](https://combos.game/play/f21f5d3fc39ed46e571279e28e995ce8) | 1 | Complete spec = one-shot build, zero fixes; UGC hook without a camera |
| [毫秒反应局 Millisecond Reaction](examples/ms-reflex/) | Tap on green, 5 rounds, average-ms rank card | [▶ play](https://combos.game/play/28185913e918a376b139ff0c511b9ff9) | 1 | External verification of a WebGL game: screenshot pixel probe instead of getImageData |
| [灵魂汤底 Soul Soup](examples/soul-soup/) | Three gentle choices in a rainy-night store reveal your soul soup | [▶ play](https://combos.game/play/1040f4909f4dc83398a9739ea27bd384) | 1 | Deterministic mapping (27 paths → 6 soups) written into the spec, implemented verbatim |
| [崩塌实验室 Crash Lab](examples/crash-lab/) | Blender-grade 3D physics destruction in slow motion | [▶ play](https://combos.game/play/9b198fca47ea7195ca115dc396b85b7b) | 1 | Built by gpt-6-astra on demand; seeded physics ±0% measured |
| [灰烬王座 Ash Throne](examples/ash-throne/) | Three-phase souls-like boss duel, dodge-and-strike | [▶ play](https://combos.game/play/aa231fec03a4e477ba35bb49b25025bc) | 1 | gpt-6-astra × max reasoning; built-in e2e hook (__combosGameplayTest) |

## How were these built?

Read [docs/how-built-with-agent.md](docs/how-built-with-agent.md) — the full methodology: distribution-first design, spec templates, bounded Boo turns, independent browser verification of every hash, and the four real incidents that shaped the process.

Built with the companion skill: [combos-skills / combos-game-creator](https://github.com/convergeai-labs/combos-skills).

![Dual-agent collaboration: the human directs, the agent verifies, Boo builds](docs/assets/dual-agent-loop.png)

## A note on honesty

**Every game carries a permanent visible honesty disclaimer**: quiz answers are human-written style parodies (not real model outputs); percentile figures ("击败了全国 X% 的人", "top X% of players") are labeled theater, not real leaderboards; One Stroke Fortune's fortunes are program-generated entertainment; Soul Soup is labeled "entertainment, not a psychological diagnosis". No vendor logos are used anywhere.

## License

MIT (docs and specs). Screenshots are provided as verification evidence for reference.
