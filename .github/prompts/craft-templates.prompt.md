---
mode: 'agent'
tools: ['codebase']
description: 'Work with Craft CMS Twig templates'
---

# Craft CMS Template Development

Create or modify Craft CMS Twig templates with proper structure and functionality:

1. **Template Architecture**:
   - Follow Craft's template hierarchy and naming conventions
   - Use proper template extends/includes with `_layout.twig`
   - Implement responsive design patterns

2. **Craft Twig Usage**:
   - Use Craft's Element queries (`craft.entries`, `craft.assets`, etc.)
   - Implement proper pagination with `craft.entries.limit()`
   - Handle Matrix fields, Relations, and custom Field Types

3. **Performance Optimization**:
   - Use `{% cache %}` tags appropriately for performance
   - Implement lazy loading for images and content
   - Optimize Element queries with proper criteria

4. **Content Modeling**:
   - Work with Sections, Entry Types, and Field Layouts
   - Handle multi-site content and localization
   - Implement proper SEO meta tags and structured data

5. **Frontend Integration**:
   - Include CSS/JS assets using `{% css %}` and `{% js %}` tags
   - Implement proper form handling with CSRF protection
   - Use Craft's asset transforms for responsive images

Focus on:
- Following Craft's Twig templating best practices
- Using existing template patterns in ${workspaceFolder}
- Creating accessible, performant templates
- Proper error handling and fallbacks
