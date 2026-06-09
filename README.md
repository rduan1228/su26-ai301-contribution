# su26-ai301-contribution
# Contribution [1]: feat: Add top-level daft.concat() for concatenating multiple DataFrames #6892

**Contribution Number:** 1
**Student:** Ran Duan
**Issue:** [[GitHub issue link]](https://github.com/Eventual-Inc/Daft/issues/6892)  
**Status:** [Phase I] [In Progress]

---

## Why I Chose This Issue

Having worked with Spark and Databricks, I've personally hit this exact pain point — looping through DataFrames to concatenate them is a common and annoying pattern in real pipelines. This issue is also a great entry point into the Daft codebase: well-scoped, pure Python, and the implementation path is already clear from the issue description.
---

## Understanding the Issue

### Problem Description

No top-level daft,concat() exists. users must manually loop and chain df.concat(other) calls to combine multiple DataFrames. 

### Expected Behavior

daft.concat([df1, df2, df3) returns a single concatenated DataFrame, similar to pd.concat() in pandas.

### Current Behavior

Users must write:
result = dfs[0]
for df in dfs[1:]:
    result = result.concat(df)

### Affected Components

daft/__init__.py - expose the new top-level function
DataFrame.concat() - existing method that the new function wraps
Tests - new test coverage for teh top-level API
---

## Reproduction Process

### Environment Setup

[Notes on setting up your local development environment - challenges you faced, how you solved them]

### Steps to Reproduce

1. [Step 1]
2. [Step 2]
3. [Observed result]

### Reproduction Evidence

- **Commit showing reproduction:** [Link to commit in your fork]
- **Screenshots/logs:** [If applicable]
- **My findings:** [What you discovered during reproduction]

---

## Solution Approach

### Analysis

[Your analysis of the root cause - what's causing the issue?]

### Proposed Solution

[High-level description of your fix approach]

### Implementation Plan

Using UMPIRE framework (adapted):

**Understand:** [Restate the problem]

**Match:** [What similar patterns/solutions exist in the codebase?]

**Plan:** [Step-by-step implementation plan]
1. [Modify file X to do Y]
2. [Add function Z]
3. [Update tests]

**Implement:** [Link to your branch/commits as you work]

**Review:** [Self-review checklist - does it follow the project's contribution guidelines?]

**Evaluate:** [How will you verify it works?]

---

## Testing Strategy

### Unit Tests

- [ ] Test case 1: [Description]
- [ ] Test case 2: [Description]
- [ ] Test case 3: [Description]

### Integration Tests

- [ ] Integration scenario 1
- [ ] Integration scenario 2

### Manual Testing

[What you tested manually and results]

---

## Implementation Notes

### Week [X] Progress

[What you built this week, challenges faced, decisions made]

### Week [Y] Progress

[Continue documenting as you work]

### Code Changes

- **Files modified:** [List]
- **Key commits:** [Links to important commits]
- **Approach decisions:** [Why you chose certain approaches]

---

## Pull Request

**PR Link:** [GitHub PR URL when submitted]

**PR Description:** [Draft or final PR description - much of the content above can be adapted]

**Maintainer Feedback:**
- [Date]: [Summary of feedback received]
- [Date]: [How you addressed it]

**Status:** [Awaiting review / Iterating / Approved / Merged]

---

## Learnings & Reflections

### Technical Skills Gained

[What you learned technically]

### Challenges Overcome

[What was hard and how you solved it]

### What I'd Do Differently Next Time

[Reflection on your process]

---

## Resources Used

- [Link to helpful documentation]
- [Tutorial or Stack Overflow post that helped]
- [GitHub issues or discussions that helped]
