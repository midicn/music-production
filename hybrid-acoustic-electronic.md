---
id: hybrid-acoustic-electronic
site: prod
cat: A2
order: 310
title: 混合编制
title_en: Hybrid Acoustic and Electronic Scoring
summary: 真乐器管表情，合成器管稳定，先分工再谈音色。
summary_en: Real instruments carry expression and synths carry stability; assign the roles before choosing sounds.
level: standard
tags: [编曲, 混合编制, 合成器, 配器]
tags_en: [arranging, hybrid ensemble, synthesizer, orchestration]
alias: [混合编制, 真乐器与合成器, 电子管弦, hybrid scoring, acoustic electronic]
links:
  - "[[glossary:timbre]]"
  - "[[glossary:sidechain]]"
  - "[[glossary:texture]]"
  - "[[instrument:software-synth]]"
instances:
  - oga-000047 | 钢琴、电钢、失真吉他、合成贝斯与弦乐同场，各层分工听得出来（CC0）
  - oga-000052 | 钢琴、颤音琴、钢弦吉他、合成贝斯与合成弦乐并置，真假比例清楚（CC BY 4.0）
  - oga-000064 | 钢琴、管钟、大提琴与方波、锯齿主音轮流领奏，声学与电子交替（CC0）
sources:
  - Buhler, Nevelsteen and Deemer, Hearing the Movies（Oxford University Press）关于混合配乐与音色分层的章节
  - Karen Collins, Game Sound（MIT Press）关于电子与管弦混合编制的章节
  - Curtis Roads, The Computer Music Tutorial（MIT Press）关于合成音色与空间处理的章节
updated: 2026-10-31
---

::: zh
真弦乐加合成低音，最常见的失败是两者各自都好听，合起来像两首歌叠在一起。问题不在音色，而在分工：它们抢了同一个角色。

## 先分工，再挑音色

混合编制先列角色：脉冲、低频、和声重量、纹理、高点。每个角色只给一个主承担者。常见分工是合成器负责脉冲与低频，真乐器负责和声重量与表情，采样打击负责节奏的锐度。角色定完再挑音色，才不会出现三件乐器都在做同一件事。若两件都想承担同一角色，就让其中一件改走音区或改走节奏。

## 空间与低频

真乐器自带房间，合成器默认是干的。把两者放进同一个空间，靠的不是给合成器加一个大混响，而是让它的早期反射与真乐器接近：短预延迟、相近的混响时间、少量高频吸收。如果真乐器录得很近，也可以把它的房间压小去迁就合成器。关键是全曲统一，不要主歌一个空间、副歌换另一个。

低频最容易打架。合成低音与贝斯、底鼓与低音提琴，通常只留一个主，另一个让位：错开八度、错开时间，或用侧链让几毫秒。别用均衡硬切来分，切出来的洞会让低频变薄。判断方法很简单：独奏低音组，听哪一件在定义音高；定义音高的那件留下，另一件改成质感层。

## 动态与领奏

真乐器的价值在力度、换气与音头的微小差异；合成器的价值在每一拍都一样。让合成器守住时间与音准，让真乐器在长音、渐强与句尾做文章。全曲都交给合成器会显得机械，全曲都交给真乐器又难保持力度，两者交替领奏，段落之间才有呼吸。

| 角色 | 真乐器 | 合成器 | 注意 |
|---|---|---|---|
| 低频 | 贝斯、大提琴、低音提琴 | 合成贝斯、次低音 | 只留一个定义音高 |
| 脉冲 | 打击、拨弦 | 琶音、序列 | 不要两层同拍 |
| 和声 | 弦乐、铜管、合唱 | 铺底 Pad | 音区错开，别叠满 |
| 纹理 | 弓杆、泛音、气声 | 噪声、调制 Pad | 控制密度 |
| 高点 | 小号、齐奏 | Lead、Riser | 一次只给一个 |

## 加倍与真空

最常见的坏法是把所有东西都加倍：弦乐加合成弦乐，贝斯加合成低音，鼓加电子鼓，结果每一层都在抢同一块频段。第二种是空间不统一，真乐器在音乐厅，合成器在真空里。第三种是动态被压平，合成器的稳定把真乐器的表情也磨掉了。判断标准是撤掉合成器后音乐是否还站得住；站不住，说明它在替真乐器干活，而不是补充。

```audiolab
{"type":"instrument","gm":"Synth Bass 1","synth":"plucked","phrase":["D2","D2","F2","G2","A2","G2","F2","D2"],"label":"低频只能有一个主人","label_en":"Only one owner for the low end","hint":"听合成低音与弦乐低音是否在抢同一个音区","hint_en":"Hear whether synth and string bass fight for one register"}
```
:::

::: en
Real strings plus a synth bass usually fail in the same way: each sounds good alone, and together they sound like two songs stacked. The trouble is not timbre but role, because both are doing the same job.

## Assign roles before sounds

List the roles first: pulse, low end, harmonic weight, texture, peak. Give each role one primary owner. A common split has synths handling pulse and low end, real instruments carrying weight and expression, and sampled percussion sharpening the rhythm. Choose sounds after that, or three instruments end up doing one thing. If two want the same role, move one to a different register or a different rhythm.

## Space and low end

Real instruments bring a room; synths arrive dry. Putting them in one space is not a matter of a large reverb on the synth but of matching early reflections: short pre-delay, a similar decay, a little high-frequency absorption. If the real instruments were recorded close, shrink their room instead to meet the synth. What matters is consistency; do not give the verse one space and the chorus another.

The low end fights hardest. Between synth bass and bass guitar, or kick and double bass, keep one as the owner and make the other yield by octave, by timing, or by a few milliseconds of sidechain. Do not split them with a hard equaliser cut; the hole thins the whole bottom. Solo the low group and hear which instrument defines the pitch. Keep that one and turn the other into a texture layer.

## Dynamics and taking the lead

A real instrument is valuable for small differences in attack, breath and force; a synth is valuable because every beat is identical. Let the synth hold time and tuning while the real players shape long notes, crescendos and phrase endings. An all-synth arrangement sounds mechanical, an all-acoustic one struggles to stay even, and alternating the lead gives the sections room to breathe.

| Role | Acoustic | Electronic | Watch for |
|---|---|---|---|
| Low end | Bass, cello, double bass | Synth bass, sub | One pitch owner only |
| Pulse | Percussion, plucked strings | Arpeggio, sequencer | No two layers on the beat |
| Harmony | Strings, brass, choir | Pad | Separate registers, do not stack |
| Texture | Col legno, harmonics, breath | Noise, modulated pad | Keep density in check |
| Peak | Trumpet, unison | Lead, riser | One at a time |

## Doubling and vacuum

The usual failure is doubling everything: strings plus synth strings, bass plus synth bass, drums plus electronic drums, until every layer fights for the same band. The second is mismatched space, real instruments in a hall and synths in a vacuum. The third is flattened dynamics, where the steadiness of the synth sands off the players' expression. A simple test: mute the synths and see whether the music still stands. If it collapses, they were doing the instruments' job rather than adding to it.

```audiolab
{"type": "instrument", "gm": "Synth Bass 1", "synth": "plucked", "phrase": ["D2", "D2", "F2", "G2", "A2", "G2", "F2", "D2"], "label": "Only one owner for the low end", "label_en": "Only one owner for the low end", "hint": "Hear whether synth and string bass fight for one register", "hint_en": "Hear whether synth and string bass fight for one register"}
```
:::
