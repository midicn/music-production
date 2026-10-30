---
id: collaboration-and-handoff
site: prod
cat: A1
title: 协作与工程交付
title_en: Collaboration and Handoff
summary: 把工程交给别人前，先让它能自己说明白。
summary_en: What to freeze, name and write down before another person opens your session, so the handoff survives missing plug-ins.
level: standard
tags: [协作, 交付, 工作流]
tags_en: [collaboration, handoff, workflow]
alias: [工程交付, 协作, 交接, handoff]
links:
  - "[[glossary:daw]]"
  - "[[glossary:stems]]"
  - "[[glossary:plugin]]"
instances:
  - pdmx-000600 | 进行曲编制规整，适合练总谱、分谱与工程说明的对应
  - oga-000004 | 战斗曲分层明确，适合练交付前冻结音源与标注段落
  - groove-000010 | 长循环素材，适合练交接时写清速度、起点与循环次数
sources:
  - 工程交接与并轨、冻结的做法，依通行 DAW 文档核查，未抄文本
  - 分轨与工程说明的交付惯例，依影视与唱片后期流程通识核查，未抄文本
updated: 2026-10-28
---

::: zh
交付不是把工程发过去，而是让对方不必问你，就能打开、听懂并继续做。

## 问题

对方打开工程，插件缺失、采样找不到、速度图对不上，只能在聊天里一句句问。来回几轮，一下午的活拖成一周。

## 做法

先把重的虚拟乐器冻结或并轨成音频，同时保留 MIDI 以便修改。轨道按角色命名，段落用标记写清主歌、副歌与转调。附一页说明，写采样率、速度、拍号、调性、参考曲与关键决定。工程与分轨一起交付，所有分轨从同一零点开始。

## 参数与判断

影视方向用 48 kHz，纯音乐常用 44.1 kHz，位深 24。留 6 dB 余量，不要贴着零。确认并轨后淡变与尾音仍在。插件清单写清哪些必需、哪些只是口味，对方没有的提前换成音频或原厂替代。

## 听什么

在一台只有原厂插件的机器上打开，逐组独奏。听平衡是否还在，标记是否落在正确的小节。若某条轨明显变薄，多半是缺失插件被跳过了。

```audiolab
{"type":"instrument","gm":"Cello","synth":"bowed","phrase":["C3","E3","G3","B3","A3","G3","E3","C3"],"label":"交接后仍要能改的一句","label_en":"A line that must stay editable","hint":"听连奏与尾音，并轨后这些细节应当保留","hint_en":"Hear the legato and tail; printing should keep both"}
```

## 常见误解

分轨不能代替需要继续编辑的工程。只发音频也不更安全，它拿走了改一个音的能力。长消息不是文档，下个月就搜不到。
:::

::: en
Handing off is not sending a project file. It is letting someone else open it, understand it and continue without asking you.

## The problem

The other person opens the session and finds missing plug-ins, missing samples and a misaligned tempo map. Questions arrive one message at a time, and an afternoon stretches into a week.

## The practice

Freeze heavy virtual instruments to audio, but keep the MIDI so edits remain possible. Name tracks by role and mark verse, chorus and key change. Attach a one-page note with sample rate, tempo, meter, key, reference track and the main decisions. Deliver session and stems together, starting from the same zero point.

## Settings and judgement

Use 48 kHz for picture work and 44.1 kHz for music-only projects, at 24 bit. Leave about 6 dB of headroom instead of sitting near zero. Confirm fades and tails survive printing. List which plug-ins are essential and which are taste. For anything they lack, print audio or use stock replacements.

## What to listen for

Open it on a machine with only stock plug-ins and solo each group. Hear whether the balance still holds and whether section markers land on the right bars. If one track is thinner, a missing plug-in was probably skipped.

```audiolab
{"type": "instrument", "gm": "Cello", "synth": "bowed", "phrase": ["C3", "E3", "G3", "B3", "A3", "G3", "E3", "C3"], "label": "A line that must stay editable", "label_en": "A line that must stay editable", "hint": "听连奏与尾音，并轨后这些细节应当保留", "hint_en": "Hear the legato and tail; printing should keep both"}
```

## Common misunderstandings

Stems are not a substitute for a session when the other side must edit. Sending audio only is not safer either; it removes the ability to change a note. A long message is not documentation, because it cannot be searched next month.
:::
