---
id: granular-synthesis
site: prod
cat: B3
title: 粒子合成
title_en: Granular Synthesis
summary: 把声音切成毫秒碎片，再重新排成云。
summary_en: Cut sound into millisecond grains and rearrange them into a cloud.
level: standard
tags: [合成, 粒子, 纹理, 时间拉伸]
tags_en: [synthesis, granular, texture, time stretch]
alias: [粒子合成, 颗粒合成, 云状合成, granular, granular synthesis]
links:
  - "[[glossary:timbre]]"
  - "[[glossary:eq]]"
  - "[[instrument:software-synth]]"
  - "[[period:contemporary]]"
instances:
  - oga-000098 | 海浪与掌声采样被切成背景层，碎片重复形成的云状纹理清楚
  - oga-000079 | 金属铺底与音效层交叠，短碎音散布在长音之间
  - oga-000167 | 山洞场景叠入海浪与音效，细碎声粒在宽声场里浮动
sources:
  - Curtis Roads, Microsound — grain windows and clouds checked, not quoted
  - Udo Zölzer, DAFX — Digital Audio Effects, granular processing chapter — background checked, not quoted
updated: 2026-10-28
---

::: zh
## 起点：一个问题

两秒的声音怎样变成十分钟的云，又怎样在不改变音高的情况下变慢？粒子合成把声音切成碎片，再决定它们何时、以什么音高出现。

## 声音是怎么来的

每个粒子通常几毫秒到百毫秒，带窗函数，避免切口咔哒。播放位置可在原音频里慢移，密度决定同一时刻叠多少层。密度低时听到一颗颗颗粒，密度高时互相重叠，变成连续的云。音高由每颗粒子的播放速率决定，与位置移动分开，所以能独立拉伸时间。粒子相位不齐时，高频会互相抵消，产生柔化或金属感。

## 旋钮与耳朵

粒子长度决定粗糙度，越短越像金属与噪点，越长越保留原音色。密度决定点状还是云状，喷散量决定粒子偏离中心的距离。位置移动慢则像时间拉伸，快则像扫描。音高偏移让云整体升降，窗形影响边缘软硬。

## 耳朵要抓的点

先听海浪采样铺成背景的质感，注意是连续水声还是一颗颗碎片。再听金属铺底，判断高频被保留还是抹平。最后听山洞场景，留意细碎声粒在声场里浮动，而不是混响拖尾。

```audiolab
{"type":"instrument","gm":"Pad 6 (metallic)","synth":"bowed","phrase":["C4","E4","G4","C5"],"label":"可被切碎的金属铺底","label_en":"A metallic pad ready to be cut","hint":"先听连续的长音，再想象它被切成 30 毫秒的粒子、每秒撒 40 颗；连续的表面会变成云","hint_en":"Hear the continuous pad, then imagine it cut into 30 ms grains at 40 per second; the surface becomes a cloud"}
```

## 容易弄错的

把粒子合成当成混响，混响是反射，粒子是重排；以为颗粒越小越平滑，过小会产生边带与金属味；以为它只能做实验音乐，电影与流行里的纹理常来自它。
:::

::: en
## Starting point: a problem

How does two seconds become a ten-minute cloud, or slow without changing pitch? Granular synthesis cuts audio into short pieces and decides when each appears and its pitch.

## Where the sound comes from

A grain lasts a few milliseconds to about a hundred, with a window to avoid clicks. The read position drifts through the source, and density sets how many layers overlap. At low density you hear grains; at high density they overlap into a cloud. Pitch comes from each grain's playback rate, separate from position, so time stretches independently. When grain phases disagree, high frequencies cancel and the result softens or turns metallic.

## Knobs and ears

Grain length sets roughness; short grains sound metallic, long ones keep the original tone. Density decides dotted or clouded, and spray sets how far grains stray from the centre. Slow position moves stretch time, fast ones scan. Pitch offset shifts the whole cloud, and the window shape softens or hardens edges.

## What the ear should catch

Hear the seashore as a bed and ask whether it is continuous water or repeated fragments. Then hear the metallic pad and judge whether the top survives or is smoothed away. Finally hear the cave scene and notice fine grains floating across the field rather than a reverb tail.

```audiolab
{"type":"instrument","gm":"Pad 6 (metallic)","synth":"bowed","phrase":["C4","E4","G4","C5"],"label":"A metallic pad ready to be cut","label_en":"A metallic pad ready to be cut","hint":"Hear the continuous pad, then imagine it cut into 30 ms grains at 40 per second; the surface becomes a cloud","hint_en":"Hear the continuous pad, then imagine it cut into 30 ms grains at 40 per second; the surface becomes a cloud"}
```

## Easy to get wrong

That granular is a reverb, when reverb reflects and grains rearrange; that smaller grains are smoother, when too small adds sidebands; that it belongs only to experimental music, when film and pop textures often use it.
:::
