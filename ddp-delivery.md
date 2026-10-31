---
id: ddp-delivery
site: prod
cat: A8
order: 462
title: DDP 交付
title_en: DDP Delivery
summary: DDP 把整张专辑的音频、PQ 与元数据打成一套可校验的交付物。
summary_en: A DDP packages album audio, PQ data and metadata into one verifiable delivery set.
level: standard
tags: [母带, 交付, DDP, CD, 元数据]
tags_en: [mastering, delivery, DDP, CD, metadata]
alias: [DDP, DDP 镜像, 唱片交付, DDP image, CD 母盘]
links:
  - "[[glossary:lufs]]"
  - "[[glossary:mastering]]"
  - "[[glossary:headroom]]"
instances:
  - atepp-003300 | 贝多芬 Op.27 No.1 第一乐章以 Andante 开场，末段直接连到第二乐章，适合看 track mark 怎样放在乐句交界
  - atepp-003310 | 第二乐章与第一乐章之间标 attacca，音乐不停，适合练习零间隙的曲目边界
  - atepp-003319 | 第三乐章 Adagio 收束后接第四乐章，适合检查连奏段落是否被误加静音
  - atepp-003329 | 第四乐章回到 Allegro vivace，适合对照末曲尾音在 DDP 里是否完整保留
sources:
  - Red Book（IEC 60908）— CD-DA 的采样率、位深与通道规格。
  - DDP 2.0 规范与唱片厂交付惯例 — 映像、PQ 与校验文件的组成。
  - ISRC 与 CD-Text 的登记与写入规则 — 对照 IFPI 与国家 ISRC 管理机构的公开说明整理。
updated: 2026-10-31
---

::: zh
DDP 不是一种音频格式，而是一套交付容器：整张专辑的连续音频、每首的起点与索引、ISRC、CD-Text 与校验信息都在里面。唱片厂拿到它就能直接做玻璃母盘，不必再猜曲序和间隙。

## 交付包里有什么

一个可用的 DDP 通常包含连续音频映像、PQ 描述、元数据与校验文件。音频多为 16 bit / 44.1 kHz 的 PCM，按 Red Book 规格；响度与真峰值在交付前已经定稿，DDP 阶段不再改处理。PQ 描述写曲目起点、索引、间隙与预间隙；元数据写专辑名、艺人、ISRC 与 CD-Text；校验文件用 MD5 或厂方指定的清单。

## 曲目边界与 attacca

曲目边界是最容易出错的地方。贝多芬 Op.27 No.1 的第一、二乐章之间标着 attacca，第三、四乐章也连奏，音乐不停，但 CD 仍需要 track mark。做法是把标记放在乐句交界处，间隙设为零，而不是插入一段静音。反过来，现场录音或歌曲之间需要呼吸时，预间隙与淡入淡出要写进 PQ 表，不能靠后期手改。

## 一张表看清职责

| 交付物 | 负责什么 | 不该放什么 |
| --- | --- | --- |
| DDP 映像 | 连续音频与 PQ | 二次限制、未定稿的混音 |
| PQ 表 | 曲序、索引、间隙 | 凭听感临时改的标记 |
| 元数据 | 专辑、艺人、ISRC、CD-Text | 与版权登记不一致的拼写 |
| 校验文件 | 传输完整性 | 可编辑的音频文件 |

## 校验与试听

交付前把 DDP 当成一张真 CD 来听：从第一首的第一秒听到最后一首的最后一秒，检查曲目起点是否切掉起音、间隙是否多出静音、末首尾音是否被截。再用校验工具比对源文件与映像，确认传输没有改动。厂方回执上的 ISRC 与曲序要逐项对，不要只看文件名。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["E4","G4","C5","B4","G4","E4","C4","G3"],"label":"乐章之间不停顿","label_en":"No silence between movements","hint":"注意句尾没有静音，下一段从弱拍接上","hint_en":"Hear the phrase end without silence and the next idea enter on a weak beat"}
```

## 会坏在哪里

把 24 bit 母带直接塞进 DDP，厂方可能拒收；把未定稿的曲序交出去，改一次就要重做映像；在 DDP 之后再做限制或抖动，等于把已经校验过的文件换掉。DDP 适合专辑与 CD 发行，不适合单曲流媒体上传，也不适合作为唯一归档——还要留分轨、工程与未限制母带。
:::

::: en
DDP is not an audio format but a delivery container: one continuous album image, track starts and indices, ISRC, CD-Text and checksums. A plant can cut glass from it without guessing the running order or the gaps.

## What the package contains

A usable DDP usually holds a continuous audio image, a PQ description, metadata and a checksum file. The audio is commonly 16-bit / 44.1 kHz PCM to Red Book; loudness and true peak are final before delivery, and no processing changes at the DDP stage. PQ carries track starts, indices, gaps and pre-gaps; metadata carries album, artist, ISRC and CD-Text; the checksum is MD5 or whatever the plant specifies.

## Track edges and attacca

Track edges are the usual failure point. In Beethoven's Op. 27 No. 1 the first two movements are marked attacca and the third runs into the fourth, so the music never stops, yet the CD still needs track marks. Put the marks at phrase boundaries with zero gap instead of inserting silence. When a live recording or a song sequence does need air, write the pre-gap and fades into the PQ sheet rather than fixing them by hand later.

## Who does what

| Item | Carries | Must not contain |
| --- | --- | --- |
| DDP image | Continuous audio and PQ | A second limiter pass, an unfinalised mix |
| PQ sheet | Order, indices, gaps | Marks moved by ear at the last minute |
| Metadata | Album, artist, ISRC, CD-Text | Spellings that disagree with registrations |
| Checksum | Transfer integrity | An editable audio file |

## Check and listen

Audition the DDP as a real CD, from the first second of track one to the last second of the finale. Check that no start clips an attack, no gap adds silence and no ending is cut. Compare source and image with a checksum tool. Then check every ISRC and track number on the plant's receipt, not just the file names.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["E4", "G4", "C5", "B4", "G4", "E4", "C4", "G3"], "label": "No silence between movements", "label_en": "No silence between movements", "hint": "注意句尾没有静音，下一段从弱拍接上", "hint_en": "Hear the phrase end without silence and the next idea enter on a weak beat"}
```

## Where it goes wrong

A 24-bit master dropped into a DDP may be rejected. An unfinalised running order means rebuilding the image. Limiting or dithering after the DDP replaces a file that was already verified. DDP suits albums and CD release, not a single-track streaming upload, and not archiving on its own; keep stems, sessions and the unlimited master as well.
:::
