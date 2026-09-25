# Evolutionary Explanation

An agent skill for explaining complex concepts, technical principles, architectures, algorithms, systems, workflows, and design proposals progressively.

The method starts with a concrete problem and the smallest workable solution. It then exposes that solution's limitations and introduces only the next concept needed to address each limitation. The explanation ends with the complete model, trade-offs, boundaries, and a comprehension check.

## What it is good for

- Explaining technical concepts without starting with a wall of terminology
- Teaching system architecture and design decisions
- Introducing algorithms through progressively stronger solutions
- Comparing tools or approaches through explicit constraints and trade-offs
- Building explanations that remain connected to one stable example

## Repository layout

```text
evolutionary-explanation/
├── SKILL.md
├── README.md
├── LICENSE
├── examples/
│   └── frontend-frameworks.md
└── evals/
    └── evals.json
```

## Installation

Install the `evolutionary-explanation` directory as a skill in an agent environment that supports `SKILL.md` files. With the Codex skill installer, use the GitHub repository and this directory path:

```text
Repository: <owner>/<repository>
Path: evolutionary-explanation
```

The packaged `evolutionary-explanation.skill` file can also be distributed as a standalone archive when supported by the host environment.

## Expected behavior

For a complex request, the agent should generally follow this progression:

```text
concrete problem
    -> smallest workable solution
    -> limitation or failure
    -> next concept that fixes it
    -> further evolution
    -> complete model and trade-offs
```

The skill distinguishes a teaching reconstruction from a claim about the actual historical development of a technology.

## License

MIT. See [LICENSE](LICENSE).
