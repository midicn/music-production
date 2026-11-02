---
id: lossy-compression
site: prod
cat: B5
title: 有损压缩原理
title_en: How Lossy Compression Works
summary: 丢弃被掩蔽的成分换体积，代价藏在瞬态与高频里。
summary_en: Discarding masked content saves space, and the cost hides in transients and high frequencies.
level: standard
tags: [有损压缩, 心理声学, 码率, 预回声]
tags_en: [lossy compression, psychoacoustics, bitrate, pre-echo]
alias: [有损压缩, 心理声学编码, 预回声, lossy compression]
links:
  - "[[glossary:sample-rate]]"
  - "[[glossary:monitoring]]"
instances:
  - atepp-001868 | 密集变奏的音符素材，可另渲染后制作编码测试（C1） | Dense-variation notes for separate rendering and codec tests (C1)
  - groove-000000 | 鼓组瞬态的源素材，不包含编码器生成的预回声（C1） | Drum-attack source material without encoder-generated pre-echo (C1)
  - thesession-000083 | 单声部旋律素材，没有不同码率的编码对照（C1） | Single-line melody without alternate-bitrate codec renders (C1)
sources:
  - 心理声学模型与掩蔽阈值的通识；音频编码教材是主要依据。
  - Opus 与 AAC 的公开测试资料——依据来自规范与听测报告。
updated: 2026-11-02
---

::: zh
## 问题

有损编码不存全部样点，而是判断哪些成分人耳听不见，把它们用更少的比特表示。体积降下来，代价藏在瞬态与高频里。

## 原理

感知编码器利用听觉掩蔽、变换和量化等方法分配比特，但具体机制依编码器而异。码率受限时，部分素材可能出现预回声、带宽变化或调制伪影。联合立体声利用左右相关性，某些变换本身可以可逆；不能把联合立体声直接等同于声场变窄。

## 参数与做法

选择编码器、码率和声道数时，先按目标平台与用途要求，再用困难片段试听。语音、立体声音乐和低延迟通信不能共用一个“透明”码率。保存无损母版，只在发行或访问副本上编码，避免从已有有损文件反复转码。峰值余量按编码与交付规范核对，采样峰值不能替代真峰值检查。

## 听什么

从同一无损母版生成候选，解码后与原版匹配时间和电平，再检查瞬态前、持续高频、立体声定位和安静尾音。先盲听再看文件名；若无法可靠分辨差异，也应记录，而不是预先断言某个码率必然糊或必然透明。

```audiolab
{"type":"instrument","gm":"Harpsichord","synth":"plucked","phrase":["C5","E5","G5","C6","G5","E5","C5"],"label":"快速音型参照","label_en":"Fast-figure reference","hint":"这段没有码率开关。把同一无损音频分别编码、解码后匹配电平，才可检查预回声和高频伪影。","hint_en":"There is no bitrate switch. Encode and decode the same lossless audio at different settings, then match level to inspect pre-echo and high-frequency artifacts."}
```

## 常见误解

有损解码后转存无损格式可以避免下一次再编码，但不会恢复已经丢弃的信息。码率也不是跨编码器统一的质量标尺；应把文件体积、延迟、兼容性与受控听音结果一起考虑。
:::

::: en
## The question

Lossy coding skips what the ear will not notice, spending fewer bits there. Size falls, and the cost hides in transients and highs.

## How it works

Perceptual codecs allocate bits using tools such as masking models, transforms and quantisation, with mechanisms varying by codec. Limited bitrate may expose pre-echo, bandwidth changes or modulation artifacts on some material. Joint stereo exploits channel correlation and some transforms are reversible; it is not inherently a narrowed stereo image.

## Settings and practice

Choose codec, bitrate and channel count for platform and use, then audition difficult excerpts. Speech, stereo music and low-latency communication do not share one transparent bitrate. Retain a lossless master, encode distribution/access copies and avoid lossy-to-lossy generations. Check peak headroom for the codec and specification; sample peak does not replace true-peak measurement.

## What to listen for

Generate candidates from one lossless master, decode and align time and level, then inspect pre-transients, sustained highs, stereo position and quiet tails. Listen blind before filenames; record a failure to distinguish reliably rather than presuming one bitrate must blur or be transparent.

```audiolab
{"type":"instrument","gm":"Harpsichord","synth":"plucked","phrase":["C5","E5","G5","C6","G5","E5","C5"],"label":"Fast-figure reference","label_en":"Fast-figure reference","hint":"There is no bitrate switch. Encode and decode the same lossless audio at different settings, then match level to inspect pre-echo and high-frequency artifacts.","hint_en":"There is no bitrate switch. Encode and decode the same lossless audio at different settings, then match level to inspect pre-echo and high-frequency artifacts."}
```

## Common misconceptions

Saving decoded lossy audio in a lossless format can avoid another coding generation, but cannot restore discarded information. Bitrate is not a uniform quality scale across codecs; consider size, latency, compatibility and controlled listening together.
:::
