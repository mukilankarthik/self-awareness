# Contributing to Self-Awareness Skill

Thank you for considering contributing to the Self-Awareness Skill project! This document provides guidelines for contributing.

## How Can I Contribute?

### 1. Report Failure Patterns

Found a systematic failure pattern not covered in the documentation?

**Create an issue with:**
- Clear description of the failure pattern
- Example conversation showing the failure
- Frequency/severity of the issue
- Suggested prevention rule

### 2. Improve Documentation

Help make the reference files clearer and more comprehensive:

- Fix typos or unclear explanations
- Add examples to existing patterns
- Improve formatting or structure
- Add domain-specific failure patterns

### 3. Suggest Enhancements

Have ideas for new checks or improvements?

**Open an issue with:**
- Problem statement (what failure mode this addresses)
- Proposed solution
- Expected behavior change
- Any research/evidence supporting the enhancement

## Pull Request Process

### Before Submitting

1. **Fork the repository** and create a branch from `main`
2. **Test your changes** - Verify the skill still loads correctly
3. **Follow the existing format** - Match the style of existing documents
4. **Update relevant sections** - If you add a new reference file, update README.md

### Pull Request Guidelines

#### Commit Messages

Use clear, descriptive commit messages:

```
Add hallucination pattern for medical diagnosis
Fix typo in confidence-calibration.md
Update verbosity rules with user feedback examples
```

#### PR Title Format

```
[Type] Brief description

Types:
- [Feature] - New functionality or checks
- [Fix] - Bug fixes or corrections
- [Docs] - Documentation improvements
- [Refactor] - Code/content reorganization
```

#### PR Description Template

```markdown
## Problem
[What failure pattern does this address?]

## Solution
[What changes are you proposing?]

## Evidence
[Any research, examples, or observations supporting this?]

## Testing
[How have you verified this works?]
```

### Review Process

1. Maintainers will review your PR within 7 days
2. You may be asked to make changes or provide clarification
3. Once approved, your PR will be merged
4. Your contribution will be acknowledged in the README

## Style Guidelines

### Documentation Style

- **Be specific**: "I invent plausible quotes" not "I sometimes make mistakes"
- **Use examples**: Show the failure, don't just describe it
- **Action-oriented**: Provide clear prevention steps
- **Concise**: Follow the skill's own verbosity rules

### Markdown Formatting

```markdown
## Section Headers (H2)

### Subsections (H3)

**Bold for emphasis** on key terms

`Code formatting` for technical terms

- Bullet points for lists
- Keep consistent spacing
```

### Code Examples

Use fenced code blocks with language specification:

```python
# Python example
import json
data = json.loads('{"key": "value"}')
```

## Adding New Reference Files

If adding a new reference document:

1. **Place in** `self-awareness/references/` directory
2. **Follow naming convention**: lowercase with hyphens (e.g., `new-pattern.md`)
3. **Update SKILL.md**: Add reference to the new file
4. **Update README.md**: Add to documentation table
5. **Use template structure**:

```markdown
# [Pattern Name]

## What This Addresses

[Brief description of the failure pattern]

## Specific Patterns

### Pattern 1
- Description
- Example
- Prevention

### Pattern 2
- Description
- Example
- Prevention

## When to Consult This

[Triggers for referencing this document]
```

## Types of Contributions We Welcome

### High Priority

- **Systematic failure patterns** with research backing
- **Domain-specific hallucinations** (finance, medical, legal, etc.)
- **Cultural communication patterns** for non-Western contexts
- **Measurable improvements** to existing checks

### Welcome

- **Documentation clarity** improvements
- **Additional examples** of existing patterns
- **Translation** to other languages
- **Integration guides** for different platforms

### Not Accepting

- **Personal preferences** without systematic basis
- **Contradictory changes** to core principles
- **Platform-specific features** that break compatibility
- **Marketing content** or promotional material

## Community Standards

### Code of Conduct

- **Be respectful** - Disagree constructively
- **Be specific** - Vague feedback doesn't help
- **Be evidence-based** - Ground suggestions in observation
- **Be collaborative** - This is a shared learning project

### Communication

- **Issues**: For bug reports, feature requests, and discussions
- **Pull Requests**: For contributing actual changes
- **Discussions**: For brainstorming and questions

## Recognition

Contributors will be acknowledged in:
- README.md acknowledgments section
- Git commit history
- Release notes for significant contributions

## Questions?

Open an issue with the `question` label or start a discussion.

---

Thank you for helping make Claude more self-aware and reliable!
