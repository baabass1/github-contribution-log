# Contribution 1: This Door Doesn't Have an Inhand Icon State

**Contribution Number:** 1
**Student:** Yakubu Mohammed Abasss  
**Issue:** https://github.com/DarkPack13/SecondCity/issues/515  
**Status:** Phase I Complete

---

## Why I Chose This Issue

I chose this issue because it provides an opportunity to contribute to a large and long-running open-source project with an active development community. SecondCity is a complex game project that combines programming, asset management, and collaborative development, making it an excellent environment for learning how large software systems are maintained and improved.

This issue is well-scoped and beginner-friendly, which makes it a good starting point for understanding the project's structure and development workflow. I am particularly interested in learning how item definitions, sprites, and visual states are connected within the codebase and how developers track down and resolve issues that affect gameplay. By working on this issue, I hope to strengthen my skills in debugging, code investigation, and contributing effectively to a collaborative open-source project.

---

## Understanding the Issue

### Problem Description

The door shield item is missing a valid inhand icon state. As a result, the item does not display correctly when a player holds it. According to the maintainer, the required sprite already exists, but the item's icon state assignments do not correctly reference it.

### Expected Behavior

The door shield should display the correct sprite when held in a player's hand. The item's `icon_state`, `worn_icon_state`, and `inhand_icon_state` values should match the corresponding sprite names defined in the sprite files.

### Current Behavior

When a player picks up the door shield, the expected inhand icon is not displayed. This occurs because the item is missing a valid inhand icon state assignment or the assigned state does not match the available sprite names.

### Affected Components

- Door shield item definition
- `icon_state` assignments
- `worn_icon_state` assignments
- `inhand_icon_state` assignments
- Related sprite (`.dmi`) files containing the door shield icons

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
