---
id: ai-music-introduction
site: prod
cat: B7
title: AI 音乐导论
title_en: Introduction to AI Music
summary: AI 音乐分符号与音频两条路，各自解决不同的生成问题。
summary_en: AI music follows two paths, symbolic and audio, each solving a different generation problem.
level: standard
tags: [AI, 生成, 符号音乐, 音频]
tags_en: [AI, generation, symbolic music, audio]
alias: [AI 音乐导论, 人工智能音乐, AI 音乐, AI music, generative music]
links:
  - "[[glossary:midi-protocol]]"
  - "[[glossary:sampler]]"
  - "[[glossary:music-copyright]]"
instances:
  - atepp-001875 | 巴洛克创意曲的主题追逐，是符号模型最容易学到的结构
  - thesession-000000 | 同一首民间曲调有大量变体，能看出风格与具体版本的差别
  - oga-000033 | 游戏配乐层层叠加，适合判断音频生成能否做出同样的层次
  - atepp-000369 | 自由速度的夜曲，最能检验生成结果有没有演奏呼吸
sources:
  - 符号音乐生成与音频生成的综述结论，依 ISMIR 公开论文核查，未抄文本
  - 生成式音乐工具的输入条件与输出形态，依公开文档核查，未抄文本
updated: 2026-10-28
---

::: zh
让机器写出一段像某风格的音乐，今天不难；难的是让它服从结构、可以修改、权利清楚。

## 问题

一段音乐包含音高、节奏、和声、配器与演奏表情。生成哪一层，决定了输出能不能改、像不像、归谁。

## 原理或流程

符号域把音符与控制器当数据，在事件层面学习上下文，输出 MIDI 或乐谱，改一个音很容易。音频域直接在波形或频谱上生成，听感完整，却难以拆开。训练把大量作品压成统计规律，生成时按提示与条件采样；风格、段落与时长分别由不同条件控制。

## 做法与判断

先明确要的是小样、素材还是成品。要改就选符号或分层输出，要成品就选音频。检查能否指定调性、段落与时长，保留人工编辑环节，记录工具版本与提示，方便复现和替换。

## 听什么

听段落转折是否生硬，和声是否长期停在同一个区域，重复是否机械。再听尾音与混响，判断它是音乐结束还是文件结束。

## 常见误解

AI 会作曲；听起来像就等于合法；一次生成就能交付。工具能给出候选，判断仍要由人做。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","D4","E4","G4","A4","G4","E4"],"label":"一条可被续写的短句","label_en":"A short phrase waiting to be continued","hint":"听完最后两个音，想一个模型会怎样接下去，再想它会不会只是重复开头","hint_en":"After the last two notes, imagine how a model would continue, and whether it would simply repeat the opening"}
```
:::

::: en
Making a machine produce music in a recognisable style is no longer hard. Making it follow structure, stay editable and carry clear rights is.

## The problem

Music involves pitch, rhythm, harmony, orchestration and performance expression. Which layer is generated decides whether the output can be edited, how convincing it sounds and who owns it.

## How it works

Symbolic systems treat notes and controllers as data, learn context at the event level and output MIDI or notation, where one note is easy to change. Audio systems generate waveforms or spectra, sounding complete but hard to take apart. Training compresses a corpus into statistical patterns; generation samples under a prompt and conditions for style, section and length.

## Practice and judgement

Decide whether you need a demo, material or a finished track. Choose symbolic or layered output when edits matter, audio when the finished sound matters. Check key, section and duration controls, keep a human editing stage, and log tool versions and prompts for reproduction.

## What to listen for

Hear whether section changes are abrupt, harmony sits in one place and repetition feels mechanical. Then hear tails and reverb, and ask whether the music ends or the file ends.

## Common misunderstandings

AI composes; sounding similar is lawful; one generation is deliverable. Tools offer candidates; judgement remains human.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "D4", "E4", "G4", "A4", "G4", "E4"], "label": "A short phrase waiting to be continued", "label_en": "A short phrase waiting to be continued", "hint": "听完最后两个音，想一个模型会怎样接下去，再想它会不会只是重复开头", "hint_en": "After the last two notes, imagine how a model would continue, and whether it would simply repeat the opening"}
```
:::
