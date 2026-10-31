---
id: drum-miking
site: prod
cat: A4
order: 360
title: 鼓组拾音
title_en: Drum Kit Miking
summary: 鼓组录得脏，先查鼓皮、相位与串音，再换话筒
summary_en: A dirty drum sound is usually tuning, phase and bleed before it is the microphone.
level: standard
tags: [鼓组, 拾音, 相位, 串音, 房间话筒]
tags_en: [drums, miking, phase, bleed, room mic]
alias: [鼓组拾音, 鼓录音, 架子鼓录音, 鼓话筒摆位, drum miking, drum recording]
links:
  - "[[instrument:drum-kit]]"
  - "[[instrument:snare-drum]]"
  - "[[instrument:bass-drum]]"
  - "[[instrument:cymbals]]"
  - "[[glossary:phase-check]]"
  - "[[glossary:polar-pattern]]"
instances:
  - groove-000010 | 80 BPM 的放克鼓组，底鼓与军鼓交替密集，近点串音与相位问题最先在这里露出来（C1）
  - groove-000281 | 120 BPM 的爵士三拍子，ride 一直在响，考验镲片话筒的串音与门（C1）
  - groove-000684 | 70 BPM 的 6/8 摇滚，军鼓与通鼓落差大，适合比较近点与房间的比例（C1）
sources:
  - Eargle, John，The Microphone Book（Focal Press）— 鼓与打击乐拾音
  - Bartlett, Bruce，Practical Recording Techniques（Focal Press）— 鼓组摆位与串音
  - Mike Senior，Recording Secrets for the Small Studio（Focal Press）— 小房间鼓录音
updated: 2026-10-31
---

::: zh
## 先让鼓组自己成立

鼓组录得脏，先别换话筒。鼓皮旧了、响弦松了、镲片架得太低，再贵的电容话筒也救不回来。花半小时换鼓皮、调响弦、把共振的螺丝和架子按住，再让鼓手用正常力度打一遍；这一步的收益大过整条信号链。

## 逐件摆位，一支话筒一件活

| 位置 | 距离与角度 | 常见毛病 |
|---|---|---|
| 底鼓 | 开孔内 2–5 厘米，偏鼓心 | 气流扑麦、踏板噪声 |
| 军鼓上 | 鼓皮上方 3–5 厘米，指向鼓心偏边 | 太近只剩鼓皮，没有鼓腔 |
| 军鼓下 | 响弦下 5–8 厘米 | 底鼓串音、响弦沙沙声 |
| 踩镲 | 上方 10–15 厘米，朝外 | 军鼓串音 |
| 通鼓 | 鼓皮上方 3–5 厘米 | 相邻鼓与镲片串音 |
| 头顶 | 镲片上方 40–60 厘米，左右对称 | 高度不一，相位打架 |
| 房间 | 2–4 米，离地 2 米以上 | 角落低频堆积 |

近点不是越近越好。军鼓话筒贴到鼓皮一厘米，鼓腔的厚度就没了；底鼓话筒正对气流，每一脚都是低频砰声。表里的距离是起点，鼓手力度大时整体退开两三厘米，串音会少，起音也不会丢。

## 相位与门，先对齐再降噪

多支话筒收到同一套鼓，有时间差。先把头顶与军鼓、底鼓逐一对比极性，再把波形推到对齐；对齐之后，门才有意义。门放得太靠前，会把串音切成机械的呼吸声。底鼓的释放不要短于一百毫秒，房间话筒不要门，宁可让它脏一点。

## 房间话筒不是备选

房间话筒给的是鼓组作为一个整体的体积。放在鼓手正前方两到四米、高过镲片，单支即可；压缩狠一点，让它在中频顶出来。它和头顶话筒之间同样要查相位，极性反了，低频先塌下去。

## 什么时候不该加话筒

爵士、复古摇滚、小房间，一支话筒或一对头顶反而更完整，鼓手自己平衡力度，录音师只负责接住。反过来，鼓皮状态差、镲片太亮、房间又小又硬，多支话筒只会把问题放大：串音更多，相位更难对，混音时每一轨都要修。先处理鼓、房间和演奏，实在不行就用采样替换，别在相位上耗一整天。

```audiolab
{"type":"instrument","gm":"Melodic Tom","synth":"perc","phrase":["C2","G2","C2","D2","G2","C3"],"label":"近点拾音的起音","label_en":"Attack at close range","hint":"先听每一下的起音与余音，再想话筒退到三十厘米后哪些细节先消失","hint_en":"Hear each attack and tail, then imagine which details vanish when the mic backs off 30 cm"}
```
:::

::: en
## Let the kit sound right first

A muddy drum recording is rarely the microphone's fault. Old heads, a loose snare wire, a cymbal hanging too low over the snare: no expensive condenser fixes any of that. Spend half an hour changing heads, tensioning the wires and damping the hardware that rattles, then have the drummer play at normal force. That half hour buys more than the whole signal chain.

## One mic per job

| Position | Distance and angle | Usual trouble |
|---|---|---|
| Kick | 2–5 cm inside the port, off centre | Air blasts, pedal noise |
| Snare top | 3–5 cm above the head, aimed off centre | Too close loses the shell |
| Snare bottom | 5–8 cm under the wires | Kick bleed, wire hiss |
| Hi-hat | 10–15 cm above, angled outward | Snare bleed |
| Toms | 3–5 cm above the head | Neighbouring drums and cymbals |
| Overheads | 40–60 cm above the cymbals, symmetrical | Uneven height, phase fights |
| Room | 2–4 m out, 2 m up | Low-end pile-up in corners |

Closer is not automatically better. Put a snare mic 1 cm from the head and the shell depth disappears; aim a kick mic into the airflow and every beat turns into a low thump. Treat the distances in the table as a starting point: with a heavy hitter, back every mic off two or three centimetres to cut bleed without losing the attack.

## Phase and gates, in that order

Every mic hears the kit at a slightly different time. Compare polarity between each close mic and the overheads, then nudge the waveforms into alignment. Only then does a gate make sense. Gate too early and the bleed gets chopped into mechanical breathing. Keep kick release above 100 ms, and leave the room mic ungated; a little dirt is the point.

## The room mic is not optional

A room mic supplies the size of the kit as one instrument. Put a single one 2 to 4 m in front of the drummer, above cymbal height, and compress it hard enough to bring the midrange forward. Check its polarity against the overheads too; when it is inverted, the low end collapses first.

## When not to add mics

Jazz, retro rock and small rooms often sound more complete with one mic or a single overhead pair. The drummer balances the kit and the engineer just captures it. The opposite is true when the heads are tired, the cymbals are harsh and the room is small and hard: more microphones only amplify the problem with more bleed, harder phase work and another track to fix at mixdown. Fix the kit, the room and the playing first; if that fails, replace the shells with samples rather than spending the day chasing phase.

```audiolab
{"type":"instrument","gm":"Melodic Tom","synth":"perc","phrase":["C2","G2","C2","D2","G2","C3"],"label":"近点拾音的起音","label_en":"Attack at close range","hint":"先听每一下的起音与余音，再想话筒退到三十厘米后哪些细节先消失","hint_en":"Hear each attack and tail, then imagine which details vanish when the mic backs off 30 cm"}
```
:::
