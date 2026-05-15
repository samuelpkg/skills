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
| [`actix-web`](actix-web/) | Actix-web framework guardrails, patterns, and best practices for AI-assisted development. |
| [`android-compose`](android-compose/) | Jetpack Compose framework guardrails, patterns, and best practices for AI-assisted development. |
| [`aspnet-core`](aspnet-core/) | ASP.NET Core framework guardrails, patterns, and best practices for AI-assisted development. |
| [`assembly-guide`](assembly-guide/) | Assembly language guardrails, patterns, and best practices for AI-assisted development. |
| [`auto`](auto/) | Autonomous AI coding loop (Ralph Wiggum methodology). |
| [`axum`](axum/) | Axum framework guardrails, patterns, and best practices for AI-assisted development. |
| [`blazor`](blazor/) | Blazor framework guardrails, patterns, and best practices for AI-assisted development. |
| [`cleanup-project`](cleanup-project/) | Project cleanup and pruning workflow. |
| [`code-review`](code-review/) | Pre-commit code quality review workflow. |
| [`commit-message`](commit-message/) | Generate descriptive commit messages by analyzing git diffs. |
| [`cpp-guide`](cpp-guide/) | C/C++ language guardrails, patterns, and best practices for AI-assisted development. |
| [`create-prd`](create-prd/) | Product Requirements Document (PRD) creation workflow. |
| [`create-rfd`](create-rfd/) | Request for Discussion (RFD) creation workflow. |
| [`create-skill`](create-skill/) | Agent Skill creation workflow. |
| [`csharp-guide`](csharp-guide/) | C# language guardrails, patterns, and best practices for AI-assisted development. |
| [`cuda-guide`](cuda-guide/) | CUDA/GPU computing guardrails, patterns, and best practices for AI-assisted development. |
| [`dart-frog`](dart-frog/) | Dart Frog framework guardrails, patterns, and best practices for AI-assisted development. |
| [`dart-guide`](dart-guide/) | Dart language guardrails, patterns, and best practices for AI-assisted development. |
| [`dependency-update`](dependency-update/) | Safe dependency update workflow. |
| [`django`](django/) | Django 5+ framework guardrails, patterns, and best practices for AI-assisted development. |
| [`document-work`](document-work/) | Work documentation and pattern capture workflow. |
| [`echo`](echo/) | Echo framework guardrails, patterns, and best practices for AI-assisted development. |
| [`express`](express/) | Express.js framework guardrails, patterns, and best practices for AI-assisted development. |
| [`fastapi`](fastapi/) | FastAPI framework guardrails, patterns, and best practices for AI-assisted development. |
| [`fiber`](fiber/) | Fiber framework guardrails, patterns, and best practices for AI-assisted development. |
| [`flask`](flask/) | Flask framework guardrails, patterns, and best practices for AI-assisted development. |
| [`flutter`](flutter/) | Flutter framework guardrails, patterns, and best practices for AI-assisted development. |
| [`generate-agents-md`](generate-agents-md/) | Cross-tool compatibility workflow. |
| [`generate-tasks`](generate-tasks/) | Task generation and breakdown workflow. |
| [`gin`](gin/) | Gin framework guardrails, patterns, and best practices for AI-assisted development. |
| [`go-guide`](go-guide/) | Go language guardrails, patterns, and best practices for AI-assisted development. |
| [`hanami`](hanami/) | Hanami 2+ framework guardrails, patterns, and best practices for AI-assisted development. |
| [`html-css-guide`](html-css-guide/) | HTML and CSS guardrails, patterns, and best practices for AI-assisted development. |
| [`java-guide`](java-guide/) | Java language guardrails, patterns, and best practices for AI-assisted development. |
| [`kotlin-guide`](kotlin-guide/) | Kotlin language guardrails, patterns, and best practices for AI-assisted development. |
| [`ktor`](ktor/) | Ktor framework guardrails, patterns, and best practices for AI-assisted development. |
| [`laravel`](laravel/) | Laravel 11+ framework guardrails, patterns, and best practices for AI-assisted development. |
| [`lua-guide`](lua-guide/) | Lua language guardrails, patterns, and best practices for AI-assisted development. |
| [`micronaut`](micronaut/) | Micronaut framework guardrails, patterns, and best practices for AI-assisted development. |
| [`nextjs`](nextjs/) | Next.js 14+ framework guardrails, patterns, and best practices for AI-assisted development. |
| [`php-guide`](php-guide/) | PHP language guardrails, patterns, and best practices for AI-assisted development. |
| [`python-guide`](python-guide/) | Python guardrails, patterns, and best practices for AI-assisted development. |
| [`quarkus`](quarkus/) | Quarkus framework guardrails, patterns, and best practices for AI-assisted development. |
| [`r-guide`](r-guide/) | R language guardrails, patterns, and best practices for AI-assisted development. |
| [`rails`](rails/) | Rails 7+ framework guardrails, patterns, and best practices for AI-assisted development. |
| [`react`](react/) | React 18+ framework guardrails, patterns, and best practices for AI-assisted development. |
| [`refactoring`](refactoring/) | Technical debt remediation and code restructuring workflow. |
| [`rocket`](rocket/) | Rocket framework guardrails, patterns, and best practices for AI-assisted development. |
| [`ruby-guide`](ruby-guide/) | Ruby language guardrails, patterns, and best practices for AI-assisted development. |
| [`rust-guide`](rust-guide/) | Rust guardrails, patterns, and best practices for AI-assisted development. |
| [`security-audit`](security-audit/) | Security assessment workflow. |
| [`shelf`](shelf/) | Shelf framework guardrails, patterns, and best practices for AI-assisted development. |
| [`shell-guide`](shell-guide/) | Shell/Bash scripting guardrails, patterns, and best practices for AI-assisted development. |
| [`sinatra`](sinatra/) | Sinatra framework guardrails, patterns, and best practices for AI-assisted development. |
| [`solidity-guide`](solidity-guide/) | Solidity/Ethereum guardrails, patterns, and best practices for AI-assisted development. |
| [`spring-boot-java`](spring-boot-java/) | Spring Boot (Java) framework guardrails, patterns, and best practices. |
| [`spring-boot-kotlin`](spring-boot-kotlin/) | Spring Boot with Kotlin framework guardrails, patterns, and best practices. |
| [`sql-guide`](sql-guide/) | SQL language guardrails, patterns, and best practices for AI-assisted development. |
| [`swift-guide`](swift-guide/) | Swift language guardrails, patterns, and best practices for AI-assisted development. |
| [`swiftui`](swiftui/) | SwiftUI framework guardrails, patterns, and best practices for AI-assisted development. |
| [`symfony`](symfony/) | Symfony 7+ framework guardrails, patterns, and best practices for AI-assisted development. |
| [`sync-claude-md`](sync-claude-md/) | Sync per-folder CLAUDE.md and AGENTS.md files with context-aware content. |
| [`testing-strategy`](testing-strategy/) | Test planning and coverage strategy workflow. |
| [`troubleshooting`](troubleshooting/) | Debugging and problem-solving workflow. |
| [`typescript-guide`](typescript-guide/) | TypeScript/JavaScript guardrails, patterns, and best practices for AI-assisted development. |
| [`uikit`](uikit/) | UIKit framework guardrails, patterns, and best practices for AI-assisted development. |
| [`unity`](unity/) | Unity game engine guardrails, patterns, and best practices for AI-assisted development. |
| [`vapor`](vapor/) | Vapor framework guardrails, patterns, and best practices for AI-assisted development. |
| [`wordpress`](wordpress/) | WordPress framework guardrails, patterns, and best practices for AI-assisted development. |
| [`zig-guide`](zig-guide/) | Zig language guardrails, patterns, and best practices for AI-assisted development. |
||||||| c5a1062
| [`auto`](auto/) | Autonomous AI coding loop (Ralph Wiggum methodology). |
| [`cleanup-project`](cleanup-project/) | Project cleanup and pruning workflow. |
| [`code-review`](code-review/) | Pre-commit code quality review workflow. |
| [`commit-message`](commit-message/) | Generate descriptive commit messages by analyzing git diffs. |
| [`cpp-guide`](cpp-guide/) | C/C++ language guardrails, patterns, and best practices for AI-assisted development. |
| [`create-prd`](create-prd/) | Product Requirements Document (PRD) creation workflow. |
| [`create-rfd`](create-rfd/) | Request for Discussion (RFD) creation workflow. |
| [`create-skill`](create-skill/) | Agent Skill creation workflow. |
| [`csharp-guide`](csharp-guide/) | C# language guardrails, patterns, and best practices for AI-assisted development. |
| [`cuda-guide`](cuda-guide/) | CUDA/GPU computing guardrails, patterns, and best practices for AI-assisted development. |
| [`dart-guide`](dart-guide/) | Dart language guardrails, patterns, and best practices for AI-assisted development. |
| [`dependency-update`](dependency-update/) | Safe dependency update workflow. |
| [`document-work`](document-work/) | Work documentation and pattern capture workflow. |
| [`generate-agents-md`](generate-agents-md/) | Cross-tool compatibility workflow. |
| [`generate-tasks`](generate-tasks/) | Task generation and breakdown workflow. |
| [`go-guide`](go-guide/) | Go language guardrails, patterns, and best practices for AI-assisted development. |
| [`html-css-guide`](html-css-guide/) | HTML and CSS guardrails, patterns, and best practices for AI-assisted development. |
| [`java-guide`](java-guide/) | Java language guardrails, patterns, and best practices for AI-assisted development. |
| [`kotlin-guide`](kotlin-guide/) | Kotlin language guardrails, patterns, and best practices for AI-assisted development. |
| [`lua-guide`](lua-guide/) | Lua language guardrails, patterns, and best practices for AI-assisted development. |
| [`php-guide`](php-guide/) | PHP language guardrails, patterns, and best practices for AI-assisted development. |
| [`python-guide`](python-guide/) | Python guardrails, patterns, and best practices for AI-assisted development. |
| [`r-guide`](r-guide/) | R language guardrails, patterns, and best practices for AI-assisted development. |
| [`react`](react/) | React 18+ framework guardrails, patterns, and best practices for AI-assisted development. |
| [`refactoring`](refactoring/) | Technical debt remediation and code restructuring workflow. |
| [`ruby-guide`](ruby-guide/) | Ruby language guardrails, patterns, and best practices for AI-assisted development. |
| [`rust-guide`](rust-guide/) | Rust guardrails, patterns, and best practices for AI-assisted development. |
| [`security-audit`](security-audit/) | Security assessment workflow. |
| [`shell-guide`](shell-guide/) | Shell/Bash scripting guardrails, patterns, and best practices for AI-assisted development. |
| [`solidity-guide`](solidity-guide/) | Solidity/Ethereum guardrails, patterns, and best practices for AI-assisted development. |
| [`sql-guide`](sql-guide/) | SQL language guardrails, patterns, and best practices for AI-assisted development. |
| [`swift-guide`](swift-guide/) | Swift language guardrails, patterns, and best practices for AI-assisted development. |
| [`sync-claude-md`](sync-claude-md/) | Sync per-folder CLAUDE.md and AGENTS.md files with context-aware content. |
| [`testing-strategy`](testing-strategy/) | Test planning and coverage strategy workflow. |
| [`troubleshooting`](troubleshooting/) | Debugging and problem-solving workflow. |
| [`typescript-guide`](typescript-guide/) | TypeScript/JavaScript guardrails, patterns, and best practices for AI-assisted development. |
| [`zig-guide`](zig-guide/) | Zig language guardrails, patterns, and best practices for AI-assisted development. |
||||||| 53fee40
| [`assembly-guide`](assembly-guide/) | Assembly language guardrails, patterns, and best practices for AI-assisted development. |
| [`cpp-guide`](cpp-guide/) | C/C++ language guardrails, patterns, and best practices for AI-assisted development. |
| [`csharp-guide`](csharp-guide/) | C# language guardrails, patterns, and best practices for AI-assisted development. |
| [`cuda-guide`](cuda-guide/) | CUDA/GPU computing guardrails, patterns, and best practices for AI-assisted development. |
| [`dart-frog`](dart-frog/) | Dart Frog framework guardrails, patterns, and best practices for AI-assisted development. |
| [`dart-guide`](dart-guide/) | Dart language guardrails, patterns, and best practices for AI-assisted development. |
| [`django`](django/) | Django 5+ framework guardrails, patterns, and best practices for AI-assisted development. |
| [`echo`](echo/) | Echo framework guardrails, patterns, and best practices for AI-assisted development. |
| [`express`](express/) | Express.js framework guardrails, patterns, and best practices for AI-assisted development. |
| [`fastapi`](fastapi/) | FastAPI framework guardrails, patterns, and best practices for AI-assisted development. |
| [`fiber`](fiber/) | Fiber framework guardrails, patterns, and best practices for AI-assisted development. |
| [`flask`](flask/) | Flask framework guardrails, patterns, and best practices for AI-assisted development. |
| [`flutter`](flutter/) | Flutter framework guardrails, patterns, and best practices for AI-assisted development. |
| [`gin`](gin/) | Gin framework guardrails, patterns, and best practices for AI-assisted development. |
| [`go-guide`](go-guide/) | Go language guardrails, patterns, and best practices for AI-assisted development. |
| [`hanami`](hanami/) | Hanami 2+ framework guardrails, patterns, and best practices for AI-assisted development. |
| [`html-css-guide`](html-css-guide/) | HTML and CSS guardrails, patterns, and best practices for AI-assisted development. |
| [`java-guide`](java-guide/) | Java language guardrails, patterns, and best practices for AI-assisted development. |
| [`kotlin-guide`](kotlin-guide/) | Kotlin language guardrails, patterns, and best practices for AI-assisted development. |
| [`ktor`](ktor/) | Ktor framework guardrails, patterns, and best practices for AI-assisted development. |
| [`laravel`](laravel/) | Laravel 11+ framework guardrails, patterns, and best practices for AI-assisted development. |
| [`lua-guide`](lua-guide/) | Lua language guardrails, patterns, and best practices for AI-assisted development. |
| [`micronaut`](micronaut/) | Micronaut framework guardrails, patterns, and best practices for AI-assisted development. |
| [`nextjs`](nextjs/) | Next.js 14+ framework guardrails, patterns, and best practices for AI-assisted development. |
| [`php-guide`](php-guide/) | PHP language guardrails, patterns, and best practices for AI-assisted development. |
| [`python-guide`](python-guide/) | Python guardrails, patterns, and best practices for AI-assisted development. |
| [`quarkus`](quarkus/) | Quarkus framework guardrails, patterns, and best practices for AI-assisted development. |
| [`r-guide`](r-guide/) | R language guardrails, patterns, and best practices for AI-assisted development. |
| [`rails`](rails/) | Rails 7+ framework guardrails, patterns, and best practices for AI-assisted development. |
| [`react`](react/) | React 18+ framework guardrails, patterns, and best practices for AI-assisted development. |
| [`rocket`](rocket/) | Rocket framework guardrails, patterns, and best practices for AI-assisted development. |
||||||| c5a1062
| [`react`](react/) | React 18+ framework guardrails and patterns. |
| [`react`](react/) | React 18+ framework guardrails and patterns. |
| [`refactoring`](refactoring/) | Technical debt remediation and code restructuring workflow. |
| [`security-audit`](security-audit/) | Security assessment workflow. |
| [`sync-claude-md`](sync-claude-md/) | Sync per-folder CLAUDE.md and AGENTS.md files with context-aware content. |
| [`testing-strategy`](testing-strategy/) | Test planning and coverage strategy workflow. |
| [`troubleshooting`](troubleshooting/) | Debugging and problem-solving workflow. |
||||||| 53fee40
| [`ruby-guide`](ruby-guide/) | Ruby language guardrails, patterns, and best practices for AI-assisted development. |
| [`rust-guide`](rust-guide/) | Rust guardrails, patterns, and best practices for AI-assisted development. |
| [`shelf`](shelf/) | Shelf framework guardrails, patterns, and best practices for AI-assisted development. |
| [`shell-guide`](shell-guide/) | Shell/Bash scripting guardrails, patterns, and best practices for AI-assisted development. |
| [`sinatra`](sinatra/) | Sinatra framework guardrails, patterns, and best practices for AI-assisted development. |
| [`solidity-guide`](solidity-guide/) | Solidity/Ethereum guardrails, patterns, and best practices for AI-assisted development. |
| [`spring-boot-java`](spring-boot-java/) | Spring Boot (Java) framework guardrails, patterns, and best practices. |
| [`spring-boot-kotlin`](spring-boot-kotlin/) | Spring Boot with Kotlin framework guardrails, patterns, and best practices. |
| [`sql-guide`](sql-guide/) | SQL language guardrails, patterns, and best practices for AI-assisted development. |
| [`swift-guide`](swift-guide/) | Swift language guardrails, patterns, and best practices for AI-assisted development. |
| [`swiftui`](swiftui/) | SwiftUI framework guardrails, patterns, and best practices for AI-assisted development. |
| [`symfony`](symfony/) | Symfony 7+ framework guardrails, patterns, and best practices for AI-assisted development. |
| [`typescript-guide`](typescript-guide/) | TypeScript/JavaScript guardrails, patterns, and best practices for AI-assisted development. |
| [`uikit`](uikit/) | UIKit framework guardrails, patterns, and best practices for AI-assisted development. |
| [`unity`](unity/) | Unity game engine guardrails, patterns, and best practices for AI-assisted development. |
| [`vapor`](vapor/) | Vapor framework guardrails, patterns, and best practices for AI-assisted development. |
| [`wordpress`](wordpress/) | WordPress framework guardrails, patterns, and best practices for AI-assisted development. |
| [`zig-guide`](zig-guide/) | Zig language guardrails, patterns, and best practices for AI-assisted development. |

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
