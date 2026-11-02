---
id: transient-shaper
site: prod
cat: A7
title: 瞬态整形器
title_en: Transient Shaper
summary: 把音头与余音分开处理，为什么它不需要阈值也不会随力度变。
summary_en: Separating attack from sustain, and why a transient shaper needs no threshold and ignores playing level.
level: standard
tags: [效果器, 动态, 瞬态, 听感]
tags_en: [effects, dynamics, transient, listening]
alias: [瞬态整形器, 瞬态塑形, 音头, 延音, transient shaper]
links:
  - "[[glossary:compressor]]"
  - "[[instrument:drum-kit]]"
  - "[[glossary:bus]]"
instances:
  - groove-000006 | 鼓组起音的素材参照，未执行攻击增减处理 | Drum attacks as source material, without attack boost or cut processing
  - groove-000010 | 包含不同力度的鼓点，可另渲染后测试实际整形器 | Drum events at different velocities for a separate test with an actual shaper
  - pdmx-000031 | 重复节奏型的音符素材，不是瞬态整形前后对照 | Repeated rhythmic notes, not before-and-after transient shaping
sources:
  - "https://docs.slatedigital.com/VMR/Transient_Shaper.html"
  - Udo Zölzer, DAFX.
  - Sound On Sound, transient shaping explained.
updated: 2026-11-02
---

::: zh
## 起点：一个问题

瞬态整形器按声音的起音与后续包络改变增益，常用于调整鼓的敲击感和余响。部分产品采用电平相对检测，不需要用户设置阈值；也有带灵敏度、阈值或多频段检测的设计，不能把一种架构当成所有产品的规则。

## 工作方式

常见做法是比较不同速度的包络跟随器，从变化较快的部分估计起音，再控制增益。旋钮名称虽相似，检测时间、立体声联动和增益限制可能不同。电平独立只表示整体增益变化不应轻易改变检测，不保证轻奏和重奏的频谱、包络或听感完全一致。

## 数值怎么变成声音

攻击加 3–6 dB，鼓槌的点击变清楚；攻击减 3 dB，声音变软、距离变远。延音减 2–4 dB 能让鼓更紧，加则更饱满。两段都推会很快失真，镲片尤其明显。

## 耳朵要抓的点

在同一条音频上做旁通与处理对照，匹配输出电平，听鼓槌、鼓身与房间余响各发生了什么变化。先只动攻击，再只动延音，观察峰值是否超出余量。本站钢琴与鼓组 MIDI 是可选试听素材，没有实际加载瞬态整形处理，不能把换曲后的差别当作处理效果。

```audiolab
{"type":"instrument","gm":"Marimba","synth":"struck","phrase":["C4","E4","G4","C5"],"label":"马林巴音头","label_en":"Marimba attack","hint":"比较音头与后续衰减。这段没有瞬态整形器，攻击增减的效果须用同一音频的处理与旁通版本比较。","hint_en":"Compare the attack with its decay. There is no transient shaper here; compare processed and bypassed versions of the same audio for attack changes."}
```

## 容易弄错的

把瞬态整形器当压缩器；以为加攻击一定更响；用它代替 EQ 处理清晰度。
:::

::: en
## Starting point: a problem

A transient shaper changes gain according to attacks and the following envelope, often to adjust a drum's impact and sustain. Some products use level-relative detection with no user threshold; others provide sensitivity, threshold or multiband detection. One architecture does not describe every product.

## The working principle

One common approach compares envelope followers with different response speeds to estimate attacks and shape gain. Detection time, stereo linking and gain limits differ between products. Level-independent detection means an overall gain change need not alter detection; it does not make soft and hard performances identical in spectrum, envelope or sound.

## From numbers to sound

Plus 3 to 6 dB of attack sharpens a beater click; minus 3 dB softens the sound and pushes it back. Cutting sustain by 2 to 4 dB tightens a drum, while adding makes it fuller. Boosting both distorts quickly, especially on cymbals.

## What the ear should catch

Compare bypassed and processed versions of the same audio at matched output level, listening separately to beater, drum body and room tail. Change attack and sustain one at a time and watch peak headroom. The piano and drum MIDI examples are source material only; they do not apply transient shaping, and a change of piece is not a processing comparison.

```audiolab
{"type":"instrument","gm":"Marimba","synth":"struck","phrase":["C4","E4","G4","C5"],"label":"Marimba attack","label_en":"Marimba attack","hint":"Compare the attack with its decay. There is no transient shaper here; compare processed and bypassed versions of the same audio for attack changes.","hint_en":"Compare the attack with its decay. There is no transient shaper here; compare processed and bypassed versions of the same audio for attack changes."}
```

## Easy to get wrong

That a transient shaper is a compressor; that more attack always means louder; that it can replace EQ for clarity.
:::
