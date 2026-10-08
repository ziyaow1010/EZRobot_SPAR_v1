# Zyra v1 editing notes

## Positioning

Product name: Zyra. Agreed title: **Zyra: A Zero-Shot Robot Manipulation Agent with Sparse Action Programs**. Zyra is a standalone name, not a forced acronym. Legacy `spar` package names and historical archive/revision identifiers remain unchanged for reproducibility.

The central claim is a VLM-centered alternative to VLA and WAM architectures: measured geometry and sparse programs connect a general-purpose foundation model to robot execution. The vision is broader than the evidence of the first-generation report. The report leads with the route, followed by zero-shot capability and robustness, then deployment economics.

The title, EZRobot branding, and the existing sole author are provisional; supply the legal company name, full authorship, affiliations, contact information, and release URL before publication. No additional author identity is guessed.

## Sources used

- Supplied archive `SPAR-main (1).zip`, source snapshot `3b298125fab3f9db4234648853329459010d1b3a`.
- Its README, `docs/results.md`, hardware setup, configs, and open-agent implementation.
- The user's statement that zero-shot execution already works on real laboratory hardware. The draft does not invent trial counts or task diversity from that statement.
- Guava arXiv v3, Table 3: https://arxiv.org/html/2606.18363v3 . Baseline table values were checked against this primary source on October 8, 2026. Guava's title changed from its earlier version; the bibliography uses the current title.
- Primary arXiv papers for OpenVLA, DreamZero, Code as Policies, CaP-X, LIBERO, LIBERO-PRO, and LIBERO-Plus.

## Quantitative provenance

- Standard v9: 89/100 standard success, 87/100 final-state; Spatial/Object/Goal/Long 22/25, 25/25, 20/25, 22/25. Revision `600fe26`.
- PRO v9: 49/50, 50/50, 42/50, 41/50, 40/50, 46/50 in Object Pos/Task, Goal Pos/Task, Spatial Pos/Task order. Total 268/300. Final-state total 260/300. Revision `01215c2`.
- PRO aggregates calculated from integer counts: position 131/150 = 87.33%; task 137/150 = 91.33%; overall 89.33%.
- Standard v9 is a development-linked sample reused from the v8 comparison; do not call it a fresh held-out test.
- Earlier pick-place 99/100, PRO 45/50, Plus 85/100 are kept separate. Do not attribute them to open-agent v9.
- Current open-agent Plus results are not in the supplied archive. The user's approximate latest result is not substituted for a counted run; insert the new manifest and results when supplied.
- Costs are CLI/API-equivalent estimates, not actual billed amounts. No current v9 latency distribution is fabricated.

## Highest-value next inputs

1. Updated full-protocol tables, evaluation revisions, exact served models, raw records, and task manifests.
2. Real-robot task list, trial denominator, successes, interventions, and original videos or frames.
3. Current open-agent Plus results by perturbation family.
4. Latency decomposition and percentiles, billing basis, and total cost per success.
5. Controlled ablations and a same-model comparison with alternative harnesses.
6. Confirm whether the full report should include the older pick-place route in the main text or move it to supplementary material after open-agent hardware validation.

## Draft-specific points to revisit

Formal measurement provenance, collision guarantees, and contact-force interpretation are not implemented claims. The draft does not repeat universal statements that every VLA or WAM fails to generalize; it states the architectural hypothesis and cites specific robustness evidence.

Execution issues from the earlier code review should be tracked as engineering work rather than part of the product story: nominal waypoint validation does not recheck the extra 10 cm until-blocked target, and an ordinary waypoint abort may still apply that waypoint's gripper transition before skipping subsequent moves. The real backend has a separate workspace guard. These are not claimed causes of all recorded failures.

Overleaf's GitHub integration may require an explicit pull after a GitHub merge. No automatic synchronization is assumed.
