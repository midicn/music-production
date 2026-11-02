---
id: midi-latency-and-jitter
site: prod
cat: B1
title: MIDI 延迟与抖动
title_en: MIDI Latency and Jitter
summary: 延迟是消息到达晚，抖动是每次晚得不一样；两者都改变律动。
summary_en: Latency is a message arriving late; jitter is each arrival being late by a different amount.
level: standard
tags: [MIDI, 延迟, 抖动, 缓冲]
tags_en: [MIDI, latency, jitter, buffer]
alias: [MIDI 延迟, 抖动, jitter, 回环延迟]
links:
  - "[[glossary:latency]]"
  - "[[glossary:midi-protocol]]"
  - "[[glossary:latency-compensation]]"
  - "[[instrument:software-synth]]"
instances:
  - musicnet-000315 | 包含演奏速度变化，可区分谱面时间变化与链路延迟 | Tempo-changing performance data for distinguishing scored timing from link latency
  - groove-000693 | 鼓点偏离网格的律动参照，不是传输抖动测量 | Off-grid drum phrasing, not a transmission-jitter measurement
  - pdmx-000799 | 含速度变化的音符时序参照，不证明实时设备发生漂移 | Note and tempo timing reference, not evidence of real-time device drift
sources:
  - "https://help.ableton.com/hc/en-us/articles/360010545559-How-Latency-Works"
  - "https://midi.org/summary-of-midi-1-0-messages"
  - MIDI 1.0 串行速率与 USB MIDI 类帧长的公开定义——依据来自规范。
  - 本库文件的音符落点统计，由本地 SMF 解析脚本核对，数值随文件而定
updated: 2026-11-02
---

::: zh
软音源按下键盘有拖尾，录音后音符整体偏后，或前后不稳。多半不是音源慢，而是链路与缓冲。

## 问题

延迟与抖动常被混为一谈。前者让整段一起晚，后者让每个音晚得不同。前者可以补偿，后者只能减小。

## 协议或消息

传统五针 DIN MIDI 1.0 的串行速率为 31,250 bit/s，一个带起止位的字节约 320 μs，三字节消息约 0.96 ms；Running Status 可减少后续重复消息的字节数。USB、蓝牙和网络传输有不同的封包与调度方式，不能一概说成固定 1 ms 延迟。演奏到出声还包括音频缓冲、插件运算和转换器延迟。

## 参数与做法

分别测量 MIDI 事件到达时间与音频输出的往返延迟，重复多次，区分稳定偏移与分散程度。软件音源要降低的是实际监听链路延迟；接口的直接监听通常只绕过外部音频输入的 DAW 路径，不能让尚未渲染的软件乐器提前发声。不要用补偿后的时间线位置代替演奏者实际听到的延迟。

## 听什么

整体偏后像拖拍，抖动像鼓手不稳。低频与鼓点最敏感，几毫秒就能听出松。

## 常见误解

延迟不是音源的问题。降低缓冲不总是更好。MIDI 时间戳不等于音频采样位置。

```audiolab
{"type":"rhythm","sig":"4/4","bpm":100,"pattern":"q e e q e e","label":"节奏落点参照","label_en":"Rhythmic placement reference","hint":"预先排好的节奏不是 MIDI 链路延迟测试。测量时要记录发送、接收和音频输出的时间，并重复比较。","hint_en":"A pre-sequenced pattern is not a MIDI-link latency test. Measure send, receive and audio-output times repeatedly."}
```
:::

::: en
A software instrument feels sluggish, a recording lands behind the beat, or notes drift. The cause is often the chain and the buffer, not the sound engine.

## The problem

Latency and jitter are easily confused. The first moves a whole passage late, the second makes every note late by a different amount. One can be compensated, the other only reduced.

## Protocol or message

Traditional five-pin DIN MIDI 1.0 uses 31,250 bit/s: roughly 320 μs per framed byte and 0.96 ms for three bytes. Running Status can shorten subsequent repeated messages. USB, Bluetooth and network MIDI have different packet and scheduling behaviour, so they do not share a fixed one-millisecond delay. Playing-to-sound latency also includes audio buffering, plug-in processing and conversion.

## Settings and practice

Measure MIDI event arrival and audio round-trip latency separately, repeating the test to distinguish a stable offset from timing spread. For a software instrument, reduce the actual monitoring path. Interface direct monitoring generally bypasses the DAW for incoming external audio; it cannot make an unrendered virtual instrument sound sooner. A compensated timeline position is not the same as the performer's experienced delay.

## What to listen for

A constant offset sounds like dragging; jitter sounds like an unsteady drummer. Bass and kick reveal it first, where a few milliseconds already feel loose.

## Common misunderstandings

Latency is not the sound source's fault. A smaller buffer is not always better. A MIDI timestamp is not an audio sample position.

```audiolab
{"type":"rhythm","sig":"4/4","bpm":100,"pattern":"q e e q e e","label":"Rhythmic placement reference","label_en":"Rhythmic placement reference","hint":"A pre-sequenced pattern is not a MIDI-link latency test. Measure send, receive and audio-output times repeatedly.","hint_en":"A pre-sequenced pattern is not a MIDI-link latency test. Measure send, receive and audio-output times repeatedly."}
```
:::
