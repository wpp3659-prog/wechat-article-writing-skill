# AI-Trace Review

Use this file to reduce generic AI-writing signals and improve authentic editorial texture. This is not a promise to bypass any detector. Treat it as a quality gate for originality, human rhythm, and trustworthy authorship.

Public descriptions of Zhuque-like Chinese AIGC detectors emphasize comparing AI-generated content with human writing patterns and model-specific generation features. Assume detection may use multiple signals at once: statistical rhythm, repeated syntax, semantic smoothness, generic phrasing, and lack of grounded detail.

For next-sentence predictability, also read `next-sentence-predictability.md`.

## Review Levels

Classify the draft:

- Low risk: natural rhythm, concrete detail, clear stance, no obvious template language.
- Medium risk: readable but too smooth, too balanced, or too evenly structured.
- High risk: generic AI tone, repeated sentence structures, broad claims, fake specificity, or obvious transition templates.

High risk is not publish-ready.

## High-Risk Signals

## 1. Rhythm Is Too Even

Signals:

- Many sentences have similar length.
- Paragraphs are all 2-3 sentences with the same cadence.
- Each H2 follows "观点 -> 解释 -> 小结".

Revision:

- Mix one-line paragraphs with denser paragraphs.
- Break one polished paragraph into a short sentence plus a longer explanation.
- Use one hard turn without a transition when natural.
- Avoid making every section end with a neat summary.

## 1b. Next Sentence Is Too Predictable

Signals:

- After reading one sentence, the next sentence is the most obvious continuation.
- Paragraphs advance in a fully linear chain with no human pause, correction, scene, or turn.
- The article repeatedly uses "X 正在改变 Y -> 这带来机遇和挑战 -> 我们需要主动适应" style logic.

Revision:

- Read `next-sentence-predictability.md`.
- Add a concrete scene, doubt, objection, short interruption, or angle shift every 400-600 Chinese characters.
- Do not add random noise. The turn must clarify the author's thinking or make the point more memorable.

## 2. Language Is Too Template-Like

Signals:

- Repeated connectors: "首先", "其次", "此外", "最后", "综上".
- Generic claims: "具有重要意义", "带来深远影响", "值得关注".
- Every paragraph sounds equally calm and polished.

Revision:

- Replace connectors with direct movement: "问题来了", "更麻烦的是", "说白了".
- Cut empty evaluative phrases.
- Add a sharper judgment or a concrete boundary.

## 3. Content Lacks Grounding

Signals:

- Big claims without examples.
- "很多人", "某些公司", "不少案例" with no support.
- Advice that sounds correct but cannot be pictured.

Revision:

- Add a concrete scene, workflow, role, or decision.
- Use sourced facts when factual claims matter.
- If no real case exists, mark a replaceable editor note instead of inventing.

Example:

```markdown
<!-- 编辑建议：这里换成你公司或行业里真实发生过的一次流程变化。 -->
```

## 4. Emotion Is Too Neutral

Signals:

- The article never shows doubt, frustration, surprise, pressure, or preference.
- Every viewpoint is perfectly balanced.
- The ending refuses to take a stance.

Revision:

- Add one honest tension: concern, annoyance, uncertainty, or relief.
- State what the author thinks readers should stop doing.
- Keep nuance, but do not hide behind "各有利弊".

## 5. Specificity Is Fake

Signals:

- Specific dates, numbers, names, or personal stories appear without source or user input.
- The article says "我有个朋友" when no such story was provided.

Revision:

- Remove unsupported specifics.
- Turn them into hypothetical scenes.
- Ask for user material only if the missing detail is essential.

## 6. Section Templates Repeat

Signals:

- Every H2 starts with a definition.
- Every section ends with a slogan.
- Bullets appear in the same shape repeatedly.

Revision:

- Vary section openings: scene, question, claim, contrast, example.
- Let one section be mostly narrative and another mostly analytical.
- Use bullets only when they truly help scanning.

## Final AI-Trace Pass

Before final output, answer:

- Does the first screen feel written by a person with a stance?
- Can a reader picture at least 3 concrete moments or use cases?
- Are there unsupported "real" details? If yes, remove or mark them.
- Would two adjacent sections still make sense if one transition sentence were removed? If yes, the structure may be too smooth; add a more human turn.
- Is the final paragraph natural, or does it sound like a generated conclusion?

If two or more answers are weak, revise before scoring.
