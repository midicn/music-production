---
id: sample-library-organization
site: prod
cat: A1
title: 素材与循环库整理
title_en: Organizing Samples and Loops
summary: 素材库的价值不在多少 GB，而在三秒内找得到。
summary_en: A sample library earns its keep through naming, tempo tagging and duplicate control, not through raw file count.
level: standard
tags: [素材, 采样库, 整理]
tags_en: [samples, library, organization]
alias: [素材库, 采样整理, 循环库, sample library]
links:
  - "[[glossary:sampler]]"
  - "[[glossary:tempo]]"
  - "[[glossary:sample-clearance]]"
instances:
  - groove-000000 | 标注速度与拍号的鼓循环，适合练按 BPM 与风格归档
  - groove-000010 | 长循环含多次变奏，适合练重命名与去重
  - oga-000001 | 配乐片段含多段素材，适合练按用途而非来源建目录
sources:
  - 采样库命名、标签与去重的做法；采样管理惯例是主要依据。
  - 授权信息随素材保存的惯例——依据来自采样清权流程惯例。
updated: 2026-10-28
---

::: zh
素材库的价值不在多少 GB，而在三秒内能不能找到对的声音。

## 问题

两百 GB 循环，常用的还是那四条。不同素材包互相重复，文件名里没有速度与调性，试听变成不停滚动。库越收越大，真正能用的部分却没变。

## 做法

先按来源分目录，再按类型分。文件名写清速度、调性与角色，例如 92bpm_Am_hat_groove。只保留一个主库，其它位置引用它。把真正会用的声音收进一份很短的收藏清单，其余大胆删除或归档。

## 参数与判断

单次采样与循环分开标记，因为变速时它们的表现不同。去重按内容哈希，不按文件名。授权与来源说明跟文件放在一起，没有条款的采样迟早是麻烦。试听时对齐响度，否则更响的那条永远赢。

## 听什么

把两个候选对齐到同一响度，问哪个更适合编曲，而不是哪个更响。听起来更好的循环，常常只是更亮或更响。检查循环的首尾，坏的剪辑点会限制它的每一次使用。

```audiolab
{"type":"instrument","drum":"36","synth":"perc","phrase":["36","38","42","36","38","46"],"label":"库里的一条鼓循环","label_en":"One drum loop from the library","hint":"先听首尾能否相接，再想它该用什么名字","hint_en":"Hear whether the ends meet, then decide what to call it"}
```

## 常见误解

素材包越多选择越多，其实只是搜得更久。改名会弄坏旧工程，所以要在导入前改，或用库管理器改。大库不等于归档，没有说明就无法重建。
:::

::: en
A library is measured by how fast you find the right sound, not by how many gigabytes it holds.

## The problem

Two hundred gigabytes of loops, and the same four are used. Packs duplicate each other, tempo and key are missing from filenames, and auditioning becomes scrolling. The collection grows while the usable part stays flat.

## The practice

Organise by source first, then by type. Rename files with tempo, key and role, such as 92bpm_Am_hat_groove. Keep one canonical library and reference everything else from it. Mark a short favourites list for the sounds you actually reach for, and delete or archive the rest without guilt.

## Settings and judgement

Tag one-shots separately from loops, because they behave differently when tempo changes. Deduplicate by content hash rather than by filename. Keep licence and provenance notes beside the files, since a sample without terms is a future problem. Audition at matched loudness, or the louder file will win every comparison.

## What to listen for

Play two candidates at the same level and ask which fits the arrangement, not which sounds bigger. A loop that seems better is often just brighter or louder. Check the loop's tail and start, because a bad edit point limits every use.

```audiolab
{"type": "instrument", "drum": "36", "synth": "perc", "phrase": ["36", "38", "42", "36", "38", "46"], "label": "One drum loop from the library", "label_en": "One drum loop from the library", "hint": "先听首尾能否相接，再想它该用什么名字", "hint_en": "Hear whether the ends meet, then decide what to call it"}
```

## Common misunderstandings

More packs do not mean more options, only more searching. Renaming breaks old projects, so do it before import or through the library manager. A large library is not an archive, and without notes it cannot be rebuilt.
:::
