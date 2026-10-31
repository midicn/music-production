---
id: reason
site: prod
cat: C
order: 9
title: Reason
title_en: Reason
summary: 以机架式虚拟设备与控制电压布线为核心的 DAW，像一间可保存的录音棚。
summary_en: A DAW built on a rack of virtual devices and CV patching, like a studio you can save.
level: standard
tags: [DAW, 机架, 合成器]
tags_en: [DAW, rack, synthesizer]
alias: [Reason, Reason Studios, 理由, 机架宿主]
links:
  - "[[glossary:daw]]"
  - "[[instrument:sequencer]]"
  - "[[glossary:sound-design]]"
instances:
  - groove-000002 | 86 BPM 的灵魂乐鼓循环，适合对照鼓机编程与摆动；这是该工具常见产出的参照，不是该工具的演示
  - groove-000839 | 75 BPM 的嘻哈律动，用来对照步进鼓格与低频处理；这是该工具常见产出的参照，不是该工具的演示
  - oga-000017 | 一分半的弹跳风格游戏配乐，可对照合成器音色与段落切换；这是该工具常见产出的参照，不是该工具的演示
  - groove-000000 | 半分钟的放克鼓循环，用来对照机架里的鼓组与效果链；这是该工具常见产出的参照，不是该工具的演示
sources:
  - 厂商公开的产品说明、平台与授权方式，对照2026-10 复核整理。
  - 机架、组合器与控制电压的功能范围（官方文档）。
  - 插件格式与工程交换的限制，参考DAW 文档。
updated: 2026-10-30
tool_kind: daw
tool_vendor: Reason Studios
tool_form: 桌面应用
tool_platforms: [Windows, macOS]
tool_price: 买断
tool_jobs: [编曲, 声音设计, 混音]
tool_verified: 2026-10-30
---

::: zh
## 适用工作

在机架里搭一套鼓机、贝斯与合成器，做完整伴奏。用鼓机设备编程鼓组，用合成器做音色，用组合器把整套设置存成一个预设。用控制电压布线做非常规调制，得到硬件式的随机与联动。混音并导出成品或分轨，把整套设备以插件形式放进别的宿主里使用。给一段说唱或电子曲做 beat，保留可改的鼓组与贝斯。用同一套组合器预设做现场演出，切换场景不必重建；把一整套机架存成模板，下一首只换鼓组与和弦。

## 原理

机架视图模拟硬件：设备上下堆叠，音频与控制信号走线，翻到背面接线。组合器把多个设备包成一个可保存的整体，旋钮可以映射到任意参数。控制电压是调制信号，能让一个设备的包络去推另一个设备的音高或滤波。自带混音台。整套设备可以作为插件运行在别的 DAW 里。鼓机可以按步进或实时录制。设备面板上的旋钮都能被组合器的宏接管，现场只动几个大旋钮。关键词是机架、控制电压、组合器、鼓机。

## 边界

- 音频编辑与 comping 深度不如 Pro Tools、Cubase，录整支乐队不是强项。
- 没有记谱、视频配乐与 AAF，影视流程要换工具。
- 插件生态以自家格式为主，换宿主后只有插件形式能带走设备。
- 机架隐喻对新手不直观，控制电压要先懂调制才用得上。
- 授权有永久与订阅两条线，升级策略要先看清。
- 自带音源偏电子，管弦与真实乐器要另配采样库。
- 机架设备越堆越多时，工程会变得难读，命名与分组要一开始就做。
- 采样与音色引用外部库时，归档要把库一起带上。

## 替代

要更大生态的电子制作，Ableton Live 或 FL Studio 更常见；要传统录音混音，Studio One 或 Pro Tools 更顺；要模块化，Bitwig 更彻底。搭配 MIDI 控制器、外部硬件与插件宿主；控制电压接硬件需要专门的接口。

## 上手

先学三件事：机架与走线、鼓机的图案编程、组合器与控制电压。配合「减法合成」「采样器的结构」「参数自动化」读。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s","bpm":96,"label":"96 BPM 的十六步鼓格","label_en":"A sixteen-step drum grid at 96 BPM","hint":"先听每一格的位置，再想哪一步挪动会让律动变懒","hint_en":"Hear where each step sits, then imagine moving one to loosen the groove"}
```
:::

::: en
## Jobs it covers

Build a drum machine, bass and synths in a rack and finish a whole backing track. Program drums on the drum devices, shape sounds on the synths, and store the whole setup as one Combinator preset. Patch control voltage for unconventional modulation and hardware-style randomness and linkage. Mix and export a master or stems, and run the entire rack as a plug-in inside another host. Produce a beat for a rap or electronic track and keep the drums and bass editable. Perform live with the same Combinator presets, switching scenes without rebuilding.

## How it works

The rack view imitates hardware: devices stack vertically, audio and control signals run between them, and the back panel is where you patch. A Combinator wraps several devices into one savable whole, with knobs mapped to any parameter. Control voltage is a modulation signal, so one device's envelope can push another device's pitch or filter. A mixer is built in. The rack can run as a plug-in inside another DAW. Drum devices take step input or real-time recording. Vocabulary: rack, CV, Combinator, drum machine.

## Limits

- Audio editing and comping are less deep than in Pro Tools or Cubase; tracking a full band is not the strength.
- There is no notation, video scoring or AAF, so film work means another tool.
- The plug-in ecosystem is centred on the company's own format, and moving hosts only carries devices in plug-in form.
- The rack metaphor is not obvious to beginners, and CV only makes sense once modulation does.
- Licensing comes in perpetual and subscription lines, so read the upgrade policy before committing.
- Built-in sounds lean electronic; orchestras and real instruments need outside libraries.
- As devices pile up, sessions become hard to read, so name and group from the start.

## Alternatives

For electronic production with a larger ecosystem, Ableton Live and FL Studio are more common. For traditional recording and mixing, Studio One or Pro Tools is smoother. For modular depth, Bitwig goes further. Pair Reason with a MIDI controller, outboard gear and a plug-in host; CV to hardware needs a dedicated interface.

## First three things

Learn three things first: the rack and its cabling, pattern programming on the drum devices, and the Combinator with CV. Read the entries on subtractive synthesis, sampler architecture and parameter automation.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s","bpm":96,"label":"A sixteen-step drum grid at 96 BPM","label_en":"A sixteen-step drum grid at 96 BPM","hint":"Hear where each step sits, then imagine moving one to loosen the groove","hint_en":"Hear where each step sits, then imagine moving one to loosen the groove"}
```
:::
