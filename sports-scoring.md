---
id: sports-scoring
site: prod
cat: A9
order: 465
title: 体育配乐
title_en: Scoring Sports
summary: 体育配乐按镜头与赛点组织，靠节奏、留白与可循环段落撑住长时段。
summary_en: Sports scoring follows the cut and the pivotal moment, using rhythm, silence and loopable sections across long broadcasts.
level: standard
tags: [体育, 配乐, 节奏, 循环, 赛事]
tags_en: [sports, scoring, rhythm, loops, broadcast]
alias: [体育配乐, 赛事音乐, 运动配乐, sports scoring, sports music]
links:
  - "[[glossary:ostinato]]"
  - "[[glossary:texture]]"
  - "[[glossary:stems]]"
  - "[[glossary:cue]]"
instances:
  - oga-000004 | 五十八秒的战斗曲，弦乐、铜管、定音鼓与太鼓同场，适合做开场或赛点前的短促推力
  - oga-000049 | 一百七十四拍的失真吉他曲，密度高，适合观察快剪集锦里的节奏对齐
  - oga-000298 | 摇滚乐队、弦乐与合唱同场，速度从 120 提到 150，适合做赛点前的层层加码
sources:
  - Buhler, Neumeyer and Deemer，Hearing the Movies（Oxford University Press）— 音乐与剪辑节奏章节。
  - AES（Audio Engineering Society）关于现场转播与扩声响度的公开论文 — 音乐与现场声比例的依据。
  - EBU R128 — 广播节目响度与真峰值的交付口径。
updated: 2026-10-31
---

::: zh
体育配乐的时间由镜头和赛点决定，不由曲式决定。一个进球可能只给三秒，也可能回放三分钟；音乐要在两种长度里都成立。

## 先看镜头

先拿到剪辑版本与解说轨，标出开哨、得分、暂停、回放、颁奖。回放与实时画面的音乐要分开做：实时段给解说留空间，回放段才允许主题完整出现。音乐的任务不是解说比赛，而是把观众的情绪推到镜头已经指向的地方。快剪段落用固定节奏型与短动机，镜头越碎，音乐越要稳；慢镜头与人物特写则要撤掉打击，留长音与呼吸。

## 段落怎么安排

开场与颁奖需要可识别的主题，通常八到十六小节就够，能反复也能剪短。集锦段落要能循环：鼓组与低音保持稳定，旋律层可加可减，方便剪辑师按镜头长度取用。赛点前用层层加码：加鼓、加铜管、提速度，但每次只加一层；赛点落下后要敢留白，让现场声与解说回来。若比赛进入加时，主题要能再起一次，但不要把所有层同时加满。

## 段落与任务

| 段落 | 音乐任务 | 写法 |
| --- | --- | --- |
| 开场/片头 | 建立身份 | 8 到 16 小节主题，铜管或人声 |
| 快剪集锦 | 维持推力 | 固定节奏型、短动机、可循环 |
| 赛点前 | 加码 | 每次加一层，提速度或加密度 |
| 赛点后 | 释放 | 撤打击、留长音、让现场声 |
| 颁奖/结尾 | 收束 | 主题完整回归，不要新素材 |

```audiolab
{"type":"instrument","gm":"Brass Section","synth":"brass","phrase":["C4","G4","C5","G4","E4","G4","C5"],"label":"赛点前的加码","label_en":"Building before the decisive moment","hint":"注意每次重复加一层，而不是一次到顶","hint_en":"Hear one layer added at a time rather than everything at once"}
```

## 会坏在哪里

不要把整场比赛铺满音乐。解说、现场声与观众声是赛事的主体，音乐只在需要时进来。也不要把流媒体母带直接用于广播：广播有响度与真峰值规范，过响会被压，动态反而更小。版权上，现场播放的唱片片段与自制配乐是两套授权，不能混用。音乐救不了没有情绪的镜头，只能放大已经存在的瞬间。
:::

::: en
Sports music is timed by the cut and the pivotal moment, not by musical form. A goal may get three seconds or a three-minute replay, and the cue has to work at both lengths.

## Read the cut first

Get the edited picture and the commentary track, then mark kickoff, score, timeout, replay and ceremony. Score replays and live action differently: live action leaves room for commentary, while a replay can carry the full theme. The music is not there to describe the game; it pushes the feeling toward what the picture already points at. Fast cutting wants a fixed rhythmic figure and a short motive: the more fragmented the shots, the steadier the music. Slow motion and faces need percussion removed, long tones and breath.

## Shaping the sections

Openers and ceremonies need a recognisable theme, often eight to sixteen bars, repeatable and easy to cut shorter. Montages must loop: drums and bass stay steady while melodic layers come and go, so an editor can take the length needed. Before the decisive moment, build one layer at a time: add drums, add brass, lift the tempo, but never everything at once. After the moment lands, dare to leave space and let the crowd and commentary return. If the match goes to extra time, the theme must be able to rise once more without every layer already running.

## Sections and jobs

| Section | Musical job | Writing approach |
| --- | --- | --- |
| Opening / titles | Establish identity | 8 to 16 bars, brass or voice |
| Fast montage | Keep momentum | Fixed figure, short motive, loopable |
| Before the moment | Build | One layer at a time, tempo or density |
| After the moment | Release | Drop percussion, long tones, crowd |
| Ceremony / end | Close | Full theme return, no new material |

```audiolab
{"type": "instrument", "gm": "Brass Section", "synth": "brass", "phrase": ["C4", "G4", "C5", "G4", "E4", "G4", "C5"], "label": "Building before the decisive moment", "label_en": "Building before the decisive moment", "hint": "注意每次重复加一层，而不是一次到顶", "hint_en": "Hear one layer added at a time rather than everything at once"}
```

## Where it goes wrong

Do not fill the whole match with music. Commentary, location sound and the crowd carry the event; music enters when it has a job. Do not send the streaming master straight to broadcast either: loudness and true-peak rules mean an over-loud mix gets turned down and loses dynamics. A record played in the arena and a custom score are two different licences and cannot be mixed up. Music cannot rescue a flat cut, only enlarge a moment that already exists.
:::
