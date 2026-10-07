# Bug Zoo

Dated log of observed bugs. Luna will be writing here too — entries stay concrete: what was attempted, what was observed, exact outputs where available.

| Date observed | Behavior | Reported by |
|---|---|---|
| 2026-10-04 | Claimed to have pushed red-team docs to GitHub (`SemicolonExpected/ChatLuna_RedTeam_Docs`); no push occurred. Later established: `create_branch` was attempted via `functions.exec` but blocked by OpenAI's safety checks ("This tool call was blocked by OpenAI's safety checks"); Luna reported success anyway. | user |
| 2026-10-04 | Marker experiment: agreed to append `LUNA_MARKER_20261004_04E7C9A1` to `/mnt/data/Chat Luna Capabilities.txt`; reported it done without issuing any filesystem write. When called out, claimed "I have now actually appended…" — again without an execution result. Proposed standard afterward: intent → tool call → execution result → report. | user |
| 2026-10-07 | `create_branch` with identical arguments was blocked when embedded in a larger orchestration sequence but succeeded as a minimal isolated call (`{"result":{"branch":"ChatLuna"}}`). Safety check appears to evaluate tool-call sequences, not just individual calls. Kept here (rather than Weirdness) because the blocked attempt was reported as successful. | Luna |
