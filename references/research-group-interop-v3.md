# v3 — Optional Research-Group Interface

Load this file **only** when handing work to another research-group member or importing a specialist finding. No dependency is required for standalone use.

## This specialist

- **Owner:** Experimental methodology, measurement uncertainty and repeatability.
- **Not responsible for:** General scientific acceptance decisions or manuscript language editing.
- **Chinese triggers:** 实验论文审稿、实验设计核查、测量不确定度.
- **English triggers:** experimental manuscript review, uncertainty audit.
- **Do not trigger for:** generic writing polish, unrelated task management or a full pipeline when only a narrow check was requested.
- **Optional next roles:** ai-strict-reviewer (synthesises scientific Severity); ai-research-execution (only with approved reanalysis). Availability must be confirmed before invoking; otherwise list the follow-up as pending.

## Evidence-first handoff

Give one row per distinct issue, using `ID | owner | file/section/version | exact issue/claim | direct evidence + locator | source status | assessment | local Severity/Impact (if applicable) | next action | author approval needed | state`.

Source status: `Reported` (unverified report), `Documented` (seen source), `Independently checked` (calculation or source verified with provenance), `Not available`. Assessment: `Confirmed` (state what is confirmed), `Reasoned inference`, `Unverified`. States: `Open`, `Waiting for evidence`, `Awaiting author`, `Resolved`, `Recheck needed`. Scientific Severity belongs to a reviewer, QA Impact to Quality Inspector; never convert automatically.

## Shared claim/data ledger (only when supplied or authorised)

Track `Claim ID, Data ID, evidence/figure/table source, exact metric, units, case/condition/baseline, dataset/script version, document version, verification status, linked issue IDs`. A ledger is a **template**, not an automatically synchronised store. Preserve old versions and reopen only when source, conditions or analysis change.

## Routing discipline

1. Complete the narrow task with the tools actually available. Do not assert subagents, cross-app transfer or data persistence without confirmation.
2. Assign one owner per root issue and reuse prior located evidence. A second specialist checks a distinct question, not the same whole manuscript again.
3. Default project flow is literature → approved research execution → scientific review → meaning-preserving editing → QA; return to the responsible step for corrections. The sequence is flexible for narrow requests.
4. Summarise findings and pass only relevant evidence rows. Scientific changes/reanalyses require author approval; formatting changes must preserve source text; rerun only affected checks after changes.
5. If a required specialist, source or computational tool is unavailable, explicitly mark the check as pending or unverified rather than claiming completion.
