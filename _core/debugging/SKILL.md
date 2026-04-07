---
name: debugging
description: Quick debugging and issue identification skill. Use when tasks require rapid error detection, pattern-based troubleshooting, identifying obvious issues, or supporting Claude's debugging process with focused analysis of specific components.
version: 1.0.0
category: _core
agent: gemini
overridable: true
---

# Debugging

This skill provides systematic approaches for identifying and resolving issues across code, systems, and processes.

## Universal Debugging Protocol

Follow this sequence for any debugging task:

### 1. Reproduce the Issue

- Identify exact steps to trigger the problem
- Note what works vs what doesn't
- Establish baseline behavior
- Document error messages verbatim

### 2. Isolate the Cause

Use binary search methodology:
```
1. Identify the scope (which component/module)
2. Divide the scope in half
3. Test which half contains the issue
4. Repeat until root cause found
```

### 3. Form Hypothesis

Based on symptoms, hypothesize root cause:
- What component is likely responsible?
- What changed recently?
- What assumptions might be wrong?

### 4. Test Hypothesis

- Design minimal test case
- Change one variable at a time
- Document results
- Iterate if hypothesis is wrong

### 5. Fix and Verify

- Implement fix
- Test the exact reproduction case
- Test edge cases
- Verify no regression introduced

## Code Debugging Strategies

### Reading Error Messages

Extract maximum information:
1. **Error type** - What kind of error?
2. **Location** - File, line number, function
3. **Stack trace** - Call sequence leading to error
4. **Context** - Variable values, system state

### Common Bug Patterns

**Type errors:**
```
- Check variable types match expectations
- Verify function signatures
- Inspect type coercion behavior
```

**Logic errors:**
```
- Add print/log statements
- Trace execution flow
- Verify conditional logic
- Check loop boundaries
```

**Runtime errors:**
```
- Validate input data
- Check null/undefined values
- Verify resource availability
- Inspect race conditions
```

**Performance issues:**
```
- Profile code execution
- Identify bottlenecks
- Check algorithm complexity
- Review memory usage
```

## Debugging Tools and Techniques

### Print Debugging
Most direct approach:
```python
print(f"DEBUG: variable_name = {variable_name}")
print(f"DEBUG: Entering function X with args: {args}")
```

### Interactive Debugging
For complex issues, use step-through debugging:
- Set breakpoints at suspected locations
- Inspect variable state
- Step through execution line-by-line

### Rubber Duck Debugging
Explain the code line-by-line to identify flawed assumptions.

### Git Bisect
For regression bugs:
```bash
git bisect start
git bisect bad  # Current broken state
git bisect good <commit>  # Known working state
# Git will binary search to find breaking commit
```

## Systematic Investigation Process

When cause is unclear:

```
1. List what IS working correctly
2. List what is NOT working
3. Identify the boundary between working/broken
4. Focus investigation on that boundary
```

## Root Cause Analysis

Don't stop at symptoms—find the true root cause:

**Five Whys Technique:**
```
Issue: Server crashed
Why? → Out of memory
Why? → Memory leak
Why? → Connections not being closed
Why? → Missing cleanup in error handler
Why? → Error handler was added recently without full review
Root cause: Insufficient code review process
```

## Environment-Specific Debugging

### Works on My Machine
When behavior differs across environments:
- Compare environment variables
- Check dependency versions
- Verify configuration files
- Review system resources

### Intermittent Issues
For sporadic bugs:
- Increase logging
- Look for race conditions
- Check timing dependencies
- Review concurrent access patterns

## Documentation Standards

When debugging, document:
1. **Initial symptoms** - What was observed
2. **Reproduction steps** - How to trigger
3. **Investigation process** - What was tried
4. **Root cause** - What was actually wrong
5. **Fix applied** - What solved it
6. **Prevention** - How to avoid in future

## Common Anti-Patterns to Avoid

- Changing multiple things simultaneously
- Assuming you know the cause without testing
- Fixing symptoms instead of root cause
- Not verifying the fix solves the original problem
- Skipping documentation of findings

## Error Prevention Strategies

After fixing a bug, consider:
- Adding tests to prevent regression
- Adding input validation
- Improving error messages
- Documenting tricky behavior
- Refactoring to make bugs less likely

## Quick Debugging Checklist

Before diving deep:
- [ ] Have you reproduced the issue?
- [ ] Did you read the error message completely?
- [ ] Is this a new issue or regression?
- [ ] What changed recently?
- [ ] Does it work in a simpler case?
- [ ] Have you checked the obvious things first?