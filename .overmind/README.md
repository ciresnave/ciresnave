# `.overmind/` — OverMind settings for CireSnave

This folder holds settings that [OverMind](https://github.com/ciresnave/OverMind) reads for this
account. It follows OverMind's draft standard for app folders in a `<username>/<username>` repo
(`USER-REPO-APP-FOLDERS-SPEC.md` in OverMind). Nothing here affects this profile's README.

## Rules

- **Only CireSnave merges here, and his merge is the approval.** Agents have read access and propose
  changes from a fork. Each PR quotes his words verbatim.
- **No secrets, ever**: no passwords, tokens, keys, PINs or codes. A secret is never an approval.
- OverMind reads this folder from the default branch only. An open PR changes nothing.

## Contents

- `lane-restart/approvals/` — startup-dialog approvals for `lane-restart`, OverMind's session
  restart tool (OverMind `RESTART-TOOL-DESIGN.md` §12). Each `<id>.json` names one dialog, matched
  exactly, and the single keystroke that answers it. `lane-restart` finds this folder through
  `~/.overmind/lane-restart.json`:

  ```json
  { "approvals": { "repo": "ciresnave/ciresnave", "path": ".overmind/lane-restart/approvals" } }
  ```

  - `claude-peers-dev-channels.json` confirms the `--dangerously-load-development-channels` dialog
    for `server:claude-peers` only, on every lane, until 2027-03-19.
