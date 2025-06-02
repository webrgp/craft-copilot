# Craft Copilot

A drop-in enhancement for Craft CMS projects that supercharges GitHub Copilot with Claude Code-style behavior and Craft CMS expertise.

## Quick Setup

1. Copy these files to your Craft CMS project root:
   ```bash
   cp -r .github .vscode /path/to/your/craft-project/
   ```

2. Install recommended VSCode extensions:
   - GitHub Copilot
   - GitHub Copilot Chat
   - Twig Language 2

3. Restart VSCode and enjoy enhanced AI assistance!

## What's Included

### Core Configuration
- `.github/copilot-instructions.md` - Craft CMS specialized behavior guidelines
- `.vscode/settings.json` - Enhanced context awareness and Twig support

### Craft-Specific Prompts
Access via Command Palette → "Chat: Open Prompt Library":

- **craft-plugin-create** - Generate complete Craft plugins
- **craft-field-type** - Create custom Field Types  
- **craft-element-type** - Build custom Element Types
- **craft-templates** - Develop Twig templates with Craft patterns
- **craft-config-setup** - Configure environments and deployment

### Enhanced Features
- Proactive, action-oriented responses (like Claude Code)
- Deep Craft CMS architecture understanding
- Automatic Twig syntax highlighting and Emmet support
- Context-aware suggestions for Craft APIs and patterns
- Complete feature implementation vs. code snippets

## Usage Examples

**Plugin Development:**
```
@workspace /craft-plugin-create Create a custom Element Type for managing team members with name, role, and bio fields
```

**Template Work:**
```
@workspace /craft-templates Build a responsive blog listing page with pagination and Matrix field support
```

**Debugging:**
```
@workspace /debug-fix The entry query in templates/blog/index.twig is returning wrong results
```

## Benefits

- **Faster Development** - AI understands Craft patterns and completes entire features
- **Better Code Quality** - Follows Craft best practices and coding standards  
- **Reduced Context Switching** - AI proactively handles implementation details
- **Craft Expertise** - Deep knowledge of Element API, Twig, plugins, and architecture
