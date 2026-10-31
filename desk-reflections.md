---
id: desk-reflections
site: prod
cat: A5
title: 桌面反射
title_en: Desk Reflections
summary: 桌面、调音台与屏幕的早期反射，会在中频挖出梳状凹陷。
summary_en: Early reflections from the desk, console and screen comb-filter the midrange before the room gets a say.
level: standard
tags: [桌面反射, 早期反射, 梳状滤波, 控制室, 摆位]
tags_en: [desk reflections, early reflections, comb filtering, control room, placement]
alias: [桌面反射, 调音台反射, 屏幕反射, desk bounce, console reflection]
order: 394
links:
  - "[[glossary:comb-filtering]]"
  - "[[glossary:nearfield-monitor]]"
  - "[[glossary:monitoring]]"
  - "[[instrument:digital-piano]]"
instances:
  - essen-000191 | 单声部民歌，只有一条人声线，桌面反射造成的中频凹陷最容易辨认（C1）
  - mutopia-000546 | 人声与钢琴，中频集中，适合比较不同台面高度下的鼻音（C1）
  - pdmx-000237 | 钢琴与贝斯的爵士，钢琴中低音区能听出台面反射的空洞（C1）
sources:
  - Everest, F. Alton，Master Handbook of Acoustics（McGraw-Hill）— 早期反射与梳状滤波
  - Newell, Philip，Recording Studio Design（Focal Press）— 控制室台面与调音台反射
  - Genelec，Monitor Setup Guide（厂商文档）— 桌面摆放与声学处理建议
updated: 2026-10-31
---

::: zh
人声在中频发闷、军鼓的边击像被压扁，把音箱换到桌子另一侧，问题跟着桌子走。桌面、调音台斜面、屏幕，再加上近处侧墙，是最容易被忽略的几处反射面，它们离耳朵太近，反射声几乎与直达声同时到达。

## 路径差只有几十厘米

反射声比直达声多走的路程决定第一个凹谷，频率约为声速除以两倍路径差。多走 0.2 米，谷落在 860 Hz 附近；多走 0.4 米，谷落到 430 Hz。路径越短，谷越靠中高频，正好压在人声与军鼓的敏感区。梳状滤波是一串等间距的谷，不是一条光滑的下降曲线。

## 四个面各改什么

| 反射面 | 典型路径差 | 首个凹谷 | 症状 | 处理 |
|---|---|---|---|---|
| 桌面 | 0.15–0.30 米 | 570–1140 Hz | 人声鼻音、木吉他发硬 | 倾斜或铺吸声垫 |
| 调音台斜面 | 0.10–0.25 米 | 690–1700 Hz | 中高频毛刺 | 减少平面、换角度 |
| 屏幕 | 0.20–0.35 米 | 490–860 Hz | 中央声像发虚 | 后移、降低、吸声 |
| 近侧墙 | 0.30–0.60 米 | 290–570 Hz | 宽度不自然 | 对称吸声或扩散 |

## 桌子怎么改

把音箱抬到支架上，让箱体前沿与桌面齐平或略高，减少桌面反射进入轴线的比例。桌面无法撤掉时，在音箱与听音位之间的桌面上铺吸声垫，正对反射点。调音台倾斜安装比平放好，屏幕后移并压低，让反射点落到头后方。所有改动保持左右对称，否则声像会偏。

## 别把反射当成音箱缺陷

同一对音箱在两张桌子上表现不同，说明问题在反射，不在单元。近场监听提高直达声比例，但桌面反射的路径差太小，近场消不掉。用均衡压掉那个谷往往无效，因为谷由时间差造成，不是频响不平。判断办法很简单：把音箱抬高三十厘米再听，凹陷移动或消失，就是桌面反射。

```audiolab
{"type":"instrument","gm":"Marimba","synth":"struck","phrase":["C4","D4","E4","G4"],"label":"中频凹陷听辨","label_en":"Hearing a midrange notch","hint":"播这四颗音，再把头低下去贴近桌面又抬起；某个音忽厚忽薄，说明反射路径在变。","hint_en":"Play these four notes, then drop your head toward the desk and raise it again; a note that thickens and thins marks the reflection path changing."}
```
:::

::: en

A vocal sounds dull in the midrange and a snare rim click seems squashed; move the speakers to the other side of the desk and the problem follows the desk. The desktop, the console surface and the screen are the three reflectors people forget, and all three sit close enough that their reflections arrive almost with the direct sound.

## A path difference of centimetres

The extra distance the reflection travels sets the first notch, at roughly the speed of sound divided by twice that difference. An extra 0.2 m puts the notch near 860 Hz; 0.4 m brings it to 430 Hz. Shorter paths push the notch up into the region where voices and snares live. The result is a comb of evenly spaced notches, not a smooth roll-off.

## What each surface does

| Surface | Typical path difference | First notch | Symptom | Treatment |
|---|---|---|---|---|
| Desktop | 0.15–0.30 m | 570–1140 Hz | Nasal voice, hard acoustic guitar | Angle it or add a pad |
| Console top | 0.10–0.25 m | 690–1700 Hz | Midrange grit | Break up the flat area |
| Screen | 0.20–0.35 m | 490–860 Hz | Soft centre image | Move back and down |
| Near side wall | 0.30–0.60 m | 290–570 Hz | Unnatural width | Symmetrical absorption |

## Fixing the desk, not the speaker

Raise the monitors on stands so the front edge sits level with or slightly above the desktop, which keeps the desk reflection out of the listening axis. If the desk has to stay, lay an absorbent pad on the desk between speaker and listener, right on the reflection point. An angled console beats a flat one; push the screen back and lower it so its reflection lands behind your head. Keep every change symmetrical or the image will shift.

## A reflection is not a driver fault

When the same pair behaves differently on two desks, the desk is the variable. Nearfield monitoring raises the ratio of direct to reflected sound, but the desk path is so short that proximity does not remove it. EQ rarely helps, because the notch comes from a time difference rather than a tilted response. The quick test: lift the speakers thirty centimetres and listen again; if the dip moves or disappears, the desk caused it.

```audiolab
{"type":"instrument","gm":"Marimba","synth":"struck","phrase":["C4","D4","E4","G4"],"label":"Hearing a midrange notch","label_en":"Hearing a midrange notch","hint":"Play these four notes, then drop your head toward the desk and raise it again; a note that thickens and thins marks the reflection path changing.","hint_en":"Play these four notes, then drop your head toward the desk and raise it again; a note that thickens and thins marks the reflection path changing."}
```
:::
