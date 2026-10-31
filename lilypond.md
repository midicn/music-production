---
id: lilypond
site: prod
cat: B6
title: LilyPond 文本记谱
title_en: LilyPond and Text-Based Notation
summary: 乐谱写成纯文本，改一行重排整份，代价是看不见版面。
summary_en: A score kept as plain text rebuilds the whole page from one edit, at the cost of not seeing it while you type.
level: standard
tags: [记谱, LilyPond, 纯文本, 排版]
tags_en: [notation, LilyPond, plain text, engraving]
alias: [LilyPond, 文本记谱, 代码记谱, lilypond, text notation]
order: 511
links:
  - "[[glossary:score]]"
  - "[[glossary:midi-protocol]]"
  - "[[glossary:tablature]]"
instances:
  - mutopia-000042 | 众赞歌三条音乐轨的轨名还留着 \new 字样，能看出文本谱表怎样直接变成 MIDI 轨 | Three music tracks still carry the word \new in their names, showing how staves become MIDI tracks
  - mutopia-001435 | 《魔王》的声乐与钢琴上下谱表各占一轨，轨名 up 与 down 来自同一声部组的上下两行 | Erlkönig puts the voice and the two piano staves on separate tracks, named up and down from one staff group
  - mutopia-000497 | 贝多芬第五第一乐章，12 条轨按 one 到 twelve 命名，木管、圆号与弦乐各占一行 | Beethoven's Fifth, first movement, twelve tracks named one through twelve, each wind, horn and string line kept apart
sources:
  - LilyPond 官方 Notation Reference，音乐变量、谱表装配与版面设置章节
  - Mutopia Project 的公开乐谱源文件，LilyPond 源与导出 MIDI 可对照
  - Elaine Gould, Behind Bars, Faber Music，总谱与分谱排版的一般规范
updated: 2026-10-31
---

::: zh
四重奏分谱要改三个音，图形界面里得点开三个窗口；源文件里改三行，重跑一次，整份版面按新内容重排。

## 文本换来的三件事

乐谱存成纯文本，第一件事是差异看得见：改了哪个音、动了哪条连线，版本记录逐行列出。第二件事是复用：主题写成变量，三个乐章引用同一个定义，改一处全跟着变。第三件事是批量：一套模板配不同参数，几十份分谱一次生成。代价同样具体，版面要编译后才看得到，少一个括号就要从报错行往回找。

## 一个文件分几层

写顺手的文件通常分四层：版本与纸张、音乐变量、谱表与歌词的装配、输出块。变量只放音高与节奏，装配层决定它落到哪张谱表、配哪段歌词，输出层分别生成版面与音频。层分清楚，改音高就不会牵动排版参数。

| 层 | 典型写法 | 改动之后 |
|---|---|---|
| 版本与纸张 | `\version`、`\paper`、全局谱表字号 | 全文字号、页边与谱表间距 |
| 音乐变量 | `music = \relative c' { … }` | 所有引用处一起变 |
| 装配 | `\new Staff`、`\new Lyrics \lyricsto` | 谱表数、声部与歌词归属 |
| 输出 | `\layout`、`\midi` | PDF 版面与音频文件 |

## 编译这一关

写完运行 lilypond 加文件名，得到 PDF 和一份日志。日志里最有用的是小节校验：每小节末尾写一条竖线，时值与拍号对不上就报出行号。未定义的变量、超出谱表的加线与缺失字体也在这里出现。升级版本时先用 convert-ly 改语法，再逐段比对输出，别一次把整份改完。

## 分谱与批量

总谱与分谱可出自同一个文件：给段落打标签，导出时按标签保留需要的声部。分谱的谱号、移调与换页单独设置，总谱版面不会替它适配。批量生成时把调性、速度、标题抽成参数，模板里只留结构；出错先查参数表再查模板。

## 哪里会坏

版面由算法决定，特殊间距要一层层覆盖参数，覆盖越多越脆，换个版本就可能全乱。大总谱编译要等，改一个音也重跑整份。协作者只读谱不读代码，改稿要经手会写文件的人。微分音、图形谱与部分民族记谱要靠额外宏包或手绘。导出的 MIDI 只是附带产物，连奏与力度记号表达有限，别拿它当演奏参考。

```audiolab
{"type":"instrument","gm":"Church Organ","synth":"reed","phrase":["C4","E4","G4","E4","C4","E4","G4","E4"],"label":"同一段音乐写进变量，重复时一个音都不差","label_en":"One passage stored as a variable, repeated note for note","hint":"听第二遍是否与第一遍完全相同，再想图形界面里要复制几次","hint_en":"Hear whether the second pass matches the first, then count the copying a GUI would need"}
```
:::

::: en
Three notes change in a quartet part. A graphical editor means opening three windows; a text file means editing three lines, compiling once, and letting the page reflow around the new content.

## What text buys you

Keep a score as plain text and changes become visible line by line: which pitch moved, which slur was cut, who made the edit. Material can be defined once as a variable and cited in three movements, so one fix propagates everywhere. Templates with different parameters produce dozens of parts in a single pass. The price is concrete: layout exists only after compilation, and one missing brace sends you hunting back from an error line.

## Layers inside one file

A workable file separates four layers: version and paper, music variables, the assembly of staves and lyrics, and the output blocks. Variables hold pitch and rhythm; assembly decides which staff receives them and which text sits underneath; output produces page and sound separately. Keep the layers apart and a pitch fix never disturbs spacing.

| Layer | Typical syntax | What changes downstream |
|---|---|---|
| Version and paper | `\version`, `\paper`, global staff size | Type size, margins, staff spacing |
| Music variables | `music = \relative c' { … }` | Every place that cites it |
| Assembly | `\new Staff`, `\new Lyrics \lyricsto` | Staff count, voice and text ownership |
| Output | `\layout`, `\midi` | PDF layout and audio |

## Passing the compiler

Run lilypond on the file and you get a PDF plus a log. The most useful lines are bar checks: place a bar line at every measure and a duration that disagrees with the metre is reported with a line number. Undefined variables, ledger lines far outside the staff and missing fonts surface in the same place. Before a version upgrade, run convert-ly over the syntax, then compare output passage by passage rather than converting everything at once.

## Parts and batches

Score and parts can come from one source: tag each passage, keep only the staves a player needs at export. Clefs, transposition and page turns in parts need their own settings; the score layout will not adapt for them. For batch work, pull key, tempo and title out as parameters and leave structure in the template. When something breaks, check the parameter table before the template.

## Where it breaks

Layout is algorithmic. Special spacing needs override after override, and a tall stack of overrides is brittle across versions. A large score takes time to compile, and one pitch change rebuilds the whole file. Collaborators who read music but not code cannot edit directly. Microtones, graphic scores and some regional systems need extra packages or hand drawing. Exported MIDI is a by-product: slurs and dynamic marks survive poorly, so do not treat it as a performance reference.

```audiolab
{"type": "instrument", "gm": "Church Organ", "synth": "reed", "phrase": ["C4", "E4", "G4", "E4", "C4", "E4", "G4", "E4"], "label": "One passage stored as a variable, repeated note for note", "label_en": "One passage stored as a variable, repeated note for note", "hint": "Hear whether the second pass matches the first, then count the copying a GUI would need", "hint_en": "Hear whether the second pass matches the first, then count the copying a GUI would need"}
```
:::
