# Independent final read-only QC: V59B vs V61A/B/C

**2026-11-15, Europe/Istanbul.** Reviewed real Mac PNGs (554 × 554) at native size, the existing pixel-nearest `V57C_V59B_V61_4X_COMPARE.png` for the face/head/neck, and independently recalculated pixel differences plus SHA-256 from the actual files. No image edits or generation performed.

**Recommendation: V61B is the safest provisional choice among V61A/B/C. Do not certify as 9/10; overall customer-quality gate remains NO-GO.** V61B retains the prior V59B upper edge cleanup but reduces the abrupt lower-row transition to negligible 1 RGB code value at y154 and zero at y155. Visual review shows no new rectangular neck/shoulder patch resembling rejected V60. Residual scalp/ear/cheek/jaw compositing halo remains and must be distinguished from the repaired lower boundary.

| Candidate | Photo /10 | Head-edge naturalness /10 | y154 max channel delta vs unchanged V57C | Verdict |
|---|---:|---:|---:|---|
| V59B | 6.9 | 6.4 | **39** then 0 at y155 | Old abrupt lower cutoff remains |
| V61A | 6.8 | 6.5 | **0** then 0 | Most aggressive/earliest fade (starts y137); risks reintroducing more of original lower cheek/jaw halo |
| **V61B** | **7.0** | **6.7** | **1** then 0 | **Safest balance:** smooth lower termination with less reversion of V59B's original edge cleanup |
| V61C | 6.9 | 6.5 | **1** then 0 | Latest/steepest fade (starts y146); still a more visible transition above cutoff at 147–151 |

Scores are conservative, subjective visual judgments, not machine-certified realism. Differences are subtle at native resolution; none passes strict photorealistic delivery thresholds.

## Pixel-verified boundary findings

- **V59B→V61A** changed 315 pixels, bounding box x220–251/y139–154; **V61B** changed 143 pixels, bounding box x220–242/y144–154; **V61C** changed 114 pixels, bounding box x220–242/y147–154. No large rectangular region was changed in the shoulder or body.
- For each candidate, all pixels **from y155 downward** match V59B exactly; neck/shoulder x110–315, y160–230: **0 changed pixels**; facial interior x200–228, y78–129: **0**; fish, hands, net and water y235 onward: **0**. This specifically rules out a **new** V60-type patch introduced by V61 in those protected regions.
- Consecutive row max RGB-channel differences from V57C at **y150–155**: V59B **88, 106, 88, 66, 39, 0**; V61A **17, 13, 7, 2, 0, 0**; V61B **33, 27, 14, 5, 1, 0**; V61C **51, 44, 23, 8, 1, 0**. The previous V59B y154 cutoff is resolved numerically in all V61 versions.
- The V61 changed area is localized to the bottom of the head silhouette only. The remaining dark jaw/neck outline and some pale scalp/cheek/ear halo were already present upstream and remain visually detectable at 4×. No new upper/head patch or hard rectangular shoulder boundary is apparent in the actual comparison.

## SHA-256 evidence

| PNG | SHA-256 |
|---|---|
| `IRFAN_FISH_V59B_WIDE_PHOTO_SKY_TRUE_MATTE_QA_HOLD.png` | `244eb330b15e903fd8352bd5a65dbe6ae0ed4c279cd06adb0a1fcf32444d8af3` |
| `IRFAN_FISH_V61A_VERTICAL_SKY_EDGE_FADE_QA_HOLD.png` | `de32847c667287c2e69c2000a68e98662cff51fe74213b92e6fa6af798d97c45` |
| `IRFAN_FISH_V61B_VERTICAL_SKY_EDGE_FADE_QA_HOLD.png` | `dfc15ce0d4135538f56db0ec8654bda9716c518b2e97f292be8e2a2795e99124` |
| `IRFAN_FISH_V61C_VERTICAL_SKY_EDGE_FADE_QA_HOLD.png` | `2b9df07e9074b64ec8621e50e13b461976e6ae9b2e3168f6e3c16cdb38d6e7a9` |

**Decision scope:** This audit selects **V61B over V59B/A/C as the safest current technical candidate**, while retaining its `QA_HOLD` status. It does not certify global source likeness, 9/10 photographic naturalness, Hindsight checkpoint completion, or final release.
