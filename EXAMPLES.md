# Drupal 11 Expert - Usage Examples

This document provides detailed examples of using the Drupal 11 Expert skill plugin with Claude Code.

## Table of Contents

1. [Basic Module Creation](#basic-module-creation)
2. [Custom Block Plugin](#custom-block-plugin)
3. [Custom Entity with Fields](#custom-entity-with-fields)
4. [Form with AJAX](#form-with-ajax)
5. [Event Subscriber](#event-subscriber)
6. [Custom Service](#custom-service)
7. [Theme Development](#theme-development)
8. [Code Review and Refactoring](#code-review-and-refactoring)

---

## Basic Module Creation

### Request:

```
/drupal-setup

Create a simple Drupal 11 module called "hello_world" that:
- Provides a custom page at /hello that displays "Hello, Drupal 11!"
- Has proper routing and controller
- Uses dependency injection for current user service
- Displays the current user's name if logged in
```

### What You'll Get:

The skill will generate:
- `hello_world.info.yml` - Module definition
- `hello_world.routing.yml` - Route definition
- `src/Controller/HelloController.php` - Controller with dependency injection
- Complete documentation and explanation

---

## Custom Block Plugin

### Request:

```
/drupal-setup

Create a custom block plugin called "UserActivityBlock" that:
- Shows the last 5 nodes created by the current user
- Is configurable (admin can set number of items to display)
- Includes proper caching (by user and modified nodes)
- Uses dependency injection for entity_type.manager
- Handles users with no content gracefully
```

### What You'll Get:

- Module structure
- Block plugin with PHP attributes
- Configuration form
- Build method with render array
- Cache metadata (contexts, tags, max-age)
- Configuration schema

---

## Custom Entity with Fields

### Request:

```
/drupal-setup

Create a custom content entity called "Task" with:
- Fields: title, description, status (todo/in_progress/done), priority (low/medium/high), due_date
- Proper entity access control
- List builder for admin UI
- Forms for add/edit
- Entity views
- Route provider
- Configuration for bundle support (optional)
```

### What You'll Get:

- Complete entity class with annotations/attributes
- Base field definitions
- Entity access control handler
- List builder
- Form handlers (default, add, edit, delete)
- Route provider
- Entity links
- Module configuration
- Permission definitions
- Menu links

---

## Form with AJAX

### Request:

```
/drupal-setup

Create a multi-step registration form with AJAX:
- Step 1: Email and username validation (AJAX validation)
- Step 2: Personal information (name, phone)
- Step 3: Preferences (newsletter, notifications)
- Progress indicator
- Ability to go back
- Proper validation at each step
- CSRF protection
- Submit creates user account
```

### What You'll Get:

- Form class with state management
- AJAX callbacks for validation
- Multi-step form logic
- Progress indicator render array
- Validation handlers
- Submit handler
- AJAX response commands
- Security measures

---

## Event Subscriber

### Request:

```
/drupal-setup

Create an event subscriber that:
- Listens to node insert/update/delete operations
- Logs all operations to watchdog
- Sends email notification when article nodes are published
- Integrates with Mail API
- Uses dependency injection for logger and mail manager
```

### What You'll Get:

- Event subscriber class
- Service definition in .services.yml
- Proper event subscription method
- Event handlers for each operation
- Logger integration
- Mail sending implementation
- Proper error handling

---

## Custom Service

### Request:

```
/drupal-setup

Create a custom service called "ContentStatistics" that:
- Calculates content statistics (total nodes, by type, by author)
- Uses database queries efficiently
- Implements caching (1 hour cache)
- Uses dependency injection for database and cache services
- Provides methods: getTotalNodes(), getNodesByType(), getTopAuthors()
- Is injectable in other services/controllers
```

### What You'll Get:

- Service class with proper namespace
- Service definition in .services.yml
- Constructor with dependency injection
- Public methods with documentation
- Database query implementations
- Caching implementation
- Usage examples in controllers/blocks

---

## Theme Development

### Request:

```
/drupal-setup

Create a custom theme called "modern_corporate" with:
- Base theme: stable9
- Responsive layout (mobile-first)
- Custom block regions (header, sidebar_left, content, sidebar_right, footer)
- CSS/JS libraries organization
- Preprocess functions for nodes and blocks
- Template suggestions
- Breakpoints for responsive images
```

### What You'll Get:

- `modern_corporate.info.yml` - Theme definition with regions
- `modern_corporate.libraries.yml` - Asset definitions
- `modern_corporate.theme` - Preprocess functions
- `modern_corporate.breakpoints.yml` - Responsive breakpoints
- Template files structure
- CSS organization (base, layout, components, utilities)
- JavaScript with Drupal behaviors
- Theme suggestions examples

---

## Code Review and Refactoring

### Request:

```
/drupal-setup

Review and refactor this controller to use Drupal 11 best practices:

[paste legacy code using \Drupal::service(), no dependency injection,
deprecated functions, poor caching, etc.]

Requirements:
- Use dependency injection
- Replace deprecated APIs
- Add proper caching
- Improve security
- Follow coding standards
```

### What You'll Get:

- Line-by-line analysis of issues
- Refactored code with dependency injection
- Updated to Drupal 11 APIs
- Proper cache metadata
- Security improvements
- PSR-12 formatting
- Explanation of each change

---

## Advanced Examples

### Example 1: Custom Field Type

```
/drupal-setup

Create a custom field type "color_picker" with:
- Storage for color hex value
- Field widget with HTML5 color input
- Field formatter to display color swatch
- Field settings for default color
- Schema definition
```

### Example 2: Queue Worker

```
/drupal-setup

Create a queue worker that:
- Processes content imports in background
- Uses QueueInterface and QueueWorker plugin
- Handles failures gracefully
- Logs progress
- Is triggerable via cron
```

### Example 3: REST Resource

```
/drupal-setup

Create a custom REST resource for "tasks" entity:
- GET, POST, PATCH, DELETE methods
- Proper authentication
- Access control
- Serialization support
- Rate limiting considerations
```

### Example 4: Custom Cache Bin

```
/drupal-setup

Create a custom cache bin for external API responses:
- Service definition
- Cache backend configuration
- Helper service to interact with cache
- Clear cache on config change
```

---

## Tips for Best Results

1. **Be Specific**: The more details you provide, the better the output
2. **Mention Requirements**: Security, caching, testing needs, etc.
3. **Ask for Explanations**: Request architectural explanations
4. **Request Reviews**: Ask for code review of existing code
5. **Iterate**: Refine the output by asking for specific changes

---

## Common Patterns

### Pattern 1: "Create and Explain"

```
/drupal-setup

Create a [component] and explain:
- Why you chose this approach
- What Drupal APIs are used
- How caching works
- Security considerations
```

### Pattern 2: "Review and Improve"

```
/drupal-setup

Review this code and improve:
- Performance
- Security
- Code quality
- Drupal 11 compliance

[paste code]
```

### Pattern 3: "Complete Implementation"

```
/drupal-setup

Provide a complete, production-ready implementation of [feature] including:
- All required files
- Configuration
- Tests
- Documentation
```

---

## Testing the Generated Code

After receiving code from the skill:

1. **Copy Files**: Copy generated files to your Drupal installation
2. **Clear Cache**: `drush cr`
3. **Enable Module**: `drush en module_name`
4. **Test Functionality**: Use the feature as intended
5. **Check Logs**: Look for errors in watchdog
6. **Run Tests**: `phpunit` for generated tests
7. **Code Standards**: `phpcs --standard=Drupal,DrupalPractice module_name/`

---

## Troubleshooting

### Issue: Generated code doesn't work

**Solution**: Ensure you're using Drupal 11.x and PHP 8.2+. Check logs for specific errors.

### Issue: Module won't enable

**Solution**: Check that all file paths are correct and composer dependencies are installed.

### Issue: Deprecated API warnings

**Solution**: Report back to the skill - it should only use Drupal 11 APIs.

---

## Next Steps

After mastering these examples:

1. Combine patterns to create complex features
2. Ask for architectural advice
3. Request code reviews of your own code
4. Get guidance on contrib module integration
5. Learn advanced patterns (plugin derivatives, entity bundles, etc.)

---

## Contributing Examples

If you have examples you'd like to share, please contribute:

1. Test your example thoroughly
2. Document the request and output
3. Submit a pull request with your example added to this file

---

**Remember**: Always review and test generated code before deploying to production!
