# Quality Rubric

Score the article before final output. The article is publish-ready only when total score is at least 90/100, no hard-fail item exists, and AI-trace risk is not high.

## Score Breakdown

## 1. Topic Fit: 15

- 0-5: Topic is only loosely related.
- 6-10: Topic is clear but angle is ordinary.
- 11-15: Topic, reader, and angle are sharply aligned.

Check:

- Does the article answer the user's actual theme?
- Is the reader clear?
- Does the article have one core point?

## 2. Opening Hook: 15

- 0-5: Generic background opening.
- 6-10: Clear but not especially compelling.
- 11-15: Creates pain, conflict, curiosity, scene, or promise in the first 3 sentences.

## 3. Structure: 15

- 0-5: Loose sections or repeated points.
- 6-10: Logical but somewhat mechanical.
- 11-15: Each section advances the argument with natural transitions.

## 4. Content Value: 20

- 0-7: Mostly empty claims.
- 8-14: Useful but not concrete enough.
- 15-20: Specific, useful, memorable, and actionable or insightful.

Check:

- Are there examples, scenarios, methods, comparisons, or judgments?
- Does each H2 give the reader something to take away?
- Are unsupported claims removed or softened?

## 5. WeChat Reading Feel: 15

- 0-5: Sounds like generic AI prose.
- 6-10: Readable but still polished in a template-like way.
- 11-15: Human rhythm, phone-friendly paragraphs, clear voice, natural emotional texture.

## 6. Title And Summary: 10

- 0-3: Title is flat, misleading, or too broad.
- 4-7: Title and summary are accurate but not strong.
- 8-10: Title creates click interest while staying honest; summary states value within 80 Chinese characters.

## 7. Ending And Interaction: 10

- 0-3: Stiff summary or no ending.
- 4-7: Decent ending but weak interaction.
- 8-10: Natural close plus a relevant comment/share prompt.

## Hard-Fail Items

Any hard-fail item means the article is not publish-ready regardless of score:

- It deviates from the user's topic.
- Word count misses the requested target by more than 10%.
- It invents data, names, quotes, cases, dates, or sources.
- It uses obvious AI template language.
- Sentence flow remains highly predictable after one revision pass.
- It has no clear viewpoint.
- The title overpromises or does not match the body.
- Paragraphs are too long for mobile reading.
- The ending uses stiff summary language such as "综上所述" or "总而言之".
- Recent or factual claims were needed but not verified.
- AI-trace review is high risk after the first revision pass.

## Revision Rule

If score is below 90:

1. Identify the lowest-scoring 2 dimensions.
2. Also check `ai-detection-review.md` for AI-like rhythm or generic texture.
3. Re-score.
4. Run at most 2 revision loops before final output.

Do not show failed drafts unless the user asks.
