---
title: "feat(maintenance-scheduler): handle disposal + softener combination"
labels: ["enhancement"]
---

The current script applies disposal and softener adjustments independently. When both apply, the combined bump should be 1.40 × 1.15 = 1.61×, not added.

**Diff**

```diff
-bump = 0.0
-if garbage_disposal:
-    bump += cls.DISPOSAL_SOLIDS_BUMP
-if water_softener:
-    bump += cls.SOFTENER_SOLIDS_BUMP
-return round(base / (1.0 + bump), 1)
+multiplier = 1.0
+if garbage_disposal:
+    multiplier *= (1.0 + cls.DISPOSAL_SOLIDS_BUMP)
+if water_softener:
+    multiplier *= (1.0 + cls.SOFTENER_SOLIDS_BUMP)
+return round(base / multiplier, 1)
```

**Verified**

```bash
python scripts/outwestseptic_maintenance_scheduler.py 1250 4 --disposal --softener
# Output: 1.86 years (was 3.0 / 1.55 = 1.94, now 3.0 / 1.61 = 1.86)
```

---

*Out West Septic — TCEQ OSSF Installer I — OS0041298*