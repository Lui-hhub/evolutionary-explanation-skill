---
name: evolutionary-explanation
description: Use an evolutionary, progressive teaching method whenever the user asks to explain a complex concept, technical principle, architecture, algorithm, system, workflow, or design proposal, even if they do not use the phrase “evolutionary explanation.” Start with a concrete problem and the smallest workable solution, expose its limitations, then introduce only the next concept needed to overcome each limitation. Keep the explanation connected across layers, distinguish pedagogical reconstruction from real historical development, and adapt depth to the learner.
---

# Evolutionary Explanation

Help the reader build transferable understanding one layer at a time. Make complex material appear as a system that grows through successive fixes: first establish why the idea is needed, then explain how it works, and finally add formal definitions, boundaries, and engineering trade-offs.

## When to use

Use this method for complex concepts, technical principles, algorithms, protocols, system architectures, code designs, product proposals, process designs, and trade-off analysis. Do not force a complete progression onto a simple definition, fact lookup, or one-step operation.

## Core progression

First estimate the reader's background, goal, and desired depth. If the context is unclear, state a brief assumption and use a general technical-reader level.

Organize the explanation as a chain of usually 3–7 layers. Compress it for simple questions; branch or add layers for especially complex topics:

1. **Concrete problem:** Start with a realistic task, failure, or constraint. State the goal before introducing terminology.
2. **Smallest workable solution:** Give a simple model, rule, or implementation that the reader can run mentally. Keep it correct enough to support the next step without adding unrelated detail.
3. **Expose the limitation:** Use the same example or a harder input to show where the solution fails and why. Do not merely claim that it fails “at scale.”
4. **Introduce the next concept:** Add only what is needed to overcome the current limitation. Give intuition before mechanics; use pseudocode, equations, data flow, or a small diagram when useful.
5. **Continue the evolution:** Test the improved solution with the ongoing example. State what it fixes and what cost or new constraint it introduces.
6. **Assemble the full picture:** Once intuition is established, provide formal definitions, the complete flow, component relationships, boundaries, and common variants.
7. **Transfer and check:** Use a similar but different example, a short exercise, or a decision question to test understanding. Explain when another approach would be preferable.

At every layer answer three questions: What is the current solution? Which problem does it solve? Why is another layer still needed? Connect layers causally instead of presenting unrelated facts.

## Communication principles

- Carry one stable example through the explanation. If you change examples, explain how they map to each other.
- Explain a term in ordinary language before giving its name and formal definition.
- Separate the intuition model, teaching simplification, and strict fact. A pedagogical reconstruction is not a historical account; do not invent historical sequences or causal claims.
- For design proposals, connect requirements, constraints, candidate solutions, trade-offs, failure modes, and validation into one progression. Cover performance, reliability, complexity, maintainability, security, or cost when relevant.
- Use technical detail to improve understanding. Prefer small examples, tables, pseudocode, ASCII/Mermaid diagrams, and order-of-magnitude comparisons over unmotivated background.
- Do not start from an artificially primitive solution when the reader already knows the prerequisite. Say which layers are being skipped.

## Recommended output shape

Choose the headings naturally rather than forcing every section:

1. One-sentence intuition or map of the final idea
2. Problem context and goal
3. First, simplest solution
4. The example where it fails
5. The next layer introduced to fix that failure
6. One or more further evolutions
7. Complete model, formal terms, and boundaries
8. Trade-offs, when to use it, and a comprehension check

For a short answer, retain five steps: problem → simple solution → limitation → improvement → summary, with one or two sentences per step. For a deep answer, expand the internal mechanics of each evolution and state what capability has been gained at the end of each layer.

## Quality check

Before delivering, check:

- Can the reader understand the problem before encountering the terminology?
- Is every new concept motivated by a concrete limitation in the previous layer?
- Does one example carry the explanation, or is every transition explained?
- Are the conditions under which each simplification works and fails stated?
- Is pedagogical reconstruction clearly separated from real history?
- Does the reader understand the final solution's costs, boundaries, and alternatives?
