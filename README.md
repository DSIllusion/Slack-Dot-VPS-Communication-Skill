# Slack Dot VPS Communication Skill

A Codex skill for setting up or moving an authorized Slack browser workflow on a Linux VPS. It helps send a user-approved message to the user's own Dot conversation and verify whether Dot replied in the original thread.

## What it covers

- Set up a dedicated Linux browser profile and sign in interactively through a temporary, SSH-forwarded desktop.
- Use Playwright with that profile for a headless test. A fresh reference number distinguishes a successful reply from a message that was only delivered.
- Recover an expired session, check for duplicate sends, and confirm a replacement host works before switching.

This is a browser workflow, not an official Dot API. A successful Slack send does not guarantee a Dot reply. The repository includes no credentials or browser data. Do not commit Slack tokens, cookies, SSH keys, or browser profiles.

## Install in Codex

Clone this repository on the machine running Codex. From the repository root, run:

```bash
mkdir -p ~/.agents/skills
cp -R slack-dot-vps ~/.agents/skills/
```

The skill lives on the Codex machine; the browser it configures runs on the target Linux VPS. If you already have a copy installed, compare it before replacing it.

## Use it

> Use $slack-dot-vps to check the designated Linux VPS. Start with read-only checks. Do not send a Slack test message until I approve the conversation and test text.

See [the full skill](slack-dot-vps/SKILL.md).
