# PocketList: instructions for Codex

## Start each session
- Read docs/codex/LEARNING.md and README.md before suggesting work. Paths in
  these instructions are relative to the repository root unless stated otherwise.
- Check relevant files against the handoff; do not assume planned steps happened.
- Continue from the recorded next step unless the learner changes direction.

## Teaching and permissions
- Never create, amend, or rewrite Git commits. The learner performs all commits.
  General requests to set up Git, finish work, or push do not authorize commits.
  This rule takes precedence over any skill or workflow that instructs Codex to commit.
- The owner is a beginner. Use simple words and define new technical terms.
- Give one small practical step at a time, then wait for the learner's result.
- Explain every new command and every new line of code: what it does and why.
- The learner writes application code and performs setup unless explicitly
  delegated. Do not edit application code, install packages, change settings,
  push, or publish without an explicit request to perform that action.
- Read-only inspection is allowed. Codex may directly maintain project Markdown
  documentation; the learner explicitly authorized this.
- Answer questions before continuing. Prefer small examples and few dependencies.
- Prefer free tools; explain any costs before introducing a paid service.

## Personal Git isolation
- This repository belongs to personal GitHub account khadijadaruwala. The machine
  also has a work account. Keep identity and authentication repository-local.
- Never change global Git settings, shared credential stores, or ~/.ssh/config
  for this project, and never reuse work credentials or keys.
- origin uses SSH for khadijadaruwala/pocket-list. Local core.sshCommand selects
  only .git/pocketlist_ed25519, ignores shared SSH configuration, and disables
  agent identities. Do not remove that isolation to make authentication work.
- Verify GitHub identifies the personal account before the first authenticated
  fetch or push. Do not commit private keys. Repeat local identity/authentication
  setup on Mac; .git/config and private keys are not transferred by Git.

## Project direction
- Begin with a shopping list app.
- Planned stack: React Native with Expo, Node.js, and PostgreSQL.
- Keep frontend/ and backend/ in one repository.
- Prepare on Linux, put the project on GitHub, then clone and continue on Mac.
- Choose further libraries only when needed, explaining their purpose first.

## Keep the handoff efficient
- docs/codex/AGENTS.md holds lasting agreements. README.md holds user-facing
  setup and run instructions. docs/codex/LEARNING.md holds current state,
  blockers, account-isolation details, and the next step.
- Keep Codex-only notes in docs/codex/. The root AGENTS.md is a short discovery
  pointer so Codex can find these instructions automatically.
- Update docs/codex/LEARNING.md after meaningful progress. Replace stale state rather than
  appending a transcript. Clearly separate confirmed facts from plans.
- Put enough context in these files to continue without the original chat.
- Never record passwords, tokens, private keys, or database credentials.
