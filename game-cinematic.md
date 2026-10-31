---
id: game-cinematic
site: prod
cat: A9
order: 466
title: 游戏过场
title_en: Game Cinematics
summary: 过场音乐要跟镜头与交互状态对齐，并在进入可玩段时干净退出。
summary_en: Cinematic music must follow the cut and the interaction state, then exit cleanly into gameplay.
level: standard
tags: [游戏, 过场, 配乐, 交互, 交付]
tags_en: [games, cinematics, scoring, interaction, delivery]
alias: [游戏过场, 过场动画配乐, 游戏过场音乐, game cinematic, cutscene music]
links:
  - "[[glossary:cue]]"
  - "[[glossary:stems]]"
  - "[[glossary:texture]]"
  - "[[glossary:sound-design]]"
instances:
  - oga-000324 | 近六分钟的 the ritual，合唱、弦乐与钢琴交替，适合观察过场里主题如何先出现再变形
  - oga-000045 | 四分多钟的 elegy for the summer of 4096，合成弦乐与钢琴铺底，适合做长镜头的情感段
  - oga-000298 | 摇滚乐队、弦乐与合唱同场，速度从 120 提到 150，适合做过场高潮的加码
sources:
  - Marks, Aaron，The Complete Guide to Game Audio（Focal Press）— 过场、循环与状态切换章节。
  - Collins, Karen，Game Sound（MIT Press）— 游戏叙事与音乐功能章节。
  - AES（Audio Engineering Society）关于游戏音频与交互音乐的公开论文 — 过场与可玩段衔接的做法核对。
updated: 2026-10-31
---

::: zh
游戏过场看起来像电影，制作却要按交互状态组织。音乐可能在镜头结束前就被跳过，也可能因为玩家按键而提前退出。

## 过场不是电影片段

过场有确定的镜头，却没有确定的观看时长。玩家可以跳过，平台可能加载延迟，镜头还会被 QTE 或对话选项打断。音乐要写成可进出：开头有清晰的进入点，中段有可循环的铺垫，结尾有可硬切的收束。不要写只有完整听完才成立的长句。过场的音频文件按状态命名，引擎才能按事件取用；可跳过版与完整版要共用同一个起点。

## 音乐与交互状态对齐

先和关卡设计确认状态：过场进入、可跳过、QTE、对话选择、回到可玩。每个状态对应一个音乐段或一个参数，状态表要交给音频程序，而不是只留在作曲的工程里。进入可玩段时，音乐要么在强拍收束，要么用短淡化退出，不能拖在半空中。若过场与可玩段共用主题，保留同一个动机，但把配器与密度换掉，玩家才会感到世界连续、控制权已交回。

## 段落与交付

| 过场段落 | 音乐任务 | 交付要点 |
| --- | --- | --- |
| 冷开场 | 建立世界与主题 | 前 3 秒内可辨认的动机 |
| 对话/铺垫 | 不抢台词 | 长音、少换和声、可循环 |
| 高潮/QTE | 推到位 | 强拍落点与画面动作对齐 |
| 退出到可玩 | 交回控制 | 强拍收束或 0.5 到 1 秒淡化 |
| 可跳过版本 | 不留下残响 | 独立的短版与干净尾音 |

```audiolab
{"type":"instrument","gm":"Choir Aahs","synth":"vocal","phrase":["D3","A3","D4","F4","E4","D4"],"label":"过场主题的第一次出现","label_en":"First statement of the cinematic theme","hint":"注意合唱进来时，弦乐是否让出了中频","hint_en":"Hear whether the strings clear the midrange when the choir enters"}
```

## 会坏在哪里

过场音乐不能依赖玩家一定看完。跳过、加载失败、语言版本不同都会改变时长；只写一个完整版，等于把风险留给引擎。也不要把过场当成预告片：预告片靠三幕与 hit point，过场靠叙事状态与可退出。若音乐在可玩段还在继续，玩家会分不清何时该操作。过场越接近电影，越要提前确认跳过点与混音优先级。
:::

::: en
A game cinematic looks like film, but it is built around interaction states. The music may be skipped before the shot ends, or cut short when the player presses a button.

## Not a film scene

A cinematic has fixed shots but no fixed viewing time. Players skip, platforms load late, and QTE prompts or dialogue choices interrupt the cut. Write music that can enter and leave: a clear entry, a loopable middle and an ending that can hard-cut. Avoid long phrases that only work if heard to the end. Name the audio files by state so the engine can fetch them by event, and give the skippable and full versions the same starting point.

## Align with interaction states

Confirm the states with level design: cinematic in, skippable, QTE, dialogue choice, return to play. Each state maps to a section or a parameter, and the state table has to reach the audio programmer, not stay in the composer's session. On the return to play, the music either resolves on a strong beat or fades out in under a second; it cannot hang in mid-air. If the cinematic and gameplay share a theme, keep the motive but change orchestration and density, so the world feels continuous and control has changed hands.

## Sections and delivery

| Cinematic section | Musical job | Delivery point |
| --- | --- | --- |
| Cold open | Establish world and theme | A motive recognisable within 3 seconds |
| Dialogue / setup | Stay out of the lines | Long tones, few chord changes, loopable |
| Climax / QTE | Land the hit | Strong beat aligned to the action |
| Exit to play | Hand back control | Strong-beat close or 0.5 to 1 second fade |
| Skippable version | Leave no tail | A separate short version with a clean ending |

```audiolab
{"type": "instrument", "gm": "Choir Aahs", "synth": "vocal", "phrase": ["D3", "A3", "D4", "F4", "E4", "D4"], "label": "First statement of the cinematic theme", "label_en": "First statement of the cinematic theme", "hint": "注意合唱进来时，弦乐是否让出了中频", "hint_en": "Hear whether the strings clear the midrange when the choir enters"}
```

## Where it goes wrong

Cinematic music cannot assume the player watches to the end. Skipping, failed loading and different language versions all change the duration; one full-length version leaves the risk to the engine. Nor is a cinematic a trailer: trailers run on three acts and hit points, cinematics on narrative states and exit points. If the music continues into gameplay, the player cannot tell when to take control. The closer a cinematic gets to film, the earlier the skip points and mix priority must be agreed.
:::
