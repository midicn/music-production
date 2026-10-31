---
id: sample-rate-delivery
site: prod
cat: B5
order: 382
title: 交付采样率
title_en: Delivery Sample Rate
summary: 采样率跟接收方走，转换只做一次，不要放在限制器之后。
summary_en: Delivery rate follows the receiver; convert once, and never after the limiter.
level: standard
tags: [采样率, 交付, 重采样, 真峰值]
tags_en: [sample rate, delivery, resampling, true peak]
alias: [交付采样率, 导出采样率, delivery sample rate]
links:
  - "[[glossary:sample-rate]]"
  - "[[glossary:true-peak]]"
  - "[[glossary:bit-depth]]"
  - "[[glossary:latency]]"
instances:
  - groove-001062 | 拉丁打击乐的镲与沙锤集中在高频，44.1 与 48 的差别先在这里显形（C1）
  - atepp-001115 | 肖邦第一叙事曲的钢琴泛音密集，转换后尾音的光泽会变（C1）
  - cyberhymnal-008729 | 管风琴赞美诗的低频与长混响，检验重采样有没有引入振铃（C1）
sources:
  - Audio Engineering Society, AES5-2018，专业音频应用的首选采样频率（标准）
  - ITU-R BS.1770-4，节目响度与真峰值测量（标准）
  - Avid Pro Tools Reference Guide，会话采样率与采样率转换的行为说明（产品文档）
updated: 2026-10-31
---

::: zh
## 48 kHz 是兼容选择，不是音质等级

把一段 44.1 kHz 的成品转成 48 kHz，不会变得更清楚；它只是换了一个时基，方便视频工程接收。反过来，48 kHz 的素材要进 CD，也得回到 44.1。交付环节的采样率先看兼容，音质排在后面。

## 接收方与采样率对照

| 接收方 | 采样率 | 备注 |
|---|---|---|
| 数字发行与流媒体 | 44.1 或 48 | 两者都收，按母带原样交，不必为平台改 |
| 视频、广告、广播 | 48 | 与画面同一时基，省一次转换 |
| CD 母版 | 44.1 | 配 16 位与抖动 |
| 影视后期 | 48 或 96 | 以对方工程为准，先问再转 |
| 游戏中间件 | 48 | 转换后复查循环点与响度 |
| 高解析发行 | 96 或 192 | 只在全程高采样率制作时有意义 |

同一批交付里不要混用两种采样率。剪辑软件按文件自身速率解释，混着放会出现整体偏移，画面对不上。

## 转换只做一次，放在限制之前

重采样是滤波，会改变瞬态与高频相位；转两次就是滤两次，损失叠加。顺序也要注意：先转换采样率，再进限制器，最后测真峰值。反过来，在限制器之后转换，滤波过冲可能把原本 -1 dBTP 的文件推过 0。若只能转换成品，至少留 1 dB 余量，并在转换后重测。

44.1 与 48 的比值不是整数，转换器要做非整数比重采样，质量差异比整数比更明显。选带抗混叠滤波的离线转换，不要拿实时预览的设置导正式文件。

## 96 kHz 留在制作端

96 kHz 的用处是给变调、时间伸缩与非线性插件留余量，不是交付格式。文件体积翻倍，插件负担上升，接收方往往还要转回 48。只有全程 96 kHz 制作、且发行方明确要求时才交 96；否则在 96 制作、48 交付，高采样率工程留作存档。

## 常见的坏法

- 只改文件头或扩展名，播放速度与音高跟着变
- 交付文件标着 48 kHz，内容其实是 44.1，导入后整轨偏移
- 限制器之后重采样，真峰值超标却没人复测
- 同一批文件混着 44.1 与 48，剪辑时对不齐
- 为“更清楚”把 44.1 升到 96，体积变大，细节没变

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C6","E6","G6","C7"],"label":"高音区的泛音","label_en":"Overtones high on the keyboard","hint":"先听高音的空气感，再想降采样时哪一层最先消失","hint_en":"Hear the air around the top notes, then decide which layer a lower rate removes first"}
```
:::

::: en
## 48 kHz is a compatibility choice, not a quality grade

Converting a finished 44.1 kHz track to 48 kHz does not make it clearer; it changes the time base so a video project can accept it. Go the other way, and 48 kHz material headed for CD must return to 44.1. At delivery, sample rate is first a question of compatibility and only second a question of sound.

## Match the rate to the receiver

| Receiver | Rate | Note |
|---|---|---|
| Digital release and streaming | 44.1 or 48 | Both accepted; send the master as cut |
| Video, advertising, broadcast | 48 | Shares the picture time base and saves a conversion |
| CD master | 44.1 | With 16-bit depth and dither |
| Film post | 48 or 96 | Follow their session; ask before converting |
| Game middleware | 48 | Recheck loop points and loudness after conversion |
| High-resolution release | 96 or 192 | Meaningful only if made at that rate throughout |

Do not mix rates inside one delivery batch. Editing software reads each file at its own rate, and a mixed batch drifts out of sync with picture.

## Convert once, before the limiter

Resampling is filtering, and it alters transients and high-frequency phase; two conversions filter twice and stack the loss. Order matters as well: convert the rate, then limit, then measure true peak. Convert after limiting and filter overshoot can push a file that sat at -1 dBTP past 0. If a finished file must be converted, leave at least 1 dB of margin and measure again afterwards.

The ratio between 44.1 and 48 is not an integer, so the converter performs asynchronous resampling, where quality differences show more clearly than in integer ratios. Use an offline converter with an anti-aliasing filter rather than exporting with real-time preview settings.

## Keep 96 kHz in production

The point of 96 kHz is margin for pitch shifting, time stretching and nonlinear plugins, not a delivery format. Files double in size, plugins work harder, and the receiver often converts back to 48 anyway. Deliver 96 only when the whole project was made there and the publisher asks for it; otherwise work at 96, deliver at 48, and archive the high-rate session.

## How it goes wrong

- Changing only the header or extension, so speed and pitch shift
- A file labelled 48 kHz that actually holds 44.1, drifting as soon as it is imported
- Resampling after the limiter, with no true-peak recheck
- A batch that mixes 44.1 and 48, impossible to align in the edit
- Upconverting 44.1 to 96 for supposed clarity, gaining size but no detail
:::
