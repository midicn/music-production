---
id: vocal-riding
site: prod
cat: A6
order: 432
title: 人声骑乘：逐句电平与动态
title_en: Vocal Riding: Line-by-Line Level and Dynamics
summary: 骑乘让每个字的重量按歌词走，整轨压低只会抹平句法。
summary_en: Riding follows the weight of each word in the lyric; lowering the whole track only flattens the phrasing.
level: standard
tags: [混音, 人声, 自动化, 动态]
tags_en: [mixing, vocal, automation, dynamics]
alias: [人声骑乘, 人声自动化, vocal riding, vocal automation]
links:
  - "[[glossary:automation]]"
  - "[[glossary:compressor]]"
  - "[[glossary:gain-staging]]"
  - "[[instrument:voice]]"
instances:
  - openscore-000008 | 《魔王》在角色与叙事之间切换，句与句的重量差很大
  - openscore-000007 | 法语艺术歌曲长句多，气口与句尾最容易听出骑乘是否自然
  - mutopia-000546 | 人声与钢琴贴得近，句内小起伏必须保留
sources:
  - Bobby Owsinski, The Mixing Engineer's Handbook（Cengage）人声电平与自动化章节
  - David Gibson, The Art of Mixing（Thomson）主唱重音与句法章节
  - iZotope, Nectar 官方文档中 Vocal Assistant 与电平自动化章节
updated: 2026-10-31
---

::: zh
## 先分清三层动态

人声的起伏来自三处：演唱本身的强弱、句与句之间的电平差、字与字之间的微小抖动。骑乘只管第二层，压缩管第三层，第一层要保留。若把三者都交给压缩器，字头会变钝，长音会抽吸，情绪被压成一条直线。先听一遍无处理的干声，标出哪些词是支点，哪些只是过门。

## 四种动作

| 症状 | 动作 | 幅度与时长 | 别做 |
|---|---|---|---|
| 句首被吃掉 | 提前一两个字起推 | 0.5–2 dB，随乐句缓入 | 不要把上一句尾也推高 |
| 长音渐弱 | 跟着气息补 | 一到两秒内 1–3 dB | 不要用压缩硬顶 |
| 爆破音过重 | 单字快速下拉 | 10–30 ms，1–2 dB | 不要画成阶梯 |
| 副歌整体偏高 | 整段先降，再句内补 | 静态 1–2 dB | 不要只靠限制器 |

动作要写在推子上，不写在剪辑里。剪辑改的是素材，推子改的是关系，后者随时能回退。

## 写自动化之前

先把每句的 clip gain 对齐到同一视觉电平，清掉明显的气口噪声，再挂一个慢启动、二比一的压缩，只做两到三 dB。压缩稳住字内峰值，剩下的句间落差留给推子。自动化用 latch 或 touch 写，画完把节点简化，避免锯齿。小音量下检查一遍，哪些字听不见，就在那里补，而不是整轨加高。

## 会坏在哪里

每个字都一样响，听起来像朗读，不像演唱。推子画得太密，长音会一抖一抖；气口被推高，句子会失去呼吸。压缩做了六 dB 以上，骑乘就失去意义。说唱与高声压的摇滚里，有些句子本来就该被伴奏盖住一点，全部拉到前景反而假。

```audiolab
{"type":"instrument","gm":"Voice Oohs","synth":"vocal","phrase":["G4","A4","B4","D5","B4","A4","G4","E4"],"label":"一句有支点的旋律","label_en":"A phrase with a strong turning point","hint":"先听哪几个音需要补，再想压缩会先抹平哪里","hint_en":"Hear which notes need support, then imagine what the compressor would flatten first"}
```
:::

::: en
## Separate three layers

A vocal moves at three scales: how hard the singer sings, the level difference between lines, and tiny wobbles inside words. Riding handles the middle layer, compression the smallest one, and the first must be preserved. Hand all three to a compressor and consonants soften, long notes pump, and the emotional line flattens. Listen to the dry take once and mark which words carry the phrase and which merely pass through.

## Four moves

| Symptom | Move | Amount and timing | Avoid |
|---|---|---|---|
| First word is buried | lift one or two words early | 0.5–2 dB, eased into the phrase | pushing the previous line's tail as well |
| Long note fades | follow the breath | 1–3 dB across one or two seconds | holding it up with compression |
| A plosive is too loud | short dip on that syllable | 10–30 ms, 1–2 dB | drawing it as a staircase |
| Whole chorus sits high | lower the section, then ride inside it | 1–2 dB static | relying on the limiter |

Write moves on the fader, not in the edit. Editing changes the material; a fader changes relationships and can be undone.

## Before drawing automation

Match each line with clip gain until it looks even, clean obvious breath noise, then use a slow 2:1 compressor for 2–3 dB. Compression holds peaks inside a word; the fader handles the distance between lines. Write in latch or touch, then simplify the nodes to avoid zipper noise. Check at low volume and lift only the words that disappear, not the whole track.

## Where it breaks

When every syllable is equally loud it sounds read, not sung. Dense fader moves make long notes wobble; lifting breaths removes the breathing. If the compressor already works 6 dB or more, riding has nothing left to shape. In rap and loud rock some lines should sit slightly under the backing; pulling everything forward sounds false.

```audiolab
{"type": "instrument", "gm": "Voice Oohs", "synth": "vocal", "phrase": ["G4", "A4", "B4", "D5", "B4", "A4", "G4", "E4"], "label": "A phrase with a strong turning point", "label_en": "A phrase with a strong turning point", "hint": "Hear which notes need support, then imagine what the compressor would flatten first", "hint_en": "Hear which notes need support, then imagine what the compressor would flatten first"}
```
:::
