# matsengrp agents for Codex

This repository contains Codex custom agents adapted from the Claude Code subagents originally created by Erick Matsen.

The Codex-compatible agent definitions live in `.codex/agents/`. For convenience, the same agents are also installed into `~/.codex/agents/` so they can be reused from other projects.

The conversion follows the OpenAI Codex custom agents documentation:
- Project-scoped agents: `.codex/agents/*.toml`
- Global agents: `~/.codex/agents/*.toml`

## Example Uses

Use `/agents` inside Codex to inspect available custom agents, then ask Codex to delegate to one of them.

```text
Use the topic-sentence-stickler agent to review main.tex.
```

```text
Use the clean-code-reviewer agent to review the current PR, limiting scope to changed files.
```

```text
Use the pdf-question-answerer agent to read Koenig2017.pdf and explain how they determined antibody binding affinity.
```

## Available Agents

- **antipattern-scanner** - Detects architectural antipatterns and focused clean-code violations
- **clean-code-reviewer** - Performs strict code review with an emphasis on clean code and maintainability
- **code-smell-detector** - Gives gentle, mentoring feedback on semantic code smells and readability
- **journal-submission-checker** - Runs final manuscript checks on repositories, citations, and submission readiness
- **math-pr-summarizer** - Writes mathematical summaries for pull requests with statistical or computational work
- **pdf-proof-reader** - Proofreads academic PDF page proofs for typos and grammar issues only
- **pdf-question-answerer** - Extracts and explains findings from scientific PDFs
- **scientific-tex-editor** - Edits scientific LaTeX writing using Matsen-style guidance
- **snakemake-pipeline-expert** - Reviews and improves Snakemake workflows and project structure
- **tex-grammar-checker** - Performs meticulous grammar review for TeX and LaTeX documents
- **tex-verb-tense-checker** - Checks tense usage in scientific LaTeX writing
- **topic-sentence-stickler** - Strengthens paragraph structure through better topic sentences

## Notes

Agents that analyze PDFs still depend on [pdf-navigator-mcp](https://github.com/matsengrp/pdf-navigator-mcp).

The original Claude-style Markdown agent files are kept in this repository as source material for the Codex TOML versions.
