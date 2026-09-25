- closes #1028
- closes #1029
- closes #1030
- closes #1031

### Changes Made:
- **Insurance Claims**: Enforced a strict `require_admin_auth()` check on `approve_claim` and `reject_claim` to patch the unauthorized access vulnerability.
- **Grant Renewals**: Re-worked the near-completion eligibility gate in `grant_renewal.rs` to enforce strict completion requirements for single-milestone grants, rather than vacuously passing.
- **Evidence Schema**: Implemented caller vs. owner validation in `certify_evidence` to prevent grant owners from self-certifying their own evidence schemas.
- **Dispute Resolution**: Replaced the single-vote dispute resolution threshold with a mathematically rigorous strict majority requirement (`(panel_size / 2) + 1`) based on the assigned arbiter panel size.
