# Contributing to Claude Toolbox

Thank you for your interest in contributing to Kanopi's Claude Code toolbox!

## How to Contribute

### Reporting Issues

- Use the GitHub issue tracker for bug reports and feature requests
- Check if the issue already exists before creating a new one
- Provide as much detail as possible:
  - Claude Code version
  - Plugin version
  - Operating system
  - Steps to reproduce
  - Expected vs actual behavior

### Submitting a New Plugin

To add a new plugin to the Claude Toolbox marketplace:

1. **Develop your plugin** following the [Claude Code plugin structure](https://docs.claude.com/en/docs/claude-code/plugins)

2. **Create plugin metadata** (`plugins/your-plugin-name.json`):
   ```json
   {
     "name": "your-plugin-name",
     "displayName": "Your Plugin Name",
     "description": "Brief description",
     "version": "1.0.0",
     "publisher": "Kanopi Studios",
     "repository": {
       "type": "git",
       "url": "https://github.com/kanopi/your-plugin-name"
     }
   }
   ```

3. **Update .claude-plugin/marketplace.json** to include your plugin in the `plugins` array

4. **Update README.md** with plugin information

5. **Submit a pull request** with:
   - Plugin description
   - Documentation link
   - Test results
   - Example usage

### Plugin Requirements

All plugins in the Claude Toolbox marketplace must:

- ✅ Follow Claude Code plugin conventions
- ✅ Include comprehensive documentation
- ✅ Have appropriate `allowed-tools` permissions
- ✅ Follow Kanopi coding standards
- ✅ Include usage examples
- ✅ Be GPL-2.0-or-later licensed
- ✅ Work with DDEV (if applicable)
- ✅ Support both Drupal and WordPress (if applicable)

### Code Review Process

1. Submit your pull request
2. Kanopi team reviews the plugin
3. Address any feedback
4. Plugin is merged and published

### Testing

Before submitting:

- Test plugin commands in multiple environments
- Verify tool permissions are correct
- Ensure documentation is accurate
- Check for any security concerns

## Code of Conduct

- Be respectful and professional
- Focus on constructive feedback
- Help create an inclusive environment
- Follow Kanopi's values and standards

## Questions?

- Open an issue for marketplace questions
- Contact specific plugin repositories for plugin-specific questions

## License

By contributing, you agree that your contributions will be licensed under GPL-2.0-or-later.
