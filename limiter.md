---
id: limiter
site: prod
cat: A7
title: 限制器
title_en: The Limiter
summary: 用前视、释放与真峰值设置控制峰值，并检查瞬态和失真的代价。
summary_en: Use lookahead, release and true-peak settings to control peaks while checking transient and distortion costs.
level: standard
tags: [效果器, 动态, 限制器, 响度]
tags_en: [effects, dynamics, limiter, loudness]
alias: [限制器, 限幅器, 峰值限制, ceiling, limiter]
links:
  - "[[glossary:true-peak-limiter]]"
  - "[[glossary:clipping]]"
  - "[[instrument:drum-kit]]"
instances:
  - groove-000007 | 可渲染鼓循环，提高限制量后等响度比较军鼓音头 | Render the loop, increase limiting and compare snare attacks at matched loudness
  - groove-000000 | 鼓循环可用于检查释放与节奏的关系，抽吸取决于实际检测与恢复行为 | A drum loop tests release against rhythm; pumping depends on actual detection and recovery
  - oga-000004 | 铜管齐奏可作峰值素材，逐步增加限制量并检查失真及真峰值 | Brass tutti supplies peak material; increase limiting gradually while checking distortion and true peak
sources:
  - Giannoulis, Massberg and Reiss, Digital Dynamic Range Compressor Design, JAES 2012.
  - ITU-R BS.1770-4, Algorithms to Measure Audio Programme Loudness and True-peak Level.
updated: 2026-11-02
---

::: zh
## 难在哪

限制器是一种重点控制峰值上限的动态处理器，常用于交付链末端，也可用于其他控峰任务。它与压缩器有共同机制，区别不能简单归为一个只管峰值、另一个只管平均电平。

## 一层层看原理

限制器可通过峰值检测、增益包络和可选的前视来控峰，具体比率、启动与释放实现各异。前视延迟给处理器提前响应的时间，不保证没有失真。真峰值模式估算重建峰值并据此控制输出；过采样倍率、精度、延迟与后续编码仍需按产品说明和实际导出检查。

## 旋钮与耳朵

先按项目要求设输出上限，再逐渐增加输入增益，听最强音头、低频恢复与安静部分是否受损。释放和前瞻可从厂家默认值开始，但要以具体节奏与算法验证。开启真峰值模式后仍应测量最终输出；有损交付还需检查编码后的峰值。

## 耳朵要抓的点

用同一音频做旁通与限制对照，匹配响度后判断是保留了所需峰值关系，还是出现抽吸、失真或持续部分被抬高。不要用固定“推进3 dB必然变扁”的结果替代实际听音。

```audiolab
{"type":"instrument","drum":"38","synth":"perc","phrase":["36","38","42","38","36","42","38","46"],"label":"限制器测试的鼓点","label_en":"Drum hits for limiter tests","hint":"在 DAW 逐步增加限制量，匹配输出响度，比较音头、尾音与失真；另测导出文件的真峰值。","hint_en":"Increase limiting gradually in a DAW and match output loudness to compare attack, decay and distortion. Measure true peak on the exported file separately."}
```

## 容易弄错的

以为限制器能把响度无限推高；以为 ceiling 设在 0 dBFS 就不会削波；以为限制器只影响峰值、不影响密度。
:::

::: en
## Where it gets hard

A limiter emphasises peak-ceiling control and is often placed near delivery output, though it has other uses. It shares mechanisms with compressors; the distinction is not simply peaks versus average level.

## Inside the mechanism

Limiters can control peaks through detection, a gain envelope and optional lookahead; ratios and attack/release designs vary. Lookahead delays the signal to allow advance response but does not guarantee distortion-free results. True-peak mode estimates reconstructed peaks and controls output accordingly; check oversampling, accuracy, latency and later encoding against documentation and exports.

## Knobs and ears

Set the output limit for the project, then raise input gradually while checking loud attacks, bass recovery and quiet detail. Start release and look-ahead from documented defaults and test against the rhythm and algorithm. Measure output even with true-peak mode enabled, and check encoded peaks for lossy delivery.

## What the ear should catch

Compare bypass and limiting on the same audio at matched loudness, judging peak relationships, pumping, distortion and raised sustain. A fixed claim that 3 dB of drive must flatten the sound is not a substitute for listening.

```audiolab
{"type":"instrument","drum":"38","synth":"perc","phrase":["36","38","42","38","36","42","38","46"],"label":"Drum hits for limiter tests","label_en":"Drum hits for limiter tests","hint":"Increase limiting gradually in a DAW and match output loudness to compare attack, decay and distortion. Measure true peak on the exported file separately.","hint_en":"Increase limiting gradually in a DAW and match output loudness to compare attack, decay and distortion. Measure true peak on the exported file separately."}
```

## Easy to get wrong

That a limiter can push loudness without limit; that a ceiling at 0 dBFS prevents clipping; that limiting changes only peaks and never density.
:::
