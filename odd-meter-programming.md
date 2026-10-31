---
id: odd-meter-programming
site: prod
cat: B2
order: 370
title: 奇数拍编程：分组、重音与网格
title_en: "Programming Odd Meters: Grouping, Accent and Grid"
summary: 奇数拍靠分组与重音成立，少打一拍只会得到瘸的 4/4。
summary_en: Odd meters are built from grouping and accent; a missing beat only gives you a limping 4/4.
level: standard
tags: [奇数拍, 5/4, 7/8, 重音, 网格]
tags_en: [odd meter, 5/4, 7/8, accent, grid]
alias: [奇数拍, 奇数拍编程, 5/4 拍, 7/8 拍, odd meter, odd time]
links:
  - "[[glossary:meter]]"
  - "[[glossary:additive-rhythm]]"
  - "[[glossary:accent]]"
  - "[[glossary:beat]]"
instances:
  - abcmisc-000776 | 《Dospatsko Horo》是 7/8，按 3+2+2 数，重音落在第 1、4、6 个八分（C1）
  - abcmisc-000748 | 《Daronee》5/4，同一小节可按 3+2 或 2+3 数，换分组听重音怎么挪（C1）
  - abcmisc-000860 | 《Jambolsko Pajdusko》5/8，按 2+3 数，和 5/4 的 3+2 对照（C1）
  - abcmisc-000800 | 《Gankino》11/8，按 2+2+3+2+2 分组，练长小节不丢拍（C1）
sources:
  - Cooper & Meyer, The Rhythmic Structure of Music（节奏结构教材）
  - Kostka, Payne & Almén, Tonal Harmony，拍号与非对称拍章节（和声教材）
  - Ableton Live 用户手册，拍号、节拍器与网格设置（软件文档）
updated: 2026-10-31
---

::: zh
## 拍号只是标签，分组才是内容

把 4/4 的一拍删掉，得到的是瘸的 4/4，不是 7/8。奇数拍的听感来自分组：5/4 走 3+2 或 2+3，7/8 走 3+2+2 或 2+2+3，5/8 常走 2+3，11/8 常走 2+2+3+2+2。同一串八分音符，换一种分组，重音、舞步、低音落点全变。写之前先用嘴数一遍；嘴上数不顺的分组，画进钢琴卷帘也不会顺。

## 分母决定怎么数

7/8 与 5/8 按八分音符数，5/4 与 7/4 按四分音符数。上排数字相同、下排不同，数法不能共用。速度也要说清单位：7/8 标 120 BPM，指的是四分音符还是八分音符，实际速度差一倍。跟鼓手或编曲伙伴沟通时，写 3+2+2 比只写 7/8 有用，因为分组直接告诉对方重音在哪。

## 常用分组与落点

| 拍号 | 分组 | 重音落点 | 常见来源 |
|---|---|---|---|
| 5/4 | 3+2 | 1、4 | 巴尔干舞曲、前卫摇滚 |
| 5/4 | 2+3 | 1、3 | 叙事段落、慢速 riff |
| 5/8 | 2+3 | 1、3（八分） | 帕伊杜什科 |
| 7/8 | 3+2+2 | 1、4、6（八分） | 巴尔干霍罗 |
| 7/8 | 2+2+3 | 1、3、5（八分） | 民谣、电影配乐 |
| 11/8 | 2+2+3+2+2 | 1、3、5、8、10（八分） | 科普尼察 |

分组不是唯一的写法，同一首曲子可以在段落之间换一种数法，听感会立刻从“前长后短”变成“前短后长”。写谱时把分组标在拍号旁边，比事后加一排重音记号更省事。

## 网格、循环与量化

先把拍号设对，再设网格：5/4 用四分或八分网格，7/8 与 5/8 用八分网格，11/8 可以切到十六分画细一点。循环长度按小节算，7/8 一小节就是七个八分，用秒数凑会在接缝处错位。底鼓放每组第一拍，军鼓放第二组或第三组头上；留一个空比每拍都敲更容易数。量化强度留一点余量，全部贴死会让分组听起来像节拍器。素材如果是按 4/4 弹进来的，先改拍号再重录，量化只会把错位固定下来。

## 哪里会坏

