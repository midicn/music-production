---
id: job-game-sfx
site: prod
cat: D
order: 521
title: 游戏音效
title_en: Game Sound Effects
summary: 按事件做短音效，控制长度、峰值与变体，交进引擎就能触发。
summary_en: Event-driven sound effects with controlled length, peak and variants, ready to trigger in the engine.
level: standard
tags: [流程, 游戏音频, 音效, 引擎]
tags_en: [workflow, game audio, sfx, engine]
alias: [游戏音效, 音效制作, SFX, game sfx]
links:
  - "[[glossary:sound-design]]"
  - "[[glossary:headroom]]"
  - "[[instrument:electronic-drums]]"
instances:
  - oga-000053 | 一秒八的 fanfare，十九个音，可听奖励提示怎样短到不打断操作
  - oga-000334 | 六秒的胜利短曲，句法完整，适合对照「提示」与「过场」的长度差别
  - oga-000283 | 四秒半的选单音，起音清楚，可参考 UI 音效的收尾
  - oga-000031 | 五十七秒、三十九个音的循环，留白多，可作环境底噪层的参照
sources:
  - Audiokinetic Wwise Help（官方文档）— 音频文件导入、Event 与 Sound SFX 的组织方式。
  - Marks, Aaron. The Complete Guide to Game Audio（Focal Press）— 事件、变体与交互音频实务。
  - Unity Asset Store Submission Guidelines — Audio 分类对峰值、切片与首尾静音的要求。
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
## 先按事件分类，不按音色分类

游戏音效的最小单位是事件：玩家点了什么、打中了什么、踩到了什么。先列事件表，写清触发条件、同时可能响几条、一分钟会重复几次，再决定做几条变体。只做一条，玩家听十次就腻；做十条，包体和维护成本一起涨。判断标准是重复频率，不是音色好不好听。

## 长度与峰值按事件定

| 事件 | 常见长度 | 变体 | 关键处理 |
|---|---|---|---|
| UI 点击 | 60–200 毫秒 | 2–3 条 | 起音清楚，尾音短 |
| 奖励、升级 | 1–3 秒 | 1–2 条 | 句法完整，可留尾 |
| 武器、命中 | 200–600 毫秒 | 3–5 条 | 起音硬，低频收住 |
| 脚步 | 100–300 毫秒 | 4–8 条 | 与地面材质配套 |
| 环境层 | 20–60 秒循环 | 1–2 条 | 无缝，低频留余量 |

表里的长度是起点，不是标准。真正的上限由同屏叠加决定：十个命中同时响，单条再干净也会糊。峰值留 3–6 dB 余量，给引擎里的总线压缩和音乐留位置。

## 从素材到引擎的顺序

交 48 kHz、24 bit WAV 干声，循环另附无缝版与循环点位置。先做干声，不加混响；混响进引擎再做，否则同一个音效换到洞穴里就带着房间味。统一峰值与起点，切掉首尾多余静音，只留五到十毫秒防爆音。变体不要只随机音高，改起音、尾音和一点长度，听感才不会像玩具。循环音效首尾各留同样长的尾巴，交叉淡化后再进 Wwise 或 FMOD。命名按事件、材质、序号写，程序照表就能挂上。导入后先单独听，再叠对白、音乐和环境试三次。

## 验收要在游戏里听

- 同一事件连发十次，没有一条像复读
- 最响的命中不盖过对白与音乐
- 快速点击 UI，声音不糊成一片
- 脚步换地面时没有爆音
- 3D 移动时近处不炸、远处不凭空消失
- 循环接缝听不出来
- 文件名与事件表一一对应
- 包体在预算内

## 失败模式

把混响烘进文件，换场景就脏；变体只做音高随机，听感像玩具；峰值顶到零，叠加后削波；UI 音效拖到一秒，连点变噪音；环境循环只有十秒，玩家很快听出周期；命名靠 final2，程序找不到；音效和对白同频段，战斗时听不清台词；只交大文件，移动端包体超标。

```audiolab
{"type":"instrument","gm":"Taiko Drum","synth":"struck","phrase":["D2","D2","A2"],"label":"命中与收尾的三个音","label_en":"Three hits for impact and release","hint":"前两下短，第三下落低，听尾音多长才不拖进下一次触发","hint_en":"Keep the first two short and let the third fall; hear how long a tail can run before it muddies the next trigger"}
```
:::

::: en
## Sort by event, not by timbre

The smallest unit in game audio is the event: what the player clicked, hit or stepped on. Build an event list first, with the trigger condition, how many instances can sound at once and how often the event repeats in a minute, then decide how many variants to make. One variant tires after ten repeats; ten variants raise the package size and the maintenance cost. Repetition rate is the test, not whether the timbre sounds cool.

## Length and peak by event

| Event | Typical length | Variants | Key treatment |
|---|---|---|---|
| UI click | 60–200 ms | 2–3 | Clear attack, short tail |
| Reward, level-up | 1–3 s | 1–2 | Complete phrase, tail allowed |
| Weapon, impact | 200–600 ms | 3–5 | Hard attack, low end controlled |
| Footstep | 100–300 ms | 4–8 | Matched to floor material |
| Ambience | 20–60 s loop | 1–2 | Seamless, low end kept in reserve |

The lengths are starting points, not rules. The real ceiling comes from stacking: ten impacts at once turn any clean file into mud. Leave 3–6 dB of peak margin for bus compression and music in the engine.

## From source to engine

Deliver dry 48 kHz, 24 bit WAV files, with a seamless version and loop point for anything that loops. Work dry without reverb; add reverb in the engine, or the same effect carries the room into a cave. Match peaks and start points, trim excess silence and leave five to ten milliseconds to avoid a click. Do not randomize pitch alone; vary the attack, the tail and a little length so the variants do not sound like toys. For loops, leave an equal tail at both ends and crossfade before importing into Wwise or FMOD. Name by event, material and index so the programmer can attach it from the list. Audition each file alone, then with dialogue, music and ambience three times.

## Check it inside the game

- Ten repeats of the same event, none sounding like a copy
- The loudest impact does not cover dialogue or music
- Fast UI clicks do not blur into noise
- No pop when footsteps change surface
- In 3D, close sounds do not explode and distant ones do not vanish
- The loop seam is inaudible
- File names match the event list one to one
- The package fits the size budget

## Failure modes

Reverb baked into the file turns dirty in another space. Pitch-only variants sound like toys. Peaks at zero clip once stacked. A one-second UI sound becomes noise under fast clicking. A ten-second ambience loop reveals its period. Names like final2 cannot be found by the programmer. Effects share the dialogue band and lines disappear in combat. Only large files are delivered, and the mobile package goes over budget.
:::
