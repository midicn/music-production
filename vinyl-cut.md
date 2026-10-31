---
id: vinyl-cut
site: prod
cat: A8
order: 463
title: 黑胶刻片
title_en: Vinyl Cutting
summary: 黑胶刻片受侧长、低频与高频三条物理限制，母带要另做一版。
summary_en: A vinyl cut is limited by side length, low-end motion and high-frequency heat, so it needs its own master.
level: standard
tags: [母带, 黑胶, 刻片, 低频, 动态]
tags_en: [mastering, vinyl, cutting, low end, dynamics]
alias: [黑胶刻片, 黑胶母带, 刻片, vinyl cut, lacquer cut]
links:
  - "[[glossary:headroom]]"
  - "[[glossary:lufs]]"
  - "[[glossary:limiter]]"
  - "[[glossary:phase]]"
instances:
  - pdmx-001129 | 贝多芬第五的定音鼓与低弦冲击密集，适合检查低频是否该收成单声道
  - groove-000008 | 灵魂乐鼓循环的低频稳定，适合对照刻片前后底鼓与贝斯的重心
  - aria-002937 | 霍尔斯特《行星》的铜管与打击动态大，适合观察高潮段是否需要让刻片头留余量
sources:
  - Katz, Bob，Mastering Audio（Focal Press）— 黑胶预母带、刻片电平与低频处理章节。
  - AES（Audio Engineering Society）关于黑胶刻片与纹槽几何的公开论文 — 刻片头运动与高频过热的依据。
  - RIAA 均衡曲线（Recording Industry Association of America）— 刻片与回放的低频补偿口径。
updated: 2026-10-31
---

::: zh
黑胶不是把 24 位 WAV 换个容器。刻片头要在有限的时间里推动纹槽：低频振幅太大就会跳针，高频能量太高会烧刻片头，单面太长则纹槽变窄、电平下降。

## 三条物理限制

第一是侧长。12 英寸 33 转的单面通常控制在 18 到 22 分钟，越长，纹槽越密，可用的电平与高频越少。第二是低频。左右声道反相的低频会让刻片头垂直行程过大，通常把 100 Hz 以下收成单声道，或至少检查相位。第三是高频。密集的齿音、失真吉他与强压缩的镲片会让刻片头过热，刻出的纹槽回放时发糙。

## 为黑胶另做一版母带

| 问题 | 刻片上的后果 | 母带上的做法 |
| --- | --- | --- |
| 单面超过 22 分钟 | 纹槽变窄、电平下降 | 拆面或调整曲序 |
| 低频反相 | 刻片头行程过大、跳针 | 100 Hz 以下转单声道 |
| 高频过密 | 刻片头过热、回放失真 | 轻降 8 到 12 kHz，减少削波 |
| 整体过响 | 刻片头没有余量 | 留 3 到 6 dB 峰值余量 |
| 尾音太长 | 纹槽间距不够 | 收短尾音或换曲序 |

## 刻片前的检查

先问厂方要刻片规格：转速、单面时长、是否半速刻片、是否需要 DMM。若一张专辑超过两面容量，先决定拆成双张还是删曲，再开始刻片；曲序定了再改，试刻也要重做。再单独做一版黑胶母带：不追求流媒体响度，保留更多动态；低频收单声道；高频做轻微柔化；每面最后一首的尾音留够空间。试刻必须听，尤其听每面最后一首的内圈。刻片厂通常还要一份曲序表，写清每面时长与首尾淡出，和母带一起交能减少来回。

```audiolab
{"type":"instrument","gm":"Timpani","synth":"perc","phrase":["C2","G2","C2","G1"],"label":"低频的行程","label_en":"Low-end travel","hint":"注意低频脉冲的幅度，刻片头要为此留出余量","hint_en":"Hear the size of the low pulses; the cutter head needs room for them"}
```

## 不该做的事

不要把流媒体母带直接送刻片，也不要在刻片后再做有损编码。黑胶的动态与底噪和数字母带不同，A/B 时先对齐响度。内圈失真、跳针与高频过热往往不是靠均衡能补救的，严重时只能重刻或换曲序。黑胶适合完整专辑与有仪式感的发行，不适合把响亮当成唯一目标的单曲。
:::

::: en
Vinyl is not a 24-bit WAV in another container. The cutter has to move a groove in limited time: too much low-frequency amplitude and the stylus jumps, too much high-frequency energy and the cutter head overheats, too long a side and the grooves narrow and the level drops.

## Three physical limits

Side length first. A 12-inch side at 33 rpm usually stays between 18 and 22 minutes; longer means tighter grooves and less available level and high end. Low end second. Out-of-phase bass makes the cutter head travel too far vertically, so everything below 100 Hz is usually summed to mono, or at least checked for phase. High end third. Dense sibilance, distorted guitars and heavily compressed cymbals heat the head, and the groove plays back rough.

## Cut a separate master

| Problem | What happens at the lathe | What to do in the master |
| --- | --- | --- |
| A side over 22 minutes | Narrower grooves, lower level | Split the side or change the order |
| Out-of-phase bass | Excessive head travel, jumps | Sum below 100 Hz to mono |
| Dense high end | Overheated head, distorted playback | Ease 8 to 12 kHz, reduce clipping |
| Overall too loud | No headroom for the cutter | Leave 3 to 6 dB peak margin |
| Very long tails | Not enough groove spacing | Shorten tails or resequence |

## Checks before cutting

Ask the plant for its specs: speed, side length, half-speed or DMM. If an album exceeds two sides, decide between a double LP and cutting a track before work starts; changing the order later means a new test cut. Then make a separate vinyl master: less loud than the streaming version, more dynamics kept, bass summed, highs gently softened, and enough room at the end of each side. A test cut must be heard, especially the inner groove of the last track on each side. The plant usually wants a running-order sheet with side timings and fade points, and sending it with the master saves a round of questions.

```audiolab
{"type": "instrument", "gm": "Timpani", "synth": "perc", "phrase": ["C2", "G2", "C2", "G1"], "label": "Low-end travel", "label_en": "Low-end travel", "hint": "注意低频脉冲的幅度，刻片头要为此留出余量", "hint_en": "Hear the size of the low pulses; the cutter head needs room for them"}
```

## What not to do

Do not send the streaming master straight to the cutter, and do not encode lossily after cutting. Vinyl has a different noise floor and dynamic feel, so match loudness before A/B. Inner-groove distortion, jumps and high-frequency heat rarely respond to EQ; severe cases mean recutting or changing the running order. Vinyl suits a complete album and a release with ceremony, not a single whose only goal is loudness.
:::
