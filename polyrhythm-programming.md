---
id: polyrhythm-programming
site: prod
cat: B2
order: 371
title: 复节奏编程：3 对 4 与层间对位
title_en: "Programming Polyrhythms: Three Against Four and Layered Counterpoint"
summary: 3 对 4 先找十二格公共网格，再让两层各自数得通。
summary_en: Three against four starts with a shared twelve-step grid, then each layer has to count on its own.
level: standard
tags: [复节奏, 3 对 4, 对位, 网格, 层]
tags_en: [polyrhythm, 3 against 4, counterpoint, grid, layers]
alias: [复节奏, 复节奏编程, 三对四, 交叉节奏, polyrhythm, cross rhythm]
links:
  - "[[glossary:polyrhythm]]"
  - "[[glossary:cross-rhythm]]"
  - "[[glossary:hemiola]]"
  - "[[glossary:tuplet]]"
instances:
  - atepp-001261 | 肖邦《Fantaisie-Impromptu》，右手十六分音符对左手三连音，4 对 3 的典型（C1）
  - atepp-000492 | 李斯特《Un sospiro》，三连音琶音托着二连音旋律，3 对 2 的层次清楚（C1）
  - abcmisc-000743 | 《Daichovo Horo》9/8 按 2+2+2+3 分组，三拍组与二拍组在同一小节里交错（C1）
sources:
  - Peter Magadini, Polyrhythms — The Musician's Guide（教材）
  - Toussaint, The Geometry of Musical Rhythm（节奏结构教材）
  - Ableton Live 用户手册，网格分辨率与连音符（软件文档）
updated: 2026-10-31
---

::: zh
## 先算公共网格

3 对 4 的公共格是十二：从第一格起，三的那层每隔四格落一次，四的那层每隔三格落一次，第十二格后重新对齐。5 对 4 要二十格，3 对 2 只要六格。先算清这个数，再决定网格分辨率。用直十六分画 3 对 4，总有一层落在格子之间；把一小节切成十二份，两层都能落在整格。这个数算错一次，后面的对齐都会偏。

## 每条轨用各自的网格

底鼓与贝斯留在 4/4 的十六分网格，另一条轨用三连音或五连音。拍号不用改，改的是每条轨的网格与音符时值。两条轨都量化到同一个网格，对位会被抹平；至少让其中一条保留演奏的偏差。DAW 的连音符开关通常只作用于当前轨，切轨时先确认网格，别把三连音画到直十六分上。

## 层间对位

| 比例 | 公共格 | 听感 | 常见写法 |
|---|---|---|---|
| 3:2 | 6 | 滚动、摇摆 | 6/8 与 3/4 交替、爵士八分 |
| 4:3 | 12 | 稳定但悬 | 左手三连音、右手十六分 |
| 3:4 | 12 | 重心相反 | 鼓组对旋律 |
| 5:4 | 20 | 紧张、不易数 | 现代配乐、前卫摇滚 |

3:4 与 4:3 的公共格相同，差别在谁先落、谁更密。比例不是越复杂越好：3:2 已经足够给一段 4/4 第二个重心；5:4 放在快速度里，听众只会听到乱。写的时候先决定哪一层负责锚点，再决定另一层往哪里偏。

## 先分开听，再合起来

单独听每一层，确认它自己数得通；再合起来，听重合的那一拍是否落在该落的地方。低频层通常负责锚点，让它简单；复杂的那层放中高频，才有空间被听见。单声道再检查一遍，别让宽度掩盖拍点冲突。两层都成立之后再考虑第三层，三层以上要有明确的主次，否则每层都在抢耳朵。

## 哪里会坏

最常见的失败是把两条轨都量化到十六分：三连音被拉直，对位消失，只剩一个切分节奏。第二个失败是层数太多，每层都在动，听众抓不到任何一层。第三个失败是频率打架，两层都占低频，公共网格算得再准也听不出来。先做两层，确认各自成立，再考虑加层。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C2","E4","E4","G5","C2","E4","G5","E4","C2","G5","E4","E4"],"label":"十二格里的 3 与 4","label_en":"Three and four inside twelve steps","hint":"低音 C 每四格落一次，高音 G 每三格落一次，第十二格后重新重合","hint_en":"The low C lands every four steps, the high G every three, and they realign after the twelfth"}
```
:::

::: en
## Find the shared grid first

Three against four shares twelve steps: from the first step, the three layer lands every four steps and the four layer every three, then they realign after the twelfth. Five against four needs twenty steps; three against two needs only six. Work out that number before choosing a grid resolution. Drawn on straight sixteenths, three against four always leaves one layer between grid lines; cut the bar into twelve and both layers land on whole steps. Get the number wrong once and every alignment after it drifts.

## Each track keeps its own grid

Keep the kick and bass on the 4/4 sixteenth grid and put the other track on triplets or quintuplets. The meter stays put; what changes is each track's grid and note values. Quantise both tracks to the same grid and the counterpoint is erased, so let at least one track keep some of its played deviation. A DAW's tuplet setting usually applies only to the active track; check the grid when you switch tracks, or triplets end up drawn on straight sixteenths.

## Layer against layer

| Ratio | Shared steps | Sound | Common writing |
|---|---|---|---|
| 3:2 | 6 | Rolling, swaying | 6/8 against 3/4, jazz eighths |
| 4:3 | 12 | Stable but suspended | Left-hand triplets, right-hand sixteenths |
| 3:4 | 12 | Opposite weight | Drums against melody |
| 5:4 | 20 | Tense, hard to count | Modern scores, prog rock |

3:4 and 4:3 share the same grid; the difference is who starts first and who is denser. Complexity is not a virtue by itself: 3:2 is enough to give a 4/4 section a second centre of gravity, while 5:4 at a fast tempo mostly reads as confusion. Decide which layer anchors before deciding where the other one leans.

## Hear each layer alone, then together

Listen to each layer on its own and check that it counts. Then put them together and hear whether the shared hit lands where it should. The low layer usually anchors, so keep it simple; put the complex layer in the midrange where it has room. Check in mono so width does not hide a clash. Add a third layer only after two already stand, and give three or more layers a clear hierarchy, or every layer fights for the ear.

## Where it breaks

The usual failure is quantising both tracks to sixteenths: triplets get pulled straight, the counterpoint disappears, and only a syncopated rhythm remains. The second failure is too many layers, with everything moving and nothing for the ear to hold. The third is frequency collision: if both layers occupy the low end, even a correct shared grid will not be heard. Build two layers, confirm each stands alone, then consider a third.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C2","E4","E4","G5","C2","E4","G5","E4","C2","G5","E4","E4"],"label":"Three and four inside twelve steps","label_en":"Three and four inside twelve steps","hint":"The low C lands every four steps, the high G every three, and they realign after the twelfth","hint_en":"The low C lands every four steps, the high G every three, and they realign after the twelfth"}
```
:::
