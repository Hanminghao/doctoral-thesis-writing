---
name: doctoral-thesis-writing
description: Plan, draft, revise, and audit Chinese doctoral theses built from multiple research works. Use when the user asks for a dissertation outline, introduction, research-foundation chapter, paper-derived method chapter, system/application chapter, conclusion, or whole-thesis consistency review.
---

# Doctoral Thesis Writing

Use this skill for a dissertation-sized narrative. It supports both the global outline and the writing workflow inside each chapter. Read [thesis-writing-patterns.md](references/thesis-writing-patterns.md) when deciding structure or prose conventions, and read [chapter-workflows.md](references/chapter-workflows.md) for the selected chapter mode.

## Working principles

- Build one thesis argument from the research works; do not paste papers into consecutive chapters.
- Organize chapters by scientific problem and capability progression, not by publication date.
- Keep one main question per research chapter. A chapter may contain several modules only when they answer the same question.
- Use the recurring chapter shape `引言 → 问题定义/方法 → 实验与分析 → 本章小结`; add a short chapter-specific related-work section only when it is needed.
- Map every contribution claim to concrete evidence: dataset, comparison, ablation, visualization, deployment case, or verified publication result.
- Separate facts from interpretation. Never invent metrics, datasets, citations, publication status, author order, or clinical claims.
- Preserve boundaries between adjacent works. If two works share data or a technique, state their different research questions, supervision, scale, and output.
- End each chapter with what it establishes and why the next chapter is needed. End the thesis with capability gains, limits, and testable future work.
- Use formal, direct Chinese academic prose. Define abbreviations at first use, keep terminology stable, and avoid claims stronger than the evidence.

## Originality and similarity control

Reference theses are structural examples only. Their wording, paragraph order, transitions, contribution lists, figure captions, examples, and conclusions must not be reused. Standard academic labels such as “绪论”“相关研究基础”“实验结果与分析”“本章小结” are conventional and may be retained, but the prose and argument inside them must come from the user's own topic, papers, data, and results.

When drafting:

- write from primary evidence and the user's research records, not by paraphrasing a reference dissertation sentence by sentence;
- redesign the literature-review categories around this thesis's scientific questions;
- give each chapter an original problem statement, transition, figure caption, and evidence interpretation;
- cite the source when a definition, taxonomy, equation, or prior claim comes from published work;
- treat any similarity scan as a screening tool, not as proof of originality; unresolved high-overlap passages must be rewritten or properly quoted/cited before submission.

Before final delivery, run a phrase-level self-check against the reference material when text extraction is available. Flag long repeated phrases, distinctive sentence templates, copied lists, and near-identical captions. Do not attempt to evade a formal checker by making cosmetic word substitutions; rewrite the reasoning in the thesis's own structure and voice.

## Choose a mode

Infer the mode from the request; if several apply, start with the global outline and then route to the relevant chapter mode.

### `outline`

Use for “规划大纲”“设计论文结构”“如何组织几篇论文”. Inspect the project, reference theses, approved title, and available papers. Produce:

1. a one-paragraph thesis thesis statement;
2. a chapter map with each chapter's question, input, method, evidence, and transition;
3. a claims–evidence matrix;
4. a figure/table plan;
5. risks and boundaries, especially duplicated works or missing evidence;
6. a writing order.

Prefer `绪论 + 研究基础 + one chapter per coherent work + 总结与展望`. Use a seven-chapter layout when there are four coherent works; use eight or more chapters when the work count or scientific boundaries require it. Do not split a chapter only to mirror a paper if the chapter would be thin.

### `introduction`

Use for 第 1 章. Write from broad field to thesis gap to research questions to contributions to organization. The literature review must be synthesized by problem or information source, not a list of papers. Every listed contribution must appear later as a research chapter with evidence.

### `foundation`

Use for 第 2 章 or a related research basis chapter. Define data objects, task formulations, notation, common models, metrics, and experimental conventions shared by later chapters. Move paper-specific novelty to the corresponding research chapter. End with a unified technical route.

### `work`

Use for a chapter derived from one paper or one tightly connected work package. Follow the per-chapter workflow in the reference. Rewrite the paper's introduction and conclusion to fit the dissertation, retain only necessary related work, and make the method self-contained. Present experiments in the order `settings → main comparison → ablation → qualitative/interpretability → discussion`.

### `system`

Use when the research includes an implementation, deployment, clinical/industry scenario, or integrated prototype. Treat the system as a validation layer for preceding methods: requirements, architecture, data flow, modules, deployment, representative cases, limitations, and chapter summary. Do not claim clinical efficacy from a prototype demonstration.

### `conclusion`

Use for the final chapter. Re-synthesize the research questions and evidence instead of repeating abstracts. Include a cross-chapter comparison, overall limitations, and concrete future work. Future work must follow from observed gaps, such as missing modalities, cross-domain generalization, biological validation, or untested deployment conditions.

### `audit`

Use for a whole-thesis review. Check title and contribution alignment, chapter transitions, duplicated definitions, notation, citation provenance, figure/table numbering, experiment consistency, publication claims, and compliance with the local graduate-school template. Report issues with file and section references when available.

## Evidence and source handling

Before drafting a paper-derived chapter, locate the accepted/publication PDF, supplementary material, source code or LaTeX, experiment tables, and reviewer responses if available. Prefer the publication version for bibliographic facts and the author's source for implementation details. Mark unresolved items as `[待核验]`; never fill them from memory.

For the current thesis project, use `论文大纲规划.md` as a working map when it exists, and verify it against the local paper PDFs before changing the map. Keep planning documents outside the Overleaf source folder unless the user explicitly asks to sync them.

## Required output quality

For planning, return a reviewable outline rather than generic advice. For drafting, return prose that can be inserted into the target `.tex` file, with section labels, figure/table placeholders, and citation placeholders tied to verified sources. For audits, classify findings as `必须修改`, `建议修改`, or `待确认`, and state the evidence for each finding.

## Supporting references

- [thesis-writing-patterns.md](references/thesis-writing-patterns.md): patterns distilled from the five reference dissertations and boundaries for applying them.
- [chapter-workflows.md](references/chapter-workflows.md): detailed workflows and checklists for outline, introduction, foundation, work, system, conclusion, and audit modes.
