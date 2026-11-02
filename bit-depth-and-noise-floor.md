---
id: bit-depth-and-noise-floor
site: prod
cat: A4
title: 位深与噪声底
title_en: Bit Depth and Noise Floor
summary: 位深决定量化噪声的底，也就是弱奏能安静到哪里
summary_en: Bit depth sets the quantisation noise floor, and therefore how quiet a soft passage can stay.
level: standard
tags: [录音, 位深, 噪声]
tags_en: [recording, bit depth, noise]
alias: [位深, 比特深度, 量化噪声, bit depth, word length, noise floor]
links:
  - "[[glossary:bit-depth]]"
  - "[[glossary:noise-floor]]"
  - "[[glossary:dither]]"
instances:
  - atepp-005000 | 钢琴 MIDI，可另行渲染为低电平音频后做量化实验 | Piano MIDI that can be rendered at low level for a separate quantisation experiment
  - openscore-000818 | 歌声与钢琴声部的 MIDI 参照，不包含不同位深的录音对照 | Voice-and-piano MIDI reference, without alternate bit-depth recordings
  - mutopia-001594 | 吉他练习曲的音符素材，可另制淡出音频检查量化 | Guitar-study notes for separately rendering a fade to examine quantisation
sources:
  - "https://downloads.izotope.com/guides/izotope-dithering-with-ozone.pdf"
  - "https://downloads.izotope.com/docs/rx6/39-dither/index.html"
  - Lipshitz, Wannamaker and Vanderkooy, Quantization and Dither, JAES
  - AES Convention paper on bit-depth audibility in quiet passages
updated: 2026-11-02
---

::: zh
## 问题

位深决定量化噪声的底，也就是弱奏能安静到哪里。24 位与 16 位的差别不是清晰度，而是安静程度与余量。

## 信号链

定点 PCM 的位深决定可表示的幅度级数。量化误差在未加抖动时可能随信号变化，表现为失真；它并不天然集中在高频。合适的抖动可降低误差与信号的相关性，噪声整形则进一步改变噪声的频率分布。实际录音的底噪还受话筒、话放和转换器限制。

## 摆位与参数

录音通常选 24 位，为演奏的突发峰值保留余量，电平应按素材和设备设定。源文件是 16 位，不代表 DAW 的内部运算也是 16 位；多数现代工程使用浮点处理。提高增益会同时提高已有噪声，不能恢复录制时没留下的信噪比。交付位深按接收方要求确定，在最终定点量化处配置抖动。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4"],"label":"钢琴弱奏参照","label_en":"Quiet piano reference","hint":"观察音符的衰减即可；这段合成演示没有位深切换，也没有展示录音噪声底。不要为寻找噪声而大幅提高监听音量。","hint_en":"Observe the note decay. This synthesis demo has no bit-depth switch and does not measure a recording noise floor; do not raise monitoring excessively to seek noise."}
```

## 听什么

要比较量化影响，可把同一条浮点淡出分别导出为低位深、加抖动和未加抖动版本，再统一增益比较尾音与噪声。测试时先降低监听音量，避免放大噪声时意外过响。本站 MIDI 试听用于观察弱奏与尾音，不包含这些不同位深的音频版本，不能据此断言 16 位一定粗糙、24 位一定可闻地更好。

## 常见误解

- 位深不能代替采样率，两者分别涉及幅度量化与时间采样。
- 浮点处理的余量不等于音频接口或最终定点文件不会削波。
- 抖动用于控制重新量化的失真，不是降噪或修复削波。
:::

::: en
## The problem

Bit depth sets the level of quantisation noise, and therefore how quiet a soft passage can stay. The difference between 24 and 16 bits is not clarity but silence and headroom.

## Signal chain

Fixed-point PCM bit depth sets the number of representable amplitude levels. Without dither, quantisation error can depend on the signal and become distortion; it is not inherently concentrated at high frequencies. Suitable dither reduces that correlation, while noise shaping changes the noise spectrum. Microphones, preamps and converters also limit a recording's noise floor.

## Placement and settings

Recording at 24 bits leaves practical room for unexpected peaks; set the level for the source and equipment. A 16-bit source file does not imply 16-bit internal processing: many DAWs mix in floating point. Gain raises existing noise as well as signal and cannot recover the original recording's signal-to-noise ratio. Choose delivery depth for the recipient and configure dither at final fixed-point quantisation.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4"],"label":"Quiet piano reference","label_en":"Quiet piano reference","hint":"Observe the note decay. This synthesis demo has no bit-depth switch and does not measure a recording noise floor; do not raise monitoring excessively to seek noise.","hint_en":"Observe the note decay. This synthesis demo has no bit-depth switch and does not measure a recording noise floor; do not raise monitoring excessively to seek noise."}
```

## What to listen for

To examine quantisation, export one floating-point fade at reduced depth with and without dither, then compare the tails at matched gain. Lower monitor level before amplifying noise. The MIDI examples here illustrate soft passages and decays; they are not alternate bit-depth renders and cannot establish that 16 bits always sound grainy or that 24 bits are audibly better.

## Common misconceptions

- Bit depth and sample rate describe amplitude quantisation and time sampling respectively.
- Floating-point headroom does not prevent clipping at an interface or a fixed-point output.
- Dither controls requantisation distortion; it does not remove noise or repair clipping.
:::
