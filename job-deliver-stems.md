---
id: job-deliver-stems
site: prod
cat: D
order: 8
title: 交付分轨与母带
title_en: Delivering Stems and a Master
summary: 分轨与母带的命名、响度与验收，一次交清。
summary_en: Stems and a master delivered once, with names, loudness and checks that let the recipient work without asking.
level: standard
tags: [流程, 交付, 母带, stems]
tags_en: [workflow, delivery, mastering, stems]
alias: [分轨交付, 母带交付, stems delivery, 交分轨]
links:
  - "[[glossary:stems]]"
  - "[[glossary:dither]]"
  - "[[glossary:headroom]]"
instances:
  - pdmx-000407 | 合奏层次清楚，适合练按乐器组拆 stems，是交付的参照
  - oga-000004 | 战斗曲分层明显，交付时可按鼓、低音与旋律拆组
  - groove-000010 | 鼓循环的时值与力度层次，适合练分组命名与对齐
  - pdmx-000087 | 多声部与强弱变化明显，可参考 stems 相加时的平衡
sources:
  - stems 与分轨、总线的区别；影视声音与母带交付惯例是主要依据。
  - 命名、等长起点、真峰值与抖动惯例——依据来自后期交付规范。
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

一套能被别人直接用的交付：母带 WAV、320 kbps MP3、按组拆开的 stems、伴奏版与清唱版，以及一份交付说明和校验和。如果对方只要一版，先给母带与伴奏，stems 按需再发。WAV 与 stems 用 48 kHz、24 bit，同起点、等长；stems 不带总线限制。命名统一，目录里不要出现「最终版2」「新的最终版」这类名字。

## 三步走

先打印 stems：从同一工程、同一时间点导出，关掉母带总线处理，每组峰值留 6 dB；导完把 stems 相加，与混音做一次对比。第二步做母带：按目标响度处理，真峰值不超过 -1 dBTP，位深下降时才用抖动。第三步打包：建固定目录，写清采样率、位深、速度、调性、是否做过总线处理，生成校验和，上传后让对方回执；打包前在另一台电脑上解压一次，确认目录层级没有变。

## 用到的工具与页面

DAW、响度表与文件传输就够；这里的 Stems 交付与母带交付格式两页先读。抖动只在降位深时加，48 kHz 不必重采样。命名用「曲名_内容_版本_采样率位深」，不要用空格与中文标点。母带与 stems 分两个目录，避免误发。上传用支持断点续传的服务，别用聊天软件传大文件。交付说明里留一个联系人，对方发现问题时知道找谁。

## 验收标准

stems 相加与混音在电平和相位上一致；WAV 与 stems 等长、同起点、同采样率；MP3 与母带时长一致；母带真峰值不超过 -1 dBTP；响度达到约定目标；母带与伴奏的电平差不超过 0.5 dB；伴奏版没有残留人声；说明里的速度与调性正确；校验和能对上；对方导入后不用再猜文件名。交付说明控制在一页内，对方才会读。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","E4","G4","C5"],"label":"一条 stem 单独听要成立","label_en":"One stem must stand on its own","hint":"先听这一组，再想它与其他组相加后会不会打架","hint_en":"Hear this group alone, then ask whether it will clash when summed with the others"}
```

## 常见返工原因

stems 带着母带限制器，相加后动态被压两次；把 stems 与分轨混为一谈，对方收到几十条单轨；文件长度不一，影视或现场对不上；采样率混用，导入后速度错；只交 WAV，平台上传要 MP3；命名含空格与中文，服务器识别失败；没有说明，母带师不知道有没有做总线处理；忘交伴奏版，发行前临时补；校验和对不上，传输中途已经损坏。
:::

::: en
## What you have to hand over

A delivery someone else can use directly: master WAV, 320 kbps MP3, stems split by group, instrumental and clean versions, plus a delivery note and checksums. If only one version is wanted, send the master and instrumental first and the stems on request. WAV and stems run at 48 kHz and 24 bit, same start, same length; stems carry no master-bus limiting. Names follow one scheme, and the folder contains no "final2" or "new final".

## Three steps

Print stems first: export from the same session at the same start point, bypass the master bus, and leave 6 dB of peak headroom on each group. Sum the stems and compare them with the mix. Second, master: process to the agreed loudness, keep true peak below -1 dBTP, and add dither only when reducing bit depth. Third, package: build a fixed folder, state sample rate, bit depth, tempo, key and whether bus processing was used, generate checksums, upload, and ask for a receipt.

## Tools and pages

A DAW, a loudness meter and a transfer service are enough. Read the site pages Delivering Stems and Master Delivery Formats first. Dither belongs only at bit-depth reduction; 48 kHz needs no resampling. Name files as song_content_version_rate_depth, without spaces or Chinese punctuation. Keep masters and stems in separate folders so the wrong file is not sent. Put a contact in the delivery note so the recipient knows whom to ask.

## Acceptance checks

Stems sum to the mix in level and phase. WAV and stems share length, start and sample rate; the MP3 matches the master in duration. The master's true peak stays below -1 dBTP. Loudness meets the agreed target. The instrumental contains no vocal residue. Tempo and key in the note are correct. Checksums match. The recipient can import without guessing a file name.

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","E4","G4","C5"],"label":"一条 stem 单独听要成立","label_en":"One stem must stand on its own","hint":"先听这一组，再想它与其他组相加后会不会打架","hint_en":"Hear this group alone, then ask whether it will clash when summed with the others"}
```

## Why work gets sent back

Stems carry the master limiter and the dynamics are squashed twice when summed. Files differ in length and do not line up in film or live use. Sample rates are mixed and everything plays at the wrong speed. Only WAV is delivered when the platform wants MP3. Names contain spaces and Chinese punctuation and the server rejects them. No note says whether bus processing was applied. The instrumental is forgotten and has to be made before release. Checksums do not match because the transfer was already damaged.
:::
