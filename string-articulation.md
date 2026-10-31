---
id: string-articulation
site: prod
cat: A3
title: 弦乐奏法与记谱
title_en: String Articulation and Notation
summary: 连奏、断奏、顿弓与滑音都要写成演奏动作，不能只靠一个力度记号。
summary_en: Legato, staccato and slides are playing actions to write down, not effects left to a dynamic mark.
level: standard
tags: [配器, 弦乐, 弓法, 记谱]
tags_en: [orchestration, strings, bowing, notation]
alias: [弦乐奏法, 弓法, 连奏断奏, 滑音记谱, string articulation, bowing]
order: 330
links:
  - "[[glossary:legato]]"
  - "[[glossary:staccato]]"
  - "[[glossary:glissando]]"
  - "[[instrument:violin]]"
  - "[[instrument:cello]]"
instances:
  - musicnet-000097 | 贝多芬《第八弦乐四重奏》第一乐章，四把琴各占一个通道，换弓与音头都露在外面 | Beethoven's Eighth Quartet, first movement, four separate channels expose every bow change
  - musicnet-000067 | 贝多芬《第十五弦乐四重奏》第一乐章，长线条乐句可听连奏在哪里换弓 | Beethoven's Fifteenth Quartet, first movement, long lines reveal where the bow changes
  - pdmx-000065 | 巴赫《第一大提琴组曲》，单声部大提琴，任何音头与尾音都无处可藏 | Bach's First Cello Suite, a single line with no place to hide an attack or a release
sources:
  - Samuel Adler, The Study of Orchestration, W. W. Norton, 弦乐弓法与分奏章节
  - Norman Del Mar, Anatomy of the Orchestra, Faber, 弦乐组的弓法处理
  - Elaine Gould, Behind Bars, Faber, 弦乐奏法与连音线记谱
updated: 2026-10-31
---

::: zh
把整句写成一排没有起伏的长音，弦乐组只会还你一片没有方向的音墙。奏法写作从弓速、弓压与换弓点开始，音高只是其中一项。

## 先写弓，再写音

弦乐的可控项比键盘多：连弓、分弓、断奏、顿弓、跳弓、泛音、弱音器，以及靠码与靠指板。谱上只写力度，首席只能按习惯猜。把弓法、连音线、点与弓位写出来，一组人才有同一套动作。落笔前先决定这一句是一口气，还是一下一下，再排音高与和声。

## 连奏的缝在换弓处

[[glossary:legato|连奏]]也有缝。同一弓内的音靠手指落指，痕迹小；换弓、换弦时右手要提前。连音线该跨过句法单位，而不是每小节断一次。长音结尾留一点弓速，别让声音在换弓前先虚掉。四把琴写齐奏，换弓点要统一，否则同一旋律会出现四条不同的呼吸。

## 断奏不是一种

点、楔形、连音线下的点不是一回事。短分弓停在弦上，顿弓让弓咬住再放，跳弓让弓离弦弹回。速度越快步幅越小，慢速硬写跳弓只会变成一片噪声。MIDI 里只能用音长与力度近似：断奏写成十六分时值、力度抬高一档，比单纯缩短音符更接近。[[glossary:staccato|断奏]]的记号写清楚，排练才不用猜。

| 记号 | 演奏动作 | 适合速度 | MIDI 近似 |
|---|---|---|---|
| 连音线 | 一弓多音，换弦不换弓 | 中慢 | 音尾相接，CC11 平顺 |
| 点 | 短分弓，弓不离弦 | 中快 | 时值减半，力度加十左右 |
| 楔形 | 顿弓，咬住再放 | 中慢 | 时值更短，起音更重 |
| 直线加 gliss. | 换把滑音 | 任意 | 弯音轮或重叠级进 |
| 靠指板或靠码 | 音色变暗或变薄 | 任意 | 换音色或衰减高频 |

## 滑音与特殊弓位

滑音分两种：换把时手指沿弦移动是 [[glossary:portamento|portamento]]，按弦滑过所有音是 [[glossary:glissando|glissando]]。谱上要写起点、终点和时值，别只画一条斜线。靠指板、靠码、加弱音器、弓杆击弦都是音色指令，写上去之前先确认人数：一个人做是颜色，十个人做是另一件乐器。

## 写满之后坏在哪

分奏超过四部，每个声部都弱，音准开始漂；断奏铺满整段，弓法没有喘息；滑音每个乐句都来一次，听感发腻。采样库切换奏法还有延迟，弓法写得太碎，mockup 里会先吃掉音头。

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["G3","A3","B3","D4","G4"],"label":"五个音与它们的缝","label_en":"Five notes and the gaps between them","hint":"这条短句每个音之间都有缝，谱上的连音线要做的正是把缝收掉","hint_en":"Every note here is separated; a slur on the score exists to close those gaps"}
```
:::

::: en
Write a phrase as one flat sustained line and a string section gives you a wall of sound with no direction. Articulation starts with bow speed, bow pressure and where the bow changes; pitch is only one part of it.

## Bow first, pitch second

Strings offer more controls than a keyboard: slurred bowing, separate bows, staccato, martelé, spiccato, harmonics, mutes, and playing near the bridge or the fingerboard. A dynamic mark alone leaves the principal guessing. Write the bowing, slurs, dots and contact point, and the section shares one set of actions. Decide whether the phrase is one breath or a series of strokes before voicing the harmony.

## Legato has seams

Legato has seams too. Notes under one bow leave a small mark; a bow change or string crossing needs the right hand to prepare early. Slurs should span phrases, not stop at every barline. Keep a little bow speed at the end of a long note so the tone does not fade before the change. For a four-part unison, align the bow changes or the same line will breathe four different ways.

## Staccato is several things

A dot, a wedge and a dot under a slur are not the same. Short separate bows stay on the string, martelé bites and releases, spiccato lets the bow bounce. The faster the passage, the smaller the stroke; writing spiccato at a slow tempo only makes noise. MIDI can only approximate with length and velocity: a sixteenth-length note with one velocity step up gets closer than simply shortening the note.

| Mark | Action | Tempo | MIDI approximation |
|---|---|---|---|
| Slur | Several notes, one bow | Slow to moderate | Notes end to end, smooth CC11 |
| Dot | Short separate bow on the string | Moderate to fast | Half length, velocity plus ten |
| Wedge | Martelé, bite and release | Slow to moderate | Shorter length, harder attack |
| Line with gliss. | Shift slide | Any | Pitch bend or overlapping steps |
| Sul tasto or ponticello | Darker or thinner tone | Any | Change patch or roll off highs |

## Slides and contact points

A shift of the hand along the string is portamento; a finger sliding through every pitch is glissando. Notate the start, the end and the duration instead of drawing a diagonal line. Sul tasto, sul ponticello, mutes and col legno are colour instructions; count the players before using them. One player makes a colour, ten make a different instrument.

## Where it breaks

More than four divisions and every part is weak and drifting in pitch. Staccato across a whole page leaves no room to breathe. A slide in every phrase becomes a mannerism. Sample libraries also lag when switching articulations, and bowing written too finely loses its attacks in a mockup.

```audiolab
{"type": "instrument", "gm": "Violin", "synth": "bowed", "phrase": ["G3", "A3", "B3", "D4", "G4"], "label": "Five notes and the gaps between them", "label_en": "Five notes and the gaps between them", "hint": "Every note here is separated; a slur on the score exists to close those gaps", "hint_en": "Every note here is separated; a slur on the score exists to close those gaps"}
```
:::
