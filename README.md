# ITU-T Recommendation Reviewer

A **model-agnostic AI agent skill** that reviews draft **ITU-T Recommendations** (including ITU-T | ISO/IEC common texts, amendments, and corrigenda) for compliance with the official ITU-T drafting rules — before the text goes to TSB or is proposed for consent, determination, or approval.

The skill is written entirely in plain Markdown, so **any large language model or AI agent can use it** — point the model at the files on GitHub, load them into the model's context, or install them in any agent framework that supports the open [Agent Skills](https://agentskills.io) format (SKILL.md + reference files).

It encodes the drafting and presentation rules from three authoritative sources:

1. **ITU-T Editing Guidelines — Author's guide for drafting ITU-T Recommendations** (06/2023) — the primary rulebook for pure ITU-T texts ([ITU permalink](https://www.itu.int/oth/T0A0F0000040005))
2. **Rules for presentation of ITU-T | ISO/IEC common text** (09/2014) — overrides the Author's guide for joint ITU-T | ISO/IEC documents
3. **Recommendation ITU-T A.1** (09/2019) — ITU-T working methods ([ITU permalink](https://www.itu.int/rec/T-REC-A.1))
4. **TSAG LS20 Attachment 1** — draft *Checklist for draft ITU-T Deliverables* (source: contribution TSAG-C48 by OKI, NICT and The University of Tokyo; TSAG, Geneva, January 2026). A rapporteur-meeting readiness checklist circulated by TSAG to all Study Groups for comment — currently a **draft**, and reported as such.

> The ITU source documents themselves are **not** redistributed in this repository. They are © ITU and available free of charge from the links above and the [ITU-T website](https://www.itu.int/en/ITU-T/).

## What it does

Given a draft Recommendation (as .docx, PDF, or pasted text), the skill instructs the model to:

1. **Classify the document type first** — pure ITU-T text, ITU-T | ISO/IEC common text, or amendment/corrigendum — and apply the correct rulebook.
2. **Run a six-pass review**: skeleton & mandatory elements → boilerplate wording → references & citations → definitions & abbreviations → figures/tables/equations/notes → quality checklist & language.
3. **Produce a structured review report** with an overall verdict (READY / MINOR REVISION / MAJOR REVISION), findings graded Critical / Major / Minor, each pinpointed to a clause and citing the governing rule, plus the Annex D pre-approval checklist as a pass/fail table.
4. **Offer follow-through** — corrected clauses with revision marks, rewritten definitions, or ready-to-paste boilerplate.

The skill checks drafting/presentation compliance and internal consistency. It does **not** judge the technical correctness of the standard's subject matter, and it never predicts approval outcomes.

## Quick start — no download required

You do not have to clone or download anything. If your model or agent can fetch web pages (for example Claude with web access, ChatGPT with browsing, Gemini, or any agent with a `fetch`/`web_fetch` tool), simply tell it where the skill lives and let it read the files itself.

Attach your draft and send a prompt such as:

```
Use the following skill file
https://github.com/openitu/itu-t-recommendation-reviewer/blob/main/SKILL.md
and all the files in the folder
https://github.com/openitu/itu-t-recommendation-reviewer/tree/main/references
to review the attached draft Recommendation for ITU-T compliance.
```

The model will fetch `SKILL.md`, follow its instructions to load the five reference files, and then run the review on your draft. The same prompt works in Chinese or any other working language:

```
请读取 https://github.com/openitu/itu-t-recommendation-reviewer/blob/main/SKILL.md
以及 https://github.com/openitu/itu-t-recommendation-reviewer/tree/main/references
目录下的全部文件，并据此检查附件中的 ITU-T 建议书草案是否符合编辑规则。
```

Tips:

- If the model has trouble reading the GitHub HTML pages, give it the **raw** URLs instead, e.g. `https://raw.githubusercontent.com/openitu/itu-t-recommendation-reviewer/main/SKILL.md` and `https://raw.githubusercontent.com/openitu/itu-t-recommendation-reviewer/main/references/<file>.md`.
- Always referencing the `main` branch means you automatically get the latest version of the rules — no need to re-download after each update.
- If your model has no web access, use one of the installation options below.

## Installation

### Any LLM (ChatGPT, Gemini, Qwen, DeepSeek, local models, …)

The skill is just Markdown. Attach or paste `SKILL.md` plus the five files in `references/` into the conversation (or your tool's knowledge/context feature), then ask the model to review your draft following SKILL.md.

### Agent frameworks supporting the Agent Skills format

Clone this repository into your agent's skills directory, e.g. for Claude Code:

```
git clone https://github.com/OpenITU/itu-t-recommendation-reviewer.git \
  ~/.claude/skills/itu-t-recommendation-reviewer
```

### Claude apps (claude.ai / desktop / Cowork)

Download [`itu-t-recommendation-reviewer.skill`](https://github.com/openitu/itu-t-recommendation-reviewer/blob/main/itu-t-recommendation-reviewer.skill) and add it in **Settings → Capabilities → Skills**.

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

Contributions are welcome — see [CONTRIBUTING.md](CONTRIBUTING.md).

Please note: **all changes go through pull requests and require review and approval by the maintainer** before they are merged. Direct pushes to `main` are not accepted.

## Disclaimer

This is an independent community project. It is not endorsed by, affiliated with, or approved by the International Telecommunication Union (ITU), nor by any AI vendor. "ITU" and "ITU-T" are used solely to describe the subject matter. Always verify review findings against the current official ITU-T editing guidelines.

## License

[MIT](LICENSE) — anyone may download, use, modify, and redistribute this skill, commercially or otherwise, provided the license notice is preserved.
