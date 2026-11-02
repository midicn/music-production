---
id: sample-rate-choice
site: prod
cat: A4
title: 采样率选择
title_en: Choosing a Sample Rate
summary: 采样率决定能记录的最高频率，也决定体积与流程兼容
summary_en: Sample rate sets the highest frequency you can capture, and the file size and workflow that follow.
level: standard
tags: [录音, 采样率, 交付]
tags_en: [recording, sample rate, delivery]
alias: [采样率, 采样频率, 取样率, sample rate, sample frequency]
links:
  - "[[glossary:sample-rate]]"
  - "[[glossary:bit-depth]]"
  - "[[instrument:cymbals]]"
instances:
  - groove-001062 | 打击乐编制参照，不能由 MIDI 直接听出降采样损失 | Percussion instrumentation reference; MIDI alone does not reveal downsampling loss
  - mutopia-000981 | 人声旋律的音符参照，不包含真实演唱齿音的录音 | Vocal-melody notes without a recording of real vocal sibilants
  - openscore-001257 | 钢琴与人声声部的 MIDI 素材，没有不同采样率对照 | Piano-and-voice MIDI material without alternate sample-rate renders
sources:
  - "https://docs.scipy.org/doc/scipy/reference/generated/scipy.signal.resample_poly.html"
  - Pohlmann, Principles of Digital Audio, sampling and conversion chapters
  - AES recommended practice for sampling frequency and studio interchange
updated: 2026-11-02
---

::: zh
## 问题

采样率决定能记录的最高频率，也决定文件大小与处理负担。44.1、48 与 96 kHz 没有绝对优劣，只有与用途、后续流程是否匹配。

## 信号链

话筒信号经话放进入转换器的抗混叠滤波器，再按设定速率采样。转换器内部的过采样与滤波设计，往往比工程上标称的数字更影响高频表现。

## 摆位与参数

音乐成品用 44.1 kHz，影视与视频用 48 kHz，需要大量变调或重处理时用 88.2 或 96 kHz。整张工程只用一个速率，避免反复转换。交付前先确认平台要求，不要等到母带阶段才改。

```audiolab
{"type":"instrument","drum":"49","synth":"perc","phrase":["49","49"],"label":"镲片音色参照","label_en":"Cymbal timbre reference","hint":"这里只提供镲片音色，不能切换采样率。采样率差异须通过受控音频导出测试，不能用换音色来替代。","hint_en":"This provides a cymbal sound without a sample-rate switch. Compare controlled audio exports rather than substituting a change of timbre."}
```

## 听什么

44.1 kHz 的奈奎斯特频率为 22.05 kHz，不能据此推断 15 kHz 以上必然变钝。要比较采样率，使用同一源文件、已知转换设置和匹配电平的音频，不要用不同录音互比。没有听出可靠差别时，按交付与协作要求选择即可；本站 MIDI 试听不是不同采样率录音的盲听测试。

## 常见误解

- **96 kHz 一定更好听** → 多数回放设备听不出，代价是体积与 CPU。
- **采样率可以随时改** → 每次转换都是一次滤波。
- **44.1 与 48 只差一点** → 差的是整条流程的兼容性。
:::

::: en
## The problem

Sample rate sets the highest frequency you can capture, and with it file size and processing load. 44.1, 48 and 96 kHz are not better or worse; they either match the job and workflow, or they do not.

## Signal chain

The microphone signal passes through the preamp into the converter's anti-aliasing filter, then is sampled at the chosen rate. The converter's oversampling and filter design often matter more than the number on the session.

## Placement and settings

Use 44.1 kHz for music releases, 48 kHz for film and video, and 88.2 or 96 kHz for heavy pitch shifting. Keep one rate for the whole project and avoid repeated conversion. Confirm the delivery requirement before mastering.

```audiolab
{"type":"instrument","drum":"49","synth":"perc","phrase":["49","49"],"label":"Cymbal timbre reference","label_en":"Cymbal timbre reference","hint":"This provides a cymbal sound without a sample-rate switch. Compare controlled audio exports rather than substituting a change of timbre.","hint_en":"This provides a cymbal sound without a sample-rate switch. Compare controlled audio exports rather than substituting a change of timbre."}
```

## What to listen for

The Nyquist frequency at 44.1 kHz is 22.05 kHz; that does not imply inevitable dulling above 15 kHz. Compare rates using one source, known conversion settings and matched level rather than different recordings. If no reliable audible difference emerges, follow delivery requirements. The MIDI examples are not a blind test of recordings at different sample rates.

## Common misconceptions

- **96 kHz always sounds better** → most playback systems cannot show it, and it costs space and CPU.
- **The rate can be changed at any time** → every conversion is another filter.
- **44.1 and 48 are almost the same** → what differs is compatibility along the chain.
:::
