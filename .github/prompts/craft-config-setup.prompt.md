---
mode: 'agent'
tools: ['codebase']
description: 'Configure Craft CMS project settings and environment'
---

# Craft CMS Configuration Setup

Configure Craft CMS project settings, environment, and deployment:

1. **Environment Configuration**:
   - Set up proper `.env` file with database and environment settings
   - Configure `config/general.php` for different environments
   - Set up `config/db.php` with proper database connections

2. **Project Config**:
   - Review and sync `config/project/` YAML files
   - Handle field layouts, sections, and content model changes
   - Ensure proper project config application across environments

3. **Performance and Caching**:
   - Configure Redis or file-based caching in `config/app.php`
   - Set up proper asset caching and transforms
   - Configure template caching strategies

4. **Security Settings**:
   - Set up proper security headers and CSRF protection
   - Configure user permissions and access controls
   - Implement proper password policies and 2FA if needed

5. **Plugin Configuration**:
   - Configure installed plugins via config files
   - Set up plugin-specific environment variables
   - Handle plugin licensing and updates

6. **Deployment Setup**:
   - Configure proper file permissions and folder structure
   - Set up database migration and backup strategies
   - Implement proper logging and error handling

Focus on:
- Following Craft CMS configuration best practices
- Using environment-specific settings appropriately
- Ensuring security and performance optimization
- Creating maintainable, scalable configuration in ${workspaceFolder}
