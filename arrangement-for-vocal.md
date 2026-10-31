---
id: arrangement-for-vocal
site: prod
cat: A2
order: 306
title: 为人声留位
title_en: Arranging Around a Vocal
summary: 人声听不清，多半是伴奏在同一频段和同一时刻做了太多事。
summary_en: A vocal disappears when the backing fills the same band at the same moment, not when it is merely quiet.
level: standard
tags: [编曲, 人声, 频段, 织体]
tags_en: [arranging, vocal, frequency, texture]
alias: [人声留位, 给人声让位, 伴奏编配, arrangement for vocal, vocal space]
links:
  - "[[glossary:tessitura]]"
  - "[[glossary:voicing]]"
  - "[[glossary:doubling]]"
  - "[[instrument:voice]]"
instances:
  - openscore-000131 | 舒伯特《美丽的磨坊女》中的一首，人声与钢琴的声部关系清楚，适合先练让位（CC0）
  - openscore-000008 | 《魔王》在人声的叙事与角色之间切换，动态落差大（CC0）
  - openscore-000018 | 福雷的无词练声曲，长句连续，适合听伴奏怎样托住旋律（CC0）
sources:
  - Walter Piston, Orchestration（W. W. Norton）关于人声与伴奏平衡的章节
  - The New Grove Dictionary of Music and Musicians 中 art song 与 accompaniment 条目
  - Bobby Owsinski, The Mixing Engineer's Handbook 关于人声与伴奏频段分配的章节
updated: 2026-10-31
---

::: zh
副歌一来人声就没了，通常不是人声太小，而是伴奏在 1 到 4 kHz 同时干了三件事：铺和弦、走旋律、打节奏。把这三件事分开，比把人声推高三格有效得多。

## 先定人声的音区

编曲前先唱一遍，标出每段的实际音区与最舒服的几个音。人声在哪个八度、哪几个音上最有力，决定了伴奏的音区该怎么让。人声低时，中低频容易和吉他、钢琴左手打架；人声高时，弦乐与合成铺底会盖住泛音。把主唱旋律单独导一轨，循环播放，任何新声部加进来时，都能立刻听出有没有挡住。

## 频段：让路要有次序

人声的可懂度主要在 1 到 4 kHz，厚度在 200 到 400 Hz，齿音在 5 kHz 以上。伴奏不是一律切掉这些频段，而是分工：铺底让出 1 到 3 kHz，吉他改用中高频的分解，钢琴左手收在 200 Hz 以下。几件乐器同时占同一块，切谁都不干净，最好的办法是换音区或换节奏型。

| 频段 | 人声在这里是什么 | 伴奏怎么让 |
|---|---|---|
| 80 到 200 Hz | 胸腔共鸣的底 | 低音与底鼓分工，别都堆在这里 |
| 200 到 500 Hz | 厚度，也最容易浑 | 钢琴左手、节奏吉他减层 |
| 1 到 3 kHz | 字头与可懂度 | 铺底与弦乐让开，或窄带挖一点 |
| 3 到 6 kHz | 存在感与齿音 | 控制镲片与明亮合成器 |
| 6 kHz 以上 | 空气感 | 少叠高频亮点 |

## 密度：少弹一个音

同一时刻发声的声部数，比每件乐器的音量更能决定人声是否突出。主歌只留三件：人声、低音、一个和声乐器；副歌再加一层，但让新层走长音而不是切分。人声句尾的空隙留给伴奏回应，形成呼应，而不是所有乐器从头到尾齐奏。删掉一层，往往比拉低六条推子更有效。

## 动态：段落之间要有落差

全程一样满，人声就没有地方出来。主歌收、预副歌推、副歌放，是常见做法；也可以在最后一段副歌撤掉鼓，只留人声与低音。动态不只靠音量，还靠音区与密度：副歌让人声留在原音区，把伴奏往高低两端拉开，人声反而更清楚。反过来，如果副歌只是把所有推子推高，人声的相对位置不会变，只是整体更吵。

