---
id: job-game-loop
site: prod
cat: D
order: 4
title: 游戏循环与交互层
title_en: Game Loops and Interactive Layers
summary: 能无缝循环、按状态分层的游戏音乐素材。
summary_en: Game music assets that loop without a seam, stack by state and arrive ready for the engine.
level: standard
tags: [流程, 游戏音频, 循环, 分层]
tags_en: [workflow, game audio, looping, layers]
alias: [游戏循环, 交互音乐, game loop, 分层音乐]
links:
  - "[[glossary:stems]]"
  - "[[instrument:electronic-drums]]"
instances:
  - oga-000009 | 三十一秒的场景循环，长度与配器适合观察探索状态，是游戏素材的参照
  - oga-000013 | 三十三秒的复古战斗循环，节奏密度高，可对照战斗层怎样加厚
  - oga-000031 | 五十七秒的氛围循环，留白多，适合练接缝与低频处理
  - oga-000089 | 一分多钟的循环曲，段落稳定，可参考长循环怎样避免听觉疲劳
sources:
  - 游戏音乐的循环点、垂直分层与状态切换做法，参考游戏音频惯例。
  - 中间件导入、等长导出与命名惯例；游戏音频制作流程是主要依据。
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

一组能在引擎里循环的音乐素材：探索循环 30–120 秒，战斗层可以叠在探索层上，另有胜利、失败与菜单提示音。提示音另做一版不带尾音的，方便程序硬切。交 48 kHz、24 bit WAV，循环点用采样数写清，附速度、调性、小节数与分层说明。文件名按场景、层与编号统一，导入 Wwise 或 FMOD 之后不用再猜哪条是哪条。

## 三步走

先画状态图：探索、战斗、胜利、失败、菜单，每个状态一条循环与一条过渡。第二步写循环：先定循环的呼吸，再定配器，别反过来；多渲染一小节尾巴，让混响与延迟跨过接缝，循环点落在小节线，戴耳机连听十遍不点头。第三步拆层：把鼓、低音、旋律、氛围分成可独立开关的组，全部从 0:00 等长导出，再进中间件试切，记录每次切换的听感。

## 用到的工具与页面

DAW 加 Wwise 或 FMOD 就够，这里的游戏音频导论、循环与片段两页先读。用电子鼓与合成器做层，先保证每一层单独听也成立。战斗层不要靠加音量，要靠加密度与高频。如果引擎支持，给每条循环再加一个可切换的过渡段，切换就不会硬切。需要交给音频程序时，按 Stems 交付的命名规则做，并附一张状态与素材对应表，写清哪条循环配哪个场景。

## 验收标准

循环接缝在十次重复里听不出；各层相加不削波；从探索切战斗不超过一拍；循环长度是完整小节；所有文件等长、同采样率；循环点在采样级对齐，说明里注明采样率；引擎里导入后速度与调性正确；没有直流偏移与突然的音量跳变；提示音短到不打断操作。

```audiolab
{"type":"rhythm","sig":"4/4","bpm":120,"pattern":"q q e e q","cycles":2,"label":"循环接缝落在哪里","label_en":"Where the loop seam sits","hint":"听两遍，第二遍开头有没有被上一遍的尾巴顶住","hint_en":"Hear two passes; does the second downbeat collide with the tail of the first"}
```

## 常见返工原因

循环点切在混响尾巴上，每次回头都断；层与层不同步，叠起来相位打架；战斗层只是把探索层调响；文件按导出顺序命名，程序对不上；循环长度不是整小节，节拍器一进就漂；只交混合版，无法按状态切换；把循环做成一次性成品，玩家听第二遍就腻；把过场音乐写成线性成品，玩家中途退出就悬在半空。
:::

::: en
## What you have to hand over

A set of music assets that loop inside the engine: an exploration loop of thirty to one hundred twenty seconds, a combat layer that stacks on top of it, plus victory, failure and menu stings. Deliver 48 kHz, 24 bit WAV, loop points written in samples, with tempo, key, bar count and a layer map. Name files by scene, layer and number so nobody has to guess after import into Wwise or FMOD.

## Three steps

Draw the state chart first: explore, combat, victory, failure, menu. Give each state one loop and one transition. Second, write the loop: render an extra bar so reverb and delay cross the seam, place the loop point on a bar line, and listen ten times on headphones without flinching. Third, split the layers: drums, bass, melody and atmosphere become groups that can be muted independently. Export everything from 0:00 at equal length, then test the switches in middleware and note how each one feels.

## Tools and pages

A DAW plus Wwise or FMOD is enough. Read the site pages Introduction to Game Audio and Loops and Clips first. Build layers from electronic drums and synths, and make sure each layer stands up when heard alone. Do not make combat louder; make it denser and brighter. When handing over to an audio programmer, follow the naming rules in Delivering Stems and include a state-to-asset table showing which loop belongs to which scene.

## Acceptance checks

The seam is inaudible across ten repeats. Layers sum without clipping. Switching from explore to combat takes no more than one beat. Loop length is a whole number of bars. All files share length and sample rate. Tempo and key are correct after import. There is no DC offset and no sudden level jump. Stings are short enough not to interrupt control.

```audiolab
{"type":"rhythm","sig":"4/4","bpm":120,"pattern":"q q e e q","cycles":2,"label":"循环接缝落在哪里","label_en":"Where the loop seam sits","hint":"听两遍，第二遍开头有没有被上一遍的尾巴顶住","hint_en":"Hear two passes; does the second downbeat collide with the tail of the first"}
```

## Why work gets sent back

The loop point cuts a reverb tail, so every return breaks. Layers are not aligned and phase against each other. Combat is just the exploration layer turned up. Files are named by export order and the programmer cannot match them. The loop is not a whole bar and drifts against the click. Only a mixed version is delivered, so states cannot switch. A cutscene is written as a linear track, leaving it hanging when the player exits early.
:::
