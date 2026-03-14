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
- [ ] **Acceptance Criteria Testable** - Can QA verify these?
- [ ] **Dependencies Listed** - What does this depend on?

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

**Automatic failures:**
- [ ] Linting errors

## Reviewing Pull Requests

### PR Description Review

Check that PR description includes:

- [ ] **Title** - Clear, concise summary
- [ ] **Spec Link** - Link to related specification
- [ ] **Changes** - What changed and why?
- [ ] **Testing** - How was this tested?
- [ ] **Breaking Changes** - Any migrations needed?
- [ ] **Screenshots** - Visual changes shown (if UI)

### Example PR Description

```text
## Title
Fix: Prevent duplicate session creation on rapid login

## Spec
Implements: [001-authentication/spec.md](link)

## Changes
- Added mutex lock to login endpoint
- Prevents multiple simultaneous logins creating multiple sessions
- Only first login succeeds, others get 409 Conflict

## Testing
- Added integration test for concurrent logins
- Verified on staging with 100 concurrent users
- No performance impact (lock acquired for ~10ms)

## Breaking Changes
None - Only affects invalid (concurrent) requests

## Deploy Notes
- No database migration needed
- Safe to deploy anytime
```

## Review Process

### Step 1: Author Submits PR

- [ ] PR description complete
- [ ] All tests passing locally
- [ ] Self-reviewed before submitting

### Step 2: Automated Checks

- [ ] Linting passes
- [ ] Tests pass
- [ ] Security scan clean
- [ ] No conflicts with main

### Step 3: Code Review

- [ ] 1st reviewer reviews and comments
- [ ] 2nd reviewer reviews and approves
- [ ] Author responds to comments
- [ ] If requested changes: author updates and requests re-review

### Step 4: Merge

- [ ] All checks passing
- [ ] All conversations resolved
- [ ] Minimum approvals received
- [ ] Ready to deploy

## Reviewing Different Types of Changes

### Feature Implementation

**Focus on:**

- Spec completeness - All acceptance criteria met?
- Code quality - Is it maintainable?
- Test coverage - Edge cases tested?
- Performance - Will this scale?

### Bug Fix

**Focus on:**

- Root cause - Is this fixing the real issue or symptom?
- Regression - Could this break other things?
- Test - Includes test that prevents regression?

### Documentation

**Focus on:**

- Clarity - Can a newcomer understand?
- Accuracy - Is information correct?
- Completeness - Are all edge cases covered?
- Examples - Do examples work as shown?

## Difficult Reviews

### Disagreement with Approach

**Don't say:**
> "This approach is wrong"

**Say:**
> "I see this approach could work. I have concerns about X because Y.
> Have you considered Z approach? Here's a link to more info."

### Performance Concerns

Provide evidence:

```text
I notice this query could be slow with 100,000 records.

Before optimization:
SELECT * FROM transactions 
WHERE user_id IN (...) -- 500 IDs
-- Full scan of transactions table

After optimization:
SELECT * FROM transactions 
WHERE user_id IN (...) 
AND created_at > NOW() - INTERVAL 90 DAY
-- Uses index on (created_at, user_id)

This should reduce query time from 2s to 50ms.
Can you add this date filter to spec?
```

### Security Issues

Be specific:

```text
## Security: SQL Injection Risk

The query uses string concatenation:
```sql
query = "SELECT * FROM users WHERE email = '" + email + "'"
```

If email = `' OR '1'='1`, this executes malicious SQL.

Solution: Use parameterized queries:

```javascript
db.query('SELECT * FROM users WHERE email = ?', [email])

See: [OWASP SQL Injection](link)
```

## Red Flags

**Block approval if:**

- Hardcoded secrets/credentials
- Security vulnerability
- Breaks existing links/structure
- No spec/issue linked

**Request changes if:**

- Poor documentation
- Violates naming conventions
- Performance degradation
- Missing error handling
- Incomplete spec implementation

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
