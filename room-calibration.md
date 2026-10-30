---
id: room-calibration
site: prod
cat: A5
title: 房间校准
title_en: Room Calibration
summary: 校准让房间的偏差可听、可测、可补偿，而不是靠猜。
summary_en: Calibration makes room errors audible, measurable and correctable instead of a matter of guesswork.
level: standard
tags: [房间校准, 测量, 均衡, 驻波, 参考曲]
tags_en: [room calibration, measurement, EQ, room modes, reference tracks]
alias: [校准, 房间校正, 声学校准, calibration, room correction]
links:
  - "[[glossary:room-treatment]]"
  - "[[glossary:room-mode]]"
  - "[[glossary:reference-track]]"
  - "[[glossary:monitoring]]"
instances:
  - pdmx-002760 | 《Corcovado》钢琴与尼龙弦吉他，编制小，校准后容易判断旋律与低频（C1）
  - atepp-000369 | 格里格《夜曲》，独奏钢琴，能听出校准对中高频的副作用（C1）
  - pdmx-000801 | 低音提琴协奏曲的钢琴改编，低频连续，适合检查校准是否只压峰不填谷（C1）
  - essen-000191 | 单声部民歌，用来检查校准后人声是否变薄（C1）
sources:
  - Toole, Floyd，Sound Reproduction（Focal Press）— 房间校正与听觉章节核对，未引用
  - Everest, F. Alton，Master Handbook of Acoustics（McGraw-Hill）— 测量与均衡章节核对，未引用
updated: 2026-10-28
---

::: zh
## 问题
自动校准把频响拉平后，低频反而更空，声像也散了。校准不是把曲线修成直线，而是分清哪些偏差能修、哪些只能靠摆位与处理。

## 物理或房间
房间传输函数由直达声、早期反射与模态共同决定。低频模态区，某个谷往往是抵消，均衡硬提只会增加失真与邻近频率的峰；中高频的窄谷多来自反射，应优先处理反射面。测量话筒要加载校准文件，单点测量只代表一个位置。

## 做法与判断
先摆位、再做声学处理，最后才用均衡。测至少五个位置，取平均看趋势；只削峰，不填深谷。校准限制在低频，中高频交给摆位。校准后放几首熟悉的参考曲，确认人声不薄、低频不空、声像不散。

## 听什么
播扫频，听校准前后哪些峰被压下去、哪些谷仍在。放一段独奏人声，确认中频没有被过度校正。再听贝斯与底鼓，判断低频是变紧还是变轻。最后按单声道检查声像。

## 常见误解
自动校准不能替代声学处理。频响平直不等于好听，时域行为同样重要。测量话筒不加载校准文件，读数不可信。一次测量不足以代表整个听音区。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C3","E3","G3","C4","G4"],"label":"校准前后，同一段参考","label_en":"The same reference, before and after calibration","hint":"校准前后播同一段，先匹配响度，再听人声与低频是否更稳。","hint_en":"Play this before and after calibration, match loudness first, then judge whether voice and bass are steadier."}
```
:::

::: en
## The problem
Auto-calibration flattens the response, then the bass feels hollow and the image drifts. Calibration is not a straight line; it is knowing which errors can be corrected.

## Physics or room
The room transfer function combines direct sound, early reflections and modes. In the modal region a dip is often cancellation, and boosting it adds distortion and neighbouring peaks; narrow dips come from reflections, so treat the surface. Measurement mics need their calibration file, and one point represents one seat.

## Practice and judgement
Place speakers, treat the room, then equalise. Measure at least five positions and average the trend; cut peaks, leave deep nulls alone. Limit correction to the bass and let placement handle the rest. Finish on familiar references, checking vocal body, bass weight and image.

## What to listen for
Sweep and hear which peaks fall and which nulls remain. On a solo voice, check that the midrange is not over-corrected. On bass and kick, decide whether the low end got tighter or merely quieter. Check mono.

## Common misunderstandings
Auto-calibration cannot replace treatment. A flat response is not the same as good sound; time behaviour matters too. A measurement mic without its calibration file is unreliable. One measurement cannot represent the whole area.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C3","E3","G3","C4","G4"],"label":"The same reference, before and after calibration","label_en":"The same reference, before and after calibration","hint":"Play this before and after calibration, match loudness first, then judge whether voice and bass are steadier.","hint_en":"Play this before and after calibration, match loudness first, then judge whether voice and bass are steadier."}
```
:::
