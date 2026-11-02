---
id: phase-and-delay
site: prod
cat: A5
title: 相位与延迟
title_en: Phase and Delay
summary: 相位差与延迟造成梳状滤波，改变音色与声像。
summary_en: Phase differences and delay cause comb filtering, changing timbre and stereo image.
level: standard
tags: [相位, 延迟, 梳状滤波, 极性, 单声道]
tags_en: [phase, delay, comb filtering, polarity, mono]
alias: [相位, 延迟, 极性, 梳状滤波, phase, delay, comb filtering]
links:
  - "[[glossary:phase]]"
  - "[[glossary:comb-filtering]]"
  - "[[glossary:delay]]"
  - "[[glossary:monitoring]]"
instances:
  - pdmx-000237 | 可渲染后复制同一音频，比较等增益求和与加入延迟后的频谱 | Render and duplicate one audio source to compare equal-gain summation with and without delay
  - essen-000517 | 单声部素材便于制作极性反转与延迟的独立对照，需在 DAW 中处理 | A single line supports separate polarity and delay comparisons made in a DAW
  - mutopia-000497 | 可观察配器层次；检查延迟造成的宽度时应固定渲染音色与声部设置 | Inspect orchestral layers; keep timbres and part settings fixed when testing delay-based width
sources:
  - Everest, F. Alton，Master Handbook of Acoustics（McGraw-Hill）— 相位与梳状滤波章节核对，未引用
  - Howard, David M. & Angus, Jamie，Acoustics and Psychoacoustics（Focal Press）— 延迟与听觉章节核对，未引用
updated: 2026-11-02
---

::: zh
## 问题
两支话筒录同一声源，推子一合，低频少了、声音变薄；单声道检查时，宽大的合成器突然塌到中间。相位与延迟在求和时改变了频谱。

## 物理或房间
相位描述周期中的位置，延迟是时间移动。两个等幅相同信号相隔τ秒相加时，抵消频率为(2k+1)/(2τ)，增强间隔为1/τ；例如1 ms延迟的第一处抵消在500 Hz，后续梳齿相隔1000 Hz。实际录音若幅度、指向和反射不同，抵消不会都同样深。空气中传播每米约需2.9 ms，仍受温度影响。

## 做法与判断
先用正确的左右求和做单声道检查，再定位相关的多话筒、并行或延迟路径。极性开关、移动话筒和样点延迟解决的是不同问题。需要空间感的近远拾音或立体声阵列，不一定应移动到完全对齐；把测量、路由与目标音色一起考虑。

## 听什么
按单声道按钮，听低频与中央人声是否变薄；再切换一支话筒的极性，比较哪一种更实。播短促鼓点，听两路合并后音头是否变软。用延迟时，听梳状滤波是想要的颜色，还是意外的空洞。

## 常见误解
相位与极性不是一回事，180 度反转只是特例。反转极性不一定更好，要看话筒距离与声源。延迟不总是敌人，立体声加宽与回声都要用它。

```audiolab
{"type":"instrument","gm":"Acoustic Guitar (steel)","synth":"plucked","phrase":["C4","G4","C4","G4"],"label":"延迟实验的短句素材","label_en":"A short phrase for a delay experiment","hint":"先录下单一音色，等增益复制一路；分别测试零延迟、1毫秒延迟和极性反转，并保持监听音量。","hint_en":"Record one timbre and duplicate it at equal gain. Compare zero delay, 1 ms delay and polarity inversion at a stable monitoring level."}
```
:::

::: en
## The problem
Two mics on one source sum and the bass disappears; a wide synth collapses in mono. Phase and delay have changed the spectrum.

## Physics or room
Phase describes position in a cycle; delay shifts time. Summing identical equal-level signals separated by τ seconds gives nulls at (2k+1)/(2τ), spaced by 1/τ. At 1 ms the first null is 500 Hz and subsequent teeth are 1000 Hz apart. Real recordings differ in level, directivity and reflections, so null depths vary. Sound travel is roughly 2.9 ms per metre, depending on temperature.

## Practice and judgement
Use correct left/right summing for mono checks, then locate related multi-mic, parallel or delayed paths. Polarity inversion, microphone movement and sample delay address different issues. Close/room captures or stereo arrays intended to convey space need not be fully aligned; consider measurement, routing and the target sound together.

## What to listen for
Press mono and hear whether bass and vocal thin out; flip one mic's polarity. On a drum hit, hear if the attack softens. With delay, decide whether the comb is colour or a hole.

## Common misunderstandings
Phase and polarity differ; a 180-degree flip is a special case. Inverting is not always better; it depends on distance and source. Delay is not always the enemy; widening and echo rely on it.

```audiolab
{"type":"instrument","gm":"Acoustic Guitar (steel)","synth":"plucked","phrase":["C4","G4","C4","G4"],"label":"A short phrase for a delay experiment","label_en":"A short phrase for a delay experiment","hint":"Record one timbre and duplicate it at equal gain. Compare zero delay, 1 ms delay and polarity inversion at a stable monitoring level.","hint_en":"Record one timbre and duplicate it at equal gain. Compare zero delay, 1 ms delay and polarity inversion at a stable monitoring level."}
```
:::
