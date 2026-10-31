---
id: nearfield-monitoring
site: prod
cat: A5
title: 近场监听
title_en: Nearfield Monitoring
summary: 近场箱贴近听，中频可信，低频要靠别的系统复核。
summary_en: Close speakers make the midrange trustworthy; low end needs another system to confirm.
level: standard
tags: [监听, 近场, 中频, 摆位, 校准]
tags_en: [monitoring, nearfield, midrange, placement, calibration]
alias: [近场监听, 近场音箱, 近场箱, nearfield monitoring, nearfield speaker]
links:
  - "[[glossary:nearfield-monitor]]"
  - "[[glossary:reference-monitor]]"
  - "[[glossary:monitoring]]"
  - "[[glossary:room-mode]]"
instances:
  - mutopia-000546 | 人声与钢琴集中在中频，近场最容易听出鼻音与掩蔽
  - groove-000000 | 放克鼓循环，瞬态与底鼓在小箱上是否立得住一听便知
  - oga-000057 | 钢琴与两种贝斯同场，可检查低频延伸与中低频厚度
sources:
  - Newell, Philip，Recording Studio Design（Focal Press）— 近场监听与房间关系章节核对，未引用
  - Toole, Floyd，Sound Reproduction（Focal Press）— 听音位置与低频边界增益章节核对，未引用
updated: 2026-10-28
---

::: zh
## 要解决的事
近场监听把音箱放在一米左右，听者主要听到直达声。它让中频判断更可靠，但小口径低频有限。问题是何时信它，何时换一套系统。

## 背后的逻辑
近场箱的直达声压过房间反射，因此受房间模式影响较小；分频点附近的中频相位简单，人声与乐器的轮廓清楚。代价在低频，五英寸单元在六十赫兹以下迅速衰减，混音者容易把低频推多。把高音单元与耳朵齐平，离墙留出距离，音量控制在七十五到八十 dB，避免等响曲线改变判断。

## 参数与取舍
先校准电平与摆位，再用熟悉的人声与钢琴检查中频。低频交给耳机或更大的系统复核，不要在小箱上做超低频决定。贴墙会抬高低频边界增益，桌面反射会染色中频，需要垫高或倾斜。单只音箱做单声道检查，能听出相位与掩蔽。

## 耳朵要抓的点
人声是否站得住，钢琴中低音区是否浑浊，鼓的瞬态是否清楚。同一段素材换到耳机，若低频突然多出一截，说明近场箱的低频不可信。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C3","G3","E3","B3","D4"],"label":"钢琴的中低音区","label_en":"The piano's middle-low register","hint":"先听这几个音在小箱上的厚度，再换耳机，注意低频多出多少","hint_en":"Hear these notes on small speakers first, then on headphones, and notice how much low end appears"}
```

## 容易弄错的
以为近场就是准确，贵的就是平的。近场只保证中频可信，低频与超低频必须另找参照。开大音量只会让等响曲线替你做决定。
:::

::: en
## The problem to solve
Nearfield monitoring places speakers about a metre away, so the listener hears mostly direct sound. That makes the midrange dependable, but small woofers run out of low end. The question is when to trust them and when to check on another system.

## The logic behind it
Direct sound outweighs room reflections at close range, so room modes matter less. Around the crossover, phase is simple and voices keep a clear outline. The cost is bass: a five-inch woofer falls away quickly below sixty hertz, and mixers tend to overdo the low end. Put the tweeter at ear height, leave space behind the cabinet, and work near seventy-five to eighty decibels so equal-loudness curves do not steer you.

## Settings and trade-offs
Calibrate level and placement, then check the midrange on a familiar voice and piano. Confirm bass on headphones or a larger system; do not decide sub-bass on small boxes. A wall behind lifts the low boundary gain, and a desk colours the midrange, so raise or tilt the monitors. Use one speaker in mono to hear phase and masking.

## What the ear catches
Does the voice hold its place, does the piano's middle-low register turn muddy, do drum transients stay clear? Move the same passage to headphones; if bass suddenly appears, the nearfield's low end is not trustworthy.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C3", "G3", "E3", "B3", "D4"], "label": "The piano's middle-low register", "label_en": "The piano's middle-low register", "hint": "先听这几个音在小箱上的厚度，再换耳机，注意低频多出多少", "hint_en": "Hear these notes on small speakers first, then on headphones, and notice how much low end appears"}
```

## Common misconceptions
That nearfield means accurate, or that expensive means flat. Nearfield only guarantees the midrange; bass and sub-bass need another reference. Turning up the volume only lets the loudness curve decide.
:::
