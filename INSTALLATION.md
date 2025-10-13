# Installing from Kanopi Claude Plugins Marketplace

## Quick Start

### Step 1: Add the Kanopi Marketplace

```bash
claude plugins marketplace add kanopi-claude-plugins https://github.com/kanopi/kanopi-claude-plugins
```

### Step 2: List Available Plugins

```bash
claude plugins marketplace list kanopi-claude-plugins
```

### Step 3: Install CMS Cultivator

```bash
claude plugins install kanopi-claude-plugins/cms-cultivator
```

### Step 4: Verify Installation

```bash
claude plugins list
```

You should see `cms-cultivator` in the list of installed plugins.

### Step 5: Start Using Commands

Open Claude Code in your project:

```bash
cd /path/to/your/drupal-or-wordpress-project
claude
```

Try some commands:

```bash
/pr-desc PROJ-123        # Generate PR description
/a11y-audit              # Run accessibility audit
/perf-analyze queries    # Analyze query performance
/security-scan deps      # Scan dependencies
```

## Alternative Installation Methods

### Direct from GitHub (Without Marketplace)

```bash
claude plugins install https://github.com/kanopi/cms-cultivator
```

### Manual Installation

```bash
cd ~/.config/claude/plugins
git clone https://github.com/kanopi/cms-cultivator.git
claude plugins enable cms-cultivator
```

## Updating Plugins

### Update from Marketplace

```bash
claude plugins update kanopi-claude-plugins/cms-cultivator
```

### Update Manual Installation

```bash
cd ~/.config/claude/plugins/cms-cultivator
git pull origin main
```

## Troubleshooting

### Marketplace Not Found

If you get an error that the marketplace is not found:

1. Verify the marketplace URL is correct:
   ```bash
   curl https://raw.githubusercontent.com/kanopi/kanopi-claude-plugins/main/marketplace.json
   ```

2. Re-add the marketplace:
   ```bash
   claude plugins marketplace remove kanopi-claude-plugins
   claude plugins marketplace add kanopi-claude-plugins https://github.com/kanopi/kanopi-claude-plugins
   ```

### Plugin Not Installing

If the plugin fails to install:

1. Check your internet connection
2. Verify Git is installed: `git --version`
3. Try manual installation method above

### Commands Not Working

If commands are not available after installation:

1. Verify the plugin is enabled:
   ```bash
   claude plugins list
   ```

2. If not enabled, enable it:
   ```bash
   claude plugins enable cms-cultivator
   ```

3. Restart Claude Code

## Support

- **Issues:** [GitHub Issues](https://github.com/kanopi/cms-cultivator/issues)
- **Documentation:** [https://kanopi.github.io/cms-cultivator/](https://kanopi.github.io/cms-cultivator/)
- **Marketplace Issues:** [GitHub Issues](https://github.com/kanopi/kanopi-claude-plugins/issues)

---

**Last Updated:** 2025-10-13
