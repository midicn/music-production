---
id: mix-revision
site: prod
cat: A6
order: 436
title: 混音修改：客户意见怎么落到工程
title_en: Mix Revisions: Turning Notes into Session Changes
summary: 每条意见先变成时间点、动作和验收句，再决定改不改。
summary_en: Turn each note into a time, an action and an acceptance line before touching the session.
level: standard
tags: [混音, 修改, 客户, 版本]
tags_en: [mixing, revision, client, versioning]
alias: [混音修改, 改混音, mix revision, mix notes]
links:
  - "[[glossary:reference-track]]"
  - "[[glossary:mixdown]]"
  - "[[glossary:stems]]"
  - "[[glossary:automation]]"
instances:
  - pdmx-000450 | 《德意志安魂曲》段落多、时间长，修改最容易漏掉后面的对应段
  - musicnet-000097 | 四重奏乐章结构清楚，适合用段落标记定位客户说的第二段
  - oga-000011 | 首领曲循环层多，客户说太满时可以先从删层试
sources:
  - Bobby Owsinski, The Mixing Engineer's Handbook（Cengage）修订与客户沟通章节
  - Avid, Pro Tools Reference Guide 中 playlists、markers 与 comments 章节
  - Apple, Logic Pro User Guide 中 alternatives 与 project versions 章节
updated: 2026-10-31
---

::: zh
## 把话变成工程语言

“人声再暖一点”不是指令。要问清三样：时间点、参考、可接受的边界。暖可以指 200 Hz 多一点、齿音少一点、混响短一点，也可以是失真。几种做法差别很大。收到意见先复述一遍，让对方确认你理解的是同一件事；确认不了，就做两版对照，不要在一版里猜。

## 修改单

| 意见 | 落点 | 先查 | 验收 |
|---|---|---|---|
| 人声太干 | 发送量与预延迟 | 干湿比、句尾 | 尾音自然进入伴奏 |
| 鼓不够硬 | 总线启动时间与饱和 | 瞬态、极性 | 小音量下仍有冲击 |
| 低频太多 | 贝斯与底鼓的 60–120 Hz | 掩蔽、单声道 | 手机不轰，车里不浑 |
| 整体太满 | 编曲层与中频 | 2–5 kHz 堆积 | 主次仍分得开 |

每行都要落到轨、参数、幅度和一句可验收的话。写不清的意见，先不做。

## 一轮怎么走

冻结当前版本，复制工程再动手。按时间点逐条改，只改本轮修改单里的内容，顺手发现的毛病记到下一轮。导出时保持同一响度，A/B 时对齐电平，否则更响的一版总被当成更好。发回时附一份改动记录：改了什么、没改什么、为什么。客户确认后再进入下一轮。

## 版本与交付

文件名带版本号与日期，工程内用快照或另存，别覆盖上一版。修改单、参考曲、导出文件放在同一文件夹。定稿后导出分轨与纯伴奏，写清采样率、位深和总线处理。被否掉的版本保留到项目结束，客户改口时能找回来。

## 不该照做的时候

意见若会破坏可懂度、超出交付规格，或只基于手机外放，先说明代价再给替代方案。用对齐响度的对照让对方听差别，比争论形容词有效。客户坚持时照做并记录，但不要把责任写进工程名。合同里写清修改轮次，超出部分另计。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","B4","G4","E4"],"label":"同一句，改前与改后","label_en":"The same phrase before and after a revision","hint":"对齐响度再切换，听改的是音色还是电平","hint_en":"Match loudness before switching; hear whether tone or level moved"}
```
:::

::: en
## Turn words into session language

"Warmer vocal" is not an instruction. Ask for three things: a time, a reference and an acceptable boundary. Warm can mean more 200 Hz, less sibilance, a shorter reverb or added distortion, and those are very different moves. Repeat the note back until the client confirms you mean the same thing; if that fails, make two versions instead of guessing inside one.

## The revision sheet

| Note | Lands on | Check first | Acceptance |
|---|---|---|---|
| Vocal too dry | send level and pre-delay | wet/dry, line endings | tails enter the backing naturally |
| Drums not hard enough | bus attack and saturation | transients, polarity | impact remains at low volume |
| Too much low end | bass and kick at 60–120 Hz | masking, mono | no boom on a phone, no mud in a car |
| Overall too full | arrangement layers and mids | 2–5 kHz build-up | hierarchy still reads |

Every row must land on a track, a parameter, an amount and one acceptance sentence. If a note cannot be written that way, do not start.

## Run one round

Freeze the current version and duplicate the session before touching it. Work through the timecodes and change only what is on this round's list; log anything else for the next round. Export at the same loudness and match levels for A/B, or the louder version will always win. Send a change log: what changed, what did not, and why. Start the next round only after approval.

## Versions and delivery

Put version and date in the file name, and use snapshots or Save As inside the session rather than overwriting. Keep notes, references and exports in one folder. After approval, export stems and an instrumental, with sample rate, bit depth and bus processing written down. Keep rejected versions until the project closes so a changed mind can be answered.

## When not to comply

If a note hurts intelligibility, breaks the delivery spec or comes only from a phone speaker, explain the cost and offer an alternative. A matched-loudness comparison settles arguments faster than adjectives. If the client insists, do it and document it, but do not put blame in the file name. State the number of revision rounds in the contract and price the rest.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "E4", "G4", "B4", "G4", "E4"], "label": "The same phrase before and after a revision", "label_en": "The same phrase before and after a revision", "hint": "Match loudness before switching; hear whether tone or level moved", "hint_en": "Match loudness before switching; hear whether tone or level moved"}
```
:::
