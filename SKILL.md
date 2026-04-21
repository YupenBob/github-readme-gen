---
name: github-readme-gen
description: Generate or improve GitHub README.md for open source projects. Use when user asks to "优化README", "生成README", "写一个README", "improve README", "create README for repo", or when working on GitHub repo documentation. Analyzes project type and applies appropriate pattern from high-star project research.
---

# GitHub README Generator

## Quick Start

1. Read `references/patterns.md` for the research findings on high-star READMEs
2. Read `assets/template.md` for the reusable template
3. Ask user about their project:
   - Project name, GitHub URL, website URL
   - Project type (framework/tool/education/resource-collection)
   - Key features (3-5 bullets)
   - Tools/categories count if it's a toolbox

## Workflow

### Step 1: Identify Project Type

From `references/patterns.md`:

- **框架/库型** → 徽章多，冷静克制，Ecosystem表格
- **教育/学习型** → 故事开头，多语言，动机Why
- **资源集合型** → 高密度分类列表，无情感
- **工具/命令型** → 金句开篇，使用命令展示
- **工具站型（如CloverTools）** → freeCodeCamp+awesome混合，分类表格

### Step 2: Apply Template

Read `assets/template.md` and fill in placeholders:

```
{{PROJECT_NAME}}      → 项目名称
{{BANNER_OR_LOGO}}    → Banner图片或Logo（可选）
{{USER}}/{{REPO}}      → GitHub用户名/仓库名
{{REPO_URL}}           → https://github.com/xxx/xxx
{{WEBSITE_URL}}        → 在线地址
{{ONE_LINE_TAGLINE}}  → 一句话描述（前缀 > ）
{{EXTENDED_DESCRIPTION}}→ 2-3句扩展描述（可选）
{{FEATURES_LIST}}      → Markdown无序列表，3-5条
{{QUICK_START_CODE_BLOCK}}→ 代码块展示快速使用
{{TOOLS_TABLE}}        → 分类表格（工具站类项目用）
{{LICENSE}}            → MIT / Apache-2.0 等
{{YEAR}}-{{END_YEAR}}  → 版权年份
{{AUTHOR}}             → 作者名
{{SPONSORS_OR_FOOTER}} → 赞助商/鸣谢（可选）
```

### Step 3: Add Badges

From `references/patterns.md` Section V, select 3-6 appropriate badges:

```markdown
[![GitHub stars](https://img.shields.io/github/stars/USER/REPO)](URL)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Website](https://img.shields.io/website?url=URL)](URL)
```

### Step 4: Output

Generate the complete README.md content and write it to the project directory.

## Special Cases

### 工具站/导航站（参考CloverTools模式）

Always include a tools classification table:

```markdown
## 📂 工具分类

| 分类 | 工具数 | 代表工具 |
|------|-------|---------|
| 格式转换 | 45+ | JSON格式化、Base64、URL编码 |
| 开发工具 | 80+ | 正则测试、颜色转换、Cron生成 |
```

### 已有README需要优化

1. Keep existing structure if it's working
2. Add missing elements from the checklist:
   - [ ] Logo/Banner
   - [ ] Badge row (3-6 badges)
   - [ ] One-line tagline (prefix `>`)
   - [ ] Features list (3-5 bullets)
   - [ ] Quick start section
   - [ ] Contributing link
   - [ ] License at bottom
3. Don't overhaul a working README, only fill gaps

## References

- Full patterns analysis: `references/patterns.md`
- Reusable template: `assets/template.md`
