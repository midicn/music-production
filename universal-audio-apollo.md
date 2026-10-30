---
id: universal-audio-apollo
site: prod
cat: C
order: 32
title: Universal Audio Apollo
title_en: Universal Audio Apollo
summary: 带板载 DSP 的接口，卖点是录音时就能用建模前级与插件，代价是生态绑定。
summary_en: An interface with on-board DSP, sold on modelled preamps and plugins while tracking — the price is ecosystem lock-in.
level: standard
tags: [音频接口, DSP, 建模, 录音]
tags_en: [audio interface, DSP, modelling, recording]
alias: [Apollo, UAD, 阿波罗, Unison, 建模话放]
tool_kind: hardware
tool_vendor: Universal Audio
tool_form: 硬件
tool_platforms: [macOS, Windows]
tool_price: 硬件
tool_jobs: [录音, 混音, 声音设计]
links:
  - "[[glossary:preamp]]"
  - "[[glossary:amp-simulator]]"
  - "[[glossary:plugin]]"
instances:
  - groove-000005 | 八十七拍的嘻哈鼓组，边录边压能少一轮返工，正好检验 DSP 够不够用；这是该工具常见产出的参照，不是该工具的演示
  - wikifonia-000323 | 爵士标准曲的旋律，吉他或键盘直接进接口走箱体建模，省掉摆麦；这是该工具常见产出的参照，不是该工具的演示
  - openscore-000002 | 人声加钢琴的短歌，歌手需要听到带混响的返听才敢放声；这是该工具常见产出的参照，不是该工具的演示
sources:
  - 厂商公开的前置建模、DSP 与插件授权说明，按官方页面核对，未抄文本
  - 录音监听延迟与插件运算的关系，按数字音频通识核对
tool_verified: 2026-10-30
updated: 2026-10-30
---

::: zh
## 它能完成什么

录主唱时就把压缩与混响送进监听，歌手听到的是接近成品的声音。用前置建模把一支普通动圈录出厚度，不必再接一台硬件话放。吉他直接进接口走箱体与话筒建模，省掉摆麦和试位。把鼓组先压住再录，减少后期返工。把插件运算放在板载芯片上跑，电脑处理器还能留给别的活。

## 它怎么工作

板载 DSP 让插件在接口内部运算，信号进电脑之前就已经处理过，所以监听几乎没有延迟。前置建模不只是加一段均衡：它改变输入阻抗与增益结构，让话筒看到的前级特性跟着变，这也是它和普通插件区别最大的地方。配套的控制软件负责返听混音与插件加载，授权绑定在硬件上，换机要重新登记。

## 边界与坑

- 买接口等于买插件库：DSP 插件跟着硬件走，转手与换机都要处理授权。
- 算力有限，几个重型插件就能吃满一块芯片，通道一多只能取舍。
- 前置建模只对自家前置有效，接外部话放时这一段用不上。
- 原生版与 DSP 版授权分开，订阅与买断也不是一回事，下单前看清。
- 不同型号的电脑接口与系统支持不一样，老机型在新系统上可能停止更新。
- 建模是别人的耳朵做的决定，不合适时你只能换一个模型，改不了它的骨架。
- 接口本身不差，只是你付的钱有一半在软件上，算预算时别只比通道数。

## 替代与搭配

不需要建模，干净接口加原生插件更便宜也更快；要极稳的驱动与路由，RME 更省心；偏爱硬件染色，外接话放更直接。搭配外部时钟与数字扩展可以补通道数，但建模仍只在前几路上生效。

## 上手路径

先学三件事：返听混音、前置建模的增益结构、DSP 余量核算。再决定哪些插件必须实时、哪些留到混音。别一次装十个插件试音，先固定一条链再换。配合读话放、箱体建模、插件三条。

```audiolab
{"type":"instrument","gm":"Electric Guitar (clean)","synth":"plucked","phrase":["E2","B2","E3","G#3","B3","G#3","E3","B2"],"label":"直接进接口的吉他","label_en":"A guitar straight into the interface","hint":"听干净音色里的动态，建模前级要能接住拨弦的瞬态","hint_en":"Listen to the dynamics of a clean guitar; a modelled preamp has to catch the pick attack"}
```
:::

::: en
## What it lets you finish

Put compression and reverb in the singer's cue while tracking, so they hear something close to the finished record. Give an ordinary dynamic microphone weight through preamp modelling without buying a hardware preamp. Plug a guitar straight in and use cabinet and microphone models instead of placing a mic. Compress the kit on the way in and save a pass later. Offload plug-in work to the on-board chips and leave the computer's processor for something else.

## How it works

The DSP chips run plug-ins inside the interface, before the signal reaches the computer, which is why monitoring feels almost immediate. Preamp modelling is more than an EQ curve: it changes input impedance and gain structure so the microphone sees a different front end. That is the part ordinary plug-ins cannot copy. The companion console software handles cue mixes and plug-in loading, and licences live with the hardware, so moving to another unit means re-registering.

## Limits and traps

- Buying the interface means buying into a plug-in library. DSP licences follow the box, and resale or replacement has paperwork.
- The chips are finite. A few heavy plug-ins can fill one, so a big session forces choices.
- Preamp modelling only applies to the built-in inputs. With an external preamp that section is dead weight.
- Native and DSP licences are separate, and subscription is not the same as purchase. Read before ordering.
- Computer connectivity and OS support differ by model; older units may stop receiving updates.
- The models are somebody else's taste. If one does not suit the source, you can swap models but not the underlying character.

## Alternatives and pairings

If you do not need modelling, a clean interface plus native plug-ins is cheaper and faster. For bulletproof drivers and routing, RME is calmer; for hardware colour, an external preamp is more direct. Add a clock and digital expansion for more channels, remembering that modelling only covers the first few inputs.

## First three things to learn

Learn the cue mix, the gain structure of preamp modelling, and how to budget DSP. Then decide which plug-ins must run live and which can wait for the mix. Read the preamp, amp simulator and plug-in entries alongside this one.

```audiolab
{"type":"instrument","gm":"Electric Guitar (clean)","synth":"plucked","phrase":["E2","B2","E3","G#3","B3","G#3","E3","B2"],"label":"直接进接口的吉他","label_en":"A guitar straight into the interface","hint":"听干净音色里的动态，建模前级要能接住拨弦的瞬态","hint_en":"Listen to the dynamics of a clean guitar; a modelled preamp has to catch the pick attack"}
```
:::
