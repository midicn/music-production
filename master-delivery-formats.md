---
id: master-delivery-formats
site: prod
cat: A8
title: 母带交付格式
title_en: Master Delivery Formats
summary: 母带交付要写清格式、采样率、位深与真峰值余量。
summary_en: A master handoff should state format, sample rate, bit depth and true-peak margin so nobody has to guess.
level: standard
tags: [母带, 交付, 格式]
tags_en: [mastering, delivery, formats]
alias: [交付格式, 母带导出, master delivery]
links:
  - "[[glossary:true-peak-limiter]]"
  - "[[glossary:lufs]]"
  - "[[glossary:limiter]]"
instances:
  - musicnet-000265 | 弗雷钢琴四重奏的弱奏与尾音，适合检查交付文件的噪声与淡出
  - pdmx-000855 | 柴可夫斯基第六的强奏段落，适合对照交付版与有损预览的峰值
  - pdmx-001623 | 舒伯特《未完成》的段落转换，适合练习按发行格式导出不同版本
sources:
  - 母带交付的位深、采样率与真峰值规格——依据来自发行与母带交付惯例。
  - 元数据、命名与 DDP 的用途，对照唱片制作与发行流程整理。
updated: 2026-10-28
---

::: zh
交付不是把文件拖进文件夹。格式、位深、采样率、响度与命名都会影响后面的人怎么用，也影响听众最终听到什么。

## 问题

有人把 32 bit 浮点工程文件当母带交出去，发行方不认；有人从 44.1 kHz 升到 96 kHz，以为更高级，文件却更大而内容没变。最容易忽略的是真峰值，文件在本地不削波，转成有损格式后却出现失真。

## 目标与标准

常见的母带交付是 24 bit PCM 的 WAV，采样率与混音一致，通常 44.1 或 48 kHz。流媒体分发接受 24 bit，CD 用 16 bit 加 DDP。真峰值留在 -1 dBTP 左右，文件开头与结尾留少量静音，命名写清曲名、版本与日期。

## 做法

先确认发行方要求，再决定格式。导出无损母带、平台上传版与一个 320 kbps 的试听版，三者的响度与尾音要一致。写入曲名、艺人、ISRC 等元数据，附一份说明，写清是否做过限制、采样率与真峰值。最后做一次转码试听与备份。

## 听什么

听有损版的高频是否刺，低频是否失真，尾音是否被截。下面这段钢琴可以对照无损与压缩版的起音和余韵。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","G4","E4","C5"],"label":"转码后的起音","label_en":"Attack after encoding","hint":"先听无损，再听压缩版，注意高频与尾音的变化","hint_en":"Hear lossless first, then the encoded file, watching highs and tail"}
```

## 常见误解

32 bit 浮点不一定更适合交付，它适合制作过程，发行常要 24 bit PCM。采样率也不是越高越好，没有对应内容时升频只增加体积。MP3 不能当母带，它只能做试听或预览。
:::

::: en
Delivery is not dragging a file into a folder. Format, bit depth, sample rate, loudness and naming affect how others use the master.

## The problem

Some send a 32-bit float session as the master and the distributor rejects it. Others upsample 44.1 to 96 kHz and get larger files with no new content. True peak is easiest to miss, since a file that does not clip locally can distort after encoding.

## Goals and standards

A common master is a 24-bit PCM WAV at the mix sample rate, usually 44.1 or 48 kHz. Streaming accepts 24 bit, while CD uses 16 bit with a DDP. Keep true peak near -1 dBTP, leave head and tail silence, and name files with title, version and date.

## Practice

Confirm the distributor's requirements first. Export the lossless master, the upload version and a 320 kbps preview with matching loudness and tails. Write title, artist and ISRC metadata, note limiting and true peak, then do a transcoded listen and a backup.

## What to listen for

Hear whether the lossy version hardens highs, distorts lows or cuts the tail. The piano figure below compares attack and decay.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "G4", "E4", "C5"], "label": "Attack after encoding", "label_en": "Attack after encoding", "hint": "先听无损，再听压缩版，注意高频与尾音的变化", "hint_en": "Hear lossless first, then the encoded file, watching highs and tail"}
```

## Common misunderstandings

32-bit float is not necessarily better for delivery; it suits production, while releases often want 24-bit PCM. Higher sample rates are not automatically better, since upsampling only adds size. An MP3 is for preview only.
:::
