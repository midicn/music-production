---
id: focusrite-scarlett
site: prod
cat: C
order: 33
title: Focusrite Scarlett
title_en: Focusrite Scarlett
summary: 两路进两路出的入门接口，做小样与单人录音够用，短板在增益上限与扩展性。
summary_en: A two-in two-out starter interface that is enough for demos and solo tracking, with limits on gain and expansion.
level: standard
tags: [音频接口, 入门, 录音, 小样]
tags_en: [audio interface, beginner, recording, demo]
alias: [Scarlett, 福克斯特, 2i2, Solo, 入门声卡]
tool_kind: hardware
tool_vendor: Focusrite
tool_form: 硬件
tool_platforms: [macOS, Windows]
tool_price: 硬件
tool_jobs: [录音, 编曲, 播客]
links:
  - "[[glossary:preamp]]"
  - "[[glossary:condenser-microphone]]"
  - "[[instrument:acoustic-guitar]]"
instances:
  - thesession-000001 | 一支小提琴或长笛的单声部曲调，一支话筒或一路线路输入就能录完
  - openscore-000009 | 人声加钢琴的短歌，两路输入刚好一唱一伴，最能看出这种接口的典型用法
  - giantmidi-000916 | 独奏钢琴的起伏，两路话筒录一台琴时要靠摆位而不是靠增益硬推
sources:
  - 厂商公开的输入输出、幻象电源与监听功能说明，参考官方页面。
  - 话放增益与低灵敏度动圈话筒的匹配关系；录音惯例是主要依据。
tool_verified: 2026-10-30
updated: 2026-10-30
---

::: zh
## 适用工作

用一支电容话筒加一路 DI 录完一首人声小样。给播客或线上课程提供稳定输入，接上就能用。把合成器与鼓机的线路输出直接录成音频轨。带一支低灵敏度动圈录人声，只要肯把增益开大。两路同时录唱与吉他，事后对齐修一修就能发。在支持回环的型号上，把线上会议的发言与系统声音一起录下来。

## 原理

接口走 USB 总线供电，插上电脑就出现输入输出，不需要外接电源。每路有话放、幻象电源与增益旋钮，前面板能开直接监听，把输入原样送到耳机与主输出。部分型号带一个固定的高频提升开关，用来补动圈话筒的暗淡，也有型号把系统声音回环进来。旋钮没有刻度，增益只能看灯，回放时最好记下位置。转换与话放都是干净取向，够用但不出彩。

## 边界

- 增益上限因代次而异。推低灵敏度动圈时常常要开到接近最大，底噪跟着上来。
- 只有两路，录鼓或小乐队不够；扩展口在高端型号才有。
- 总线供电遇到劣质集线器或长线会掉线，录音中途断连最伤人。
- 驱动支持有年限，系统大版本更新后要确认还能用。
- 高频提升开关是固定曲线，弥补不了话筒本身的缺陷，别把它当万能。
- 这个价位，钱更该花在房间与话筒上；它不会成为瓶颈，也不会救你。
- 面板没有真正的电平表，只有颜色灯，判断余量最终要靠 DAW 表头。

## 替代

预算再紧，Behringer UMC 系列能完成同样的活；愿意多花一点，Audient iD 的话放更扎实；要更多通道与数字扩展，Clarett 或 MOTU M 系列更合适。搭配 Cloudlifter 一类的前置放大器，可以让低输出动圈在入门接口上工作得体面。

## 上手

先学三件事：增益结构、直接监听与软件监听的区别、幻象电源什么时候开。再练一次两话筒摆位，把一支话筒录到 -12 dBFS 再谈音色。配合读话放、电容话筒、音频接口三条。

```audiolab
{"type":"instrument","gm":"Acoustic Guitar (steel)","synth":"plucked","phrase":["G2","D3","G3","B3","D4","B3","G3","D3"],"label":"一支话筒下的木吉他","label_en":"A steel-string guitar under one microphone","hint":"听拨弦的瞬态与琴箱共鸣，入门话放要接得住又不糊","hint_en":"Listen to the pick attack and body resonance; a budget preamp must hold it without blurring"}
```
:::

::: en
## Jobs it covers

Record a full vocal demo with one condenser and one DI. Give a podcast or online class a reliable input that works when plugged in. Capture a synth or drum machine from its line outputs as audio. Track a vocal on a low-output dynamic, provided you are willing to push the gain. Record voice and guitar together on two inputs and fix the alignment afterwards.

## How it works

The box is bus powered over USB, so inputs and outputs appear as soon as it is connected. Each channel has a preamp, phantom power and a gain knob, and a direct-monitor switch sends the input to the headphones and main outputs untouched. Some models add a fixed high-frequency lift to brighten dull dynamic mics, and some offer a loopback of the computer's output. Conversion and preamps are clean rather than characterful: serviceable, not memorable.

## Limits

- Gain range varies by generation. With a low-output dynamic you often run near maximum, and the noise floor comes up with it.
- Two inputs are not enough for a kit or a small band, and digital expansion appears only on the dearer models.
- Bus power drops out with a poor hub or a long cable. Losing the connection mid-take is the expensive failure.
- Driver support has a shelf life; check that a major OS update still works before relying on it.
- The high-frequency switch is a fixed curve. It cannot repair a dull microphone, so do not treat it as a cure.
- At this price the money belongs in the room and the mic. This box will not be your bottleneck, nor will it rescue you.

## Alternatives

On a smaller budget, the Behringer UMC range does the same job. Spending a little more buys the firmer preamps of an Audient iD; needing more channels and digital expansion points to Clarett or the MOTU M series. An inline booster such as a Cloudlifter lets a low-output dynamic behave on a starter interface.

## First three things

Learn gain staging, the difference between direct and software monitoring, and when phantom power should be on. Then practise one two-microphone placement. Read the preamp, condenser microphone and audio interface entries alongside this one.

```audiolab
{"type":"instrument","gm":"Acoustic Guitar (steel)","synth":"plucked","phrase":["G2","D3","G3","B3","D4","B3","G3","D3"],"label":"一支话筒下的木吉他","label_en":"A steel-string guitar under one microphone","hint":"听拨弦的瞬态与琴箱共鸣，入门话放要接得住又不糊","hint_en":"Listen to the pick attack and body resonance; a budget preamp must hold it without blurring"}
```
:::
