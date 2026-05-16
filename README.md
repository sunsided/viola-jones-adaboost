# Viola-Jones AdaBoost-enabled Face Detection

This repo implements the Viola-Jones object detection framework for face detection purely for the fun of it.

## Prerequisites

### Required Tools

| Tool | Purpose | Install Command |
|------|---------|-----------------|
| [Miniconda](https://docs.conda.io/en/latest/miniconda.html) | Python environment management | See below |
| [Task](https://taskfile.dev/) | Task runner | `sh -c "$(curl --location https://taskfile.dev/install.sh)" -- -d -b ~/.local/bin` |

### Installing Miniconda

**Linux:**
```bash
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
bash Miniconda3-latest-Linux-x86_64.sh
# Follow prompts, then restart your terminal or run:
source ~/.bashrc  # or ~/.zshrc
```

**macOS:**
```bash
# Using Homebrew
brew install miniconda

# Or download installer
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
bash Miniconda3-latest-MacOSX-x86_64.sh
```

**Windows:**
Download and run the installer from: https://docs.conda.io/en/latest/miniconda.html

### Installing Task

See https://taskfile.dev/installation/ for all options.

Quick install:
```bash
# Linux/macOS
sh -c "$(curl --location https://taskfile.dev/install.sh)" -- -d -b ~/.local/bin

# Or with npm
npm install -g @go-task/cli

# Or with Homebrew (macOS/Linux)
brew install go-task/tap/go-task
```

## Quick Start

```bash
# 1. Create the conda environment
task env:create

# 2. Start Jupyter Notebook
task jupyter

# 3. Open viola-jones.ipynb in your browser
```

## Available Tasks

| Command | Description |
|---------|-------------|
| `task env:create` | Create the conda environment from `environment.yaml` |
| `task env:remove` | Remove the conda environment |
| `task env:update` | Update environment when `environment.yaml` changes |
| `task env:activate` | Open a shell with the environment activated |
| `task jupyter` | Start Jupyter Notebook server |
| `task --list` | Show all available tasks |

## Troubleshooting

### "conda is not installed"

Follow the Miniconda installation steps above. After installation, **restart your terminal** or run `source ~/.bashrc` (or `~/.zshrc`) to activate conda in your current session.

### "command not found: task"

Make sure `~/.local/bin` is in your PATH:
```bash
export PATH="$HOME/.local/bin:$PATH"
```

Add this to your `~/.bashrc` or `~/.zshrc` to make it permanent.

## Project Structure

```
.
├── environment.yaml      # Conda environment specification
├── Taskfile.dist.yaml    # Task definitions
├── viola-jones.ipynb     # Main notebook
├── images/               # Sample images
└── README.md             # This file
```

Start exploring at [viola-jones.ipynb](viola-jones.ipynb).
