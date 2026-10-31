---
id: sbir-boundary
site: prod
cat: A5
title: 边界干涉 SBIR
title_en: Boundary Interference (SBIR)
summary: 后墙与台面把低频抵消出一段深谷，先算频率再挪箱子。
summary_en: A wall or console behind the speaker cancels part of the low end; work out the frequency before moving anything.
level: standard
tags: [边界干涉, SBIR, 低频, 摆位, 梳状滤波]
tags_en: [SBIR, boundary interference, low end, placement, comb filtering]
alias: [边界干涉, 音箱后墙, 低频抵消, speaker boundary interference, SBIR]
order: 390
links:
  - "[[glossary:comb-filtering]]"
  - "[[glossary:nearfield-monitor]]"
  - "[[glossary:room-mode]]"
  - "[[instrument:double-bass]]"
instances:
  - pdmx-000801 | 低音提琴低音区连续下行，挪动音箱后能听出被后墙吃掉的那一段（C1）
  - pdmx-000237 | 钢琴与贝斯的爵士，贝斯线慢，便于逐音比较近墙与离墙的差别（C1）
  - cyberhymnal-000527 | 赞美诗的低音声部持续发声，适合听边界干涉造成的空洞（C1）
sources:
  - Everest, F. Alton，Master Handbook of Acoustics（McGraw-Hill）— 扬声器边界干涉与低频抵消
  - Newell, Philip，Recording Studio Design（Focal Press）— 控制室低频与扬声器嵌入
  - Toole, Floyd，Sound Reproduction（Focal Press）— 房间边界与低频响应
updated: 2026-10-31
---

::: zh
低频在某一段突然塌下去，换一对音箱还在同一处塌，问题多半不在单元，而在音箱背后那面墙。边界干涉由直达声与墙面反射声相减造成，它挑频率，也挑距离。

## 距离决定谷的位置

音箱到后墙的距离 d 带来 2d 的路径差，第一个深谷落在声速除以四倍距离处：一米约 86 Hz，半米约 172 Hz，两米约 43 Hz。近墙摆放把谷推到中低频，远处摆放把谷压到更低、更难处理的位置。墙角会叠加侧墙与地面的反射，谷不止一个。

## 四处边界各管一段

| 边界 | 典型距离 | 首个深谷 | 听感 | 先做什么 |
|---|---|---|---|---|
| 后墙 | 0.3–1 米 | 86–286 Hz | 人声发薄、贝斯少一截 | 挪箱或嵌入 |
| 侧墙 | 0.6–1.5 米 | 57–143 Hz | 左右不对称、中央偏移 | 对称摆位 |
| 地面 | 1–1.2 米 | 70–86 Hz | 低频发闷、脚下发虚 | 支架与减震 |
| 台面 | 0.2–0.4 米 | 215–430 Hz | 中低频空洞 | 倾斜台面 |

## 先挪，再吸，最后才均衡

把音箱从后墙挪开，找一个谷不落在关键音区的距离；嵌入墙体能消掉后墙反射，但要求箱体与墙密封。墙角放厚吸声体对高频有效，低频需要足够厚的多孔材料或共振结构。均衡只能压峰，填谷等于给抵消频率加能量，越提越空。

## 什么时候不该先动墙

房间很小、听音距离不足一米时，直达声占主导，边界干涉的谷常被房间模式盖过，先处理模式更划算。已经嵌入墙体的主监听，后墙干涉基本消失，此时该查侧墙与台面。把每处凹陷都归给边界干涉也不对：分频、驻波、桌面反射都会在频响曲线上留下痕迹，移动音箱后谷跟着移动，才是边界干涉。

```audiolab
{"type":"instrument","gm":"Contrabass","synth":"bowed","phrase":["E1","G1","A1","C2"],"label":"后墙抵消：低音逐个听","label_en":"Wall cancellation, one low note at a time","hint":"在听音位播这四个音，再把音箱前后挪十厘米复播；某个音变实或变空，就是抵消换了频率。","hint_en":"Play these four notes at the listening position, then shift the speakers ten centimetres and repeat; a note that fills in or hollows out marks the cancellation moving."}
```
:::

::: en

The low end collapses in a narrow band, and a different pair of speakers collapses in the same place. The drivers are usually fine; the wall behind them is not. A reflection arriving just after the direct sound subtracts from it, and which frequencies suffer depends on how far the speaker sits from the boundary.

## Distance sets the notch

A gap of d metres puts the first deep notch near the speed of sound divided by four times the distance: about 86 Hz at one metre, 172 Hz at half a metre, 43 Hz at two metres. Close to the wall the notch lands in the low midrange; far out it drops lower, where treatment rarely reaches. Corners add the side wall and floor, so more than one notch appears.

## Four boundaries, four bands

| Boundary | Typical distance | First notch | What it sounds like | First move |
|---|---|---|---|---|
| Rear wall | 0.3–1 m | 86–286 Hz | Thin voice, bass loses a layer | Move or flush-mount |
| Side wall | 0.6–1.5 m | 57–143 Hz | Image pulls, left and right differ | Symmetrical layout |
| Floor | 1–1.2 m | 70–86 Hz | Woolly low end, no footing | Stands and decoupling |
| Console top | 0.2–0.4 m | 215–430 Hz | Hollow low midrange | Angle the surface |

## Move first, absorb second, equalise last

Pull the speakers away from the wall until the notch misses the notes that matter; flush mounting removes the rear reflection but needs a sealed joint between cabinet and wall. Thick absorbers in the corners work on the top end; the bottom needs real depth or a resonant structure. EQ can cut a peak, but boosting a null feeds the cancellation and makes the hole wider.

## When the wall is not the first suspect

In a small room with less than a metre of listening distance the direct sound dominates, and modal behaviour usually outweighs boundary interference; treat the modes first. A flush-mounted main monitor has no rear-wall notch left, so look at the side walls and the console instead. Not every dip is boundary interference: crossover behaviour, standing waves and desk reflections all leave marks on the same curve. Move the speaker and watch whether the dip travels with it.

```audiolab
{"type":"instrument","gm":"Contrabass","synth":"bowed","phrase":["E1","G1","A1","C2"],"label":"Wall cancellation, one low note at a time","label_en":"Wall cancellation, one low note at a time","hint":"Play these four notes at the listening position, then shift the speakers ten centimetres and repeat; a note that fills in or hollows out marks the cancellation moving.","hint_en":"Play these four notes at the listening position, then shift the speakers ten centimetres and repeat; a note that fills in or hollows out marks the cancellation moving."}
```
:::
