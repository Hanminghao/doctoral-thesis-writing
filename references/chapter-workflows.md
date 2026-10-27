# Chapter Workflows

## Global outline workflow

1. Inventory the thesis title, degree requirements, accepted/publication works, source PDFs, experiments, figures, and existing chapter files.
2. Group the works by scientific question or information source. Do not group only by venue or year.
3. Write one sentence for the thesis problem and one sentence for the capability progression.
4. Build a chapter matrix:

| Chapter | Question | Input/supervision | Method | Evidence | Transition |
|---|---|---|---|---|---|
| 1 | Why does the problem matter? | field and gap | thesis framing | literature and motivation | to foundations |
| 2 | What is shared? | common data/tasks | notation and basis | definitions and metrics | to first work |
| work | What bottleneck is solved? | chapter-specific | method | experiments/analysis | to next gap |
| final | What was established? | all chapters | synthesis | contribution matrix | to future work |

5. Check that every contribution has a chapter and every research chapter has evidence.
6. Add a figure for the global route and a table comparing works, supervision, task, and output.

## Chapter 1 workflow: 绪论

### Draft order

1. Write the research object and application value.
2. Explain why current data, task, or deployment conditions make the problem hard.
3. Organize related work into 3–5 capability categories.
4. End each category with a concrete unresolved gap.
5. Convert gaps into research questions.
6. Write one contribution paragraph per research chapter.
7. Add the technical route figure and chapter map.

### Quality checks

- The title terms all appear in the background and contributions.
- Each contribution is later supported by a chapter and experiment.
- Related work compares mechanisms and limitations; it is not a bibliography dump.
- Claims use the evidence level actually available.
- The final organization paragraph matches the real `.tex` includes.

## Chapter 2 workflow: 相关研究基础

1. List concepts used in at least two later chapters.
2. Define data objects, tasks, notation, model families, metrics, and experimental conventions.
3. Give each subsection a “why it is needed later” closing sentence.
4. Put the thesis-wide technical route at the end.
5. Remove paper-specific novelty and repeated introductions.

For computational pathology, the shared basis commonly includes WSI and patch organization, multi-scale/graph representations, vision-language learning, molecular or spatial transcriptomic alignment, generation models, and task metrics. Use only the items actually used by the thesis.

## Work chapter workflow: 单篇论文/单项工作

### Before drafting

- Read the publication PDF, supplementary material, source or appendix, and experiment tables.
- Extract the exact task, data, method modules, baselines, metrics, and limitations.
- Build a local claims–evidence table.
- Decide what belongs in Chapter 2 and what must be reintroduced here.

### Draft sequence

1. **引言**: bottleneck → prior limitation → chapter question → contribution preview.
2. **Problem and setup**: input, output, assumptions, notation, datasets if chapter-specific.
3. **Overall framework**: one data-flow figure and a paragraph explaining the complete path.
4. **Method modules**: write in execution order; each module states input, operation, output, and purpose.
5. **Objective/training**: define each loss and explain what evidence it is intended to produce.
6. **Experiments**: settings, main comparison, ablations, qualitative/interpretability, discussion.
7. **Chapter summary**: answer the chapter question and identify the next unresolved problem.

### Required experiment narration

For every table or figure, state:

- what question it tests;
- which methods or conditions are compared;
- the main observation;
- the mechanism that plausibly explains it;
- the limit of the conclusion.

## System/application workflow

1. Define the scenario and the role of the system.
2. Separate functional requirements from privacy, latency, reliability, and maintainability requirements.
3. Draw the data flow from acquisition to preprocessing, model service, and result display.
4. Describe modules and interfaces, then implementation details.
5. Show representative normal, degraded, missing-input, and recovery cases when those cases are supported.
6. Report system evidence separately from offline algorithm evidence.
7. State deployment and validation limits.

## Chapter 8 workflow: 总结与展望

1. Restate the thesis problem in one paragraph.
2. Summarize each contribution using problem–method–evidence–value.
3. Add a cross-chapter comparison table.
4. Explain how information, supervision, or capability grows across chapters.
5. List limitations that are visible from the experiments.
6. Convert each limitation into one testable future direction.

## Whole-thesis audit workflow

Run these checks after substantial edits:

- **Story**: title, abstract, Chapter 1 questions, chapter titles, and conclusion describe the same thesis.
- **Coverage**: every major claim has evidence; every important experiment supports a stated claim.
- **Boundaries**: adjacent works have distinct questions and are not presented as one method unless technically integrated.
- **Terminology**: abbreviations, symbols, dataset names, task names, and method names are stable.
- **Figures/tables**: captions explain the comparison, labels are readable, references are complete, and numbering is continuous.
- **Citations**: publication facts come from verified sources; unresolved items are marked `[待核验]`.
- **Repetition**: shared foundations are defined once; chapter introductions focus on the local gap.
- **Formal items**: abstracts match, achievement list is accurate, front matter is complete, and the template compiles cleanly.

