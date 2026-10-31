---
id: fabfilter-pro-q
site: prod
cat: C
order: 11
title: Pro-Q（动态均衡）
title_en: Pro-Q (Dynamic EQ)
summary: 频段能跟着电平自己动，修共振与压齿音各走一步。
summary_en: Bands that move with level, so a resonance or a sibilant can be tamed without a second processor.
level: standard
tags: [插件, 均衡, 动态均衡, 混音]
tags_en: [plugin, EQ, dynamic EQ, mixing]
alias: [Pro-Q, FabFilter Pro-Q, 动态均衡, dynamic EQ, 均衡插件]
tool_kind: plugin
tool_vendor: FabFilter
tool_form: 插件
tool_platforms: [macOS, Windows]
tool_price: 买断
tool_jobs: [混音, 母带, 声音设计]
tool_verified: 2026-10-30
links:
  - "[[glossary:dynamic-eq]]"
  - "[[glossary:eq]]"
  - "[[glossary:sidechain]]"
instances:
  - atepp-001124 | 肖邦《第一叙事曲》的钢琴，低音区厚、高音区亮，适合练分段衰减与窄带处理（C1）
  - musicnet-000067 | 贝多芬第十五弦乐四重奏，四件乐器挤在中频，窄带动作很容易听出（C1）
  - cyberhymnal-000003 | 赞美诗《Child Divine》，长音和声稳定，适合分辨静态衰减与动态段（C1）
sources:
  - FabFilter 官方产品页的频段、动态处理与相位模式说明，参考公开资料。
  - 参量均衡与动态均衡的常见用法；混音惯例是主要依据。
updated: 2026-10-30
---

::: zh
## 能替你做完什么

把录好的钢琴、弦乐或人声里固定的共振削掉，不必重录。给某件乐器开一条窄带，让它在副歌里露出来，而不整体提亮。把现场录音里空调与低频轰鸣的一段单独收掉，句子其余部分不动。压住只在强奏时出现的低频堆积或齿音，弱奏时保持原样。在总线上分中、侧处理，修单声道兼容问题。母带前做最后一遍清理，低频、浑浊、刺耳各归一段。

## 它怎么工作

每个频段是一个参量滤波器，中心频率、增益、Q 与斜率独立可调。频段还能挂上动态检测：信号超过阈值时按设定的范围增减，等于把压缩动作限制在一条窄带上。频谱抓取把鼠标停在频谱上就能落一个段，省去猜频率。最小相位模式延迟低，线性相位模式保住相位关系但要付出前摇延迟。中侧模式让中间与两侧分开处理，代价是单声道回放时要再核对一次。增益补偿可以按段或整体生效，A/B 时先对齐响度再判断。

## 哪里会坑你

- 动态段不是压缩器。范围开得太大，弱奏和强奏会像两套 EQ，音色在句子里忽明忽暗。
- 线性相位模式的前摇延迟在录音和现场不能用；零延迟模式在低频仍有相位偏移。
- 段数多、每段都开动态时 CPU 明显上升，几十个实例的工程会先卡在它这里。
- 中侧处理会把两侧的噪声也分开，宽度感可能变假，单声道回放要再核一次。
- 它是插件，没有硬件版。工程交给别人前要确认对方装了同一插件，否则只能导出音频或交截图。
- 频谱显示的时间窗短，低频分辨率有限，看图形不能代替听。

## 换成什么

TDR Nova 也有动态段，免费档就能做窄带控制；需要更多段数与相位模式时看 DMG Equilibrium；通道条式的用法可看 iZotope Neutron。它常与 Pro-C 串联：先用动态段修共振，再用压缩器管整体电平。

## 先学三件事

先学 Q 与增益的配合，再学动态段的阈值与范围，最后学增益补偿与 A/B。配合「均衡器的三种形态」「动态均衡」「侧链」三篇读。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C3","G3","C4","E4","G4"],"label":"待分段的钢琴和弦","label_en":"A piano chord to divide into bands","hint":"先听低音区的堆积，再想哪一段该用动态、哪一段只需静态衰减","hint_en":"Hear the low-mid build-up first, then decide which band needs dynamics and which needs a static cut"}
```
:::

::: en
## What it finishes for you

Remove a fixed resonance from a recorded piano, string section or voice without another take. Lift one instrument with a narrow band so it reads in the chorus without brightening the whole mix. Remove air-conditioning rumble from one stretch of a location take and leave the rest alone. Hold a low-mid build-up or a sibilant that appears only on loud notes, leaving quiet phrases untouched. Correct mono compatibility by treating mid and side separately on a bus. Do a last pass before mastering, with low end, mud and harshness each on its own band.

## How it works

Each band is a parametric filter with independent frequency, gain, Q and slope. A band can also carry a dynamics detector: when the signal crosses a threshold, gain moves within a set range, which confines the action to one narrow region. Spectrum grab places a band where you point, so you stop guessing at frequencies. Minimum-phase mode keeps latency low; linear-phase mode preserves phase relationships at the cost of pre-ring and added delay. Mid/side mode processes the centre and the sides separately, at the price of a mono check afterwards. Gain compensation works per band or across the curve, so match loudness before an A/B.

## Where it bites

- A dynamic band is not a compressor. With a wide range, quiet and loud phrases sound like two different EQs, and the timbre breathes within a line.
- Linear-phase mode adds latency that rules it out for tracking and live use; zero-latency mode still shifts phase at low frequencies.
- Many bands with dynamics enabled raise CPU noticeably; a session with dozens of instances will choke here first.
- It is a plugin with no hardware counterpart; before handing a session over, confirm the other studio owns it or print audio.
- The spectrum display uses a short window and resolves lows poorly; the graph does not replace listening.

## What to swap in

TDR Nova also offers dynamic bands and covers narrow control in its free tier. DMG Equilibrium suits projects that need more bands and flexible phase modes. iZotope Neutron is the channel-strip route. Pro-Q usually runs into Pro-C: the dynamic bands fix resonances, then the compressor handles overall level.

## First three things

Learn Q against gain, then a dynamic band's threshold and range, then gain compensation and A/B. Read the pages on EQ shapes, dynamic EQ and sidechain alongside it.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C3","G3","C4","E4","G4"],"label":"待分段的钢琴和弦","label_en":"A piano chord to divide into bands","hint":"先听低音区的堆积，再想哪一段该用动态、哪一段只需静态衰减","hint_en":"Hear the low-mid build-up first, then decide which band needs dynamics and which needs a static cut"}
```
:::
