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
  - atepp-000195 | 钢琴弱奏素材，可另制16位导出并测量结果（C1） | Quiet-piano material for a separate 16-bit export and measurement (C1)
  - giantmidi-003263 | 和弦尾音的参照，不包含加/不加抖动的两个版本（C1） | A chord-tail reference without dithered and undithered versions (C1)
  - musicnet-000265 | 室内乐声部参照，不能据此决定交付所需位深（C1） | Chamber-music parts that do not determine required delivery depth (C1)
sources:
  - "https://downloads.izotope.com/docs/rx6/39-dither/index.html"
  - Audio Engineering Society, AES3-2009，数字音频接口的字长与传输规定（标准）
  - Ken C. Pohlmann, Principles of Digital Audio，量化、抖动与噪声整形（教材）
  - BBC 交付技术规范，音频交付文件的位深与文件形态要求（机构规范）
updated: 2026-11-02
---

::: zh
## 位深不是音量档位

未处理的16位整数 PCM 转存24位时，不会恢复原录音细节；但后续增益或混音运算可以产生需要更高精度保存的结果。应区分原始素材位深、内部运算格式和最终交付格式。

## 接收方决定交什么

| 用途 | 先核对的要求 | 输出检查 |
|---|---|---|
| 音乐发行 | 发行方接受的PCM格式、位深与采样率 | 文件属性、真峰值、完整头尾 |
| CD母版 | 16位、44.1 kHz及制作方格式要求 | 最终量化与抖动、曲目衔接 |
| 影视/广播 | 项目指定的采样率、位深和响度规范 | 通道布局、时间起点、响度报告 |
| 工程交换/分轨 | 双方支持的整数或浮点格式 | 等长、同起点、命名与素材完整性 |

表里的位深不是音质排名。接收方要 16 位，就交 16 位；交 24 位让对方自己转，等于把降位与抖动的责任推给下游。

## 抖动只加在最后一次降位

抖动用于控制重新量化的失真，通常放在最终定点量化处；不能把24位一概列为“禁止抖动”。24位的量化误差往往低于素材本底，是否使用以及噪声整形强度应按处理器说明与交付要求决定。若之后还要改增益或限幅，应保留高精度母版，完成修改后重新生成最终交付，而不是认为旧抖动能保护后续任意处理。

## 导出前的五项核对

- 按书面要求确定格式，不用文件体积判断音质
- 保存高精度母版，记录最终量化和抖动设置
- 导出后核对文件属性、头尾、声道和峰值
- 不重复添加不必要的抖动
- 文件名和清单注明采样率、位深与版本

## 会坏在哪

容易出错的是把升位深当作修复信息、只留最终有损文件、忘记记录抖动设置，或在交付文件上继续修改却不重新检查。加过抖动不等于噪声必然随音乐起伏；噪声调制、量化误差与编码伪影需要分别检查。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["E4","G4","B4","E5"],"label":"交付前的弱奏参照","label_en":"Quiet-passage delivery reference","hint":"弱奏可帮助选择测试片段，交付位深仍应按规范确定。这里没有16/24位开关，也没有抖动对照。","hint_en":"Quiet passages can help choose test material; delivery depth follows the specification. There is no 16/24-bit switch or dither comparison here."}
```
:::

::: en
## Bit depth is not a volume setting

Converting unprocessed 16-bit integer PCM to 24 bits does not restore recording detail. Later gain or mixing can nevertheless produce results worth saving at higher precision. Distinguish source depth, internal processing format and final delivery format.

## The receiver decides

| Use | Confirm first | Check output |
|---|---|---|
| Music distribution | Accepted PCM format, depth and rate | Properties, true peak and complete boundaries |
| CD master | 16-bit/44.1 kHz and authoring requirements | Final quantisation, dither and transitions |
| Film/broadcast | Project rate, depth and loudness specification | Channels, time origin and loudness report |
| Session/stem exchange | Mutually supported integer or float format | Length, start, naming and complete media |

The table is not a ranking of sound quality. If the receiver asks for 16 bits, send 16 bits; sending 24 and letting them convert pushes the reduction and the dither downstream.

## Dither once, on the last reduction

Dither controls requantisation distortion, normally at final fixed-point quantisation; it is not universally forbidden at 24 bits. Error at 24 bits often lies below source noise, so follow processor documentation and delivery requirements for dither and shaping. Keep a high-precision master if gain or limiting will change, then regenerate final delivery rather than treating earlier dither as protection for arbitrary later processing.

## Five checks before export

- Follow written format requirements rather than file size as a quality ranking
- Keep a high-precision master and log final quantisation and dither
- Check file properties, boundaries, channels and peaks after export
- Avoid unnecessary repeated dither
- Label rate, depth and version in filenames and inventories

## Where it breaks

Common errors include treating increased depth as restored information, keeping only a final lossy file, losing dither settings, or editing delivery files without rechecking. Dither does not inherently make noise pump with the music; noise modulation, quantisation error and codec artifacts are separate issues.
:::
