---
id: job-film-cue
site: prod
cat: D
order: 3
title: 一分钟短片配乐
title_en: Scoring a One-Minute Film
summary: 一分钟短片的配乐：贴片、情绪推进与可交付文件。
summary_en: A one-minute score that locks to picture, carries the emotional turn and arrives as files an editor can use.
level: standard
tags: [流程, 影视配乐, 贴片, 交付]
tags_en: [workflow, film scoring, sync, delivery]
alias: [短片配乐, 一分钟配乐, film cue, 影视配乐]
links:
  - "[[glossary:cue]]"
  - "[[glossary:sync-license]]"
  - "[[period:romantic]]"
instances:
  - oga-000004 | 五十八秒的战斗曲，长度接近一分钟，可听短曲怎样维持张力，是配乐的参照
  - oga-000002 | 一分半的场景曲，段落切换清楚，可对照画面转场处的处理
  - oga-000003 | 一分三十五秒的紧张段落，适合观察低音与打击怎样推动情绪
  - pdmx-000087 | 探戈的强弱起伏与乐器进出，可参考一段音乐如何完成情绪转向
sources:
  - 短片配乐的贴片、hit point 与 stems 交付做法，参考影视配乐惯例。
  - 配乐与画面同步、帧率与响度目标的处理；后期制作惯例是主要依据。
tool_kind: guide
tool_vendor: —
tool_form: 流程
tool_platforms: [通用]
tool_price: 不适用
tool_jobs: [流程]
tool_verified: 2026-10-30
updated: 2026-10-30
---

::: zh
## 你要交的是什么

一条一分钟短片的配乐：与画面同起点，按项目帧率对齐，长度覆盖到最后一帧。交立体声混音、按组拆开的 stems（弦乐、管乐、打击、合成）、一条 30 秒短版，以及写明速度、调性与 hit point 的 cue sheet。cue sheet 里写清每条提示的用途，不要只写时间码。文件用 48 kHz、24 bit，按项目零点对齐；需要 handle 时另附一版首尾各带两帧余量的文件，剪辑师才有地方下刀。

## 三步走

先贴片：把整片看三遍再动手，第一遍不看时间码。通读画面，标出剪辑点、转场、台词与片名出现的帧，把时间码写进工程，再决定哪里需要音乐、哪里必须留白；第一个音从哪一帧进，也要一起定。第二步写主题：用四到八小节动机，安排一次情绪转向，放在全片后段；转场前留气口，不要用满。第三步做 mockup 与打印，按帧检查起点，导出 stems 与混音，最后关掉参考音轨，对一遍画面。

## 用到的工具与页面

支持视频轨的 DAW 就够；这里的影视配乐导论与主题动机两页先读。选一条参考配乐定音色密度，但不要照抄旋律。画面改版时，先向剪辑师要锁定版，再开始写。要交给混音师时，按 Stems 交付的命名与等长规则做；响度按对方给的目标，没有目标就交未限制的混音，并附一版 -14 LUFS 的参考。片名出现前的那一拍，往往比整段配乐更重要。

## 验收标准

音乐起点与终点落在约定帧；主要 hit point 的误差不超过两帧；台词段落里音乐让出 2–3 dB；留白处的底噪与音乐段一致，切换时不跳；stems 相加与混音一致；30 秒短版能独立成立；cue sheet 的时间码与工程一致；任何版本都没有爆音与突然切断的混响。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C3","G3","C4","E4"],"label":"一分钟里的一次情绪转向","label_en":"One emotional turn inside a minute","hint":"听四个音怎样从低处抬起来，再想它该落在哪一帧","hint_en":"Hear the four notes rise, then decide which frame they should land on"}
```

## 常见返工原因

从 0:00 写起，没对画面；情绪从头到尾一个强度，转场没有落点；音乐压住台词；只交一条混音，混音师无法单独调整；stems 从不同起点导出，相加对不上；速度图没写，改一版画面就要整段重做；把未锁定的画面当最终版，剪辑一改就全乱；把参考曲的旋律写进去，发行时才发现权利问题。
:::

::: en
## What you have to hand over

A one-minute score locked to picture: same start as the film, aligned to the project frame rate, running to the last frame. Deliver a stereo mix, stems split by group (strings, winds, percussion, synth), a thirty-second cutdown, and a cue sheet listing tempo, key, hit points and the purpose of each cue. Use 48 kHz and 24 bit, aligned to the project zero; supply a separate version with two frames of handle at each end so the editor has a clean edge.

## Three steps

Spot the picture first. Read the cut, mark every edit, transition, line of dialogue and the frame where the title appears, and put those timecodes into the session. Decide where music is needed and where silence must stay. Second, write the theme: a four-to-eight-bar motif with one emotional turn placed late in the film; leave air before transitions instead of filling them. Third, mock it up and print it, check the start frame by frame, export stems and mix, then mute the reference and watch the film again.

## Tools and pages

A DAW with a video track is enough. Read the site pages Introduction to Film Scoring and Leitmotif in Film first. Use a reference score to set density, never to borrow its melody. When handing over to a mixer, follow the naming and equal-length rules in Delivering Stems. Deliver to the loudness target you were given; if there is none, send an unlimited mix plus a -14 LUFS reference. The beat before the title often matters more than the whole cue.

## Acceptance checks

The music starts and ends on the agreed frames. Main hit points are within two frames. Music drops 2–3 dB under dialogue. Stems sum to the mix. The thirty-second cutdown works on its own. The cue sheet timecodes match the session. No version clips or cuts off a reverb tail.

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C3","G3","C4","E4"],"label":"一分钟里的一次情绪转向","label_en":"One emotional turn inside a minute","hint":"听四个音怎样从低处抬起来，再想它该落在哪一帧","hint_en":"Hear the four notes rise, then decide which frame they should land on"}
```

## Why work gets sent back

The cue starts at 0:00 without checking picture. The emotion stays at one level and transitions have no landing. Music covers dialogue. Only a stereo mix is delivered, so the mixer cannot rebalance. Stems start at different points and do not sum. No tempo map exists, so a new picture cut means starting over. A reference melody is copied and the rights problem appears at release.
:::
