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
  - atepp-003869 | 钢琴音符参照，不是双话筒录音及其合并结果 | Piano-note reference rather than two microphone recordings and their sum
  - musicnet-000067 | 四重奏声部的MIDI参照，不包含窄带EQ前后录音 | Quartet MIDI parts without before-and-after narrow-band EQ recordings
  - groove-000010 | 鼓组音符素材，不证明EQ改变了频段的到达时间 | Drum notes that do not establish EQ-induced changes in arrival time
sources:
  - "https://www.fabfilter.com/help/pro-q/using/processingmode"
  - FabFilter, Pro-Q 4 user manual, minimum-phase and linear-phase modes.
  - Robert Bristow-Johnson, Cookbook Formulae for Audio EQ Biquad Filter Coefficients.
  - Zölzer, DAFX.
updated: 2026-11-02
order: 440
---

::: zh
EQ既改变幅度响应，也可能改变相位响应。影响是否可闻、是否影响多轨求和，取决于滤波器设计、修正幅度、源信号和并行路径，不能由一次低频提升直接推断音头错位。

## 最小相位为什么必然动相位

常见最小相位EQ的幅度与相位变化相关；线性相位滤波器则让相关频率成分经历近似相同的群延迟，需要相应处理延迟，并可能带来前振铃。线性相位不是“全频相位不变”，动态EQ也不只有一种相位设计。

## 三种做法对照

同一处修正可以用不同方式完成，代价各不相同。

| 模式 | 应观察什么 | 取舍 |
|---|---|---|
| 最小相位 | 频率相关相位与多轨求和 | 通常较低延迟，幅相同时变化 |
| 线性相位 | 固定处理延迟、振铃与瞬态 | 可保留频率间相对时间关系，但需检查前振铃 |
| 动态EQ | 检测条件、随时间变化的滤波和所选相位模式 | 不同产品实现不同 |

## 在什么素材上听得出来

用同一测试信号或真实多话筒录音，分别比较EQ旁通、最小相位与线性相位设置，并补偿报告的处理延迟。独听、合听与单声道检查各有用途；频谱变化不能只靠“更早”或“更软”的形容词诊断。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C2","G2","C3","E3"],"label":"多音高和弦参照","label_en":"Multi-pitch chord reference","hint":"这段合成声音没有双话筒录音和可切换EQ。相位影响须用实际滤波器、测量信号或受控多轨音频检查。","hint_en":"This synthesis has neither a two-microphone recording nor switchable EQ. Examine phase using actual filters, test signals or controlled multitrack audio."}
```

## 哪里会坏

线性相位是否产生明显前振铃，与滤波形状、低频分辨率和素材有关；不是每次使用都会听见。多轨上加入EQ后应重新检查组合音色，但不必认为所有最小相位处理都会破坏对齐。处理器的作用需与演奏、电平和路由问题分别确认。
:::

::: en
EQ changes magnitude and may change phase response. Audibility and multitrack summing depend on filter design, correction, source and parallel paths; a bass boost alone does not establish a shifted attack.

## Why minimum phase must move phase

Magnitude and phase are linked in a typical minimum-phase EQ. A linear-phase filter gives relevant components approximately equal group delay, requiring processing latency and potentially introducing pre-ringing. Linear phase does not mean unchanged phase everywhere, and dynamic EQ does not have one universal phase design.

## Three ways to make the same move

The same correction can be done several ways, each with its own price.

| Mode | Inspect | Trade-off |
|---|---|---|
| Minimum phase | Frequency-dependent phase and multitrack sum | Usually low latency with linked magnitude/phase changes |
| Linear phase | Processing latency, ringing and transients | Can preserve relative timing between frequency components; inspect pre-ringing |
| Dynamic EQ | Detection, time-varying filtering and selected phase mode | Implementation differs between products |

## Where the ear can tell

Use one test signal or real multi-microphone recording to compare bypass, minimum-phase and linear-phase settings, compensating reported processing latency. Solo, summed and mono checks serve different purposes; descriptions such as earlier or softer are not measurements of phase response.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C2","G2","C3","E3"],"label":"Multi-pitch chord reference","label_en":"Multi-pitch chord reference","hint":"This synthesis has neither a two-microphone recording nor switchable EQ. Examine phase using actual filters, test signals or controlled multitrack audio.","hint_en":"This synthesis has neither a two-microphone recording nor switchable EQ. Examine phase using actual filters, test signals or controlled multitrack audio."}
```

## Where it breaks

Audible linear-phase pre-ringing depends on filter shape, low-frequency resolution and material; it does not occur perceptibly in every use. Recheck combined sound after EQ on multitracks without assuming all minimum-phase processing ruins alignment. Distinguish processor effects from performance, level and routing problems.
:::
