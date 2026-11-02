---
id: drum-miking
site: prod
cat: A4
order: 360
title: 鼓组拾音
title_en: Drum Kit Miking
summary: 鼓组录得脏，先查鼓皮、相位与串音，再换话筒
summary_en: A dirty drum sound is usually tuning, phase and bleed before it is the microphone.
level: standard
tags: [鼓组, 拾音, 相位, 串音, 房间话筒]
tags_en: [drums, miking, phase, bleed, room mic]
alias: [鼓组拾音, 鼓录音, 架子鼓录音, 鼓话筒摆位, drum miking, drum recording]
links:
  - "[[instrument:drum-kit]]"
  - "[[instrument:snare-drum]]"
  - "[[instrument:bass-drum]]"
  - "[[instrument:cymbals]]"
  - "[[glossary:phase-check]]"
  - "[[glossary:polar-pattern]]"
instances:
  - groove-000010 | 放克鼓组节奏参照，不包含近讲话筒串音或相位记录（C1） | Funk-drum rhythm without close-mic spill or phase recordings (C1)
  - groove-000281 | 爵士三拍鼓型的ride声部参照，不是镲片话筒测试（C1） | Jazz-triple-meter ride part, not a cymbal-microphone test (C1)
  - groove-000684 | 6/8鼓型的配器参照，没有近点与房间话筒的对照（C1） | A 6/8 drum arrangement without close and room microphone comparisons (C1)
sources:
  - "https://www.shure.com/en-US/docs/education/Microphone-Techniques-for-Recording"
  - Eargle, John，The Microphone Book（Focal Press）— 鼓与打击乐拾音
  - Bartlett, Bruce，Practical Recording Techniques（Focal Press）— 鼓组摆位与串音
  - Mike Senior，Recording Secrets for the Small Studio（Focal Press）— 小房间鼓录音
updated: 2026-11-02
---

::: zh
## 先让鼓组自己成立

先检查鼓的调音、响弦、硬件杂响和演奏平衡，再选择话筒。录一小段正常力度的表演，确认问题来自乐器、房间还是拾音链；不要用固定的换鼓皮或换设备顺序代替实际检查。

## 逐件摆位，一支话筒一件活

| 位置 | 距离与角度 | 常见毛病 |
|---|---|---|
| 底鼓 | 开孔内 2–5 厘米，偏鼓心 | 气流扑麦、踏板噪声 |
| 军鼓上 | 鼓皮上方 3–5 厘米，指向鼓心偏边 | 太近只剩鼓皮，没有鼓腔 |
| 军鼓下 | 响弦下 5–8 厘米 | 底鼓串音、响弦沙沙声 |
| 踩镲 | 上方 10–15 厘米，朝外 | 军鼓串音 |
| 通鼓 | 鼓皮上方 3–5 厘米 | 相邻鼓与镲片串音 |
| 头顶 | 镲片上方 40–60 厘米，左右对称 | 高度不一，相位打架 |
| 房间 | 2–4 米，离地 2 米以上 | 角落低频堆积 |

表中距离只能作为试验起点。移动话筒会同时改变目标声、串音、气流和乐器不同发声部位的比例；退远不保证减少串音。每次只改距离或角度之一，回听同样的鼓点，并为鼓槌和镲片留出安全空间。

## 相位与门，先对齐再降噪

分别独听与合听近讲、头顶和房间话筒，检查极性及时间关系。波形移动对齐是一种编辑选择，可能改变原本需要的空间感，不应自动用于所有话筒。使用门限时检查是否截掉弱击或镲片尾音，释放时间按实际衰减设置，不套固定毫秒值。

## 房间话筒不是备选

房间话筒的位置按房间、扩声和目标空间比例选择，不必固定在鼓手前方某个高度。加入时先匹配音量，听低频、军鼓位置和镲片是否改变；比较极性或微调时间时，保留未移动版本作为参照。

## 什么时候不该加话筒

爵士、复古摇滚、小房间，一支话筒或一对头顶反而更完整，鼓手自己平衡力度，录音师只负责接住。反过来，鼓皮状态差、镲片太亮、房间又小又硬，多支话筒只会把问题放大：串音更多，相位更难对，混音时每一轨都要修。先处理鼓、房间和演奏，实在不行就用采样替换，别在相位上耗一整天。

```audiolab
{"type":"instrument","gm":"Melodic Tom","synth":"perc","phrase":["C2","G2","C2","D2","G2","C3"],"label":"鼓点音色参照","label_en":"Drum-hit timbre reference","hint":"合成鼓音不保留原始话筒距离或串音。实际摆位比较应录同一套鼓并保留各话筒的独立轨道。","hint_en":"Synthesized drums do not retain original mic distance or spill. Record the same kit with separate microphone tracks to compare placement."}
```
:::

::: en
## Let the kit sound right first

Check tuning, snare wires, hardware rattles and performance balance before choosing microphones. Record a short passage at normal playing level to distinguish instrument, room and signal-chain problems rather than following a fixed replacement order.

## One mic per job

| Position | Distance and angle | Usual trouble |
|---|---|---|
| Kick | 2–5 cm inside the port, off centre | Air blasts, pedal noise |
| Snare top | 3–5 cm above the head, aimed off centre | Too close loses the shell |
| Snare bottom | 5–8 cm under the wires | Kick bleed, wire hiss |
| Hi-hat | 10–15 cm above, angled outward | Snare bleed |
| Toms | 3–5 cm above the head | Neighbouring drums and cymbals |
| Overheads | 40–60 cm above the cymbals, symmetrical | Uneven height, phase fights |
| Room | 2–4 m out, 2 m up | Low-end pile-up in corners |

Distances in the table are trial starting points. Moving a microphone changes wanted sound, spill, airflow and the balance of radiating surfaces; moving farther away does not guarantee less spill. Change distance or angle separately, compare the same hits, and leave clearance for sticks and cymbals.

## Phase and gates, in that order

Listen separately and together to close, overhead and room microphones, checking polarity and timing. Waveform alignment is an editing choice that may alter wanted spatial character, not an automatic requirement. With gates, check quiet hits and cymbal tails; set release for actual decay rather than a fixed millisecond value.

## The room mic is not optional

Choose room-microphone position for the room, PA and desired ambience rather than one prescribed location. Add it at a controlled level and listen for changes in bass, snare position and cymbals. Keep an unshifted version while comparing polarity or timing adjustments.

## When not to add mics

Jazz, retro rock and small rooms often sound more complete with one mic or a single overhead pair. The drummer balances the kit and the engineer just captures it. The opposite is true when the heads are tired, the cymbals are harsh and the room is small and hard: more microphones only amplify the problem with more bleed, harder phase work and another track to fix at mixdown. Fix the kit, the room and the playing first; if that fails, replace the shells with samples rather than spending the day chasing phase.

```audiolab
{"type":"instrument","gm":"Melodic Tom","synth":"perc","phrase":["C2","G2","C2","D2","G2","C3"],"label":"Drum-hit timbre reference","label_en":"Drum-hit timbre reference","hint":"Synthesized drums do not retain original mic distance or spill. Record the same kit with separate microphone tracks to compare placement.","hint_en":"Synthesized drums do not retain original mic distance or spill. Record the same kit with separate microphone tracks to compare placement."}
```
:::
