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

_Seed migrations are tracked separately. The first skill subtrees will land in follow-up PRs._

When the migration is in progress, this section will list each migrated skill with a one-line description and a link to its subdirectory.

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
