---
mode: chat
tools: [codebase]
description: Create or modify Craft CMS Element Types
---

# Craft CMS Element Type Development

Create or modify a Craft CMS Element Type with complete functionality:

1. **Element Class Structure**:
   - Extend `craft\base\Element` or appropriate base class
   - Implement required abstract methods (`displayName`, `pluralDisplayName`, etc.)
   - Define element attributes and database table structure

2. **Database and Migrations**:
   - Create proper migration for element table
   - Define relationships with other elements
   - Handle element deletion and cascading updates

3. **Control Panel Integration**:
   - Create element index template and controller
   - Implement element edit form with proper field layout
   - Add element actions (delete, duplicate, etc.)

4. **Query and Criteria**:
   - Create custom ElementQuery class extending `craft\elements\db\ElementQuery`
   - Implement search, filtering, and sorting capabilities
   - Add custom criteria methods for the element type

5. **Frontend and API**:
   - Ensure proper URL routing and element URLs
   - Add GraphQL support with custom fields and queries
   - Implement Element API endpoints if needed

6. **Advanced Features**:
   - Add element relations and reference tags
   - Implement proper permissions and user access
   - Handle element status, drafts, and revisions if applicable

Focus on:
- Following Craft's Element architecture patterns
- Using existing Element Types as reference in ${workspaceFolder}
- Creating robust, scalable element structure
- Proper integration with Craft's control panel and APIs