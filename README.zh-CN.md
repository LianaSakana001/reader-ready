# reader-ready · 去除 AI 味

[English](README.md) · [中文 Skill](SKILL.zh-CN.md) · [English skill](SKILL.md)

让文字和成品适合实际阅读它们的人。处理无关的制作细节、助手旁观口吻、多余解释和模板化表达，保留作者原意与材料用途。

可在起草、修改和交付检查时使用，适用于申请材料、报告、文章、表格、PPT、讲稿、科研论文，以及含文字的 figure。

## 它会怎样处理

| 情况 | 编辑判断 |
| --- | --- |
| 图中有对理解没有帮助的内部项目名称 | 直接省略，无需补一个替代名称。 |
| 证明页说明截图如何拼接 | 保留证据和有用说明，删除制作过程叙述。 |
| 个人成果条目写“申请人为合作作者” | 按材料采用合适口吻，使用有依据的身份和贡献。 |
| PPT讲稿含本地图片路径 | 让讲稿服务于收件人，需要的制作记录放在适当位置。 |
| 论文反复声明“不能证明”原本就没有声称的内容 | 直接陈述有依据的结果，在需要的位置保留实质限定。 |
| 教程或复现交接确实需要路径 | 保留，按具体用途判断。 |

根据语境决定保留、改写、移出或删除。名称、代词、路径、被动句和标点都不是禁词。已经清楚的文字可以原样保留。

## 科研论文

中英文版均明确支持摘要、引言、方法、结果、讨论和图注的起草与修改。[科研写作参考](references/scientific-writing.zh-CN.md)覆盖：

- 保持正式、符合学科惯例的表达，统一术语，按需要使用被动句或第一人称。
- 围绕研究问题、关键发现及其意义组织有吸引力的论证。
- 直接、适度地表达主张，减少重复道歉、假想审稿人质疑和自动追加的免责声明。
- 保留准确统计、样本单位、引文和实质限定。科研故事的吸引力来自问题与发现，不要求文学化。

## 安装

通过社区 [Skills CLI](https://github.com/vercel-labs/skills) 安装，按提示选择使用的助手和安装范围：

```sh
npx skills add LianaSakana001/reader-ready --skill reader-ready
```

安装到用户范围，供 Codex 使用：

```sh
npx skills add LianaSakana001/reader-ready --skill reader-ready --agent codex --global
```

也可以把仓库复制到所用助手的技能目录下，文件夹命名为 `reader-ready`，保留 `SKILL.md`、`references/` 和 `agents/` 的相对位置。Codex 支持的目录见[官方技能文档](https://learn.chatgpt.com/docs/build-skills)。使用这些指令不需要安装 Python 包、配置模型 API 密钥或依赖其他写作 skill。

### 选择指令语言

默认入口 `SKILL.md` 使用英文，`SKILL.zh-CN.md` 是等价中文版。两个版本均可按任务输出中文或英文。

需要中文指令时，在**独立的安装副本中**把 `SKILL.zh-CN.md` 复制为 `SKILL.md`，同时保留 `references/` 和 `agents/`。Release 提供已经整理好的中英文安装包。安装其中一个即可，名称都为 `reader-ready`，无需重复加载。源仓库中的两个版本保持不变，便于后续更新。

## 使用

可以直接对助手说：

> 用 reader-ready 整理这份给评审看的申请材料，保留规定字段，以我的口吻写。

> 用 reader-ready 修改论文结果和讨论，保留正式科研表达，突出研究主线，去掉重复的防御性措辞。

> 用 reader-ready 检查这份准备发给合作者的 PPT，包括讲稿和图里的文字。

> 用 reader-ready 审阅这份文件，只给修改建议，不改文件。

在 Codex CLI 或 IDE 扩展中，也可以使用 `$reader-ready`。支持自动选择的宿主可以根据任务匹配使用。

## 包含内容

- `SKILL.md` / `SKILL.zh-CN.md`：等价的中英文核心指令。
- `references/`：中英文编辑案例和科研写作指导。
- `agents/openai.yaml`：可选的界面信息。
- `tests/`：双语行为案例和验证方法。
- [SOURCES.md](SOURCES.md)：参考来源、固定版本和取舍说明。

这是指令型 skill。读取或修改 PDF、PPTX、工作簿和图片仍需宿主提供相应工具；工具不足时，助手应明确哪些部分没有检查。它不会为未检查的文件出具完成声明，也不提供 AI 作者身份评分。

## 参与改进与许可

欢迎补充真实适用的修改案例、应当保留原文的反例，以及双语一致性修正。请勿在公开 issue 中提交私人材料。行为发生变化时同步更新中英文版，并参考[验证案例](tests/README.md)检查。

采用 [MIT 许可](LICENSE)。参考项目及其许可见 [SOURCES.md](SOURCES.md)。
