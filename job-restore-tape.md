---
id: job-restore-tape
site: prod
cat: D
order: 6
title: 修复老录音
title_en: Restoring an Old Recording
summary: 把老录音清洗、降噪、去嗡，并留下可追溯的存档。
summary_en: Clean an old recording of clicks, noise and hum, and leave an archive that can be traced back to the raw transfer.
level: standard
tags: [流程, 修复, 降噪, 存档]
tags_en: [workflow, restoration, denoise, archive]
alias: [老录音修复, 音频修复, tape restoration, 降噪]
links:
  - "[[glossary:noise-floor]]"
  - "[[glossary:sample-rate]]"
  - "[[glossary:dither]]"
instances:
  - pdmx-000107 | 老探戈的旋律与乐队层次，可参考修复要保住哪些细节，是成品参照
  - pdmx-000077 | 旋律叙事清楚的旧式歌曲，适合对照降噪后字头是否还在
  - pdmx-000048 | 小编制歌曲的呼吸与尾音，可参考修复时哪些东西不能削掉
  - pdmx-000037 | 老式流行歌曲的伴奏与旋律比例，适合练 A/B 时的判断
sources:
  - 磁带转录、去嗡与降噪的处理顺序，对照音频修复惯例整理。
  - 原始文件留存、校验和与存档格式（档案数字化惯例）。
tool_kind: guide
tool_vendor: —
tool_form: 流程
tool_platforms: [通用]
tool_price: 不适用
tool_jobs: [流程]
tool_verified: 2026-10-30
updated: 2026-10-30
---

::: zh
## 你要交的是什么

一份可存档的修复结果：原始转录、修复版、可访问的压缩版，以及记录处理链的日志。修复版保留转录时的采样率与位深；转录时用 96 kHz、24 bit 留出处理余量。如果原载体已经脆化，先做一次转录副本，再谈清洗。交 WAV 与一份说明，写清噪声类型、处理顺序、降噪量与任何无法修复的段落。原始文件另存一份，永不覆盖。

## 三步走

先备份与转录：清洗磁头与走带路径，确认转速与方位角，录一条不经任何处理的原始文件，做校验和。第二步分段处理：先修点击与断裂，再去嗡，最后做宽带降噪与温和均衡；每段处理前先存一版中间文件，不要在同一条链上反复覆盖。第三步 A/B：每加一个处理就与原始对比，宁可留一点底噪，也不要把演唱或乐器的尾音削掉；处理顺序写进日志，随时可以退回上一步。

## 用到的工具与页面

DAW 加频谱修复工具就够，先读这里的音频修复，以及词典里的噪声底。去嗡用窄带陷波，只压基频与主要谐波；电网频率在中国是 50 Hz，在美国是 60 Hz，先测再压。频谱视图能看见嗡声的横线，也能看见被误伤的泛音。降噪分两三次小幅做，不要一次拉满。老录音的高频本来就少，提升时用宽而缓的搁架，别用尖峰均衡。

## 验收标准

点击与爆音消失；50 或 60 Hz 的嗡声基频下降，语音或乐器不变得发闷；降噪后没有金属感与水声；整体响度提升但峰值不削波；左右声道都检查，单声道兼容时嗡声不能反弹；原始文件与校验和保留；日志能复原每一步；存档版与访问版分开命名，采样率与位深写在说明里。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","G3","A3","E3"],"label":"修复时要保住的声音","label_en":"What restoration must preserve","hint":"先听尾音与呼吸，再想降噪会不会把它们一起带走","hint_en":"Hear the tails and breath, then ask whether denoising would take them too"}
```

## 常见返工原因

只留修复版，原始文件丢了；降噪一次拉满，尾音与气口被吃掉；去嗡频率猜错，嗡声还在；只处理左声道，右声道的嗡声还在；反复转采样，高频越转越少；用重压缩把动态压平；没写日志，三个月后无法复现；把修复版当母带，直接削波发布；只交压缩版，档案用途不够。
:::

::: en
## What you have to hand over

An archive-ready restoration: the raw transfer, the restored version, an access copy and a log of the processing chain. The restored file keeps the sample rate and bit depth of the transfer; transfer at 96 kHz and 24 bit to leave room for processing. If the carrier is already brittle, make a transfer copy before discussing cleaning. Deliver WAV plus a note describing the noise types, the order of treatment, how much reduction was used and any passage that could not be repaired. Keep the raw file separately and never overwrite it.

## Three steps

Back up and transfer first. Clean the heads and tape path, confirm speed and azimuth, record a raw file with no processing, and generate a checksum. Second, work in stages: repair clicks and dropouts, then remove hum, then apply broadband denoising and gentle EQ. Third, compare: after every process, A/B against the raw. Keep a little noise rather than shave off the tails of voices or instruments. Write the order into the log so any step can be undone.

## Tools and pages

A DAW and a spectral repair tool are enough. Read the site page Audio Restoration first, then the glossary entry Noise Floor. Remove hum with narrow notches on the fundamental and its main harmonics; mains frequency is 50 Hz in China and 60 Hz in the US, so measure before cutting. Denoise in two or three small passes, never one wide-open pass. Old recordings have little high end to begin with, so lift it with a broad, gentle shelf rather than a spike.

## Acceptance checks

Clicks and pops are gone. The 50 or 60 Hz hum fundamental is lower without making voices or instruments dull. Denoising leaves no metallic edge or watery texture. Overall level is raised without clipping. The raw file and checksum are kept. The log can reproduce every step. Archive and access copies are named apart, with sample rate and bit depth stated.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","G3","A3","E3"],"label":"修复时要保住的声音","label_en":"What restoration must preserve","hint":"先听尾音与呼吸，再想降噪会不会把它们一起带走","hint_en":"Hear the tails and breath, then ask whether denoising would take them too"}
```

## Why work gets sent back

Only the restored file survives and the raw is lost. Denoising is pushed to the maximum and tails and breath disappear. The hum frequency is guessed and the hum remains. Repeated sample-rate conversion eats the high end. Heavy compression flattens the dynamics. No log exists, so nothing can be reproduced three months later. The restored file is treated as a master and clipped at release. Only a compressed access copy is delivered, which is not enough for an archive.
:::
