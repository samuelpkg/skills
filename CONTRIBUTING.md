# Contributing to samuelpkg/skills

This repo is the canonical home for skill-tier Samuel plugins (per [RFD 0012](https://github.com/samuelpkg/samuel/blob/main/docs/rfd/0012.md)). One repo, many subdirectories, one PR queue.

## Adding a new skill

1. **Pick a name.** Kebab-case, no `samuel-` prefix, unique across the registry. The name becomes both the subdirectory and the registry plugin name.
2. **Create the subtree.**
   ```text
   <skill-name>/
   ├── SKILL.md                 # required — the body the agent reads
   ├── samuel-plugin.toml       # required — the manifest
   ├── scripts/                 # optional — shell scripts the skill ships
   ├── references/              # optional — reference docs the skill points at
   └── assets/                  # optional — non-code resources
   ```
3. **Author the manifest.** Minimum shape:
   ```toml
   name = "<skill-name>"
   version = "1.0.0"
   kind = "skill"
   summary = "One-line description (≤80 chars)."

   [samuel]
   framework = "^2.0.0"
   protocol  = "^1.0.0"

   [provides]
   skills = ["<skill-name>"]

   [capabilities.filesystem]
   read  = ["/workspace"]
   write = []
   ```
   Full schema: see [`samuelpkg/samuel`/docs/plugin-authors/manifest.md](https://github.com/samuelpkg/samuel/blob/main/docs/plugin-authors/manifest.md).
4. **Open the PR.** Title: `Add skill: <name>`. CODEOWNERS routes review.
5. **After merge, register it.** Open a follow-up PR against [`samuelpkg/samuel-registry`](https://github.com/samuelpkg/samuel-registry) adding:
   ```toml
   [[plugins]]
   name        = "<skill-name>"
   repo        = "github.com/samuelpkg/skills"
   subpath     = "<skill-name>"
   latest      = "main"
   upstream    = true
   kind        = "skill"
   description = "One-line description."
   ```

## Editing an existing skill

PRs that touch one subpath are reviewed by that subpath's CODEOWNERS only. Cross-cutting changes (manifest schema bumps, capability-pattern updates) carry the top-level CODEOWNERS and require a maintainer review.

The registry installs the current `main` HEAD for every skill in this repo, so a merge is the release. There is no separate tag step.

## When NOT to use this repo

- **Your plugin needs versioned releases (`vX.Y.Z`).** The monorepo's tag namespace is shared; until [RFD 0012 §2c](https://github.com/samuelpkg/samuel/blob/main/docs/rfd/0012.md) lands a prefixed-tag convention, versioned skills belong in their own repo at `github.com/<owner>/samuel-<name>`.
- **Your plugin is wasm or oci tier.** Those keep per-repo hosting because the cosign identity pattern is per-repo. See the [plugin authors guide](https://github.com/samuelpkg/samuel/blob/main/docs/plugin-authors/index.md).
- **Your plugin needs a release workflow that signs artifacts.** Skills here ship as source-from-`main`; no signing pipeline runs. If you need signed artifacts, use a dedicated repo with [`samuelpkg/samuel-plugin-release`](https://github.com/samuelpkg/samuel-plugin-release).

## Code of conduct

Same as the framework — see [samuelpkg/samuel/CODE_OF_CONDUCT.md](https://github.com/samuelpkg/samuel/blob/main/CODE_OF_CONDUCT.md).
