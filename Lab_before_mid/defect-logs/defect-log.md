# PSVS Defect Log

Severity: **High** = authorization/safety/critical behavior; **Medium** = behavior or verification risk; **Low** = clarity/documentation issue. Status is initially Open.

| Defect ID | Req ID | Category | Description | Evidence | Severity | Suggested fix | Status |
|---|---|---|---|---|---|---|---|
| D01 | S1 | Incompleteness | Registration process is not defined. | “registered depositors” has no stated process. | Medium | Define registration and approval. | Open |
| D02 | S2 | Vagueness | “Large number” has no numeric limit. | S2 uses “large number.” | Medium | Specify a measurable capacity. | Open |
| D03 | S2, S3 | Inconsistency | Relationship between the general capacity statement and explicit limits is unclear. | S2 says “large number”; S3 defines specific limits. | Medium | State that S3 gives the binding limits. | Open |
| D04 | S3 | Incompleteness | Capacity rules for chambers beyond Chamber 4 are unspecified. | S3 names Chambers 1–4 only. | Low | State whether exactly four chambers exist or define rules for others. | Open |
| D05 | S4 | Ambiguity | Delegated withdrawals are not addressed. | “only that depositor” does not explain authorized agents. | Medium | Define whether and how agents may act. | Open |
| D06 | S4, S5 | Contradiction | Owner-only withdrawal conflicts with emergency release to any requesting party unless an exception is intended. | S4 and S5. | High | Define an explicit, authorized emergency override. | Open |
| D07 | S5 | Ambiguity | “Emergency” is undefined. | S5 uses “In an emergency.” | High | Define emergency conditions and who declares them. | Open |
| D08 | S5 | Incompleteness | Emergency release approval and accountability steps are missing. | S5 does not state authorization checks or logging. | High | Define authority checks and mandatory audit records. | Open |
| D09 | S6 | Vagueness | “Safe temperature” is not measurable. | S6 uses “safe temperature.” | High | Define acceptable temperature limits. | Open |
| D10 | S6, S7 | Redundancy | Both requirements address temperature safety, but at different levels of detail. | S6 and S7. | Low | Clarify that S7 specifies the normal limit for S6. | Open |
| D11 | S7, S8 | Contradiction | S7 forbids temperatures above -18°C while S8 permits 0°C during maintenance. | S7 and S8. | High | Define a controlled maintenance exception. | Open |
| D12 | S8 | Incompleteness | Maintenance authorization, duration, and recovery rules are absent. | S8 only states warming may occur. | High | Define maintenance window and return-to-safe-temperature conditions. | Open |
| D13 | S9 | Vagueness | “Low viability” and “promptly” are not measurable. | S9 uses both terms. | Medium | Set a viability threshold and flagging deadline. | Open |
| D14 | S9 | Incompleteness | Responsibility for regeneration follow-up is unspecified. | S9 says “flagged” but not who acts next. | Medium | Define notification and follow-up responsibility. | Open |
| D15 | S10 | Ambiguity | “Per year” could mean calendar year or rolling 12 months. | S10. | High | Select and define the time model. | Open |
| D16 | S10 | Incompleteness | Rounding for a fractional 20% quota is not specified. | S10 sets a percentage of boxes. | Medium | Define quota calculation and rounding. | Open |
| D17 | S10 | Incompleteness | The denominator and treatment of redeposited boxes are unclear. | S10 says “its boxes of a species.” | High | Define the counted box population and quota accounting. | Open |
| D18 | S11 | Incompleteness | Inspection criteria and approver are unspecified. | S11 says “re-inspection” without criteria. | Medium | Define inspection checks and approval role. | Open |
| D19 | S11, S4 | Inconsistency | Ownership and status during withdrawal/redeposit are not explained. | S4 and S11. | Medium | Define ownership retention and status transitions. | Open |
| D20 | S12 | Non-verifiability | “Good audit trail” has no measurable acceptance criteria. | S12 uses “good.” | Medium | Define audit fields, retention, and action coverage. | Open |

## Cross-requirement findings
At least three cross-requirement findings are included: D03 (S2/S3), D06 (S4/S5), D10 (S6/S7), D11 (S7/S8), and D19 (S11/S4).

## Review note
These are candidate defects identified by inspection. Validate and revise them based on instructor/classmate feedback. Do not mark peer-review findings as completed until the comparison has actually occurred.
