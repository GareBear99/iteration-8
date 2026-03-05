Synth — Dynamic Modules Shell (v2)

What this is
- A blueprint-gated shell builder (your "empty repo vessel") that becomes functional by attaching MODULE BLUEPRINTS.
- 3 blueprint lanes:
  1) Shell Blueprint (geometry + pivots/edges)
  2) Ship Module Blueprint (Master Control "eye" module)
  3) Scanner Module Blueprint (Synthesis Scanner probe + HUD window)
  (+ optional HUD module blueprint)

Run
- Open index.html (file:// is fine)
- Upload Shell Blueprint JSON first (use blueprint_octagon.json to test)
- Optionally upload module_ship_default.json / module_scanner_default.json / module_hud_default.json

Controls
- WASD: move the Master Control eye (inspection / camera intent)
- Mouse: aim vector
- C: toggle center reticle
- `: toggle debug overlay
- R: reset

Module blueprint format
{
  "moduleType": "ship" | "scanner" | "hud",
  "id": "NAME",
  "style": "iteration4" | "default",
  "config": { ... },
  "script": "optional JS hooks (advanced)"
}

Notes
- Core stays deterministic + lightweight (Canvas2D, fixed timestep, no per-frame allocations).
- All build actions remain ping-gated (GRANT/DENY receipts) and fail-closed SAFE_MODE on errors.
