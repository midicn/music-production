---
id: microphone-types
site: prod
cat: A4
title: 麦克风类型
title_en: Microphone Types
summary: 电容、动圈、铝带各有换能方式，选型先看声源与声压
summary_en: Condenser, dynamic and ribbon microphones transduce sound differently. Choose by source and sound pressure.
level: standard
tags: [录音, 话筒, 换能方式]
tags_en: [recording, microphone, transducer]
alias: [话筒类型, 麦克风种类, 电容麦, 动圈麦, 铝带麦, condenser, dynamic, ribbon]
links:
  - "[[glossary:condenser-microphone]]"
  - "[[glossary:dynamic-microphone]]"
  - "[[glossary:ribbon-microphone]]"
  - "[[instrument:voice]]"
instances:
  - openscore-000008 | 声乐与钢琴可作录音练习曲目；换能类型比较需同一声源的实际录音 | Voice and piano supply a practice piece; transducer comparisons require recordings of the same actual source
  - mutopia-001541 | 吉他织体可帮助选择录音片段，不能由 MIDI 渲染推断电容话筒瞬态 | Guitar texture helps select recording passages; MIDI rendering cannot establish condenser transient response
  - groove-000003 | 鼓组可作节奏参考，高声压稳定性需依据话筒规格及实际摆位测试 | Drums offer rhythm reference; high-SPL stability requires model specifications and placement tests
sources:
  - "https://service.shure.com/articles/en_US/Knowledge/what-is-phantom-power"
  - Eargle, The Microphone Book, 3rd ed., transducer and directivity chapters
  - Olson, Acoustical Engineering, pressure and pressure-gradient microphone theory
updated: 2026-11-02
---

::: zh
## 问题

电容、动圈和铝带描述换能方式，不是音质等级。选择还要看指向性、频响、灵敏度、自噪声、最大声压与实际摆位；同一类型内部的差别也可能很大。

## 信号链

电容话筒以电容变化检测振动，其供电可能来自幻象电源、电池或专用电源，并非全部要求48V。动圈利用线圈在磁场中运动；铝带让导电薄带在磁场中运动。主动铝带可能需要幻象电源，被动型号的要求也各不相同；必须按具体手册接线供电，不能只凭是否有变压器判断安全。

## 摆位与参数

先按话筒手册确认供电、最大声压和防风要求，再选不会碰撞或受强气流冲击的位置。录一小段，固定增益逐步改变距离与角度，比较直达声、房间声、近讲效应与齿音。具体厘米数只能是某一设备和声源的起点，不能由电容、动圈或铝带三个名称直接决定。

```audiolab
{"type":"instrument","gm":"Cello","synth":"bowed","phrase":["G3","D4","A4","E5"],"label":"大提琴音色参照","label_en":"A cello-timbre reference","hint":"比较合成与采样的音头和尾音。话筒对照应另录同一演奏，固定距离、方向并匹配输出响度。","hint_en":"Compare synthetic and sampled attack and decay. For mic comparison, record the same performance at fixed distance and angle, matching output loudness."}
```

## 听什么

轮换话筒时固定声源、距离和方向，并按灵敏度调整增益以匹配输出响度。比较所需的细节、底噪和离轴染色，不预设电容一定齿音多、动圈一定中频厚或铝带一定柔和。记录型号和位置，才能重复判断。

## 常见误解

- 换能类型不能替代具体型号的声压、供电和环境规格
- 防风、防潮和声压要求按手册操作
- 不清楚某支铝带的幻象电源要求时，先停止送电并查明型号
- 摆位与声源状态也会明显改变录音结果
:::

::: en
## The problem

Condenser, moving-coil and ribbon describe transduction, not quality grades. Also consider pattern, response, sensitivity, self-noise, maximum SPL and placement; models within one category may differ substantially.

## Signal chain

Condenser microphones detect capacitance changes and may use phantom, battery or dedicated power, not universally 48 V. A moving-coil mic moves a coil in a magnetic field; a ribbon moves a conductive strip. Active ribbons may require phantom and passive requirements vary. Follow the exact manual and wiring rather than inferring safety solely from the presence of a transformer.

## Placement and settings

Confirm power, maximum SPL and wind precautions in the mic manual before choosing a position protected from impact and strong airflow. Record a short passage, varying distance and angle at fixed gain to compare direct sound, room, proximity and sibilance. A distance in centimetres is only a starting point for one setup, not something determined solely by condenser, moving-coil or ribbon type.

```audiolab
{"type":"instrument","gm":"Cello","synth":"bowed","phrase":["G3","D4","A4","E5"],"label":"A cello-timbre reference","label_en":"A cello-timbre reference","hint":"Compare synthetic and sampled attack and decay. For mic comparison, record the same performance at fixed distance and angle, matching output loudness.","hint_en":"Compare synthetic and sampled attack and decay. For mic comparison, record the same performance at fixed distance and angle, matching output loudness."}
```

## What to listen for

Keep source, distance and orientation fixed when changing microphones, adjusting gain for matched loudness. Compare required detail, noise and off-axis colour without assuming all condensers are sibilant, moving-coils mid-heavy or ribbons soft. Log model and position for repeatable judgement.

## Common misconceptions

- Transduction type does not replace model-specific SPL, power and environment specifications
- Follow documented wind, moisture and sound-pressure precautions
- If ribbon phantom requirements are unknown, leave power off until the model is identified
- Placement and source condition also substantially affect the result
:::
