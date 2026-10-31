---
id: groove-template
site: prod
cat: B2
order: 372
title: 律动模板
title_en: Groove Templates
summary: 模板存的是推后与提前的毫秒差，不是那串音符
summary_en: A groove template stores the milliseconds of push and lag, not the note pattern.
level: standard
tags: [律动, 模板, 摇摆, 时值, 力度]
tags_en: [groove, template, swing, timing, velocity]
alias: [律动模板, 节奏模板, 手感模板, groove template, groove pool]
links:
  - "[[glossary:velocity]]"
  - "[[glossary:beat]]"
  - "[[glossary:tempo]]"
  - "[[glossary:agogic-accent]]"
instances:
  - groove-000010 | 80 BPM 放克，底鼓与军鼓的落点差异就是可以存下来的手感（C1）
  - groove-000002 | 86 BPM 的灵魂乐循环，适合做“松”模板的参照（C1）
  - groove-000005 | 87 BPM 的嘻哈循环，适合检验十六分摇摆要留多少（C1）
  - groove-000494 | 124 BPM 爵士摇摆，三连音网格的落差是模板的核心参数（C1）
sources:
  - Ableton Live 用户手册，Groove Pool 与 warp 标记（厂商文档）
  - Magenta, Groove MIDI Dataset 数据说明（公开数据集文档）
  - Bernard Purdie 关于 half-time shuffle 的公开访谈
updated: 2026-10-31
---

::: zh
## 模板存的不是音符

同一段鼓，换一个人打，音符位置差不多，听感差很远。差在十六分音符的第二下推了多少、军鼓落在拍后几毫秒、踩镲的力度曲线。模板存的是这些偏差，不是那一串音符；把音符存下来，只是存了一个循环。

## 该记录的几个量

| 项目 | 常见范围 | 作用 |
|---|---|---|
| 十六分摇摆 | 54–62% | 决定“直”还是“摆” |
| 底鼓提前 | 5–15 毫秒 | 让低频先到，听感更稳 |
| 军鼓滞后 | 10–25 毫秒 | 制造“拖”的后拍 |
| 力度范围 | 40–110 | 决定动态与呼吸 |
| 音符长度 | 踩镲 30–80 毫秒 | 决定干湿与密度 |

数字只是起点，真正的模板要按曲子的速度与编制微调。速度越快，同样的毫秒差在听感上越小。

## 从一段录音里提取，再按速度缩放

选一段演奏最稳的八小节，把瞬态对齐到网格，量出每一拍的偏差，取平均。只取一段会过拟合：同一套鼓的四个段落，偏差可能不一样。做两三个变体，分别对应“紧”“松”“拖”，比做一个万能模板有用。

模板跟着速度走时，毫秒差要按比例缩放，否则慢歌会显得太拖、快歌又太死。换编制也要改：模板里有房间话筒的尾巴，换成采样鼓时那条尾巴可能不存在。模板是起点，不是终点；先用它把骨架摆好，再按曲子改。

## 模板不该做什么

模板不能替代编曲。段落没有起伏、贝斯和底鼓撞在一起，再好的律动模板也救不了。也别把别人的手感整套搬过来：模板里应该有你自己的取舍，否则每首歌都会像同一个 session 的复制品。

```audiolab
{"type":"instrument","gm":"Woodblock","synth":"perc","phrase":["C5","C5","C5","C5","C5","C5","C5","C5"],"label":"八下均匀的落点","label_en":"Eight evenly spaced hits","hint":"先听这八下均匀的样子，再想第 2、4、6、8 下往后推一点会变成什么","hint_en":"Hear the even eighths, then imagine pushing hits 2, 4, 6 and 8 slightly late"}
```
:::

::: en
## A template is not a note pattern

Hand the same beat to another drummer and the notes land in nearly the same places, yet it sounds like a different record. What changes is how far the second sixteenth is pushed, how many milliseconds the snare sits behind the beat, how the hi-hat velocities curve. A template stores those deviations, not the pattern; saving the notes only saves a loop.

## What to measure

| Item | Usual range | What it does |
|---|---|---|
| Sixteenth swing | 54–62% | Sets straight versus swung |
| Kick ahead | 5–15 ms | Low end arrives first, feels steadier |
| Snare behind | 10–25 ms | Creates the laid-back backbeat |
| Velocity range | 40–110 | Controls dynamics and breath |
| Note length | Hi-hat 30–80 ms | Controls dryness and density |

These numbers are starting points. A real template is tuned to the tempo and instrumentation of the song; the faster the music, the less the same millisecond gap is perceived.

## Extracting one, then scaling it to tempo

Pick the steadiest eight bars, align the transients to the grid, measure the deviation on each beat and average. One section overfits: the four sections of a single drum take may not share the same feel. Make two or three variants, one tight, one loose, one behind, rather than one universal template.

When the template follows tempo, the millisecond offsets need to scale, or slow songs drag and fast songs stiffen. A change of instrumentation matters too: a template built around room-mic tails may lose those tails when the kit becomes samples. A template is a starting point; set the skeleton with it, then adjust to the song.

## What a template must not do

It cannot replace arrangement. If the sections have no shape and the bass collides with the kick, no groove template rescues the track. Nor should you import someone else's feel wholesale; the template should contain your own choices, or every song turns into a copy of the same session.
:::
