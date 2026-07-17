# Getamazednow.ai — Site Build Brief

**Purpose of this document:** Project brief for building the getamazednow.ai brand hub site, to be handed to Cowork for build-out and pushed to GitHub for GitHub Pages hosting.

---

## 1. Objective

Build a personal AI-brand hub site for Duane Gomes, positioned around **Agentic AI Architecture** and **Responsible AI Governance**, aimed primarily at hiring panels, Communities of Practice, and technical peers reviewing his portfolio during an active job search. The site is the connective tissue between his GitHub project demos, Medium thought-leadership series, and professional credibility markers.

---

## 2. Domain & Registration

- **Domain:** `getamazednow.ai`
- **Registrar decision:** Cloudflare or Namecheap (2-year minimum registration is enforced by the `.ai` registry regardless of registrar — avoid GoDaddy's teaser-pricing/high-renewal model).
- **Canonical URL style:** `www.getamazednow.ai` (www-canonical, not apex-canonical).

---

## 3. Hosting Architecture

- **Platform:** GitHub Pages (static site) — chosen over AWS self-hosting (EC2 ruled out entirely) and over AWS S3+CloudFront, to minimize ongoing maintenance and keep everything inside the existing GitHub-centric workflow already used for `Ea-Agent-Mesh` and `genai-observability-demo`.
- **Repo structure:** A **dedicated repo** for the site — explicitly **not** the GitHub profile repo (`getamazednow/getamazednow`). Keeps the profile README doing one job (a short pointer/teaser) while the branded site iterates independently.
  - Suggested repo name: `getamazednow-ai`
- **Build/deploy:** Deploy from branch (`main`, `/root` or `/docs`), custom domain set in repo Settings → Pages, HTTPS enforced once DNS propagates (GitHub auto-provisions SSL via Let's Encrypt).

---

## 4. DNS Structure

`.ai` apex domains cannot take a CNAME record (DNS-standard restriction) — only subdomains can. Structure:

| Record | Type | Target | Purpose |
|---|---|---|---|
| `getamazednow.ai` (apex) | `A` × 4 | `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153` | Resolves apex, redirects to `www` |
| `www.getamazednow.ai` | `CNAME` | `<username>.github.io` | **Canonical** — main brand hub |
| `mesh.getamazednow.ai` (example) | `CNAME` | `<username>.github.io` (Ea-Agent-Mesh repo) | Project subdomain — live demo |
| `observability.getamazednow.ai` (example) | `CNAME` | `<username>.github.io` (genai-observability-demo repo) | Project subdomain — live demo |

**Note:** If using Cloudflare for DNS, set proxy status to **DNS only** (grey cloud) initially, until GitHub's SSL certificate issuance is confirmed working — orange-cloud proxying can interfere with cert provisioning.

Each project subdomain requires its **own repo** with its own custom domain set in that repo's Pages settings — GitHub Pages ties one custom domain to one repo, so subdomains cannot be served as sub-paths of a single repo.

---

## 5. Information Architecture — Landing Page (`www.getamazednow.ai`)

| Section | Purpose / Content |
|---|---|
| **Hero** | Getamazednow AI wordmark/logo (Tensor Node Lattice), one-line positioning statement — *Agentic AI Architecture & Responsible AI Governance* |
| **Project tiles** | Grid of cards, one per subdomain/project (Ea-Agent-Mesh, GenAI Observability Demo, future additions). Each tile: short description, "Live Demo →" (links to subdomain), "Source →" (links to GitHub repo) |
| **Thought leadership strip** | Pulls in the Responsible AI Operations Series (Medium: medium.com/@duane.gomes) — "AI Observability Is No Longer Optional", "Building the AI Control Plane", and future third article |
| **Credibility bar** | 33 years technology experience; verticals: Financial Services, Banking, Retail, Healthcare, Education, Utilities; geographies: India, Australia, US, South-East Asia. Scannable, not a full CV |
| **Contact/CTA** | LinkedIn, GitHub profile link, and a call-to-action inviting Agentic AI conversations |

---

## 6. Brand Application

Apply the **Getamazednow AI Design System (v1.2)** throughout — colours, Poppins/Inter typography, Tensor Node Lattice logo, consistent with existing deliverables (Medium article infographics, PowerPoint executive deck, whitepaper). Reference the `getamazednow-ai-brand` skill/plugin for tokens, covers, and header/footer treatments so the site is visually consistent with the rest of the portfolio.

---

## 7. Housekeeping / Quality Bar

Before linking any project tile's "Source →" to a live GitHub repo, ensure that repo's `README.md` is polished — a hiring panel clicking through to source code is evaluating engineering hygiene, not just the demo output.

---

## 8. Open Items / Decisions for Cowork to Confirm or Flag

- Confirm final project list and subdomain names before wiring DNS.
- Confirm whether the thought-leadership strip pulls live from Medium (via RSS/manual embed) or is manually updated per article.
- Confirm repo name (`getamazednow-ai` suggested, not finalized).

---

## 9. Out of Scope (for this build)

- AWS hosting (S3+CloudFront or EC2) — explicitly not pursued for this site; AWS account reserved for potential future serverless backend work behind live demos (Lambda + API Gateway) if interactivity beyond static HTML is ever needed.
- Profile repo (`getamazednow/getamazednow`) — not used for site hosting; keeps a separate, lightweight role as GitHub profile teaser.
