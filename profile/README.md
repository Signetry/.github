<p align="center">
  <img src="profile/assets/mark.png" alt="Signetry" width="120" height="120"/>
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
# source-available (All Rights Reserved); installed from source, not PyPI
pip install "signetry-core @ git+https://github.com/Signetry/core@v0.6.0"
```

## Contributing

Signetry is **source-available** (All Rights Reserved, © 2026 Binay Dalai) — not open source.
Contributions are welcome under a **Contributor License Agreement**: you're credited, but gain
no ownership or right to use/sell it. See any repo's `CONTRIBUTING.md` and `CLA.md`.
