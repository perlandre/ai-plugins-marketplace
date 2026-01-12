# Perlandre's Plugins Marketplace

Claude Code plugins for documentation, diagrams, and developer productivity.

## Installation

From Claude Code:

```bash
/plugin marketplace add perlandre/ai-plugins-marketplace
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
/plugin install app-diagram
```

**Usage:**
```
"Generate diagrams for this application"
"Update diagrams after my changes"
```

---

### icp-dev

A Claude Code plugin that makes Internet Computer (ICP) development feel native and seamless. Provides slash commands for common workflows (local dev, deployment, cycles management) with safety guardrails for risky operations.

**Features:**
- `/icp-dev` - Bootstrap command to start replica and deploy canisters
- `/icp-status` - Status dashboard showing replica, canisters, and cycles
- `/icp-deploy` - Mainnet deployment with safety checks and verification
- `/icp-topup` - Guided workflow for topping up canister cycles
- `/icp-clean` - Wipe local state and redeploy fresh (with `--keep-ii` option to preserve Internet Identity sessions)
- Automatic VetKD artifact management for encryption projects

**Install:**
```bash
/plugin install icp-dev
```

**Usage:**
```
"/icp-dev" — Start local development environment
"/icp-dev --clean" — Fresh start with wiped state
"/icp-status --network ic" — Check mainnet canister status
"/icp-deploy --network ic" — Deploy to mainnet (guided)
"/icp-topup" — Top up canister cycles
"/icp-clean --keep-ii" — Reset state but keep test logins
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
