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
  - mutopia-000180 | 连续长音里，时钟不稳时高频先发毛
  - groove-000775 | 鼓组瞬态密集，失锁的咔嗒容易被当成鼓边
  - m21-000030 | 四声部合唱同时进入，错位会让和声整体发浑
sources:
  - Watkinson, The Art of Digital Audio, clocking and interfacing chapters
  - AES Convention paper on word clock distribution and jitter
updated: 2026-10-28
---

::: zh
## 问题

多台数字设备各自计时，采样点就会错位。轻则高频发毛，重则每隔几秒一声咔嗒。规则只有一条：选一个主时钟，其余设备跟随。

## 信号链

主时钟可以是转换器、声卡或独立时钟，经字时钟、ADAT 或嵌入的数字流分发。每台从设备锁定之后，采样点才落在同一张时间网格上。

## 摆位与参数

选一台最稳定的设备做主时钟，其余设为外部同步。全场采样率必须一致，48 kHz 工程里不要留 44.1 kHz 设备。时钟线尽量短，避免过长的菊花链；等锁定指示灯稳定再开录。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"q q q q","bpm":120,"label":"全场共用的那一个时钟","label_en":"The one clock everyone shares","hint":"先听它有多稳，再想两台设备各走各的会怎样","hint_en":"Hear its steadiness, then imagine two devices each keeping their own time"}
```

## 听什么

播放持续和弦或管风琴长音，听高频是否毛糙、有没有周期性的轻响。调换主从再听同一段，锁定不稳时低频也会显得散。

## 常见误解

- **各自用自己的时钟更准** → 各自都准，合起来不准。
- **时钟只影响数字接口** → 它决定每一次采样的时刻。
- **听到咔嗒才要查** → 高频发毛已经是早期症状。
:::

::: en
## The problem

When several digital devices keep their own time, their samples land in different places. The first symptom is a slightly gritty top end; the next is a click every few seconds. One master clock, everything else following.

## Signal chain

The master can be a converter, an interface or a dedicated clock, distributed over word clock, ADAT or an embedded digital stream. Once each slave locks, its samples fall on the same time grid.

## Placement and settings

Choose the most stable device as master and set the rest to external sync. Every device must run the same rate; do not leave a 44.1 kHz unit in a 48 kHz session. Keep clock cables short, avoid long daisy chains, and wait for lock before recording.

```audiolab
{"type": "rhythm", "sig": "4/4", "pattern": "q q q q", "bpm": 120, "label": "The one clock everyone shares", "label_en": "The one clock everyone shares", "hint": "先听它有多稳，再想两台设备各走各的会怎样", "hint_en": "Hear its steadiness, then imagine two devices each keeping their own time"}
```

## What to listen for

Play a sustained chord or an organ note and listen for a rough top end or periodic soft ticks. Swap the master and slave roles and hear it again; when lock is unstable, the low end also sounds loose.

## Common misconceptions

- **Each device is more accurate on its own clock** → each may be accurate, the sum is not.
- **Clock only affects digital connections** → it sets every sampling instant.
- **Nothing is wrong until you hear a click** → a gritty top end is already a symptom.
:::
