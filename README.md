# Opencode Config

Personal opencode configuration repository.

## Installation

Symlink the `.opencode` folder from your home directory to this repository:

```bash
ln -s "$PWD" ~/.opencode
```

This allows you to version control your opencode configuration while keeping it in the standard location expected by the tool.

## Structure

- `README.md` - This file
- `.gitignore` - Files to ignore in this repo
- `AGENTS.md` - Agent configurations and references
- `agents/` - Custom agent definitions
- `themes/` - Custom UI themes

## Usage

After symlinking, opencode will use this folder as its configuration directory.
