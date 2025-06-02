---
mode: 'agent'
tools: ['codebase']
description: 'Debug and fix issues systematically'
---

# Debug and Fix

Systematically debug and resolve the issue:

1. **Investigate**: Search the codebase to understand the problem context
2. **Reproduce**: Identify steps to reproduce the issue if possible
3. **Root Cause**: Analyze the code to find the underlying cause
4. **Fix**: Implement a proper solution that addresses the root cause
5. **Test**: Verify the fix works and doesn't break existing functionality
6. **Validate**: Run relevant tests, builds, and checks

Approach:
- Examine related files and dependencies in ${workspaceFolder}
- Consider the impact of changes on other parts of the system
- Follow existing error handling patterns
- Ensure the fix is robust and maintainable

Provide a complete fix, not just identification of the problem.
