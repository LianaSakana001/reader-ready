# reader-ready

[简体中文](README.zh-CN.md) · [English skill](SKILL.md) · [中文 Skill](SKILL.zh-CN.md)

Prepare writing for the people who will actually read it. Remove irrelevant production details, misplaced assistant narration, redundant explanations, and formulaic prose while preserving the author's meaning and the document's purpose.

Use it when drafting, revising, or preparing applications, reports, articles, forms, slide decks, speaker notes, scientific manuscripts, and figures containing text.

## What it changes

| Situation | Editorial decision |
| --- | --- |
| A figure includes a private project name that adds nothing | Omit it. No replacement name is required. |
| A supporting page explains how screenshots were stitched | Keep the evidence and relevant caption; remove assembly chatter. |
| A personal achievement entry says “The applicant is a contributing author” | Use the appropriate authorial voice and verified role or contribution. |
| Speaker notes include a local image path | Keep the talk notes useful to recipients; move production references out when needed. |
| A paper repeatedly says its results “cannot prove” things it never claimed | State the supported result directly; retain material boundaries where they matter. |
| A tutorial or reproduction handoff needs a path | Keep it. Context determines relevance. |

The skill decides whether to keep, rewrite, move, or remove information. Names, pronouns, paths, passive voice, and punctuation are not blacklisted. Clear writing can stay unchanged.

## Scientific writing

Both instruction editions explicitly support drafting and revising abstracts, introductions, methods, results, discussions, and figure legends. The [scientific writing guide](references/scientific-writing.en.md) covers:

- Formal, field-appropriate prose, with stable terminology and suitable passive or first-person constructions.
- A clear research argument: why the question matters, what the study found, and what the contribution changes.
- Direct, proportionate claims without repeated apologies, imagined reviewer objections, or automatic disclaimers.
- Accurate statistics, sample units, citations, and substantive qualifications. Scientific storytelling does not require literary language.

## Install

With the community [Skills CLI](https://github.com/vercel-labs/skills), choose your agent and installation scope:

```sh
npx skills add LianaSakana001/reader-ready --skill reader-ready
```

For a user-wide Codex installation:

```sh
npx skills add LianaSakana001/reader-ready --skill reader-ready --agent codex --global
```

Alternatively, copy this repository into a `reader-ready` directory in your agent's skill location, keeping `SKILL.md`, `references/`, and `agents/` together. See [Codex's official skill documentation](https://learn.chatgpt.com/docs/build-skills) for supported local locations. No Python package, model API key, or other writing skill is required to use these instructions.

### Choose the instruction language

The default `SKILL.md` is English. `SKILL.zh-CN.md` is the equivalent Chinese edition. Both can produce Chinese or English and follow the language of the task.

To use Chinese instructions, copy the Chinese edition to `SKILL.md` **inside a separate installation copy**. Keep `references/` and `agents/` alongside it. Release archives provide ready-to-install English and Chinese packages. Install one edition under the name `reader-ready`; loading both is unnecessary. Keep the source repository's two editions intact for updates.

## Use

Ask your agent:

> Use reader-ready to prepare this application for the review panel. Keep the required fields and write in my voice.

> Use reader-ready to revise this manuscript's Results and Discussion. Keep formal scientific prose, sharpen the research argument, and remove redundant defensive wording.

> Use reader-ready to review this deck before I send it to colleagues, including the speaker notes and text in figures.

> Review this document with reader-ready. Give recommendations only; do not change the file.

In Codex CLI or the IDE extension, the skill can also be mentioned as `$reader-ready`. Automatic selection is allowed when the host supports it.

## What is included

- `SKILL.md` / `SKILL.zh-CN.md`: equivalent core instructions.
- `references/`: paired editorial examples and scientific-writing guidance.
- `agents/openai.yaml`: optional interface metadata.
- `tests/`: bilingual behavioral cases and evaluation guidance.
- [SOURCES.md](SOURCES.md): references, pinned versions, and the choices made when adapting ideas.

This is an instruction skill. Reading or editing a PDF, PPTX, workbook, or image still requires suitable tools in the host. When those tools are unavailable, the agent should describe the specific unchecked surface. It does not certify a file it could not inspect or provide an AI-authorship score.

## Contributing and license

Useful contributions include realistic before/after cases, cases where an apparent problem should be left alone, and corrections to bilingual equivalence. Keep private materials out of public issues. Update both instruction editions when changing behavior; use [the behavioral cases](tests/README.md) to check the change.

[MIT](LICENSE). Source projects and their licenses are credited in [SOURCES.md](SOURCES.md).
