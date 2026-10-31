---
id: sidechain-compression
site: prod
cat: A6
title: 侧链压缩
title_en: Sidechain Compression
summary: 让一条声部在另一条出现时自动后退，关键在于时机与幅度。
summary_en: One part steps back when another appears, and timing plus amount matter more than the ratio.
level: standard
tags: [混音, 侧链, 压缩, 律动]
tags_en: [mixing, sidechain, compression, groove]
alias: [侧链, 侧链压缩, 泵感, sidechain, pumping]
links:
  - "[[glossary:sidechain]]"
  - "[[glossary:compressor]]"
  - "[[glossary:bus]]"
  - "[[instrument:drum-kit]]"
instances:
  - groove-001103 | 四拍底鼓间隔均匀，侧链泵感最容易听
  - oga-000002 | 鼓与合成贝斯并置，侧链让位是否自然一听便知
  - groove-000006 | 流行鼓组密集，检查侧链释放是否拖慢律动
sources:
  - Giannoulis, Massberg and Reiss, Digital Dynamic Range Compressor Design, JAES 2012 — background checked, not quoted
  - Bobby Owsinski, The Mixing Engineer's Handbook, sidechain section — background checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

侧链常被当成舞曲的泵感开关。它真正的作用，是让一条声部在另一条出现时自动让位。

## 目标与判断

先确定谁触发、谁让位、让多少。底鼓触发贝斯是最常见的组合，人声触发铺底也有效。判断标准是让位发生在需要的那几毫秒，而不是整段都在抖。释放太长会拖慢律动，太短会产生点击。

## 做法

把底鼓送进侧链输入，阈值设到只有底鼓能触发；比率二比一到四比一；启动一到十毫秒；释放跟随速度，约八十到二百毫秒。用增益衰减表确认每次只减三到六分贝。需要更自然的让位时，改用动态均衡或音量自动化。旁通时对比整段，而不是只看表。

## 听什么

听贝斯在底鼓之后是否迅速回来；听泵感是否与拍点一致；把侧链旁通，听低频是否立刻变浑；在副歌最密处检查是否过度抽吸。

```audiolab
{"type":"instrument","gm":"Synth Bass 1","synth":"plucked","phrase":["E1","E1","G1","E1"],"label":"合成贝斯","label_en":"Synth bass","hint":"先听贝斯，再让底鼓触发侧链","hint_en":"Hear the bass, then let the kick trigger the sidechain"}
```

## 常见误解

以为侧链只属于舞曲；以为释放越短越紧；以为侧链能替代编曲上的让位。
:::

::: en
## The problem

Sidechain is often treated as a pump switch for dance music. Its real job is to make one part step back when another appears.

## Goal and judgement

Decide who triggers, who moves, and by how much. Kick triggering bass is the common pair; vocal triggering a pad also works. The move should happen for the few milliseconds needed, not for the whole bar. Too long a release drags the groove; too short a release clicks.

## Method

Send the kick to the sidechain input and set the threshold so only the kick triggers. Try 2 to 1 up to 4 to 1, attack 1 to 10 ms, release around 80 to 200 ms following the tempo. Check the gain-reduction meter for 3 to 6 dB per hit. For a more natural result, use dynamic EQ or volume automation instead. Compare the full section when bypassing, not just the meter.

## What to listen for

Whether the bass returns quickly after each kick; whether the pump lands on the beat; whether bypassing the sidechain makes the low end muddy; whether the chorus is over-pumped.

```audiolab
{"type": "instrument", "gm": "Synth Bass 1", "synth": "plucked", "phrase": ["E1", "E1", "G1", "E1"], "label": "Synth bass", "label_en": "Synth bass", "hint": "先听贝斯，再让底鼓触发侧链", "hint_en": "Hear the bass, then let the kick trigger the sidechain"}
```

## Common misconceptions

That sidechain belongs only to dance music; that a shorter release is tighter; that sidechain replaces arrangement.
:::
