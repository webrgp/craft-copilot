# Craft CMS Copilot - Code-Style Instructions

## Craft CMS Project Specialization

### Current Project Context
- **Craft CMS 5.7.0** fresh installation with Solo edition
- **PHP 8.2** platform requirement
- **DDEV** development environment setup
- **Project Config** enabled with YAML-based configuration
- **Single Site** setup named "Craft Copilot"
- **Timezone**: America/Los_Angeles

### Craft CMS 5.x Architecture Understanding
- Recognize modern Craft 5.x project structure (config/, templates/, web/, storage/)
- Understand Craft's MVC pattern and plugin architecture
- Work with Craft's Element API, Field Types, and Content modeling
- Know Craft's Twig templating with custom filters and functions
- Understand Craft's database schema and Active Record patterns
- Use Project Config for environment synchronization

### Craft 5.x Specific Patterns
- Use Craft's service classes and dependency injection container
- Follow Craft's PSR-12 coding standards and PSR-4 autoloading
- Implement proper Element Types, Field Types, and Widgets
- Use Craft's event system and plugin hooks appropriately
- Work with Craft's console commands (`./craft`) and queue jobs
- Leverage Craft 5.x performance improvements and new APIs

### Development Environment
- Use DDEV commands for database and environment management
- Work with environment-specific config files (.env.example.dev, .env.example.staging, .env.example.production)
- Understand Craft's caching strategies and invalidation
- Use Craft CLI tools for migrations and plugin management

### Common Project Tasks
- Create and modify Craft plugins with proper Craft 5.x structure
- Build custom Field Types and Element Types
- Implement Craft CMS templates with proper Twig syntax
- Configure Craft settings and sync via project config
- Work with Craft's GraphQL API and Element API
- Handle Craft's asset management and transforms
- Create sections, entry types, and field layouts

## Core Behavior Guidelines

### Be Proactive and Direct
- Take action when asked, don't just provide suggestions
- Complete entire features or fixes, not just code snippets
- Be concise and direct - avoid unnecessary explanations unless asked
- Focus on "doing" rather than "explaining how to do"

### Context Awareness
- Always consider the entire project structure and codebase
- Understand existing patterns, libraries, and conventions before making changes
- Check package.json, imports, and neighboring files to understand the tech stack
- Follow existing code style and naming conventions

### Task Management
- Break complex tasks into smaller, manageable steps
- Complete one task fully before moving to the next
- Verify solutions work (run tests, builds, lints when possible)
- Handle errors and edge cases proactively

### Code Quality Standards
- Never add comments unless explicitly requested
- Follow security best practices - never expose secrets or keys
- Use existing libraries and utilities rather than reinventing
- Write idiomatic code that matches the project's patterns

### File Operations
- Prefer editing existing files over creating new ones
- Only create new files when absolutely necessary
- Never create documentation files unless explicitly requested
- Understand file purposes before making changes

### Craft Development Workflow
- Use Craft's CLI tools (`./craft` command) for plugin and migration tasks
- Use DDEV commands (`ddev craft`, `ddev composer`) for containerized development
- Understand Craft's caching and invalidation strategies
- Work with Craft's project config and environment-specific settings
- Follow Craft 5.x plugin development best practices
- Ensure compatibility with Craft CMS 5.7.0 and PHP 8.2
- Sync project config changes across environments

## Response Format
- Keep responses short and actionable
- Provide specific file paths and line numbers when referencing code
- Use format: `file_path:line_number` for code references
- Minimize explanatory text - focus on implementation

## Tool Usage
- Search codebase thoroughly before making assumptions
- Use multiple approaches to understand context
- Verify changes work in the actual environment
- Take real actions rather than just providing instructions
