---
id: loudness-metering
site: prod
cat: B5
title: 响度表
title_en: Loudness Metering
summary: 采样峰值、真峰值与 LUFS 分别描述什么，怎样一起检查导出音频。
summary_en: What sample peak, true peak and LUFS describe, and how to use them together when checking an export.
level: standard
tags: [响度, 峰值, LUFS, 真峰值]
tags_en: [loudness, peak, LUFS, true peak]
alias: [响度表, 电平表, LUFS 表, loudness meter, true peak]
links:
  - "[[glossary:lufs]]"
  - "[[glossary:headroom]]"
  - "[[glossary:meter]]"
instances:
  - groove-000003 | 鼓循环渲染后可同时观察采样峰值、真峰值与短时响度的变化 | Render the drum loop and observe sample peak, true peak and short-term loudness together
  - atepp-001114 | 钢琴演奏数据可作动态素材；用固定音色渲染后测量，不含原现场掌声 | Piano performance data supplies dynamic material; measure a fixed-timbre render without claiming original audience applause
  - cyberhymnal-000001 | 持续管风琴音可用于比较持续响度与峰值，但过载风险需在实际音频链测量 | Sustained organ can compare continuous loudness with peak level; measure overload in the actual audio path
sources:
  - "https://support.spotify.com/us/artists/article/loudness-normalization/"
  - ITU-R BS.1770 响度测量方法的用途，参考公开标准说明。
  - 真峰值与采样峰值之差；数字音频惯例是主要依据。
updated: 2026-11-02
---

::: zh
## 容易停住的地方

峰值表描述幅度上限，响度表按规定的加权、时间窗口和门限计算节目电平。它们是不同的测量工具，不能用一个数完全代表主观音量或制作质量。交付要求可能同时包含响度与真峰值限制。

## 原因

采样峰值以dBFS记录样点幅度；真峰值以dBTP估算重建后样点之间可能出现的峰值。短时响度常用三秒窗口，整体响度对测量范围积分并应用相应门限。平台降低整曲回放增益通常不会再次压缩其内部动态；某些播放模式可能另加限制，须与单纯增益归一化区分。

## 怎么绕过去

按交付规范设置测量范围，完整播放节目并记录整体响度、峰值和必要的动态指标。比较两版时先匹配响度，再听音色和段落关系；不要为了命中单一LUFS数值自动削平所有瞬态。输出余量按实际平台、格式与编码要求确定。

## 听这几处

把同一鼓循环或钢琴段落渲染为音频，同时看峰值与响度；再做一版只降低增益、一版改变压缩，比较它们怎样影响段落关系。持续管风琴音可帮助观察长音电平，但不能仅凭持续响度判断是否过载，仍需检查实际峰值与输出链。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"e e e e e e e e","bpm":80,"label":"响度测量的稳定节奏","label_en":"A steady rhythm for metering","hint":"把节奏录入 DAW，用峰值表与响度表同时观察；改变重音后重测，比较峰值与短时响度的响应。","hint_en":"Record the rhythm in a DAW and watch peak and loudness meters together. Change accents and remeasure their different responses."}
```
:::

::: en
## Where people stall

Peak meters describe amplitude limits; loudness meters use specified weighting, windows and gating to measure programme level. Neither number completely describes perceived volume or production quality. Delivery requirements may specify both loudness and true-peak limits.

## The reason

Sample peak in dBFS measures sample amplitude; true peak in dBTP estimates reconstructed inter-sample peaks. Short-term loudness commonly uses a three-second window, while integrated loudness measures the selected programme with applicable gating. Turning down playback gain normally does not compress internal dynamics again; any mode that adds limiting is a separate operation.

## How to get around it

Measure the complete programme using the required scope, logging integrated loudness, peaks and any required dynamic metrics. Loudness-match versions before judging timbre and sectional relationships rather than flattening every transient to hit one LUFS number. Choose headroom for the actual platform, format and codec.

## Listen to these

Render one drum loop or piano passage and observe peak and loudness together. Compare a gain-only reduction with a compressed version to examine their effects on musical contrasts. Sustained organ audio helps inspect continuous level, but loudness alone cannot diagnose overload; check actual peaks and the output path.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"e e e e e e e e","bpm":80,"label":"A steady rhythm for metering","label_en":"A steady rhythm for metering","hint":"Record the rhythm in a DAW and watch peak and loudness meters together. Change accents and remeasure their different responses.","hint_en":"Record the rhythm in a DAW and watch peak and loudness meters together. Change accents and remeasure their different responses."}
```
:::
