---
id: synth-patch-documentation
site: prod
cat: B3
title: 音色存档
title_en: Documenting a Patch
summary: 音色要能被别人原样调回来，参数、版本与依赖缺一不可。
summary_en: A patch is archived only when someone else can recall it exactly; parameters, versions and dependencies have to travel with it.
level: standard
tags: [音色设计, 预设, 版本, 归档, 复现]
tags_en: [sound design, presets, versions, archiving, recall]
alias: [音色存档, 预设管理, 音色归档, patch documentation, preset recall]
order: 412
links:
  - "[[glossary:synthesizer]]"
  - "[[instrument:prophet-5]]"
  - "[[instrument:software-synth]]"
  - "[[glossary:midi-protocol]]"
instances:
  - oga-000329 | 合成铜管的调制轮事件写了数百条，不记下路由与深度就无法复原（C1）
  - oga-000270 | 多条通道各自写入混响与合唱深度，存档要连控制器一起去（C1）
  - oga-000327 | 弯音事件密集，音高作为调制目标被反复推动，重开工程容易失真（C1）
  - oga-000163 | 锯齿主音与铺底共用音色家族，适合练习按层记录参数（C1）
sources:
  - Sequential Circuits，Prophet-5 用户手册（厂商文档）— 预设保存与调用
  - MIDI Association，MIDI 1.0 Detailed Specification — 控制器与音色消息
  - Gordon Reid，Sound On Sound Synth Secrets — 参数与调制路由
updated: 2026-10-31
---

::: zh
三个月后打开旧工程，同一个预设听起来不一样：插件升级了，波表换了版本，采样路径断了。音色存档要解决的不是记下来，而是换一台机器也能调回来。

## 存档要存五样

| 项目 | 记什么 | 为什么 | 怎么记 |
|---|---|---|---|
| 参数 | 振荡器、滤波器、包络、效果 | 决定音色骨架 | 预设文件加参数表 |
| 调制 | 源、目标、深度、曲线 | 决定运动与手感 | 调制矩阵截图或表格 |
| 依赖 | 波表、采样、第三方预设 | 缺一个音色就变 | 文件名加版本与校验值 |
| 环境 | 插件版本、固件、DAW | 升级会改算法 | 写进预设说明 |
| 试听 | 固定 MIDI 与渲染片段 | 用耳朵验收 | 与预设放同一目录 |

## 三种粒度

最小粒度是预设文件，只保证参数一致；中等粒度是工程快照，连同 MIDI、自动化与效果链一起存；最大粒度是文字说明，写清设计意图、可替换部件与已知问题。演出与协作至少要做到中等粒度，因为自动化往往写在工程里，不在预设里。

## 命名与版本

文件名用音色名加版本加日期，版本从一点零开始：改听感升大版本，微调参数升小版本。每次保存附一行说明，写清改了什么、为什么改。别用 final、new、good 这类词，三个月后没人分得清。

## 复现失败先查什么

先确认插件与固件版本，再确认波表与采样的文件名和校验值，然后查全局设置：复音数、滑音、基准音高、效果发送。工程里的自动化最容易漏，尤其是控制器编号被重新映射过。跨机器时还要看采样率，部分振荡器的抗混叠与采样率相关，换到另一个采样率音色会变。

```audiolab
{"type":"instrument","gm":"Pad 2 (warm)","synth":"bowed","phrase":["C4","E4","G4","B4"],"label":"调回来之后，用同一句验收","label_en":"The same phrase after a recall","hint":"存档前后各播一次这个和弦；先听音头，再听两秒后的亮度，任何一处不同都说明参数没存全。","hint_en":"Play this chord before and after the recall; check the attack first, then the brightness two seconds in. Any difference means something was not saved."}
```
:::

::: en

Open a project three months later and the same patch sounds wrong: the plugin has been updated, the wavetable is a different revision, the sample path is broken. Documentation is not about writing things down; it is about recalling the sound on another machine.

## Five things travel with a patch

| Item | What to record | Why it matters | How to keep it |
|---|---|---|---|
| Parameters | Oscillators, filter, envelopes, effects | They are the skeleton of the sound | Preset file plus a parameter sheet |
| Modulation | Source, target, depth, curve | It sets movement and feel | Matrix screenshot or table |
| Dependencies | Wavetables, samples, third-party presets | One missing file changes everything | Names with version and checksum |
| Environment | Plugin build, firmware, DAW | Updates alter algorithms | Note it in the preset description |
| Audio | Fixed MIDI and a render | The ear is the final check | Same folder as the preset |

## Three levels of detail

The smallest unit is the preset file, which only guarantees parameter values. The middle level is a project snapshot, carrying MIDI, automation and the effect chain. The largest is a written note covering intent, replaceable parts and known issues. For sessions and collaboration, aim for the middle level at least, because automation often lives in the project rather than the preset.

## Naming and versions

Name files with patch, version and date, starting at one point zero: a change in character raises the major number, a parameter nudge raises the minor. Add one line with each save saying what changed and why. Avoid final, new or good; three months on, nobody can tell them apart.

## When a recall fails

Check plugin and firmware builds first, then the names and checksums of wavetables and samples, then global settings: polyphony, glide, tuning, effect sends. Automation is the usual omission, especially when controller numbers were remapped. Across machines, check the sample rate too: some oscillators change their anti-aliasing with the rate, and the timbre follows.

```audiolab
{"type":"instrument","gm":"Pad 2 (warm)","synth":"bowed","phrase":["C4","E4","G4","B4"],"label":"The same phrase after a recall","label_en":"The same phrase after a recall","hint":"Play this chord before and after the recall; check the attack first, then the brightness two seconds in. Any difference means something was not saved.","hint_en":"Play this chord before and after the recall; check the attack first, then the brightness two seconds in. Any difference means something was not saved."}
```
:::
