---
id: loudness-metering
site: prod
cat: B5
title: 响度表
title_en: Loudness Metering
summary: 峰值表防削波，响度表管感受，LUFS 与真峰值各看一头。
summary_en: Peak meters stop clipping and loudness meters track perception; LUFS and true peak each watch one end.
level: standard
tags: [响度, 峰值, LUFS, 真峰值]
tags_en: [loudness, peak, LUFS, true peak]
alias: [响度表, 电平表, LUFS 表, loudness meter, true peak]
links:
  - "[[glossary:lufs]]"
  - "[[glossary:headroom]]"
  - "[[glossary:meter]]"
instances:
  - groove-000003 | 80 BPM 灵魂乐鼓循环，底鼓的瞬态看峰值，整体厚度看响度（C1）
  - atepp-001114 | 肖邦第一叙事曲现场录音，掌声与弱奏并存，响度表比峰值表更贴近听感（C1）
  - cyberhymnal-000001 | 管风琴赞美诗，长音持续时响度平稳，容易掩盖峰值表看不到的过载风险（C1）
sources:
  - ITU-R BS.1770 响度测量方法的用途，参考公开标准说明。
  - 真峰值与采样峰值之差；数字音频惯例是主要依据。
updated: 2026-10-28
---

::: zh
## 容易停住的地方

一首歌响不响，和它的峰值高不高不是一回事。峰值表只告诉你有没有超过满刻度，响度表告诉你人耳觉得多响。母带、播客、流媒体交付都按响度定标准，所以两把尺子都得看。

## 原因

峰值表读的是单个采样点或相邻样点间的最大幅度，单位 dBFS，超过 0 就削波。响度表先对信号做频率加权，模拟人耳对中频更敏感的特性，再在时间上做门限与积分，得到 LUFS。短期响度看三秒窗口，整体响度看整段，真峰值用插值估算采样点之间的实际峰值，能抓到采样峰值漏掉的过冲。流媒体平台会把过响的曲子往下压，压得越多，动态被削得越狠。

## 怎么绕过去

混音时盯峰值，留 3 到 6 dB 余量。母带时盯整体响度，按交付平台的目标定值，别一味追响。真峰值保持在负一 dBTP 以下，给有损编码留空间。用短期响度看段落之间的平衡，用整体响度看整首。比较两版时先对齐响度，否则更响的那版总显得更好。手机、电视、车载的回放响度差别很大，别只在一个环境里定标准。

## 听这几处

在灵魂乐鼓循环里听底鼓的冲击与整体厚度的关系，在叙事曲现场录音里听弱奏是否被掌声淹没，在管风琴长音里听持续段是否稳定。表上的数字只是参照，最终还是要用耳朵确认段落之间的起伏还在。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"e e e e e e e e","bpm":80,"label":"80 BPM 的稳定律动","label_en":"A steady 80 BPM pulse","hint":"每一拍的重音让响度表跳动，听重音与持续音之间的落差","hint_en":"Each accent makes the meter jump; hear the gap between accents and sustain"}
```
:::

::: en
## Where people stall

How loud a track feels is not the same as how high its peaks sit. A peak meter only says whether the signal passed full scale; a loudness meter says how loud the ear judges it. Mastering, podcasting and streaming delivery all set targets in loudness, so both rulers matter.

## The reason

A peak meter reads the largest amplitude of a sample or between neighbouring samples in dBFS, and anything above zero clips. A loudness meter applies frequency weighting that mimics the ear's sensitivity to the midrange, then gates and integrates over time to produce LUFS. Short-term loudness uses a three-second window, integrated loudness covers the whole programme, and true peak interpolates between samples to catch overshoots a sample peak misses. Streaming platforms turn down tracks that are too loud, and the more they turn down, the more dynamics get squeezed.

## How to get around it

While mixing, watch peaks and leave 3 to 6 dB of headroom. While mastering, watch integrated loudness and set it to the delivery target instead of chasing maximum level. Keep true peak below minus one dBTP to leave room for lossy encoding. Use short-term loudness to judge balance between sections and integrated loudness for the whole track. Align loudness before comparing two versions, otherwise the louder one always seems better. Phones, televisions and cars play back at very different levels, so do not set the standard in one room only.

## Listen to these

On the soul loop, hear how kick impact relates to overall weight; on the live ballade, whether quiet passages survive the applause; on the organ hymn, whether sustained passages stay steady. The numbers are a reference, and the ear still has to confirm that the rise and fall between sections is intact.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"e e e e e e e e","bpm":80,"label":"A steady 80 BPM pulse","label_en":"A steady 80 BPM pulse","hint":"Each accent makes the meter jump; hear the gap between accents and sustain","hint_en":"Each accent makes the meter jump; hear the gap between accents and sustain"}
```
:::
