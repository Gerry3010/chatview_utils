# ⚠️ AI-agent-maintained fork

Fork of [`chatview_utils`](https://github.com/SimformSolutionsPvtLtd/chatview_utils)
(MIT) maintained for the **Chattr** app, alongside the sibling
[chatview fork](https://github.com/Gerry3010/chatview).

- **Maintenance:** auto-synced with upstream **weekly**, kept current on a
  **best-effort basis by an AI agent**; patches at the agent's best judgement,
  **no warranty**.
- **Upstream (file issues/PRs there):** https://github.com/SimformSolutionsPvtLtd/chatview_utils
- **Integration branch:** `chattr` (patches on top of an upstream release tag).

Chattr-specific changes on top of upstream `3.1.0`:
- `ChatController.getUserFromId` returns a **fallback ChatUser** for unknown ids
  instead of **throwing** — an unknown sender/reactor id no longer crashes the
  whole message-list render.
