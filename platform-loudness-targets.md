---
id: platform-loudness-targets
site: prod
cat: A8
title: 各平台响度目标
title_en: Platform Loudness Targets
summary: 不同平台回放目标不同，母带响度要按发布场景取舍。
summary_en: Streaming, broadcast and club playback normalise or expect different levels, so a master's loudness should follow its release context.
level: standard
tags: [母带, 响度, 流媒体]
tags_en: [mastering, loudness, streaming]
alias: [平台响度, 流媒体响度, platform loudness]
links:
  - "[[glossary:lufs]]"
  - "[[glossary:loudness-normalization]]"
  - "[[glossary:true-peak-limiter]]"
instances:
  - pdmx-000995 | 段落对比可作响度实验素材，先渲染再施加固定增益，检查动态关系 | Render contrasting sections, then apply fixed gain to inspect their dynamic relationship
  - mutopia-001411 | 稀疏钢琴织体便于比较增益调整，音源底噪与尾音需以实际渲染为准 | Sparse piano helps compare gain changes; source noise and tails depend on the actual render
  - essen-000024 | 短曲便于练习整段 LUFS 与真峰值测量，按实际平台要求生成交付版本 | A short piece supports integrated-LUFS and true-peak practice; create delivery versions for actual platform requirements
sources:
  - "https://support.spotify.com/us/artists/article/loudness-normalization/"
  - Spotify、Apple Music 与 YouTube 的响度归一目标——依据来自平台公开帮助文档。
  - 流媒体与广播响度目标的差异，对照交付与母带惯例整理。
updated: 2026-11-02
---

::: zh
平台会按自己的目标调整回放音量。母带做得过响，不一定在平台上更响，反而可能被压小。

## 问题

同一首母带在不同回放模式下可能有不同电平。若制作时已经用重限制牺牲瞬态，平台后来降低整体增益不会把瞬态恢复；这项增益调整本身也不等于再做一次动态压缩。比较时须区分母带处理与播放器行为。

## 目标与标准

回放归一目标不等于所有母带的强制交付响度。以Spotify截至2026-11-02的说明为例，Normal模式使用−14 LUFS，另有用户选择的其他模式，网页与第三方设备行为也可能不同。广播、影视和其他平台须分别查当前规范，不能把−14 LUFS与−1 dBTP当作全行业统一标准。

## 做法

先确认发行方要接收什么，再检查归一化后的试听。专辑或EP不必每首都做成同一个整体响度：有意的曲间对比应保留，平台也可能采用整张专辑的共同增益。保留高质量母版，需要不同用途版本时，分别记录处理目标和设置。

## 听什么

用匹配响度的参考判断音色、瞬态和段落关系。平台只降低增益时，不会自动修复此前压坏的动态，也不会再把它压得更扁；若听到明显失真，应分别检查原母版、编码和播放模式。

```audiolab
{"type":"instrument","gm":"Flute","synth":"blown","phrase":["C5","E5","G5","E5","C5"],"label":"固定增益调整的测试短句","label_en":"A phrase for a fixed-gain comparison","hint":"在 DAW 录下后测整段响度，再只用固定增益调整。音量会变，内部强弱比例不应被当作压缩改变。","hint_en":"Record and measure integrated loudness, then change only fixed gain. Level changes; do not mistake that for compression of internal dynamics."}
```

## 常见误解

平台会归一，不代表母带可以随便做响，音色与动态仍由母带决定。-14 LUFS 不是所有平台的统一值，各家算法与目标并不相同。归一也不会让压坏的瞬态恢复。
:::

::: en
Platforms adjust playback level to their own target. A very loud master may simply be turned down, its dynamics gone.

## The problem

One master can play at different levels under different playback modes. If heavy limiting already sacrificed transients, later fixed-gain reduction will not restore them; the gain change itself is not another stage of dynamic compression. Separate mastering decisions from player behaviour when comparing.

## Goals and standards

Playback normalisation targets are not mandatory loudness values for every master. Spotify’s guidance checked on 2026-11-02 uses −14 LUFS for Normal with other user modes and different behaviour on web or third-party devices. Check current requirements separately for broadcast, picture and other platforms rather than imposing one industry-wide LUFS/true-peak pair.

## Practice

Confirm delivery requirements before checking normalised playback. Album or EP tracks need not have identical integrated loudness: preserve intentional contrasts, and a platform may apply a common album gain. Retain a high-quality master and document goals and settings for any use-specific versions.

## What to listen for

Use loudness-matched references for timbre, transients and section relationships. Gain reduction neither repairs previously lost dynamics nor automatically compresses them further. Investigate the master, codec and playback mode separately when audible distortion appears.

```audiolab
{"type":"instrument","gm":"Flute","synth":"blown","phrase":["C5","E5","G5","E5","C5"],"label":"A phrase for a fixed-gain comparison","label_en":"A phrase for a fixed-gain comparison","hint":"Record and measure integrated loudness, then change only fixed gain. Level changes; do not mistake that for compression of internal dynamics.","hint_en":"Record and measure integrated loudness, then change only fixed gain. Level changes; do not mistake that for compression of internal dynamics."}
```

## Common misunderstandings

Normalisation does not mean any loudness will do, because tone and dynamics still come from the master. Nor is -14 LUFS universal; services differ. Normalisation is not quality control, since crushed transients do not return.
:::
