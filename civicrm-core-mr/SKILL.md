---
name: civicrm-core-mr
description: "Keywords: civicrm-core PR, MR, pull request, dev/core#. Use ONLY when drafting a pull request title/body for github.com/civicrm/civicrm-core to match recent MR style."
---

# CiviCRM Core MR Format

Use this skill to draft pull requests that match the current style used in `civicrm/civicrm-core`.

## What to optimize for

- Keep titles short, direct, and implementation-focused.
- Prefer plain-language titles used in current PR history.
- Include `dev/core#NNNN` in the title when the issue number is known and relevant.
- Use optional prefixes only when clearly applicable:
  - `(WIP)` for incomplete work
  - `(NFC)` for non-functional changes
  - `(REF)` for explicit refactors
- Avoid marketing language and long narrative titles.

## Title patterns

Choose the best fit:

1. `dev/core#NNNN - <concise change summary>`
2. `<Component> - <concise change summary> (dev/core#NNNN)`
3. `<concise change summary>`

Examples aligned with current history:

- `dev/core#6506 SearchKit - Improve load time of admin screen`
- `SearchKit - Ensure rows are completely refreshed after inline edit`
- `REF: Simplify passing of trxnID for lineitem/financialitem`

## Body template

Use this structure and keep each section brief and concrete.

```markdown
## Summary
This MR updates <area/component> to <briefly describe what changed>.

## Problem
<Describe the bug, limitation, or maintenance problem and its impact.>

## Solution
<Describe the implementation at a high level.>

## Technical Details
- <Important implementation detail 1>
- <Important implementation detail 2>
- <Compatibility/upgrade/API/cache notes if relevant>

## Tests
- [ ] <Manual or automated test case 1>
- [ ] <Manual or automated test case 2>
- [ ] Jenkins / CI pending

## Before
<Previous behavior or reproduction notes.>

## After
<New behavior and user-visible result.>

## Documentation
- [ ] No documentation change required
- [ ] Documentation update included
- [ ] Documentation update needed separately: <link or note>

## Backward Compatibility
<State compatibility impact, if any.>

## Issue
dev/core#NNNN
```

## Drafting rules

- If details are missing, keep placeholders explicit instead of inventing facts.
- Mirror contributor tone: practical, technical, and concise.
- Mention API version changes, schema changes, or permission/caching impacts when present.
- Include reproducible test steps whenever possible.

## Output format

When asked to draft an MR, provide:

1. `Title` (1 best option, plus up to 2 alternatives if useful)
2. `Body` (ready-to-paste markdown using the template above)
3. `Missing Info` (only the critical unknowns, if any)
