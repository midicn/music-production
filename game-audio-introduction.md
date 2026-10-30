---
id: game-audio-introduction
site: prod
cat: A9
title: 游戏音频导论
title_en: Introduction to Game Audio
summary: 游戏音乐不是一条固定音轨，而是被玩家行为触发与拼接的素材系统。
summary_en: Game music is not one fixed track but a system of assets triggered and reassembled by what the player does.
level: standard
tags: [游戏音频, 循环, 触发, 状态, 中间件]
tags_en: [game audio, looping, triggers, states, middleware]
alias: [游戏音频, 游戏音乐, game audio, game music]
links:
  - "[[glossary:sound-design]]"
  - "[[glossary:stems]]"
  - "[[instrument:drum-kit]]"
instances:
  - oga-000001 | 游戏小镇曲 adventure-begins，循环长度与配器适合作为场景音乐的例子
  - oga-000053 | 不到两秒的 fanfare，可听短促的奖励提示音怎样写成完整乐句
  - oga-000004 | 战斗曲 battle 01，节奏密度高，适合观察战斗状态与探索状态的区别
sources:
  - Marks, Aaron，The Complete Guide to Game Audio（Focal Press）— 循环与状态切换章节核对，未引用
  - Collins, Karen，Game Sound（MIT Press）— 游戏音乐的历史与功能核对，未引用
updated: 2026-10-28
---

::: zh
游戏里的音乐不是按分钟播放的成品，而是一组可以被触发、循环、叠加的素材。玩家走到哪里、打到哪里，决定听到什么。

## 问题

线性配乐有确定的开头与结尾，游戏没有。同一段音乐可能被听三十秒，也可能十分钟；玩家还会暂停、死亡、重开。音乐必须在这种情况下成立。

## 交互或流程

常见结构是场景循环、战斗层与提示音。循环要无缝接回开头，战斗层在开战时淡入，提示音短到不打断操作。音频中间件按状态切换素材，作曲阶段就要把循环点与过渡写清楚。

## 做法与判断

先画状态图，列出探索、战斗、胜利、失败与菜单。为每个状态定一条循环与一条过渡，循环长度取三十秒到两分钟。判断标准是切回探索时是否突兀，若突兀，问题通常在过渡而不是循环本身。

## 听什么

听小镇曲的循环怎样留下重复空间，听战斗曲的鼓与低音怎样拉高节奏密度，听两秒的 fanfare 怎样完成起承转合。演示用铜管吹一个三音上行，听它作为奖励提示是否够短。

```audiolab
{"type":"instrument","gm":"Brass Section","synth":"brass","phrase":["C4","E4","G4"],"label":"两秒内完成的提示","label_en":"A cue that resolves in two seconds","hint":"奖励音要短到不打断操作，又要听得出结束","hint_en":"A reward sting must be short enough not to interrupt, yet sound finished"}
```

## 常见误解

游戏音乐不是电影配乐的缩短版，它要能被切断与重组。循环也不等于简单重复，接缝处常需要单独处理。另一点，音效与音乐由同一套总线管理，响度与动态要一起规划。
:::

::: en
Game music is not a finished track played by the minute. It is a set of assets triggered, looped and layered; where the player walks or fights decides what is heard.

## The problem

Linear scores have a clear beginning and end; games do not. The same piece may be heard for thirty seconds or ten minutes, and the player may pause, die or restart at any moment. The music must still work.

## Interaction or workflow

The usual structure is a scene loop, a combat layer and short stings. The loop returns seamlessly to its start, the combat layer fades in when fighting begins, and a sting is short enough not to interrupt control. Middleware switches these assets by state, so loop points and transitions must be written while composing.

## Practice and judgement

Draw a state chart: explore, combat, victory, failure, menu. Give each state a loop and a transition, with loops of thirty seconds to two minutes. The test is whether returning to explore feels abrupt. If so, the fault is usually the transition.

## What to listen for

Hear the town loop leave space for repetition, drums and bass raise the density in battle, and a two-second fanfare complete an arc. The demo is a three-note brass rise; is it short enough as a reward?

```audiolab
{"type": "instrument", "gm": "Brass Section", "synth": "brass", "phrase": ["C4", "E4", "G4"], "label": "A cue that resolves in two seconds", "label_en": "A cue that resolves in two seconds", "hint": "奖励音要短到不打断操作，又要听得出结束", "hint_en": "A reward sting must be short enough not to interrupt, yet sound finished"}
```

## Common misunderstandings

Game music is not a shortened film score; it must survive being cut and reassembled. A loop is not plain repetition, and its seam often needs separate work. Sound effects and music share buses, so loudness is planned together.
:::
