---
id: vocal-miking
site: prod
cat: A4
order: 363
title: 人声拾音
title_en: Vocal Miking
summary: 齿音、爆破与房间声，多数能在摆位上解决，换话筒往往排在后面
summary_en: Most sibilance, plosive and room problems yield to placement before a new mic.
level: standard
tags: [人声, 拾音, 指向, 齿音, 房间]
tags_en: [vocals, miking, polar pattern, sibilance, room]
alias: [人声拾音, 人声录音, 唱歌录音, 话筒距离, vocal miking, vocal recording]
links:
  - "[[instrument:voice]]"
  - "[[glossary:polar-pattern]]"
  - "[[glossary:condenser-microphone]]"
  - "[[glossary:noise-floor]]"
instances:
  - openscore-000008 | 《魔王》在叙事与角色之间切换，从耳语到喊叫，距离与指向一变就听得出（C1）
  - openscore-000018 | 福雷的练声曲没有字词，气口与房间声成为主要信息（C1）
  - m21-000065 | 巴赫四部众赞歌，四声部同录，单支话筒的距离决定声部能否抱在一起（C1）
sources:
  - Huber & Runstein, Modern Recording Techniques, vocal tracking chapter
  - Bartlett, Practical Recording Techniques, vocal miking section
  - Shure, Microphone Techniques for Recording（厂商文档）
updated: 2026-10-31
---

::: zh
## 三个数先站住

人声话筒有几个能测出来的起点：嘴到网罩十五到二十五厘米，话筒高过嘴十到十五厘米，偏轴十到二十度。电容话筒按这组数起步；喊唱与说唱可以收到五到十厘米，代价是近讲效应把低频顶起来，需要在话放或均衡上收一点。防喷罩离网罩五厘米左右，贴着嘴唇放，气流照样打在振膜上。

## 按症状分诊

| 症状 | 先改 | 再改 |
|---|---|---|
| 齿音刺 | 抬高十到十五厘米，偏轴十到二十度 | 去齿音，换话筒 |
| 爆破音重 | 防喷罩离网罩五厘米，略偏轴 | 高通，剪辑补 |
| 房间声多 | 心形指向，歌手背后挂厚毯 | 吸音屏，另找房间 |
| 声音发闷 | 退后五厘米，查是否贴住网罩 | 换电容话筒 |
| 耳机漏音 | 压低伴奏，让歌手靠近 | 换封闭耳机 |

表格的顺序就是动手的顺序：摆位能解决的，不先动插件，更不先换话筒。

## 齿音与爆破

齿音集中在五到八千赫兹，是气流经过牙齿的瞬态。话筒抬高、偏轴，齿音先退一步，再去考虑去齿音插件；压过头，s 会变成 th，字头一起糊掉。爆破音是 p、b、t 那一口气，直接打在振膜上就是低频砰声，偏轴加防喷罩能压住大半。近讲效应在十厘米以内最明显，声音变厚、低频变多；要这种质感就留着，不要就在话放上切掉八十赫兹以下。

## 指向选的是房间

心形指向压的是背后，不是正面。卧室里两面平行的墙会把反射直接送回话筒，挂一条厚毯、放一块吸音屏，比换一支更贵的话筒有用。全指向收的是整个房间，只有房间本身好听时才值得用。耳机音量开大，节拍声会从耳罩缝里漏进人声轨，后期几乎拿不掉；把伴奏压低，让歌手靠近话筒唱。

## 什么时候该退后

古典、民歌、需要大动态的段落，近讲会把强弱压平。让歌手退到半米到一米，用房间声托住音色，动态才留得住。房间不好又非要远距离，只会把噪声和反射一起收进来；这时近一点、加一点混响，比追求自然更诚实。

```audiolab
{"type":"instrument","gm":"Voice Oohs","synth":"vocal","phrase":["A3","C4","E4","A4","G4","E4"],"label":"距离与气口","label_en":"Distance and breath","hint":"先听每个音的起音与元音，再想话筒退后二十厘米时气口与房间谁先出现","hint_en":"Hear each onset and vowel, then imagine breath versus room 20 cm farther back"}
```
:::

::: en
## Three numbers to start from

A vocal mic has a few measurable starting points: 15 to 25 cm from mouth to grille, 10 to 15 cm above the mouth, and 10 to 20 degrees off axis. A condenser works well from there. Shouting and rap can move in to 5 or 10 cm, at the cost of proximity effect lifting the low end, which needs a little control at the preamp or on the EQ. Keep the pop filter about 5 cm off the grille; pressed against the lips, the air still reaches the diaphragm.

## Sorting by symptom

| Symptom | Change first | Change later |
|---|---|---|
| Piercing sibilance | Raise 10–15 cm, angle 10–20 degrees | De-esser, different mic |
| Heavy plosives | Pop filter 5 cm off the grille, off axis | High-pass, edit the take |
| Too much room | Cardioid, blanket behind the singer | Booth panel, another room |
| Dull, boxy voice | Move back 5 cm, check grille contact | A condenser instead |
| Headphone bleed | Lower the backing, singer steps in | Closed-back headphones |

The order of the table is the order of the work: if placement can fix it, do not reach for a plugin, and do not change the microphone first.

## Sibilance and plosives

Sibilance lives around 5 to 8 kHz and comes from air passing the teeth. Raise the mic and angle it off axis and the sibilance steps back before you touch a de-esser. Push the reduction too far and "s" turns into "th" while the consonants smear. Plosives are the puff behind p, b and t; straight into the diaphragm it lands as a low thump, and an off-axis angle plus a pop filter removes most of it. Proximity effect is strongest inside 10 cm, thickening the voice and adding low end. Keep it if that is the sound; if not, roll off below 80 Hz at the preamp.

## The pattern chooses the room

Cardioid rejects what is behind the mic, not what is in front. In a bedroom, two parallel walls send reflections straight back into the capsule, and a heavy blanket or a booth panel does more than a more expensive microphone. Omni takes the whole room and only earns its place when the room is worth hearing. Loud headphones leak the click through the earcup gap into the vocal track, where it cannot be removed later; lower the backing and let the singer work closer.

## When to step back

Classical singing, folk and wide dynamic passages flatten under a close mic. Move the singer back half a metre to a metre and let the room carry the tone so the dynamics survive. A poor room plus a distant mic only collects more noise and reflection; moving in and adding a little reverb is the more honest choice.
:::
