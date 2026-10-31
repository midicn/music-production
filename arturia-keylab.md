---
id: arturia-keylab
site: prod
cat: C
order: 39
title: Arturia KeyLab
title_en: Arturia KeyLab
summary: 带旋钮、推子与打击垫的 MIDI 键盘，配软音源好用，手感与真钢琴是两回事。
summary_en: A MIDI keyboard with knobs, faders and pads that works well with software instruments — its feel is not a piano's.
level: standard
tags: [MIDI 键盘, 控制器, 编曲, 软音源]
tags_en: [MIDI keyboard, controller, arranging, software instruments]
alias: [KeyLab, Arturia, 键盘, MIDI 控制器, Analog Lab]
tool_kind: hardware
tool_vendor: Arturia
tool_form: 硬件
tool_platforms: [macOS, Windows]
tool_price: 硬件
tool_jobs: [编曲, 演奏录入, 声音设计]
links:
  - "[[instrument:midi-controller]]"
  - "[[instrument:virtual-instruments]]"
  - "[[glossary:velocity]]"
instances:
  - wikifonia-000225 | 一首慢歌的旋律与和弦，用键盘铺垫最直接，力度层次决定伴奏是否死板
  - giantmidi-003673 | 钢琴独奏曲，用键盘录入时要靠力度与踏板才能接近真实演奏
  - oga-000004 | 游戏配乐的战斗段，合成器声部与鼓垫一起用，正好检验控制器的分工
  - mutopia-000046 | 四声部和声，用键盘弹进 DAW 再分轨，比鼠标点音符快得多
sources:
  - 厂商公开的键盘规格、控制器数量与随附软件说明——依据来自官方页面。
  - MIDI 力度、触后与控制器映射的通识，对照 MIDI 规范整理。
tool_verified: 2026-10-30
updated: 2026-10-30
---

::: zh
## 能替你做完什么

把钢琴、电钢与合成器声部弹进 DAW，不必用鼠标点音符。用旋钮与推子实时抓插件参数，做自动化时手上有感觉。用打击垫打鼓或触发片段，现场也能用。一键切换软音源预设，写歌时不必停下来找音色。用随附的软件音源先做出小样，再决定要不要买更贵的库。用琴键录入弦乐与管乐的旋律，再用控制器画表情。

## 它怎么工作

键盘把按键、力度、触后与控制器变化编码成 MIDI 消息，经 USB 送进电脑，本身不发声。旋钮与推子可以映射到任意插件参数，映射关系存在控制软件里，也可以跟着工程走。打击垫发送音符或控制变化，部分型号还能输出电压信号去控制模块合成器。与主流 DAW 的集成靠脚本，走的是通用的控制协议，不是深度定制。这些脚本由厂商维护，系统升级后要跟着更新。

## 哪里会坑你

- 手感是半配重，弹钢琴声部时和真琴差得远，快速重复音与踏板细节会露馅。
- 触后与部分控制只在高端型号上有，买之前确认，别按图片猜。
- DAW 集成只覆盖主流几家，冷门宿主只能退回通用映射。
- 经集线器连接时偶发断连，录音中途掉线会留下半截音符。
- 随附软件要注册与授权，换电脑时要重新激活。
- 它不是音频接口，也不解决延迟；监听延迟仍取决于声卡与缓冲。
- 八十八键版本仍然不是击弦机，练琴不能靠它。

## 换成什么

预算更低，Novation Launchkey 与 Akai MPK 系列都能完成同样的活；要更深度的宿主集成，Native Instruments 的键盘与自家软件配合更紧。搭配一台稳定接口与一块表情踏板，演奏表情会立刻好听一截。

## 先学三件事

先学三件事：MIDI 通道与映射、力度曲线、DAW 的集成脚本。再练一次用推子写自动化，手感不对就先改曲线。配合读 MIDI 控制器、软音源、力度三条。

```audiolab
{"type":"instrument","gm":"Electric Piano 1","synth":"struck","phrase":["F3","A3","C4","E4","C4","A3","F3"],"label":"键盘弹出的电钢和弦","label_en":"An electric piano chord played on keys","hint":"听力度变化带来的明暗，键盘的力度曲线决定它好不好弹","hint_en":"Listen to how velocity changes the tone; the keybed's velocity curve decides how playable it feels"}
```
:::

::: en
## What it finishes for you

Play piano, electric piano and synth parts into the DAW instead of clicking notes. Grab plug-in parameters with knobs and faders so automation has a feel under the hand. Hit pads for drums or clip triggering, live as well as in the studio. Switch software presets in one move and keep writing instead of hunting for a sound. Sketch with the bundled instruments before deciding whether to buy a bigger library.

## How it works

The keyboard encodes keys, velocity, aftertouch and control changes as MIDI over USB and makes no sound itself. Knobs and faders map to any plug-in parameter, with the mapping stored in the control software or carried by the project. Pads send notes or control changes, and some models output control voltage for modular gear. Integration with major DAWs runs on scripts over common control protocols rather than deep custom code.

## Where it bites

- The action is semi-weighted. Piano parts expose the gap, especially fast repeated notes and pedal detail.
- Aftertouch and some controls appear only on the higher models; confirm before buying from a photo.
- DAW integration covers the mainstream few. An unusual host falls back to generic mapping.
- Connections through a hub occasionally drop, and a dropout mid-take leaves half a phrase.
- The pads feel shallow next to a dedicated drum controller, so finger drumming has a ceiling.
- The bundled software needs registration and reactivation when you change computers.
- It is not an audio interface and does not solve latency; monitoring still depends on the interface and buffer. The 88-key version is still not a hammer action and is no practice piano.

## What to swap in

On a smaller budget the Novation Launchkey and Akai MPK ranges do the same work; for deeper host integration, Native Instruments keyboards pair more tightly with their own software. A stable interface and an expression pedal make performance feel better immediately.

## First three things

Learn MIDI channels and mapping, the velocity curve, and the DAW integration script. Then write one automation pass with a fader. Read the MIDI controller, software instruments and velocity entries alongside this one.

```audiolab
{"type":"instrument","gm":"Electric Piano 1","synth":"struck","phrase":["F3","A3","C4","E4","C4","A3","F3"],"label":"键盘弹出的电钢和弦","label_en":"An electric piano chord played on keys","hint":"听力度变化带来的明暗，键盘的力度曲线决定它好不好弹","hint_en":"Listen to how velocity changes the tone; the keybed's velocity curve decides how playable it feels"}
```
:::
