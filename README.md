# Practical Lessons from Production AI

This presentation, "Practical Lessons from Production AI," provides a technical blueprint for moving beyond simple prompt engineering to robust systems engineering. It introduces the Solver-Checker Algorithm, a framework designed to manage the inherent "Plausibility Paradox" of Large Language Models (LLMs).

- [Practical Lessons from Production AI] (https://github.com/dwellman/AI/blob/main/Practical%20Lessons%20from%20Production%20AI.pdf)
- [VAWK Demo] (https://drive.google.com/file/d/18-zMEe3cm4t1P1UrEKhdkGRH2aByRlPi/view?usp=drive_link)
- [BUUI Adventure] (https://drive.google.com/file/d/1HJnNMo0YLnASPL-Dl3UzcEouwSrl-Z8G/view?usp=drive_link)

## Core Themes

- **The Plausibility Paradox**: LLMs are probabilistic engines optimized for fluent, plausible output rather than objective truth. Hallucination is viewed as a "feature" of this fluency, but becomes a "bug" (or "smudge") when it violates critical business logic or regulatory rules.


- **Visible vs. Invisible Ink**: "Visible Ink" represents the AI's fluent dialogue and tone, while "Invisible Ink" encompasses the underlying business logic, intent, and regulatory constraints that must govern that dialogue.

- **Epistemics vs. Governance**: The framework distinguishes between Epistemics—content that must be observationally true within a specific story or context—and Governance—outputs that must be factually accurate and verifiable through deterministic systems.

## Ideas Introduced

- **Visible Ink**: “The Surface”: What the AI says. It is the dialogue, the tone, and the fluency.

- **Invisible Ink**: “The Understructure or Armature”: The rules the AI must obey. It is the business logic, the regulatory rules, and your specific intent.

- **A Story**: Any process where the "Invisible Ink" (the story rules) must govern the "Visible Ink" (the output) to maintain trust and utility.

- **Execution Truth**: The "Ground Truth" or binary correctness. It is the verified proof—such as a successful compile or a validated state change—that ensures the Invisible Ink has been successfully defended.

- **A Smudge**: The “Plausibility Paradox” or "when is hallucination a bug or not a bug?" – When the Visible Ink (the plausible performance) bleeds through and overwrites the Invisible Ink (the story/business rules).

## The Solver-Checker Algorithm
The centerpiece of the presentation is a 5-pattern framework for building reliable AI boundaries:

- **Grounding**: establishing a shared language and anchoring outputs in a source of truth to avoid invented facts.

- **Orchestration**: coordinating multi-step procedures into a testable, debuggable sequence using state machines and controlled budgets.

- **Verification**: employing deterministic checks and external "judges" (like a compiler or interpreter) to ensure binary correctness.

- **Trust UX**: maintaining user control by making AI uncertainty explicit and providing verifiable "receipts" for decisions.

- **Compound Learning**: using offline evaluation harnesses and fixed test sets to drive continuous improvement without performance regression.

## Technical Demos ("Proof of Work")

The framework is demonstrated through two distinct open-source projects that utilize 1980s-era software rigor to govern modern AI:

- **VAWK (Coding/Execution Truth)**: A "vibe coding" tool that uses BNF (Backus-Naur Form) Grammars and a Python interpreter to verify that AI-generated code actually runs before it is presented to the user. [https://github.com/dwellman/vawk]

- **BUUI Adventure (Gaming/Narrative Truth)**: A text adventure engine where AI-driven narrative is constrained by a deterministic World-State and game engine rules to ensure story consistency. [https://github.com/dwellman/adventure]

## Suggested Reading
The presentation draws inspiration from three foundational texts that bridge the gap between human storytelling and software engineering:

- **Invisible Ink** by Brian McDonald (Narrative Philosophy) [https://a.co/d/8zIOQlJ]

- **The Mythical Man-Month** by Frederick Brooks Jr. (Systems Engineering) [https://a.co/d/4Rc07fg]

- **The Elements of Programming Style** by Kernighan & Plauger (Logic and Clarity) (Kernighan is the 'K' in VAWK) [https://a.co/d/35IA5ZW]

## Theoretical Frameworks as Position Papers:

- [Move 37](https://github.com/dwellman/AI/blob/main/papers/move-37.md): On the shift from truth to reward-seeking behavior.
  
- [The Dark Triad](https://github.com/dwellman/AI/blob/main/papers/dark-triad.md): Emergent behavioral risks in self-reinforcing models.

- [Artificial Empathy](https://github.com/dwellman/AI/blob/main/papers/artificial-empathy.md): Operationalizing ethics through system constraints.

## Organization
```
/
├── presentation.pdf        # The "Practical Lessons from Production AI" deck
├── papers/
│   ├── move-37.md          # Reward drift and plausibility thesis
│   ├── dark-triad.md       # Behavioral risks (Narcissism/Psychopathy)
│   └── artificial-empathy.md # Ethical alignment through constraints
├── demos/
│   ├── vawk/               # Vibe AWK coder implementation
│   └── adventure/          # BUUI Adventure implementation
└── README.md               # Summary of the "Five Patterns" and how they link the papers to the code
```

[ai-adoption-qa.md] (https://github.com/dwellman/AI/blob/main/ai-adoption-qa.md)
