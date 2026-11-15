# Independent strict visual QA: V61B vs V72A/B/C

**2026-11-15, Europe/Istanbul | READ-ONLY image inspection.** Reviewed the actual 554 × 554 V61B, V72A and V72C PNGs at full frame, plus the actual `V72_FACE_EDGE_5X_NATIVE_COMPARE.png` and `V72_HEAD_NECK_3X_NATIVE_COMPARE.png` boards showing V61B and all three V72 variants. V72B is directly represented on both boards. No source images were edited or regenerated. Scores below are visual judgments, not automated authenticity measurements.

**Verdict: NO-GO for the strict 8.5/10 photorealism gate. None of V72A/B/C is a material improvement over V61B. Retain V61B as the conservative overall baseline. If a V72 candidate must be kept for comparison, choose V72A as the least intrusive V72 variant, still QA_HOLD.**

| Image | Full photo /10 | Face/scalp edge /10 | Strict gate | Visual finding |
|---|---:|---:|---|---|
| V61B original | 7.0 | 6.7 | FAIL | Soft white-gray rim around right scalp/temple and cheek, dark line around lower jaw/beard; otherwise coherent native full-frame image |
| V72A | 7.0 | 6.8 | FAIL | Slightly calmer right face-to-sky transition; residual pale scalp rim and beard-neck dark outline remain; change too small to call a material fix |
| V72B | 6.9 | 6.7 | FAIL | Further edge processing gives no convincing natural hair/sky contact; mild risk of a processed, dark seam around the jaw |
| V72C | 6.8 | 6.5 | FAIL | Strongest local relighting/decontamination, but a more visually assertive dark border and artificial smooth transition remain |

**Observed at 5× / 3×:** The near-white contour alongside the upper right scalp and temple is reduced inconsistently, rather than fully replaced with naturally antialiased flyaway hair/skin against cloudy sky. The jaw/beard underside retains a near-black outline that reads as a matte/compositing seam; variants B/C do not remove it and C looks hardest. The hairline against sky remains suspiciously uniform and pixel-stair-stepped in the nearest-neighbor magnification. These are visible limitations, not a claim that a new defect affects the protected face interior. The shoulder seam and background continuity appear unchanged at 1×; no broad rectangular patch was seen. At full 554 × 554, differences between versions are subtle and the original background, fish, clothing and pose are consistent.

**Source and variant provenance as recorded in `V72_SOURCE_PIXEL_SHA_AUDIT.json` / `V72_RUN_LOG.txt` (the original source files were visually inspected; SHA and pixel counts here are from the recorded audit, not independently recomputed because the Mac terminal hit its retained-session limit):**

| File | Logged SHA-256 | Logged changed pixels vs V61B |
|---|---|---:|
| `IRFAN_FISH_V61B_VERTICAL_SKY_EDGE_FADE_QA_HOLD.png` | `dfc15ce0d4135538f56db0ec8654bda9716c518b2e97f292be8e2a2795e99124` | baseline |
| `IRFAN_FISH_V72A_REAL_CAMERA_LIGHTWRAP_QA_HOLD.png` | `3e35e6798b8f5fea907be12c696e7e80e7d7b9b042c00978e4a3e01193f5a039` | 1,484 |
| `IRFAN_FISH_V72B_REAL_CAMERA_LIGHTWRAP_QA_HOLD.png` | `ed0d339c415e773b3a1b05d96c1a2f926b65a3975322617b42fd5e377ebdc0c5` | 1,648 |
| `IRFAN_FISH_V72C_REAL_CAMERA_LIGHTWRAP_QA_HOLD.png` | `da13bb119aaec38b89a265c81639df7ec815eee208e3ef69f897c32d5b8509b2` | 1,683 |

The producer's audit reports `body_face_core_fish_pixel_lock_pass=true` for each V72 file, and the authoring script asserts rows 155 onward unchanged. This audit has not independently recomputed those pixel checks; visual inspection is consistent with that report. Hindsight checkpoint completion was not independently reverified in this worker audit and this report grants no production/release acceptance.

**Decision for prime:** V61B stays the safer reference. V72A is the best V72 experiment, but its <0.2-point edge improvement is not material; V72B/C are not recommended. Keep all four QA_HOLD and customer delivery NO-GO. Root problem remains contact matte quality around scalp/jaw rather than overall composition.
