# WeChat Article Writing Skill

一个专门用于中文微信公众号选题策划、大纲规划和文章写作的 Codex Skill。

它只负责内容策划、写作与编辑，不负责微信公众号发布、草稿箱上传、图片生成、爬虫开发、平台自动化或 API 调用。

## 可视化页面

本仓库包含一个静态 HTML 介绍页：

```text
docs/index.html
```

本地打开即可预览，也可以在 GitHub Pages 中选择 `main` 分支的 `/docs` 目录发布为网页。

## 能做什么

- 根据任意赛道生成公众号选题池
- 从粗想法、热点、素材里提炼选题角度
- 判断选题是否适合当下追热点
- 对候选选题做 100 分评分与 Top 3 推荐
- 输出推荐选题、写作角度、大纲和标题方向
- 根据一个主题生成完整公众号文章
- 控制文章字数
- 自动判断文章结构
- 自动选择公众号表达风格
- 生成标题、摘要、金句、留言引导
- 做 100 分质量自检
- 做 AI 痕迹审稿
- 降低“下一句过于可预测”的生成式写作问题

## 适合场景

- 公众号选题策划
- 热点选题判断
- 账号内容支柱规划
- 公众号文章大纲
- 公众号长文
- 微信推文正文
- 自媒体观点文
- AI / 商业 / 职场 / 成长 / 教育 / 情感 / 产品 / 服务 / 个人 IP 等赛道
- 文章润色、扩写、改写

## 安装

把本仓库克隆到 Codex skills 目录：

```powershell
git clone https://github.com/<your-name>/wechat-article-writing-skill.git "$env:USERPROFILE\.codex\skills\wechat-article-writing"
```

或者手动复制本仓库目录到：

```text
C:\Users\<you>\.codex\skills\wechat-article-writing
```

macOS / Linux:

```bash
git clone https://github.com/<your-name>/wechat-article-writing-skill.git ~/.codex/skills/wechat-article-writing
```

## 使用

做选题策划：

```text
$wechat-article-writing 我做职场成长公众号，帮我策划 15 个选题，并推荐最值得写的 3 个
```

判断热点能不能写：

```text
$wechat-article-writing 最近 AI 智能体很热，帮我判断这个话题适不适合公众号追，并给出写作角度
```

从选题进入正文：

```text
$wechat-article-writing 写一篇公众号文章，主题是：AI 时代普通人怎么保住竞争力，字数 1800 字
```

也可以指定风格：

```text
$wechat-article-writing 写一篇公众号文章
主题：2026 年下半年 AI 趋势预测
字数：1500 字
风格：理性分析型
```

## 支持的表达风格

- 理性分析型
- 口语陪伴型
- 犀利观点型
- 故事叙事型
- 干货方法型
- 品牌转化型
- 深度随笔型

## 选题能力

选题模块不绑定具体赛道，而是从读者、痛点、利益、场景、趋势、反常识、误区避坑、方法论、案例故事、争议观点和系列潜力中生成角度。

默认输出：

- 账号/赛道判断
- 候选选题池
- Top 3 推荐选题
- 推荐主选题
- 写作角度
- 文章大纲
- 标题方向
- 风险与补充材料
- 下一步建议

当用户要求判断“当下热门”“热搜”“近期趋势”时，会使用公开信息做热度验证，并给出热度评分、依据、内容空位和是否建议追热点。

## 输出内容

完整文章默认输出：

- 标题
- 摘要
- 正文
- 备选标题
- 金句
- 留言引导
- 质量自检

## 说明

AI 痕迹审稿用于提升文章原创质感和真人编辑感，不承诺绕过任何检测器。

## License

MIT
