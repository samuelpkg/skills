# samuelpkg/skills

Canonical skill-tier monorepo for the [Samuel v2](https://github.com/samuelpkg/samuel) plugin ecosystem.

Each top-level subdirectory is one installable skill plugin; the public registry references them via `subpath = "<name>"`. The layout mirrors [`anthropics/skills`](https://github.com/anthropics/skills) — one repo, one PR queue, one place to land contributions.

The architectural rationale and the cut line versus per-repo hosting for wasm/oci tiers is documented in [RFD 0012](https://github.com/samuelpkg/samuel/blob/main/docs/rfd/0012.md).

## Install a skill

```sh
samuel install <skill-name>
```

`samuel install` resolves names through [`samuelpkg/samuel-registry`](https://github.com/samuelpkg/samuel-registry); the registry knows which entries are subpath-vendored here and clones only the relevant subtree.

## Skills index

| Name | Description |
| --- | --- |
| [`auto`](auto/) | Autonomous AI coding loop (Ralph Wiggum methodology). |
| [`cleanup-project`](cleanup-project/) | Project cleanup and pruning workflow. |
| [`code-review`](code-review/) | Pre-commit code quality review workflow. |
| [`commit-message`](commit-message/) | Generate descriptive commit messages by analyzing git diffs. |
| [`create-prd`](create-prd/) | Product Requirements Document (PRD) creation workflow. |
| [`create-rfd`](create-rfd/) | Request for Discussion (RFD) creation workflow. |
| [`create-skill`](create-skill/) | Agent Skill creation workflow. |
| [`dependency-update`](dependency-update/) | Safe dependency update workflow. |
| [`document-work`](document-work/) | Work documentation and pattern capture workflow. |
| [`generate-agents-md`](generate-agents-md/) | Cross-tool compatibility workflow. |
| [`generate-tasks`](generate-tasks/) | Task generation and breakdown workflow. |
| [`go-guide`](go-guide/) | Go language guardrails and patterns. |
| [`react`](react/) | React 18+ framework guardrails and patterns. |
| [`refactoring`](refactoring/) | Technical debt remediation and code restructuring workflow. |
| [`security-audit`](security-audit/) | Security assessment workflow. |
| [`sync-claude-md`](sync-claude-md/) | Sync per-folder CLAUDE.md and AGENTS.md files with context-aware content. |
| [`testing-strategy`](testing-strategy/) | Test planning and coverage strategy workflow. |
| [`troubleshooting`](troubleshooting/) | Debugging and problem-solving workflow. |

The table grows one row per migrated skill; the full plan for fanning out the remaining `samuelpkg/samuel-*` skill repos is tracked in [RFD 0012](https://github.com/samuelpkg/samuel/blob/main/docs/rfd/0012.md).

## Contributing a new skill

See [CONTRIBUTING.md](CONTRIBUTING.md) for the full workflow. The short version:

1. Create a top-level directory matching your skill's `name` (kebab-case).
2. Add `SKILL.md` (the human-and-agent-readable body) and `samuel-plugin.toml` (the manifest).
3. Open a PR. CODEOWNERS scopes review to the affected subpath.
4. After merge, open a second PR against [`samuelpkg/samuel-registry`](https://github.com/samuelpkg/samuel-registry) adding the registry entry.

## When this repo is wrong for your plugin

- **You need versioned releases.** The monorepo's tag namespace is shared; a skill that wants `vX.Y.Z` tagged releases belongs in its own repo until [RFD 0012 §2c](https://github.com/samuelpkg/samuel/blob/main/docs/rfd/0012.md) lands a prefixed-tag convention.
- **Your plugin is wasm or oci tier.** Those keep per-repo hosting to preserve the cosign identity boundary. See the [plugin authors guide](https://github.com/samuelpkg/samuel/blob/main/docs/plugin-authors/index.md) for the right scaffold.

## License

MIT — see [LICENSE](LICENSE). Plugins that vendor third-party content carry their own attribution in the subdirectory's `samuel-plugin.toml` `authors` field; the monorepo license covers Samuel-original contributions only.
