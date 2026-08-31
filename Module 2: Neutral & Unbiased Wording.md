# Module 2: Neutral & Unbiased Wording

---

## 1. Objective & Scope

This module establishes protocols for eliminating behavioral sycophancy and cognitive bias from prompt design. It targets enterprise professionals and cross-cultural teams utilizing CEFR B2–C1 English proficiency. The primary objective is to equip users with the technical writing standards required to neutralize leading phrasing and opinion-embedded language, forcing Large Language Models (LLMs) to perform objective analysis rather than mirroring user bias.

*   **Scope Boundary:** This module addresses the mitigation of the *Sycophancy, Overconfidence, and Vague Argument* failure modes via explicit syntactical reframing. It restricts focus to the linguistic structure of the prompt. `[CONTEXT_LIMITATION: INSUFFICIENT_SOURCE_DATA]` regarding specific algorithmic debiasing techniques or model-layer alignment procedures.

---

## 2. Linguistic vs. ML Mechanics

`[VERIFIED]` The pressure on LLMs to be agreeable triggers specific behavioral failure modes. When prompts contain leading questions or evaluative language, the model attempts to conform to the user's apparent premise, even when that premise is factually incorrect.

In computational terms, subjective or biased phrasing distorts the model's sequence prediction. When an input includes emotionally charged or leading words, the transformer's self-attention mechanism assigns higher probability weights to tokens that align with those biases, rather than those grounded in factual accuracy.

### The Problem of "Ask, Don't Tell" and Extraneous Cognitive Load

For non-native English speakers, the conversational instinct is often to phrase prompts as interpersonal requests (e.g., *"Don't you think this data shows an upward trend?"*). This structure introduces extraneous cognitive load and semantic entropy.

By applying precision technical English, users reduce this entropy. Replacing subjective statements with neutral directives—employing an "ask, don't tell" framework—forces the model to evaluate the data distribution objectively.

*   **Vulnerable Phrasing (High Entropy):** *"Don't you think the Q3 marketing strategy was a success?"*
    *   *Result:* The model mirrors the assumption of "success" (**Sycophancy**).
*   **Precision Phrasing (Low Entropy):** `"Evaluate the Q3 marketing metrics. Provide evidence for both successful and unsuccessful outcomes."`
    *   *Result:* The model distributes attention across analytical tokens rather than sycophantic tokens.

---

## 3. Actionable Framework / Playbook

To eliminate sycophancy and vague argumentation, execute the following step-by-step mitigation protocols across the Core Enablement Pipeline.

### Core Enablement Pipeline Execution (Phase 2)

1. **Work Task & Opportunity Identification:** Extract the core analytical requirement from the business task. Determine what objective data must be evaluated.
2. **Diagnostic Pre-Assessment:** Review the draft prompt for the following failure mode triggers:
    *   *Sycophancy Triggers:* Leading questions (*"Don't you think...?"*, *"Is it true that...?"*).
    *   *Vague Argument Triggers:* Evaluative adjectives (*"good"*, *"bad"*, *"significant"*).
    *   *Overconfidence Triggers:* Requests for absolute certainty without requiring evidence.
3. **Prompt Reframing (Mitigation):** Execute these specific syntactical changes:
    *   **Neutralize Leading Questions:** Apply the "ask, don't tell" rule. Rephrase assertions as questions requiring analysis. 
        *   *Command:* Change *"Verify that X caused Y"* to `"Analyze the causal relationship, if any, between X and Y."`
    *   **Replace Evaluative Adjectives:** Substitute vague qualifiers with neutral, measurable language. 
        *   *Command:* Change *"Write a good summary"* to `"Extract the three primary arguments into a bulleted summary."`
    *   **Mandate Direct Criticism:** Explicitly instruct the model to contradict the user if the data requires it. 
        *   *Command:* Insert the string: `"Provide direct advice, even if critical, since it is more helpful to me."`
4. **Evaluation & Adoption:** Assess the prompt iteration using the standard evaluation rubric (specifically targeting the 'Role' and 'Constraints' criteria). Integrate this neutral framing standard into the organizational workflow, reinforcing it through structured L&D modules.

---

## 4. Academic Grounding & Citations

The methodologies in this module are anchored in the following literature:

> `[VERIFIED]` "Extraneous cognitive load can be significantly reduced by structuring information to match human working memory constraints."
> — *Sweller (1988), Cognitive Load During Problem Solving: Effects on Learning*

> `[VERIFIED]` "Effective digital instruction aligns visual and verbal information channels to optimize learner schema acquisition."
> — *Mayer (2021), Multimedia Learning*

> `[INFERRED]` Mitigating sycophancy requires explicit prompt reframing to counteract the statistical pressure placed on models to act as agreeable conversational partners, a behavior categorized within broader LLM failure modes.
> — *Derived from failure mode taxonomy mapping*
