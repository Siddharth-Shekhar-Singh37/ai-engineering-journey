# Week 1: Setup (26 Oct – 1 Nov 2026)

## What I learned
- An environment is a controlled "kitchen" for code: a fixed Python version,
  exact library versions, kept separate from other projects, and written down
  so anyone can rebuild it.

- The 7 steps of setting up any environment: choose the machine, pin Python,
  create a private space (.venv), install libraries, lock exact versions,
  point the editor at it, verify and save the recipe.

- Commit the recipe (pyproject.toml, uv.lock, .python-version), never the
  cooked meal (.venv). `uv sync` rebuilds the environment from the recipe.

- Git has three stages: working directory → staging area (git add) →
  committed (git commit), then git push sends it to GitHub.

- One logical change per commit, with Conventional Commit messages
  (e.g. "chore: ...").

- Git settings have two levels: global (~/.gitconfig, wiped on container
  rebuild) and local (.git/config, survives because the repo folder survives).

- A devcontainer defines the environment as code, so it is identical on any
  machine. I pinned Python 3.12 because new versions (3.14) often lack
  library support.

- Security basics: 2FA on GitHub, private no-reply commit email, $0 spending
  caps, API keys never in code.

## What I built
- Public repo `ai-engineering-journey` with README, Python .gitignore and
  MIT licence.

- A devcontainer pinned to Python 3.12 that installs uv automatically.

- A uv project with numpy, committed with its lockfile.

- 3 commits pushed: initial commit → dev container → uv project.

## What confused me
- Why there were three different Pythons on one machine, and which one
  VS Code was using.

- The Git LFS warning after rebuilding: old hooks from the previous image
  were calling a tool that no longer existed. Fixed by removing the hooks.

- `git log` showing only one commit when I reopened the codespace. A second
  check (git fetch + git log --all) showed nothing was wrong.
  
- Setting up an environment on my own still feels hard. I will do the
  practice drill (practice-env repo) alone to prove I can.

- Start Phase 1, Week 2: vectors and dot products (Mon 2 Nov).