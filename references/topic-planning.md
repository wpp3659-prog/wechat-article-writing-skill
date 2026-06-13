# Topic Planning

Use this reference when the user asks for topic ideas, topic angles, content planning, account positioning, content pillars, outlines, or whether a public-account topic is worth writing.

## Core Principle

Plan topics from the relationship between reader, problem, benefit, and timing. Do not bind the skill to a single industry.

Use this formula:

```text
domain + target reader + concrete problem + emotion or benefit + distinct judgment = topic angle
```

Examples:

- Weak: AI tools
- Strong: 普通人别再收藏 AI 工具清单了，真正拉开差距的是工作流
- Weak: 职场成长
- Strong: 为什么越努力的人，越容易在职场里失去方向感
- Weak: 家庭教育
- Strong: 孩子不自律，很多时候不是懒，而是目标太抽象

## Input Routing

If the user gives only a domain:

1. Infer likely audience groups.
2. Generate content pillars.
3. Produce 10-20 candidate topics across different angles.
4. Rank the top 3.

If the user gives a rough idea:

1. Identify the hidden reader pain or benefit.
2. Rewrite it into 5-8 sharper topic angles.
3. Recommend the strongest one and explain why.

If the user gives source material:

1. Extract claims, scenes, conflict, useful facts, and emotional signals.
2. Convert them into candidate topics.
3. Mark which topics need more evidence before writing.

If the user asks "what should I write now":

1. Ask for or infer account position and reader.
2. If current popularity matters, run Heat Check Mode.
3. Recommend topics that balance heat, account fit, and content vacancy.

If the user has not selected a domain or reader:

- Prefer inferring from the request and material.
- Ask one concise clarification only when the output would otherwise be generic.

## Angle Library

Generate candidate topics from multiple sources. Avoid producing ten titles that are only wording variants of the same angle.

### Audience Angle

Use when the account serves a specific group.

- 新手, 普通人, 职场人, 创业者, 老板, 管理者, 宝妈, 学生, 自由职业者, 中年人, 内容创作者, 产品经理, 销售, 教师, 家长.

Prompt shape:

```text
对[人群]来说，[领域变化]真正影响的不是[A]，而是[B]
```

### Pain Point Angle

Use when the reader has anxiety, confusion, friction, or repeated failure.

- 焦虑, 迷茫, 低效, 不会选, 没结果, 怕落后, 没资源, 没人带, 踩坑, 成本高, 难坚持.

Prompt shape:

```text
你在[事情]上卡住，不是因为[表面原因]，而是因为[真实问题]
```

### Benefit Angle

Use when the article can promise a concrete gain.

- 赚钱, 省钱, 省时间, 提升竞争力, 降低风险, 改善关系, 提高效率, 增强判断力, 抓住机会.

Prompt shape:

```text
想在[场景]里获得[收益]，先学会判断这[数量]件事
```

### Scenario Angle

Use when the value appears in a recognizable life or work situation.

- 上班, 带团队, 创业, 转行, 育儿, 学习, 买课, 做副业, 做账号, 谈合作, 求职, 管钱, 做决策.

Prompt shape:

```text
当你在[场景]遇到[问题]，真正有效的不是[A]，而是[B]
```

### Trend Angle

Use when recent change matters.

- 新技术, 新政策, 平台规则, 消费变化, 行业洗牌, 职业变化, 用户习惯变化, 资本变化.

Prompt shape:

```text
[趋势]正在改变[人群]的[关键决策]，但多数人还在用旧方法
```

Run Heat Check Mode when the trend is current or the user asks whether it is hot.

### Counterintuitive Angle

Use when the topic needs stronger opinion and shareability.

Prompt shape:

```text
大家都以为[A]，但真正重要的是[B]
```

This angle works best when the article can prove the claim with examples, logic, or data.

### Misconception Or Pitfall Angle

Use when readers are likely wasting effort or making a common mistake.

Prompt shape:

```text
很多人做不好[事情]，不是因为不努力，而是一开始就选错了[关键变量]
```

### Method Angle

Use when the user wants practical value.

Prompt shape:

```text
把[复杂问题]拆成[数量]步，[人群]也能开始行动
```

### Case Or Story Angle

Use when the material contains people, companies, events, or turning points.

Prompt shape:

```text
从[案例]看懂：[领域]里最容易被忽略的[判断]
```

Do not invent cases. Use user-provided cases or well-sourced public cases.

### Controversy Angle

Use when public discussion has real disagreement.

Prompt shape:

```text
[争议问题]，我的判断是：[明确立场]
```

Avoid empty provocation. A controversy angle must still deliver evidence, reasoning, or a useful decision frame.

### Series Angle

Use when the account needs a content plan, not one article.

Create a series by audience stage, problem stage, decision stage, case type, or method layer.

Example:

```text
AI 普通人系列：
1. 工具不是关键，工作流才是关键
2. 不要学提示词，先学任务拆解
3. 普通人最适合用 AI 做的 5 类小生意
```

## Domain Weighting

Use the same planning method across domains, but adjust the scoring emphasis.

- AI, technology, business, finance: prioritize trend, evidence, judgment, and decision value.
- Workplace, growth, education: prioritize pain point, scenario, method, and reader relevance.
- Emotion, family, relationships: prioritize resonance, concrete scenes, emotional truth, and non-generic insight.
- Product, service, course, consulting: prioritize pain, conversion path, proof, objection handling, and trust.
- Culture, lifestyle, personal IP: prioritize distinctive voice, story, perspective, and long-term series potential.
- Knowledge popularization: prioritize clarity, accuracy, examples, and explanation structure.
- Local life, stores, venues: prioritize immediacy, concrete detail, audience need, and practical decision value.

## Topic Pool Output

When building a topic pool, include enough variety for the user to choose.

Recommended format:

```markdown
## 账号/赛道判断
- 目标读者：
- 内容支柱：
- 当前更适合的方向：

## 候选选题池
| # | 选题 | 角度来源 | 适合读者 | 推荐理由 |
|---|---|---|---|---|

## Top 3 推荐选题
1. 选题：
   - 推荐理由：
   - 适合写法：
   - 风险：

## 推荐主选题
- 主选题：
- 核心判断：
- 读者为什么会点开：
- 读者看完能带走什么：

## 文章大纲
1. 开头钩子：
2. 第一部分：
3. 第二部分：
4. 第三部分：
5. 结尾：

## 下一步建议
建议先确认这个选题，再进入完整写作。
```

## Topic Quality Rules

A strong topic should have:

- A clear reader.
- A specific problem or desire.
- A point of view, not only a category.
- A reason to read now.
- Enough evidence, examples, or experience to support the article.
- A WeChat-friendly article shape.
- A title that can be concrete without becoming clickbait.

Avoid:

- Generic categories such as "AI 发展趋势", "如何成长", "亲子教育思考".
- Pure keyword stacking.
- Topics that are hot but unrelated to the account.
- Topics that require facts the writer cannot verify.
- Angles that only work as short-video hooks but cannot support a long article.
- Moralizing topics with no practical or emotional payoff.
