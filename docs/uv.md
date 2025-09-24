# uv — Modern Python Package & Project Manager

`uv` is a high-performance, “all-in-one” tool for managing Python projects. It aims to replace or consolidate many of the tools in the typical Python ecosystem (like pip, virtualenv, pipx, poetry, pyenv, etc.) while being much faster and giving a smooth developer experience. :contentReference[oaicite:0]{index=0}

---

## Key Features

- **Dependency and environment management**  
  Handles installing, upgrading, removing dependencies; locks and syncs environments. Automatically manages virtual environments for your projects. :contentReference[oaicite:1]{index=1}  
- **Tool execution & “ephemeral” tools**  
  You can run CLI tools without permanently installing them, using commands like `uvx` (alias for `uv tool run`). Useful for linting, formatting, etc. :contentReference[oaicite:2]{index=2}  
- **Python version management**  
  Provides commands to install and pin specific Python versions. :contentReference[oaicite:3]{index=3}  
- **Project initialization, building & publishing**  
  Scaffold Python projects, build distributions, publish to package indexes. :contentReference[oaicite:4]{index=4}  
- **Pip interface compatibility**  
  Supports many existing workflows: `uv pip install …`, dealing with `requirements.txt`, etc. So migration is often smooth. :contentReference[oaicite:5]{index=5}

---

## Why Use uv

| Benefit | Detail |
|---|---|
| **Speed** | Much faster dependency resolution, installations, environment setup compared to pip, virtualenv, pip-tools. :contentReference[oaicite:6]{index=6} |
| **Reduced tool-sprawl** | One tool instead of juggling many (pip, pipx, poetry, virtualenv, pyenv, etc.). Fewer contexts to switch. :contentReference[oaicite:7]{index=7} |
| **Better reproducibility** | Lock files, isolated tool / project environments, version pinning. :contentReference[oaicite:8]{index=8} |
| **Modern UX** | Clean commands, alias like `uvx`, good docs, nicer developer experience. :contentReference[oaicite:9]{index=9}

---

## Basic Usage

Here are some common commands you’ll use with `uv`:  

```bash
# Install uv (one of the ways)
curl -LsSf https://astral.sh/uv/install.sh | sh  
# or via pip: pip install uv :contentReference[oaicite:10]{index=10}

# Add dependencies in a project
uv add requests flask

# Lock dependencies, sync them
uv lock
uv sync

# Run a tool once without installing it permanently
uvx ruff check src/

# Permanently install a tool
uv tool install ruff

# Manage Python versions
uv python install 3.12
uv python pin 3.12

# Build and publish
uv build
uv publish
```
