- closes #1036
- closes #1037
- closes #1038
- closes #1039

### Changes Made:
- **`matching.rs`**: Replaced the raw addition inside `isqrt()` with `checked_add` to entirely eliminate `i128::MAX` overflow panics. Also capped the contributor list evaluation to securely guard against permanent DoS locking of the matching pool.
- **`grant_transfer.rs`**: Strengthened `accept_transfer` by strictly gating it behind an `Active` grant state assertion.
- **`invoice.rs`**: Upgraded `validate_line_items` to exclusively compute totals utilizing `checked_mul` instead of raw multiplication operators.
