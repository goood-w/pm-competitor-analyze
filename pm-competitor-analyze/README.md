# pm-competitor-analyze

面向产品经理日常决策的竞品分析 Skill。它优先服务模块改版、PRD 证据补充、页面/流程拆解和专项能力对比，而不是默认生成大而全的行业报告。

## 适用场景

- 已有我方 PRD、方案、页面或产品想法，需要找竞品证据辅助判断。
- 想对比某个专项能力，例如智能排班、简历优化、课程评估、付费转化。
- 想拆解一个竞品页面、注册流、购买页或 AI 生成流程。
- 想学习一个标杆产品的单个机制，而不是写全景公司分析。
- 明确需要市场进入、战略扫描或商业模式对标。

不适合：无目标罗列功能清单、只凭截图断言完整产品能力、把竞品做法直接当作需求。

## 设计依据

方法来源沉淀在 [references/source-analysis-and-design.md](./references/source-analysis-and-design.md)：

- 《如何用 Skill 做竞品调研？》：提供主流程，以我方 PRD/问题为锚点，使用用户手册、更新日志等高质量材料做专项分析。
- 《原来优秀的产品经理都是这么写竞品分析文档的》：提供完整竞品分析文档骨架。
- 《AI 做竞品分析实战：输出深度洞察，效率飙升 80%》：提供页面/流程拆解方法。
- `yuanzheng10/competitive-analysis`：提供 10 大维度和市场/战略扫描框架。

## 目录结构

```text
pm-competitor-analyze/
├── SKILL.md
├── README.md
├── CHANGELOG.md
├── agents/
│   └── openai.yaml
└── references/
    ├── source-analysis-and-design.md
    ├── evidence-rules.md
    └── report-templates.md
```

## 本地安装

把本目录复制到 Codex Skills 目录：

```bash
mkdir -p ~/.codex/skills
cp -R pm-competitor-analyze ~/.codex/skills/
```

如果使用发布包：

```bash
mkdir -p ~/.codex/skills
ditto -x -k dist/pm-competitor-analyze.skill ~/.codex/skills
```

安装后可以在新对话中直接说：

```text
请用 $pm-competitor-analyze，基于我的 PRD 和这几个竞品用户手册，分析“简历优化前是否需要先展示评分与差距”。
```

## 使用建议

最好同时提供：

- 我方产品、PRD、页面或当前假设。
- 本次要回答的产品决策问题。
- 竞品名称、链接、截图、用户手册、更新日志或价格页。
- 地区、端、账号类型、版本、付费层级等体验条件。

输出默认是 Markdown 文档，适合复制到飞书、Notion、PRD 附录或汇报材料。

## 发布包

`dist/pm-competitor-analyze.skill` 是可分发压缩包，包含运行所需的 Skill 源码、说明和参考文件。`dist/SHA256SUMS` 用于校验文件完整性。
