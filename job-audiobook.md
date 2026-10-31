---
id: job-audiobook
site: prod
cat: D
order: 520
title: 有声书制作
title_en: Producing an Audiobook
summary: 长文本分章、朗读与音乐垫底，交能过平台质检的文件。
summary_en: Chapterized long-form narration with a restrained music bed, delivered to pass a platform's audio check.
level: standard
tags: [流程, 有声书, 朗读, 长文本]
tags_en: [workflow, audiobook, narration, long-form]
alias: [有声书, 有声书制作, audiobook, 长文本朗读]
links:
  - "[[glossary:loudness-normalization]]"
  - "[[glossary:noise-floor]]"
  - "[[instrument:voice]]"
instances:
  - oga-000031 | 五十七秒、只有三十九个音的循环，留白多，可听垫底会不会盖住朗读
  - pdmx-000015 | 九十秒的钢琴独奏，音符稀疏，适合对照章节之间的过渡音乐
  - mutopia-001682 | 三十七秒的熟悉旋律，句法完整，可听它为何不适合垫在正文下
  - oga-000089 | 一分多钟的循环曲，结构稳定，可参考长章节里的重复处理
sources:
  - ACX 音频提交要求（Audible/ACX 官方）— 响度、峰值、底噪与文件格式的验收口径。
  - AES TD1008《Recommendations for Loudness of Internet Audio Streaming and On-Demand Distribution》（2021）— 语音类内容的响度目标。
  - Adobe Audition 官方文档 — Match Loudness 与 Diagnostics 面板的测量与批处理用法。
tool_kind: guide
tool_vendor: —
tool_form: 流程
tool_platforms: [通用]
tool_price: 不适用
tool_jobs: [流程]
tool_verified: 2026-10-31
updated: 2026-10-31
---

::: zh
## 先确认朗读是不是唯一主线

有声书里，音乐是客人。旁白一开口就是十几分钟，任何带旋律、带歌词、带明显节拍的垫底都会和语句抢重音。先问三件事：有没有角色对白，章节之间要不要过渡，平台允不允许音乐。若平台按单声道人声验收，正文段只留干声，音乐放到章节头尾，别铺满整章。

## 音乐只能放在三个位置

| 位置 | 长度 | 做法 | 容易出的问题 |
|---|---|---|---|
| 章节头 | 5–15 秒 | 一句主题，落在章名之后 | 抢走第一句朗读 |
| 章节尾 | 10–30 秒 | 收束，不淡到全无 | 切断旁白的尾音 |
| 正文垫底 | 通常不做 | 必须做时比人声低 25 dB 以上，去掉旋律 | 长听疲劳，质检不过 |

位置定完再写音乐。章节头用同一条主题做变体，整本书才有统一感；每章换一首新曲，听到第三章就像换了一本书。

## 录音、剪辑与接缝

一次录一章，口误当场重录，别指望后期拼。每章留三五秒环境声，剪辑时用它填缝，接缝才不会一段静、一段有底噪。降噪只去持续噪声，不要把底噪压成抽气声；齿音和气口留着，听感才像人。角色对白靠距离、语气和轻微音色区分，变调会像另一个人。音乐单独一轨，句间让 2–3 dB，句中不要起伏。工具用 Reaper、Pro Tools 或 Audition 都行，批处理与响度报告要能留档。

## 交付清单

- 一个文件一章，文件名含书号、章号与版本
- 单声道 44.1 kHz、24 bit WAV，另交平台要求的 MP3
- 章节头留 0.5–1 秒环境声，章节尾留 1–5 秒，正文不留长空白
- 整章响度按平台目标，峰值低于平台上限
- 安静段底噪可接受，降噪后没有金属尾音
- 首句与末句完整，没有吞字、没有半口气
- 音乐版与纯人声版等长、同起点
- 附一份读音表，列出人名、地名与专有名词

## 哪里会坏

整章响度不齐，听众每章都要调音量；降噪过头，齿音变薄，像隔着纸；音乐在句尾淡出，下一句像从水里冒出来；角色靠变调区分，听着像换了个播音员；章节文件起点不一，连播时有缝；只交 WAV，平台要求 MP3，转码后峰值过冲；垫底带歌词，和朗读互相拆台；把整本书塞进一个文件，平台无法分章，听众也没法跳转。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","G3","E4"],"label":"章节之间的三个音","label_en":"Three notes between chapters","hint":"音与音之间留出空隙，听它是否给下一句朗读让路","hint_en":"Leave space between the notes and hear whether the next spoken line has room"}
```
:::

::: en
## Narration is the only through-line

In an audiobook, music is a guest. A narration runs for ten or fifteen minutes without a break, and any bed with a melody, a lyric or a clear pulse competes with the stress of the sentence. Ask three questions first: is there character dialogue, does the chapter need a transition, and does the platform allow music at all. If the platform checks a mono voice track, keep the body dry and put music only at chapter edges.

## Three places music can go

| Position | Length | Approach | Common problem |
|---|---|---|---|
| Chapter opening | 5–15 s | One statement of the theme, after the chapter title | Steals the first spoken line |
| Chapter ending | 10–30 s | Close without fading to nothing | Cuts the narrator's tail |
| Under the body | Usually none | If required, 25 dB or more below the voice and without melody | Long-form fatigue, failed QC |

Decide the position before writing. Reuse one theme at chapter openings so the book feels whole; a new cue for every chapter makes chapter three feel like a different book.

## Recording, editing and seams

Record one chapter at a time and redo fluffs on the spot. Keep three to five seconds of room tone per chapter and use it to fill edits, or the seam will alternate between silence and hiss. Noise reduction should remove steady noise only; do not squeeze the floor into a pumping void. Keep breaths and sibilance. Distinguish characters by distance, delivery and slight timbre, not pitch shifting. Put music on its own track and drop it 2–3 dB between phrases, never inside a phrase. Reaper, Pro Tools or Audition all work; keep batch processing and loudness reports on file.

## Delivery checklist

- One file per chapter, named with book code, chapter and version
- Mono 44.1 kHz, 24 bit WAV, plus the MP3 the platform asks for
- Half a second to one second of room tone at the head, one to five seconds at the tail, no long gaps in the body
- Chapter loudness on the platform target, peak below its ceiling
- Acceptable noise floor in quiet passages, no metallic residue after cleanup
- First and last lines complete, no swallowed words or half breaths
- Music and dry versions equal length and same start
- A pronunciation sheet for names, places and specialist terms

## Where it breaks

Chapter levels drift and the listener adjusts volume every chapter. Over-reduction thins the sibilance until the voice sounds like it is behind paper. Music fades at the end of a phrase and the next line surfaces from underwater. Pitch-shifted characters sound like a different announcer. Chapters start at different points and the seams show in continuous playback. Only WAV is delivered, the platform wants MP3, and the transcode overshoots. A bed with lyrics fights the narration. The whole book arrives as one file, so the platform cannot chapterize it and the listener cannot jump.
:::
