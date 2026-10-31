---
id: midi-quantize-notes
site: prod
cat: B1
title: 录制量化的取舍
title_en: The Cost of Quantizing
summary: 量化修的是时间，代价是演奏的微差；先决定哪里必须对齐。
summary_en: Quantizing fixes timing at the cost of performance nuance, so decide first what must sit on the grid.
level: standard
tags: [MIDI, 量化, 律动, 演奏]
tags_en: [MIDI, quantize, groove, performance]
alias: [量化, 录制量化, 音符量化, 对齐网格, quantize, quantizing]
order: 341
links:
  - "[[glossary:rubato]]"
  - "[[glossary:tempo]]"
  - "[[glossary:velocity]]"
instances:
  - atepp-000004 | 斯克里亚宾《练习曲》Op.8 之十，霍洛维茨的演奏，可听同一动机每次落点的差别 | Scriabin's Etude Op.8 No.10 played by Horowitz, with each return of the motive placed differently
  - atepp-000005 | 同一首的阿什肯纳齐版本，可与前一版对照句尾收束的时间 | The same etude by Ashkenazy, useful for comparing where phrases end
  - atepp-000006 | 同一首的索科洛夫版本，同一和弦在不同演奏者手里落点不同 | A third reading by Sokolov, where the same chords land in different places
sources:
  - Ableton Live Reference Manual, 量化 MIDI 音符与 groove
  - Apple Logic Pro User Guide, 量化与时间校正
  - Steinberg Cubase Operation Manual, 量化面板与迭代量化
updated: 2026-10-31
---

::: zh
一段听起来不齐的钢琴，量化到十六分音符后往往不是齐了，而是死了。

## 先分清不齐的三种来源

不齐有三种：演奏本身的时间差、录音链路的延迟、编辑时误拖的音符。前两种要保留或补偿，第三种才该对齐。把所有音都推到网格上，等于把三种问题当成一种处理。先听一遍，标出哪几拍是真的错，再决定量化范围。

## 网格与强度

网格决定最小单位，强度决定往格子上靠多少。八分网格适合铺底与长音，十六分适合快速音型，三连音段落要用三连音网格。强度不必百分之百：六十到八十之间，听感还在演奏者手里。量化起点之后，音符长度与控制器不会跟着走，踏板的落点要单独检查。

| 素材 | 网格 | 强度 | 备注 |
|---|---|---|---|
| 贝斯与底鼓 | 十六分 | 九十到一百 | 先对齐重音 |
| 节奏吉他 | 十六分 | 七十到八十五 | 保留扫弦先后 |
| 钢琴伴奏 | 八分 | 五十到七十 | 旋律轨不动 |
| 独奏 rubato | 不对齐 | 零 | 只修明显错音 |
| 鼓的轻击 | 十六分三连 | 三十到五十 | 别压成平均 |

## 哪些素材不该硬量化

独奏的 [[glossary:rubato|rubato]]、装饰音、吉他扫弦、竖琴琶音，这些时间差就是表情。把它们对齐，听起来会像自动伴奏。鼓的轻击也一样：轻轻提前的半拍是律动，不是错误。[[glossary:tempo|速度]]自由的段落，网格本身就不成立。

## 保留微差的做法

先复制一轨，再在副本上量化；用强度而不是硬对齐；对手工修过的段落做局部量化，不要全曲套用。需要统一律动时，从一段演奏里提取 groove 再套到别的轨上，比统一网格自然。量化完把副本静音留着，下一次改版还能找回原来的时间。

## 过度量化会坏在哪

十六分网格套在三连音上，会把音移到错误位置；强度拉满后，重音的位置被网格改写，句子没有方向；控制器与音符分开处理，踏板会和手的落点错开。最麻烦的是不可逆：量化后直接保存，原始时间信息就没了。[[glossary:velocity|力度]]可以事后补，时间不行。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","D4","E4","G4","E4"],"label":"一条完全对齐的动机","label_en":"A motive lined up exactly","hint":"这条动机每个音都等距，量化到网格后大致如此；再想演奏里的微小提前与推迟去了哪里","hint_en":"Every note here is evenly spaced, much like a hard-quantized part; then ask where the tiny early and late notes went"}
```
:::

::: en
A piano take that sounds unsteady rarely becomes steady after quantizing to sixteenths; it becomes lifeless.

## Three sources of unsteadiness

Timing can be off for three reasons: the performance itself, latency in the recording chain, or a note dragged by mistake while editing. The first two should be kept or compensated; only the third should be aligned. Pushing every note onto the grid treats all three as one problem. Listen once and mark the beats that are actually wrong before choosing a range.

## Grid and strength

The grid sets the smallest unit, strength sets how far notes move toward it. Eighths suit pads and sustains, sixteenths suit fast figures, and triplet passages need a triplet grid. Strength does not have to be 100 percent; between sixty and eighty the performance still feels played. Quantizing note starts does not move note lengths or controller data, so pedal points need a separate check.

| Material | Grid | Strength | Note |
|---|---|---|---|
| Bass and kick | Sixteenths | 90 to 100 | Align accents first |
| Rhythm guitar | Sixteenths | 70 to 85 | Keep the strum order |
| Piano accompaniment | Eighths | 50 to 70 | Leave the melody alone |
| Rubato solo | None | 0 | Fix only clear mistakes |
| Drum ghost notes | Sixteenth triplets | 30 to 50 | Do not flatten them |

## What not to quantize

Rubato solos, grace notes, guitar strums and harp arpeggios carry expression in their timing. Align them and the result sounds like a backing track. Drum ghost notes work the same way: a touch early is groove, not error. In a passage with free tempo, the grid itself does not apply.

## Keeping the nuance

Duplicate the track and quantize the copy; use strength instead of hard alignment; quantize locally where you edited by hand rather than across the whole song. When a shared feel is needed, extract the groove from one performance and apply it to the others, which sounds more natural than one grid for everything. Mute the copy and keep it, so the next revision can recover the original timing.

## Where over-quantizing breaks

A sixteenth grid over triplets moves notes to the wrong place. Full strength lets the grid rewrite the accents and the phrase loses direction. Treating controllers separately from notes leaves the pedal out of step with the hand. The worst part is that it is irreversible: save after quantizing and the original timing is gone. Velocity can be fixed later; time cannot.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "D4", "E4", "G4", "E4"], "label": "A motive lined up exactly", "label_en": "A motive lined up exactly", "hint": "Every note here is evenly spaced, much like a hard-quantized part; then ask where the tiny early and late notes went", "hint_en": "Every note here is evenly spaced, much like a hard-quantized part; then ask where the tiny early and late notes went"}
```
:::
