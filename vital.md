---
id: vital
site: prod
cat: C
order: 18
title: Vital（免费波表合成）
title_en: Vital (Free Wavetable Synth)
summary: 免费的波表合成器，调制与频谱变换给得很大方。
summary_en: A free wavetable synth that gives away deep modulation and spectral warping.
level: standard
tags: [插件, 合成器, 波表, 免费]
tags_en: [plugin, synthesizer, wavetable, free]
alias: [Vital, Vital Audio, 免费波表合成器, Matt Tytel]
tool_kind: plugin
tool_vendor: Matt Tytel
tool_form: 插件
tool_platforms: [macOS, Windows, Linux]
tool_price: 免费
tool_jobs: [编曲, 声音设计, 游戏音频]
tool_verified: 2026-10-30
links:
  - "[[instrument:wavetable-synthesis]]"
  - "[[instrument:software-synth]]"
  - "[[glossary:synthesizer]]"
instances:
  - oga-000009 | 游戏《海滩》场景配乐，铺底长、变化慢，适合检验波表漂移是否自然（C1，参照不是该插件的演示）。
  - oga-000003 | 游戏《背刺》配乐，紧张段落的低频与高频噪声层同时存在（C1，参照不是该插件的演示）。
  - groove-000000 | 138 BPM 放克鼓组，节奏密，合成贝斯只能占中低频的一条缝（C1，参照不是该插件的演示）。
  - groove-000010 | 80 BPM 放克循环，速度慢，长音与滑音的空间更大（C1，参照不是该插件的演示）。
sources:
  - Vital 官方产品页的振荡器、频谱变换与授权档位说明，依公开资料核对，未抄原文
  - 波表合成与调制矩阵的常见做法，依合成通识核对，未抄文本
updated: 2026-10-30
---

::: zh
## 它能完成什么

- 不花钱就做出可用的合成贝斯、主奏与铺底。
- 用频谱变换把一条波表改成另一种谐波分布，得到非常规音色。
- 给游戏与短片做会呼吸的持续层，用慢速调制撑住画面。
- 把同一波表复制到多层，做微失谐的宽声部，宽度不靠立体声效果。
- 用采样振荡器读一段素材，再把它当波表来扫。
- 把同一套调制用到多轨，保持音色家族的一致性。

## 它怎么工作

振荡器读波表，波表位置可以手绘、导入或由内置表变形得到。Vital 的特色在频谱变换：在波表上做频率轴的拉伸、谐波权重的重排与相位扰动，得到用普通滤波做不到的谐波结构。三个滤波器可以串联或并联，调制矩阵把 LFO、包络、随机源与 MIDI 连到几乎任何参数上，界面用动画显示调制深度。两个频段各自扫，能得到会分叉的音色。采样振荡器读入音频后按音高重放，但它不是完整的采样器。

## 边界与坑

- 频谱变换与多层失谐很吃 CPU，几轨铺底同时开就会顶到上限。
- 免费档不含官方预设包与部分云功能，预设生态要靠社区与自建。
- 免费档与付费档的预设不直接互换，工程交接要注明档位。
- 插件格式以官方下载页为准，Pro Tools 用户要先确认 AAX 是否提供。
- 采样振荡器只做单音重放，不能切片、不能做多重采样映射。
- 界面动画多，老机器上会拖累显示；音频线程与界面线程要分开看。

## 替代与搭配

Serum 的波表编辑与预设生态更成熟；Surge XT 同样免费且偏减法与混合合成；Pigments 的引擎更多。它适合与采样器分工：Vital 做合成层，采样器做真实乐器，混音时两边频段分开。

## 上手路径

先学波表位置与滤波的分工，再学频谱变换的三个轴向，最后学调制矩阵的深度控制。配合本站「波表合成」「软件合成器」「合成器」三篇读。

```audiolab
{"type":"instrument","gm":"Pad 2 (warm)","synth":"bowed","phrase":["C3","G3","D4","E4"],"label":"一层待变形的铺底","label_en":"A pad waiting to be warped","hint":"先听它的静态谐波，再想频谱拉伸后哪一段会变亮","hint_en":"Hear the static harmonics first, then imagine which region brightens when the spectrum is stretched"}
```
:::

::: en
## What it lets you finish

- Make usable synth bass, leads and pads without spending anything.
- Reshape a wavetable's harmonic distribution with spectral warping for unconventional tones.
- Build breathing sustain layers for games and short films, held by slow modulation.
- Stack copies of one wavetable into layers with slight detune, for width without stereo effects.
- Load a piece of audio into the sample oscillator and scan it as a wavetable.
- Apply one modulation scheme across several tracks so a family of sounds stays related.

## How it works

The oscillators read wavetables whose position can be drawn, imported, or produced by morphing the built-in tables. Vital's distinguishing feature is spectral warping: stretching the frequency axis, reweighting harmonics and disturbing phase produce harmonic structures that ordinary filtering cannot reach. Three filters can run in series or parallel, and a modulation matrix connects LFOs, envelopes, random sources and MIDI to nearly every parameter, with depth shown as animation. Two bands sweeping at once produce a tone that splits apart. The sample oscillator reads audio and plays it at pitch, but it is not a full sampler.

## Limits and traps

- Spectral warping and layered detune are CPU-hungry; a few pad tracks at once will reach the ceiling.
- The free tier excludes the official preset packs and some cloud features, so the preset ecosystem depends on the community and on your own patches.
- Presets do not transfer cleanly between the free and paid tiers, so a handover must state which tier the session used.
- Plugin formats follow the official download page, and Pro Tools users should confirm whether AAX is offered.
- The sample oscillator plays one note at a time and does not slice or map multisamples.
- The interface is animation-heavy and slows down on older machines; audio threads and display threads have to be judged separately.

## Alternatives and pairings

Serum has the more mature wavetable editor and preset ecosystem. Surge XT is also free and leans toward subtractive and hybrid synthesis. Pigments offers more engines. Vital works well beside a sampler: Vital supplies the synthetic layer, the sampler the real instruments, and the mix keeps their ranges apart.

## First three things to learn

Learn wavetable position against filtering, then the three axes of spectral warping, then modulation depth. Read the site's pages on wavetable synthesis, software synths and the synthesizer alongside it.

```audiolab
{"type":"instrument","gm":"Pad 2 (warm)","synth":"bowed","phrase":["C3","G3","D4","E4"],"label":"一层待变形的铺底","label_en":"A pad waiting to be warped","hint":"先听它的静态谐波，再想频谱拉伸后哪一段会变亮","hint_en":"Hear the static harmonics first, then imagine which region brightens when the spectrum is stretched"}
```
:::
