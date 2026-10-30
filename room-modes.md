---
id: room-modes
site: prod
cat: A5
title: 房间模式与驻波
title_en: Room Modes and Standing Waves
summary: 房间在低频形成驻波，几个音被抬高，另几个被抵消。
summary_en: Parallel walls trap low frequencies in standing waves, boosting some notes and cancelling others.
level: standard
tags: [驻波, 房间模式, 低频, 轴向模式, 声学处理]
tags_en: [standing waves, room modes, low end, axial modes, acoustic treatment]
alias: [驻波, 房间模式, 轴向模式, standing wave, room mode]
links:
  - "[[glossary:room-mode]]"
  - "[[glossary:bass-trap]]"
  - "[[glossary:room-treatment]]"
  - "[[instrument:double-bass]]"
instances:
  - cyberhymnal-000527 | 赞美诗《Veni Emmanuel》的低音声部，持续音适合暴露房间的轴向模式（C1）
  - pdmx-000801 | 低音提琴协奏曲的钢琴改编，低音区旋律清楚，能逐个音比较房间响应（C1）
  - pdmx-000237 | 钢琴与贝斯的爵士，低音线移动慢，便于听出某一音上的驻波（C1）
sources:
  - Everest, F. Alton，Master Handbook of Acoustics（McGraw-Hill）— 房间模式章节核对，未引用
  - Newell, Philip，Recording Studio Design（Focal Press）— 小房间低频处理章节核对，未引用
updated: 2026-10-28
---

::: zh
## 问题
低音在某几个音上轰头，换一个音又像被抽走；挪动三十厘米，结论全变。这不是音箱频响坏了，而是房间在固定频率上形成了驻波。

## 物理或房间
两片平行墙面之间会形成轴向驻波，频率为 n 乘声速除以两倍间距。四米长的房间，轴向模式约在 43、86、129 Hz。声源与听音位置落在压力腹点时最响，落在节点时最弱。房间越小，低频问题越集中在少数几个音上。

## 做法与判断
先量长宽高，算出三个方向的轴向模式并列表。把音箱与听音位从正中、从墙边挪开，避开明显节点；低频陷阱放在压力最大的墙角。用扫频确认峰与谷，窄而深的谷不要用均衡硬提，那是抵消。

## 听什么
播缓慢的低音扫频，或只用贝斯与底鼓的段落。某个音明显变厚、拖尾变长，记下频率；再前后左右移动头部，若响度变化很大，就是驻波。换到房间另一角，峰谷位置会移动。

## 常见误解
吸音棉不等于低频陷阱，薄棉对几十赫兹几乎无效。均衡可以压峰，却很难填谷。大房间也有模式，只是频率更低、分布更密。

```audiolab
{"type":"instrument","gm":"Contrabass","synth":"bowed","phrase":["E1","F1","G1","A1","B1","C2"],"label":"低音半音阶，逐个音听房间","label_en":"Low chromatic notes, one room at a time","hint":"在房间里播这几个低音，注意哪一个明显更响或拖尾更长；移动听音位置再听一遍。","hint_en":"Play these low notes in the room and notice which one is louder or rings longer; move your listening position and repeat."}
```
:::

::: en
## The problem
One bass note booms, the next seems hollow, and moving thirty centimetres changes the verdict. The speaker is not broken; the room has standing waves at fixed frequencies.

## Physics or room
Parallel walls form axial modes at n times sound speed divided by twice the spacing. A four-metre room has modes near 43, 86 and 129 Hz. Sound is loudest at pressure antinodes and weakest at nodes; small rooms crowd problems into fewer notes.

## Practice and judgement
Measure the room, calculate axial modes and list them. Move speakers and listener away from the centre and walls to avoid nodes; put bass traps where pressure peaks. Confirm by sweep, and never boost a deep null with EQ.

## What to listen for
Play a slow bass sweep, or only bass and kick. When one note thickens and rings longer, note the frequency; move your head. A large level change means a standing wave. Repeat in another corner.

## Common misunderstandings
Foam is not a bass trap; thin foam does almost nothing at tens of hertz. EQ can cut a peak but rarely fills a null. Large rooms have modes too, just lower and denser.

```audiolab
{"type":"instrument","gm":"Contrabass","synth":"bowed","phrase":["E1","F1","G1","A1","B1","C2"],"label":"Low chromatic notes, one room at a time","label_en":"Low chromatic notes, one room at a time","hint":"Play these low notes in the room and notice which one is louder or rings longer; move your listening position and repeat.","hint_en":"Play these low notes in the room and notice which one is louder or rings longer; move your listening position and repeat."}
```
:::
