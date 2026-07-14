# ITU-T Recommendation Reviewer

A **model-agnostic AI agent skill** that reviews draft **ITU-T Recommendations** (including ITU-T | ISO/IEC common texts, amendments, and corrigenda) for compliance with the official ITU-T drafting rules — before the text goes to TSB or is proposed for consent, determination, or approval.

The skill is written entirely in plain Markdown, so **any large language model or AI agent can use it** — load the files into the model's context, or install them in any agent framework that supports the open [Agent Skills](https://agentskills.io) format (SKILL.md + reference files).

It encodes the drafting and presentation rules from three authoritative sources:

1. **ITU-T Editing Guidelines — Author's guide for drafting ITU-T Recommendations** (06/2023) — the primary rulebook for pure ITU-T texts ([ITU permalink](https://www.itu.int/oth/T0A0F0000040005))
2. **Rules for presentation of ITU-T | ISO/IEC common text** (09/2014) — overrides the Author's guide for joint ITU-T | ISO/IEC documents
3. **Recommendation ITU-T A.1** (09/2019) — ITU-T working methods ([ITU permalink](https://www.itu.int/rec/T-REC-A.1))

> The ITU source documents themselves are **not** redistributed in this repository. They are © ITU and available free of charge from the links above and the [ITU-T website](https://www.itu.int/en/ITU-T/).

## What it does

Given a draft Recommendation (as .docx, PDF, or pasted text), the skill instructs the model to:

1. **Classify the document type first** — pure ITU-T text, ITU-T | ISO/IEC common text, or amendment/corrigendum — and apply the correct rulebook.
2. **Run a six-pass review**: skeleton & mandatory elements → boilerplate wording → references & citations → definitions & abbreviations → figures/tables/equations/notes → quality checklist & language.
3. **Produce a structured review report** with an overall verdict (READY / MINOR REVISION / MAJOR REVISION), findings graded Critical / Major / Minor, each pinpointed to a clause and citing the governing rule, plus the Annex D pre-approval checklist as a pass/fail table.
4. **Offer follow-through** — corrected clauses with revision marks, rewritten definitions, or ready-to-paste boilerplate.

The skill checks drafting/presentation compliance and internal consistency. It does **not** judge the technical correctness of the standard's subject matter, and it never predicts approval outcomes.

## Installation

### Any LLM (ChatGPT, Gemini, Qwen, DeepSeek, local models, …)

The skill is just Markdown. Attach or paste `SKILL.md` plus the five files in `references/` into the conversation (or your tool's knowledge/context feature), then ask the model to review your draft following SKILL.md.

### Agent frameworks supporting the Agent Skills format

Clone this repository into your agent's skills directory, e.g. for Claude Code:

```bash
git clone https://github.com/TheTaoism/itu-t-recommendation-reviewer.git \
  ~/.claude/skills/itu-t-recommendation-reviewer
```

### Claude apps (claude.ai / desktop / Cowork)

Download [`itu-t-recommendation-reviewer.skill`](./itu-t-recommendation-reviewer.skill) and add it in **Settings → Capabilities → Skills**.

## Usage

Upload or paste your draft and ask, for example:

- *"Review this draft Recommendation for ITU-T compliance."*
- *"Does my draft follow the ITU-T Author's Guide? Prepare it for TSB submission."*
- *"检查这份 ITU-T 建议书草案是否符合编辑规则。"*
- *"How should I structure the Definitions clause of an ITU-T | ISO/IEC common text?"*

The report is delivered in your working language; quoted rule text and suggested replacement text stay in English (the publication language).

## Repository layout

```
SKILL.md                          # Skill entry point: workflow, report template, severity calibration
references/
  structure-rules.md              # Mandatory elements, clause order, required boilerplate
  formatting-rules.md             # Fonts, numbering, figures, tables, notes, citation style
  definitions-rules.md            # Rules for writing definitions
  common-text-rules.md            # Deviations for ITU-T | ISO/IEC joint texts
  quality-checklist.md            # Annex D pre-approval checklist + A.1 process checks
itu-t-recommendation-reviewer.skill   # Packaged skill for Claude apps (optional convenience)
```

## Contributing

Contributions are welcome — see [CONTRIBUTING.md](./CONTRIBUTING.md).

Please note: **all changes go through pull requests and require review and approval by the maintainer** before they are merged. Direct pushes to `main` are not accepted.

## Disclaimer

This is an independent community project. It is not endorsed by, affiliated with, or approved by the International Telecommunication Union (ITU), nor by any AI vendor. "ITU" and "ITU-T" are used solely to describe the subject matter. Always verify review findings against the current official ITU-T editing guidelines.

## License

[MIT](./LICENSE) — anyone may download, use, modify, and redistribute this skill, commercially or otherwise, provided the license notice is preserved.
