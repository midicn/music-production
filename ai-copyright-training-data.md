---
id: ai-copyright-training-data
site: prod
cat: B7
title: 版权与训练数据争议
title_en: Copyright and Training Data
summary: 训练数据、风格模仿与版权边界，是 AI 音乐最难绕开的问题。
summary_en: Training data, style imitation and copyright boundaries are the hardest issues in AI music.
level: standard
tags: [AI, 版权, 训练数据, 清权]
tags_en: [AI, copyright, training data, clearance]
alias: [版权与训练数据争议, AI 版权, 训练数据, training data, AI copyright]
links:
  - "[[glossary:music-copyright]]"
  - "[[glossary:public-domain]]"
  - "[[glossary:fair-use]]"
  - "[[glossary:creative-commons]]"
instances:
  - thesession-000000 | 传统曲调本身多已进入公有领域，具体记谱与录音仍受各自条款约束
  - atepp-000238 | 肖斯塔科维奇的作品是二十世纪创作，适合讨论风格与具体作品的界线
  - mutopia-000439 | 巴赫众赞歌属公有领域，做风格参照时风险最低
  - abcmisc-000139 | 现代作曲家写的克莱兹默圆舞曲，风格传统而作品不旧
sources:
  - 美国版权局关于 AI 生成材料登记政策的公开说明，依官方文件核查，未抄文本
  - 知识共享许可 4.0 的署名与再分发条款，依官方文本核查，未抄文本
updated: 2026-10-28
---

::: zh
模型从大量作品里学统计规律，输出又常与原作相似。权利归谁、署名给谁、训练是否合法，三件事要分开谈。

## 问题

一首歌有两层权利，词曲与录音；MIDI 曲目涉及的是词曲与演奏数据。训练数据来自公有领域、授权曲库或网络抓取，来源不同，风险不同。

## 原理或流程

风格本身不受版权保护，具体的旋律、和声进行与编曲可以受版权保护。判断侵权看输出与原作是否实质相似，不看模型是否听过。文本与数据挖掘的例外在各司法辖区不同，商用与研究的边界也不同。

## 做法与判断

记录数据来源与许可，避免用受保护作品做明确模仿。生成后做相似度检查，商用前确认平台条款与输出权利归属，保留人类修改的证据。用公有领域作品做风格参照，风险最低。

## 听什么

听旋律轮廓是否与原曲重合，听标志性和声与节奏型是否被照搬。再听编曲层，配器与织体常比旋律更容易露出原型。

## 常见误解

非商业就不侵权；标注来源就没事；风格可以版权。标注只解决署名，不解决授权。

```audiolab
{"type":"instrument","gm":"Clarinet","synth":"reed","phrase":["D4","F4","A4","G4","E4","D4"],"label":"一段可被追溯到原型的旋律","label_en":"A melody that can be traced to a prototype","hint":"听它的轮廓与节奏型，再想改几个音是否就算新作品","hint_en":"Hear the contour and rhythmic figure, then ask whether changing a few notes makes a new work"}
```
:::

::: en
Models learn statistical patterns from many works, and their output resembles existing music. Ownership, credit and the legality of training are three separate questions.

## The problem

A song carries two layers of rights, composition and recording; MIDI tracks involve composition and performance data. Training data comes from the public domain, licensed libraries or scraping, and each source carries different risk.

## How it works

Style itself is not protected, while a specific melody, harmonic progression or arrangement may be. Infringement turns on substantial similarity between output and original, not on whether the model heard it. Text and data mining exceptions differ by jurisdiction, and the line between research and commercial use differs too.

## Practice and judgement

Record sources and licences, and avoid deliberate imitation of protected works. Run a similarity check after generation, confirm platform terms and output ownership before commercial use, and keep evidence of human edits. Public domain works make the safest style references.

## What to listen for

Hear whether a melodic contour matches an existing song, or a signature harmony and rhythm is copied. Then hear the arrangement; orchestration and texture reveal a prototype more than the melody.

## Common misunderstandings

Non-commercial use cannot infringe; crediting the source settles it; style can be copyrighted. Credit answers attribution, not permission.

```audiolab
{"type": "instrument", "gm": "Clarinet", "synth": "reed", "phrase": ["D4", "F4", "A4", "G4", "E4", "D4"], "label": "A melody that can be traced to a prototype", "label_en": "A melody that can be traced to a prototype", "hint": "听它的轮廓与节奏型，再想改几个音是否就算新作品", "hint_en": "Hear the contour and rhythmic figure, then ask whether changing a few notes makes a new work"}
```
:::
