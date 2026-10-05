# reader-ready

English · [简体中文](README.zh-CN.md)

**Write for the reader.**

Audience-aware editing for writing and text-bearing artifacts. Shape the content, voice, and level of detail around the people who will receive the work, while preserving the author's meaning, evidence, and genre.

Use the same editorial judgment during drafting, revision, and final review: in applications, reports, articles, forms, slides, speaker notes, scientific manuscripts, and figure text.

## How it works

**Understand the reader and purpose → decide what belongs → shape the expression → check the deliverable.**

1. **Establish the context.** Identify the audience, purpose, author or speaker, genre, and the parts of the file that will be shared.
2. **Choose what belongs.** Keep information that helps readers understand, assess, locate, or act. Rewrite useful information whose voice or placement is wrong; move production notes into the working conversation or an appropriate existing record; remove details that add nothing.
3. **Shape the expression.** Use the right authorial voice, make the important points easy to find, and preserve the genre's level of formality. Remove redundant explanations and formulaic prose where they obscure the content.
4. **Check what readers receive.** Inspect relevant text in the actual file, including notes, captions, and embedded figure text, using the tools available for that format.

These are contextual decisions. An irrelevant project name can simply disappear without a replacement. A path may be essential in a reproduction handoff and irrelevant in a shared presentation. Clear writing can stay unchanged.

## One approach across different kinds of work

| Context | How the shared approach applies |
| --- | --- |
| Applications and personal materials | Use the appropriate authorial voice and verified roles or contributions. Preserve required fields; remove labels that repeat what is already clear. |
| Supporting documents | Keep evidence and useful captions. Leave screenshot assembly instructions and page-replacement reminders in the working conversation. |
| Reports, articles, and forms | Organize information around the reader's task. Keep useful references and required content; trim repetitive explanations and empty framing. |
| Slides and speaker notes | Make slide text and notes serve the presentation. Remove irrelevant local paths and production instructions from the shared material. |
| Figures and charts | Keep labels, definitions, and evidence needed to understand the result. Omit internal names and process labels that add nothing. |
| Scientific manuscripts | Build a clear research argument in formal academic prose, with claims calibrated to the evidence and qualifications placed where they help interpretation. |
| Technical handoffs and tutorials | Retain paths, versions, and pending tasks when they are part of what the recipient needs. |

### Applying the approach to scientific writing

Scientific writing uses the same core rules, with [additional guidance](references/scientific-writing.en.md) loaded when drafting or revising a manuscript. This covers abstracts, introductions, methods, results, discussions, and figure legends.

- **Preserve academic register.** Use precise, stable terminology and field-appropriate constructions, including passive voice or first person when appropriate.
- **Give the argument a clear direction.** Connect the research question, gap, evidence, findings, and contribution. When restructuring is within scope, order material by its role in the argument rather than the sequence of analyses performed.
- **Make supported claims directly.** A result already phrased as an association usually does not need an automatic sentence denying causality. Remove repeated apologies and pre-emptive rebuttals; place substantive qualifications where readers need them.
- **Keep the evidence intact.** Preserve statistics, sample units, citations, consequential counterevidence, and limitations that affect interpretation. The interest comes from the question and findings, with claims proportionate to the evidence.

For example, if an observational study's design and limitations are already clear, “X was associated with Y” may be sufficient. Adding “However, this cannot prove causality” after every such result repeats a boundary already expressed by the claim. If the surrounding text implies causality, revise that implication or retain the specific qualification it needs.

## Use

Ask your agent:

> Use reader-ready to prepare this application for the review panel. Keep the required fields and write in my voice.

> Use reader-ready to revise this manuscript's Results and Discussion. Keep formal scientific prose, sharpen the research argument, and remove redundant defensive wording.

> Use reader-ready to review this deck before I send it to colleagues, including the speaker notes and text in figures.

> Review this document with reader-ready. Give recommendations only; do not change the file.

The skill follows the scope of the request: drafting, editing, or recommendations only. In Codex CLI or the IDE extension, it can also be mentioned as `$reader-ready`. Automatic selection is allowed when the host supports it.

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

### Instruction language

The default `SKILL.md` is English. `SKILL.zh-CN.md` is the equivalent Chinese edition. Both can produce Chinese or English and follow the language of the task.

To use Chinese instructions, copy the Chinese edition to `SKILL.md` **inside a separate installation copy**. Keep `references/` and `agents/` alongside it. [Releases](https://github.com/LianaSakana001/reader-ready/releases) provide ready-to-install English and Chinese packages. Install one edition under the name `reader-ready`; loading both is unnecessary. Keep the source repository's two editions intact for updates.

## Project contents and execution

- [SKILL.md](SKILL.md) / [SKILL.zh-CN.md](SKILL.zh-CN.md): equivalent core instructions.
- `references/`: paired editorial examples and scientific-writing guidance, consulted as relevant to the task.
- `agents/openai.yaml`: interface metadata.
- [tests/](tests/README.md): bilingual behavioral cases and evaluation guidance.
- [SOURCES.md](SOURCES.md): references, pinned versions, and the choices made when adapting ideas.

The core instructions establish the shared editorial judgment; the references provide detail for specific contexts. Both instruction languages follow the same approach.

File editing, text recognition in images, and rendering checks use the host's tools. The skill guides editorial choices and the scope of inspection; the agent reports the delivery status based on the checks actually completed.

## Contributing and license

Useful contributions include realistic before/after cases, cases where an apparent problem should be left alone, and corrections to bilingual equivalence. Keep private materials out of public issues. Update both instruction editions when changing behavior; use [the behavioral cases](tests/README.md) to check the change.

[MIT](LICENSE). Source projects and their licenses are credited in [SOURCES.md](SOURCES.md).
