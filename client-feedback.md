---
id: client-feedback
site: prod
cat: A1
order: 304
title: 客户反馈轮次
title_en: Running Client Feedback Rounds
summary: 把“感觉不对”拆成可执行条目，一轮只改一类，再按同一标准验收。
summary_en: Turn a vague note into actionable items, change one class of problem per round, and accept against the same standard.
level: standard
tags: [客户, 修改, 验收, 流程]
tags_en: [client, revision, acceptance, workflow]
alias: [客户反馈, 修改轮次, 改稿流程, client feedback, revision rounds]
links:
  - "[[glossary:reference-track]]"
  - "[[glossary:mixdown]]"
  - "[[glossary:stem-mastering]]"
instances:
  - pdmx-000614 | 《致爱丽丝》的一份文件，可与另一版逐段对照，确认只改了该改的地方（CC0）
  - pdmx-000643 | 同一曲的另一份文件，适合练一轮只动一处的修改纪律（CC0）
  - oga-000002 | 九条轨的场景曲，客户说太满时可以从删层开始（CC0）
sources:
  - Bobby Owsinski, The Mixing Engineer's Handbook 关于修订、客户沟通与版本管理的章节
  - Avid Pro Tools 与 Apple Logic Pro 官方文档中关于工程快照、注释与导出版本的说明
  - AES 关于混音修订与母带交付流程的会议文献
updated: 2026-10-31
---

::: zh
客户说“感觉不对”，你回“哪里不对”，这一轮基本白改。反馈轮次要做的，是把一句感受变成时间点、问题类型和验收标准，然后按批次改，而不是边聊边改。

## 收：把感受落到时间点

收到反馈先别动手。让对方给出时间点、参考曲和一句期望：第四十八秒的副歌不够开，参考是某首歌的副歌，希望人声更靠前。三样齐了，问题才能定位。如果对方只说“再高级一点”，就放两版对照让他选，一版加宽，一版加动态，选完再动手。文字、语音、截图都能用，但最后要落到一份共享修改单上，标序号、时间点、优先级和负责人。

| 客户原话 | 可能在说什么 | 可执行的改法 |
|---|---|---|
| 太满 | 中频堆叠，层次不清 | 删一层，或让主奏让出中频 |
| 不够高级 | 动态平，音色薄 | 加段落落差，换更有质感的音色 |
| 人声听不清 | 齿音、掩蔽、电平 | 先查 2 到 4 kHz 的掩蔽，再动人声 |
| 结尾怪 | 尾巴被切或淡出太短 | 补混响尾，重做淡出 |
| 跟参考不像 | 低频或空间不同 | 对齐响度后比低频与混响时间 |

## 改：一轮只动一类

修改单按类型分组：结构、编曲、音色、电平、效果。一轮只处理一组，其余冻结。这样下一轮听到的差异才可归因，也不会出现“改了人声结果鼓也变了”的争论。每轮开始前存快照，命名写清轮次与日期；每轮结束导出一份对照版，保留上一版。客户临时加的需求记进下一轮，不插队，否则永远收不了尾。

## 验收：三条同时满足

验收不看客户语气，看三条：修改单上的条目逐条关闭；与上一版在同等响度下 A/B，确认只改了约定部分；按最初的 brief 与交付规格再听一遍，没有被修改带偏。三条都过才签字。签完再提的新意见算新一轮，重新报价或排期。这是职业边界，不是不近人情。

## 停：范围写不清就会无限改

无限轮次的根源通常不是客户难缠，而是范围没写清：包含几轮、每轮改什么、超出怎么计费。遇到反复推翻已验收部分，或每轮都换参考的情况，停下来重确认 brief，比继续改更省时间。反馈轮次管的是流程，管不了品味；双方对“好”的定义不同时，先对齐参考，再谈修改。还有一种失败是照单全收：客户要加的东西互相打架，最后谁都不满意，这时该拿回判断，说明代价，而不是把每条意见都做一遍。

```audiolab
{"type":"instrument","gm":"Electric Piano 1","synth":"struck","phrase":["E4","G4","B4","D5","B4","G4","E4"],"label":"两版之间只差一处","label_en":"One change between two versions","hint":"先听是不是只有一层变了，再决定要不要继续改","hint_en":"Check whether only one layer moved before opening another round"}
```
:::

::: en
When a client says it feels wrong and you ask what feels wrong, that round is already wasted. A feedback round turns a feeling into a timecode, a category and an acceptance test, then changes things in batches instead of chatting through each tweak.

## Collect: anchor the feeling to a timecode

Do not touch the session when the notes arrive. Ask for a timecode, a reference and one sentence of intent: the chorus at 0:48 does not open up, the reference is a particular song's chorus, the vocal should sit further forward. With those three, the problem can be located. If the note is only 'make it more premium', send two versions, one wider and one more dynamic, and let the client choose before you edit. Text, voice notes and screenshots all work, but everything ends on one shared revision sheet with numbers, timecodes, priority and owner.

| What the client says | What it may mean | An actionable change |
|---|---|---|
| Too full | Midrange stacking, unclear layers | Remove a layer or clear the lead's midrange |
| Not premium enough | Flat dynamics, thin tone | Add section contrast, choose a richer sound |
| Vocal unclear | Sibilance, masking, level | Check masking around 2 to 4 kHz first |
| The ending is odd | Tail cut or fade too short | Restore the reverb tail, redo the fade |
| Does not match the reference | Different low end or space | Match loudness, then compare both |

## Change: one category per round

Group the sheet by type: structure, arrangement, timbre, level, effects. Handle one group per round and freeze the rest. Only then can the next listen be attributed, and nobody argues that changing the vocal also moved the drums. Save a snapshot before each round with the round number and date, and export a comparison version at the end while keeping the previous one. New requests go to the next round rather than jumping the queue, or the work never closes.

## Accept: three conditions at once

Acceptance is not about the client's tone of voice but three conditions: every item on the sheet is closed; an A/B against the previous version at matched loudness shows only the agreed changes; and a final listen against the original brief and delivery spec shows nothing drifted. Sign only when all three hold. Anything raised after sign-off is a new round with new scheduling or a new fee. That is a professional boundary, not unfriendliness.

## Stop: unclear scope means endless rounds

Endless rounds usually come from an unclear scope rather than a difficult client: how many rounds, what each covers, what happens beyond them. When approved parts get reopened or the reference changes every round, pause and reconfirm the brief; that saves more time than another edit. Feedback rounds govern process, not taste. When the two sides define good differently, align on references before discussing changes. The other failure is accepting everything: requests that contradict each other leave nobody satisfied, and the right move is to state the trade-off rather than implement every note.

```audiolab
{"type": "instrument", "gm": "Electric Piano 1", "synth": "struck", "phrase": ["E4", "G4", "B4", "D5", "B4", "G4", "E4"], "label": "One change between two versions", "label_en": "One change between two versions", "hint": "Check whether only one layer moved before opening another round", "hint_en": "Check whether only one layer moved before opening another round"}
```
:::
