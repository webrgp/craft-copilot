---
applyTo: "**/*.php,**/composer.json,**/*.twig"
---

# Craft CMS 5.7.0 Project Coding Guidelines

## Project Context
- **Craft CMS 5.7.0** Solo Edition
- **PHP 8.2** with modern features enabled
- **DDEV** containerized development environment
- **Project Config** enabled for environment synchronization

## PHP Code Style (PSR-12 + Craft 5.x Standards)

### Basic Formatting
- Use PSR-12 coding standards as the foundation
- Use trailing commas in multi-line arrays and method definitions
- Place chained method calls on separate lines
- Use strict comparison operators (`===` and `!==`)
- Use single quotes by default for strings
- Initialize arrays explicitly

### Type Declarations (PHP 8.2 Features)
- Declare method argument and return types whenever possible
- Use `(int)` and `(float)` for type casting
- Leverage PHP 8.2 union types, intersection types, and `mixed` type
- Use readonly properties and classes where appropriate
- Specify array member class names when it makes sense

### Naming Conventions
- Namespaces should be lowercase
- Getter methods without arguments should start with `get`
- Private properties should begin with an underscore
- Use interfaces in docblock type declarations

### Class Structure
- Use `self::` for referencing private static methods
- Follow Craft's service pattern for plugin architecture
- Extend appropriate Craft base classes (`craft\base\Plugin`, `craft\base\Element`, etc.)

### Docblocks
- Use full sentences with proper capitalization and punctuation
- Use `@inheritdoc` for overridden methods
- Use `bool` and `int` instead of `boolean` and `integer`
- Document all public methods with proper `@param` and `@return` tags

### Control Flow
- Use "happy path" control flow patterns
- Avoid unnecessary `else` statements when possible
- Return early from methods to reduce nesting

### Craft 5.x Specific Patterns
- Controllers should return Response objects or strings
- Use Yii's declarative condition syntax for database queries
- Follow Craft's event system patterns for plugin hooks
- Use Craft's dependency injection container appropriately
- Leverage Craft 5.x performance improvements and new APIs
- Use Project Config for environment synchronization
- Follow DDEV containerized development practices

## Twig Templates

### Structure
- Follow Craft's template hierarchy and naming conventions
- Use proper template inheritance with `{% extends %}` and `{% include %}`
- Implement responsive design patterns

### Performance
- Use `{% cache %}` tags appropriately
- Optimize Element queries with proper criteria
- Use asset transforms for responsive images

### Content
- Use Craft's Element queries (`craft.entries`, `craft.assets`)
- Handle Matrix fields and Relations properly
- Implement proper pagination patterns