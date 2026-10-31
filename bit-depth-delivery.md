---
id: bit-depth-delivery
site: prod
cat: B5
order: 380
title: 交付位深
title_en: Delivery Bit Depth
summary: 位深由接收方决定，抖动只在最后一次降位时加。
summary_en: Delivery depth follows the receiver, and dither belongs only on the final reduction.
level: standard
tags: [位深, 交付, 抖动, 母带]
tags_en: [bit depth, delivery, dither, mastering]
alias: [交付位深, 导出位深, 24 位交付, bit depth delivery]
links:
  - "[[glossary:bit-depth]]"
  - "[[glossary:dither]]"
  - "[[glossary:noise-floor]]"
  - "[[glossary:true-peak]]"
instances:
  - atepp-000195 | 德彪西《月光》的弱奏与长衰减，降成 16 位时噪声底最先露出来（C1）
  - giantmidi-003263 | 萨蒂《玄秘曲》的极弱和弦余韵，适合对照加与不加抖动（C1）
  - musicnet-000265 | 弗雷钢琴四重奏的安静段落，用来判断 24 位是否真的必要（C1）
sources:
  - Audio Engineering Society, AES3-2009，数字音频接口的字长与传输规定（标准）
  - Ken C. Pohlmann, Principles of Digital Audio，量化、抖动与噪声整形（教材）
  - BBC 交付技术规范，音频交付文件的位深与文件形态要求（机构规范）
updated: 2026-10-31
---

::: zh
## 位深不是音量档位

把 16 位文件另存成 24 位，不会多出任何细节，只会多出八个零。位深在录音时划定可用动态范围，在交付时决定最轻的段落能不能活下来；素材一旦已经是 16 位，再升位深只是换了一个更大的容器。

## 接收方决定交什么

| 交付对象 | 位深 | 抖动 | 说明 |
|---|---|---|---|
| 数字发行 WAV | 24 位 | 不加 | 平台自行转码，留 1 dB 真峰值余量 |
| CD 或 16 位母版 | 16 位 | 最后一次加 | TPDF 或噪声整形，按发行方要求 |
| 影视与广播后期 | 24 位 | 不加 | 通常与 48 kHz 一起交，保留余量 |
| 工程交换 | 32 位浮点 | 不加 | 只在双方约定时使用，不用于发行 |
| 分轨 stems | 24 位 | 不加 | 等长、同起点、同采样率 |

表里的位深不是音质排名。接收方要 16 位，就交 16 位；交 24 位让对方自己转，等于把降位与抖动的责任推给下游。

## 抖动只加在最后一次降位

抖动把量化误差打散成低电平噪声，代价是噪声底略微抬高。它属于最后一次降位：从 32 位浮点直接导出 16 位时加一次；中间过程、24 位文件、还要继续做母带的版本都不加。加过抖动的文件不要再做增益、重采样或限制，否则噪声被重新整形，前面那一步白做。噪声整形把噪声推向高频，对 CD 有利，对流媒体转码不一定；拿不准时用平直的 TPDF。

## 导出前的五项核对

- 位深与接收方的书面要求一致，不凭印象选
- 16 位版本由 32 位浮点或 24 位一次性降位，只加一次抖动
- 降位后重测真峰值，抖动可能让峰值略微上升
- 24 位文件不做无意义的升位，也不叠加抖动
- 文件名与随附清单写明位深与采样率

## 会坏在哪

用 24 位容器装 16 位素材，听感不会变，却让人误以为还有余量。对已经限幅的素材再抖动，噪声会跟着音乐起伏，安静段反而更脏。把 16 位文件升到 32 位浮点再处理，不会恢复被抹掉的细节，只会把量化噪声一起放大。最隐蔽的一种：导出 24 位给母带，母带又降 16 位并加抖动，而前一版已经加过，噪声被叠了两层。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["E4","G4","B4","E5"],"label":"弱奏后的余韵","label_en":"The tail after a soft chord","hint":"先听尾音的长度，再想 16 位导出时哪一段会先被噪声盖住","hint_en":"Hear how long the tail lasts, then decide which part a 16-bit export would bury in noise"}
```
:::

::: en
## Bit depth is not a volume setting

Save a 16-bit file as 24-bit and nothing new appears except eight zeroes. Bit depth sets headroom while recording and decides, at delivery, whether the quietest passage survives. Once the source is already 16-bit, a larger word length is just a larger container.

## The receiver decides

| Destination | Depth | Dither | Note |
|---|---|---|---|
| Digital release WAV | 24-bit | No | The platform transcodes; leave 1 dB of true-peak margin |
| CD or 16-bit master | 16-bit | Once, at the end | TPDF or noise shaping, as the label asks |
| Film and broadcast post | 24-bit | No | Usually paired with 48 kHz and headroom |
| Session exchange | 32-bit float | No | Only by agreement, never for release |
| Stems | 24-bit | No | Equal length, common start, common rate |

The table is not a ranking of sound quality. If the receiver asks for 16 bits, send 16 bits; sending 24 and letting them convert pushes the reduction and the dither downstream.

## Dither once, on the last reduction

Dither scatters quantization error into low-level noise, at the cost of a slightly raised floor. It belongs to the final reduction: add it once when exporting 16-bit from 32-bit float. Do not add it to intermediate stages, to 24-bit files, or to a version that still faces mastering. A dithered file should not be gained, resampled or limited afterwards, or the noise is reshaped and the earlier decision is wasted. Noise shaping pushes noise toward high frequencies, which suits CD but not necessarily streaming transcodes; when in doubt, use flat TPDF.

## Five checks before export

- The depth matches the receiver's written spec, not a guess
- The 16-bit version comes from 32-bit float or 24-bit in one pass, with one dither
- True peak is measured again after reduction, since dither can raise it slightly
- 24-bit files are not pointlessly upconverted or dithered
- The filename and delivery note state both depth and sample rate

## Where it breaks

A 24-bit container holding 16-bit audio changes nothing audible but suggests headroom that is not there. Dithering material that is already limited makes the noise pump with the music and dirties the quiet bars. Upconverting 16-bit to 32-bit float restores none of the lost detail and amplifies the quantization noise along with everything else. The quietest failure: a 24-bit file goes to mastering, mastering reduces to 16-bit and dithers, and the earlier version was already dithered, so the noise is stacked twice.
:::
