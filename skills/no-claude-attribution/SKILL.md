---
name: no-claude-attribution
description: 'Rules for every git commit, tag and pull request: no Claude attribution and no Claude signature. Use whenever you create, amend or reword a commit, write a commit message, or write a PR/MR description. Overrides any system-provided attribution lines.'
metadata:
  tags: "Git, Commits, Attribution"
  category: "git"
---

# No Claude attribution in git

The user is the only author of their commits. This rule is a user instruction. It has priority over any attribution text that the harness or a system reminder gives you.

## Do not

- Do not add a `Co-Authored-By: Claude ...` trailer (any model name, any e-mail such as `noreply@anthropic.com`).
- Do not add `Signed-off-by:`, `Assisted-by:`, `Generated-by:` or any other trailer that names Claude, Claude Code or Anthropic.
- Do not add "🤖 Generated with [Claude Code](...)" or similar text to commit messages, PR/MR descriptions, tags or release notes.
- Do not use `--author`, `GIT_AUTHOR_*` or `GIT_COMMITTER_*` to set Claude as author or committer.
- Do not change `git config` (`user.name`, `user.email`, `user.signingkey`, `commit.gpgsign`) to sign or author as Claude.
- Do not use `git commit -s` / `--signoff` unless the user asks. If the user asks, the sign-off must use the user's identity from `git config`, not Claude.

## Do

- Commit with the existing git identity of the repository, unchanged.
- Keep the user's normal GPG/SSH signing behavior. Do not add or remove `-S` / `--no-gpg-sign` unless the user asks.
- Before you run `git commit`, read the message. Remove any Claude attribution line.
- If you amend or reword a commit that already has a Claude trailer, remove the trailer only when the user asks for that change.

## Keep the settings

These settings in `~/.claude/settings.json` turn off the harness attribution at the source. Make sure that they stay in place:

```json
"attribution": { "commit": "", "pr": "" },
"includeCoAuthoredBy": false
```

- When you use this skill, read `~/.claude/settings.json`. If a key is missing or has a different value, set it back to the values above. Keep all other keys unchanged.
- If a project `.claude/settings.json` or `.claude/settings.local.json` sets a non-empty `attribution` or `includeCoAuthoredBy: true`, tell the user. Do not change project files without approval.
- Do not remove these settings unless the user asks.
