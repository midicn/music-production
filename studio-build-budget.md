---
id: studio-build-budget
site: prod
cat: A5
title: 录音棚预算
title_en: Budgeting a Studio Build
summary: 钱先给房间、电与监听，麦克风和插件放到后面，顺序错了很难补。
summary_en: Spend on the room, power and monitoring first; microphones and plugins come later, and that order is hard to reverse.
level: standard
tags: [录音棚, 预算, 声学处理, 隔声, 监听]
tags_en: [studio, budget, acoustic treatment, sound isolation, monitoring]
alias: [录音棚预算, 工作室建造, 装修预算, studio budget, build budget]
order: 398
links:
  - "[[glossary:room-treatment]]"
  - "[[glossary:absorption]]"
  - "[[glossary:nearfield-monitor]]"
  - "[[glossary:monitoring]]"
instances:
  - groove-000001 | 105 BPM 放克鼓组，房间反射多时鼓点会糊成一片，最能显出处理的价值（C1）
  - atepp-000369 | 钢琴独奏余响长，房间做与不做，尾巴的干净程度差别明显（C1）
  - essen-000517 | 单声部民歌，人声干净，适合检查新房间有没有把中频吸空（C1）
  - cyberhymnal-006346 | 持续和弦，低频厚度能验证角落处理是否到位（C1）
sources:
  - Newell, Philip，Recording Studio Design（Focal Press）— 录音棚建造流程与预算分配
  - Everest, F. Alton，Master Handbook of Acoustics（McGraw-Hill）— 隔声、吸声与房间处理
  - Ballou, Glen，Handbook for Sound Engineers（Focal Press）— 录音棚电气与空调噪声
updated: 2026-10-31
---

::: zh
先买一支好麦克风，房间没处理，录出来还是糊的，这笔钱花得最冤。录音棚预算有一条顺序：先解决声音进出的边界，再解决房间内部，最后才是设备。

## 先花的四项

| 顺序 | 项目 | 为什么在前面 | 能省吗 | 后补的代价 |
|---|---|---|---|---|
| 1 | 尺寸与隔声 | 尺寸改不了，漏声吸声补不回 | 不能 | 拆改重来 |
| 2 | 电、接地、空调 | 本底噪声决定录音下限 | 不能 | 返工穿墙 |
| 3 | 声学处理 | 决定监听可不可信 | 不能 | 设备越买越听不准 |
| 4 | 监听与摆位 | 决定所有判断 | 可分批 | 混音翻译差 |

## 隔声与吸声是两笔钱

隔声解决声音传出去和传进来，靠质量、密封与浮筑结构；吸声解决房间内部的反射，靠多孔材料与扩散体。两者常被混为一谈：把吸声棉塞进墙里，隔声几乎不增加。空调与风管的噪声属于第三笔，风量不足或风速过高都会让本底噪声压在录音上，改起来比买设备贵。

## 后花的设备怎么排

麦克风、话放、插件可以按项目逐步添置，因为它们不改变房间。先买一只通用的大振膜电容麦与一支动圈麦，覆盖人声与鼓；话放够用即可；插件先补均衡与压缩，混响放在最后。升级音箱要谨慎：房间没处理时，换更贵的监听只会把问题听得更清楚。

## 预算最容易失控的地方

把预算全押在设备上，房间只做软装；隔声只做一面墙，声音从门缝与管道绕过去；空调留到最后，风噪无法接受又没有预算改；监听摆位迁就家具，买再好的箱子也白搭。报价单里还应留出一成到一成半的余量，用于拆改与不可预见的结构问题。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5"],"label":"房间做完之后的中频","label_en":"Midrange after the room is done","hint":"在空房间与处理后的房间各播一次，注意和弦的每个音是否一样清楚；有帮助的是均匀，不是更响。","hint_en":"Play this once in the bare room and once after treatment; listen for whether every note stays equally clear. Evenness is the gain, not loudness."}
```
:::

::: en

Buy a good microphone first, record in an untreated room, and the result is still mushy; that is the worst value in the build. Studio budgets have an order: settle the boundary the sound crosses, then the inside of the room, then the gear.

## The four things that come first

| Order | Item | Why it comes first | Can it wait | Cost of doing it late |
|---|---|---|---|---|
| 1 | Dimensions and isolation | A room's size is fixed; absorption cannot stop a leak | No | Demolish and rebuild |
| 2 | Power, earth, HVAC | Sets the noise floor of every recording | No | Cutting walls again |
| 3 | Acoustic treatment | Makes monitoring trustworthy | No | Better gear, worse decisions |
| 4 | Monitors and placement | Shapes every judgement | In stages | Mixes that fail elsewhere |

## Isolation and absorption are separate bills

Isolation keeps sound in and out, using mass, seals and floating construction. Absorption handles reflections inside, using porous material and diffusers. The two get confused: packing absorptive fibre into a wall adds almost no isolation. HVAC is a third bill, and undersized ducts or high air velocity put noise right on top of the recording; correcting that later costs more than any microphone.

## Ordering the gear that comes later

Microphones, preamps and plugins can arrive project by project because they do not change the room. Start with one general-purpose large-diaphragm capacitor mic and one dynamic, enough for voice and drums; a clean preamp is enough; plugins should cover EQ and compression before reverb. Upgrade monitors with care: in an untreated room, a better speaker only makes the problem clearer.

## Where the budget escapes

All the money on gear and only soft furnishings on the walls; isolation on one wall while sound slips through door gaps and ducts; HVAC left to the end, with unacceptable noise and no budget to fix it; monitors placed to suit the furniture, which defeats any speaker. Keep a contingency of ten to fifteen per cent for demolition surprises and structural work.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5"],"label":"Midrange after the room is done","label_en":"Midrange after the room is done","hint":"Play this once in the bare room and once after treatment; listen for whether every note stays equally clear. Evenness is the gain, not loudness.","hint_en":"Play this once in the bare room and once after treatment; listen for whether every note stays equally clear. Evenness is the gain, not loudness."}
```
:::
