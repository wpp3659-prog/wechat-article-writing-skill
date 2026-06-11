---
name: wechat-article-writing
description: Writes complete Chinese WeChat Official Account articles from a topic, opinion, outline, note, draft, or source material. Use when the user asks to write, draft, expand, polish, rewrite, or generate a 公众号文章, 微信公众号推文, 微信文章, 推文正文, 自媒体长文, or public-account article. Supports controllable word count, reader positioning, article structure selection, title generation, human-like Chinese prose, quality scoring, and revision until publish-ready. This skill only handles writing and editing, not publishing, API upload, image generation, or WeChat draft submission.
---

# WeChat Article Writing

Write complete Chinese WeChat Official Account articles from the user's topic, idea, outline, draft, or source material. Focus on article quality only. Do not publish, upload, generate images, or call WeChat APIs.

## Operating Mode

Produce a complete article in one pass when the user gives a usable topic. Ask at most one clarification when the topic is too vague to write responsibly, such as "写一篇公众号文章" with no domain, angle, reader, or material.

Infer reasonable defaults instead of asking setup questions:

- `target_reader`: infer from topic and wording.
- `purpose`: default to delivering value and encouraging reader engagement.
- `tone`: default to clear, warm, opinionated, and conversational.
- `expression_style`: infer from topic, article type, and user wording.
- `target_word_count`: default to normal length.
- `article_type`: infer from the topic.

If the user requests only a title, outline, rewrite, polish, shortening, or expansion, perform only that writing task.

## Word Count Control

Use Chinese character count as the practical target for Chinese articles.

- Exact count requested: stay within plus or minus 10%.
- Range requested: stay inside the range.
- "短文" or "简短": 800-1200 Chinese characters.
- "正常" or no length request: 1800-2200 Chinese characters.
- "长文", "深度", or "详细": 2500-4000 Chinese characters.
- Under 800 characters: write a compact public-account post, not a full long article.
- Over 4000 characters: briefly note that this is long for WeChat completion rate, then continue if the user explicitly requested it.

If the requested word count conflicts with the requested depth, prioritize the user's explicit word count.

## Source And Fact Rules

Use web search before writing when the article depends on recent facts, statistics, news, laws, prices, product releases, public events, or any claim likely to have changed. Use primary or reputable sources and integrate findings naturally.

For evergreen opinion, reflection, method, or user-provided material, write from the user's context and common knowledge.

Never invent specific data, named cases, expert quotes, research findings, dates, source attributions, or user experiences. If a useful concrete detail is missing, use a clearly framed hypothetical scenario or add an editor note for the user to replace with a real detail.

## Article Type Routing

Choose one primary article type. If needed, read `references/article-frameworks.md`.

- Opinion: strong viewpoint, argument, counterargument, reader reflection.
- Practical Guide: problem, method, steps, examples, takeaway.
- Story: scene, conflict, turning point, insight, resonance.
- Industry Analysis: event, background, trend, impact, judgment.
- Personal Reflection: experience, observation, lesson, emotional closure.
- Product or Service Article: pain point, scenario, solution, proof, call to action.
- List or Roundup: value promise, curated items, comparison, decision help.

If unsure, choose Opinion for abstract themes and Practical Guide for how-to themes.

## Expression Style Routing

Choose one primary expression style before drafting. If the user specifies a style, follow it. If not, infer a style from topic, reader, and article type. Read `references/expression-styles.md` when choosing or applying the style.

Available styles:

- Rational Analysis: technology, business, AI, industry trends, serious explainers.
- Conversational Companion: workplace, personal growth, life observation, emotional resonance.
- Sharp Opinion: commentary, controversial views, hot takes, counterintuitive claims.
- Story Narrative: people, cases, brand stories, personal experience.
- Practical Method: tutorials, checklists, frameworks, operational advice.
- Brand Conversion: product, service, course, consulting, business copy.
- Deep Essay: personal IP, cognition, long-termism, reflective themes.

Use at most one secondary style. Do not blend many styles into a vague "公众号腔".

## Writing Workflow

