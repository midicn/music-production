---
id: sample-rate-conversion
site: prod
cat: B5
title: 采样率转换
title_en: Sample-Rate Conversion
summary: 44.1 与 48 kHz 互转不是改个数字，滤波器决定转完还剩多少细节。
summary_en: Converting between 44.1 and 48 kHz is not a renumbering exercise; the filter decides how much detail survives.
level: standard
tags: [采样率, 重采样, 滤波, 混叠]
tags_en: [sample rate, resampling, filtering, aliasing]
alias: [重采样, 采样率转换, SRC, sample rate conversion, resampling]
links:
  - "[[glossary:sample-rate]]"
  - "[[glossary:bit-depth]]"
  - "[[glossary:latency]]"
instances:
  - groove-000000 | 138 BPM 放克鼓组，镲片与军鼓边击的高频最先暴露重采样留下的毛刺（C1）
  - atepp-001115 | 肖邦第一叙事曲，钢琴泛音密集，转换后尾音的颗粒与空气感会变（C1）
  - cyberhymnal-008729 | 管风琴赞美诗，低频与长混响检验重采样是否引入振铃（C1）
sources:
  - 采样定理与重建滤波的表述，依数字音频通识教材核对，未抄原文
  - 常见采样率之间的整数与非整数比关系，依公开技术资料核对，未抄文本
updated: 2026-10-28
---

::: zh
## 问题

素材来自 44.1 kHz 的唱片、48 kHz 的视频工程、96 kHz 的现场录音，最后要汇到一个工程里。直接把采样率标签改掉会改变播放速度与音高，必须重采样。转得好不好，听的是高频还剩多少、瞬态有没有糊。

## 原理

重采样先在原采样率上插值出连续波形，再按新采样率重新取点。理想插值需要无限长的 sinc 核，实际用有限长度的滤波器近似，长度与滚降决定质量。降采样前必须先低通，把超过新奈奎斯特频率的成分滤掉，否则它们折回可听频段变成混叠。44.1 与 48 的比值是 147 比 160，属非整数比，需要更长的滤波器；48 与 96 是整数比，处理简单得多。实时转换为了低延迟会缩短滤波器，离线转换可以慢慢算。

## 参数与做法

同一工程统一采样率，减少反复转换。给视频做配乐直接录 48 kHz，省掉最后一次转换。母带保持在录制时的采样率，交付前一次性转换。离线导出时选高质量设置，实时监听用低延迟设置即可。位深与采样率是两件事，转采样率不会自动加抖动。超过 96 kHz 的采样率对回放收益有限，麦克风与房间往往先成为瓶颈。

## 听什么

在放克鼓组的镲片上听高频是否发毛，在钢琴叙事曲的尾音上听泛音是否变薄，在管风琴长音上听低频是否有嗡鸣。转换质量差时，声音不会明显变糟，只会变得不那么干净。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C6","E6","G6","C7","G6","E6","C6","G5"],"label":"高把位泛音","label_en":"High-register overtones","hint":"最高几个音的能量集中在高频，重采样滤波不当时这里最先失去光泽","hint_en":"The top notes live in the high band, where a poor resampling filter dulls first"}
```
:::

::: en
## The problem

Material arrives at 44.1 kHz from records, 48 kHz from video projects and 96 kHz from location recordings, and all of it has to meet in one session. Simply relabelling the rate changes speed and pitch, so the audio must be resampled. Whether it goes well is audible in how much high end survives and whether transients smear.

## How it works

Resampling interpolates a continuous waveform at the old rate, then samples it again at the new one. Ideal interpolation needs an infinitely long sinc kernel; real converters approximate it with finite filters whose length and roll-off set the quality. Before downsampling, everything above the new Nyquist frequency must be filtered out, or it folds back into the audible band as aliasing. The ratio between 44.1 and 48 is 147 to 160, a non-integer, so the filter must be longer; 48 to 96 is an integer ratio and much simpler. Real-time conversion shortens filters to keep latency low, while offline conversion can take its time.

## Settings and practice

Keep one sample rate per project and convert as few times as possible. For picture work, record at 48 kHz and skip the last conversion. Keep the master at its recording rate and convert once at delivery. Use high-quality settings for offline export and low-latency settings only for live monitoring. Bit depth and sample rate are separate issues, and resampling does not add dither by itself. Rates above 96 kHz buy little on playback, because microphones and rooms usually limit first.

## What to listen for

On the funk kit, listen for grit on the cymbals; on the Chopin ballade, for thinning overtones in the tail; on the organ hymn, for hum in the low pedal. Bad conversion rarely sounds obviously broken, it just sounds less clean.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C6","E6","G6","C7","G6","E6","C6","G5"],"label":"High-register overtones","label_en":"High-register overtones","hint":"The top notes live in the high band, where a poor resampling filter dulls first","hint_en":"The top notes live in the high band, where a poor resampling filter dulls first"}
```
:::
