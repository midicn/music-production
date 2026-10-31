---
id: sample-orchestra-vs-real
site: prod
cat: A3
title: 采样乐队与真乐队
title_en: Sample Orchestra vs Real Players
summary: 采样能对齐和修改，真乐队给的是连奏与呼吸的不可预测。
summary_en: Samples give alignment and revisions; real players give the unpredictability of bowing and breath.
level: standard
tags: [配器, 采样, 录音, 预算]
tags_en: [orchestration, samples, recording, budget]
alias: [采样乐队, 真乐队, 采样与实录, sample orchestra, live orchestra]
order: 334
links:
  - "[[glossary:sampler]]"
  - "[[glossary:legato]]"
  - "[[glossary:dynamics]]"
  - "[[instrument:virtual-instruments]]"
  - "[[instrument:violin]]"
instances:
  - pdmx-000065 | 巴赫《第一大提琴组曲》，单声部大提琴，弓速与换弓都露在外面，采样最难遮 | Bach's First Cello Suite, one exposed line where bow speed and changes are hardest to fake
  - musicnet-000097 | 贝多芬《第八弦乐四重奏》第一乐章，四把琴各占一个通道，可听四声部怎样互相让路 | Beethoven's Eighth Quartet, first movement, four channels showing how the parts make room for each other
  - pdmx-000120 | 科普兰《普通人的号角》，铜管齐奏的音头与层次，最考验采样能否站得住 | Copland's Fanfare for the Common Man, where brass attacks and layers test any sample library
sources:
  - Paul Gilreath, The Guide to MIDI Orchestration, 采样乐队的动态层与连奏
  - Andrea Pejrolo and Rich DeRosa, Acoustic and MIDI Orchestration for the Contemporary Composer, Focal Press
  - Vienna Symphonic Library, 乐器文档中的连奏与力度层说明
updated: 2026-10-31
---

::: zh
只够录一天弦乐时，最该进棚的不是整段配乐，而是采样永远做不像的那几句连奏和弱奏。

## 先看用途

片子要改十版，还是只交一版；镜头里有没有乐手；音乐是背景还是主角。这些问题决定真录的比例。需要频繁改调的广告，全采样更省；片尾要署上乐手名字的纪录片，真录的那几件乐器就是凭据。先定用途，再谈音色。

## 动态与连奏差在哪

采样把力度分成层，层与层之间靠交叉淡化。写一个从弱到强的长音，采样会在某个点换层，听感像换了一张录音。真乐队的渐强是连续的，还带着弓速、气息和房间。[[glossary:legato|连奏]]也一样：采样的连奏是预录的过渡音，速度快时会露接缝，慢时会显得太整齐。

## 哪些声部最值得录

独奏弦乐、木管独奏、铜管渐强、流行弦乐的滑音，这几类最难替代。内声部的长音、打击乐、已经埋在混音里的铺底，用[[glossary:sampler|采样]]通常够。把预算放在能被听见的独奏上，比平均分给每个声部有效。写谱时就要标出哪些句子里有独奏，别等录完再找。

| 方案 | 适合 | 修改成本 | 风险 |
|---|---|---|---|
| 全采样 | 广告、试映、频繁改版 | 低 | 动态层断点、连奏接缝 |
| 独奏真录加采样乐队 | 歌曲、纪录片 | 中 | 真独奏与采样组的房间不匹配 |
| 分组真录加采样补 | 中等预算影视 | 中高 | 编辑点与呼吸对不上 |
| 全真录 | 专辑、院线片 | 高 | 改一个音往往要重新约人 |

## 预算怎么切

先录最难的八小节，而不是从头录到尾。把独奏、弱奏、渐强单独排时间，齐奏与长音留给采样。真录前用采样做一版完整 mockup，让乐手听到目标，而不是只看到谱。录音当天先排难段，不按谱面顺序走，省下的是反复找感觉的时间。

## mockup 的陷阱

全部对齐到网格、每个音都满力度、渐强画成直线，听起来干净，却没有呼吸。真乐队进来后，指挥会按乐句而不是按格子处理，原来的 mockup 反而成了限制。[[glossary:dynamics|力度]]写得太满，乐手没有余地。把 mockup 当参考，不要当标准答案。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["D3","A3","D4","F4","A4"],"label":"弦乐组的一条连线","label_en":"A string section line","hint":"先听合成近似，再切到采样，注意音头与尾音哪一处更整齐","hint_en":"Hear the synth first, then the sampled strings, and notice which attack and tail sound too even"}
```
:::

::: en
With one day of string sessions, the bar is not the whole score; it is the few legato and soft phrases that samples never quite deliver.

## Start with the use

Will the film be revised ten times or delivered once? Are players visible on screen? Is the music background or foreground? Those answers set the ratio of live playing. An advert with constant retiming is cheaper fully sampled; a documentary that credits players earns credibility from the instruments you record. Decide the use before the timbre.

## Where dynamics and legato differ

Samples split dynamics into layers and crossfade between them. Write a long crescendo and the patch changes layer at some point, so the ear hears a different recording. A real crescendo is continuous and carries bow speed, breath and room. Legato is the same story: sampled legato uses pre-recorded transitions, which show a seam at fast speeds and sound too even at slow ones.

## Which parts are worth recording

Solo strings, solo woodwind, brass swells and pop-string slides are the hardest to replace. Inner sustains, percussion and pads already buried in the mix are usually fine sampled. Spend the budget on solos that will be heard rather than spreading it evenly. Mark those solo phrases in the score instead of looking for them after the session.

| Option | Suits | Revision cost | Risk |
|---|---|---|---|
| All samples | Adverts, previews, frequent cuts | Low | Layer breaks, legato seams |
| Live solos plus sampled band | Songs, documentaries | Medium | Solo and sample room do not match |
| Section sessions plus samples | Mid-budget film | Medium-high | Edit points and breaths misalign |
| Full live orchestra | Albums, cinema releases | High | One changed note means new players |

## Splitting the budget

Record the hardest eight bars first, not the piece from beginning to end. Schedule solos, soft passages and swells separately, and leave tuttis and sustains to samples. Before the session, make a complete sampled mockup so the players hear the target rather than only reading it. Start the day with the hardest passages instead of running the score in order, and save the time normally spent finding the feel.

## The mockup trap

Everything on the grid, every note at full velocity, every crescendo drawn as a straight line: it sounds clean and has no breath. When the players arrive, the conductor shapes phrases rather than bars, and the mockup becomes a limit instead of a guide. Dynamics written at full tilt leave no room. Treat the mockup as a reference, not as the answer.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["D3", "A3", "D4", "F4", "A4"], "label": "A string section line", "label_en": "A string section line", "hint": "Hear the synth first, then the sampled strings, and notice which attack and tail sound too even", "hint_en": "Hear the synth first, then the sampled strings, and notice which attack and tail sound too even"}
```
:::
