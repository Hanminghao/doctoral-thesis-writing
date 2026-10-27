# Dissertation Writing Patterns

This reference distills the common writing architecture observed in five Fudan doctoral dissertation examples: a pathology-image analysis thesis, a multimodal emotion-understanding thesis, a real-world video object segmentation thesis, an adversarial patch thesis, and the LMC multimodal emotion thesis. The goal is to transfer durable writing decisions, not copy topic-specific content.

## Shared dissertation architecture

The examples consistently use:

1. front matter: abstract, English abstract, lists of figures/tables, contents, and academic achievements;
2. Chapter 1: introduction;
3. Chapter 2: research foundations or related work;
4. Chapters 3–6: four research or application chapters;
5. Chapter 7: summary and outlook;
6. references, doctoral-period achievements, and acknowledgements.

The number of research chapters is flexible. The invariant is that each chapter owns one research question and ends with a local summary. A dissertation with five independent works can use eight chapters: introduction, foundations, five work chapters, conclusion.

## Introduction pattern

The reference introductions use this order:

1. field background and practical/scientific value;
2. evolution of the field and the specific technical object;
3. categorized state of the art;
4. unresolved challenges, written as explicit questions;
5. research content and contributions, one item per later chapter;
6. full-text organization.

The strongest introductions do not enumerate papers one by one. They synthesize prior work by the missing capability, such as context modeling, real-world robustness, attack/defense setting, or multimodal information source.

## Foundations chapter pattern

Chapter 2 introduces only what multiple later chapters need. Typical subsections are:

- data and task definitions;
- core model families and notation;
- learning or optimization concepts;
- common evaluation metrics and datasets;
- a short chapter summary that leads to the first method chapter.

The foundations chapter should not duplicate the full related work of each paper. Novel modules, contribution-specific assumptions, and paper-specific implementation details belong in later chapters.

### Pathology-specific refinement

The pathology dissertation organizes Chapter 1 and Chapter 2 by learning setting and clinical task rather than by model name. Its foundation chapter separately defines weakly supervised multiple-instance learning, semi-supervised learning, active learning, and multimodal deep learning, then gives a glossary of abbreviations. For a computational-pathology dissertation, this is a useful pattern: define WSI/patch/spot objects, task supervision, clinical endpoints, and common metrics before introducing the proposed methods.

The pathology example also shows that a multimodal or prognosis chapter benefits from explicit data curation, cohort composition, statistical software, and interpretability analysis. Include those details only when the thesis has the corresponding evidence.

## Research chapter pattern

Across the examples, a research chapter usually follows:

### 1. 引言

State the specific bottleneck, why existing solutions are insufficient, and the chapter's contribution. The final paragraph previews the method and experiments.

### 2. 问题定义与方法

Introduce input/output, assumptions, symbols, and the full framework before individual modules. A reader should be able to reconstruct the algorithm from this section alone.

Recommended order:

1. task formulation;
2. overall architecture;
3. data representation or preprocessing;
4. core modules in data-flow order;
5. objective functions and training/inference procedure;
6. complexity, implementation, or design discussion when it supports a claim.

### 3. 实验设计与结果分析

Use a stable order:

1. datasets and evaluation metrics;
2. implementation details and baselines;
3. main comparison;
4. controlled ablations;
5. qualitative, visualization, interpretability, or case analysis;
6. discussion of what the evidence proves and what it does not prove.

### 4. 本章小结

State the problem solved, the mechanism that solved it, the evidence supporting it, and the capability passed to the next chapter. Do not merely repeat the abstract.

## System/application chapter pattern

When a thesis contains a deployment or prototype chapter, the examples use:

1. application motivation and scenario;
2. functional and non-functional requirements;
3. overall architecture and data flow;
4. key modules;
5. implementation and representative cases;
6. deployment limits and chapter summary.

The system chapter should verify that earlier methods can be organized into a usable loop. It should report conditions, cases, latency or resource information when available, and clear boundaries around clinical or operational claims.

## Summary and outlook pattern

The final chapter has two jobs:

- compress the thesis into a coherent answer to the research questions;
- identify the next experiments or systems that follow from the limitations.

Use one numbered paragraph for each major contribution, then add a cross-chapter synthesis. Future work should be concrete: a new data condition, a new supervision source, a new generalization setting, or a measurable deployment target.

## Front matter and formal completeness

The examples all treat the following as part of dissertation completeness:

- Chinese and English abstracts with matching contributions;
- lists of figures and tables when the thesis contains them;
- consistent title, advisor, department, degree, and classification information;
- a doctoral-period publication/achievement list;
- an abbreviation/glossary page when the thesis contains many repeated technical terms;
- references and acknowledgements.

Check these after content is stable. Do not allow a placeholder title, author information, or publication claim to survive into a submission build.

## What to transfer and what not to transfer

Transfer:

- problem-driven chapter ordering;
- one question per work chapter;
- repeated chapter skeleton;
- explicit experiment purpose and local summary;
- cross-chapter transitions;
- a final contribution and limitation synthesis.

Do not transfer blindly:

- the exact number of chapters;
- topic-specific sections such as emotion theory, adversarial attacks, or video segmentation taxonomies;
- a system chapter when no actual system evidence exists;
- claims of clinical or real-world effectiveness without corresponding data;
- a paper's conference page limit or citation style into a dissertation.

## Similarity boundary

The safe unit of transfer is a **chapter function**, not a paragraph. It is acceptable for several dissertations to contain an introduction, a foundations chapter, a method section, an experiment section, and a local summary because these are conventional academic functions. It is unsafe to reproduce:

- the same motivation paragraphs or sentence skeletons;
- the same order of literature categories when it does not follow the new thesis's questions;
- distinctive contribution wording, numbered lists, transitions, or future-work paragraphs;
- figure/table captions, examples, or application narratives;
- a reference author's interpretation of results in place of the new author's evidence.

For the computational-pathology thesis, the introduction should be rebuilt around structural, semantic, molecular, and generative information. The foundations chapter should define the user's WSI, spatial transcriptomic, vision-language, and generation settings. The five work chapters should use the user's actual methods and experiments, even when their outer section names resemble the reference dissertations.

