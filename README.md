# My GitHub Codespaces Dotfiles

This repository is my personal collection of dotfiles to create a consistent and clean development environment across all of my **GitHub Codespaces**.

The main goal here is to stop Codespaces from running automatic setup commands (`npm install`, `npm run build`, etc.) by default. This gives me a clean slate every time I spin up a new environment, allowing me to run all commands manually.

---

## What's In This Repo?

This setup is intentionally minimal. Here are the key files and why they exist:

* **`.devcontainer.json`**: This is the most important file. It provides a default configuration for any Codespace I launch from a repository that *doesn't* have its own `devcontainer.json`. It's configured to be minimal and **not run any automatic commands** when a codespace is created or started.

* **`.gitignore`**: A general-purpose `.gitignore` file to prevent common system files from macOS (`.DS_Store`) and Windows (`Thumbs.db`) from being accidentally committed in any project.

* **(Other future files)**: I can add other personal configuration files here later, like `.bashrc`, `.zshrc`, or `.gitconfig`, to further customize my default terminal environment.

---

## How Is This Used?

This repository isn't meant to be cloned for every project. Instead, it's linked directly to my GitHub account settings.

To re-enable this or check if it's working, I need to:

1.  Go to my GitHub **Settings**.
2.  Navigate to the **Codespaces** section in the sidebar.
3.  Under the **Dotfiles** section, make sure this repository (`your-username/dotfiles`) is selected.

Changes pushed to this repository will be automatically picked up by any **new** Codespaces I create. To apply changes to an existing Codespace, I'll need to rebuild its container.
