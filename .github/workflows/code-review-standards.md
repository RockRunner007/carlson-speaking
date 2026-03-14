# Guidance Review Standards

Guidelines for reviewing speaking guidance, specifications, and other markdown content.

## Review Objectives

1. **Accuracy** - Is the guidance factually and logically correct?
2. **Clarity** - Is the guidance easy to understand and follow? Is the language simple and direct?
3. **Tone** - Is the communication style appropriate for the intended audience and persona?
4. **Structure** - Is the document well-organized with clear headings and logical flow?
5. **Consistency** - Does the guidance align with existing content and project standards?

## Reviewing Guidance & Specifications

### Content Review Checklist

- [ ] **User Stories Clear** - Is the objective of the speaking guidance clear?
- [ ] **Actionable Advice** - Is the guidance practical and can it be applied?
- [ ] **Persona Alignment** - Does the content match the target persona's needs and perspective?

### Example Spec Review Comment

```text
## Issue: Tone is not aligned with persona

**Guidance:**
> "Just tell the executive the project is delayed."

**Problem:** This tone is too blunt for the 'Boss' persona. It lacks context and reassurance.

**Suggestion:**
> "Let's rephrase this for the 'Boss' persona. Consider: 'We need to proactively inform the executive about a revised timeline, highlighting the risk mitigation and the new expected delivery date.'"
```

### Approval Requirements

**Minimum reviewers:**

- Content: 1 approval
- Governance/Process: 2 approvals

## Reviewing Pull Requests

### PR Description Review

Check that PR description includes:

- [ ] **Title** - A clear, concise summary of the change.
- [ ] **Description** - What changed and why?
- [ ] **Related Spec/Issue** - A link to the relevant specification or issue.

## Review Process

### Step 1: Author Submits PR

- [ ] PR description complete
- [ ] Self-reviewed before submitting

### Step 2: Automated Checks

- [ ] Linting passes
- [ ] Security scan clean
- [ ] No conflicts with main

-### Step 3: Peer Review

- [ ] 1st reviewer reviews and comments
- [ ] 2nd reviewer reviews and approves
- [ ] Author responds to comments
- [ ] If requested changes: author updates and requests re-review

### Step 4: Merge

- [ ] All automated checks passing
- [ ] All review conversations resolved
- [ ] Minimum approvals received

## Reviewing Content

**Focus on:**

- Clarity - Can a newcomer understand?
- Accuracy - Is information correct?
- Completeness - Are all edge cases covered?
- Examples - Do examples work as shown?

## Difficult Reviews

### Disagreement on Style or Tone

**Don't say:**
> "This is written poorly."

**Say:**
> "I think we can align the tone more closely with the 'Cynic' persona. For example, instead of 'This is a great idea,' we could try 'This might work, but have we considered the potential downsides?' What do you think?"

## Red Flags

**Block approval if:**

- Hardcoded secrets/credentials
- Security vulnerability
- Breaks existing links/structure
- No spec/issue linked

**Request changes if:**

- Poor documentation
- Violates style guide or naming conventions
- Tone is misaligned with the target persona
- The purpose of the change is not clear from the PR description

## Praise & Recognition

**Good review includes:**

- Acknowledgment of good solutions
- Explanation of why approach is good
- Appreciation for testing
- Recognition of effort

**Example:**
> Great solution using memoization! This is much cleaner than the previous approach and improves performance by 40%. Thanks for adding comprehensive tests - the coverage is excellent.

## Review Metrics

Track per month:

| Metric | Target | Action |
|--------|--------|--------|
| Review time | < 24h | Prioritize |
| Approval rate | 90%+ | Ensure quality |
| Revision rate | < 30% | Improve reviews |
| Rework cycles | < 2 | Clear feedback |

## References

- [Code Review Best Practices](https://google.github.io/eng-practices/review/)
- [Conventional Commits](https://www.conventionalcommits.org/)
- [Spec-Kit](https://github.com/github/spec-kit)
