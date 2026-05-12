<div align="center">

# DesignMD

**A structured design intelligence and benchmark platform for modern websites.**

[![Live Demo](https://img.shields.io/badge/demo-designmd.adityaraj.info-D14E2F?style=flat-square)](https://designmd.adityaraj.info)
[![Benchmarks](https://img.shields.io/badge/benchmarks-56_sites-2A2620?style=flat-square)](https://designmd.adityaraj.info/benchmarks)
[![Status](https://img.shields.io/badge/status-public_beta-2A2620?style=flat-square)](https://designmd.adityaraj.info)
[![License](https://img.shields.io/badge/license-MIT-2A2620?style=flat-square)](./LICENSE)

[**Live site**](https://designmd.adityaraj.info) ·
[**Benchmark catalog**](https://designmd.adityaraj.info/benchmarks) ·
[**Examples**](./examples) ·
[**Roadmap**](./docs/roadmap.md)

</div>

---

## What is DesignMD

DesignMD turns any production website into a structured, AI-ready design specification — a `DESIGN.md` file containing the real color palette, typography system, spacing scale, breakpoints, component patterns, and interaction states extracted directly from the live DOM and CSSOM.

It is not a UI inspiration gallery. It is a **measurement layer** — every signal is pulled from the source page, not inferred. The result is a searchable benchmark intelligence layer that compounds in value as more sites are measured.

```
URL  →  Token extraction (DOM + CSSOM)  →  DESIGN.md spec  →  AI-ready context
```

Paste `stripe.com`. Get back a complete design specification you can drop into Claude, Cursor, or any AI coding agent so it builds UI that actually matches the source brand.

## Live demo

→ **[designmd.adityaraj.info](https://designmd.adityaraj.info)**

Try any of the curated benchmarks:
- [Stripe](https://designmd.adityaraj.info/benchmarks/stripe) · [Linear](https://designmd.adityaraj.info/benchmarks/linear) · [Vercel](https://designmd.adityaraj.info/benchmarks/vercel)
- [Anthropic](https://designmd.adityaraj.info/benchmarks/anthropic) · [Mercury](https://designmd.adityaraj.info/benchmarks/mercury) · [Notion](https://designmd.adityaraj.info/benchmarks/notion)

Or paste your own URL on the homepage.

## Features

### Live measurement, not inference

Every signal in a generated `DESIGN.md` is sourced from the live production page:

| Signal | Source |
|---|---|
| Color palette + roles (background / foreground / accent / text-inverse) | DOM color extraction |
| Typography system (families, sizes, weights, line-heights) | Computed styles |
| Spacing scale | Layout primitive measurement |
| Breakpoints | `@media` rule enumeration |
| Hover / focus states | CSSOM pseudo-class traversal |
| Contrast pairs | WCAG-compliant pair measurement |
| Component archetypes | CSS-selector frequency analysis |
| Z-index ladder | Stacking context inventory |

### Structured benchmark catalog

56 measured websites organized across 13 curated categories — AI · developer tools · databases · hosting · productivity · design · analytics · fintech · auth · media · marketing · e-commerce · other notable.

Each benchmark is a stable URL with structured metadata (`/benchmarks/<slug>`) and machine-readable JSON (`/benchmarks/<slug>.json`).

### AI-ready output

The generated `DESIGN.md` is purpose-built for LLM context windows. Drop it into:

- **Claude / Claude Code** — as `CLAUDE.md` or via `@DESIGN-<domain>.md` reference
- **Cursor** — via `.cursor/rules` directives
- **GitHub Copilot, Windsurf, Aider** — as project context
- **Plain ChatGPT** — paste it as a system message

The AI then builds UI that adheres to the **real** design system of the source brand, not a hallucinated approximation.

### Structured exports

- **`/benchmarks/<slug>`** — human-readable page (DESIGN.md rendered + side panel of measured signals)
- **`/benchmarks/<slug>.json`** — full raw extraction as JSON
- **`/benchmarks/<slug>.jpg`** — pre-cropped hero thumbnail
- **`/sitemap.xml`** — full crawlable index for ingestion pipelines

## Architecture (high-level)

```
┌──────────────────┐
│  User-provided   │
│        URL       │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐     ┌────────────────────┐
│  Token extractor │ ──▶ │  Structured tokens │
│ (DOM + CSSOM)    │     │   (palette, type,  │
│                  │     │  spacing, motion)  │
└──────────────────┘     └─────────┬──────────┘
                                   │
                  ┌────────────────┼────────────────┐
                  │                │                │
                  ▼                ▼                ▼
        ┌─────────────────┐  ┌─────────────┐  ┌──────────────┐
        │  DESIGN.md spec │  │  JSON API   │  │   Card grid  │
        │   (AI-ready)    │  │  (machine)  │  │   (human)    │
        └─────────────────┘  └─────────────┘  └──────────────┘
```

The extraction pipeline, prompt engineering, and automation internals are **not part of this repository** — see [proprietary boundary](#proprietary-boundary) below.

## Sample output

A snippet from [`examples/DESIGN-stripe.md`](./examples/DESIGN-stripe.md):

```markdown
## Color Palette & Roles

### Primary
- **Brand Indigo (#0a2540)** — Hero typography, primary footer surface
- **Stripe Purple (#635bff)** — Primary buttons, focus rings, link accents

### Surface
- **Pure White (#ffffff)** — Page background, card surface
- **Cool Mist (#f6f9fc)** — Secondary surface, alternating sections

### Typography
| Role | Font | Size | Weight | Line Height |
|---|---|---|---|---|
| Display | Sohne Var | 64px | 600 | 1.05 |
| H1 | Sohne Var | 40px | 600 | 1.15 |
| Body | Sohne Var | 18px | 400 | 1.6 |
| Code | Sohne Mono | 14px | 400 | 1.5 |

### Breakpoints (measured live)
- 480px · 600px · 768px · 880px · 1024px · 1200px · 1440px
```

Full file: [DESIGN-stripe.md](./examples/DESIGN-stripe.md) · [Live page](https://designmd.adityaraj.info/benchmarks/stripe)

More examples in [`/examples`](./examples):
- [Stripe](./examples/DESIGN-stripe.md) · [Linear](./examples/DESIGN-linear.md) · [Vercel](./examples/DESIGN-vercel.md) · [Notion](./examples/DESIGN-notion.md)
- [Anthropic](./examples/DESIGN-anthropic.md) · [Mercury](./examples/DESIGN-mercury.md) · [Figma](./examples/DESIGN-figma.md) · [Airbnb](./examples/DESIGN-airbnb.md)

## Why this exists

Every AI coding agent is good at writing code. None of them is good at matching a specific brand's visual system without ground-truth grounding. Existing solutions fail in distinct ways:

| Approach | Failure mode |
|---|---|
| **AI guesses from text prompt** | Hallucinates plausible-looking but wrong colors, fonts, spacing |
| **Designer manually documents tokens** | Stale within weeks; doesn't scale across teams |
| **Screenshot → vision model** | Loses structural info; treats decorative pixels as design intent |
| **Existing design-system catalogs** | Hand-curated, static, biased to designer aesthetics |

DesignMD measures every signal live, then formalizes it as an `MD` spec that survives the round-trip into an AI context window. The benchmark catalog turns every well-known production site into a reference implementation that compounds in value over time.

## Use cases

- **AI-assisted UI development** — give Claude/Cursor a real design spec for any reference brand
- **Design system audits** — measure your own production site against industry leaders
- **Competitive analysis** — see exactly how Stripe, Linear, or Notion structure their visual systems
- **Onboarding new designers** — link to a measured spec instead of writing one from scratch
- **Research & teaching** — quantitative material for design education

## Roadmap

See [`docs/roadmap.md`](./docs/roadmap.md) for the full plan. Highlights:

- [x] **Initial 56-site benchmark catalog** — done
- [x] **Curated category collections** with editorial taglines
- [x] **AI-ready DESIGN.md exports** (markdown + JSON + thumbnail)
- [ ] **300-site catalog expansion** — in progress
- [ ] **Comparison pages** — `/benchmarks/compare/notion-vs-linear` style queries
- [ ] **Structured search API** — query benchmarks by palette / font / breakpoint
- [ ] **Token diff over time** — track how a site's design evolves
- [ ] **CLI client** — `designmd <url>` from your terminal
- [ ] **Anonymous user accounts** — saved history, higher quotas

## Proprietary boundary

This is a **showcase repository**. It contains:

- ✅ Sample `DESIGN.md` outputs from the live catalog (`/examples`)
- ✅ Architecture overview (high-level)
- ✅ UI screenshots and product positioning (`/screenshots`)
- ✅ Roadmap, FAQ, and contribution guidance (`/docs`)

It does **not** contain:

- ❌ The extraction pipeline (`extractTokens`)
- ❌ Prompt engineering for the LLM stage
- ❌ The Playwright runner or browser automation
- ❌ Server source code
- ❌ Rate-limiting, caching, or auth internals
- ❌ Schema definitions or database code

For access to the production codebase, please reach out — [adityaraj.info](https://adityaraj.info).

## Contributing

This is a curated showcase, not an open-source project. We welcome:

- 🪲 **Bug reports** on `https://designmd.adityaraj.info` (via GitHub Issues here)
- 💡 **Benchmark suggestions** — open an issue with a URL you want measured
- ✍️ **Documentation improvements** in `/docs`
- 🎨 **Better sample examples** — PRs against `/examples` welcome

For larger contributions (extraction quality, new categories, comparison logic, etc.), please open an issue first to discuss.

## License

[MIT](./LICENSE) — covers the **materials in this repository only**: `README`, sample `DESIGN.md` outputs, documentation, screenshots, and the example thumbnails.

The MIT license **does not** extend to:

- The DesignMD production source code, automation, or infrastructure
- The token-extraction pipeline (DOM/CSSOM measurement code)
- The LLM prompts and generation logic
- The DesignMD name, logo, and brand identity

For licensing the platform itself or commercial deployment, please reach out — [adityaraj.info](https://adityaraj.info).

## Acknowledgments

Built by [Aditya Raj](https://adityaraj.info). DesignMD is powered by automated browser instrumentation, frontend analysis pipelines, and AI-assisted specification generation.

Thanks to the designers and engineers behind the modern web whose publicly accessible systems make benchmarking and design research possible.

---

<div align="center">

**[Try the live demo →](https://designmd.adityaraj.info)**

</div>
