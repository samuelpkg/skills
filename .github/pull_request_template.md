## Summary

<!-- One or two sentences. What changed and why. -->

## Affected skills

<!-- One subpath per line, e.g.:
- go-guide/
- typescript/
-->

## Checklist

- [ ] `samuel-plugin.toml` parses (TOML valid + required keys present: `name`, `version`, `kind`, `summary`).
- [ ] `SKILL.md` has YAML frontmatter with `name` matching the manifest.
- [ ] The subpath directory name matches the manifest `name`.
- [ ] If a new skill: a follow-up registry PR will land at [`samuelpkg/samuel-registry`](https://github.com/samuelpkg/samuel-registry) once this merges.
- [ ] If editing an existing skill: behavior change documented in the body of `SKILL.md`, not just in the PR.

## Registry follow-up

<!-- Link to the samuel-registry PR (or "N/A" if this is a refactor that doesn't change the registry surface). -->
