---
id: wavetable-synthesis
site: prod
cat: B3
title: 波表合成
title_en: Wavetable Synthesis
summary: 一张单周期波表，让音色在演奏中滑动。
summary_en: A table of single-cycle waves lets the timbre slide while you play.
level: standard
tags: [合成, 波表, 扫描, 数字音色]
tags_en: [synthesis, wavetable, scanning, digital timbre]
alias: [波表合成, 波表, 扫描合成, wavetable, wavetable synthesis]
links:
  - "[[glossary:timbre]]"
  - "[[instrument:wavetable-synthesis]]"
  - "[[instrument:software-synth]]"
  - "[[period:modern]]"
instances:
  - oga-000142 | 场景音乐里主音与铺底多次换色，像波表在不同帧之间移动
  - oga-000116 | 洞穴场景用 charang 主音与金属铺底，音色明暗随段落滑动
  - oga-000163 | 锯齿主音配扫频铺底，适合听同一波形被连续塑形
sources:
  - Curtis Roads, The Computer Music Tutorial.
  - Udo Zölzer, DAFX.
updated: 2026-10-28
---

::: zh
## 这件事难在哪

固定波形只能靠滤波器改明暗，能不能让波形本身在演奏中变形？波表合成把单周期波形排成表，让音色滑动。

## 工作方式

波表存的不是几秒的录音，而是一组单周期波形，每帧只含一个周期。播放时按音高读出某一帧，再按位置参数在相邻帧之间插值。位置可由 LFO、包络或力度推动，按住的音会从柔和变尖，或从方波滑向金属。表必须限带，否则高音区会混叠。多个波表振荡器失谐叠加，还能得到更宽的立体声。

## 数值怎么变成声音

表的种类决定音色的起点，位置决定当前帧，扫描量与扫描速率决定运动幅度与快慢。慢扫像铺底在呼吸，快扫像有节奏的摆动，位置突变则有数字化的台阶感。失谐与齐奏让声音变宽，滤波器负责收掉过亮的高频。

## 耳朵要抓的点

先听场景音乐里主音换色的段落，注意音色是连续滑动还是突然跳帧。再听洞穴场景的金属铺底，判断明亮度是否随段落推进。最后听扫频铺底，把注意力放在波形变化上，而不是滤波扫动。

```audiolab
{"type":"instrument","gm":"Pad 6 (metallic)","synth":"bowed","phrase":["C4","E4","G4","C5"],"label":"金属铺底的音色移动","label_en":"A metallic pad on the move","hint":"先听当前这一帧，再想象位置在八小节里从柔和滑到尖锐；亮度会变，但音高不动","hint_en":"Hear the current frame, then imagine the position sliding from soft to sharp over eight bars; brightness moves while pitch stays put"}
```

## 容易弄错的

把波表当成采样，采样是一段长音频，波表只是一串单周期；以为波表只能做电子舞曲，它也能做安静的铺底；以为表越多越好，选错表再扫也只是在错的方向上移动。
:::

::: en
## What makes it hard

A fixed waveform can only be reshaped by a filter, so can the wave morph? Wavetable synthesis lines up single-cycle waves and lets the timbre slide.

## The working principle

A wavetable stores single-cycle waves, not seconds of audio; each frame holds one period. Playback reads one frame at the played pitch and interpolates between frames by position. Position can be pushed by an LFO, envelope or velocity, so a held note moves from soft to sharp, or from square toward metal. Tables must be band-limited or high notes alias. Several detuned wavetable oscillators widen the stereo image.

## From numbers to sound

The table sets the family, position the current frame, and scan amount and rate how far and fast it travels. A slow scan breathes, a fast one sways, and a hard jump steps digitally. Detune and unison widen the sound, while the filter trims an over-bright top.

## What the ear should catch

Hear the passage where the lead changes colour and ask whether it slides or jumps. Then hear the metallic cave bed and judge whether brightness follows the section. Finally hear the sweeping pad and focus on the wave changing rather than on a filter sweep.

```audiolab
{"type":"instrument","gm":"Pad 6 (metallic)","synth":"bowed","phrase":["C4","E4","G4","C5"],"label":"A metallic pad on the move","label_en":"A metallic pad on the move","hint":"Hear the current frame, then imagine the position sliding from soft to sharp over eight bars; brightness moves while pitch stays put","hint_en":"Hear the current frame, then imagine the position sliding from soft to sharp over eight bars; brightness moves while pitch stays put"}
```

## Easy to get wrong

That a wavetable is a sample, when a sample is long audio and a wavetable is single cycles; that wavetables belong only to dance music, when they also make quiet beds; that more tables are better, when a wrong table scanned hard only moves the wrong way.
:::
