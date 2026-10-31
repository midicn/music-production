---
id: guitar-miking
site: prod
cat: A4
order: 361
title: 吉他拾音
title_en: Guitar Miking
summary: 电吉他先定音箱、房间与纸盆位置，木吉他先避开音孔
summary_en: For electric guitar, settle the amp, the room and the cone; for acoustic, move away from the soundhole.
level: standard
tags: [吉他, 拾音, 音箱, 相位, 梳状滤波]
tags_en: [guitar, miking, amplifier, phase, comb filtering]
alias: [吉他拾音, 吉他录音, 音箱拾音, 木吉他录音, guitar miking, guitar recording]
links:
  - "[[instrument:electric-guitar]]"
  - "[[instrument:acoustic-guitar]]"
  - "[[glossary:phase]]"
  - "[[glossary:comb-filtering]]"
instances:
  - mutopia-001639 | 塔雷加《阿德丽塔》旋律与低音分得开，音孔与十二品的低频差别容易听出（C1）
  - mutopia-000060 | 《西班牙罗曼史》分解和弦连续，音孔话筒最容易把低音弦收成轰鸣（C1）
  - mutopia-001203 | 梅尔茨 A 小调练习曲句短、音区集中，适合固定摆位后比较三档距离（C1）
sources:
  - Bobby Owsinski，The Recording Engineer's Handbook（Bobby Owsinski Media Group）— 吉他音箱与木吉他录音
  - Eargle, John，The Microphone Book（Focal Press）— 纸盆位置与双话筒相位
  - Shure，Microphone Techniques for Recording（厂商文档）— 乐器摆位与相位
updated: 2026-10-31
---

::: zh
电吉他录成纸片，多半是话筒站在纸盆最亮的一圈上；木吉他轰成一团，多半是对着音孔。这两件事都发生在拧增益之前。

## 音箱与纸盆：先定声源，再定点

同一台音箱，音量从三成推到七成，纸盆的压缩与泛音会换一层，所以先让吉他手在房间里调到想要的动静，再摆话筒。话筒离网布二到五厘米，略偏轴十五到三十度，高频收一点，更接近耳朵在箱前听到的样子。

| 位置 | 距离 | 音色 | 风险 |
|---|---|---|---|
| 防尘帽中心 | 2–5 厘米 | 亮，齿感强 | 失真刺耳 |
| 防尘帽边缘 | 3–6 厘米 | 平衡，常见起点 | 受指向影响大 |
| 纸盆外圈 | 3–8 厘米 | 暗，厚度足 | 混音里发闷 |

表里的位置只对应一只纸盆，换音箱或纸盆尺寸都要重听。音箱摆位也属于房间：离墙半米以上，别塞进角落，墙角会堆低频，近墙的反射会糊掉起音。房间太硬，先搬音箱、挂厚布，再换话筒。

## 双话筒的距离账

两支话筒收同一声源，路程差造成梳状滤波。一毫秒约三十四厘米，两支差十厘米，第一个陷波就落在中高频。做法有三种：一近一远，远的压低；两支并排贴紧，当作一支用；或者录完在 DAW 里对齐波形。相位没查之前，不要用均衡去填那个陷波。两支型号不同时，先听音色差，再决定谁主谁辅。

## 木吉他的两个拾音点

木吉他不要对着音孔。音孔收的是空腔共鸣，低频轰；对准十二品，距离十五到二十五厘米，略偏琴颈，手指与琴弦的细节更清楚。想要立体声，用一对小振膜做 XY，或把间距拉到三十到五十厘米，先查单声道兼容。右手位置、指甲长度、椅子吱呀声，比话筒型号更能改变结果。

## 哪里会坏

话筒贴住网布，近讲效应把声音变厚，箱体震动也收成隆隆声。电吉他同时走 DI 和话筒，两轨之间的延迟要用耳朵对，不要只看波形；对齐到采样点，反而可能丢掉一点自然的厚度。房间很小、音箱很响时，近点话筒会把墙面反射一起收进来，听起来像蒙了一层；这时换话筒位置只是在几种妥协里挑一个，先加临时吸声或换个房间更有效。

```audiolab
{"type":"instrument","gm":"Acoustic Guitar (steel)","synth":"plucked","phrase":["E3","B3","E4","G#4","B4","E4"],"label":"十二品与音孔之间的音色","label_en":"Tone between the 12th fret and the soundhole","hint":"先听起音里的指甲与琴弦，再想话筒移向音孔后低频会多出什么","hint_en":"Hear nail and string in the attack, then imagine the low end as the mic moves to the soundhole"}
```
:::

::: en
A thin electric guitar usually comes from the mic sitting on the brightest ring of the cone; a boomy acoustic usually comes from aiming at the soundhole. Both happen before you touch the gain.

## The amp and the cone: fix the source, then the point

Push the same amp from three to seven on the dial and the cone compression and overtones change character, so let the player find the sound in the room before you place a microphone. Put the mic 2 to 5 cm off the grille and 15 to 30 degrees off axis: the top end softens toward what an ear hears in front of the cab.

| Position | Distance | Tone | Risk |
|---|---|---|---|
| Dust cap centre | 2–5 cm | Bright, edgy | Harsh distortion |
| Edge of the cap | 3–6 cm | Balanced, usual start | Sensitive to angle |
| Outer cone | 3–8 cm | Dark and thick | Dull in the mix |

Those positions describe one cone. Change the speaker or its size and listen again. The cab is part of the room too: keep it at least half a metre off the wall and out of corners, where the low end piles up and nearby reflections smear the attack. In a hard room, move the cab or hang heavy cloth before changing microphones.

## The distance bill for two mics

Two mics on one source arrive at different times, and the difference produces comb filtering. One millisecond is roughly 34 cm, so a 10 cm gap puts the first notch in the upper midrange. Three options: a close mic plus a distant one turned down, two mics taped together as one, or align the waveforms after recording. Do not reach for EQ to fill that notch before checking polarity. If the two models differ, judge the tonal gap first and decide which one leads.

## Two points for acoustic guitar

Do not aim at the soundhole. It captures the cavity resonance and turns the low end to mud. Aim at the 12th fret from 15 to 25 cm, slightly toward the neck, and finger and string detail comes through. For width, use a small-diaphragm pair in XY, or space them 30 to 50 cm apart, then check mono. Right-hand position, nail length and a creaking chair change the result more than the mic model does.

## Where it breaks

Push the mic against the grille cloth and proximity effect thickens the tone while cabinet vibration becomes rumble. When you track DI and mic together, align the two tracks by ear rather than by waveform alone; snapping them to the sample can cost a little natural weight. In a small room with a loud amp, the close mic collects wall reflections and the guitar sounds veiled; moving the mic only picks a different compromise, so add temporary absorption or change rooms first.

```audiolab
{"type":"instrument","gm":"Acoustic Guitar (steel)","synth":"plucked","phrase":["E3","B3","E4","G#4","B4","E4"],"label":"十二品与音孔之间的音色","label_en":"Tone between the 12th fret and the soundhole","hint":"先听起音里的指甲与琴弦，再想话筒移向音孔后低频会多出什么","hint_en":"Hear nail and string in the attack, then imagine the low end as the mic moves to the soundhole"}
```
:::
