---
id: audio-file-formats
site: prod
cat: B5
title: 音频文件格式
title_en: Audio File Formats
summary: 未压缩、无损、有损三类，在体积与兼容之间取舍。
summary_en: Uncompressed, lossless and lossy formats trade file size against compatibility and fidelity.
level: standard
tags: [文件格式, 无损, 有损, 归档]
tags_en: [file formats, lossless, lossy, archiving]
alias: [音频格式, WAV, AIFF, FLAC, MP3, AAC, Opus]
links:
  - "[[glossary:bit-depth]]"
  - "[[glossary:sample-rate]]"
instances:
  - pdmx-000153 | 二十六分钟的管风琴托卡塔，未压缩 WAV 与无损压缩的体积差最直观（C1）
  - groove-000000 | 三十七秒鼓循环体积很小，格式选择对短素材几乎无所谓（C1）
  - atepp-000195 | 四分半的钢琴曲是常见单曲长度，格式与码率的取舍在这类时长上最典型（C1）
sources:
  - WAV、AIFF、FLAC 的容器与编码结构，参考格式公开规范。
  - 有损编码在低码率下的表现；公开听测资料是主要依据。
updated: 2026-10-28
---

::: zh
## 问题

同一段音乐可以存成未压缩的 WAV 或 AIFF、无损的 FLAC，或有损的 MP3、AAC、Opus。选择是在体积、兼容与音质之间取舍。

## 原理

WAV 与 AIFF 是容器，里面装 PCM 样点，前者小端、后者大端。FLAC 用线性预测加熵编码，解压后与原始样点逐位相同，体积约减半。MP3 用心理声学模型丢掉被掩蔽的成分，AAC 在低码率下更稳，Opus 在低延迟与语音场景表现好。容器与编码是两件事。

## 参数与做法

归档用 WAV 或 FLAC，交付用 24 位 WAV，流媒体按平台指定格式上传。试听用 256 kbps 以上的 AAC 或 Opus。不要反复转码有损文件，每转一次都会再丢一层。先算体积再选格式。

## 听什么

在二十六分钟的管风琴托卡塔上比较未压缩与无损的体积，在三十七秒的鼓循环上听短素材的差异，在四分半的钢琴曲上听单曲长度的取舍。有损格式重点听镲片与高频泛音。

```audiolab
{"type":"instrument","gm":"Church Organ","synth":"reed","phrase":["C3","G3","C4","E4","G4","C5"],"label":"长持续和弦","label_en":"A long sustained chord","hint":"同样的声音，未压缩与无损只差体积，有损则要听高频","hint_en":"Uncompressed and lossless differ only in size, while lossy asks you to hear the top"}
```

## 常见误解

WAV 音质一定比 FLAC 好，两者解压后完全相同。MP3 320 kbps 不等于无损。文件扩展名不决定音质，编码方式才决定。把有损文件转成 FLAC 不会恢复已经丢掉的信息。
:::

::: en
## The question

The same music can be stored as uncompressed WAV or AIFF, lossless FLAC, or lossy MP3, AAC and Opus. The choice trades file size against compatibility and fidelity.

## How it works

WAV and AIFF are containers holding PCM samples, one little-endian and one big-endian. FLAC uses linear prediction and entropy coding, so it decompresses bit-for-bit and roughly halves the size. MP3 discards masked content; AAC holds up better at low rates, and Opus suits low latency and speech. Container and codec are separate things.

## Settings and practice

Archive as WAV or FLAC, deliver 24-bit WAV, and upload in the platform's requested format. Audition at 256 kbps AAC or above. Do not transcode lossy files repeatedly. Work out the size before choosing.

## What to listen for

On a twenty-six-minute organ toccata, compare uncompressed and lossless size. On a thirty-seven-second drum loop, hear how little format matters. On a four-minute piano piece, hear the trade at a typical single length. For lossy files, listen to cymbals and high overtones.

```audiolab
{"type": "instrument", "gm": "Church Organ", "synth": "reed", "phrase": ["C3", "G3", "C4", "E4", "G4", "C5"], "label": "A long sustained chord", "label_en": "A long sustained chord", "hint": "同样的声音，未压缩与无损只差体积，有损则要听高频", "hint_en": "Uncompressed and lossless differ only in size, while lossy asks you to hear the top"}
```

## Common misconceptions

WAV is not better than FLAC, since both decode identically. MP3 at 320 kbps is not lossless. A file extension does not set quality; the codec does. Converting a lossy file to FLAC restores nothing.
:::
