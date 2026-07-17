# getamazednow.ai — Brand Hub

The personal AI-brand hub for **Duane Gomes**, positioned around **Agentic AI Architecture** and **Responsible AI Governance**. It's the connective tissue between the GitHub project demos, the Medium *Responsible AI Operations* series, and professional credibility markers.

**Live:** [www.getamazednow.ai](https://www.getamazednow.ai)

## Stack

Static HTML/CSS, hosted on **GitHub Pages** (deploy from `main`, `/root`). No build step, no framework — deliberately low-maintenance and fast.

## Structure

```
index.html                 Landing page (hero · project tiles · thought-leadership · credibility · CTA)
assets/
  styles.css               Site styles, wired to the design-system tokens
  tokens.css               Getamazednow AI Design System v1.2 tokens (--gai-*)
  logo/                     Tensor Node Lattice logo, keyline, background & favicon variants
CNAME                      Custom domain: www.getamazednow.ai
.nojekyll                  Serve files as-is (bypass Jekyll)
robots.txt · sitemap.xml   SEO
Design-System-Localisation.md   Project localisation of the brand system
```

## Branding

Applies the **Getamazednow AI Design System v1.2** — Ink/Signal palette, Poppins + Inter type, and the Tensor Node Lattice mark. Colours and type consume `--gai-*` tokens unchanged; nothing is invented locally.

## Local preview

```bash
python3 -m http.server 8080   # then open http://localhost:8080
```

## Deployment

GitHub Pages builds from `main` (`/root`). The custom domain (`www.getamazednow.ai`) is set in **Settings → Pages**; HTTPS is enforced once DNS propagates. See the site brief for the full DNS record structure (apex `A` records + `www` / project-subdomain `CNAME`s).

---

*A Getamazednow Company.*
