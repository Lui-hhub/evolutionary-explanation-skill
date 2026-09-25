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

### Codex skill installer

Install directly from this GitHub repository with the Codex skill installer:

```bash
python3 ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo Lui-hhub/evolutionary-explanation-skill \
  --path .
```

Restart or start a new Codex session after installation so the skill is loaded.

### Manual installation

Clone the repository into the local skills directory:

```bash
git clone https://github.com/Lui-hhub/evolutionary-explanation-skill.git \
  ~/.codex/skills/evolutionary-explanation
```

The directory containing `SKILL.md` must be directly under the agent's skills directory. For a custom skills location, copy the repository there instead.

### Installing from a local checkout

If the repository is already cloned, copy it into the skills directory:

```bash
cp -R /path/to/evolutionary-explanation ~/.codex/skills/evolutionary-explanation
```

### Verifying the installation

Confirm that the skill file is present:

```bash
test -f ~/.codex/skills/evolutionary-explanation/SKILL.md && \
  echo "evolutionary-explanation is installed"
```

Then ask the agent to explain a complex topic, such as: `Explain how a frontend framework evolves from manual DOM updates.` The response should progress from a concrete problem through limitations and successive concepts.

For other agent runtimes that support `SKILL.md` files, install the `evolutionary-explanation` directory in that runtime's configured skills directory. With a GitHub-based installer, the repository and path are:

```text
Repository: Lui-hhub/evolutionary-explanation-skill
Path: .
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