## 会做坏的地方

给人声让位不等于把伴奏做薄。全曲挖空 2 kHz，会让人声孤立、伴奏发闷；过度侧链压缩会让和弦每次随人声抽气；把所有伴奏压成一样响，动态没了，人声也失去对比。目标是让人听清字，不是让伴奏消失。混音阶段再补往往已经太晚，最好在编曲时就决定谁在什么时候说话。

```audiolab
{"type":"instrument","gm":"Voice Oohs","synth":"vocal","phrase":["G4","A4","B4","D5","B4","A4","G4","E4"],"label":"给人声留一条缝","label_en":"Leaving a gap for the voice","hint":"听伴奏有没有在同一个音区跟着唱","hint_en":"Hear whether the backing sings along in the same register"}
```
:::

::: en
When the chorus arrives and the voice vanishes, the vocal is usually not too quiet. The backing is doing three jobs at once between one and four kilohertz: holding chords, carrying a melody and marking the rhythm. Separating those jobs works far better than pushing the vocal up three decibels.

## Set the vocal's register first

Sing the song before arranging and mark the actual range of each section and the notes where the voice is strongest. That range decides where the backing must yield. A low vocal collides with guitar and piano left hand in the low mids; a high vocal loses overtones under strings and pads. Bounce the lead melody to its own track, loop it, and any new part will announce immediately whether it blocks the voice.

## Frequency: yielding in order

Intelligibility sits mainly between one and four kilohertz, body between two and four hundred hertz, sibilance above five. The backing should not cut all of it but divide the work: pads clear one to three kilohertz, guitars move to broken figures higher up, the piano left hand stays below two hundred. When several instruments occupy the same band, no cut is clean; change register or change the rhythm instead.

| Band | What the voice has there | How the backing yields |
|---|---|---|
| 80 to 200 Hz | Chest resonance | Split the role between bass and kick |
| 200 to 500 Hz | Body, and the easiest to muddy | Thin piano left hand and rhythm guitar |
| 1 to 3 kHz | Consonants and intelligibility | Move pads and strings aside, or notch narrowly |
| 3 to 6 kHz | Presence and sibilance | Tame cymbals and bright synths |
| Above 6 kHz | Air | Avoid stacking high sparkle |

## Density: play one note fewer

How many parts sound at once decides whether a vocal stands out more than any single level. A verse can run on three: voice, bass and one chordal instrument. The chorus adds a layer, but that layer holds long notes rather than syncopation. Leave the gaps at phrase endings for the backing to answer, so the arrangement converses instead of everyone playing from bar one to the end. Removing a layer usually beats pulling down six faders.

## Dynamics: contrast between sections

If everything is full all the time, the voice has nowhere to emerge. A common shape is a restrained verse, a building pre-chorus and an open chorus; another is dropping the drums in the final chorus and leaving voice and bass. Dynamics come from register and density as much as level: keep the voice where it is in the chorus and spread the backing towards the outer registers, and the voice often becomes clearer. Raise every fader instead and the vocal keeps the same relative place, only louder.

## Where it goes wrong

Making room is not the same as thinning the backing. Scooping two kilohertz across the whole song isolates the voice and leaves the track hollow; heavy sidechain compression makes chords pump with every syllable; flattening the backing to one level removes the contrast the voice needs. The goal is intelligible words, not a backing that disappears. Fixing it at the mix is often too late; decide who speaks when at the arranging stage.

```audiolab
{"type": "instrument", "gm": "Voice Oohs", "synth": "vocal", "phrase": ["G4", "A4", "B4", "D5", "B4", "A4", "G4", "E4"], "label": "Leaving a gap for the voice", "label_en": "Leaving a gap for the voice", "hint": "Hear whether the backing sings along in the same register", "hint_en": "Hear whether the backing sings along in the same register"}
```
:::
