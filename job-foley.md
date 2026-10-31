---
id: job-foley
site: prod
cat: D
order: 522
title: 拟音
title_en: Foley
summary: 用道具和表演对上画面，交同步、无底噪的拟音轨。
summary_en: Props and performance locked to picture, delivered as clean, sync-accurate Foley tracks.
level: standard
tags: [流程, 拟音, 影视后期, 同步]
tags_en: [workflow, foley, post-production, sync]
alias: [拟音, foley, 拟音棚, 脚步拟音]
links:
  - "[[glossary:sound-design]]"
  - "[[glossary:reverb]]"
  - "[[instrument:drum-kit]]"
instances:
  - groove-000007 | 六十五拍的慢速鼓型，间隔宽，可对照脚步与动作的落点
  - groove-000002 | 八十六拍的灵魂乐鼓型，起音清楚，适合练动作与声音的同步
  - oga-000076 | 八秒的四小节鼓型，短而完整，可参考一次性动作的收尾
  - oga-000031 | 五十七秒、只有三十九个音的循环，留白多，可对照拟音轨该留多少空气
sources:
  - SMPTE ST 12-1 — 时间码（Time and Control Code）的帧率与同步口径。
  - Vanessa Theme Ament, The Foley Grail：The Art of Performing Sound for Film, Games, and Animation（Focal Press）— 拟音棚、道具与表演方法。
  - iZotope RX 官方文档 — De-noise、De-click 与频谱修复的使用边界。
tool_kind: guide
tool_vendor: —
tool_form: 流程
tool_platforms: [通用]
tool_price: 不适用
tool_jobs: [流程]
tool_verified: 2026-10-31
updated: 2026-10-31
---

::: zh
## 拟音是表演，不是找素材

脚步、衣物、开门、放下杯子，这些声音的说服力来自表演：重量、节奏、犹豫、克制。素材库能给环境层和远处的声音，给不了「这个人踮着脚走过湿地板」。先看锁定画面，列出动作表和每个动作要传达的信息，再决定用哪些道具。观众听不出拟音，只会觉得这个人真实或不真实。

## 从道具到轨道

按动作表准备道具：不同鞋底、布料、钥匙、门锁、杯碟。棚里铺好对应地面，脚步在固定位置原地演，别跟着画面走动。传声器距离固定，录干声，保留动作之间的自然间隔。每一条按动作切，不按整场切，同步点写进标记。轻高通去掉低频轰鸣，用 RX 或同类工具少量去噪，混响留到混音阶段。脚步、衣物、道具分轨，后期才能单独调。

## 同步点清单

- 脚跟落地与画面接触同帧，最多差一帧
- 衣物声比动作晚一到两帧，不提前
- 道具放下先有接触声，再有滑动声
- 每次脚步有变化，不复制同一条
- 用力声只在动作需要时加
- 关门有锁舌与门框两段
- 动作之间保留环境声，不切出真空
- 拟音不与对白抢中频

## 棚里的声音怎么保真

小振膜电容或动圈都行，近讲，避开强反射面；地面铺厚毯，墙面用吸音板压住拍手声。监听用封闭耳机，别把棚的回声当成素材。录 48 kHz、24 bit，保留原始 take 与同步标记。底噪要低于对白轨，否则一叠上去就听到棚的嘶声。降噪只去持续成分，布料和纸张的细碎声一压就假。

## 什么时候不该补拟音

画面没锁定就录，剪辑一改全废；用库音效代替表演，脚步像飘在地上；每条脚步同一 take，听感机械；拟音盖住对白；混响烘得太湿，和场景不匹配；棚的底噪比对白高；动作与声音差两三帧，观众说不出哪里怪；把拟音和音乐混成一轨交，混音师无法单独处理；降噪过度，布料声变成纸片。

```audiolab
{"type":"instrument","drum":"35","synth":"perc","phrase":["35","35","35"],"label":"三下脚步的间隔","label_en":"Three footsteps and the space between","hint":"听三下的间隔是否均匀，再想画面里哪一步该重一点","hint_en":"Hear whether the spacing is even, then decide which step in the picture should land harder"}
```
:::

::: en
## Foley is a performance, not a search

Footsteps, cloth, a door, a cup set down: these sounds persuade through performance, through weight, pace, hesitation and restraint. A library can supply ambience and distant sound, but not the sense of someone tiptoeing across a wet floor. Watch the locked picture, list the actions and what each one has to say, then choose the props. The audience does not hear Foley; they only decide whether the person feels real.

## From prop to track

Prepare props from the action list: different soles, fabrics, keys, locks, cups and plates. Lay the matching floor in the studio and perform footsteps in place rather than walking with the picture. Keep the microphone distance fixed, record dry and preserve the natural gaps between actions. Cut each take by action, not by scene, and mark the sync points. Use a gentle high-pass against rumble, light noise reduction in RX or a similar tool, and leave reverb for the mix. Keep footsteps, cloth and props on separate tracks so they can be balanced later.

## Sync checklist

- Heel contact on the same frame as the picture, within one frame at most
- Cloth arrives one or two frames after the move, never before
- A prop makes contact before it slides
- Every step differs; no take is copied
- Effort sounds appear only where the action needs them
- A door close has both latch and door frame
- Room tone stays between actions, with no vacuum
- Foley does not fight dialogue in the midrange

## Keeping the recording clean

Either a small-diaphragm condenser or a dynamic microphone works; stay close and avoid hard reflective surfaces. Cover the floor with thick rug and tame the walls with absorbers so a handclap does not ring. Monitor on closed headphones and do not mistake the room for the source. Record 48 kHz, 24 bit and keep the original takes with sync marks. The noise floor must sit below the dialogue track, or the studio hiss arrives with every layer. Remove steady noise only; over-clean cloth and paper turn into thin sheets.

## When not to add Foley

Recording before picture lock wastes every take when the cut changes. Library effects instead of performance make the feet float. One take for every step sounds mechanical. Foley covers dialogue. Too much reverb does not match the space. The studio floor is louder than the dialogue. Sound and action drift two or three frames and the viewer cannot say why it feels wrong. Foley is mixed into the music stem, so the mixer cannot separate it. Over-reduction turns cloth into paper.
:::
