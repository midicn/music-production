---
id: fabfilter-pro-c
site: prod
cat: C
order: 12
title: Pro-C（压缩）
title_en: Pro-C (Compression)
summary: 把动态管住而不改音色，风格预设给的是动作方式。
summary_en: Dynamic control that leaves the tone alone, with styles that describe behaviour rather than genre.
level: standard
tags: [插件, 压缩, 动态, 混音]
tags_en: [plugin, compression, dynamics, mixing]
alias: [Pro-C, FabFilter Pro-C, 压缩插件, compressor plugin]
tool_kind: plugin
tool_vendor: FabFilter
tool_form: 插件
tool_platforms: [macOS, Windows]
tool_price: 买断
tool_jobs: [混音, 母带, 录音]
tool_verified: 2026-10-30
links:
  - "[[glossary:compressor]]"
  - "[[glossary:sidechain]]"
  - "[[glossary:parallel-compression]]"
instances:
  - groove-000007 | 65 BPM 的摇滚鼓循环，底鼓与军鼓瞬态间隔大，起音与释放的设定一听就分晓（C1）
  - pdmx-000007 | 莫扎特第四十交响曲，弦乐与木管的强弱起伏大，适合看整体动态被收住多少（C1）
  - musicnet-000020 | 巴赫第三无伴奏大提琴组曲前奏，单声部弓压变化连续，适合旁观压缩动作（C1）
sources:
  - FabFilter 官方产品页的风格、膝点、前视与侧链说明（公开资料）。
  - 压缩器起音、释放与增益补偿的常用取值，参考混音惯例。
updated: 2026-10-30
---

::: zh
## 适用工作

把一条人声压到句句可闻，又不必逐字画音量。给旁白或播客做温和的电平控制，句尾不忽然掉下去。让贝斯在整首歌里保持同一存在感，低音不忽然冒头。在总线上把几件乐器粘在一起，让它们听起来像在同一间屋子。用侧链让底鼓出现时低频让路，做电子与流行里的呼吸感。用并行压缩补密度，同时保住原轨的瞬态。

## 原理

压缩器读的是超过阈值的电平，按比率缩小，再用起音与释放决定动作快慢。Pro-C 的风格旋钮改的是这套动作的曲线：有的释放带程序依赖，有的拐点更软，对应人声、总线或母带常见的做法。膝点决定拐弯的圆滑程度，前视提前看信号，侧链输入可挂 EQ 做频率选择性触发。干湿比让并行压缩在一个插件里完成。自动增益只是把输出补回响度，不改变压缩本身。比率低于 2 比 1 时更像电平整形，高于 8 比 1 才开始接近限幅。

## 边界

- 它偏干净，想要 1176 或 LA-2A 那种染色，它给不了；风格名是动作描述，不是年代复刻。
- 前视越长延迟越大，录音监听时要把延迟补偿算进去。
- 它是单频段压缩，低频触发导致高频一起被压时，需要多段或侧链 EQ，不是加更多比率能解决。
- 串联两个单段压缩不会变成多段，频段之间仍然互相牵动。
- 侧链触发用立体声还是单声道要统一，否则左右会轮流让路。
- 自动增益容易让人误以为「更响就是更好」，A/B 时要把两版响度对齐再判断。
- 过采样与高内部精度会提高 CPU，几十轨都挂时先算清代价。
- 它是插件，工程交接要确认对方装了同一款，否则只能打印音频。

## 替代

要染色看 Waves CLA-2A 与 CLA-76；要极灵活的比率、前视与侧链滤波看 DMG Compassion；预算有限时 TDR Kotelnikov 可做母带级干净压缩。它常跟在 Pro-Q 后面：先修频段，再管动态，最后用限幅器收顶。

## 上手

先学阈值与比率的配合，再学起音释放对瞬态的影响，最后学增益补偿与并行。配合「压缩器参数」「侧链」「并行压缩」三篇读。

```audiolab
{"type":"instrument","drum":"36","phrase":["36","38","42","46","42","38","36"],"label":"一组鼓点，听瞬态","label_en":"A drum pattern to hear transients","hint":"先听军鼓的敲击，再想慢起音会削掉多少、快释放会不会抽气","hint_en":"Hear the snare hit first, then imagine what a slow attack removes and where a fast release pumps"}
```
:::

::: en
## Jobs it covers

Keep a vocal audible in every phrase without drawing volume. Level narration or a podcast without letting the end of each sentence fall away. Hold a bass at one presence level so it stops jumping out between sections. Glue instruments on a bus so they sound like one room. Duck low end under the kick with a sidechain, the breathing motion of pop and electronic music. Add density with parallel compression while transients survive.

## How it works

It reads level above a threshold, scales it by a ratio, and uses attack and release to set how fast it moves. The style control changes the shape of that motion: some styles tie release to the material and bend more softly, which is why some settings suit vocals or a master. Knee sets how rounded the corner is, lookahead reads ahead, and the sidechain input can take an EQ for frequency-selective triggering. A dry/wet control makes parallel compression possible inside one instance. Auto gain only restores output loudness, not the compression itself. A ratio below 2 to 1 shapes level; above 8 to 1 it approaches limiting.

## Limits

- For the colour of an 1176 or LA-2A, this is the wrong box; style names describe behaviour, not vintage emulation.
- Longer lookahead adds latency; count it in when tracking with direct monitoring.
- It is single-band. When a low note pulls the whole spectrum down, the fix is multiband work or a filtered sidechain, not more ratio.
- Two single-band compressors in series do not become multiband; the bands still pull on each other.
- Decide whether the sidechain trigger is stereo or mono, or left and right take turns ducking.
- Auto gain invites the mistake of hearing louder as better; match levels before choosing between two versions.
- Oversampling and high precision cost CPU, so dozens of instances need budget.
- It is a plugin; confirm the other studio has it before handing over, or print audio.

## Alternatives

Waves CLA-2A and CLA-76 supply colour. DMG Compassion offers flexible ratio, lookahead and sidechain filtering. TDR Kotelnikov is a clean mastering option. Pro-C usually follows Pro-Q: fix the bands, control the dynamics, then let a limiter catch the top.

## First three things

Learn threshold against ratio, attack and release against transients, then gain compensation and parallel use. Read the pages on compressor parameters, sidechain and parallel compression alongside it.

```audiolab
{"type":"instrument","drum":"36","phrase":["36","38","42","46","42","38","36"],"label":"一组鼓点，听瞬态","label_en":"A drum pattern to hear transients","hint":"先听军鼓的敲击，再想慢起音会削掉多少、快释放会不会抽气","hint_en":"Hear the snare hit first, then imagine what a slow attack removes and where a fast release pumps"}
```
:::
