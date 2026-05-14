# Installing from Claude Toolbox

> **Platforms:** Claude Toolbox works in Claude Code, Claude Desktop, and OpenAI Codex. The steps below cover Claude Code; for Codex, see the [Codex Installation](#codex-installation) section.

## Quick Start (Claude Code)

### Step 1: Open Claude Code

Navigate to your project and start Claude Code:

```bash
cd /path/to/your/drupal-or-wordpress-project
claude
```

### Step 2: Add the Claude Toolbox Marketplace

Inside Claude Code CLI:

```bash
/plugin marketplace add kanopi/claude-toolbox
```

### Step 3: Install CMS Cultivator

```bash
/plugin install cms-cultivator@claude-toolbox
```

### Step 4: Verify Installation

```bash
/plugin
```

Select "Manage Plugins" to see `cms-cultivator` in your installed plugins list.

### Step 5: Start Using Skills

CMS Cultivator skills activate automatically from natural language — no command syntax to remember:

```
"I'm ready to commit my changes"      → commit-message-generator
"Is this button accessible?"          → accessibility-checker
"This query is slow"                  → performance-analyzer
"Does this follow Drupal standards?"  → code-standards-checker
"Create a PR for my current branch"   → pr-create
```

You can also invoke skills explicitly:

```bash
/pr-create PROJ-123          # Create a PR with a generated description
/audit-a11y                  # Run a comprehensive accessibility audit
/audit-perf                  # Analyze Core Web Vitals
/audit-security              # Scan for OWASP Top 10 vulnerabilities
/audit-live-site             # Multi-dimensional audit (parallel specialists)
```

In OpenAI Codex, use `@skill-name` instead of `/skill-name`.

See the [Skills overview](https://kanopi.github.io/cms-cultivator/commands/overview/) for the full list of 46 skills.

## Codex Installation

For OpenAI Codex users:

### Step 1: Add the Marketplace

```bash
codex plugin marketplace add kanopi/claude-toolbox
```

### Step 2: Open the Plugin Browser

```bash
codex/plugins
```

Browse to **CMS Cultivator** and select **Install plugin**.

### Step 3: Invoke Skills

In Codex, prefix skill names with `@` instead of `/`:

```bash
@pr-create PROJ-123
@audit-a11y
@audit-perf
```

Skills also activate automatically from natural language, the same as in Claude Code.

## Alternative Installation Methods

### Direct from GitHub (Without Marketplace)

Inside Claude Code CLI:

```bash
/plugin install https://github.com/kanopi/cms-cultivator
```

### Manual Installation

```bash
cd ~/.config/claude/plugins
git clone https://github.com/kanopi/cms-cultivator.git
```

Then inside Claude Code CLI:

```bash
/plugin enable cms-cultivator
```

## Updating Plugins

### Update from Marketplace

Inside Claude Code CLI:

```bash
/plugin update cms-cultivator@claude-toolbox
```

### Update Manual Installation

```bash
cd ~/.config/claude/plugins/cms-cultivator
git pull origin main
```

## Troubleshooting

### Marketplace Not Found

If you get an error that the marketplace is not found:

1. Verify the marketplace file exists:
   ```bash
   curl https://raw.githubusercontent.com/kanopi/claude-toolbox/main/.claude-plugin/marketplace.json
   ```

2. Re-add the marketplace inside Claude Code CLI:
   ```bash
   /plugin marketplace remove claude-toolbox
   /plugin marketplace add kanopi/claude-toolbox
   ```

### Plugin Not Installing

If the plugin fails to install:

1. Check your internet connection
2. Verify Git is installed: `git --version`
3. Try manual installation method above

### Commands Not Working

If commands are not available after installation:

1. Verify the plugin is enabled inside Claude Code CLI:
   ```bash
   /plugin
   ```

2. Select "Manage Plugins" and ensure `cms-cultivator` is enabled

3. If not enabled, enable it:
   ```bash
   /plugin enable cms-cultivator
   ```

4. Restart Claude Code

## Support

- **Issues:** [GitHub Issues](https://github.com/kanopi/cms-cultivator/issues)
- **Documentation:** [https://kanopi.github.io/cms-cultivator/](https://kanopi.github.io/cms-cultivator/)
- **Marketplace Issues:** [GitHub Issues](https://github.com/kanopi/claude-toolbox/issues)

---

**Last Updated:** 2026-05-14
