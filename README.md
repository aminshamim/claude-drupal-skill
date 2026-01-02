# Drupal 11 Expert - Claude Code Skill Plugin

A professional Claude Code skill plugin that provides expert-level assistance for Drupal 11 development. This plugin transforms Claude into a senior Drupal architect with deep knowledge of Drupal 11 core APIs, modern development patterns, and best practices.

## Features

- **Drupal 11.x Compatibility** - Only uses current, non-deprecated APIs
- **Modern Architecture** - Emphasizes services, dependency injection, and event subscribers
- **Security First** - Built-in guidance for secure coding practices
- **Production Ready** - Code that can be deployed without warnings or issues
- **Comprehensive Coverage** - Modules, themes, plugins, forms, routing, entities, and more
- **Best Practices** - Follows PSR-4, PSR-12, and Drupal coding standards
- **Configuration Management** - Proper config schemas and CMI integration
- **Testing Support** - Guidance for unit, kernel, and functional tests

## What This Skill Provides

This skill enables Claude to:

- Generate complete, installable Drupal 11 modules
- Create custom plugins (Blocks, Fields, Queue Workers, etc.)
- Build secure forms with AJAX support
- Implement proper routing and controllers with access control
- Create custom entities with proper field definitions
- Write event subscribers to replace legacy hooks
- Develop accessible, performant themes
- Follow dependency injection patterns
- Implement proper caching strategies
- Generate configuration schemas
- Write comprehensive tests

## Installation

### Install from Git

```bash
claude-code plugins install https://github.com/yourusername/claude-drupal-skill
```

Replace `yourusername` with your GitHub username after you push to git.

### Manual Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/claude-drupal-skill
   ```

2. Install the plugin:
   ```bash
   claude-code plugins install /path/to/claude-drupal-skill
   ```

### Verify Installation

```bash
claude-code plugins list
```

You should see `drupal-11-expert` in the list of installed plugins.

## Usage

### Activate the Skill

To activate the Drupal 11 expert mode, simply use the skill command:

```bash
/drupal-setup
```

Or in your conversation with Claude Code:

```
User: /drupal-setup
```

Once activated, Claude will operate as a senior Drupal 11 architect for the remainder of your session.

### Example Use Cases

#### 1. Create a Custom Module

```
User: /drupal-setup
User: Create a custom module called "event_manager" that provides:
- A custom content entity for events
- A block to display upcoming events
- A form to register for events
- Proper configuration management
```

#### 2. Build a Custom Block Plugin

```
User: /drupal-setup
User: Create a configurable block plugin that displays the current user's
recent activity with caching support
```

#### 3. Implement a Custom Form with AJAX

```
User: /drupal-setup
User: Create a multi-step form for user registration with AJAX validation
and proper security measures
```

#### 4. Review Existing Code

```
User: /drupal-setup
User: Review this controller code and refactor it to use dependency injection
and follow Drupal 11 best practices
[paste code]
```

#### 5. Create a Custom Entity

```
User: /drupal-setup
User: Create a custom content entity called "Product" with fields for name,
description, price, and image. Include proper entity access control.
```

#### 6. Build Event Subscribers

```
User: /drupal-setup
User: Create an event subscriber that logs all node operations and sends
notifications on specific content type updates
```

## What Makes This Different

### Standards Compliance

- **Only Drupal 11.x APIs** - No deprecated code
- **PHP 8.2+** - Modern PHP features
- **Symfony 6.x** - Leverages Symfony components properly
- **PSR-4/PSR-12** - Modern PHP standards

### Security Focus

- Proper input validation
- Output escaping best practices
- CSRF protection
- Permission and access control
- SQL injection prevention

### Modern Patterns

- Dependency Injection over service locators
- Event Subscribers over hooks where applicable
- Plugin API utilization
- Configuration API (not variables)
- Proper cache metadata

### Production Quality

Every generated code includes:
- Complete file structure
- Configuration schemas
- Cache metadata
- Access control
- Error handling
- Documentation

## Skill Command Reference

### Main Skill

- `/drupal-setup` - Activate Drupal 11 expert mode

Once activated, Claude will maintain this expertise throughout your session.

## Advanced Usage

### Custom Module Development Workflow

1. **Activate the skill:**
   ```
   /drupal-setup
   ```

2. **Request module creation:**
   ```
   Create a module called "my_custom" that does [description]
   ```

3. **Claude will provide:**
   - Complete file structure
   - All necessary files with full code
   - Configuration schemas
   - Service definitions
   - Proper documentation

4. **Review and refine:**
   ```
   Add a permission check for [specific requirement]
   ```

   ```
   Refactor this to use dependency injection
   ```

### Theme Development

```
/drupal-setup
Create a custom theme called "corporate_theme" with:
- Responsive layout
- Custom block regions
- SASS/CSS organization
- Accessibility features
```

### Entity Development

```
/drupal-setup
Create a custom content entity "Invoice" with:
- Line items using entity reference
- Computed total field
- PDF generation capability
- Proper access control
```

## API Knowledge Base

This skill has comprehensive knowledge of:

- **Core APIs**: Entity, Form, Render, Database, Configuration, Cache
- **Plugin System**: Block, Field, Queue, Condition, Filter, and more
- **Symfony Components**: Routing, Events, Dependency Injection, HTTP
- **Service Container**: Service definition, injection, compilation
- **Theming**: Twig, render arrays, libraries, preprocess functions
- **Security**: XSS prevention, CSRF, permissions, input validation
- **Testing**: Unit, Kernel, Functional, JavaScript tests

## Coding Standards

All generated code follows:

- [Drupal Coding Standards](https://www.drupal.org/docs/develop/standards)
- [PSR-4: Autoloading Standard](https://www.php-fig.org/psr/psr-4/)
- [PSR-12: Extended Coding Style](https://www.php-fig.org/psr/psr-12/)
- [Drupal API Documentation Standards](https://www.drupal.org/docs/develop/standards/api-documentation-and-comment-standards)

## Requirements

- Claude Code CLI (latest version)
- Basic understanding of Drupal concepts
- PHP development environment (for testing generated code)

## Project Structure

```
claude-drupal-skill/
├── claude-code.json          # Plugin manifest
├── README.md                 # This file
├── EXAMPLES.md              # Detailed usage examples
├── skills/
│   └── drupal-setup.md      # Main skill prompt
└── .gitignore               # Git ignore rules
```

## Contributing

Contributions are welcome! If you find issues or have improvements:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## Changelog

### Version 1.0.0

- Initial release
- Complete Drupal 11.x API coverage
- Module, theme, and plugin development support
- Security and best practices guidance
- Configuration management support
- Testing guidelines

## License

MIT License - See LICENSE file for details

## Support

For issues, questions, or contributions:
- GitHub Issues: [https://github.com/yourusername/claude-drupal-skill/issues](https://github.com/yourusername/claude-drupal-skill/issues)

## Resources

- [Drupal 11 API Documentation](https://api.drupal.org/api/drupal/11.x)
- [Drupal.org](https://www.drupal.org/)
- [Claude Code Documentation](https://github.com/anthropics/claude-code)

## Disclaimer

This skill provides code generation assistance. Always review and test generated code thoroughly before deploying to production. The skill maintainers are not responsible for issues arising from the use of generated code.

---

**Made with Claude Code** - Empowering developers to build better Drupal applications faster.