舞曲、广告、儿歌里，奇数拍会让听众找不到落脚点，除非分组本身成为钩子。把 7/8 写成 4/4 加一个休止，编辑时看不出，演出时鼓手会迷路。速度单位标错，DAW 与谱面会差一倍。最常见的失败是 5/4 被弹成 4/4 加抢拍，量化之后听着整齐，重音却始终错位。

```audiolab
{"type":"instrument","gm":"Electric Bass (finger)","synth":"plucked","phrase":["E2","B2","B2","E3","B2","E3","B2"],"label":"7/8 的 3+2+2","label_en":"3+2+2 in 7/8","hint":"七个八分音，第 1、4、6 个更高；先拍腿数 3+2+2，再听低音","hint_en":"Seven eighths with the 1st, 4th and 6th accented; count 3+2+2 on your leg first"}
```
:::

::: en
## The time signature is a label; the grouping is the music

Delete one beat from 4/4 and you get a limping 4/4, not 7/8. Odd meters are heard through their grouping: 5/4 runs 3+2 or 2+3, 7/8 runs 3+2+2 or 2+2+3, 5/8 usually runs 2+3, and 11/8 usually runs 2+2+3+2+2. Change the grouping of the same string of eighth notes and the accents, the dance step and the bass landing points all change. Count it aloud before writing anything; a grouping your mouth cannot follow will not flow in the piano roll either.

## The denominator decides how to count

Count 7/8 and 5/8 in eighth notes, and 5/4 and 7/4 in quarter notes. The top number can match while the bottom one changes, so the counting method cannot be shared. State the tempo unit as well: a 120 BPM marking in 7/8 may refer to the quarter or the eighth, a factor of two in real speed. When talking to a drummer or an arranging partner, writing 3+2+2 is more useful than writing 7/8, because the grouping tells them where the weight goes.

## Common groupings and where they land

| Meter | Grouping | Accents | Common source |
|---|---|---|---|
| 5/4 | 3+2 | 1, 4 | Balkan dance, prog rock |
| 5/4 | 2+3 | 1, 3 | Narrative sections, slow riffs |
| 5/8 | 2+3 | 1, 3 (eighths) | Paidushko |
| 7/8 | 3+2+2 | 1, 4, 6 (eighths) | Balkan horo |
| 7/8 | 2+2+3 | 1, 3, 5 (eighths) | Folk, film score |
| 11/8 | 2+2+3+2+2 | 1, 3, 5, 8, 10 (eighths) | Kopanitsa |

Grouping is not fixed for a whole piece: a section can switch from 3+2 to 2+3, and the feel turns from long-short to short-long at once. Write the grouping next to the time signature; it saves a row of accent marks added after the fact.

## Grid, loop length and quantise

Set the meter before the grid: 5/4 works on quarters or eighths, 7/8 and 5/8 on eighths, and 11/8 may need sixteenths to draw the detail. Set loop length in bars. One bar of 7/8 is seven eighths, and building it from seconds will drift at the seam. Put the kick on the first beat of each group and the snare on the head of the second or third group; leaving a gap is easier to count than filling every slot. Keep some quantise strength in reserve, because snapping everything flat makes the grouping sound like a metronome. If the take was played in 4/4, change the meter and play it again; quantising only locks the wrong accents in place.

## Where it breaks

In dance music, advertising and children's songs, an odd meter leaves listeners without a foothold unless the grouping itself becomes the hook. Notating 7/8 as 4/4 plus a rest looks fine in the edit and loses the drummer on stage. Mark the tempo unit wrongly and the DAW and the score end up a factor of two apart. The most common failure is a 5/4 played as 4/4 plus a rushed beat: after quantising it sounds tidy, while the accents stay wrong throughout.

```audiolab
{"type":"instrument","gm":"Electric Bass (finger)","synth":"plucked","phrase":["E2","B2","B2","E3","B2","E3","B2"],"label":"3+2+2 in 7/8","label_en":"3+2+2 in 7/8","hint":"Seven eighths with the 1st, 4th and 6th accented; count 3+2+2 on your leg first","hint_en":"Seven eighths with the 1st, 4th and 6th accented; count 3+2+2 on your leg first"}
```
:::
