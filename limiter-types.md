---
id: limiter-types
site: prod
cat: A8
title: 限制器类型
title_en: Limiter Types
summary: 峰值限制、削波与多段限制解决的不是同一个问题。
summary_en: Peak limiting, clipping and multiband limiting solve different problems, and swapping them shows up first in the attack.
level: standard
tags: [母带, 限制器, 削波, 响度]
tags_en: [mastering, limiter, clipping, loudness]
alias: [限制器类型, 砖墙限制, 削波器, 多段限制, limiter types, clipper]
links:
  - "[[glossary:limiter]]"
  - "[[glossary:true-peak-limiter]]"
  - "[[glossary:clipping]]"
  - "[[glossary:lufs]]"
instances:
  - groove-000004 | 可渲染鼓组，再等响度比较限制与削波对音头、尾音的影响 | Render drums and compare limiting and clipping on attack and decay at matched loudness
  - mutopia-000497 | 可渲染动态起伏段，对比不同峰值处理，固定输入与输出响度 | Render dynamic sections and compare peak processing with fixed input and matched output loudness
  - oga-000011 | 密集底鼓可作失真测试素材，限制与削波差异需实际处理后判断 | Dense kicks offer distortion-test material; judge limiting/clipping differences only after processing
sources:
  - Giannoulis, Massberg and Reiss, Digital Dynamic Range Compressor Design, JAES 2012.
  - ITU-R BS.1770-4, Algorithms to Measure Audio Programme Loudness and True-peak Level.
  - FabFilter, Pro-L 2 user manual, limiting styles and oversampling.
updated: 2026-11-02
order: 460
---

::: zh
峰值限制与削波都可控制上限，但改写波形和增益包络的方式不同。相同输出峰值并不保证相同响度、音头或失真。用同一输入制作对照，再按目标动态与可接受失真选择，不只看处理器名称。

## 四种常见类型

| 方法 | 主要动作 | 检查重点 |
|---|---|---|
| 峰值限制 | 按检测峰值控制增益 | 起音、恢复、输出峰值 |
| 削波 | 由非线性幅度曲线改写峰值 | 新谐波、互调、混叠 |
| 多段限制 | 分频后分别控峰 | 跨频带平衡、求和与相位 |
| 真峰值限制 | 估算样点间峰值并据此控增益 | 检测精度、输出余量、后续编码结果 |

## 选择看交付

先按交付规范确定峰值上限，再根据素材选择限制、削波或其他处理。真峰值限制并不保证所有后续编码器都绝不产生过冲，仍应检查最终编码解码结果。目标响度、保留动态和可接受失真需要共同取舍，不由“原声用某类、电子用另一类”单独决定。

## 参数与听感

每次只改一项设置，并在相同响度下比较。前瞻和释放怎样改变瞬态取决于算法，不是越长或越短就必然有某种音色。过采样可能减少部分非线性混叠，但检测精度、处理延迟和资源成本应分别查看说明与输出测量。

```audiolab
{"type":"instrument","drum":"38","synth":"perc","phrase":["36","38","42","38","36","38","49","46"],"label":"限制与削波测试的鼓点","label_en":"Drum hits for limiting/clipping tests","hint":"在 DAW 给同一录音分别加限制器与削波器，匹配输出响度，比较音头、低频失真及增益衰减。","hint_en":"Apply a limiter and clipper separately to one recording in a DAW. Match output loudness and compare attack, bass distortion and gain reduction."}
```

## 边界与失败模式

限制器不能自动修复编曲或混音失衡。多级处理是否有用，要比较每一级的目标和残留失真；不要因为第二级动作就断定它只在替第一级补错。保存未限制的高精度版本，最终检查峰值、响度和头尾。
:::

::: en
Peak limiting and clipping can both control a ceiling but alter waveforms and gain envelopes differently. Equal output peak does not guarantee equal loudness, attack or distortion. Compare the same input and choose for intended dynamics and acceptable artifacts rather than the processor name alone.

## Four common types

| Method | Main action | Check |
|---|---|---|
| Peak limiting | Gain control from detected peaks | Attacks, recovery and output peak |
| Clipping | Nonlinear amplitude mapping | Added harmonics, intermodulation and aliases |
| Multiband limiting | Peak control after splitting bands | Balance, summation and phase |
| True-peak limiting | Gain control using estimated inter-sample peaks | Estimation, headroom and later encoded output |

## The choice follows delivery

Choose the peak limit from the delivery specification, then select limiting, clipping or another process for the source. True-peak limiting does not guarantee zero overshoot from every later codec; inspect the final encoded/decoded result. Loudness, retained dynamics and acceptable distortion must be considered together rather than by an acoustic/electronic genre rule.

## Reading the controls by ear

Change one setting at a time and compare at equal loudness. Look-ahead and release behaviour depend on the algorithm rather than one inevitable long/short result. Oversampling may reduce some nonlinear aliases, but inspect detection precision, latency and resource cost separately.

```audiolab
{"type":"instrument","drum":"38","synth":"perc","phrase":["36","38","42","38","36","38","49","46"],"label":"Drum hits for limiting/clipping tests","label_en":"Drum hits for limiting/clipping tests","hint":"Apply a limiter and clipper separately to one recording in a DAW. Match output loudness and compare attack, bass distortion and gain reduction.","hint_en":"Apply a limiter and clipper separately to one recording in a DAW. Match output loudness and compare attack, bass distortion and gain reduction."}
```

## Limits and failure modes

A limiter does not automatically repair arrangement or mix imbalance. Judge multistage processing by each stage’s purpose and residual distortion, not by assuming the second only fixes the first. Preserve an unlimited high-precision version and check final peaks, loudness and boundaries.
:::
