---
applyTo: "**/*"
---

# Craft CMS Code Review Guidelines

## Project Context
Review code for a Craft CMS 5.7.0 project with DDEV development environment, focusing on AI-enhanced developer experience and Craft CMS best practices.

## Code Review Priorities

### 1. Craft CMS 5.x Compliance
- Verify compatibility with Craft CMS 5.7.0 APIs
- Check for proper use of Craft's dependency injection container
- Ensure Project Config synchronization compatibility
- Validate proper Element Type and Field Type implementations
- Review plugin structure follows Craft 5.x standards

### 2. PHP 8.2 Best Practices
- Look for proper type declarations and return types
- Check for appropriate use of PHP 8.2 features (readonly, union types)
- Verify proper error handling and exception management
- Ensure PSR-12 coding standards compliance
- Review for security vulnerabilities and best practices

### 3. Performance Considerations
- Check for efficient Element queries with proper criteria
- Review template caching strategies (`{% cache %}` usage)
- Validate asset transform usage for images
- Look for N+1 query problems in templates
- Ensure proper database indexing for custom fields

### 4. Security Review
- Verify CSRF protection in forms
- Check for proper input validation and sanitization
- Review user permission and access control implementations
- Ensure no secrets or credentials are hardcoded
- Validate proper file upload security measures

### 5. Template Quality (Twig)
- Check for proper template inheritance patterns
- Review responsive design implementation
- Verify accessibility considerations (ARIA, semantic HTML)
- Ensure proper pagination patterns
- Look for XSS prevention measures

### 6. Code Organization
- Review file structure follows Craft conventions
- Check for proper separation of concerns
- Validate service class implementations
- Ensure proper namespace usage
- Review for code duplication and reusability

### 7. Documentation and Comments
- Verify docblocks are complete and accurate
- Check for meaningful variable and method names
- Review inline comments for necessity (avoid over-commenting)
- Ensure README and setup instructions are current

### 8. Testing Considerations
- Look for testable code structure
- Check for proper dependency injection for testing
- Review mock and stub usage in tests
- Validate test coverage for critical functionality

### 9. Environment Compatibility
- Verify DDEV configuration compatibility
- Check environment variable usage
- Review multi-environment configuration (dev/staging/production)
- Ensure proper .gitignore patterns

### 10. Craft-Specific Patterns
- Review proper use of Craft's event system
- Check GraphQL schema definitions if applicable
- Validate proper asset volume configurations
- Review entry type and section configurations
- Check field layout implementations

## Review Checklist

### Critical Issues (Block Merge)
- [ ] Security vulnerabilities present
- [ ] Breaks existing functionality
- [ ] Performance regressions
- [ ] Incompatible with Craft CMS 5.7.0
- [ ] Missing required error handling

### Major Issues (Needs Fixing)
- [ ] Code doesn't follow Craft coding standards
- [ ] Missing proper type declarations
- [ ] Inefficient database queries
- [ ] Accessibility issues in templates
- [ ] Missing or incorrect docblocks

### Minor Issues (Suggestions)
- [ ] Code organization improvements
- [ ] Variable naming enhancements
- [ ] Template optimization opportunities
- [ ] Additional test coverage needed
- [ ] Documentation improvements

## Review Response Format
Structure feedback with:
1. **Summary**: Brief overview of changes and overall quality
2. **Critical Issues**: Must-fix items that block merge
3. **Suggestions**: Improvements for code quality
4. **Praise**: Highlight good practices and clever solutions
5. **Craft-Specific Notes**: CMS-specific observations and recommendations

## Common Craft CMS Patterns to Look For

### Good Patterns
```php
// Proper service injection
public function __construct(
    private readonly MyService $myService
) {}

// Efficient Element queries
$entries = Entry::find()
    ->section('blog')
    ->limit(10)
    ->with(['author'])
    ->all();
```

### Anti-Patterns to Flag
```php
// Missing type declarations
public function processData($data) {
    return $data;
}
```

```twig
{# Avoid in templates - causes N+1 queries #}
{% for entry in craft.entries.section('blog').all() %}
    {{ entry.author.name }}
{% endfor %}
```
