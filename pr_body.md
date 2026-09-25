- closes #1040
- closes #1041
- closes #1042
- closes #1047

### Changes Made:
- **`reviewer_reward`**: Wired up the `accrue_reward` dead code logic to correctly distribute reward pool funds.
- **`migration`**: Added a strict monotonicity check in `run_migration` to reject older or identical target versions, preventing desync.
- **`milestone_template`**: Replaced the unbounded scan in `public_templates()` with a paginated index map to mitigate cheap private-template spam.
- **`open_review`**: Enforced the missing registration requirement check inside `submit_review` as promised by the doc-comments.
