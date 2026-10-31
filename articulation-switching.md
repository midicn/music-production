---
id: articulation-switching
site: prod
cat: B4
order: 492
title: 奏法切换的工程做法
title_en: Articulation Switching in Practice
summary: 键位、控制器还是映射表，选错一条，换奏法就会吃掉音头。
summary_en: Keyswitch, controller or mapping table: choose badly and every articulation change eats the attack.
level: standard
tags: [奏法, 键位切换, 采样器, 工作流]
tags_en: [articulation, keyswitch, sampler, workflow]
alias: [奏法切换, 键位切换, 控制器切换, keyswitch, UACC, articulation map]
links:
  - "[[glossary:staccato]]"
  - "[[glossary:sampler]]"
  - "[[instrument:violin]]"
instances:
  - musicnet-000097 | 贝多芬第八弦乐四重奏第一乐章，分弓与连弓在同一主题里来回换
  - pdmx-000070 | 巴伯《弦乐柔板》，长连奏里偶尔的换弓最考验切换是否干净
  - musicnet-000248 | 坎比尼木管五重奏，五件管乐各有吐音与连音，切换逻辑不能只按弦乐写
sources:
  - Spitfire Audio 的 UACC 说明（官方文档），统一控制器切换奏法的约定。
  - Steinberg Cubase 的 Expression Maps 文档（官方文档）。
  - Elaine Gould, Behind Bars, Faber，奏法与记谱的对应。
updated: 2026-10-31
---

::: zh
同一个音，拉、弹、吐、滑是四件事。采样库把每件事录成一组样本，剩下的问题是：演奏时用什么动作告诉它换组。

## 换的不只是音色

按下 C4 时，库要决定放连奏、断奏还是泛音。这个决定发生在音符之前，而不是录完之后；等句子录完再改，音头已经错了。切换系统把演奏意图提前送到采样器，所以它既影响音色，也影响时间。切换点落在长音中间，前半句和后半句会像两件乐器。

## 五条切换路径

| 路径 | 怎么送 | 适合 | 风险 |
|---|---|---|---|
| 键位 | 在演奏音域下方按一个音 | 单人操作、录音 | 低音区被占用，忘按会沿用上一组 |
| CC32 / UACC | 控制器值对应奏法 | 统一多套库 | 不同库的值表不同，换库要重映射 |
| Program Change | 按通道换音色 | 多通道模板 | 通道膨胀，混响与声像要另配 |
| 映射表 | DAW 把记号翻成键位或 CC | 制谱同步、影视配乐 | 换宿主重做，导出 MIDI 丢映射 |
| 一奏法一轨 | 每轨固定音色 | 分轨交付、后期替换 | 轨道多，连奏跨轨困难 |

键位最直接，也最容易忘。控制器把整套库收进一个通道，代价是值表难搬。映射表让谱面记号直接驱动音色，离开这套工程就留在宿主里。

## 切换要跟着乐句走

切换点放在换气、换弓、休止附近，别落在长音中间。一个连音线内反复换奏法，采样器来不及释放前一组，会出现两层音头。写谱时把奏法写在音符上，演奏时把它当呼吸的一部分；后期补键位，往往补不出原来的语气。

## 延迟与追发

采样库换组要预读，第一声可能晚几毫秒到几十毫秒。模板里给整套乐器加负延迟，能把听感拉回拍点，但实时演奏会变得别扭，录音时先关掉。播放从中途开始时，DAW 要追发当前奏法；没有 chase 的宿主会从默认音色开始，头一小节听起来像换了一件乐器。循环段落回到开头，也要检查键位是否被重置。

## 切碎了会怎样

每两个音换一次奏法，听起来像演示库的清单，不像音乐。键位压进大提琴的 C 弦音域，低音声部就没法弹；控制器和颤音共用 CC1 时，换奏法会顺手改掉揉弦。最隐蔽的失败是导出：工程里听着对，导成 MIDI 给别人，映射表留在宿主里，收到的只是一串普通音符。

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["A4","A4","A4","E4","E4","E4"],"label":"同一句的两种奏法","label_en":"One phrase, two articulations","hint":"前三个音连、后三个音断，切换点若压在音头上，会像换了乐器","hint_en":"Three connected notes, then three detached; a switch on the attack sounds like a different instrument"}
```
:::

::: en
One pitch can be bowed, plucked, tongued or slid. A sample library records each action as its own group, and the practical question is how the player tells it to switch.

## More than timbre changes

Press C4 and the library must choose legato, staccato or harmonic. That choice happens before the note, not after the take; correct it later and the attack is already wrong. A switching system sends intent ahead of the note, so it shapes timing as well as tone. Put the switch in the middle of a long note and the phrase sounds like two instruments.

## Five routes

| Route | How it is sent | Fits | Risk |
|---|---|---|---|
| Keyswitch | A note below the playing range | One player, recording | Low range is occupied; forget it and the last group stays |
| CC32 / UACC | A controller value selects the group | Several libraries under one rule | Value tables differ; remap when the library changes |
| Program Change | A channel selects the patch | Multi-channel templates | Channel count grows; reverb and pan need separate work |
| Mapping table | The DAW translates marks into keys or CC | Score sync, film work | Rebuild in another host; MIDI export drops the map |
| One track per articulation | Each track holds one patch | Stem delivery, later replacement | Many tracks; legato across tracks is hard |

Keyswitches are direct and easy to forget. Controllers fit a whole library into one channel, at the cost of a template that is hard to move. A mapping table lets marks on the page drive the sound, but the relationship stays inside that project.

## Switch with the phrase

Place switches near breaths, bow changes and rests, not inside a sustained note. Change articulation repeatedly under one slur and the sampler cannot release the previous group, leaving two attacks. Write the articulation on the note and treat it as part of the breath; keyswitches added afterwards rarely recover the original phrasing.

## Latency and chase

A library pre-reads when it changes group, so the first note can arrive milliseconds late. Negative delay on the whole instrument pulls the sound back onto the beat, but it feels wrong under the fingers and should be off when recording. Start playback mid-phrase and the DAW must chase the current articulation; a host without chase begins on the default patch, and the first bar sounds like another instrument. After a loop, check that the keyswitch was reset.

## What breaks when it is chopped up

Changing articulation every two notes sounds like a library demo, not music. A keyswitch set too low covers the cello's C string; when articulation and vibrato share CC1, a switch also changes the vibrato. The quietest failure is export: the project plays correctly, but the MIDI file carries plain notes and the map stays in the host.

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["A4","A4","A4","E4","E4","E4"],"label":"One phrase, two articulations","label_en":"One phrase, two articulations","hint":"Three connected notes, then three detached; a switch on the attack sounds like a different instrument","hint_en":"Three connected notes, then three detached; a switch on the attack sounds like a different instrument"}
```
:::
