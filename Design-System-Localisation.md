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

## Business pack (`business-pack/`, git-ignored — private)
Localised artefacts, Design System v1.2:
1. **Artefacts:** Business Plan · Platform Product Feature Set · Product Roadmap (Word, whitepaper cover **W2 · Framed lower hero**, default `Hero-Lattice` image) + Executive Summary deck (PowerPoint, **P1 centred** title, Ink sandwich, `Slide-BG-Ink`).
2. **Version + status:** current set **v2.0 · DRAFT** (July 2026, repositioned as the continuous AI-assurance layer post investor review; adds Design Partner Prospectus v2.0). v1.0 originals retained alongside.
3. **Legacy colour remap:** none — built natively on brand tokens.
4. **Reference implementation:** `business-pack/Getamazednow_AI_Business_Plan_v2.0.docx` (cover + running header/footer per spec §3–§5, §7–§8).

## Naming hierarchy (decided Jul 2026)
- **Brand essence (lockup only):** "Practical AI. Possible Futures." — lives inside the logo lockup, never repeated as page text.
- **Company positioning (Getamazednow AI):** "the continuous AI-assurance layer" — topbar, meta/SEO, investor pack.
- **Product suite:** **Getamazednow Assure™** — tagline "see it, prove it, stand behind it" (verbs map to Observe / Evidence / Architect-vision). Tiers: Assure · Observe, Assure · Evidence.
- **Assure wordmark treatment (proposed for design-system master v1.3):** Poppins 800, letter-spacing .015em; `signalDeep #2E7DA6` on light surfaces (AA), `Signal #5FA8CC` on Ink. Web class: `.assure` / `.assure--on-ink`. No new colours or fonts — existing tokens at a heavier weight.
- **Trademark status:** "GETAMAZEDNOW" — 0 existing AU marks (IP Australia, Jul 2026). "ASSURE" exact-word — 147 AU marks across classes; common word, own only as the compound. Use ™ (not ®); formal attorney search in classes 9 & 42 before filing.

## Site pages (public)
- `index.html` repositioned to assurance-layer messaging (Jul 2026): Govern verb **prove it**, Architect carries a `plane__vision` pill, engagement strip (`.engage`), motto *see it, prove it, stand behind it*.
- `trust.html` + `privacy.html` — content pages on the `.page` pattern (topbar identity per §6, Ink footer).
