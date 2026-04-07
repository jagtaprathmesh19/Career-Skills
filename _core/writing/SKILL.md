---
name: writing
description: Fast content generation and structured writing skill. Use when tasks require quick drafts, templated content, simple documentation, list creation, or supporting Claude's writing process with initial content generation.
version: 1.0.0
category: _core
agent: gemini
overridable: true
---

# Writing

This skill provides frameworks for creating clear, effective written content across all domains.

## Core Writing Principles

### 1. Know Your Audience

Before writing:
- Who will read this?
- What do they already know?
- What do they need to learn?
- What action should they take?

**Adjust tone accordingly:**
- Technical experts: Use precise terminology, skip basics
- General audience: Explain concepts, avoid jargon
- Executives: Lead with conclusions, support with data
- Beginners: Build up progressively, define terms

### 2. Structure First

Every document needs clear structure:

```
Introduction
├── Hook (why this matters)
├── Context (background)
└── Thesis (main point)

Body
├── Section 1
│   ├── Main point
│   ├── Supporting evidence
│   └── Examples
├── Section 2
└── Section 3

Conclusion
├── Recap main points
├── Implications
└── Call to action (if applicable)
```

### 3. Clarity Over Cleverness

- Use simple words over complex ones
- Use active voice over passive
- Keep sentences under 25 words when possible
- One idea per paragraph
- Remove unnecessary words

**Before:** "The utilization of this methodology facilitates the achievement of superior outcomes."
**After:** "This method produces better results."

## Document Types

### Technical Documentation

**Purpose:** Enable users to accomplish specific tasks

**Structure:**
1. **Overview** - What this does, when to use it
2. **Prerequisites** - What you need first
3. **Steps** - How to do it (numbered, clear)
4. **Examples** - Concrete use cases
5. **Troubleshooting** - Common issues and solutions
6. **Reference** - Detailed parameters/options

**Best practices:**
- Start with quick-start guide
- Use code examples generously
- Include expected output
- Link to related documentation

### Reports and Analysis

**Purpose:** Inform decisions with data and insights

**Structure:**
1. **Executive Summary** - Key findings and recommendations (one page max)
2. **Background** - Context and objectives
3. **Methodology** - How analysis was conducted
4. **Findings** - What the data shows (organized by theme)
5. **Recommendations** - What to do based on findings
6. **Appendix** - Supporting details, raw data

**Best practices:**
- Lead with conclusions
- Use data visualizations
- Clearly separate facts from opinions
- Quantify impact where possible

### Business Communications

**Purpose:** Drive action or convey information efficiently

**Email structure:**
```
Subject: [Action required] + specific topic

Opening: State purpose in first sentence

Body: 
- Context (brief)
- Details (what they need to know)
- Action items (clear, assigned, with deadlines)

Closing: 
- Next steps
- Availability for questions
```

**Best practices:**
- Subject line indicates urgency and topic
- First sentence = why they got this email
- Bullet points for scannability
- Bold key action items
- Keep under 200 words if possible

### User Guides

**Purpose:** Help users learn and use a product/system

**Structure:**
1. **Getting Started** - First-time setup
2. **Core Features** - Main functionality (task-focused)
3. **Advanced Features** - Power user capabilities
4. **FAQ** - Common questions
5. **Glossary** - Terms and definitions

**Best practices:**
- Task-based organization ("How to X")
- Screenshots for visual processes
- Step-by-step instructions
- Tips and warnings in callouts

## Writing Quality Standards

### Editing Checklist

**First pass - Structure:**
- [ ] Clear introduction stating purpose?
- [ ] Logical flow of sections?
- [ ] Each section has clear focus?
- [ ] Conclusion summarizes key points?

**Second pass - Clarity:**
- [ ] Removed unnecessary jargon?
- [ ] Defined technical terms?
- [ ] Active voice used primarily?
- [ ] Sentences clear and concise?

**Third pass - Polish:**
- [ ] Spelling and grammar correct?
- [ ] Consistent formatting?
- [ ] Links working?
- [ ] Examples accurate?

### Common Writing Issues

**Wordiness:**
```
❌ "In order to achieve the goal of..."
✅ "To achieve..."

❌ "Due to the fact that..."
✅ "Because..."

❌ "At this point in time..."
✅ "Now..."
```

**Passive voice:**
```
❌ "The report was written by the team."
✅ "The team wrote the report."

❌ "Mistakes were made."
✅ "We made mistakes."
```

**Unclear antecedents:**
```
❌ "When using the API with the database, it may fail."
   (Which fails? API or database?)
✅ "The API may fail when connecting to the database."
```

## Style Guidelines

### Headings
- Use sentence case
- Keep descriptive and specific
- Maintain parallel structure in lists

### Lists
- Use bullets for unordered items
- Use numbers for sequential steps
- Maintain parallel grammatical structure
- Keep list items concise

### Code and Technical Terms
- Use `code blocks` for commands, file names, variables
- Indent code examples consistently
- Provide context before showing code
- Explain what code does, not just what it is

## Tone Calibration

**Formal (academic, legal, official):**
- Avoid contractions
- Use complete sentences
- Third person perspective
- Precise terminology

**Professional (business, technical docs):**
- Balanced tone
- Clear and direct
- Some contractions acceptable
- Focus on clarity

**Conversational (blogs, guides, tutorials):**
- Use "you" and "we"
- Contractions welcome
- Shorter sentences
- Personal examples OK

## Domain-Specific Writing

### API Documentation
- Endpoint, method, parameters table
- Request/response examples
- Error codes and meanings
- Rate limits and authentication

### README Files
- Project description (one paragraph)
- Installation instructions
- Quick start example
- Link to full documentation

### Change Logs
```
## [Version] - Date
### Added
- New features

### Changed
- Modified behavior

### Fixed
- Bug fixes

### Removed
- Deprecated features
```

## Accessibility Considerations

- Use descriptive link text (not "click here")
- Provide alt text for images
- Ensure sufficient contrast
- Use heading hierarchy properly
- Keep language simple and clear

## Final Review Questions

Before publishing:
- Does this accomplish its purpose?
- Would the target audience understand it?
- Is anything missing that readers need?
- Can any section be cut without losing value?
- Are examples helpful and accurate?