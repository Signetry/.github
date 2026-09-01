<p align="center">
  <img src="https://raw.githubusercontent.com/Signetry/.github/main/profile/assets/mark.png" alt="Signetry" width="120" height="120"/>
</p>

<h1 align="center">Signetry</h1>

<p align="center"><em>Seal every agent's PR with proof — earned authority in a signed receipt.</em></p>

---

**Signetry is a change-control plane for coding agents.** Any agent (Claude Code, Codex,
Cursor, Copilot, Devin — or a human) may *propose* a change; only Signetry decides how much
authority that change **earned**, and seals the verdict in an Ed25519-signed receipt.

For every change it runs one deterministic pipeline:

```
executable contract  →  untrusted-text quarantine  →  required checks  →
independent verifier  →  earned authority (0/1/2)  →  Ed25519-signed receipt
```

A coding agent cannot approve its own authority to make a change. The patch-writer is never
the patch-approver. `auto_merge` is always false — a human merges.

## Start here

| Repo | What it is |
|---|---|
| [**signetry**](https://github.com/Signetry/signetry) | The overview / front door — architecture, integrations, compatibility |
| [**core**](https://github.com/Signetry/core) | The governance kernel (`signetry-core`, the `signetry` CLI) |
| [**action**](https://github.com/Signetry/action) | **Signetry Admission** — govern every PR on the GitHub Marketplace |
| [**reviewer**](https://github.com/Signetry/reviewer) | Advisory PR reviewer with a deterministic merge-safety gate |
| [**eval**](https://github.com/Signetry/eval) | Public adversarial benchmark (attack-success-rate + utility) |
| [**plugins**](https://github.com/Signetry/plugins) · [claude-code](https://github.com/Signetry/claude-code) · [codex](https://github.com/Signetry/codex) · [cursor](https://github.com/Signetry/cursor) · [precommit](https://github.com/Signetry/precommit) | Editor / agent / hook integrations |

## Install

```bash
# open core: integrations Apache-2.0, engine BUSL-1.1; installed from source, not PyPI
pip install "signetry-core @ git+https://github.com/Signetry/core@v0.7.0"
```

## Licensing — open core

**Every surface you integrate with is [Apache-2.0](https://www.apache.org/licenses/LICENSE-2.0):**
`action`, `plugins`, `claude-code`, `codex`, `cursor`, `precommit`, `reviewer`, `eval`, the
`github-app`, and the `signetry` overview. Fork them, vendor them, ship them in a product.

**The governance kernel ([`core`](https://github.com/Signetry/core)) is source-available under
[BUSL-1.1](https://github.com/Signetry/core/blob/main/LICENSE)** and converts to Apache-2.0 on
**2030-08-31**. Read it, run it in production on your own repositories, fork it, patch it. The
one prohibition is reselling it as a competing hosted governance service. Every release carries
its own four-year clock.

Full table: **[LICENSING.md](https://github.com/Signetry/signetry/blob/main/LICENSING.md)**. If a
public repository here has no `LICENSE` file, that is a bug — open an issue.

## Contributing

Start with the [Agent Governance Leaderboard](https://github.com/Signetry/eval/blob/main/docs/LEADERBOARD.md)
if you want the shortest path to something visible: it takes submissions from *any* governance
system, including ones that beat Signetry. A leaderboard only its author can win is marketing,
and everyone can tell. See [SUBMITTING.md](https://github.com/Signetry/eval/blob/main/docs/SUBMITTING.md).

Otherwise: `eval` wants adversarial cases that get past the kernel, `core` wants detection rules
and receipt-verification hardening, and the integration repos want whatever breaks in your editor.
Each repo has its own `CONTRIBUTING.md`.

Contributions are accepted under a **[Contributor License Agreement](https://github.com/Signetry/signetry/blob/main/CLA.md)** — because code
legitimately moves across the open-core licence line, and the CLA is what lets it move without
tracking down every past contributor. It takes nothing from you: you keep the same Apache-2.0
rights as every other user, you keep the right to use your own work elsewhere, and you are
credited in `CONTRIBUTORS.md`, the Git history, and release notes.
