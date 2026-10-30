---
id: tempo-map-and-meter
site: prod
cat: A1
title: 速度与拍号图
title_en: Tempo and Meter Maps
summary: 让网格跟着音乐走，而不是让音乐迁就网格。
summary_en: Mapping tempo and meter changes so the grid follows the performance instead of forcing rubato onto a fixed click.
level: standard
tags: [速度, 拍号, 网格]
tags_en: [tempo, meter, grid]
alias: [速度图, 拍号变化, 变速, tempo map]
links:
  - "[[glossary:tempo]]"
  - "[[glossary:meter]]"
  - "[[glossary:rubato]]"
instances:
  - atepp-001124 | 叙事曲速度自由，适合练按乐句画速度图
  - pdmx-000600 | 进行曲拍点稳定，适合练固定网格与重拍对齐
  - abcmisc-000139 | 三拍子民谣，适合练 3/4 与 4/4 的网格切换
sources:
  - 速度图与拍号变化的编辑方式，依通行 DAW 文档核查，未抄文本
  - 自由速度与固定网格的取舍，依配乐与指挥实践通识核查，未抄文本
updated: 2026-10-28
---

::: zh
网格是方便，不是法律。速度图让小节跟着演奏走，而不是把自由的演奏塞进固定节拍。

## 问题

不跟节拍器录下的钢琴会自然漂移，小节线落在错误的位置。硬量化到固定网格，又会削掉让音乐成立的推拉。配乐还有第二个问题，画面上的点必须落在精确的帧上。

## 做法

先选方向。自由素材先录，再用打点或检测把拍点找出来，让小节线贴住演奏。写作素材则先在指挥轨上画好渐快、渐慢与拍号变化，再录。速度图放在一条轨上，拍号只在小节线处改，网格才读得清。

## 参数与判断

速度精度到 0.01 BPM 已够用。别把每一次呼吸都画进去，图会变成噪声，编辑反而更慢。有画面时把音频锁到时间码，并保留一份固定速度的版本用于对照。

## 听什么

让节拍器跟着速度图走，听它是否漂移。它应当贴着演奏，而不是与之打架。如果每一遍都在同一个小节对不上，是图错了，不是演奏者错了。

```audiolab
{"type":"rhythm","sig":"3/4","pattern":"q q q","bpm":90,"label":"三拍子的网格","label_en":"A three-beat grid","hint":"先听三拍循环，再想象把其中一小节改成四拍","hint_en":"Hear the three-beat loop, then imagine one bar becoming four"}
```

## 常见误解

速度图不是多加几步的量化。画图不能让松散的演奏变紧，固定网格也不代表自由演奏是错的。拍号变化与速度变化是两件事，混淆会让后面所有小节错位。
:::

::: en
A grid is a convenience, not a law. A tempo map lets bars follow the performance instead of forcing a free take onto a fixed click.

## The problem

Recorded without a click, a piano take drifts and bar lines miss the beat. Quantised to a fixed grid, the same take loses the push and pull that made it musical. Film cues add a problem, because hits must land on exact frames.

## The practice

Choose a direction. For free material, record first, then tap or detect the beat and set bar lines to the performance. For composed material, draw tempo and meter changes on a conductor track before recording. Keep the map on one track, and change meter only at bar lines so the grid stays legible.

## Settings and judgement

A hundredth of a beat per minute is enough resolution for most work. Do not map every hesitation, or the map becomes noise and editing slows. Lock audio to timecode when picture is involved, and keep a fixed-tempo copy for comparison.

## What to listen for

Run the click against the map and listen for drift. It should track the performance without fighting it. If click and player disagree at the same bar every time, the map is wrong, not the player.

```audiolab
{"type": "rhythm", "sig": "3/4", "pattern": "q q q", "bpm": 90, "label": "A three-beat grid", "label_en": "A three-beat grid", "hint": "先听三拍循环，再想象把其中一小节改成四拍", "hint_en": "Hear the three-beat loop, then imagine one bar becoming four"}
```

## Common misunderstandings

A tempo map is not quantisation with extra steps. Mapping does not make a sloppy take tight, and a fixed grid does not make a free take wrong. Meter changes are not tempo changes, and confusing them shifts every following bar.
:::
