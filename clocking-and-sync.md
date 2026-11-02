---
id: clocking-and-sync
site: prod
cat: A4
title: 时钟与同步
title_en: Clocking and Sync
summary: 多台数字设备各自计时就会错位，全场只跟一个主时钟
summary_en: Digital devices that keep their own time will drift apart. One master clock, everyone else follows.
level: standard
tags: [录音, 时钟, 同步]
tags_en: [recording, clock, sync]
alias: [字时钟, 主时钟, 时钟同步, 时钟漂移, word clock, clock sync, jitter]
links:
  - "[[glossary:sample-rate]]"
  - "[[glossary:latency]]"
  - "[[instrument:organ]]"
instances:
  - mutopia-000180 | 持续音的音乐参照，不包含设备失锁或时钟抖动记录 | Sustained musical notes without a device lock-loss or clock-jitter recording
  - groove-000775 | 鼓组节拍参照，不能据此判断数字接口同步 | Drum-beat reference that does not establish digital-interface synchronisation
  - m21-000030 | 多声部同时进入的谱面参照，不是独立设备时钟的测量 | A scored entry of multiple voices, not a measurement of independent device clocks
sources:
  - "https://archiv.rme-audio.de/old/english/download/wcm_e.pdf"
  - Watkinson, The Art of Digital Audio, clocking and interfacing chapters
  - AES Convention paper on word clock distribution and jitter
updated: 2026-11-02
---

::: zh
## 问题

直接交换数字音频的设备需要兼容的采样率和同步关系，否则可能发生样点丢失、重复、爆音或失锁。通常在一个同步域内选一台主时钟，其余设备跟随；带异步采样率转换的接口可以连接不同的时钟域。

## 信号链

主时钟可以是转换器、声卡或独立时钟，经字时钟、ADAT 或嵌入的数字流分发。每台从设备锁定之后，采样点才落在同一张时间网格上。

## 摆位与参数

选一台最稳定的设备做主时钟，其余设为外部同步。全场采样率必须一致，48 kHz 工程里不要留 44.1 kHz 设备。时钟线尽量短，避免过长的菊花链；等锁定指示灯稳定再开录。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"q q q q","bpm":120,"label":"规则节拍","label_en":"Regular pulse","hint":"这里只演示规则节拍，不改变设备的字时钟或模拟失锁。时钟同步应查看实际设备的锁定状态。","hint_en":"This demonstrates a regular pulse, not Word Clock changes or loss of lock. Check actual device lock status for sample-clock synchronisation."}
```

## 听什么

先看设备的 Sync/Lock 指示、采样率和数字输入错误记录，再沿信号链逐段排查。持续录一段音频，检查是否丢锁、出现不连续样点或爆音；不要只凭“高频发毛”或“低频松散”判断时钟优劣。普通 MIDI 试听不会改变音频接口的物理时钟，也不能模拟这类故障。

## 常见误解

- Word Clock 管采样同步，MIDI Clock 管节拍，MTC 管时间位置，三者不可混称。
- 外接昂贵时钟不保证改善音质，先保证拓扑、终端和锁定设置正确。
- 带采样率转换的数字输入应按设备说明设置，不能强套单一主从规则。
:::

::: en
## The problem

Devices exchanging digital audio need compatible sample rates and synchronisation. Otherwise samples may be lost or repeated, causing clicks or loss of lock. A typical synchronisation domain has one master and followers; an asynchronous sample-rate converter can bridge different clock domains.

## Signal chain

The master can be a converter, an interface or a dedicated clock, distributed over word clock, ADAT or an embedded digital stream. Once each slave locks, its samples fall on the same time grid.

## Placement and settings

Choose the most stable device as master and set the rest to external sync. Every device must run the same rate; do not leave a 44.1 kHz unit in a 48 kHz session. Keep clock cables short, avoid long daisy chains, and wait for lock before recording.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"q q q q","bpm":120,"label":"Regular pulse","label_en":"Regular pulse","hint":"This demonstrates a regular pulse, not Word Clock changes or loss of lock. Check actual device lock status for sample-clock synchronisation.","hint_en":"This demonstrates a regular pulse, not Word Clock changes or loss of lock. Check actual device lock status for sample-clock synchronisation."}
```

## What to listen for

Check Sync/Lock indicators, sample rate and digital-input error reports before listening impressions. Record a sustained signal and inspect for lock loss, discontinuities or clicks. Descriptions such as gritty highs or loose bass do not identify a clock fault by themselves. Ordinary MIDI playback neither changes an interface's physical clock nor simulates these faults.

## Common misconceptions

- Word Clock synchronises samples, MIDI Clock conveys beat timing, and MTC conveys position.
- An expensive external clock does not guarantee better sound; correct topology, termination and lock settings come first.
- Follow the manual for inputs with sample-rate conversion rather than forcing one master/follower rule onto every design.
:::
