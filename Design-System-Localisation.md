# Design System Localisation — getamazednow.ai site

Localises the Getamazednow AI Design System v1.2 for this project. The design-system
master stays byte-identical; project-specific values live here.

1. **Artefact / product name:** getamazednow.ai — Brand Hub (landing page)
2. **Version + status:** v1.0 · FINAL (public site)
3. **Legacy colour remap:** none — built natively on brand tokens (`--gai-*`), no inherited artefact.
4. **Reference implementation:** `index.html` + `assets/styles.css` (wired to `assets/tokens.css`).

## Applied brand decisions
- **Web topbar (§6):** Ink `#2A363B` bar, 2px Signal `#5FA8CC` bottom border, Lattice icon 64px + "Getamazednow AI" (Signal) + " · Brand Hub" (white), byline in Stone, status pills right.
- **Hero:** Ink surface with low-opacity Tensor lattice texture; Color badge with **Signal containment keyline** (same-tone-dark rule). Soft Signal halo permitted (web/hero only).
- **Accent text on white:** `signalDeep #2E7DA6` (AA), never Signal/Stone as body text.
- **Type:** Poppins (display/heading) + Inter (body), Google Fonts.
- **Favicon:** `assets/logo/Getamazednow-AI-Favicon.svg` (+ PNG fallbacks).
