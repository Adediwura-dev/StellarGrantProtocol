- closes #1032
- closes #1033
- closes #1034
- closes #1035

### Changes:
- Bounded loops in `refund_all` and `release_to_funders` by implementing pagination/chunking to remove DoS risk.
- Widened the `hash_tag` algorithm output in `grant_tags` to prevent index collisions.
- Modified `refund_all` to track exact remaining balance iteratively, preventing stranded dust rounding errors.
- Restored missing offset/pagination logic in `funder_report` to properly yield results beyond the 1,000 grant hard-limit.
