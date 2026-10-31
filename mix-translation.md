---
id: mix-translation
site: prod
cat: A6
order: 430
title: 混音翻译：手机/车/耳机/音箱的一致性
title_en: Mix Translation Across Phones, Cars, Headphones and Speakers
summary: 翻译的目标是让关键信息在每套系统上都保得住，音色差异可以接受。
summary_en: Translation keeps the key information intact on every system; differences in tone are acceptable.
level: standard
tags: [混音, 翻译, 监听, 系统]
tags_en: [mixing, translation, monitoring, playback]
alias: [混音翻译, 多系统检查, mix translation, translation check]
links:
  - "[[glossary:monitoring]]"
  - "[[glossary:reference-track]]"
  - "[[glossary:lufs]]"
  - "[[glossary:nearfield-monitor]]"
instances:
  - groove-000002 | 灵魂乐鼓循环低频饱满，手机外放与车里差得最明显
  - oga-000002 | 场景曲层数多，小音箱上先消失的往往是中低层
  - openscore-000008 | 钢琴与人声同场，手机外放下歌词是否被伴奏盖住一听便知
sources:
  - Bob Katz, Mastering Audio：The Art and the Science（Focal Press）监听与多系统重放章节
  - Bobby Owsinski, The Mixing Engineer's Handbook（Cengage）监听与参考曲章节
  - Gary Davis and Ralph Jones, Sound Reinforcement Handbook（Hal Leonard）重放系统与房间相互作用章节
updated: 2026-10-31
---

::: zh
## 先定不能丢的东西

一首歌换四套系统，音色一定会变，能守住的只有优先级。先写下三件事：主唱每个字是否可懂、底鼓与贝斯的起音是否同时到达、副歌是否比主歌更有推力。三件事在手机、车、耳机、音箱上都成立，才算翻译过关。音色偏亮或偏暗只是口味，不必强求一致。

## 四套系统各听什么

| 系统 | 最容易暴露 | 先动哪里 |
|---|---|---|
| 手机外放 | 中频拥挤、极低频消失 | 人声 2–4 kHz 的掩蔽，伴奏让出中频 |
| 耳机 | 齿音、混响尾巴、声部过宽 | 去齿音，收窄双耳差异 |
| 车里 | 60–120 Hz 轰鸣、低频掩蔽 | 贝斯与底鼓的高通和音量，而非加低频 |
| 近场音箱 | 相位、声场中心、低频对齐 | 单声道检查与摆位，再回工程 |

手机外放几乎放不出 60 Hz 以下，车里又把它放大。同一套低频在两边都“对”，通常意味着一处被牺牲。

## 回工程怎么改

每轮只改一类问题，导出后把响度对齐再比较。先减后加：中频挤就先让伴奏让位，不要直接推人声；低频轰就先切高通，不要靠限制器压。改动超过两处，听感已经无法归因。参考曲只用来校准低频量与亮度，不照搬音色。隔一天再听，确认改的是问题，不是昨晚的情绪。

## 什么时候停

四套系统里三套通过、剩下一套只差音色，可以交付。若只有一套失败，先确认那套是否代表听众：手机外放的小音量、车里的路噪、耳机的佩戴泄漏，都会改变判断。为了手机补超低频，只会让其他系统过载。翻译的终点是优先级仍在，而不是每套系统都一样。

```audiolab
{"type":"instrument","gm":"Electric Bass (finger)","synth":"plucked","phrase":["E1","G1","A1","C2"],"label":"低音线在手机与车里的差别","label_en":"A bass line heard on a phone and in a car","hint":"先在手机外放听一遍，再换耳机；注意哪几个音只剩点击声","hint_en":"Play it on a phone speaker, then on headphones; notice which notes survive only as a click"}
```
:::

::: en
## Decide what cannot disappear

Across four systems the timbre will change. Only priorities can be protected. Write down three: every lyric word stays intelligible, kick and bass arrive together, the chorus pushes harder than the verse. A mix translates when those three survive on a phone, in a car, on headphones and on speakers. A little extra brightness or darkness is taste, not failure.

## What each system reveals

| System | Usually exposed | First move |
|---|---|---|
| Phone speaker | crowded mids, no deep bass | clear 2–4 kHz masking, let the backing leave the centre |
| Headphones | sibilance, reverb tails, wide parts | de-ess, narrow the side difference |
| Car | 60–120 Hz boom, bass masking | high-pass and balance bass against kick, not more low end |
| Nearfield speakers | phase, centre image, low-end alignment | mono check and placement before processing |

A phone cannot reproduce below 60 Hz; a car can exaggerate it. If the same low end works in both, something else was probably sacrificed.

## Fix in the session

Change one class of problem per pass. Match loudness before comparing exports. Subtract first: if the mids are crowded, move the backing rather than pushing the vocal; if the low end booms, high-pass before reaching for a limiter. More than two changes at once and you cannot tell what caused the result. Use a reference for low-end weight and brightness, not for timbre. Listen again the next day and confirm you fixed a problem, not last night's mood.

## When to stop

Three systems passing and the fourth differing only in tone is enough to deliver. If one system fails alone, ask whether it represents the audience: phone volume, road noise and headphone leakage all change judgement. Adding sub-bass for a phone overloads everything else. Translation ends with the priorities intact, not with four identical systems.

```audiolab
{"type": "instrument", "gm": "Electric Bass (finger)", "synth": "plucked", "phrase": ["E1", "G1", "A1", "C2"], "label": "A bass line heard on a phone and in a car", "label_en": "A bass line heard on a phone and in a car", "hint": "Play it on a phone speaker, then on headphones; notice which notes survive only as a click", "hint_en": "Play it on a phone speaker, then on headphones; notice which notes survive only as a click"}
```
:::
