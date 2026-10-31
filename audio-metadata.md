---
id: audio-metadata
site: prod
cat: B5
title: 音频元数据
title_en: Audio Metadata
summary: 曲名、作曲家与作品号写错，检索和归档立刻失效。
summary_en: A wrong title, composer or work number breaks search and archiving immediately.
level: standard
tags: [元数据, 标签, 归档, 检索]
tags_en: [metadata, tags, archiving, search]
alias: [元数据, 标签, ID3, Vorbis comment, metadata]
links:
  - "[[glossary:opus]]"
  - "[[glossary:daw]]"
instances:
  - mutopia-000178 | 曲名、作曲家与 BWV 编号齐全，标签缺失时这条就退化成无名的托卡塔（C1）
  - thesession-000083 | 传统曲调只有曲名与体裁，没有作曲家，元数据字段的空白也要如实保留（C1）
  - atepp-000195 | 演奏版带作品名与乐章号，正是标签该承载的三层信息（C1）
sources:
  - ID3v2、Vorbis comment 与 MP4 原子的字段结构，对照公开规范整理。
  - 归档元数据的最小字段集（档案与图书馆惯例）。
updated: 2026-10-28
---

::: zh
## 问题

音频文件除了声音，还带曲名、作曲家、专辑、音轨号与封面。标签写错或缺失，检索、归档与随机播放都会跟着乱。

## 原理

不同格式用不同的标签块。WAV 用 LIST 与 INFO 块，AIFF 用文本块，FLAC 用 Vorbis comment，MP3 用 ID3v2，MP4 用 iTunes 风格的原子。常见字段包括曲名、艺术家、专辑、音轨号、年份、版权与封面。格式转换时字段名对不上就会丢，中文还涉及编码。

## 参数与做法

先统一口径，艺术家一栏写作曲家还是演奏者，全库保持一致。作品号写进专辑或注释，避免塞进曲名。批量修改前备份。用支持 Unicode 的工具，转换后抽查中文与封面。

## 听什么

这一条听的不是声音，而是能否找到。随机播放时看标签能否让曲目可辨，同一作品的不同版本能否靠标签区分。在巴赫托卡塔、里尔舞曲与《月光》之间切换，看作曲家、体裁与乐章号是否各就各位。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5"],"label":"一段可命名的动机","label_en":"A motif that can be named","hint":"想象它被存成十个文件，标签决定你还能不能找回这一段","hint_en":"Imagine it saved as ten files, where tags decide whether you find this one again"}
```

## 常见误解

文件名就是标签，换设备后文件名往往不作数。标签不影响音质所以不重要，它决定的是能否被检索。转格式标签一定保留，实际常丢。封面只是装饰，缺封面会让归档难以辨认。
:::

::: en
## The question

An audio file carries more than sound: title, composer, album, track and cover. Wrong or missing tags scramble search, archiving and shuffle.

## How it works

Formats use different tag blocks. WAV uses LIST and INFO chunks, AIFF text chunks, FLAC Vorbis comments, MP3 ID3v2, and MP4 iTunes-style atoms. Common fields include title, artist, album, track number, year, copyright and cover. Field names differ across formats, so conversion loses data, and Chinese adds encoding issues.

## Settings and practice

Decide first whether artist means composer or performer, and keep it consistent. Put work numbers in album or comment, not the title. Back up before batch edits. Use a Unicode-aware tool and spot-check Chinese text and covers after conversion.

## What to listen for

This entry is about finding, not hearing. In shuffle, see whether tags identify the track, and whether versions of one work stay distinct. Switch between a Bach toccata, a reel and Clair de lune, and check that composer, genre and movement each sit in the right field.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "E4", "G4", "C5"], "label": "A motif that can be named", "label_en": "A motif that can be named", "hint": "想象它被存成十个文件，标签决定你还能不能找回这一段", "hint_en": "Imagine it saved as ten files, where tags decide whether you find this one again"}
```

## Common misconceptions

The file name is not the tag, and it often does not travel. Tags do affect whether music is found, even if not the sound. Conversion does not always keep tags. Cover art is not decoration; it helps identify an archive.
:::