Complete this internal checklist before final output:

```text
Writing Progress:
- [ ] Step 1: Understand the topic, reader, purpose, tone, and length
- [ ] Step 2: Choose article type, structure, and expression style
- [ ] Step 3: Generate 3-5 title candidates
- [ ] Step 4: Pick the strongest title for the main article
- [ ] Step 5: Draft the complete article
- [ ] Step 6: Run AI-trace and human-authenticity review
- [ ] Step 7: Add summary, golden lines, and reader interaction prompt
- [ ] Step 8: Score with the quality gate
- [ ] Step 9: Revise until publish-ready or revision limit is reached
- [ ] Step 10: Output final article and concise quality report
```

## Writing Requirements

The article must feel like a human editor wrote it for a public account. Use Chinese unless the user asks otherwise.

Required:

- A strong opening hook in the first 3 sentences.
- A clear point of view, not a neutral encyclopedia entry.
- H2 sections that each advance the article.
- Short and medium paragraphs mixed for mobile reading.
- Concrete examples, scenarios, comparisons, methods, or judgments.
- At least 2 memorable lines.
- A natural ending, not a stiff summary.
- A reader interaction prompt.

Avoid:

- "首先", "其次", "最后", "总之", "综上所述", "总而言之".
- "在当今时代", "随着社会的发展", "值得注意的是", "不可否认".
- Empty motivational language.
- Overly balanced conclusions with no stance.
- Fake data, fake quotes, fake cases, or fake personal experience.
- Excessive bullet lists unless the article type needs them.

For stricter prose rules, read `references/writing-style.md`.

## AI-Trace Review

After drafting and before scoring, read `references/ai-detection-review.md` and run a dedicated AI-trace review. Treat this as an authenticity and editorial-quality check, not as a guarantee to bypass any detector.

Revise the article when it shows high-risk AI-like signals:

- overly even sentence and paragraph length
- mechanical "观点-解释-总结" section rhythm
- high next-sentence predictability, where each sentence follows the most obvious continuation
- broad claims without concrete scenes
- neutral, safe, over-balanced tone throughout
- repeated transition phrases or polished template language
- fake personal stories, fake examples, or unsupported specificity

Prefer adding user-replaceable editor notes over inventing personal experience.

## Quality Gate

Before final output, score the article using `references/quality-rubric.md`.

The article is publish-ready only when:

- Total score is at least 90/100.
- No hard-fail item is present.
- Word count is within the requested range or within plus or minus 10% of an exact requested count.
- AI-trace review is not high risk.

If the score is below 90 or a hard-fail item exists, revise the article before showing it. Run at most 2 revision loops. After 2 loops, output the best version and clearly mark the remaining weakness.

Do not inflate the score. Give 100/100 only when the article has a distinctive angle, strong opening, concrete value, natural human rhythm, strong title, and no obvious manual-editing gap.

## Output Format

For a full article request, output:

```markdown
# 标题

> 摘要：不超过 80 字，说明文章核心价值。

正文...

## 小标题一

正文...

## 小标题二

正文...

## 小标题三

正文...

结尾...

---

**备选标题**
1. ...
2. ...
3. ...

**金句**
- ...
- ...

**留言引导**
...

**质量自检**
- 预估字数：约 xxxx 字
- 质量评分：xx/100
- 达标状态：通过/未完全通过
- 仍建议人工补强：...
```

If the user asks for only the正文, title, outline, rewrite, polish, or review, omit unrelated sections.

## Reference Files

- `references/article-frameworks.md`: article structures and when to use them.
- `references/expression-styles.md`: public-account voice modes and style routing.
- `references/title-patterns.md`: title styles and selection rules.
- `references/writing-style.md`: public-account prose rules and anti-generic writing constraints.
- `references/ai-detection-review.md`: AI-trace review and human-authenticity revision rules.
- `references/next-sentence-predictability.md`: checks and revisions for overly predictable sentence flow.
- `references/quality-rubric.md`: 100-point scoring gate and hard-fail list.
- `references/review-checklist.md`: final checks for article readiness.
