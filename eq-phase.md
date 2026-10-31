---
id: eq-phase
site: prod
cat: A7
title: 均衡与相位
title_en: EQ and Phase
summary: 提升一段的同时，相位也在中心附近转动。
summary_en: A boost moves more than level, since minimum-phase EQ rotates phase around the bell and changes how attacks line up.
level: standard
tags: [效果器, 均衡, 相位, 瞬态]
tags_en: [effects, eq, phase, transients]
alias: [均衡相位, 相位旋转, 最小相位, 线性相位, eq phase, linear phase]
links:
  - "[[glossary:eq]]"
  - "[[glossary:phase]]"
  - "[[glossary:phase-check]]"
instances:
  - atepp-003869 | 钢琴双点拾音，两轨合并后中低频的得失最能说明均衡带来的相位变化
  - musicnet-000067 | 弦乐四重奏多话筒收录，窄带提升后声部边缘变软还是变清一听便知
  - groove-000010 | 放克鼓组循环，底鼓与贝斯重叠处推低频，起音的先后关系会改变
sources:
  - FabFilter, Pro-Q 4 user manual, minimum-phase and linear-phase modes.
  - Robert Bristow-Johnson, Cookbook Formulae for Audio EQ Biquad Filter Coefficients.
  - Zölzer, DAFX.
updated: 2026-10-31
order: 440
---

::: zh
在底鼓与贝斯重叠的 80 Hz 推上 3 dB，电平表只动了一点，音头却像错开了半步。均衡改的不只是幅度，还有它周围的相位。

## 最小相位为什么必然动相位

常见的均衡器是最小相位滤波器。提升一段，中心频率附近的相位就会转动，Q 越高，转动越急、范围越窄。幅度曲线与相位曲线由同一组系数决定，想只动幅度而不碰相位，模拟电路做不到，数字滤波器也要换一种设计。

## 三种做法对照

同一处修正可以用不同方式完成，代价各不相同。

| 做法 | 相位行为 | 延迟 | 适合 | 代价 |
|---|---|---|---|---|
| 最小相位 | 中心附近旋转 | 接近零 | 分轨与总线修正 | 瞬态边缘移动 |
| 线性相位 | 全频近似不变 | 随块长增加，常达数十毫秒 | 多轨求和后的窄修 | 起音前出现前响铃 |
| 动态均衡 | 仅触发时旋转 | 依实现 | 压住偶发共振 | 触发点音色跳动 |

## 在什么素材上听得出来

低频最容易暴露。把 60–100 Hz 推 2 dB，听底鼓与贝斯是否还同时起音；在多话筒录的钢琴上做 1–2 dB 窄带提升，听声部边缘是变清楚还是变软。高通滤波器同样带来相位旋转，转折点越高，它下方的群延迟越明显。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C2","G2","C3","E3"],"label":"低频与中频叠在一起的和弦","label_en":"A chord where low and mid overlap","hint":"先听和弦的起音，再想 80 Hz 附近提升后，低频会比中频早到还是晚到","hint_en":"Hear the attack, then ask whether a boost near 80 Hz makes the low end arrive earlier or later than the mids"}
```

## 哪里会坏

线性相位并非更干净，它的前响铃会在鼓组与钢琴独奏的起音前铺一小段预振，低频越长越难藏。已经对齐的多轨再叠最小相位提升，对齐会被打乱。把窄带提升堆在 2–4 kHz，相位旋转集中，齿音与瞬态会一起变硬。动手之前先确认问题真是频率，电平与演奏也会给出同样的症状。
:::

::: en
Push 3 dB at 80 Hz where the kick and bass overlap. The meter barely moves, yet the attack seems half a step late. EQ changes more than magnitude; it also turns phase around the band.

## Why minimum phase must move phase

Most EQs are minimum-phase filters. Boost a band and phase rotates around its centre; the higher the Q, the faster and narrower that rotation. Magnitude and phase come from the same coefficients. An analogue circuit cannot move one without the other, and a digital filter needs a different design to avoid it.

## Three ways to make the same move

The same correction can be done several ways, each with its own price.

| Approach | Phase behaviour | Latency | Good for | Cost |
|---|---|---|---|---|
| Minimum phase | Rotates near the centre | Close to zero | Track and bus fixes | Attack edges shift |
| Linear phase | Nearly flat across the band | Grows with block size, often tens of ms | Narrow fixes after summing | Pre-ringing before attacks |
| Dynamic EQ | Rotates only when triggered | Depends on design | Taming occasional resonances | Tone jumps at the trigger |

## Where the ear can tell

Low frequency exposes it first. Add 2 dB at 60–100 Hz and listen for whether kick and bass still start together. On a piano recorded with two microphones, a 1–2 dB narrow boost shows whether the edge of the part sharpens or blurs. High-pass filters rotate phase too; the higher the corner, the more group delay piles up below it.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C2", "G2", "C3", "E3"], "label": "A chord where low and mid overlap", "label_en": "A chord where low and mid overlap", "hint": "先听和弦的起音，再想 80 Hz 附近提升后，低频会比中频早到还是晚到", "hint_en": "Hear the attack, then ask whether a boost near 80 Hz makes the low end arrive earlier or later than the mids"}
```

## Where it breaks

Linear phase is not automatically cleaner. Its pre-ringing lays a small burst before attacks, which drums and solo piano expose, and the effect grows at low frequencies. Stacking minimum-phase boosts on tracks that were already aligned undoes that alignment. Pile narrow boosts around 2–4 kHz and the rotation concentrates, hardening sibilance and transients together. Confirm the problem is frequency before reaching for EQ; level and performance produce the same symptoms.
:::
