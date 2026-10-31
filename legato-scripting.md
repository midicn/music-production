---
id: legato-scripting
site: prod
cat: B4
order: 490
title: 连奏脚本
title_en: Legato Scripting
summary: 重叠的音符只是触发条件，脚本还要选过渡、压音量、补延迟。
summary_en: Overlapping notes only trigger the script; it still has to choose a transition, trim its level and pay back the delay.
level: standard
tags: [连奏, 采样器, 脚本, 演奏法]
tags_en: [legato, sampler, scripting, articulation]
alias: [连奏脚本, 连音脚本, 过渡采样, legato script, legato]
links:
  - "[[glossary:legato]]"
  - "[[glossary:sampler]]"
  - "[[instrument:violin]]"
instances:
  - musicnet-000067 | 贝多芬第十五弦乐四重奏第一乐章，长句里的换弓与换弦正是连奏脚本要模仿的缝
  - pdmx-000065 | 巴赫第一大提琴组曲，单声部线条没有和声遮挡，过渡音一假就听得出
  - musicnet-000020 | 巴赫第三大提琴组曲前奏，快速走句里每一次落指都可能触发过渡
sources:
  - Native Instruments Kontakt 手册，KSP 脚本与连奏乐器的相关章节（官方文档）。
  - Curtis Roads, The Computer Music Tutorial, MIT Press，采样回放与包络处理。
  - 弦乐换弓与管乐吐音的演奏惯例，对照配器教材整理。
updated: 2026-10-31
---

::: zh
把两个音叠在一起，采样器不会自动连起来，除非脚本在中间接过手。

## 先听断在哪

在键盘上弹一个五度，让第二个音压住第一个音的尾巴。没有脚本时，两段采样各自起音，接缝处叠出一块厚边；有脚本时，第二个音的音头被换成长短不一的过渡采样，听起来才像一根弓毛拉过去。先找到断点，才知道脚本该管什么。弦乐的换弓、换弦、换把，管乐的吐音与滑音，断法不同，用的过渡也不同。

## 脚本等的是一次重叠

脚本监听 note-on 与 note-off，记下还按着的音。新音进来时，如果旧音仍在，就触发过渡；旧音释放时，再决定是淡出还是接尾音。单声部连奏要抢占发声，复音连奏要为每一对音找过渡。音程也要判断：小二度与大三度往往不是同一条样本。触发门槛可调，重叠太短会漏，太长会让两个音头都留下。

| 参数 | 常见做法 | 调错的后果 |
|---|---|---|
| 重叠门槛 | 几毫秒到几十毫秒 | 太短不触发，太长留下双音头 |
| 过渡选择 | 按音程分组取样本 | 大跳用了级进样本，滑音变糊 |
| 过渡音量 | 压低到接近原音 | 太响像多出一个音，太轻则断开 |
| 释放处理 | 淡出或接 release 样本 | 尾音被硬切，句子像被剪断 |
| 延迟补偿 | DAW 负延迟或播放器预读 | 手感发飘，快句整体往后拖 |

## 弦乐与管乐不是一套

弦乐的连奏靠换弓与换弦，过渡样本里带着弓毛的摩擦；管乐靠气息与按键，连奏更像音高滑过去，而不是重新起音。把弦乐脚本套在长笛上，句子会显得过分黏。铜管还要考虑起音前的气息声，过长的过渡会把铜管的棱角磨平。写脚本前先问：这件乐器在两个音之间到底做了什么动作。

## 什么时候别用脚本

快速重复同一个音、又让它们略微重叠时，连奏脚本会把每次重复都当成过渡，声音反而糊成一片，这时该让[[glossary:sampler|采样器]]里的轮替组接手。超过八度的跳进，多数过渡样本只覆盖常见音程，硬触发不如留一个短缝。延迟也是代价：为了等过渡样本，播放器可能整体推迟几毫秒，实时演奏时这份延迟会传到手指上。脚本能修的是音符之间的接缝，修不了不合理的分句。

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["G3","A3","B3","C4","D4","E4"],"label":"六个音连成一条线","label_en":"Six notes joined into one line","hint":"先听每个音之间的接缝，再想象脚本把后一个音的起音换成了过渡","hint_en":"Hear the seam between notes, then imagine the script replacing the next attack with a transition"}
```
:::

::: en
Stack two notes and most samplers simply play both. A legato script is what turns the overlap into one moving line.

## Where the line breaks

Play a fifth and let the second note sit on the tail of the first. Without a script the two attacks pile up and the join sounds thick. With one, the second attack is replaced by a transition sample and the phrase reads as a single bow stroke. Find the break first: bow change, string crossing, shift, tonguing or slide. Each has its own transition.

## What the script waits for

The script watches note-on and note-off and keeps a list of held notes. A new note while an old one is still down triggers a transition; the release decides whether to fade or hand over to a release sample. Monophonic legato steals the voice, polyphonic legato finds a transition for every pair. Interval matters: a minor second and a major third rarely use the same sample. The overlap threshold is adjustable; too short and it misses, too long and both attacks remain.

| Parameter | Common practice | What goes wrong |
|---|---|---|
| Overlap threshold | A few to a few dozen milliseconds | Too short misses; too long leaves two attacks |
| Transition choice | Samples grouped by interval | A leap uses a step sample and turns muddy |
| Transition level | Trimmed close to the main note | Too loud adds a note; too quiet breaks the line |
| Release handling | Fade or a release sample | The tail is cut and the phrase sounds clipped |
| Delay compensation | Negative DAW delay or player pre-read | Playing feels loose and fast lines drag |

## Strings and winds are not one job

A string legato is a bow change or a string crossing, and the transition carries bow noise. A wind legato is breath and key work, closer to a pitch connection than a new attack. Put a string script on a flute and the line turns sticky. Brass needs the breath before the note, and a long transition sands off its edge. Ask what the instrument actually does between two pitches.

## When not to script it

On fast repeated notes the script treats every repeat as a transition and smears them; round robin should take over. Leaps beyond an octave often fall outside the recorded intervals, and a small gap beats a forced transition. Delay is the other cost: waiting for a transition can push playback a few milliseconds late, and that latency reaches the fingers in a live take. A script repairs the join, not the phrasing.

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["G3","A3","B3","C4","D4","E4"],"label":"Six notes joined into one line","label_en":"Six notes joined into one line","hint":"Hear the seam between notes, then imagine the script replacing the next attack with a transition","hint_en":"Hear the seam between notes, then imagine the script replacing the next attack with a transition"}
```
:::
