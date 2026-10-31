---
id: adobe-audition
site: prod
cat: C
order: 46
title: Audition（播客与对白后期）
title_en: Audition
summary: 以波形与频谱为核心的后期工具，擅长播客、对白清理与老录音修复。
summary_en: A waveform and spectrogram editor for podcast post, dialogue cleanup and restoration rather than music production.
level: standard
tags: [后期, 播客, 对白, 修复]
tags_en: [post-production, podcast, dialogue, restoration]
alias: [Audition, Adobe Audition, 播客后期, 对白修复]
links:
  - "[[glossary:de-esser]]"
  - "[[glossary:noise-floor]]"
  - "[[glossary:signal-to-noise]]"
instances:
  - atepp-001111 | 早期钢琴录音的转制，嘶声与踏板噪声分层出现，是修复类交付的参照
  - cyberhymnal-000003 | 管风琴赞美诗，长音里的本底噪声与机械声最难藏，是降噪判断的参照
  - mutopia-000001 | 人声与钢琴同录，气口、齿音与房间声都在，是口播清理的参照
  - openscore-000005 | 人声随钢琴起伏，动态范围大，可对照压缩与限幅的取舍，是动态处理的参照
sources:
  - Audition 的波形、频谱显示与 Match Loudness（Adobe 公开文档）。
  - 播客与对白的降噪、去齿音与响度做法，参考后期制作惯例。
tool_kind: plugin
tool_vendor: Adobe
tool_form: 桌面应用
tool_platforms: [macOS, Windows]
tool_price: 订阅
tool_jobs: [播客, 对白后期, 修复, 音频编辑]
tool_verified: 2026-10-30
updated: 2026-10-30
---

::: zh
Audition 的定位很清楚：它不管编曲，只管把已经录下来的声音修干净、对齐、送到能发布的程度。播客、采访、有声书与视频对白是它的主场。

## 能替你做完什么

把一段四十分钟的双人对谈修到可发布，响度对齐平台要求。去掉空调嗡声、键盘敲击与椅子吱呀，同时保住说话的瞬态。把采访里的口水音与过长停顿修顺，剪掉口误而不留接缝。给视频做对白替换与音效铺底，再按场景导出。批量把三十条口播统一响度并导出 MP3。

## 它怎么工作

波形编辑器处理单条素材，频谱显示让噪声、嗡声与齿音变成看得见的块，可以按频率选区修。多轨会话分对白、音乐与音效，总线加压缩与限幅。Essential Sound 按素材类型套一组预设，Match Loudness 按 ITU-R BS.1770 测量并统一响度。与 Premiere 用 Dynamic Link 往返，省掉中间文件。

## 哪里会坑你

- 没有虚拟乐器与像样的 MIDI 编辑，做不了编曲，也接不了软音源。
- 订阅制，停订就失去工具；旧工程要先导出分轨与成品，别只留会话文件。
- 与 Pro Tools 或 Nuendo 交换通常只能给分轨，插件与自动化不随工程走。
- 频谱修复过度会留下金属味与水声，原声的瞬态也会被削。
- 长文件的一次性处理很吃 CPU，处理前先备份原始素材。
- 路由与侧链弱于 DAW，复杂的音乐混音仍要回宿主。

## 换成什么

iZotope RX 在频谱修复上更深，常与 Audition 分工：RX 修单点，Audition 做响度与交付。Reaper 能兼顾后期与音乐，适合不想订阅的人。Pro Tools 则是影视后期的交换标准。与 DAW 的分工是：Audition 修素材与对白，音乐与混音回 DAW 做。

## 先学三件事

先学频谱显示与降噪、Match Loudness、多轨会话的总线。读这里的音频修复、播客片头、响度标准与真峰值，用一段带空调噪声的对白走完修复到导出。

```audiolab
{"type":"instrument","gm":"Voice Oohs","synth":"vocal","phrase":["C4","D4","E4","G4"],"label":"一段要被修干净的人声","label_en":"A voice that has to be cleaned","hint":"先听气口与尾音，再想降噪会先吃掉哪一段","hint_en":"Hear the breath and the tail, then decide what noise reduction would eat first"}
```
:::

::: en
Audition is clear about its job. It does not arrange music; it takes sound that has already been recorded and makes it clean, aligned and ready to publish. Podcasts, interviews, audiobooks and video dialogue are its home ground.

## What it finishes for you

Clean a forty-minute two-person interview until it is publishable, with loudness matched to the platform. Remove air-conditioning hum, keyboard clicks and chair creaks while keeping speech transients. Smooth mouth noise and long pauses, and cut fluffs without audible seams. Replace dialogue and lay sound effects under picture, then export per scene. Batch thirty voice spots to one loudness target and export MP3.

## How it works

The waveform editor handles one asset at a time, and the spectral display turns noise, hum and sibilance into visible blocks that can be selected by frequency. A multitrack session separates dialogue, music and effects, with compression and limiting on the bus. Essential Sound applies a set of presets by material type, and Match Loudness measures and aligns levels to ITU-R BS.1770. Dynamic Link with Premiere Pro removes intermediate files.

## Where it bites

- There are no virtual instruments and no serious MIDI editing, so it cannot arrange or host a soft synth.
- It is subscription software. Stop paying and the tool is gone, so export stems and masters rather than keeping only session files.
- Exchanges with Pro Tools or Nuendo usually mean stems; plug-ins and automation do not travel with the session.
- Overused spectral repair leaves a metallic or watery residue and shaves the original transients.
- One-pass processing of long files is CPU-heavy; back up the original media first.
- Routing and sidechaining are weaker than in a DAW, so complex music mixing still returns to a host.

## What to swap in

iZotope RX goes deeper on spectral repair and often splits the work with Audition: RX fixes single events, Audition handles loudness and delivery. Reaper covers post and music for people who avoid subscriptions, and Pro Tools is the exchange standard in picture post. The split with a DAW is simple: Audition cleans assets and dialogue, the DAW makes the music and the mix.

## First three things

The spectral display and noise reduction, Match Loudness, and bus structure in a multitrack session. Then read Audio Restoration, A Podcast Intro, and Loudness Standards and True Peak, and take one dialogue clip with air-conditioning noise from repair to export.

```audiolab
{"type":"instrument","gm":"Voice Oohs","synth":"vocal","phrase":["C4","D4","E4","G4"],"label":"A voice that has to be cleaned","label_en":"A voice that has to be cleaned","hint":"Hear the breath and the tail, then decide what noise reduction would eat first","hint_en":"Hear the breath and the tail, then decide what noise reduction would eat first"}
```
:::
