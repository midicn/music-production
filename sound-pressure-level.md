---
id: sound-pressure-level
site: prod
cat: A5
title: 声压级与 dB
title_en: Sound Pressure Level and dB
summary: 分贝是对数刻度，声压级把电压、距离与听感连在一起。
summary_en: The decibel is a logarithmic ratio; sound pressure level connects voltage, distance and perceived loudness.
level: standard
tags: [声压级, 分贝, 监听校准, 响度, 动态]
tags_en: [sound pressure level, decibel, monitor calibration, loudness, dynamics]
alias: [分贝, 声压, 响度, dB, SPL, sound pressure level]
links:
  - "[[glossary:lufs]]"
  - "[[glossary:true-peak]]"
  - "[[glossary:headroom]]"
  - "[[glossary:monitoring]]"
instances:
  - mutopia-000497 | 贝多芬第五交响曲，动态跨度大，适合在固定声压级下检查弱奏是否清楚（C1）
  - pdmx-000450 | 勃拉姆斯《德意志安魂曲》，合唱与钢琴层次多，用来比较不同监听声压下的平衡（C1）
  - cyberhymnal-000785 | 赞美诗《All for Jesus》，持续音稳定，适合用声压计校准单只音箱（C1）
sources:
  - Everest, F. Alton，Master Handbook of Acoustics（McGraw-Hill）— 声压级与心理声学章节核对，未引用
  - Ballou, Glen，Handbook for Sound Engineers（Focal Press）— 监听与测量章节核对，未引用
updated: 2026-10-28
---

::: zh
## 问题
同样旋钮位置，白天与深夜听起来不同；两段音乐电平表一样，响度却差很多。要把「响」说清，必须区分声压级、电平与听感。

## 物理或房间
声压级是声压与 20 微帕之比的常用对数乘二十。每增加 6 dB 声压翻倍，每增加 10 dB 中频听感约翻倍。自由场距离每翻倍衰减约 6 dB，房间内还受反射与模式影响。dBFS 是数字满刻度，dB SPL 是空气压强，不能直接换算。

## 做法与判断
用 C 计权、慢档声压计，在听音位测单声道粉红噪声，把每只音箱调到约 83 dB SPL，作为混音参考。日常留 6 dB 以上余量。对比时先匹配响度，再判断音色，否则更响的一方总显得更清楚。

## 听什么
同一段混音分别放在 70、80、90 dB 听。小音量下低频与高频先消失，中频反而突出；大音量时低频与齿音同时变多。再听动态大的管弦乐，确认弱奏没有被房间噪声淹没。

## 常见误解
分贝不是绝对单位，它永远是比值。功率翻倍是 3 dB，不是响度翻倍。0 dB SPL 接近听阈，不是没有声音。手机声压计只能作粗略比较。

```audiolab
{"type":"instrument","gm":"Timpani","synth":"struck","phrase":["D2","A2","D3","A3"],"label":"同一力度，低音与高音","label_en":"Same force, low and high","hint":"播放电平相同，但低频与高频的响度感不同；把音量降到很小，再听一次。","hint_en":"The playback level is fixed, yet low and high notes feel different in loudness. Lower the volume and listen again."}
```
:::

::: en
## The problem
The same knob setting sounds different at noon and midnight, and two tracks at equal meter level can differ. Separate SPL, level and perception.

## Physics or room
Sound pressure level is twenty times the log of pressure over 20 µPa. Plus 6 dB doubles pressure; plus 10 dB roughly doubles perceived loudness at mid frequencies. In a free field level drops about 6 dB per doubling of distance; rooms add reflections and modes. dBFS is digital full scale, dB SPL is air pressure.

## Practice and judgement
With a C-weighted, slow SPL meter, play mono pink noise at the listening position and set each speaker to about 83 dB SPL. Keep 6 dB of headroom. Match loudness before comparing tone, or the louder version always sounds clearer.

## What to listen for
Play the same mix at 70, 80 and 90 dB. At low level, bass and treble fade first and mids dominate; at high level, bass and sibilance grow. On a dynamic orchestral piece, check that quiet passages are not lost in room noise.

## Common misunderstandings
Decibels are always ratios, not absolutes. Doubling power is 3 dB, not double loudness. 0 dB SPL is near the hearing threshold, not silence. Phone meters are rough.

```audiolab
{"type":"instrument","gm":"Timpani","synth":"struck","phrase":["D2","A2","D3","A3"],"label":"Same force, low and high","label_en":"Same force, low and high","hint":"The playback level is fixed, yet low and high notes feel different in loudness. Lower the volume and listen again.","hint_en":"The playback level is fixed, yet low and high notes feel different in loudness. Lower the volume and listen again."}
```
:::
