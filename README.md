# combos-examples

![用 AI Agent 做游戏 —— 2 个游戏 · 16 个版本 · 0 行手写代码](docs/assets/hero.png)

**中文** | [English](README.en.md)

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Games: 2 playable](https://img.shields.io/badge/games-2%20playable-blueviolet)](https://github.com/convergeai-labs/combos-examples#在线试玩)
[![Hand-written code: 0 lines](https://img.shields.io/badge/hand--written%20code-0%20lines-orange)](docs/how-built-with-agent.md)

在 [Combos](https://combos.converge.ai) 上、**完全由 AI coding agent 驱动平台的 Boo 编辑 agent** 创作的游戏合集——没有手写一行游戏代码。每个示例都附带完整创作规格、交付报告、版本 hash 链和独立验证证据。

> 本仓库会陆续收录多个示例,当前是第一批:一天之内做出的两个游戏。

## 在线试玩

无需安装,手机浏览器直接玩(匿名可玩):

| 模型大乱斗 Model Brawl | 模型盲测 Model Blind Test |
|---|---|
| ![模型大乱斗实玩:选人→格斗→KO 结算](docs/assets/demo-brawl.gif) | ![模型盲测实玩:读题→猜模型→揭晓答案](docs/assets/demo-blindtest.gif) |
| 一键 AI 模型格斗,20 秒一局,KO 出梗结算卡 | 猜一段回答是哪个 AI 写的;全程出镜 + 自拍战绩海报 |
| [▶ 立即开打](https://combos.game/play/8dd0941ae0543fcccd0fc565a6ecaf3c) · 分享码 `58283` | [▶ 开始盲测](https://combos.game/play/ae82cf8ef3e7931e0008b02a2a7cebae) · 分享码 `89524` |

## 创作流水线

![创作流水线:传播设计→写规格→Boo 创建→独立浏览器验证→有界修复→交付报告](docs/assets/creation-pipeline.png)

每个部署 hash 都经过独立浏览器验证;验证不过就回炉,新 hash 再验证。两个游戏共 16 个部署 hash,0 行手写代码。

## 示例

| 游戏 | 一句话 | 试玩 | Hash 数 | 内含教训 |
|---|---|---|---|---|
| [模型大乱斗 Model Brawl](examples/model-brawl/) | 一键 AI 模型格斗,20 秒一局,KO 出梗结算卡 | [▶ 试玩](https://combos.game/play/8dd0941ae0543fcccd0fc565a6ecaf3c) | 9 | Slate 消息拆段事故;Boo 自测不可见的桌面输入映射反转 bug |
| [模型盲测 Model Blind Test](examples/model-blind-test/) | 猜一段回答是哪个 AI 模型写的;全程出镜 + 自拍战绩海报 | [▶ 试玩](https://combos.game/play/ae82cf8ef3e7931e0008b02a2a7cebae) | 7 | 题库分布崩(一轮 4/5 同答案);getUserMedia 永久 pending("点了没反应")根因与修复 |

## 这些游戏是怎么做出来的?

读 [docs/how-built-with-agent.md](docs/how-built-with-agent.md) —— 完整方法论:传播设计先行、规格模板、有界 Boo turn、每个 hash 的独立浏览器验证,以及塑造了这套流程的四个真实事故。

配套 skill:[combos-skills / combos-game-creator](https://github.com/convergeai-labs/combos-skills)。

![双 Agent 协作:人指挥,Agent 验证,Boo 建造](docs/assets/dual-agent-loop.png)

## 诚实声明

两个游戏都是**风格演绎的娱乐内容**:盲测题目的回答是人类按模型文风刻板印象写的段子,不是真实模型输出,游戏内常驻可见声明标注了这一点。"击败了全国 X% 的人"是标注过的伪随机演出,不是真实排行榜。所有素材不含任何厂商官方 logo。

## License

MIT(文档与规格)。截图作为验证证据提供参考。
