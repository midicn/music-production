---
id: monitor-placement
site: prod
cat: A5
title: 监听音箱摆放
title_en: Monitor Placement
summary: 摆位决定低频、声像与反射，先动音箱再动均衡。
summary_en: Placement sets low-end, imaging and reflections. Move the speakers before reaching for EQ.
level: standard
tags: [监听, 摆位, 声像, 边界增强, 梳状滤波]
tags_en: [monitoring, placement, imaging, boundary gain, comb filtering]
alias: [音箱摆位, 监听摆位, 听音位, speaker placement, monitor placement]
links:
  - "[[glossary:nearfield-monitor]]"
  - "[[glossary:monitoring]]"
  - "[[glossary:comb-filtering]]"
  - "[[instrument:piano]]"
instances:
  - essen-000191 | 单声部民歌，声源简单，最适合检查人声是否居中（C1）
  - pdmx-000237 | 钢琴与贝斯的多轨爵士，低音与钢琴的左右关系清楚（C1）
  - mutopia-000497 | 贝多芬第五交响曲，声部宽，用来检查声场宽度与对称（C1）
sources:
  - Toole, Floyd，Sound Reproduction（Focal Press）— 监听摆位与房间章节核对，未引用
  - Newell, Philip，Recording Studio Design（Focal Press）— 控制室几何章节核对，未引用
updated: 2026-10-28
---

::: zh
## 问题
同样的音箱，放在桌上、贴墙、左右不对称，声像就会偏，低频不是多就是少。多数「音箱不好听」先出在摆位，而不是单元。

## 物理或房间
音箱靠近墙面会被边界增强，距墙距离还会与直达声抵消，形成梳状滤波。左右不对称让早期反射不同，声像向一侧拉。高音单元偏离耳高，高频会衰减。两箱与头成等边三角形时声像最稳；桌面反射会在中频挖谷。

## 做法与判断
把两箱放在对称位置，高音单元与耳齐，间距与听音距离接近等边三角形。离前墙留可调距离，避开已知抵消频率；轻微内倾，让轴线在听音位后方交叉。桌面与音箱之间做减震。先挪位置，再考虑均衡。

## 听什么
播单声道人声，应停在正中间；偏左或偏右，先查对称与角度。播低音提琴，慢慢移动头部，听低频是否突然变实。再听混响宽度，确认不是被侧墙拉宽。

## 常见误解
近场音箱不能消除房间，只是提高直达声比例。音箱不是越大越好，房间与距离不匹配时更难整合。脚钉与垫材解决振动与高度，不是低频模式。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5"],"label":"单声道中心测试","label_en":"Mono centre test","hint":"播这条单声道短句，声音应稳定停在两只音箱中间；偏了先查对称与角度。","hint_en":"Play this mono phrase; it should stay centred between the speakers. If it pulls, check symmetry and angle first."}
```
:::

::: en
## The problem
The same speaker on a desk, against a wall or off-centre shifts the image and changes the bass. Most bad-speaker complaints start with placement.

## Physics or room
Near a wall the speaker gets boundary gain, and its distance to the wall can cancel direct sound and create comb filtering. Asymmetry makes early reflections differ and pulls the image sideways. A tweeter below ear height loses highs. An equilateral triangle stabilises the image; a desk reflection scoops the midrange.

## Practice and judgement
Place speakers symmetrically, tweeters at ear height, spacing close to the listening distance. Leave a gap to the front wall and avoid predicted cancellations; toe in so axes cross behind your head. Decouple speakers from the desk. Move before equalising.

## What to listen for
Play mono voice; it should sit dead centre. If it pulls left or right, check symmetry and angle. On double bass, move your head and listen for the point where the low end locks in. Then judge reverb width, not just side-wall reflection.

## Common misunderstandings
Nearfields do not remove the room, only raise the direct-to-reflected ratio. Bigger is not better when the room and distance do not suit it. Spikes and pads change vibration and height, not room modes.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5"],"label":"Mono centre test","label_en":"Mono centre test","hint":"Play this mono phrase; it should stay centred between the speakers. If it pulls, check symmetry and angle first.","hint_en":"Play this mono phrase; it should stay centred between the speakers. If it pulls, check symmetry and angle first."}
```
:::
