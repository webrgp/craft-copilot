# Craft Copilot Project Commit Message Guidelines

## Project Context
This is a fresh Craft CMS 5.7.0 installation with DDEV development environment, designed as a drop-in enhancement for Craft CMS projects to improve developer experience with AI-powered tools.

## Format Structure
Use conventional commit format with Craft CMS specific types:

```
<type>(<scope>): <description>

[optional body]

[optional footer(s)]
```

## Commit Types
- **feat**: New feature (plugin, field type, element type, template)
- **fix**: Bug fix or issue resolution
- **config**: Changes to Craft configuration, project config, or environment setup
- **content**: Content model changes (sections, fields, entry types)
- **template**: Template updates or new Twig templates
- **plugin**: Plugin-specific changes or updates
- **migration**: Database migrations or project config updates
- **copilot**: Changes to AI/Copilot configuration and prompts
- **ddev**: DDEV environment and containerization changes
- **style**: Code style changes (no functionality change)
- **refactor**: Code refactoring without feature changes
- **perf**: Performance improvements
- **test**: Adding or updating tests
- **docs**: Documentation updates
- **chore**: Build process, dependencies, or maintenance tasks

## Scope Examples
- **instructions**: Copilot instruction files and guidelines
- **prompts**: Prompt templates and configurations
- **vscode**: VSCode settings and extensions
- **ddev**: DDEV configuration and environment
- **craft5**: Craft CMS 5.x specific features
- **admin**: Control panel or admin-related changes
- **frontend**: Public-facing templates or functionality
- **api**: GraphQL, Element API, or REST endpoints
- **assets**: Asset handling, transforms, or volume changes
- **users**: User management or permissions
- **entries**: Entry-related functionality
- **fields**: Custom fields or field layouts

## Description Guidelines
- Use imperative mood ("add" not "added" or "adds")
- Start with lowercase letter
- No period at the end
- Keep under 50 characters
- Be specific about what changed

## Body Guidelines
- Explain the "why" not the "what"
- Reference Craft concepts (Elements, Fields, Sections, etc.)
- Include breaking change information
- Mention related issue numbers

## Examples

```
feat(commerce): add custom product field type for variants

Implements a new field type that allows better product variant
management with conditional logic based on product type.

Closes #123
```

```
config: update project config for multi-site setup

- Add new site groups for regional markets
- Configure locale-specific field layouts
- Update asset volume permissions

BREAKING CHANGE: Existing single-site content requires migration
```

```
fix(templates): resolve pagination issue in blog listing

The craft.entries query was not properly handling offset
calculation for paginated results on category pages.
```

```
plugin(seo): update meta field defaults for new entry types

Updates the SEO plugin configuration to provide better
default meta fields for newly created sections.
```
