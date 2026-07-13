# Contribution 1: This Door Doesn't Have an Inhand Icon State

**Contribution Number:** 1
**Student:** Yakubu Mohammed Abasss  
**Issue:** https://github.com/DarkPack13/SecondCity/issues/515  
**Status:** Phase III Complete

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

I created a fork of the SecondCity repository and reviewed the issue description and maintainer comments. The maintainer indicated that the issue is likely caused by missing or incorrect `icon_state`, `worn_icon_state`, or `inhand_icon_state` assignments rather than missing sprite assets. Before making any code changes, I plan to inspect the item definition and verify that the assigned sprite state names match those available in the corresponding sprite files.

### Steps to Reproduce

1. Launch the game and connect to a local test server.
2. Spawn or obtain a door shield item.
3. Pick up the door shield and hold it in hand.
4. Observe the item's appearance while it is held.
5. Verify whether the expected inhand sprite is displayed.
6. Inspect the item definition and compare the assigned `icon_state`, `worn_icon_state`, and `inhand_icon_state` values with the available sprite names in the corresponding `.dmi` files.
7. Confirm that the issue occurs because the item is missing a valid inhand icon state assignment or references an incorrect sprite state.

### Reproduction Evidence

- **Commit showing reproduction:** https://github.com/baabass1/SecondCity/tree/fix-door-shield-inhand-icon
- **Screenshots/logs:** https://github.com/DarkPack13/SecondCity/issues/515
- **My findings:** The issue appears to be caused by missing or incorrect `icon_state`, `worn_icon_state`, or `inhand_icon_state` assignments. The maintainer indicated that the required sprites already exist, so the fix will likely involve matching the icon state assignments to the correct sprite names in the relevant `.dmi` files.

---

## Solution Approach

### Analysis

The problem is caused by missing or incorrect `icon_state`, `worn_icon_state`, or `inhand_icon_state` assignments for the door shield item. The required sprite assets appear to already exist, so the issue is likely a mismatch between the assigned icon state names and the sprite names available in the corresponding `.dmi` files.


### Proposed Solution

Review the door shield item definition and verify that its icon state assignments match existing sprite names. If any assignments are missing or incorrect, update them to reference the correct sprite states. After making the changes, test the item in-game to confirm that the correct inhand sprite is displayed when the item is held.

### Implementation Plan

Using UMPIRE framework (adapted):

**Understand:** The door shield item does not display the correct inhand icon when held. The issue is caused by missing or incorrect icon state assignments.

**Match:** Many items in the codebase already define `icon_state`, `worn_icon_state`, and `inhand_icon_state` values that correspond to sprite names in `.dmi` files. The door shield should follow the same pattern.

**Plan:** [Step-by-step implementation plan]
1. Locate the door shield item definition in the codebase.
2. Identify the current `icon_state`, `worn_icon_state`, and `inhand_icon_state` assignments.
3. Find the corresponding sprite definitions in the relevant `.dmi` files.
4. Verify that the required sprite states already exist.
5. Update any missing or incorrect icon state assignments.
6. Test the item in-game to confirm the correct sprite appears when held.
7. Check whether related door shield items have similar issues.

**Implement (Branch):** https://github.com/baabass1/SecondCity/tree/fix-door-shield-inhand-icon

**Review:** 
- Follow the project's contribution guidelines.
- Keep the fix limited to the affected item definitions.
- Avoid modifying sprite assets unless necessary.
- Verify that changes do not affect unrelated items.
- Ensure code style matches existing project conventions.

**Evaluate:** 
- Spawn or obtain a door shield item.
- Hold the item in hand and verify that the correct inhand sprite is displayed.
- Confirm that no runtime errors or visual issues occur.
- Compare behavior before and after the fix to verify the issue is resolved.

---

## Testing Strategy

### Planned Unit Tests

- **Test case 1:** Verify that the door shield has valid `icon_state` and `inhand_icon_state` assignments.
- **Test case 2:** Verify that the assigned icon states correspond to existing sprite states in the appropriate `.dmi` file.
- **Test case 3:** Verify that the door shield correctly displays its in-hand sprite after the `inhand_icon_state` assignment is added.

### Planned Integration Tests

- **Integration scenario 1:** Spawn or obtain a door shield in-game and confirm that the correct in-hand sprite is displayed when the item is held.
- **Integration scenario 2:** Verify that the fix does not affect the door shield's inventory icon or other door shield variants.

### Manual Testing

- **Test:** Reviewed the GitHub issue description and maintainer comments.  
  **Result:** Confirmed that the issue is caused by a missing `inhand_icon_state` assignment rather than missing sprite assets.

- **Test:** Reviewed the maintainer's documented reproduction steps.  
  **Result:** Confirmed the expected workflow for reproducing and verifying the issue in-game.

- **Test:** Inspected the affected source file (`modular_darkpack/modules/doors/code/door_item.dm`) and related sprite references.  
  **Result:** Verified that the existing sprite assets already exist and only the missing `inhand_icon_state` assignment was required.

- **Test:** Reviewed the implemented code change after adding `inhand_icon_state = "door"`.  
  **Result:** Confirmed that the fix is isolated to the affected door shield item and does not modify unrelated files.

- **Test:** Attempted to build and test the project locally on macOS.  
  **Result:** The build could not be completed because the project downloaded a Linux (ELF) version of the Hypnagogic icon cutter, which cannot execute on macOS. The code change was therefore verified through source code inspection and comparison with the maintainer's issue description rather than in-game execution.

---

## Implementation Notes


### Week [4] Progress

- Forked the repository and created the development branch `fix-door-shield-inhand-icon`.
- Reviewed the issue description, maintainer comments, and relevant project documentation.
- Documented the issue summary, reproduction process, solution approach, implementation plan, and testing strategy in the contribution README.
- Identified the components likely involved in the fix, including the door shield item definition and related sprite state assignments.
- Decided to keep the fix limited to correcting existing icon state assignments rather than modifying sprite assets.

### Week [5] Progress

- Locate the door shield item definition in the codebase.
- Verify the current `icon_state`, `worn_icon_state`, and `inhand_icon_state` assignments.
- Compare the assigned values with the available sprite names in the corresponding `.dmi` files.
- Update any missing or incorrect icon state assignments.
- Test the changes in-game to verify that the correct inhand sprite is displayed.
- Check related door shield items for similar issues.

## Code Changes

**Files modified:**
- `modular_darkpack/modules/doors/code/door_item.dm` – Added the missing `inhand_icon_state` assignment for the door shield item.

**Key commits:**
- `8d37b5f0426` – **Fix missing inhand icon state for door shield**

**Approach decisions:**
- Kept the fix limited to `modular_darkpack/modules/doors/code/door_item.dm` to avoid modifying unrelated files.
- Reused the existing sprite assets instead of creating new sprite files because the required assets already exist.
- Added the missing `inhand_icon_state` assignment to match the existing `icon_state`.
- Chose a minimal, targeted fix based on the maintainer's description of the issue to reduce the risk of introducing regressions.
 
## Challenges Faced

**Challenge:** I attempted to build and test the project locally on macOS, but the build failed because the project downloaded a Linux (ELF) version of the Hypnagogic icon cutter, which cannot execute on macOS.

**Resolution:** I verified that the code change itself was isolated to `modular_darkpack/modules/doors/code/door_item.dm`, documented the platform limitation, completed manual verification through code inspection and the maintainer's reproduction steps, and pushed the fix for maintainer review.

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
