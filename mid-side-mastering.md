---
id: mid-side-mastering
site: prod
cat: A8
title: 中侧处理
title_en: Mid-Side Mastering
summary: 中间与两侧分开处理，宽度和低频各管一头。
summary_en: Processing mid and side separately lets width and low end be handled without undoing each other.
level: standard
tags: [母带, 中侧, 立体声, 相位]
tags_en: [mastering, mid-side, stereo, phase]
alias: [中侧处理, 中侧均衡, MS处理, mid-side, M/S mastering]
links:
  - "[[glossary:mid-side]]"
  - "[[glossary:stereo-technique]]"
  - "[[glossary:eq]]"
instances:
  - oga-000004 | 战斗音乐声部铺得开，中侧分开后中央与两侧的取舍听得出来
  - pdmx-000087 | 钢琴织体宽，侧声道一动就与低音争夺中心
  - musicnet-000090 | 贝多芬四重奏声部位置清楚，适合检查中置是否被拉空
sources:
  - Bob Katz, Mastering Audio.
  - Brainworx, bx_digital V3 user manual, mid-side EQ behaviour.
  - FabFilter, Pro-Q 4 user manual, mid/side processing mode.
updated: 2026-10-31
order: 456
---

::: zh
把侧声道整体推 3 dB，镲片散开了，人声却退后了半步。中侧处理分开的是位置，不是音量。

## 编码与还原

中声道是左右之和的一半，侧声道是左右之差的一半。还原时两路相加相减，回到左右。单声道播放只保留中声道，侧声道的内容完全消失。侧声道读数为负，说明两侧反相，折成单声道会互相抵消。这个性质决定了中侧处理的边界，放进侧声道的宽度，在单声道里收不回来。

## 分开做的四件事

- 侧声道在 120–200 Hz 以下高通，低频留在中间
- 侧声道窄带衰减，去掉刺耳的中高频
- 中声道轻压缩，稳住人声与底鼓
- 侧声道少量提升，只扩展 2 kHz 以上
- 全频段不动，只在中频加宽

## 操作与监听

先在中声道修平衡，再动侧声道。每次改动都按单声道检查，相关性表不要长期偏向负值。侧声道提升超过 2 dB，中央声像会变空。中声道提升低频比侧声道衰减更安全，前者不会把内容推出单声道。多段中侧处理要检查分频点，宽窄切换处的相位容易出问题。中侧压缩的启动与释放要和主链一致，否则两侧的呼吸不同步。

```audiolab
{"type":"instrument","gm":"Pad 2 (warm)","synth":"bowed","phrase":["C3","G3","C4","E4"],"label":"铺底和弦，听中间与两侧","label_en":"A sustained pad, listen to centre and sides","hint":"先听整体，再想侧声道被衰减后，哪一层会先退到中间","hint_en":"Hear the whole, then ask which layer falls back to the centre when the side is cut"}
```

## 哪里会坏

混音本身相位不稳，中侧处理会把问题放大。已经铺满的混响再加宽，尾巴盖住主唱。中侧提升放在限制器之后，峰值会重新越线。左右电平本来不齐，侧声道会带上一个偏移，听起来像声像歪了。修正声像先回混音，宽度只是收尾的修饰。
:::

::: en
Lift the side channel by 3 dB and the cymbals spread while the vocal steps back. Mid-side processing separates position, not level.

## Encode and decode

Mid is half the sum of left and right; side is half the difference. Decoding adds and subtracts them back into left and right. Mono playback keeps only mid, so everything in the side disappears. A negative side reading means the channels are out of polarity and cancel when folded to mono. That property defines the limits of the technique: width placed in the side cannot be recovered in mono.

## Four things to do separately

- High-pass the side below 120–200 Hz so the low end stays centred
- Cut a narrow band in the side to remove harsh upper mids
- Compress the mid gently to steady vocal and kick
- Lift the side a little, only above 2 kHz
- Leave the full band alone and widen the mids only

## Working and listening

Fix balance in the mid first, then move to the side. Check mono after every change, and do not let the correlation meter sit negative for long. More than 2 dB of side lift hollows out the centre. Lifting low end in the mid is safer than cutting it in the side, since the mid cannot push content out of mono. With multiband mid-side work, inspect the crossover, since phase is fragile where the bands split. Match mid-side compression attack and release to the main chain, or the two sides breathe at different rates.

```audiolab
{"type": "instrument", "gm": "Pad 2 (warm)", "synth": "bowed", "phrase": ["C3", "G3", "C4", "E4"], "label": "A sustained pad, listen to centre and sides", "label_en": "A sustained pad, listen to centre and sides", "hint": "先听整体，再想侧声道被衰减后，哪一层会先退到中间", "hint_en": "Hear the whole, then ask which layer falls back to the centre when the side is cut"}
```

## Where it breaks

If the mix itself has unstable phase, mid-side work magnifies it. A reverb that already fills the field becomes a tail over the vocal when widened further. Side lift after the limiter pushes peaks over the ceiling again. Uneven left and right levels put an offset in the side, which reads as a tilted image. Fix image problems in the mix; width is the last touch.
:::
