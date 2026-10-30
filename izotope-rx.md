---
id: izotope-rx
site: prod
cat: C
order: 16
title: RX（修复）
title_en: RX (Restoration)
summary: 频谱里直接改，噪声、嗡声与咔嗒各有对应工具。
summary_en: Edit inside the spectrogram, with a dedicated tool for noise, hum and clicks.
level: standard
tags: [插件, 修复, 降噪, 频谱编辑]
tags_en: [plugin, restoration, noise reduction, spectral editing]
alias: [RX, iZotope RX, 音频修复, spectral repair, 降噪插件]
tool_kind: plugin
tool_vendor: iZotope
tool_form: 插件
tool_platforms: [macOS, Windows]
tool_price: 买断
tool_jobs: [修复, 影视配乐, 母带]
tool_verified: 2026-10-30
links:
  - "[[glossary:noise-floor]]"
  - "[[glossary:transient-shaper]]"
  - "[[glossary:phase]]"
instances:
  - thesession-022200 | 爱尔兰传统曲调独奏，弓弦摩擦贴近音乐本体，降噪过度会先伤到它（C1，参照不是该插件的演示）
  - mutopia-000001 | 十九世纪声乐小品，人声与钢琴同谱，适合练分离与保留演奏细节（C1，参照不是该插件的演示）
  - essen-000009 | 《茶田山歌》，田野采集的民歌，人声与环境同处，修复要先决定保留多少现场（C1，参照不是该插件的演示）
sources:
  - iZotope 官方产品页的模块与独立应用说明，依公开资料核对，未抄原文
  - 谱减降噪、去嗡与去咔嗒的常见做法，依修复通识核对，未抄文本
updated: 2026-10-30
---

::: zh
## 它能完成什么

把一段对白从空调噪声与交通声里拉出来，做到可发布的清晰度。去掉 50 或 60 Hz 的电源嗡声及其谐波，同时保留低音乐器。修掉黑胶与磁带转录音源里的咔嗒、爆点与短暂 dropout。把现场音乐里的手机铃声与咳嗽从频谱上挖掉。压低现场录音的房间混响，让对白更靠近。批量处理一集播客或一张专辑，统一响度与噪声底。

## 它怎么工作

大部分模块在频域工作：把信号切成短时频谱，估计噪声或目标事件的形态，再从原信号里减去或插值。频谱编辑允许直接框选一块时间与频率，让工具根据两侧内容重建，适合处理一声咳嗽或一段鸣笛。去嗡用一组窄带陷波跟踪基频与谐波；去咔嗒检测瞬态并短窗填补；去混响估计尾音并衰减。修复助手会听一遍素材，给出模块顺序建议，但仍要逐段试听。它按素材类型给建议，音乐与对白不要共用一套参数。

## 边界与坑

- 所有修复都是信息交换。降噪越狠，齿音与弓弦摩擦越先变成水声与金属味。
- 频谱修复会抹平瞬态，鼓点与辅音上要改用短窗，不能整段框选。
- 部分模块不是实时处理，长文件要占大量内存；工程里挂多个实例会拖慢回放。
- 它救不了错误的拾音。话筒太远、房间太响的素材，修完仍然像隔着布。
- 批量处理前先在一条素材上定参数，整批套用会放大误判。
- 独立应用与插件是两套工作流，版本与授权要一致，交接时要说明对方需要哪一版。

## 替代与搭配

Steinberg SpectraLayers 的频谱编辑更自由；Acon Digital Restoration Suite 更轻量；电影对白修复常配合 Cedar 这类专用工具。它常与 Ozone 串联：RX 修素材，Ozone 做母带。

## 上手路径

先学噪声采样与降噪量的临界点，再学频谱修复的选区，最后学去嗡与去咔嗒的顺序。配合本站「音频修复」「本底噪声」「瞬态」三篇读。

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["G4","A4","B4","D5","B4","A4","G4"],"label":"弓弦与噪声的边界","label_en":"Where bow meets noise","hint":"先听弓毛摩擦，再想降噪越过哪一步会把它变成水声","hint_en":"Hear the bow friction first, then find the point where noise reduction turns it watery"}
```
:::

::: en
## What it lets you finish

Pull a dialogue take out of air-conditioning and traffic noise until it is publishable. Remove 50 or 60 Hz mains hum and its harmonics while keeping the bass instruments. Repair clicks, pops and short dropouts from vinyl and tape transfers. Remove a phone ring or a cough from a live music recording in the spectrogram. Reduce room reverb on location recordings so speech sits closer. Batch a podcast episode or an album for consistent noise floor and loudness.

## How it works

Most modules work in the frequency domain: the signal is cut into short-term spectra, the shape of the noise or the target event is estimated, and that estimate is subtracted or interpolated. Spectral editing lets you select a patch of time and frequency and rebuild it from the surrounding material, which suits a cough or a passing horn. De-hum tracks the fundamental and its harmonics with a set of narrow notches; de-click detects transients and fills them with short windows; de-reverb estimates the tail and attenuates it. Repair Assistant listens to the file and proposes a module order, but each section still needs auditioning. Its advice follows the material type, so music and dialogue should not share one set of settings.

## Limits and traps

- Every repair is a trade in information. The harder the noise reduction, the sooner sibilants and bow friction turn watery or metallic.
- Spectral repair smears transients; on drums and consonants use short windows rather than selecting a whole passage.
- Some modules are not real-time, and long files occupy a lot of memory; several instances in a session slow playback.
- It cannot rescue bad capture. Material recorded too far away or in a loud room still sounds like it is behind cloth.
- Set the parameters on one clip before batching, or a wrong estimate is applied to the whole folder.
- The standalone application and the plugins are two workflows; keep versions and licences aligned and tell a collaborator which one the job needs.

## Alternatives and pairings

Steinberg SpectraLayers gives freer spectral editing. Acon Digital Restoration Suite is lighter. Dialogue work for film often pairs with dedicated tools such as Cedar. RX usually runs before Ozone: repair the source, then master.

## First three things to learn

Learn noise sampling and the point where reduction starts to damage, then how to make a spectral selection, then the order of de-hum and de-click. Read the site's pages on audio restoration, noise floor and transients alongside it.

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["G4","A4","B4","D5","B4","A4","G4"],"label":"弓弦与噪声的边界","label_en":"Where bow meets noise","hint":"先听弓毛摩擦，再想降噪越过哪一步会把它变成水声","hint_en":"Hear the bow friction first, then find the point where noise reduction turns it watery"}
```
:::
