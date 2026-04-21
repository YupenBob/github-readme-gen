# GitHub README 高星项目模式研究

> 基于 13 个 10k+ stars 真实项目的 README 分析总结

---

## 一、必备结构（按重要性排序）

1. **Logo/Banner** — 项目标志，视觉第一眼
2. **徽章行** — CI/License/版本/Stars（3-6个精选）
3. **一句话简介** — 30秒内让读者知道这是什么
4. **特性列表** — 3-5个核心卖点
5. **快速开始** — 在线地址 + 最少使用命令
6. **目录/导航** — 大项目必备
7. **贡献指南** — 链接到 CONTRIBUTING.md
8. **License** — 底部，附年份+作者

---

## 二、徽章选择规则

| 类型 | 徽章 | 何时用 |
|------|------|--------|
| 社区 | GitHub Stars | 几乎所有项目 |
| 协议 | License | 几乎所有项目 |
| 状态 | CI/Build | 框架/库/工具类 |
| 版本 | npm/pypi version | 有包管理的项目 |
| 平台 | Website | 有独立域名的项目 |
| 社区 | Discord/Chat | 教育型/社区型 |
| 翻译 | Translations | 国际化项目 |

**原则：** 精选3-6个，太多=噪音。资源列表类项目几乎不用徽章。

---

## 三、四种项目类型写法

### 类型1：框架/库型（vue, react, TheAlgorithms）
```
Logo → 徽章行 → 一句话简介 → Ecosystem表格 → Docs链接 → Contributing → License
```
风格：冷静克制，能力描述为主

### 类型2：教育/学习型（freeCodeCamp, system-design-primer）
```
Banner图 → 动机故事 → Why三个问题 → 目录 → 详细正文 → 贡献 → License
```
风格：有温度，个人叙事，多语言翻译

### 类型3：资源集合型（awesome, public-apis）
```
Logo → 一句话 → 分类目录 → 高密度列表内容
```
风格：极度简洁，无情感，分类清晰统一

### 类型4：工具/命令型（build-your-own-x）
```
Banner → Feynman引言 → 分类目录 → 贡献 → License
```
风格：使命感驱动，金句开篇

---

## 四、CloverTools 类工具站最佳实践

参考 `freeCodeCamp` + `awesome` 混合模式：

```
Banner/Logo → 徽章行 → 一句话简介 → 特性列表 → 工具分类表格
→ 快速开始（在线地址）→ 贡献指南 → License
```

**工具分类表格模板：**
```markdown
| 分类 | 工具数 | 代表工具 |
|------|-------|---------|
| 格式转换 | 45+ | JSON格式化、Base64、URL编码 |
| 开发工具 | 80+ | 正则测试、颜色转换、Cron生成 |
```

---

## 五、徽章获取地址

```markdown
[![GitHub stars](https://img.shields.io/github/stars/YupenBob/clover-tools)](https://github.com/YupenBob/clover-tools)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Website](https://img.shields.io/website?url=https://tools.xsanye.cn)](https://tools.xsanye.cn)
[![Build](https://github.com/YupenBob/clover-tools/workflows/Deploy/badge.svg)](https://github.com/YupenBob/clover-tools/actions)
```

---

## 六、不要犯的错误

- ❌ 没有任何简介开头（学 awesome 无简介的写法，但你没有足够的内容密度支撑）
- ❌ 没有 License
- ❌ 徽章超过6个
- ❌ 使用过于复杂的 CI 徽章（先有 CI 才能用）
- ❌ README 里塞满代码（那是 docs/ 的职责）
- ❌ 中英文混杂（要么全中文要么全英文）
