# Behavioral checks / 行为验证

`cases.json` contains 17 paired English/Chinese requests and acceptance criteria. These cover omission without replacement, production notes, authorial voice, useful paths and references, formal scientific prose, narrative development, unnecessary defensive caveats, material contradictory evidence, and review-only scope.

To evaluate a change:

1. Give a fresh agent one instruction edition, its relevant references, and a case's request. Do not show the acceptance criteria or a desired answer. Use only the supplied material; do not contact outside services or edit real user files.
2. Save its actual answer outside the skill's runtime files.
3. Compare the answer with the case's acceptance criteria and source facts. Judge decisions and meaning, not exact phrasing or reduction in word count.
4. Repeat with the other instruction edition. Check semantic equivalence across editions, allowing natural differences between languages.

A structural validator can check frontmatter and links; it cannot establish editorial quality. These text-based checks do not test actual PDF/PPTX/image editing, visual inspection, automatic discovery, or performance across different models. Use real file-level tasks when validating those capabilities in a particular host.

For the initial release, the cases were run in two independent agent contexts, one per language; each batch shared context and was not equivalent to a fresh session for every case.

## Initial release check, 2026-10-06

The coordinating agent reviewed 17 English and 17 Chinese responses against the supplied facts and criteria. English responses met the criteria. The Chinese run exposed one additional editorial issue in case 08: it appended a causal disclaimer to an already scoped association. The scientific-writing references were amended in both languages to distinguish author-facing writing constraints from manuscript content. A fresh Chinese context then handled cases 08, 15, 16, and 17 successfully, removing unnecessary disclaimers while retaining material contradictory evidence and formal prose. This is a small, model-based editorial check, not a cross-model benchmark or human validation study.

Both instruction manifests and the two release packages passed the skill-creator structural validator. Relative documentation links were checked in the source and extracted packages. No actual PDF, presentation, workbook, or image was edited during this test.

---

`cases.json` 包含17组中英文请求及验收标准，覆盖直接省略无关信息、制作说明、叙述口吻、有用的路径和引用、正式科研表达、论文主线、防御性重复、实质反证，以及只审阅不修改的范围控制。

修改后，用独立上下文给助手提供一个语言版本及案例请求，不提供预期答案。保存实际回答，再依据验收标准检查语义和判断，不按措辞匹配、字数下降或自评分验收。另一语言版本也应验证。

这些文字案例不代表已经测试真实 PDF、PPTX、图片的编辑和视觉检查，也不证明自动发现或跨模型表现。首次版本可分中英文两个独立批次验证，但批次内仍共享上下文，应明确这一限制。

2026-10-06首次验证完成17条英文和17条中文请求。协调助手核对回答后，发现中文第08例在准确的相关关系后额外添加因果免责声明。两个语言版本均补充了“写作约束不自动进入正文”的规则。新的独立中文上下文随后通过08、15、16、17四例复测。该结果属于小规模模型编辑检查，不是跨模型基准或人工验证研究。双语指令、安装包结构和相对链接也完成检查。
