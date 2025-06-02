---
mode: chat
tools: [codebase]
description: Create a new Craft CMS plugin from scratch
---

# Create Craft CMS Plugin

Create a complete Craft CMS plugin with proper structure and functionality:

1. **Setup Plugin Structure**: Create the standard Craft plugin directory structure
   - `/src` folder with main plugin class
   - `/composer.json` with proper Craft dependencies
   - Plugin class extending `craft\base\Plugin`

2. **Core Plugin Files**:
   - Main plugin class with proper initialization
   - Service classes following Craft patterns
   - Translation files if needed
   - Plugin icon and configuration

3. **Implementation**:
   - Follow Craft's PSR-4 autoloading standards
   - Use Craft's dependency injection container
   - Implement proper event handling and hooks
   - Add appropriate Craft console commands if needed

4. **Integration**:
   - Register services, components, and elements properly
   - Configure plugin settings and control panel sections
   - Implement proper permissions and user access controls

Focus on:
- Following Craft CMS plugin development best practices
- Using Craft's APIs and service architecture
- Ensuring compatibility with current Craft version in ${workspaceFolder}
- Creating production-ready, installable plugin code