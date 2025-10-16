# Installing from Claude Toolbox

## Quick Start

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

### Step 5: Start Using Commands

Try some commands:

```bash
/pr-desc PROJ-123        # Generate PR description
/a11y-audit              # Run accessibility audit
/perf-analyze queries    # Analyze query performance
/security-scan deps      # Scan dependencies
```

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

**Last Updated:** 2025-10-13
