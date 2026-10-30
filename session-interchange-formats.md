---
id: session-interchange-formats
site: prod
cat: A1
title: 工程交换格式
title_en: Session Interchange Formats
summary: 换 DAW 或交后期时，能带走的通常只有时间与音量。
summary_en: What survives when a session moves between DAWs, and why positions, levels and fades travel better than plug-ins.
level: standard
tags: [交换格式, 交付, 兼容]
tags_en: [interchange, delivery, compatibility]
alias: [AAF, OMF, 工程交换, session interchange]
links:
  - "[[glossary:daw]]"
  - "[[glossary:stems]]"
  - "[[glossary:automation]]"
instances:
  - pdmx-000600 | 进行曲段落清楚，适合练导出到另一宿主后的对位
  - oga-000004 | 分层战斗曲，适合练跨软件保留片段位置与音量
  - mutopia-000498 | 交响曲慢乐章，适合检查速度图与自动化在交换后是否保留
sources:
  - 交换格式能携带与不能携带的内容，依通行 DAW 文档核查，未抄文本
  - 时间码、帧率与媒体嵌入的交付做法，依影视后期流程通识核查，未抄文本
updated: 2026-10-28
---

::: zh
工程离开原宿主时，能带走的通常只有时间位置与音量。乐器、插件与路由，大多留在原地。

## 问题

合作者用另一款软件，或画面剪辑需要把音乐放进他们的时间线。文件打开了，片段却错位，淡入淡出消失，处理少了一半。只能靠耳朵重建，一天就没了。

## 做法

先定哪些东西必须可改。对方只需要平衡与时值，就给分轨。需要移动片段，就用 AAF、OMF 或 XML 这类交换格式，它带得走片段位置、名称、音量、淡变与基础自动化。乐器与插件处理先并轨，首尾留出余量。

## 参数与判断

对方可能没有你的硬盘时，把媒体嵌入文件；素材很大且共用盘时，用引用。影视方向用 48 kHz、24 bit，确认起始时间码与帧率。导入后检查声像法则与轨道顺序，这两处会悄悄改变平衡。

## 听什么

把导入后的工程与原工程逐组对比。头尾都要查同步，不能只听中段。两条对应分轨做相减测试，是听出交换改了什么的最快办法。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["G3","B3","D4","G4","F4","D4","B3","G3"],"label":"交换前后的一段合奏","label_en":"An ensemble before and after transfer","hint":"听两端是否对齐，中段是否还保持原来的平衡","hint_en":"Hear the alignment at both ends and the balance in between"}
```

## 常见误解

交换文件不是备份，它装不下的东西会直接丢掉。分轨不比工程差，只是承诺不同。导入成功不代表混音还在，只有听能证明。
:::

::: en
When a session leaves its DAW, time and level usually survive. Instruments, plug-ins and routing mostly do not.

## The problem

A collaborator uses another program, or the picture editor needs the music in their timeline. The file opens, but clips have shifted, fades have vanished and half the processing is gone. Rebuilding by ear costs a day.

## The practice

Decide what must remain editable. If the other side only needs balance and timing, deliver stems. If they need to move clips, use an interchange format such as AAF, OMF or XML, which carries positions, names, volume, fades and basic automation. Print instrument and plug-in processing first, and keep handles at both ends.

## Settings and judgement

Embed media when the other side cannot reach your drives, and reference it when files are large and shared. Use 48 kHz and 24 bit for picture work, and confirm the start timecode and frame rate. Check pan law and track order after import, because both can change the balance silently.

## What to listen for

Compare the imported session with the original, group by group. Check sync at the head and at the tail, not only in the middle. A null test between matching stems is the fastest way to hear what the transfer changed.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["G3", "B3", "D4", "G4", "F4", "D4", "B3", "G3"], "label": "An ensemble before and after transfer", "label_en": "An ensemble before and after transfer", "hint": "听两端是否对齐，中段是否还保持原来的平衡", "hint_en": "Hear the alignment at both ends and the balance in between"}
```

## Common misunderstandings

An interchange file is not a backup, because it drops what it cannot represent. Stems are not worse than a session; they are simply a different promise. A successful import does not prove the mix survived, and only listening does.
:::
