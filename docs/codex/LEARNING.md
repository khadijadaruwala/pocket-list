# PocketList: current handoff

Updated: 2026-10-29. Read docs/codex/AGENTS.md for teaching and editing permissions.
Paths in this handoff are relative to the repository root unless stated otherwise.

## Confirmed state
- This is a beginner learning project, initially a shopping list.
- Direction: React Native with Expo, Node.js, PostgreSQL, in one repository.
- Start on remote Linux over SSH; later move to Mac through GitHub.
- Linux folder: /home/engineering/khadija/PocketList/pocket-list.
- Learner's terminal reported Node.js v24.15.0, npm 11.12.1, Git 2.43.0.
  GitHub CLI (gh) was not installed; it is optional.
- frontend/ and backend/ each contain only a .gitkeep placeholder; no application
  files are present. .gitignore now excludes installed packages,
  generated output, environment secrets, logs, and OS files.
- Git is initialized on main. Personal author name/email are set in .git/config,
  not global configuration. The personal email was supplied by the learner.
- origin is git@github.com:khadijadaruwala/pocket-list.git, the SSH form of the
  learner-provided https://github.com/khadijadaruwala/pocket-list.git repository.
- Local SSH settings select only .git/pocketlist_ed25519, ignore shared SSH
  configuration, and disable SSH agent identities and password fallback.
- Inherited credential helpers are reset locally; personal settings are not
  written to the global Git configuration. Global configuration was checked
  byte-for-byte unchanged during initialization.
- The learner generated the dedicated SSH key. Its public ED25519 key was verified
  with ssh-keygen on 2026-10-29. The learner confirmed GitHub accepted the public
  key. The learner ran the isolated SSH test and reported GitHub's successful
  greeting for khadijadaruwala. Personal authentication is confirmed by that
  output; access to the repository and its contents remain unverified.
  Never read or display the private key.
- There are no commits yet. The .gitkeep placeholders allow the intended
  frontend/ and backend/ folders to be included in the first commit.
- Codex instructions and this handoff live in docs/codex/. The root AGENTS.md
  points there for automatic discovery. README.md is kept focused on the app.
- Markdown edits are delegated to Codex. Application code and setup remain
  learner-performed unless explicitly delegated.
- Standing instruction: Codex must never create, amend, or rewrite commits.
  The learner alone performs commits, including the first commit.

## Not yet done in this session
- Frontend/backend initialization, dependency installation, or application code.
- PostgreSQL setup and connection.
- First commit and GitHub push. Remote repository contents/access are unverified.
- Mac clone, local dependencies, and app preview.
- No application build or tests have been run; there is no application yet.

## Next small step
Have the learner run git ls-remote --symref origin HEAD in their terminal to
inspect the remote default branch before deciding how to commit/push. Empty
output with no error indicates no advertised HEAD; confirm remote branches/tags
before treating the repository as empty. Do not overwrite remote history.
The learner must enter the key passphrase locally, not into chat.
The learner has authorized Git setup, but do not assume application setup is delegated.

## Following steps (plans, not completed)
1. Initialize Expo in frontend/ and a minimal Node.js project in backend/.
2. Verify each starts; put the actual working commands in README.md.
3. Finish the personal Git authentication and initial commit/push above.
4. Clone on Mac, install dependencies from lockfiles, and verify a mobile preview.
5. Teach displaying, adding, checking off, and removing shopping items.
6. Introduce backend requests and PostgreSQL storage gradually.

## Open decisions
- Remote repository contents, visibility, and access have not been checked.
- Mac hardware/OS and available Android/iPhone test device.
- Backend framework and other libraries have not been selected.

## Linux tool issue
- Ubuntu 24.04.1 LTS on KVM. The learner installed system bubblewrap; bwrap is
  now /usr/bin/bwrap. Sandbox startup still fails with:
  bwrap: loopback: Failed RTM_NEWADDR: Operation not permitted
- The same sandbox test fails in PocketList and DustMon. Folder permissions
  allow the engineering user to edit. The exact sandbox cause remains unconfirmed.
- An AppArmor audit recorded a profile transition, not an explicit denial.
  Additional AppArmor changes were proposed but paused; do not assume they happened.
- The session now allows approval requests. Approved commands outside the
  sandbox successfully read the files. This is not a sandbox repair.
- If a command is blocked, use the supported approval flow. Do not change server
  security settings or repeat package installations without new evidence.
