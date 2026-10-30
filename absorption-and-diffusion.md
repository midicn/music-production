---
id: absorption-and-diffusion
site: prod
cat: A5
title: 吸音与扩散
title_en: Absorption and Diffusion
summary: 吸音减少反射能量，扩散打散方向，两者解决不同问题。
summary_en: Absorption removes reflected energy; diffusion scatters it. They solve different acoustic problems.
level: standard
tags: [吸音, 扩散, 声学处理, 颤动回声, 低频陷阱]
tags_en: [absorption, diffusion, acoustic treatment, flutter echo, bass trap]
alias: [吸音, 吸声, 扩散, absorption, diffusion, acoustic foam]
links:
  - "[[glossary:absorption]]"
  - "[[glossary:diffusion]]"
  - "[[glossary:room-treatment]]"
  - "[[glossary:bass-trap]]"
instances:
  - essen-000517 | 单声部《阳关歌》，素材干净，适合听房间尾巴与颤动回声（C1）
  - atepp-000369 | 格里格《夜曲》，钢琴余响长，能比较吸音前后尾巴的变化（C1）
  - cyberhymnal-006346 | 赞美诗《Morgan》，持续和弦适合判断低频是否被过度吸收（C1）
sources:
  - Everest, F. Alton，Master Handbook of Acoustics（McGraw-Hill）— 吸声与扩散章节核对，未引用
  - Newell, Philip，Recording Studio Design（Focal Press）— 控制室处理章节核对，未引用
updated: 2026-10-28
---

::: zh
## 问题
录音室贴满吸音棉后，声音反而发闷、低频更乱；另一间只放几块扩散板，却听起来开阔。吸音与扩散解决的是不同问题。

## 物理或房间
吸音把声能转成热，吸声系数从 0 到 1。多孔材料在厚度接近四分之一波长时最有效，所以薄棉主要吸中高频；低频要靠厚层、膜共振或亥姆霍兹结构。扩散不减少总能量，而是把反射打散到不同方向与时间，让梳状滤波与颤动回声变弱。

## 做法与判断
先处理第一反射点与墙角：前者用 5 到 10 厘米多孔吸音，后者用低频陷阱。后墙与天花板可放扩散，保留一些反射，避免把房间吸成无响室。判断标准是拍手尾巴是否干净、说话是否费力、低频是否还轰。每次只加一处。

## 听什么
在房间中央拍手，听有没有快速重复的颤动回声；再听铙钹余响，是自然衰减还是被高频吸掉。播一段独奏人声，注意齿音与房间尾巴的比例。处理前后用同一段素材对比。

## 常见误解
吸音棉不是越多越好，它主要处理中高频。扩散板不能代替低频陷阱。地毯与窗帘能改变高频，却几乎不动 100 Hz 以下。吸得太死，混音在外面会站不住。

```audiolab
{"type":"instrument","gm":"Timpani","synth":"struck","phrase":["D2","A2","D3"],"label":"三下短音，听房间的尾巴","label_en":"Three short hits, one room tail","hint":"在房间里重放这几下短音，听每一下之后还剩多少反射；处理前后用同一段。","hint_en":"Play these short hits in the room and hear how much reflection remains after each one; compare before and after treatment with the same phrase."}
```
:::

::: en
## The problem
Foam everywhere makes a room dull while the bass stays uneven; a few diffusers elsewhere make it feel open. They solve different problems.

## Physics or room
Absorption turns sound into heat; the coefficient runs from zero to one. Porous material works near a quarter wavelength, so thin foam absorbs mostly mids and highs. Bass needs depth, membrane traps or Helmholtz resonators. Diffusion spreads reflections without removing energy, softening comb filtering and flutter echo.

## Practice and judgement
Treat reflection points and corners first: porous absorbers 5 to 10 cm at the former, bass traps at the latter. Add diffusion on the rear wall and ceiling, keeping reflection. Judge by clap, speech and bass, one change at a time.

## What to listen for
Clap in the centre and listen for fast flutter. On cymbals, decide whether the tail decays naturally or is swallowed by high absorption. Play a solo voice and compare sibilance and tail.

## Common misunderstandings
More foam is not better; it works above the bass. Diffusers cannot replace bass traps. Carpet and curtains change the top but barely touch 100 Hz. An over-dead room makes mixes fail.

```audiolab
{"type":"instrument","gm":"Timpani","synth":"struck","phrase":["D2","A2","D3"],"label":"Three short hits, one room tail","label_en":"Three short hits, one room tail","hint":"Play these short hits in the room and hear how much reflection remains after each one; compare before and after treatment with the same phrase.","hint_en":"Play these short hits in the room and hear how much reflection remains after each one; compare before and after treatment with the same phrase."}
```
:::
