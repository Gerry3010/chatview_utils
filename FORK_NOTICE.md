# ⚠️ AI-agent-maintained fork

Fork of [`chatview_utils`](https://github.com/SimformSolutionsPvtLtd/chatview_utils)
(MIT) maintained for the **Chattr** app, alongside the sibling
[chatview fork](https://github.com/Gerry3010/chatview).

- **Maintenance:** auto-synced with upstream **weekly**, kept current on a
  **best-effort basis by an AI agent**; patches at the agent's best judgement,
  **no warranty**.
- **Upstream (file issues/PRs there):** https://github.com/SimformSolutionsPvtLtd/chatview_utils
- **Integration branch:** `chattr` (patches on top of an upstream release tag).

Chattr-specific changes on top of upstream `3.1.0` (branch `chattr`):

- **`ChatController.getUserFromId` null-guard** — tag `chattr-3.1.0-p1`. Returns
  a **fallback `ChatUser`** for unknown ids instead of **throwing** — an unknown
  sender/reactor id no longer crashes the whole message-list render.
  `src/controller/chat_controller.dart`.
- **`ChatController.updateMessage` no-op + `removeMessage`** — tag
  `chattr-3.1.0-p2`. `updateMessage` is a no-op for an unknown message id
  (upstream threw `Message Not Found!`); adds a `removeMessage(id)` API that
  removes a message and re-emits the stream. `src/controller/chat_controller.dart`.

Manual patches are tagged `chattr-3.1.0-pN`; the weekly auto-sync re-tags as
`chattr-<upstream-version>` after rebasing onto a new upstream release.
