<div align="center">

# 🧠 大模型进化史

### LLM Evolution Timeline

*从 GPT-1 到多模态时代，国内外主流大模型的发展轨迹*

[![GitHub Stars](https://img.shields.io/github/stars/LLing486/llm-evolution?style=flat&logo=github&color=yellow)](https://github.com/LLing486/llm-evolution)
[![License](https://img.shields.io/github/license/LLing486/llm-evolution?style=flat)](LICENSE)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Glossary/HTML5)

**🌐 [在线预览](https://lling486.github.io/llm-evolution/)** → 打开即用，零依赖

[🧭 关键节点编年史](https://lling486.github.io/llm-evolution/milestones.html) · [📊 参数规模趋势](https://lling486.github.io/llm-evolution/chart.html)

</div>

---

## ✨ 项目简介

这是一个**交互式大模型进化时间轴**，覆盖 2018-2026 年全球主要 AI 公司的大语言模型发展脉络。

### 特性

- 🎯 **216 个模型** — 覆盖 30 家公司/团队的代表性大模型
- 🌍 **全球视野** — 🇺🇸 美国 / 🇨🇳 中国 / 🇪🇺 欧洲，国内外模型对比
- 🔍 **交互筛选** — 按地区、公司、开源/闭源、模态自由过滤
- 📅 **时间刻度** — 年份 + 季度细线 + 「今天」参考线，能看出同一个模型谁先谁后
- 🏷️ **标签自动避让** — 密集处的模型名自动分层排布，空间实在不够时折叠为 +N（悬停圆点看详情）
- 💡 **悬停详情** — 发布时间、参数规模、能力标签一目了然
- 🏆 **旗舰标记** — 粉色圆点标识各公司旗舰模型
- 📱 **响应式设计** — 桌面端、移动端均可浏览
- 🧭 **关键节点编年史** — 独立页面 [milestones.html](milestones.html)：2017–2026 的 28 个转折点，模型、产品、协议、事件混排，每条都写清「为什么是节点」和「改变了什么」
- 🚀 **零依赖** — 无框架、无构建工具，纯 HTML/CSS/JS

## 📊 覆盖公司

| 地区 | 公司 |
|:---:|------|
| 🇺🇸 美国 | OpenAI · Google · Anthropic · Meta · xAI · Microsoft · Amazon · Cohere · Thinking Machines |
| 🇪🇺 欧洲 | Mistral AI |
| 🇨🇳 中国 | DeepSeek · 阿里巴巴 · 百度 · 字节跳动 · 智谱AI · 零一万物 · 小米 · 月之暗面 · 百川智能 · 面壁智能 · MiniMax · 腾讯 · 阶跃星辰 · 蚂蚁百灵 |
| 🌐 其他 | Sarvam AI · BharatGen · Apodex |

## 🚀 快速开始

### 方式一：本地起一个静态服务器

页面通过 `fetch` 读取 `data/*.json`，所以需要走 HTTP（直接双击 `index.html` 会被浏览器的同源策略拦住，读不到数据）。

```bash
git clone https://github.com/LLing486/llm-evolution.git
cd llm-evolution

python3 -m http.server 8000
# 然后打开 http://localhost:8000/
```

### 方式二：GitHub Pages

访问 **https://lling486.github.io/llm-evolution/** 即可在线体验。

## 🏗️ 技术栈

- **HTML5** + **CSS3** + **Vanilla JavaScript**
- 暗色主题，CSS Grid/Flexbox 布局
- **数据层分离**：模型数据存放在 `data/models.json`，便于社区贡献
- 无任何外部依赖（Google Fonts 为可选增强）

## 📁 项目结构

```
llm-evolution/
├── index.html                    # 主页面（时间轴渲染引擎）
├── milestones.html               # 关键节点编年史
├── chart.html                    # 参数规模趋势图
├── data/
│   ├── models.json               # 模型数据（主时间线数据源）
│   ├── milestones.json           # 关键节点数据（含阶段划分、来源链接）
│   └── companies.json            # 公司配置
├── .github/
│   ├── workflows/
│   │   └── validate-data.yml     # CI：PR 时自动校验数据完整性
│   ├── ISSUE_TEMPLATE/
│   │   └── add-model.yml         # 添加模型的标准模板
│   └── scripts/
│       └── validate-data.js      # 数据校验脚本
├── ROADMAP.md                    # 改进计划
├── README.md
└── LICENSE
```

### 如何添加新模型

1. 编辑 `data/models.json`，按格式添加新模型条目
2. 如需添加新公司，同步编辑 `data/companies.json`
3. 提交 PR → CI 自动校验 → Review → Merge
4. GitHub Pages 自动部署 🚀

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

1. Fork 本仓库
2. 创建你的分支 (`git checkout -b feature/amazing-feature`)
3. 提交更改 (`git commit -m 'Add some amazing feature'`)
4. 推送到分支 (`git push origin feature/amazing-feature`)
5. 打开一个 Pull Request

## 📝 数据来源

模型数据基于公开资料整理，包括：

- 各公司官方博客和发布会
- arXiv 论文
- 权威科技媒体报道

> ⚠️ 部分模型参数规模未公开，标注为"未公开"。如有错误，欢迎 PR 修正。

## 📄 License

[MIT](LICENSE)

---

<div align="center">

*Built with ❤️ by [LLing486](https://github.com/LLing486)*

</div>
