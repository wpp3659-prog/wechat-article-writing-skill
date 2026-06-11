# WeChat Article Writing Skill

一个专门用于中文微信公众号文章写作的 Codex Skill。

它只负责写作与编辑，不负责微信公众号发布、草稿箱上传、图片生成或 API 调用。

## 能做什么

- 根据一个主题生成完整公众号文章
- 控制文章字数
- 自动判断文章结构
- 自动选择公众号表达风格
- 生成标题、摘要、金句、留言引导
- 做 100 分质量自检
- 做 AI 痕迹审稿
- 降低“下一句过于可预测”的生成式写作问题

## 适合场景

- 公众号长文
- 微信推文正文
- 自媒体观点文
- AI / 商业 / 职场 / 成长 / 产品类文章
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

直接在 Codex 里说：

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

## 输出内容

默认输出：

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
