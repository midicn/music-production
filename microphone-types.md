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
  - openscore-000008 | 男声与钢琴，适合比较电容与动圈在中频的差别
  - mutopia-001541 | 尼龙弦吉他细节多，适合听电容话筒的瞬态
  - groove-000003 | 鼓组节奏，适合听动圈在近距离高声压下的稳定
sources:
  - Eargle, The Microphone Book, 3rd ed., transducer and directivity chapters
  - Olson, Acoustical Engineering, pressure and pressure-gradient microphone theory
updated: 2026-10-28
---

::: zh
## 问题

电容、动圈、铝带不是三档好坏，而是三种把声压变成电压的方式。选错类型，摆位再准也补不回来。先看声源有多响、需要多少细节，再决定用哪一种。

## 信号链

电容话筒靠振膜与极化电压工作，灵敏度高、瞬态快，需要 48V。动圈靠线圈在磁场里运动，结构结实，能承受高声压。铝带是一张很薄的金属箔，常用 8 字形，质量轻、高频柔和；老式铝带在没有隔离变压器时不要开 48V。

## 摆位与参数

电容离人声 15 至 25 厘米，离吉他 20 至 30 厘米，拾取细节。动圈贴近鼓皮 2 至 5 厘米，或贴在音箱网罩前。铝带放在 30 厘米外，加防风，避免气流直吹。

```audiolab
{"type":"instrument","gm":"Cello","synth":"bowed","phrase":["G3","D4","A4","E5"],"label":"同一把琴的三种听法","label_en":"One instrument heard three ways","hint":"先听合成近似，再听 GM 采样，注意高频细节与瞬态","hint_en":"Compare synth and GM sample for high-frequency detail and transient"}
```

## 听什么

同一声源轮换三支话筒，听高频细节、低频厚度与瞬态边缘。电容的齿音更明显，动圈的中频更实，铝带的高频更收。

## 常见误解

- **电容一定更高级** → 高声压与近距离场合，动圈更稳。
- **动圈只能录鼓** → 人声与吉他音箱也常用。
- **铝带完全不能加 48V** → 现代带隔离变压器的型号可以，老式型号要先确认。
:::

::: en
## The problem

Condenser, dynamic and ribbon are not grades of quality but three ways of turning sound pressure into voltage. Pick the wrong type and no placement can repair it. First decide how loud the source is and how much detail you need.

## Signal chain

A condenser uses a diaphragm and a polarising voltage; it is sensitive and fast, and needs 48 V. A dynamic moves a coil through a magnetic field; it is rugged and tolerates high sound pressure. A ribbon is a thin metal foil, often figure-eight, light and soft on top. Do not apply 48 V to an old ribbon without an isolating transformer.

## Placement and settings

Place a condenser 15 to 25 cm from a voice, or 20 to 30 cm from a guitar, for detail. Put a dynamic 2 to 5 cm from a drum head or at a speaker grille. Set a ribbon 30 cm away with a wind screen, away from direct blasts of air.

```audiolab
{"type": "instrument", "gm": "Cello", "synth": "bowed", "phrase": ["G3", "D4", "A4", "E5"], "label": "One instrument heard three ways", "label_en": "One instrument heard three ways", "hint": "先听合成近似，再听 GM 采样，注意高频细节与瞬态", "hint_en": "Compare synth and GM sample for high-frequency detail and transient"}
```

## What to listen for

Rotate the three types on one source and listen for high-frequency detail, low-end weight and transient edge. A condenser exposes sibilance, a dynamic firms up the midrange, and a ribbon tames the top.

## Common misconceptions

- **Condensers are always better** → at high pressure up close, a dynamic is more stable.
- **Dynamics are only for drums** → they also suit voices and guitar amps.
- **Ribbons can never take 48 V** → modern isolated models can; check an old one first.
:::
