# Sources and design choices / 参考来源与取舍

Reader-ready was developed from audience-specific editorial needs and informed by the projects below. Its instructions and examples were written for this project; upstream skill files are not bundled or required at runtime. The references credit conceptual influences, not compatibility or endorsement.

本项目从面向读者的实际编辑需求出发，参考下列公开项目。指令和案例为本项目编写，没有捆绑上游 skill 文件，也不依赖它们运行。引用用于说明借鉴来源，不代表兼容性认证或原作者背书。

Repository statistics were read through the GitHub API on **2026-10-06**. Stars and forks indicate public attention, not active use or measured editing quality. Smaller specialist projects supplement the more widely followed general projects. All listed repositories reported MIT licensing at the inspected revision.

仓库关注度于 **2026-10-06** 通过 GitHub API 核对。Star 和 fork 不能代表实际使用量或编辑效果。通用项目选择传播较广的来源，规模较小的专项项目用于补充具体问题。所查版本的仓库许可均为 MIT。

| Project | Stars / forks at inspection | Inspected version |
| --- | --- | --- |
| [blader/humanizer](https://github.com/blader/humanizer) | 54,115 / 4,301 | [225a6f39](https://github.com/blader/humanizer/blob/225a6f39ac85f76ee48dbad772ea4abe4ed6c9d8/SKILL.md) · [license](https://github.com/blader/humanizer/blob/225a6f39ac85f76ee48dbad772ea4abe4ed6c9d8/LICENSE) |
| [op7418/Humanizer-zh](https://github.com/op7418/Humanizer-zh) | 18,951 / 1,228 | [f4518a8e](https://github.com/op7418/Humanizer-zh/blob/f4518a8eab97b8bfebc66a89d34320a89bef6930/SKILL.md) · [license](https://github.com/op7418/Humanizer-zh/blob/f4518a8eab97b8bfebc66a89d34320a89bef6930/LICENSE) |
| [hardikpandya/stop-slop](https://github.com/hardikpandya/stop-slop) | 17,764 / 1,295 | [8da1f030](https://github.com/hardikpandya/stop-slop/blob/8da1f030185bdfe8471220585162991eaeb970e9/SKILL.md) · [license](https://github.com/hardikpandya/stop-slop/blob/8da1f030185bdfe8471220585162991eaeb970e9/LICENSE) |
| [Worigin0314/academic-defensive-writing-auditor](https://github.com/Worigin0314/academic-defensive-writing-auditor) | 114 / 3 | [89f26b8a](https://github.com/Worigin0314/academic-defensive-writing-auditor/blob/89f26b8a7f8149e6458f657010d354587d42cfe9/SKILL.md) · [license](https://github.com/Worigin0314/academic-defensive-writing-auditor/blob/89f26b8a7f8149e6458f657010d354587d42cfe9/LICENSE) |
| [Adkid-Zephyr/anti-defensive-writing-Skill](https://github.com/Adkid-Zephyr/anti-defensive-writing-Skill) | 2,173 / 48 | [102c8b21](https://github.com/Adkid-Zephyr/anti-defensive-writing-Skill/blob/102c8b21acf5eda3a0aef3d9779a65db646c8980/skills/anti-defensive-writing-en/SKILL.md) · [license](https://github.com/Adkid-Zephyr/anti-defensive-writing-Skill/blob/102c8b21acf5eda3a0aef3d9779a65db646c8980/LICENSE) |
| [Rimagination/good-story](https://github.com/Rimagination/good-story) | 133 / 17 | [978c44d9](https://github.com/Rimagination/good-story/blob/978c44d977c6934f82923570ddfa0b7b0ef755c3/SKILL.md) · [license](https://github.com/Rimagination/good-story/blob/978c44d977c6934f82923570ddfa0b7b0ef755c3/LICENSE) |
| [K-Dense-AI/scientific-agent-skills](https://github.com/K-Dense-AI/scientific-agent-skills) | 47,669 / 4,304 | [92ace75a](https://github.com/K-Dense-AI/scientific-agent-skills/blob/92ace75ac21efe19a620434e0ca4e356081fe807/skills/scientific-writing/SKILL.md) · [license](https://github.com/K-Dense-AI/scientific-agent-skills/blob/92ace75ac21efe19a620434e0ca4e356081fe807/LICENSE) |

## blader/humanizer

Voice matching, unnecessary framing, and chat/draft residue. We retain legitimate punctuation and sentence structures instead of imposing a universal style.

参考作者声音、无效铺垫和聊天／改稿残留的处理；保留有用标点和句式，不强制统一风格。

## op7418/Humanizer-zh

Context-sensitive Chinese editing, semantic fidelity, and final-text delivery. Our artifact review additionally evaluates whether production paths and labels belong.

参考中文语境判断、语义保真和直接交付终稿；另按载体判断制作路径和标签是否应该出现。

## hardikpandya/stop-slop

Directness and respect for the reader. We do not adopt blanket bans on adverbs, passive voice, or dashes, nor a required style score.

参考直接表达和尊重读者的原则；不采用副词、被动句、破折号禁令或强制评分。

## Worigin0314/academic-defensive-writing-auditor

Distinguishing meaningful qualifications from repeated non-claim disclaimers. We use contextual decisions without a mandatory audit table, score, or caveat quota.

参考必要限定和重复免责的区分；按语境判断，不强制输出审计表、分数或限定词配额。

## Adkid-Zephyr/anti-defensive-writing-Skill

Contribution-led organization and avoiding an experiment diary or anticipatory self-defense. We keep material counterevidence and do not change prespecified outcomes to make a story favorable.

参考围绕贡献组织论文、避免实验流水账和预先自辩；保留实质反证，不为叙事有利而改变预设结局。

## Rimagination/good-story

Organizing a scientific argument around the research question and supported contribution. We do not require story cards, literary roles, or a fixed narrative template.

参考围绕研究问题和有依据的贡献组织论证；不要求故事卡、文学角色或固定叙事模板。

## K-Dense-AI/scientific-agent-skills

Scientific consistency across claims, numerical evidence, methods, and figures. The current scientific-writing module was consulted for fidelity; its evidence registries and approval workflow are not incorporated.

参考主张、定量证据、方法和图表的一致性；查阅当前科研写作模块以完善保真要求，不引入其证据台账和审批流程。

## Packaging references / 安装参考

- [OpenAI: Build skills](https://learn.chatgpt.com/docs/build-skills): manifest shape, local discovery, and invocation.
- [Vercel Skills CLI](https://github.com/vercel-labs/skills): repository installation and agent/scope options.

These are packaging references rather than editorial rules.
以上用于核对打包和安装方式，不作为编辑规则。
