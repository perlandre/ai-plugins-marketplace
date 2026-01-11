# Perlandre's Marketplace

Claude Code plugins for documentation, diagrams, and developer productivity.

## Installation

```bash
claude plugins add-marketplace github.com/perlandre/perlandre-marketplace
```

## Available Plugins

### app-diagram

Generate comprehensive state machine and sequence diagrams for any application.

**Features:**
- `diagram-generator` agent - Full codebase analysis with Opus model
- `diagram-updater` agent - Incremental updates after code changes
- Mermaid format output to `docs/diagrams/`
- Automatic inventory tracking

**Install:**
```bash
claude plugins install app-diagram
```

**Usage:**
```
"Generate diagrams for this application"
"Update diagrams after my changes"
```

---

## Adding Plugins

To add a new plugin to this marketplace, add an entry to `.claude-plugin/marketplace.json`:

```json
{
  "name": "plugin-name",
  "source": {
    "source": "url",
    "url": "https://github.com/owner/repo.git"
  },
  "description": "Plugin description",
  "version": "1.0.0",
  "category": "category"
}
```

Categories: `documentation`, `development`, `productivity`, `testing`, `security`
