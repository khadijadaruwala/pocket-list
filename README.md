# PocketList

A shopping list app built step by step as a beginner learning project.

## Planned technologies
- React Native with Expo: the Android and iPhone screens.
- Node.js: the backend server that receives requests from the app.
- PostgreSQL: the database that saves lists and items.

Data moves from the screen to the backend, then to PostgreSQL. The backend sends
a result back so the screen can update. The frontend does not connect directly
to PostgreSQL or contain database passwords.

## Folder structure
```text
pocket-list/
  frontend/       Mobile app (only a .gitkeep placeholder; not initialized)
  backend/        Node.js server (only a .gitkeep placeholder; not initialized)
  docs/codex/     Development assistant instructions and progress notes
  AGENTS.md       Short pointer to the assistant instructions
  README.md       Project overview and verified setup instructions
  .gitignore      Installed packages, generated files, and local secrets to exclude
```

PostgreSQL runs separately; backend/ will contain the code that connects to it.

## Setup status
The folders exist, but application packages and run commands are not set up yet.
Verified setup commands will be added here as each step is completed.

## Repository

[PocketList on GitHub](https://github.com/khadijadaruwala/pocket-list)

When moving to another computer, install the project dependencies there after
cloning. Git does not transfer installed packages, local account settings, SSH
keys, or the running database. Setup commands will be documented when available.
