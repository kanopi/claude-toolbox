# Kanopi Claude Plugins

[![License: GPL v2](https://img.shields.io/badge/License-GPL%20v2-blue.svg)](https://www.gnu.org/licenses/gpl-2.0)

This marketplace provides curated Claude Code plugins from Kanopi Studios.

## Installation

### Add the Kanopi Marketplace

```bash
claude plugins marketplace add kanopi-claude-plugins https://github.com/kanopi/kanopi-claude-plugins
```

### Install a Plugin

```bash
claude plugins install kanopi-claude-plugins/<plugin-name>
```

### List Available Plugins

```bash
claude plugins marketplace list kanopi-claude-plugins
```

## Available Plugins

### 🌱 CMS Cultivator

Comprehensive workflow commands for Drupal and WordPress development.

**Features:**
- 📝 PR Workflow (6 commands) - Generate descriptions, automate releases, manage documentation
- ♿ Accessibility (5 commands) - WCAG 2.1 AA compliance audits and fixes
- ⚡ Performance (5 commands) - Query optimization, asset analysis, bundle inspection
- 🔒 Security (3 commands) - Dependency audits, vulnerability scanning, security reports
- 🧪 Testing (3 commands) - Coverage analysis, report generation
- ✨ Code Quality (2 commands) - Standards enforcement, automated fixes
- 📚 Documentation (1 command) - Automated API documentation generation

**Installation:**
```bash
claude plugins install kanopi-claude-plugins/cms-cultivator
```

**Documentation:** [https://kanopi.github.io/cms-cultivator/](https://kanopi.github.io/cms-cultivator/)

**Repository:** [https://github.com/kanopi/cms-cultivator](https://github.com/kanopi/cms-cultivator)

## Requirements

- [Claude Code CLI](https://docs.claude.com/en/docs/claude-code) installed
- Git (for plugin installation)

## Support

For issues, questions, or feature requests:

1. **Plugin-specific issues:** Open an issue in the respective plugin repository
2. **Marketplace issues:** Open an issue in this repository

## Contributing

We welcome contributions! Please see individual plugin repositories for contribution guidelines.

### Adding a New Plugin to the Marketplace

1. Ensure your plugin follows the [Claude Code plugin structure](https://docs.claude.com/en/docs/claude-code/plugins)
2. Add your plugin metadata to `marketplace.json`
3. Submit a pull request with:
   - Plugin description
   - Documentation link
   - Test results
   - Example usage

## License

GPL-2.0-or-later - see [LICENSE.md](LICENSE.md) file for details.

## About Kanopi Studios

[Kanopi Studios](https://kanopi.com) is a woman-owned web design, development, and support agency dedicated to helping you create the strongest possible connections between your content and your audiences.

With concentrations in nonprofits, higher education, healthcare and corporate work, Kanopi works with a diverse group of organizations that strive to create a better digital world. Our holistic yet nimble approach allows us to jump in at any stage of your site’s lifecycle to help it achieve its full potential.
