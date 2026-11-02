---
id: sample-rate-conversion
site: prod
cat: B5
title: 采样率转换
title_en: Sample-Rate Conversion
summary: 44.1 与 48 kHz 互转不是改个数字，滤波器决定转完还剩多少细节。
summary_en: Converting between 44.1 and 48 kHz is not a renumbering exercise; the filter decides how much detail survives.
level: standard
tags: [采样率, 重采样, 滤波, 混叠]
tags_en: [sample rate, resampling, filtering, aliasing]
alias: [重采样, 采样率转换, SRC, sample rate conversion, resampling]
links:
  - "[[glossary:sample-rate]]"
  - "[[glossary:bit-depth]]"
  - "[[glossary:latency]]"
instances:
  - groove-000000 | 鼓组音符素材，可另渲染为受控重采样实验的源音频（C1） | Drum notes that can be separately rendered as source audio for a controlled resampling test (C1)
  - atepp-001115 | 钢琴音符与衰减素材，不包含转换前后的音频版本（C1） | Piano notes and decays without before-and-after resampling files (C1)
  - cyberhymnal-008729 | 持续和声的 MIDI 参照，不能验证转换器的振铃（C1） | Sustained-harmony MIDI reference that does not test converter ringing (C1)
sources:
  - "https://docs.scipy.org/doc/scipy/reference/generated/scipy.signal.resample_poly.html"
  - 采样定理与重建滤波的表述，参考数字音频惯例教材。
  - 常见采样率之间的整数与非整数比关系；公开技术资料是主要依据。
updated: 2026-11-02
---

::: zh
## 阻碍在哪

素材来自 44.1 kHz 的唱片、48 kHz 的视频工程、96 kHz 的现场录音，最后要汇到一个工程里。直接把采样率标签改掉会改变播放速度与音高，必须重采样。转得好不好，听的是高频还剩多少、瞬态有没有糊。

## 为什么会这样

数字重采样可看作插值、低通滤波与重新取样，不必先真实转换成连续模拟波形。以 44.1 转 48 kHz 为例，比例可约成 160/147，实际实现常用多相滤波避免计算后来会丢掉的样点。滤波器的通带、阻带衰减、相位响应和计算预算共同影响结果；不能只凭转换比例是否为整数判断音质。降采样需要限制新奈奎斯特频率以上的能量，避免混叠。

## 怎么绕过去

同一工程统一采样率，减少反复转换。给视频做配乐直接录 48 kHz，省掉最后一次转换。母带保持在录制时的采样率，交付前一次性转换。离线导出时选高质量设置，实时监听用低延迟设置即可。位深与采样率是两件事，转采样率不会自动加抖动。超过 96 kHz 的采样率对回放收益有限，麦克风与房间往往先成为瓶颈。

## 听这几处

从同一条高采样率录音导出两个目标采样率相同、转换质量设置不同的版本，关闭其他处理并匹配电平。用盲听与频谱检查寻找差别；没有听出差别也是有效结果。这里的 MIDI 与合成器演示不是重采样处理前后对照，不能拿它证明某个转换器改变了泛音、低频或瞬态。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C6","E6","G6","C7","G6","E6","C6","G5"],"label":"高音区旋律","label_en":"High-register phrase","hint":"这段只提供高音区的音符素材，不切换重采样算法。要验证转换，须从同一音频制作已知设置的渲染版本。","hint_en":"This supplies high-register notes, not switchable resampling algorithms. Test conversion using known-setting renders of the same audio."}
```
:::

::: en
## Where it blocks

Material arrives at 44.1 kHz from records, 48 kHz from video projects and 96 kHz from location recordings, and all of it has to meet in one session. Simply relabelling the rate changes speed and pitch, so the audio must be resampled. Whether it goes well is audible in how much high end survives and whether transients smear.

## Why it happens

Digital resampling can be understood as interpolation, low-pass filtering and sampling on a new grid; it need not construct an analogue waveform. For 44.1 to 48 kHz, the ratio reduces to 160/147. Polyphase implementations avoid calculating samples that would later be discarded. Passband, stopband attenuation, phase response and computation budget all matter; an integer ratio alone does not establish better sound. Downsampling must limit energy above the new Nyquist frequency to prevent aliasing.

## How to get around it

Keep one sample rate per project and convert as few times as possible. For picture work, record at 48 kHz and skip the last conversion. Keep the master at its recording rate and convert once at delivery. Use high-quality settings for offline export and low-latency settings only for live monitoring. Bit depth and sample rate are separate issues, and resampling does not add dither by itself. Rates above 96 kHz buy little on playback, because microphones and rooms usually limit first.

## Listen to these

Export one high-rate recording twice to the same target rate using different converter quality settings, with other processing off and levels matched. Use blinded listening and spectrum inspection; finding no audible difference is a valid result. The MIDI and synthesizer examples here are not before/after resampling renders and cannot demonstrate a converter's effect on harmonics, bass or transients.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C6","E6","G6","C7","G6","E6","C6","G5"],"label":"High-register phrase","label_en":"High-register phrase","hint":"This supplies high-register notes, not switchable resampling algorithms. Test conversion using known-setting renders of the same audio.","hint_en":"This supplies high-register notes, not switchable resampling algorithms. Test conversion using known-setting renders of the same audio."}
```
:::
