---
id: piano-miking
site: prod
cat: A4
order: 362
title: 钢琴拾音
title_en: Piano Miking
summary: 盖板决定宽度与亮度，两支话筒的间距决定单声道里还剩多少
summary_en: The lid sets width and brightness; the spacing of two mics decides what survives in mono.
level: standard
tags: [钢琴, 拾音, 立体声, 相位, 盖板]
tags_en: [piano, miking, stereo, phase, lid]
alias: [钢琴拾音, 钢琴录音, 三角钢琴录音, 钢琴话筒, piano miking, piano recording]
links:
  - "[[instrument:piano]]"
  - "[[glossary:stereo-technique]]"
  - "[[glossary:phase]]"
  - "[[glossary:room-treatment]]"
instances:
  - atepp-000075 | 斯克里亚宾《幻想奏鸣曲》慢乐章，低音与高音琶音同现，两支话筒的平衡一耳朵可辨（C1）
  - giantmidi-003263 | 萨蒂《裸体歌舞》整体很轻，踏板与房间尾巴比音符更响（C1）
  - pdmx-000263 | 李斯特《超技练习曲》强奏多，低频与盖板反射容易让近点话筒过载（C1）
sources:
  - Eargle, The Microphone Book, 3rd ed., piano chapters
  - Everest, Master Handbook of Acoustics, low-frequency treatment in small rooms
  - DPA Microphones, 钢琴拾音指南（厂商文档）
updated: 2026-10-31
---

::: zh
## 先定盖板，再谈话筒

钢琴的声音有一半从盖板反射出来。全开最亮、最宽，也把天花板与墙面的毛病一起收进来；短撑让中频更实，适合流行伴奏；闭盖能隔离，音色却发闷，只能拆前挡板或把话筒伸进琴腹补救。先问这次要不要隔离，再定盖板，然后才轮得到话筒。

| 盖板 | 音色 | 隔离 | 话筒落点 |
|---|---|---|---|
| 全开 | 亮、宽、尾巴长 | 差 | 弦上方 20–30 厘米 |
| 短撑 | 中频实、宽度中等 | 中 | 偏中高音区，避开弦槌 |
| 闭盖 | 暗、近、缺空气 | 好 | 拆前挡板，或贴近音板 |

## 两支话筒的间距账

间隔摆法把高低音区各交给一支话筒，宽度最自然，代价是中间可能空。两支相距六十到一百厘米，录完按单声道听一遍。声速约每秒三百四十米，一毫秒差三十四厘米；间距越大，单声道折叠时中频掉得越早。XY 同点交叉最稳，宽度窄；ORTF 相距十七厘米、夹角一百一十度，介于两者之间。话筒别正对弦槌那一排，起音会尖；偏十到二十度，锤头、琴弦与音板的比例自己会回来。

## 房间和机械声也是素材

开盖的琴把声音往斜上方抛，天花板、侧墙和地板会一起进话筒。琴离墙半米以上，低频不会在琴腹下面积成一片；地毯、毛毡和琴凳上的布能压住踏板与衣服的杂音。独奏录音里，踏板抬起、制音器落下的声音属于演奏；给流行歌伴奏，同样的声音就是噪声，换摆位比降噪插件直接。

## 双话筒反而更糟的时候

小房间、琴靠墙、盖板全开，第二支话筒收到的多是两次反射，不是更多细节。单声道里变薄、低频左右跳、人声一进来钢琴就退，都是相位在作怪；加宽插件救不回来，只能移动话筒。独奏与古典需要琴体与空间，一支近点加一支两米外的房间话筒，往往比一对近点更有说服力。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["A1","E2","A2","E4","C#5","A5"],"label":"低音区与高音区的重量","label_en":"Weight from the bass to the top","hint":"先听低音的下潜与高音的起音，再想两支话筒各自偏向哪一边","hint_en":"Hear the bass weight and the treble attack, then picture which side each mic favours"}
```
:::

::: en
## The lid comes first

Half of a grand piano's sound leaves through the lid. Fully open is brightest and widest, and it also gathers every flaw in the ceiling and the walls. Half stick tightens the midrange for pop backing; a closed lid gives isolation but sounds boxy, so remove the front panel or reach in over the soundboard. Decide how much isolation the session needs, set the lid, then choose microphones.

| Lid | Tone | Isolation | Mic position |
|---|---|---|---|
| Fully open | Bright, wide, long tail | Poor | 20–30 cm above the strings |
| Half stick | Solid midrange, medium width | Medium | Over the mid-treble, off the hammers |
| Closed | Dark, close, no air | Good | Front panel off, or near the soundboard |

## What the spacing costs

A spaced pair hands the bass and treble registers to separate mics. The width is natural, at the price of a possible hole in the middle. Start 60 to 100 cm apart and listen back in mono. Sound travels about 340 m per second, which is 34 cm per millisecond; the wider the pair, the earlier the midrange drops when the channels fold together. XY is stable but narrow, and ORTF at 17 cm and 110 degrees sits between the two. Keep the mics off the hammer row or the attack turns brittle; angle them 10 to 20 degrees and hammer, string and soundboard settle into balance.

## The room and the mechanism are part of the take

An open lid throws sound up and sideways, so ceiling, walls and floor all reach the microphones. Keep the piano half a metre or more from the wall and the low end stops pooling under the soundboard. Rugs, felt and a cloth on the bench mute pedals, dampers and clothing. On a solo recording the pedal lift and the damper fall belong to the performance; behind a pop vocal the same noises are clutter, and moving a mic beats any denoiser.

## When two mics make it worse

Small room, piano against a wall, lid wide open: the second mic mostly collects another reflection rather than more detail. Thinning in mono, low end that wanders between speakers, a piano that steps back as soon as the vocal enters — phase explains all of it, and a widener will not repair it. Only moving a mic will. For solo and classical work that needs body and air, one close mic plus a room mic two metres out usually says more than a close pair.
:::
