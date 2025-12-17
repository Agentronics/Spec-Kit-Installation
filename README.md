# Spec Ki+t

Build high-quality software faster.

Spec Ki+t is an open source toolkit that helps you focus on product scenarios and predictable outcomes instead of vibe coding every piece from scratch. It enables a structured, spec-driven workflow with AI coding agents.

---

## Prerequisites

- Linux / macOS / Windows  
- Supported AI coding agent  
- uv (package manager)  
- Python 3.11+  
- Git  

---

## Installation

### Option 1: Persistent Installation (Recommended)

Install once and use everywhere.

```bash
# From PyPI (recommended)
pip install specifyplus

# Or with uv tools
uv tool install specifyplus
```

Upgrade later:

```bash
pip install -U specifyplus
uv tool upgrade specifyplus
```

Uninstall:

```bash
pip uninstall specifyplus
# or
uv tool uninstall specifyplus
```

Use the tool:

```bash
specifyplus init <PROJECT_NAME>
# or
sp init <PROJECT_NAME>

specifyplus check
# or
sp check
```

Upgrade Specify core:

```bash
uv tool install specify-cli --force --from git+https://github.com/github/spec-kit.git
```

---

### Option 2: One-time Usage (No Installation)

Run without installing:

```bash
uvx specifyplus --help
uvx specifyplus init <PROJECT_NAME>
# or
uvx sp init <PROJECT_NAME>
```

---

## Spec-Driven Workflow

### 1. Establish Project Principles

```text
/sp.constitution
Create principles focused on code quality, testing standards, user experience consistency, and performance requirements
```

---

### 2. Create the Spec

```text
/sp.specify
Build an application that can help me organize my photos in separate photo albums. Albums are grouped by date and can be reorganized by dragging and dropping on the main page. Albums are never nested. Within each album, photos are previewed in a tile-like interface.
```

---

### 3. Create a Technical Plan

```text
/sp.plan
The application uses Vite with a minimal number of libraries. Use vanilla HTML, CSS, and JavaScript as much as possible. Images are not uploaded anywhere, and metadata is stored in a local SQLite database.
```

---

### 4. Break Down into Tasks

```text
/sp.tasks
```

---

### 5. Implement

```text
/sp.implement
```

---

## CLI Examples

```bash
# Basic initialization
specifyplus init my-project

# With specific AI assistants
specifyplus init my-project --ai claude
specifyplus init my-project --ai cursor
specifyplus init my-project --ai windsurf
specifyplus init my-project --ai amp

# PowerShell scripts (Windows / cross-platform)
specifyplus init my-project --ai copilot --script ps

# Initialize in current directory
specifyplus init . --ai copilot
specifyplus init --here --ai copilot

# Force merge into non-empty directory
specifyplus init . --force --ai copilot
specifyplus init --here --force --ai copilot

# Skip git initialization
specifyplus init my-project --ai gemini --no-git

# Debug mode
specifyplus init my-project --ai claude --debug

# Use GitHub token
specifyplus init my-project --ai claude --github-token ghp_your_token_here

# Check system requirements
specifyplus check
```

---

## Slash Commands

### Core Commands

- /sp.constitution – Define project principles and guidelines  
- /sp.specify – Define requirements and user stories  
- /sp.plan – Create technical implementation plans  
- /sp.tasks – Generate implementation tasks  
- /sp.implement – Execute tasks and build features  

### Optional Commands

- /sp.clarify – Clarify underspecified areas  
- /sp.analyze – Cross-artifact consistency and coverage analysis  
- /sp.checklist – Quality and completeness checklists  

---

## Environment Variables

SPECIFY_FEATURE  
Overrides feature detection for non-git repositories. Set this to the feature directory name (for example: 001-photo-albums) before running /sp.plan or follow-up commands.

---

Spec Ki+t helps you move from idea → spec → plan → tasks → working software with clarity and consistency.
