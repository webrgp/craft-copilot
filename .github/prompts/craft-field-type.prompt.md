---
mode: chat
tools: [codebase]
description: Create or modify Craft CMS Field Types
---

# Craft CMS Field Type Development

Create or modify a Craft CMS Field Type with full functionality:

1. **Field Type Class**: 
   - Extend `craft\base\Field` or appropriate base class
   - Implement required abstract methods (`normalizeValue`, `getInputHtml`, etc.)
   - Handle value validation and normalization

2. **Database Schema**:
   - Define proper content column type in `getContentColumnType()`
   - Handle migration scripts if schema changes are needed
   - Consider multi-site and localization requirements

3. **Control Panel Interface**:
   - Create field settings template in `/templates/settings.twig`
   - Implement field input template in `/templates/input.twig`
   - Add proper CSS/JS assets if needed

4. **Value Handling**:
   - Implement `normalizeValue()` for data consistency
   - Handle `serializeValue()` and `getInputHtml()` properly
   - Support field validation rules

5. **Integration**:
   - Register field type in plugin's main class
   - Add proper GraphQL support if needed
   - Consider Element API compatibility

Focus on:
- Following Craft's Field Type architecture patterns
- Using existing Craft field types as reference in ${workspaceFolder}
- Ensuring proper data handling and validation
- Creating user-friendly control panel experience