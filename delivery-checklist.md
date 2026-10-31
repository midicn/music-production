---
id: delivery-checklist
site: prod
cat: A1
order: 302
title: 交付清单
title_en: Delivery Checklist
summary: 响度、峰值、静音、命名、元数据，五项都过再发出去。
summary_en: Loudness, peaks, silence, naming and metadata, all checked before anything leaves the building.
level: standard
tags: [交付, 质检, 响度, 元数据]
tags_en: [delivery, quality control, loudness, metadata]
alias: [交付清单, 交付前检查, 收尾清单, delivery checklist, delivery QC]
links:
  - "[[glossary:lufs]]"
  - "[[glossary:true-peak]]"
  - "[[glossary:isrc]]"
  - "[[glossary:headroom]]"
instances:
  - pdmx-000855 | 柴可夫斯基第六的钢琴版，强奏与长尾都在，适合查真峰值与淡出（CC0）
  - oga-000004 | 近一分钟的战斗曲，密度高，导出前要留真峰值余量（CC BY-SA 4.0）
  - groove-000010 | 80 BPM 的放克鼓循环，头尾静音留多少，一听便知（CC BY 4.0）
sources:
  - ITU-R BS.1770 与 EBU R128 关于节目响度与真峰值测量的建议书
  - Spotify 与 Apple Music 官方帮助中心关于交付规格与响度归一化的说明
  - DDEX 关于数字发行元数据与 ISRC 的标准
updated: 2026-10-31
---

::: zh
被打回的交付，多数不是音乐问题：文件名里有空格、母带比参考响两 LU、结尾留了半秒噪声。这些在监听室里听不出来，在发行方的批处理脚本里一定会炸。

## 先把规格拿到手

平台、格式、采样率、位深、响度目标、命名规则、截止时间，这七项要在开工前写进邮件或工单。只说“发个母带”的客户，往往收到文件后才想起还要伴奏版和无人声版。规格越模糊，返工越贵。把规格抄进工程备注，交付时逐项对照，比事后解释有效。

## 响度与真峰值

响度按测量结果说话，不按推子或感觉。流媒体常见目标是整体响度负 14 LUFS 左右，广播按 EBU R128 的负 23 LUFS 或 ATSC A/85 的负 24 LKFS；真峰值控制在负 1 dBTP 以下，给有损编码留余量。测的时候用整曲积分响度，不要只看副歌；单曲与专辑的差别，也要先问清。

| 项目 | 合格线 | 怎么查 |
|---|---|---|
| 整体响度 | 按平台或合同目标，整曲积分 | 响度表，整曲播放 |
| 真峰值 | 低于负 1 dBTP | 真峰值表，含升采样 |
| 头尾 | 头不留长静音，尾收到数字静音 | 波形放大看首尾 |
| 命名 | 项目、版本、采样率、位深 | 批量检查，无空格 |
| 元数据 | 曲名、作者、版权、ISRC | 播放器与发行后台各看一次 |

## 头尾、命名与元数据

文件头留一两毫秒即可，留太长会让播放器起播迟钝；文件尾要收到数字静音，不能把混响尾巴硬切，也不能留一段底噪。循环素材的尾音要能接回开头，最好同时给首尾对齐的版本。文件名只用字母、数字、下划线与连字符，把项目、版本、采样率、位深写进去，避开“最终版”三个字。元数据填曲名、作者、版权、ISRC，工程里的 BPM 与调性写进说明文件。规则一旦定下，大小写与分隔符都不能例外。

## 别在错的系统上检查

用响度表而不是耳朵猜，用真峰值表而不是采样峰值，用发行方给的参考曲做 A/B。最常见的失败是把限制器推得过狠，文件在平台上被降到同样响度后反而更扁；也有人只查了 WAV，没查转成 AAC 后的峰值。交付清单的作用不是让你更慢，而是让返工发生在自己这里，而不是在发行方的邮件里。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5","G4","E4","C4"],"label":"同一段，两个响度","label_en":"One phrase at two levels","hint":"先对齐响度再比较，别把更响当成更好","hint_en":"Match loudness first, and do not mistake louder for better"}
```
:::

::: en
Most deliveries come back for reasons that have nothing to do with music: a space in the file name, a master two LU louder than the reference, half a second of noise at the tail. None of it is audible in the studio, and all of it breaks the recipient's batch script.

## Get the specification in writing

Platform, format, sample rate, bit depth, loudness target, naming rule and deadline belong in an email or ticket before work starts. A client who asks only for a master often remembers the instrumental and the no-vocal version after the files arrive. Vague specifications cost more in rework. Copy them into the session notes and tick them off at delivery instead of explaining later.

## Loudness and true peak

Loudness follows a measurement, not a fader or a feeling. Streaming services commonly target around minus fourteen LUFS integrated, broadcast follows EBU R128 at minus twenty-three LUFS or ATSC A/85 at minus twenty-four LKFS, and true peak should stay below minus one dBTP to leave room for lossy encoding. Measure integrated loudness over the whole track, not just the chorus, and ask whether the job is a single or an album.

| Item | Pass condition | How to check |
|---|---|---|
| Integrated loudness | Platform or contract target, whole track | Loudness meter, full playback |
| True peak | Below minus one dBTP | True-peak meter with oversampling |
| Head and tail | No long lead-in, digital silence at the end | Zoom into the waveform |
| Naming | Project, version, rate, bit depth | Batch check, no spaces |
| Metadata | Title, writer, copyright, ISRC | Player and distribution backend |

## Tails, names and metadata

A millisecond or two of lead-in is enough; longer makes players feel slow to start. The tail should reach digital silence, with no reverb chopped off and no noise floor left behind. Loops need a tail that joins the head, ideally with an aligned version supplied alongside. Use only letters, digits, underscores and hyphens in file names, and put project, version, sample rate and bit depth in the name rather than the word 'final'. Fill in title, writer, copyright and ISRC, and note tempo and key in the readme. Once the rule is set, case and separators admit no exceptions.

## Do not check on the wrong system

Use a loudness meter rather than guessing, a true-peak meter rather than sample peak, and the reference track supplied by the recipient for A/B. The common failure is a limiter pushed too hard, so the file sounds flatter once the platform turns it down; another is checking only the WAV and never the AAC. A checklist does not slow you down. It keeps the rework on your side of the handoff instead of in the recipient's inbox.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "E4", "G4", "C5", "G4", "E4", "C4"], "label": "One phrase at two levels", "label_en": "One phrase at two levels", "hint": "Match loudness first, and do not mistake louder for better", "hint_en": "Match loudness first, and do not mistake louder for better"}
```
:::
