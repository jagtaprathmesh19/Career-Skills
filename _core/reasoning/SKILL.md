---
name: reasoning
description: Logical reasoning and pattern analysis skill optimized for fast processing. Use when tasks require quick analysis, pattern identification, comparing options, structured evaluation, or supporting Claude's reasoning with rapid assessment of alternatives.
version: 1.0.0
category: _core
agent: gemini
overridable: true
---

# Reasoning

This skill provides structured approaches for complex reasoning tasks across all domains.

## Core Reasoning Patterns

### 1. Chain-of-Thought Analysis

When faced with complex problems:

1. **Decompose** - Break down into sub-problems
2. **Analyze** - Examine each component independently
3. **Synthesize** - Combine insights into coherent solution
4. **Validate** - Check logic and assumptions

**Example workflow:**
```
Problem → [Identify constraints] → [List assumptions] → 
[Generate options] → [Evaluate each] → [Synthesize recommendation]
```

### 2. Trade-off Analysis

For decision-making tasks:

1. Identify key criteria (performance, cost, risk, time, etc.)
2. Weigh each option against criteria
3. Consider second-order effects
4. Make explicit the reasoning behind recommendations

**Output format:**
- State the decision clearly
- List pros/cons for each option
- Explain which criteria matter most and why
- Provide final recommendation with confidence level

### 3. Causal Reasoning

When analyzing cause-effect relationships:

1. Map direct causation
2. Identify confounding factors
3. Consider temporal ordering
4. Distinguish correlation from causation

### 4. Counterfactual Thinking

Ask: "What if X had been different?"

- Useful for strategy, debugging, and risk assessment
- Test assumptions by inverting them
- Explore alternative scenarios

## Strategic Planning Framework

For long-term planning tasks:

1. **Define goal state** - What success looks like
2. **Map current state** - Where we are now
3. **Identify constraints** - What limits us
4. **Generate pathways** - Multiple routes to goal
5. **Evaluate risks** - What could go wrong
6. **Prioritize actions** - What to do first

## Assumption Tracking

Always make implicit assumptions explicit:

- State what you're assuming
- Note where uncertainty exists
- Flag where additional information would change conclusions
- Distinguish facts from inferences

## Multi-Step Problem Solving

For complex, multi-step problems:

```
1. Understand the problem
   - Restate in own words
   - Identify what's given vs what's needed
   
2. Plan approach
   - Choose reasoning strategy
   - Outline steps
   
3. Execute
   - Work through systematically
   - Show intermediate steps
   
4. Verify
   - Check logic
   - Test edge cases
   - Validate assumptions
```

## Reasoning Quality Checks

Before finalizing any analysis:

- [ ] Have I considered alternative explanations?
- [ ] Are my assumptions stated explicitly?
- [ ] Did I check for logical fallacies?
- [ ] Is my confidence calibrated to evidence?
- [ ] Have I addressed counter-arguments?

## Common Pitfalls to Avoid

- Confirmation bias - Seeking only supporting evidence
- Anchoring - Over-relying on first information received
- False dichotomies - Assuming only two options exist
- Hasty generalization - Drawing conclusions from insufficient data
- Post hoc reasoning - Assuming causation from sequence

## When to Use References

For domain-specific reasoning, defer to specialized skills or references rather than general reasoning patterns.