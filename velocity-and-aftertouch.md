---
id: velocity-and-aftertouch
site: prod
cat: B1
title: 力度与触后
title_en: Velocity and Aftertouch
summary: 力度写在 Note On 的第二个字节，触后是按住之后继续加的表情。
summary_en: Velocity sits in the second Note On byte, while aftertouch adds pressure held after the key.
level: standard
tags: [MIDI, 力度, 触后, 表情]
tags_en: [MIDI, velocity, aftertouch, expression]
alias: [力度, 触后, aftertouch, 通道压力, 复音触后]
links:
  - "[[glossary:velocity]]"
  - "[[glossary:midi-protocol]]"
  - "[[instrument:drum-kit]]"
instances:
  - groove-000693 | 18 条复音触后落在 49 与 55 号镲上，压力从 127 跳到 0，像镲片止音
  - groove-000507 | 11513 个音符用到 125 个力度值，音头层次最密
  - musicnet-000315 | 钢琴演奏保留 106 个力度级，弱奏与重奏分得很开
sources:
  - MIDI 1.0 规范对 Note On 力度与两类触后的定义，参考 MMA 公开规范。
  - 本库 C1 文件的力度分布与复音触后统计，由本地 SMF 解析脚本核对，数值随文件而定
updated: 2026-10-28
---

::: zh
同一个音，轻按与重按的差别常被当成音量。触后更常被忽略，键压下去之后的压力，其实还能单独成消息。

## 问题

钢琴卷帘里画的是力度柱，推子推的是音量，两者一混，表情就只剩响与轻。弦乐长音按住之后没有变化，也常常不是音源的问题，而是根本没有发触后。

## 协议或消息

Note On 的状态字节是 0x9n，后跟键号与力度，力度取 1 到 127，取 0 时按 Note Off 处理。通道压力是 0xDn，只带一个字节，作用于整条通道。复音触后是 0xAn，带键号与压力，只作用于那个音。力度在音头发一次，触后可以连续发。鼓轨常用复音触后给镲片止音。

## 参数与做法

钢琴把常用力度留在 20 到 110，两头留余量。弦乐长音用通道压力做渐强，MPE 下则用每音压力。采样器要设力度层，否则数值只改音量。触后曲线在键盘上校准，别直接信默认值。

## 听什么

力度差二十以上，重音位置就会移动。触后让长音在按住之后继续变化，像逐渐加重的揉弦；止音触后则让镲片突然收住。

## 常见误解

力度不是音量，音源可以把它映射到亮度或采样层。触后不是弯音。没有触后的键盘，也能用 CC1 代替一部分表情。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","D4","E4","G4"],"label":"力度不是音量","label_en":"Velocity is not volume","hint":"听四个音的音头差别，想象力度字节从 30 走到 110","hint_en":"Hear the attacks differ and picture the velocity byte moving from 30 to 110"}
```
:::

::: en
Soft and hard presses are often treated as quiet and loud. Aftertouch is missed, though pressure under the finger can travel as its own message.

## The problem

The piano roll draws velocity bars while the fader moves volume; mixing them flattens expression. A string note that refuses to change often lacks aftertouch, not a better patch.

## Protocol or message

Note On uses 0x9n with key and velocity from 1 to 127, where 0 means Note Off. Channel pressure is 0xDn with one byte and affects the whole channel. Polyphonic aftertouch is 0xAn with key and pressure, affecting one note. Velocity is sent at the attack, while aftertouch can stream. Drum tracks use poly aftertouch to choke cymbals.

## Settings and practice

Keep piano velocity inside 20 to 110 with headroom. Shape a long string note with channel pressure, or per-note pressure under MPE. Set velocity layers in the sampler, or the value changes only level. Calibrate the aftertouch curve on the keyboard, not the default.

## What to listen for

A velocity gap above twenty moves the accents. Aftertouch lets a held note keep changing, like a vibrato that deepens, while choke aftertouch cuts a cymbal short.

## Common misunderstandings

Velocity is not volume, as a sampler may map it to brightness or a layer. Aftertouch is not pitch bend. A keyboard without aftertouch can fake some expression with CC1.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "D4", "E4", "G4"], "label": "Velocity is not volume", "label_en": "Velocity is not volume", "hint": "听四个音的音头差别，想象力度字节从 30 走到 110", "hint_en": "Hear the attacks differ and picture the velocity byte moving from 30 to 110"}
```
:::
