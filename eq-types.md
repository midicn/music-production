---
id: eq-types
site: prod
cat: A7
title: 均衡器的三种形态
title_en: Three Shapes of EQ
summary: 图示、参量与搁架 EQ 各自动了哪一段，听感差别在哪里。
summary_en: What graphic, parametric and shelving EQs each control, and how their moves differ on the same source.
level: standard
tags: [效果器, 均衡, 频率, 听感]
tags_en: [effects, eq, frequency, listening]
alias: [EQ, 均衡器, 图示EQ, 参量EQ, 搁架EQ, equalizer]
links:
  - "[[glossary:eq]]"
  - "[[glossary:bus]]"
  - "[[instrument:piano]]"
  - "[[period:classical]]"
instances:
  - pdmx-000031 | 独奏钢琴跨越三个八度，适合分辨低架、钟形与高架各自动了哪一段
  - mutopia-001411 | 萨蒂《裸体歌舞》织体稀疏，窄带提升的染色很容易听出
  - pdmx-000070 | 弦乐慢板频段连续，适合比较搁架与参量在整体亮度上的差别
sources:
  - Huber and Runstein, Modern Recording Techniques, equalisation chapter.
  - Sound On Sound, EQ Explained by Hugh Robjohns.
updated: 2026-10-28
---

::: zh
## 难在哪

同样标着「提升 3 dB」，图示 EQ、参量 EQ 与搁架 EQ 得到的结果并不一样。分不清形态，参数再准也只是碰运气。

## 工作方式

图示 EQ 把频谱切成固定数目的推子，中心频率与带宽都锁死，胜在快；参量 EQ 每段可调中心频率、增益与 Q，Q 越大作用范围越窄；搁架 EQ 只整体抬高或压低某一频率以上或以下的内容，没有峰。三者都是滤波器组合，区别在于可控的维度。

## 旋钮与耳朵

参量段动 1–3 dB 已经很明显，Q 超过 4 会出现窄带染色，像在声音上多出一条细窄的共鸣；高架提升让整体变亮，过量则齿音刺耳；低架衰减能减薄，减太多就失去根基。图示 EQ 相邻推子互相叠加，同一频段常被抬两次。

## 耳朵要抓的点

放一段钢琴独奏，先听 200–400 Hz 的箱体感，再听 3 kHz 以上的按键噪声。窄带提升只移动一小块，搁架提升把整块布往上提。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5"],"label":"待处理的钢琴素材","label_en":"Piano material to process","hint":"先听干声，再分别试搁架与窄带提升","hint_en":"Hear it dry, then try a shelf and a narrow boost"}
```

## 容易弄错的

把 EQ 当作万能修音，忽略相位与共振；以为推子越多越精细，其实固定频段会漏掉真正的问题频率。
:::

::: en
## Where it gets hard

Both EQs claim a 3 dB boost, yet a graphic, a parametric and a shelving band give different results. Choose the wrong shape and precise numbers buy nothing.

## The working principle

A graphic EQ divides the spectrum into fixed sliders, with centre frequencies and bandwidth locked; it is fast. A parametric band lets you set centre, gain and Q, and a higher Q narrows the affected range. A shelf raises or lowers everything above or below a corner frequency and has no peak. All three are filters; they differ in which dimensions you control.

## Knobs and ears

On a parametric band, 1 to 3 dB is already audible; above Q 4 the boost rings on one narrow band. A high shelf brightens the whole signal and turns harsh when overdone. A low shelf thins a source, and too much removes its foundation. Adjacent graphic sliders overlap, so one region often gets lifted twice.

## What the ear should catch

Play a solo piano and listen first to the body around 200 to 400 Hz, then to key noise above 3 kHz. A narrow boost moves one small patch; a shelf lifts the whole cloth.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "E4", "G4", "C5"], "label": "Piano material to process", "label_en": "Piano material to process", "hint": "先听干声，再分别试搁架与窄带提升", "hint_en": "Hear it dry, then try a shelf and a narrow boost"}
```

## Easy to get wrong

That EQ can fix anything, ignoring phase and resonance; that more sliders mean more precision, when fixed bands simply miss the frequency that matters.
:::
