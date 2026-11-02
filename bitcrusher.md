---
id: bitcrusher
site: prod
cat: A7
title: 比特压碎
title_en: Bitcrushing
summary: 降位深与降采样率是两件事，一个给颗粒，一个给镜像。
summary_en: Lowering bit depth and sample rate are two different moves, one adds grain, the other aliases.
level: standard
tags: [效果器, 低保真, 量化, 混叠]
tags_en: [effects, lo-fi, quantization, aliasing]
alias: [比特压碎, 位深压缩, 降采样, 比特粉碎, bitcrusher, bit crush]
links:
  - "[[glossary:bit-depth]]"
  - "[[glossary:harmonics]]"
  - "[[instrument:software-synth]]"
instances:
  - oga-000013 | 复古游戏旋律的音符参照，未执行降位深处理 | Retro-game melody notes without bit-depth reduction
  - oga-000014 | 短促鼓点素材，没有降采样处理前后的版本 | Short drum events without before-and-after rate reduction
  - oga-000015 | 低音音符的素材参照，不包含可切换的量化台阶 | Bass-note material without switchable quantisation steps
sources:
  - Curtis Roads, The Computer Music Tutorial, quantization sections.
  - Udo Zölzer, DAFX.
updated: 2026-11-02
---

::: zh
## 为什么会用到它

Bitcrusher 常提供降低幅度精度、降低更新速率或采样保持等处理；不同插件可能只包含其中一部分。位深和速率改变的机制不同，应分开试听。

## 它怎么工作

降低位深会增大量化误差，低电平信号可能出现与信号相关的失真。降低有效更新率而不做足够带限，会让高频成分折返到较低频率，形成混叠；采样保持也会改变频谱。产生的假频率不只留在高频，具体位置由源频率和有效采样率决定。

## 旋钮与耳朵

先把混合量设为全处理，只降低位深，记下电平较小时的变化；恢复位深后再降低更新速率，区分两种效果。随后按需要混入干声并补偿输出电平。鼓、贝斯和长音的反应不同，参数值应跟素材走，不能把某个比特数或百分比当通用效果。

## 耳朵要抓的点

使用同一段已渲染音频逐项比较，保持其他处理不变。查看频谱能帮助区分原有谐波、新增失真与折返分量；“复古”属于审美选择，不由低位深或低采样率自动保证。

```audiolab
{"type":"instrument","gm":"Lead 1 (square)","synth":"reed","phrase":["C4","E4","G4","C5","G4","E4"],"label":"方波乐句参照","label_en":"Square-wave phrase reference","hint":"这里播放预设音色，没有位深或采样保持参数。需将同一音频送入 bitcrusher，分别改变位深和降采样设置。","hint_en":"This plays a preset without bit-depth or sample-hold controls. Send the same audio through a bitcrusher and change depth and rate reduction separately."}
```

## 容易弄错的

以为比特压碎等于全部 lo-fi；以为降位深与降采样率是一回事；以为加上去就会自动复古。
:::

::: en
## Why reach for it

A bitcrusher may reduce amplitude precision, reduce update rate or use sample-and-hold; plug-ins need not include every operation. Depth and rate changes have different mechanisms and should be auditioned separately.

## How it works

Reduced depth increases quantisation error and may create signal-correlated distortion at low levels. Reducing effective update rate without adequate band limiting folds higher components into lower frequencies, producing aliases; sample-and-hold also changes the spectrum. These components are not confined to high frequencies: their positions depend on source frequency and effective sample rate.

## Knobs and ears

Set the mix fully wet and reduce depth alone, noting low-level changes. Restore depth before reducing update rate to separate the effects. Then blend dry signal as needed and compensate output level. Drums, bass and sustained sounds respond differently, so no bit count or mix percentage is a universal setting.

## What the ear should catch

Compare one rendered audio passage one control at a time, keeping other processing fixed. A spectrum helps distinguish original harmonics, added distortion and aliases. A retro character is an aesthetic choice, not an automatic consequence of low depth or rate.

```audiolab
{"type":"instrument","gm":"Lead 1 (square)","synth":"reed","phrase":["C4","E4","G4","C5","G4","E4"],"label":"Square-wave phrase reference","label_en":"Square-wave phrase reference","hint":"This plays a preset without bit-depth or sample-hold controls. Send the same audio through a bitcrusher and change depth and rate reduction separately.","hint_en":"This plays a preset without bit-depth or sample-hold controls. Send the same audio through a bitcrusher and change depth and rate reduction separately."}
```

## Easy to get wrong

That bitcrushing accounts for all lo-fi; that lowering bit depth and lowering sample rate are the same; that adding it automatically sounds retro.
:::
