---
id: headphones-vs-monitors
site: prod
cat: A5
title: 监听耳机与音箱
title_en: Headphones versus Monitors
summary: 耳机揭示细节，音箱暴露房间，两者不能互相替代。
summary_en: Headphones reveal detail; speakers reveal the room. Neither can replace the other.
level: standard
tags: [监听耳机, 监听音箱, 串扰, 声像, 翻译检查]
tags_en: [headphones, studio monitors, crosstalk, imaging, translation]
alias: [耳机监听, 音箱监听, 交叉馈送, headphones, monitors, crossfeed]
links:
  - "[[glossary:headphone-mix]]"
  - "[[glossary:monitoring]]"
  - "[[glossary:crossfeed]]"
  - "[[instrument:double-bass]]"
instances:
  - pdmx-000237 | 钢琴与贝斯的爵士，低频与声像都清楚，适合耳机与音箱对照（C1）
  - essen-000517 | 单声部民歌，没有混音加工，能听出两种监听方式对中频的改写（C1）
  - atepp-001114 | 肖邦第一叙事曲，钢琴动态与余响长，适合比较耳机与音箱的衰减（C1）
sources:
  - Toole, Floyd，Sound Reproduction（Focal Press）— 耳机与房间听觉章节核对，未引用
  - Senior, Mike，Mixing Secrets for the Small Studio（Focal Press）— 监听对照章节核对，未引用
updated: 2026-10-28
---

::: zh
## 问题
耳机里低音结实、声像很宽，换到音箱上却变薄、变窄；反过来，音箱上平衡的混音在耳机里可能中频凹陷。两种监听各漏掉不同信息。

## 物理或房间
耳机绕过房间，左右耳几乎隔离，没有串扰，声像能比音箱更宽；封闭式还会加重低频。音箱让两耳同时听到两只单元，产生串扰，也激发房间模式。耳机的低频到不了身体，音箱的低频会让房间一起振动。

## 做法与判断
把耳机当检查工具，不当唯一判决。用音箱定平衡、声场与低频；用耳机查细节、噪声与齿音。响度匹配后再比较；耳机上加一点交叉馈送。最后用手机与车载做翻译检查。

## 听什么
同一段混音，先听贝斯尾音在耳机里多长，再听它在房间里是否拖成一片。听人声居中与混响深度，耳机容易把混响听成左右包裹，音箱更像前方空间。最后按单声道确认宽度。

## 常见误解
耳机不是更准确，只是去掉房间这个变量。监听音箱也不一定更高级，房间没处理时谎言更多。只在一副耳机上混音，容易把声像拉太宽。

```audiolab
{"type":"instrument","gm":"Contrabass","synth":"bowed","phrase":["E1","A1","D2","G2"],"label":"低频下潜，耳机与音箱各听一遍","label_en":"Low end, once on headphones and once on speakers","hint":"先在耳机上听下潜与尾音，再用音箱重放；房间会把某几个低音加强或抵消。","hint_en":"Hear the depth and tail on headphones first, then on speakers; the room will boost or cancel some of these notes."}
```
:::

::: en
## The problem
Headphones can sound deep and wide, then the same mix turns thin and narrow on speakers; a speaker-balanced mix may sound hollow on headphones. Each misses different information.

## Physics or room
Headphones bypass the room and isolate the ears, so crosstalk almost vanishes and images can be wider; sealed models add bass. Speakers feed both ears from both boxes, creating crosstalk and modes. Headphone bass never reaches the body; speaker bass makes the room vibrate.

## Practice and judgement
Use headphones as a check, not the only verdict. Set balance, space and low end on speakers; use headphones for detail, noise and sibilance. Match levels before comparing, add light crossfeed, and finish on a phone and in a car.

## What to listen for
Hear how long the bass tail lasts on headphones, then whether it smears in the room. Listen to vocal centre and reverb depth; headphones wrap reverb around the head, speakers place it in front. Finally check mono.

## Common misunderstandings
Headphones are not more accurate; they remove the room. Monitors are not automatically better when the room is untreated. One pair over-widens images and overdoes bass.

```audiolab
{"type":"instrument","gm":"Contrabass","synth":"bowed","phrase":["E1","A1","D2","G2"],"label":"Low end, once on headphones and once on speakers","label_en":"Low end, once on headphones and once on speakers","hint":"Hear the depth and tail on headphones first, then on speakers; the room will boost or cancel some of these notes.","hint_en":"Hear the depth and tail on headphones first, then on speakers; the room will boost or cancel some of these notes."}
```
:::
