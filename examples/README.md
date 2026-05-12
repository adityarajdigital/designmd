# Example DESIGN.md outputs

Eight curated samples from the live DesignMD catalog, showing the kind of structured design specification you get for any URL. Each `.md` file is paired with the source-site thumbnail used during extraction.

| Sample | Category | Live page |
|---|---|---|
| [`DESIGN-stripe.md`](./DESIGN-stripe.md) | Fintech | [/benchmarks/stripe](https://designmd.adityaraj.info/benchmarks/stripe) |
| [`DESIGN-mercury.md`](./DESIGN-mercury.md) | Fintech | [/benchmarks/mercury](https://designmd.adityaraj.info/benchmarks/mercury) |
| [`DESIGN-linear.md`](./DESIGN-linear.md) | Productivity | [/benchmarks/linear](https://designmd.adityaraj.info/benchmarks/linear) |
| [`DESIGN-notion.md`](./DESIGN-notion.md) | Productivity | [/benchmarks/notion](https://designmd.adityaraj.info/benchmarks/notion) |
| [`DESIGN-vercel.md`](./DESIGN-vercel.md) | Hosting | [/benchmarks/vercel](https://designmd.adityaraj.info/benchmarks/vercel) |
| [`DESIGN-anthropic.md`](./DESIGN-anthropic.md) | AI | [/benchmarks/anthropic](https://designmd.adityaraj.info/benchmarks/anthropic) |
| [`DESIGN-figma.md`](./DESIGN-figma.md) | Design | [/benchmarks/figma](https://designmd.adityaraj.info/benchmarks/figma) |
| [`DESIGN-airbnb.md`](./DESIGN-airbnb.md) | Consumer | [/benchmarks/airbnb](https://designmd.adityaraj.info/benchmarks/airbnb) |

## What's in a sample

Every generated `DESIGN.md` follows a consistent 10-section structure:

1. **Visual Theme & Atmosphere** — high-level character of the brand
2. **Color Palette & Roles** — primary, accent, surface, text, with measured hex values
3. **Typography Rules** — families, size scale, weights, line-heights
4. **Component Stylings** — buttons, inputs, cards, navigation
5. **Spacing & Layout** — spacing scale, container widths, grid systems
6. **Iconography & Imagery** — icon styles, illustration patterns
7. **Motion & Interaction** — transitions, easing, hover states
8. **Responsive Behavior** — measured breakpoints, mobile patterns
9. **Accessibility** — measured contrast pairs, focus styles
10. **Implementation Notes** — practical guidance for AI agents

## How these were generated

Each file is the unedited output from the live DesignMD pipeline at the date stamped on the corresponding `/benchmarks/<slug>` page. The pipeline:

1. Loads the source URL in a headless browser
2. Extracts CSS variables, computed styles, breakpoints, and component selectors
3. Captures multiple-fold screenshots
4. Streams the extracted token JSON + screenshots into a vision LLM
5. Saves the markdown response unchanged

No human editing has been applied to these examples.

## How to use them

See [`/docs/using-with-ai-tools.md`](../docs/using-with-ai-tools.md) for instructions on integrating these files with Claude, Cursor, Copilot, and other AI coding tools.
