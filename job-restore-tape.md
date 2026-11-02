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
  - pdmx-000107 | 探戈旋律与配器的谱面参照，不是磁带转录 | Scored tango melody and instrumentation rather than a tape transfer
  - pdmx-000077 | 旧式歌曲音符参照，不包含降噪前后的字头录音 | Older-song notes without recorded consonant attacks before and after denoising
  - pdmx-000048 | 小编制歌曲的乐句参照，不记录真实呼吸声 | Small-ensemble phrasing without recorded breathing
  - pdmx-000037 | 伴奏与旋律比例参照，不是音频修复的A/B成品 | Accompaniment/melody balance reference rather than restoration A/B audio
sources:
  - "https://www.iasa-web.org/tc05/22114-deterioration-replay"
  - 磁带转录、去嗡与降噪的处理顺序，对照音频修复惯例整理。
  - 原始文件留存、校验和与存档格式（档案数字化惯例）。
tool_kind: guide
tool_vendor: —
tool_form: 流程
tool_platforms: [通用]
tool_price: 不适用
tool_jobs: [流程]
tool_verified: 2026-10-30
updated: 2026-11-02
---

::: zh
## 你要交的是什么

先确定载体状态、录制格式与安全重放条件，再做数字转录。脆化、霉变、粘连或走带异常的磁带不应为“先留副本”而直接播放，应由熟悉该载体的人员评估。交付可包括未经处理的转录母版、修复版和访问版，分别命名并保留校验值与处理日志。采样率和位深按档案或项目规范选择。

## 三步走

在确认可重放后，使用合适且维护良好的机器核对速度、轨宽、均衡和方位角，记录设置并完整转录。处理在数字副本上进行，每一步保留可回退记录。根据具体噪声比较处理顺序，而不是默认点击、去嗡、降噪对所有磁带都相同。

## 用到的工具与页面

先测量是否有稳定的电源基频与谐波，再决定去嗡范围，不能只按所在国家猜频率。宽带降噪一次或多次是否更好，应以同一片段对照判断。不要为了“补老录音的高频”自动提升高频；先确认缺失信息与本来存在的音色，并保留原始转录。

## 验收标准

核对转录完整、左右声道、速度和时间起点；检查处理是否新增金属声、断裂或削波，是否损伤原有音符与语音。未经处理母版不必为了更响而限制动态。修复版应说明目标与不可恢复处，访问版按用途另行编码，所有版本与校验清单一起交付。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","G3","A3","E3"],"label":"修复选材的旋律参照","label_en":"Melodic reference for restoration selection","hint":"合成尾音不含磁带噪声。实际修复要留存未处理转录，并从同一录音制作处理与旁通版本。","hint_en":"Synthesized decays contain no tape noise. Preserve an unprocessed transfer and make processed and bypassed versions from the same recording."}
```

## 常见返工原因

避免覆盖原始转录、只留有损访问版、未记录处理步骤，或把不稳定载体反复试播。出现新伪影时退回上一版本，而不是继续叠加处理。保存载体与机器信息，才能解释数字文件代表了什么。
:::

::: en
## What you have to hand over

Assess carrier condition, recording format and safe replay conditions before digitisation. Do not play brittle, mouldy, sticky or mechanically unstable tape merely to obtain a first copy; seek assessment by someone familiar with the carrier. Deliver an unprocessed transfer master, restoration and access copy as appropriate, separately named with checksums and logs. Choose rate and depth for the archival or project specification.

## Three steps

Once replay is judged safe, use a suitable maintained machine and verify speed, track format, equalisation and azimuth, logging settings before a complete transfer. Process digital copies with reversible records. Compare the order for actual defects rather than assuming click repair, de-hum and denoising always follow one sequence.

## Tools and pages

Measure any stable mains fundamental and harmonics before choosing de-hum bands rather than guessing from country. Test whether one denoising pass or several is better on the same excerpt. Do not automatically boost highs to restore an old recording: distinguish lost information from original timbre and retain the raw transfer.

## Acceptance checks

Check complete transfer, channels, speed and time origin. Inspect for new metallic artifacts, discontinuities or clipping and damage to notes or speech. The unprocessed master does not need loudness-driven limiting. Document restoration aims and unrecoverable passages, encode access copies separately, and deliver versions with a checksum inventory.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","G3","A3","E3"],"label":"Melodic reference for restoration selection","label_en":"Melodic reference for restoration selection","hint":"Synthesized decays contain no tape noise. Preserve an unprocessed transfer and make processed and bypassed versions from the same recording.","hint_en":"Synthesized decays contain no tape noise. Preserve an unprocessed transfer and make processed and bypassed versions from the same recording."}
```

## Why work gets sent back

Avoid overwriting the transfer, retaining only a lossy access file, losing processing records or repeatedly trying an unstable carrier. Revert when new artifacts appear rather than stacking more processing. Preserve carrier and machine details so the digital file can be interpreted.
:::
