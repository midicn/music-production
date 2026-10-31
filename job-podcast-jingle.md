---
id: job-podcast-jingle
site: prod
cat: D
order: 2
title: 播客片头
title_en: A Podcast Intro
summary: 十到二十秒的播客片头，给口播留出落点。
summary_en: A ten-to-twenty-second podcast intro that leaves a clear landing point for the host's voice.
level: standard
tags: [流程, 播客, 片头, 口播]
tags_en: [workflow, podcast, jingle, voice-over]
alias: [播客片头, 播客 jingle, podcast intro, 节目片头]
links:
  - "[[glossary:loudness-normalization]]"
  - "[[instrument:polysynth]]"
instances:
  - oga-000000 | 二十多秒的短曲，可听一段音乐怎样在有限长度内完成起承转合，是片头的参照
  - oga-000053 | 一秒多的 fanfare，可听提示音怎样短到不打断口播，是片头的参照
  - oga-000088 | 二十四秒的循环，适合对照「片头」与「循环床」的差别
  - mutopia-001682 | 三十七秒的短旋律，句法清楚，可参考片头如何用一句就收住
sources:
  - 播客片头长度、口播落点与纯音乐版的交付做法；播客制作惯例是主要依据。
  - 播客响度与真峰值目标——依据来自播交流程。
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

一条 10–20 秒的播客片头：音乐从第一帧到最后一帧都对齐，主持人报出节目名时，音乐要让出位置或落在一个重音上。交立体声 48 kHz、24 bit WAV 与 320 kbps MP3，另附无口播的纯音乐版，以及只留最后两秒的 sting 版。有片尾时，片尾用同一调性、同一长度，别让两段像来自两个节目。片头不是主题曲，它只负责把人带进来。

## 三步走

先写最后三秒：定下节目名落在哪一拍，倒推前一句口播需要多少空间，再写前面的四到八小节。先拿到口播稿，不要等音乐做完再找主持人。第二步搭骨架：一个短动机、一次上行、一个收束，音色不抢人声，别用带歌词的采样。第三步按口播试混，报名字时音乐降 3–4 dB 或直接停一拍，再用手机外放确认字头清楚。纯音乐版从同一工程导出，只关掉对白轨。

## 用到的工具与页面

在 DAW 里建一条对白轨，把主持人干声放进去试；这里的工程模板与响度表两页先读。片头常用 -16 LUFS 立体声、真峰值 -1 dBTP，交付前用响度表核一遍，别靠耳朵猜。需要短促的收尾时，参考游戏音频导论里提示音的做法：短、清楚、有结束感。片头里不要放会持续到正文的音效，剪辑点会很难找。最后把成品放进播客宿主预听一次，上线后的压缩会改变字头。

## 验收标准

总长在 10–20 秒之间；节目名落在重拍或留白上，不被音乐盖住；第一句口播的字头清楚；主持人换气的位置没有被音乐顶住；结尾能在两拍内收住，方便接正文；纯音乐版与口播版等长；两条文件的响度差不超过 1 LU；没有淡出没做完的尾巴，也没有突然切断的混响。

```audiolab
{"type":"instrument","gm":"Brass Section","synth":"brass","phrase":["C5","G4","C5"],"label":"节目名落下前的三个音","label_en":"Three notes before the show name lands","hint":"三个音要短，最后一个落下就收住","hint_en":"Keep the three notes short; the last one lands and stops"}
```

## 常见返工原因

音乐太满，人声进来像吵架；结尾拖长，主持人只能干等；片头比正文响很多，听众先调小再调大；只交了口播版，换主持人就要重做；循环点没对齐，剪到十五秒时接缝露出来；节目名被剪在弱拍上，听感像抢话；把片头写成完整歌曲的前奏，十秒内没有落点。
:::

::: en
## What you have to hand over

A ten-to-twenty-second podcast intro: music locked from the first frame to the last, and a clear space or an accent at the moment the host says the show name. Deliver stereo 48 kHz, 24 bit WAV and a 320 kbps MP3, plus an instrumental bed with no voice and a sting version holding only the final two seconds. If there is an outro, give it the same key and length so the two do not sound like different shows.

## Three steps

Write the last three seconds first. Decide which beat the show name lands on, work backwards to the space the preceding line needs, then write the preceding four to eight bars. Second, build the skeleton: one short motif, one lift, one close. Keep the timbre out of the voice's way and avoid samples with lyrics. Third, mix against a spoken test: drop the music by 3–4 dB or leave one beat empty under the name, then check the consonants on a phone speaker. Export the instrumental from the same session with only the voice track muted.

## Tools and pages

Set up a dialogue track in the DAW and drop the host's dry voice into it. Read the site pages Session Templates and Loudness Metering first. Podcast intros commonly target -16 LUFS stereo and -1 dBTP true peak; check the meter before delivery rather than guessing by ear. For a short close, borrow the game-audio approach to stings: short, clear, finished. Do not let an effect run into the body copy, or the edit point becomes hard to find.

## Acceptance checks

The total sits between ten and twenty seconds. The show name lands on an accent or in a gap and is never covered. The first spoken consonant is clear. The ending closes within two beats so the body can start. The instrumental and voiced versions are the same length. Their loudness differs by no more than 1 LU. There is no half-finished fade and no reverb chopped off at the end.

```audiolab
{"type":"instrument","gm":"Brass Section","synth":"brass","phrase":["C5","G4","C5"],"label":"节目名落下前的三个音","label_en":"Three notes before the show name lands","hint":"三个音要短，最后一个落下就收住","hint_en":"Keep the three notes short; the last one lands and stops"}
```

## Why work gets sent back

The music is too full and the voice sounds like it is arguing with it. The tail runs long and the host has to wait. The intro is much louder than the body, so listeners turn down and then turn up. Only a voiced version is delivered, so a new host means a new session. The loop point is off and the seam appears when the intro is cut to fifteen seconds. The show name lands on a weak beat and feels like an interruption.
:::
