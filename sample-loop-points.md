---
id: sample-loop-points
site: prod
cat: B4
order: 494
title: 采样循环点
title_en: Finding Sample Loop Points
summary: 循环点要落在稳定段与整周期上，还要经得起移调和立体声检查。
summary_en: A loop point belongs on a steady, whole-cycle stretch, and must survive transposition and a stereo check.
level: standard
tags: [循环点, 采样, 波形, 移调]
tags_en: [loop point, sampling, waveform, transposition]
alias: [采样循环点, 循环起点, 循环终点, loop start, loop end, sustain loop]
links:
  - "[[glossary:sampler]]"
  - "[[glossary:timbre]]"
  - "[[instrument:samplers]]"
instances:
  - cyberhymnal-000000 | 风琴持续和弦没有起音后的衰减，循环接缝最容易听成脉动
  - pdmx-000070 | 巴伯《弦乐柔板》的长弦音，循环点错位会变成有规律的起伏
  - cyberhymnal-000005 | 四声部赞美诗的风琴长音，低音声部最适合检查循环是否漂移
sources:
  - SFZ Format 规范，loop_start、loop_end 与 loop_mode 的定义（公开规范）。
  - Native Instruments Kontakt 手册，Wave Editor 的循环与交叉淡化（官方文档）。
  - Ken C. Pohlmann, Principles of Digital Audio，采样回放与接缝。
updated: 2026-10-31
---

::: zh
一段两秒的风琴录音要撑住二十秒的和弦，靠的是让波形在一个稳定段里转圈，不是把样本拉长。循环点就是那个圈的起点和终点。

## 两秒的样本要撑二十秒

起音与衰减都留在循环外，只有中段最平稳的波形参与反复。循环点落进渐弱段，每转一圈电平就回升一次，长音会听成呼吸；落在颤音的某一侧，颤音被冻住，声音变得机械。循环区太短，反复会变成一个音高，叠在原来的音上。

## 循环的四种设置

| 形态 | 用在哪 | 听感风险 |
|---|---|---|
| 单向前进 | 最常见的持续音 | 接缝不在整周期时听到脉动 |
| 交替往返 | 波形左右对称的素材 | 方向反转处多出瞬态 |
| 释音循环 | note-off 之后的尾音 | 尾音被无限延长，像卡住 |
| 一次性 | 打击、拨弦、钢琴 | 循环反而破坏自然衰减 |

持续音用单向前进；交替往返多用于波形对称的合成素材，原声录音里少见。释音循环要单独设，别和持续循环共用同一对点。

## 找点的顺序

1. 在波形上找振幅稳定、泛音不变的中段，避开起音与衰减。
2. 起点与终点先对齐过零点，再微调到整周期。
3. 先不加淡化听接缝，有咔声再加 20 到 80 毫秒的交叉淡化。
4. 用频谱看有没有多出低频，或中频被梳状滤波挖空。
5. 上下各移一个八度，再听一遍。

对齐时看波形，也看频谱。拍频有时像音色，其实是两个相位不同的波形叠在一起。交叉淡化能盖住咔声，盖不住相位差；淡化越长，梳状滤波越明显。

## 移调之后才见真章

采样升高八度，循环缩短一半，反复频率也翻倍。整周期的循环移调后仍是整周期，非整周期的循环会把新的脉动暴露出来。立体声还要查左右声道：两边循环点差几个采样，声像会随每次回头轻微摆动。用长音听一分钟，再换到高低两个音区各听一遍。

## 不该循环的样本

钢琴、拨弦与打击的尾音本来就在衰减，循环会把它们变成持续音。带长颤音的人声或弦乐，循环锁住一个相位，颤音会失去方向。呼吸声与弓噪这类噪声素材，循环容易形成周期性的喘息。遇到这些素材，宁可把样本录长，或用多条样本拼接，也不要硬找一对点。

```audiolab
{"type":"instrument","gm":"Church Organ","synth":"blown","phrase":["C3","G3","C4","E4"],"label":"风琴长音里的接缝","label_en":"A seam inside an organ sustain","hint":"听长音是否平稳；循环接缝只在采样器反复播放同一段时出现","hint_en":"Hear whether the sustain stays steady; a loop seam appears only when a sampler repeats the same region"}
```
:::

::: en
A two-second organ recording has to hold a twenty-second chord. The sample is not stretched; the waveform circles through a steady stretch, and the loop points mark where that circle starts and ends.

## Two seconds holding twenty

The attack stays outside the loop, the decay stays outside it, and only the calm middle repeats. Put the loop inside a fading section and the level rises on every pass, so the sustain breathes. Put it on one side of a vibrato cycle and the vibrato freezes. Make the loop short enough and its repetition becomes a pitch sitting on top of the note.

## Four loop settings

| Shape | Where it is used | Audible risk |
|---|---|---|
| Forward | The usual sustained note | Pulses when the seam misses a whole cycle |
| Alternating | Material with a symmetrical waveform | A new transient where direction reverses |
| Release loop | The tail after note-off | The tail never ends and sounds stuck |
| One-shot | Percussion, plucked strings, piano | Looping destroys the natural decay |

Sustains usually run forward. Alternating loops suit synthetic material whose waveform is already symmetrical and are rare in acoustic recordings. A release loop needs its own points; do not share them with the sustain.

## The order to work in

1. Find a middle stretch with steady amplitude and stable overtones, away from attack and decay.
2. Align start and end to zero crossings, then nudge them onto whole cycles.
3. Listen without a fade first; add a 20 to 80 ms crossfade only if a click remains.
4. Check the spectrum for added low end or a scooped midrange from comb filtering.
5. Transpose an octave up and down and listen again.

Watch the waveform and the spectrum. Beating can pass for tone colour when it is really two out-of-phase waveforms summed. A crossfade hides a click but not a phase difference, and a longer fade makes the comb filtering clearer.

## Transposition is the real test

Raise the sample an octave and the loop lasts half as long in time, so its repetition rate doubles. A whole-cycle loop stays whole; a loop that only looked aligned reveals a new pulse. In stereo, check both channels: a few samples of difference between left and right makes the image drift on every pass. Audition a sustain for a minute, then try it at the top and bottom of the range.

## Samples that should not loop

Piano, plucked strings and percussion are already decaying. A loop turns that decay into a drone that sounds like an organ. A voice or string line with slow vibrato locks one phase and loses its direction. Breath and bow noise can turn into a periodic gasp. For these, record a longer sample or stitch several takes instead of forcing a pair of points.

```audiolab
{"type":"instrument","gm":"Church Organ","synth":"blown","phrase":["C3","G3","C4","E4"],"label":"A seam inside an organ sustain","label_en":"A seam inside an organ sustain","hint":"Hear whether the sustain stays steady; a loop seam appears only when a sampler repeats the same region","hint_en":"Hear whether the sustain stays steady; a loop seam appears only when a sampler repeats the same region"}
```
:::
