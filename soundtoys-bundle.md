---
id: soundtoys-bundle
site: prod
cat: C
order: 14
title: Soundtoys（饱和、延迟与调制）
title_en: Soundtoys (Saturation, Delay and Modulation)
summary: 一套带明显性格的效果器，染色、回声与摆动各有一件。
summary_en: A bundle with audible character, covering saturation, echo and movement with one tool each.
level: standard
tags: [插件, 饱和, 延迟, 调制]
tags_en: [plugin, saturation, delay, modulation]
alias: [Soundtoys, Soundtoys 5, Decapitator, EchoBoy, Little AlterBoy, 饱和插件]
tool_kind: plugin
tool_vendor: Soundtoys
tool_form: 插件
tool_platforms: [macOS, Windows]
tool_price: 买断
tool_jobs: [混音, 声音设计, 编曲]
tool_verified: 2026-10-30
links:
  - "[[glossary:delay]]"
  - "[[glossary:harmonics]]"
  - "[[glossary:phase]]"
instances:
  - groove-000000 | 138 BPM 放克鼓循环，军鼓与踩镲的瞬态密，饱和加多少立刻听得出来（C1，参照不是该插件的演示）
  - mutopia-000005 | 阿瓜多古典吉他练习曲，拨弦干净，适合听延迟与调制是否盖住起音（C1，参照不是该插件的演示）
  - oga-000004 | 游戏战斗配乐，编制满、瞬态硬，失真与滤波的取舍比纯音乐更明显（C1，参照不是该插件的演示）
sources:
  - Soundtoys 官方产品页的插件清单与授权方式说明，依公开资料核对，未抄原文
  - 饱和、延迟与调制类效果的常见用法，依混音通识核对，未抄文本
updated: 2026-10-30
---

::: zh
## 它能完成什么

给鼓组、贝斯或人声加一层可听的厚度与咬字，不必真的过一遍磁带。把一条干旋律送进短延迟或磁带式回声，做出空间与重复。用移调与共振峰控制做人声的另一种性别或年龄，或做和声层。在双轨人声或吉他上做细微的时间与音高差，让声部变宽。把鼓组或贝斯送进失真，做副歌前后的强弱对比。用滤波与颤音做运动感，把静态的铺底推起来。

## 它怎么工作

这一套不是同一个算法的多个皮肤，而是各自独立的处理。饱和类用非线性电路模型给信号加谐波，输入越大越脏；延迟类用磁带、模拟或数字的延迟线，反馈路径里常带滤波；调制类用短延迟与相位偏移做出摆动；移调类把音高与共振峰分开移动，所以能改音色而不只是改音高。共同点是界面直接、听感先行，参数多半只有几个，但每个都会明显改变结果。同一插件在单声道与立体声轨上的行为不同，宽度类尤其明显。

## 边界与坑

- 全部插件都要 iLok 授权，机器授权或加密狗二选一；换电脑与协作前先把授权算进流程。
- 染色是它的目的，不是副作用。需要透明处理时，这套会先把声音改掉。
- 延迟的反馈推高会自激，现场要设上限并留一个旁通。
- 部分插件对采样率与过采样敏感，高频失真在 96 kHz 工程里可能比 48 kHz 更明显。
- 版本升级与插件格式跟随安装器，老工程打开前要确认对方版本不低于制作时的版本。
- 没有独立运行版，也没有硬件复刻；现场要带走的是工程与授权，不是机架。

## 替代与搭配

要更可控的饱和看 FabFilter Saturn 2；要整套复古染色看 Universal Audio 的插件线；只要干净延迟，ValhallaDelay 更省事。它常放在 Valhalla 混响之前：先做出脏与重复，再让混响把尾巴接住。

## 上手路径

先学饱和的输入与输出补偿，再学延迟的反馈与滤波，最后学移调时的共振峰。配合本站「延迟」「谐波」「相位」三篇读。

```audiolab
{"type":"instrument","gm":"Electric Guitar (clean)","synth":"plucked","phrase":["E3","G3","B3","E4","B3","G3"],"label":"一段干吉他，待加厚","label_en":"A dry guitar line to thicken","hint":"先听拨弦的起音，再想饱和会添哪些谐波、短延迟会不会糊掉它","hint_en":"Hear the pick attack first, then imagine which harmonics saturation adds and whether a short delay smears it"}
```
:::

::: en
## What it lets you finish

Add audible weight and bite to drums, bass or a vocal without running to tape. Send a dry line into a short delay or tape echo to create space and repetition. Change a voice's apparent age or gender, or build a harmony layer, by moving pitch and formants separately. Widen a doubled vocal or guitar with tiny timing and tuning differences. Push drums or bass into distortion to mark the step from verse to chorus. Create movement with filtering, phase and tremolo so a static bed starts to push.

## How it works

This is not one algorithm reskinned. Saturation tools add harmonics through non-linear circuit models, and the harder they are driven the dirtier they get. Delay tools use tape, analogue or digital delay lines, often with filtering in the feedback path. Modulation tools combine short delays and phase offset to create sway. The pitch tool moves pitch and formants independently, so it changes timbre rather than only tuning. What they share is a direct interface and an ear-first design: few controls, each audibly consequential. A tool behaves differently on mono and stereo tracks, and the width processors show it most.

## Limits and traps

- Every plugin requires iLok authorisation, either machine-bound or on a dongle; factor that into machine changes and collaboration.
- Colour is the purpose, not a side effect. When a job needs transparency, this bundle changes the sound before you can decide.
- High delay feedback self-oscillates, so set a ceiling and keep a bypass ready for live use.
- Some tools are sensitive to sample rate; high-frequency distortion can differ between 96 kHz and 48 kHz sessions.
- Updates and plugin formats come through the installer, so confirm a collaborator's version is not older than the one a session was made with.
- There is no standalone version and no hardware reissue; a show travels with the session and the licence, not a rack.

## Alternatives and pairings

For more controlled saturation, FabFilter Saturn 2. For a whole vintage colour palette, Universal Audio's plugin line. If you only need clean delay, ValhallaDelay is simpler. Soundtoys usually sits before Valhalla reverb: make the dirt and the repeats first, then let the reverb catch the tail.

## First three things to learn

Learn input drive against output compensation, then feedback and filtering in the delay, then formants when shifting pitch. Read the site's pages on delay, harmonics and phase alongside it.

```audiolab
{"type":"instrument","gm":"Electric Guitar (clean)","synth":"plucked","phrase":["E3","G3","B3","E4","B3","G3"],"label":"一段干吉他，待加厚","label_en":"A dry guitar line to thicken","hint":"先听拨弦的起音，再想饱和会添哪些谐波、短延迟会不会糊掉它","hint_en":"Hear the pick attack first, then imagine which harmonics saturation adds and whether a short delay smears it"}
```
:::
