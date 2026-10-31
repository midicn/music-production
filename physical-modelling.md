---
id: physical-modelling
site: prod
cat: B3
title: 物理建模
title_en: Physical Modelling
summary: 用弦与管的物理规律，实时算出共鸣。
summary_en: Calculate the resonance of strings and tubes in real time from physical rules.
level: standard
tags: [合成, 物理建模, 拨弦, 共鸣]
tags_en: [synthesis, physical modelling, plucked string, resonance]
alias: [物理建模, 物理模型, 波导合成, physical modelling, waveguide]
links:
  - "[[glossary:timbre]]"
  - "[[instrument:classical-guitar]]"
  - "[[instrument:violin]]"
  - "[[period:contemporary]]"
instances:
  - oga-000195 | 尼龙弦与闷音吉他交替，拨弦起音与琴体共鸣接近物理模型
  - oga-000097 | 三味线与钢琴并置，拨弦的短促衰减与琴弦张力感清楚
  - oga-000134 | 日本筝旋律配气氛铺底，拨弦的共鸣与按弦变化可辨
sources:
  - Julius O. Smith, Physical Audio Signal Processing.
  - Curtis Roads, The Computer Music Tutorial.
updated: 2026-10-28
---

::: zh
## 要解决的事

不采样、不叠加正弦，能不能让合成器发出像真琴弦、真管体的声音？物理建模不录声音，而是把发声机制写成实时模型。

## 背后的机制

大多数模型分激励与共鸣两部分。拨弦时，一小段噪声或脉冲进入延迟线，延迟长度决定音高，反馈路径里的低通决定高频衰减，这就是 Karplus-Strong 形态。管乐用波导模拟管内压力波，管长决定音高，开口与指孔改变共鸣峰。阻尼、张力、吹气噪声与琴体滤波再进一步修饰。模型越接近真实，越需要处理非线性与稳定性。

## 数值怎么变成声音

阻尼大则音尾收得快，像手掌闷住琴弦；阻尼小则余音长，像空弦。激励决定是拨、是击还是吹，琴体共鸣决定中低频的厚薄。张力与硬度改变音头亮度，吹气噪声增加气感。参数极端时，模型可能自激或失控。

## 耳朵要抓的点

先听尼龙弦与闷音吉他的交替，注意起音的软硬与衰减长度。再听三味线，拨弦短促、张力感强，尾音收得干净。最后听日本筝，按弦后音高与共鸣同时变化，这是采样很难逐音重现的。

```audiolab
{"type":"instrument","gm":"Acoustic Guitar (nylon)","synth":"plucked","phrase":["E3","B3","E4","G4"],"label":"尼龙弦的拨弦","label_en":"A plucked nylon string","hint":"先听起音与余音，再想象阻尼加大，尾音会立刻收短；物理模型调的就是这根弦的损耗","hint_en":"Hear the attack and tail, then imagine more damping shortening the tail at once; a physical model tunes exactly that loss"}
```

## 容易弄错的

把物理建模当成采样，它算的是机制而不是回放录音；以为模型一定比采样真实，参数不对时会更假；以为它只能做原声乐器，电吉他音箱与金属板也能建模。
:::

::: en
## The problem to solve

Without sampling or sines, can a synth sound like a string or tube? Physical modelling records no sound; it writes the mechanism as a real-time model.

## The mechanism

Most models split into excitation and resonator. For a plucked string, a noise burst enters a delay line; the delay length sets pitch, and a low-pass in the feedback path sets how fast highs die away, the basic Karplus-Strong form. Wind instruments use waveguides to model pressure in a tube, where length sets pitch and openings shift resonances. Damping, tension, breath and body filtering refine the result. Closer models must handle nonlinearity and stability.

## From numbers to sound

More damping shortens the tail, like a hand muting a string; less damping lets it ring. Excitation decides pluck, strike or breath; body resonance sets low-mid weight. Tension and stiffness brighten the attack; breath adds air to a wind model. At extremes, a model can self-oscillate or run away.

## What the ear should catch

Hear nylon and muted guitar alternate, noting the hardness of the attack and the length of decay. Then hear the shamisen, short and tense, with a clean tail. Finally hear the koto, where pressing a string changes pitch and resonance together, a detail samples struggle to reproduce.

```audiolab
{"type":"instrument","gm":"Acoustic Guitar (nylon)","synth":"plucked","phrase":["E3","B3","E4","G4"],"label":"A plucked nylon string","label_en":"A plucked nylon string","hint":"Hear the attack and tail, then imagine more damping shortening the tail at once; a physical model tunes exactly that loss","hint_en":"Hear the attack and tail, then imagine more damping shortening the tail at once; a physical model tunes exactly that loss"}
```

## Easy to get wrong

That physical modelling is sampling, when it computes a mechanism; that a model is more real, when wrong parameters make it faker; that it only handles acoustic instruments, when cabinets and metal plates can be modelled too.
:::
