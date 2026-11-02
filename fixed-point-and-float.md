---
id: fixed-point-and-float
site: prod
cat: B5
title: 定点与浮点
title_en: Fixed Point and Floating Point
summary: 区分整数文件、浮点运算和硬件边界，判断超出满刻度后能否恢复。
summary_en: Distinguish integer files, float processing and hardware boundaries when judging recovery above full scale.
level: standard
tags: [浮点, 定点, 余量, 削波]
tags_en: [floating point, fixed point, headroom, clipping]
alias: [定点, 浮点, 32 位浮点, fixed point, floating point]
links:
  - "[[glossary:headroom]]"
  - "[[glossary:clipping]]"
  - "[[glossary:bit-depth]]"
instances:
  - pdmx-000435 | 多声部可作求和素材；同一渲染在浮点处理中升降增益，再比较定点导出的削波 | Use multiple parts for summing; boost and attenuate one float render before comparing an overloaded integer export
  - oga-000001 | 可渲染编曲检查总线峰值，内部能否恢复过载取决于实际处理链 | Render the arrangement to inspect bus peaks; overload recovery depends on the actual processing chain
  - musicnet-000067 | 四声部可作等增益叠加练习，峰值与可恢复性需测量实际渲染 | Four parts support equal-gain summing practice; measure peaks and recovery on the actual render
sources:
  - 浮点与定点音频通路的差异.
updated: 2026-11-02
---

::: zh
## 问题

定点PCM与浮点是数值表示方式。源文件格式、DAW内部运算和最终输出可采用不同表示，不能只从文件扩展名推断整条混音链的余量。

## 原理

定点文件有有限的编码范围；写入超出范围的结果需要处理，否则会削波。浮点使用有效数字与指数，通常可以在内部表示超过0 dBFS的幅度，但插件可能主动限幅、饱和或采用不同内部精度。浮点数仍有有限精度，不能逆转前面已产生的失真。

## 参数与做法

了解DAW与插件的运算路径，保持合理增益，输出到转换器或定点文件前回到要求的范围。无需为了定点交付自动加上限制器：若只需降低整体电平，可先降低增益。保存高精度中间文件便于继续处理，最终导出后重新检查峰值和文件属性。

## 听什么

可在不含非线性插件的浮点测试链中先升高增益，再用等量衰减恢复，比较恢复前后的文件。另做一版在超量时先导出定点再拉低，检查削波残留。两种路径的差别在何时量化或限幅，不是16位文件在任何情况下都会削波。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C3","G3","C4","E4","G4"],"label":"定点与浮点测试素材","label_en":"Material for fixed/float tests","hint":"渲染后在浮点通路先加增益再等量减回；另导出过载的整数文件再减，比较波形与误差。","hint_en":"Render, boost and equally attenuate within a float path. Separately export an overloaded integer file before attenuating; compare waveforms and error."}
```

## 常见误解

浮点运算的可表示范围不等于每个插件、模拟输入和输出设备都有同样余量。32位浮点中间文件可保存后续处理产生的高精度结果，却不能修复之前已经削波或噪声掩盖的素材。原始录音、内部运算和交付格式要分别判断。
:::

::: en
## The question

Fixed-point PCM and floating point are numerical representations. Source files, DAW arithmetic and final output can differ, so a file extension does not establish the headroom of the entire chain.

## How it works

A fixed-point file has a finite coding range; writing values beyond it requires handling or they clip. Floating point uses a significand and exponent and commonly represents internal levels above 0 dBFS. Plug-ins may nevertheless limit, saturate or use different internal precision. Floating point remains finite and cannot undo distortion already created.

## Settings and practice

Know the DAW and plug-in path, maintain suitable gain and bring output within requirements before a converter or fixed-point file. A limiter is not automatically required: simple gain reduction may suffice. Keep high-precision intermediates for later work and check peaks and file properties after final export.

## What to listen for

In a floating-point test chain without nonlinear plug-ins, add gain then apply equal attenuation and compare. Separately export fixed point while over range, then lower that file and inspect residual clipping. The distinction is where quantisation or limiting occurs, not that every 16-bit export must clip.

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C3","G3","C4","E4","G4"],"label":"Material for fixed/float tests","label_en":"Material for fixed/float tests","hint":"Render, boost and equally attenuate within a float path. Separately export an overloaded integer file before attenuating; compare waveforms and error.","hint_en":"Render, boost and equally attenuate within a float path. Separately export an overloaded integer file before attenuating; compare waveforms and error."}
```

## Common misconceptions

The representable float range is not shared by every plug-in, analogue input and output device. A 32-bit float intermediate file can preserve high-precision processing results but cannot repair earlier clipping or information buried in source noise. Evaluate recording, internal processing and delivery formats separately.
:::
