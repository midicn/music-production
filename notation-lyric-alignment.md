---
id: notation-lyric-alignment
site: prod
cat: B6
title: 歌词对齐
title_en: Lyric Alignment
summary: 歌词对不齐，多半是音节数没数清，不是音高写错。
summary_en: When lyrics drift out of place, the syllable count is usually wrong, not the pitches.
level: standard
tags: [记谱, 歌词, 音节, 校对]
tags_en: [notation, lyrics, syllables, proofing]
alias: [歌词对齐, 歌词对位, 音节对齐, lyric alignment, lyric setting]
order: 512
links:
  - "[[glossary:lied]]"
  - "[[glossary:strophic-form]]"
  - "[[glossary:slur]]"
  - "[[glossary:tie]]"
instances:
  - mutopia-001432 | 舒伯特《野玫瑰》声乐轨 180 个音符，三段歌词共用同一条旋律，每段都要塞进同一串音 | Schubert's Heidenröslein fits 180 vocal notes and three stanzas to one melody
  - mutopia-001435 | 《魔王》四个角色共用一条声乐轨，337 个音符装完整首诗，轨内还换过几次音色 | Erlkönig runs four characters on one vocal track, 337 notes for the whole ballad, with timbre changes inside
  - cyberhymnal-000623 | 赞美诗《Abide with Me》旋律轨 148 个音符，会众多节歌词逐节对同一条旋律 | The hymn Abide with Me, 148 notes in the melody line, several stanzas fitted to the same tune
sources:
  - Dorico 官方文档的歌词章节，音节输入、连字符与延长线
  - Sibelius 官方文档的歌词与分节歌设置
  - Elaine Gould, Behind Bars, Faber Music，歌词与音节对齐的通行规范
updated: 2026-10-31
---

::: zh
歌词对不上，多半不是音高错了，而是音节没数清：一个音节跨五个音，谱上只画一条连线，歌手会把下一个字提前唱出来。

## 先切音节

中文一字一个音节，英文按元音切，复合词照词典断。花腔与拖腔是一个音节跨几个音，音符之间要连线，歌词只写一次，后面接延长线。衬词照实写，别留空位让人猜。切开之后先数每句的音节数，再数旋律上的音符数，差两个就顺着乐句找那两个音。

## 三种情形

中文以一字一音为主，拖腔时才出现一字多音；英文赞美诗的一音多字多出现在缩写与快句里。三种情形的写法不同，混用会让谱面自相矛盾。

| 情形 | 谱面写法 | 常出的错 |
|---|---|---|
| 一音一字 | 音节之间加连字符，词尾不加 | 连字符画成破折号，或每字都加 |
| 一音多字 | 两个音节共用一个音符，用连字符或空格分开 | 第二个字被挤到下一个音 |
| 一字多音 | 音符之间加连线，歌词写一次，后面加延长线 | 延长线太短，被读成休止 |

## 改谱之后

多数软件里歌词附着在音符上，中间插一个音，后面的音节整体后移，甚至跳进下一小节。改完旋律要重新核对每一段的归属，反复段落尤其要问：第二遍唱同样的词，还是跳回第一段。分节歌按编号排列，各节音节数不一致时逐节校。MusicXML 会保留音节、连字符与延长线，转成 MIDI 全丢，校对只能在谱上看。

## 哪里会坏

中文按拼音断词、英文断在词中间，翻页处最容易被切坏；一个音节跨系统换行，连字符会落到下一行开头。声部交叉时歌词容易挂错行。谱面音节数对得上，唱出来仍可能挤，因为音符时值太短、气口不够，这时该改节奏而不是改词。译词音节数变化大，硬套原旋律就会吞字。

```audiolab
{"type":"instrument","gm":"Choir Aahs","synth":"vocal","phrase":["G4","A4","B4","A4","G4"],"label":"五个音唱同一个音节，中间不能换字","label_en":"Five notes on one syllable, with no new word in between","hint":"听这串音的走向，再想每个音下面都写一个字会挤成什么样","hint_en":"Follow the line, then imagine a separate syllable printed under every note"}
```
:::

::: en
Lyrics drift out of place for a reason that is rarely pitch: the syllable count is wrong. One syllable stretched over five notes, one slur drawn on the page, and the singer arrives at the next word early.

## Count syllables first

Chinese gives one syllable per character. English divides at vowels, and compounds follow the dictionary. Coloratura and drawn-out phrases put several notes on a single syllable: tie the notes, print the word once, then add an extension line. Write filler syllables as they are sung instead of leaving a gap for someone to guess. After dividing, count each phrase against the notes in the melody; a difference of two points to the notes worth inspecting.

## Three cases

Chinese song mostly sets one note per character, with melisma in drawn-out phrases; English hymns put two syllables on one note in abbreviations and fast lines. Each case is written differently, and mixing them makes the page contradict itself.

| Case | How it is written | Usual fault |
|---|---|---|
| One note, one syllable | Hyphen between syllables, none at word end | Hyphen drawn as a dash, or after every character |
| Two syllables, one note | Both share a note, split by hyphen or space | The second syllable slides to the next note |
| One syllable, many notes | Ties between notes, word printed once, extension after | Extension too short and read as a rest |

## After the melody moves

In most programs lyrics attach to notes. Insert one note and every later syllable shifts, sometimes into the next bar. Recheck ownership after each melodic edit, and in repeated sections ask whether the second pass repeats the words or jumps back to the first stanza. Number the stanzas and proof each one wherever syllable counts differ. MusicXML keeps syllables, hyphens and extensions; MIDI keeps none of them, so proofing happens on the page.

## Where it breaks

Words split by pinyin in Chinese and mid-word in English break worst at page turns; a syllable crossing a system break can leave its hyphen at the start of the next line. When voices cross, text attaches to the wrong line. A page can count correctly and still sing badly because the note values leave no room to breathe; fix the rhythm, not the words. Translated stanzas rarely match the original count, and forcing them swallows syllables.

```audiolab
{"type": "instrument", "gm": "Choir Aahs", "synth": "vocal", "phrase": ["G4", "A4", "B4", "A4", "G4"], "label": "Five notes on one syllable, with no new word in between", "label_en": "Five notes on one syllable, with no new word in between", "hint": "Follow the line, then imagine a separate syllable printed under every note", "hint_en": "Follow the line, then imagine a separate syllable printed under every note"}
```
:::
