# Design System Inspired by Stripe

## 1. Visual Theme & Atmosphere
Stripe's visual design combines a clean, modern aesthetic with vibrant accents that convey a sense of innovation and trust. The use of gradients and bold typography enhances the dynamic feel, while a structured layout ensures clarity and usability. The overall experience feels engaging and professional, catering to a diverse audience.

**Key Characteristics**
- Rich gradients with vibrant color transitions.
- Predominantly white background for a clean layout.
- Bold typography using a single font family.
- Clear visual hierarchy with distinct headings and body text.
- Interactive elements that respond to user actions.
- Use of space to create a balanced and organized look.
- Subtle shadows to add depth without overwhelming the design.

## 2. Color Palette & Roles

### Primary
- **#533afd** — Used for primary actions and accents.
- **#061b31** — Main text color, providing strong contrast.
- **#ffffff** — Background color, creating a clean canvas for content.

### Accent Colors
- **#e5edf5** — Light accent used in backgrounds and UI elements.
- **#f8fafd** — Soft accent for subtle backgrounds.
- **#302554** — Dark accent for depth and contrast.
- **#ffe0d1** — Light peach accent for highlights.

### Interactive
- **#533afd** — Used for primary buttons and links.
- **#061b31** — Active state for buttons and links, ensuring visibility.

### Neutral Scale
- **#000000** — Used for body text and high-contrast elements.
- **#50617a** — Secondary text color for less emphasized content.
- **#64748d** — Subdued text for less critical information.

### Surface & Borders
- **#e5edf5** — Light borders and backgrounds for cards and containers.
- **#f8fafd** — Subtle background for sections and containers.

## 3. Typography Rules
- **Font Family**: `sohne-var`, with fallback to sans-serif.
- **Hierarchy**:

| Role    | Font       | Size  | Weight | Line Height | Letter Spacing | Notes                |
|---------|------------|-------|--------|-------------|----------------|----------------------|
| Display | sohne-var  | 48px  | 700    | 1.2         | 0              | Main display text    |
| H1      | sohne-var  | 32px  | 700    | 1.2         | 0              | Primary heading      |
| H2      | sohne-var  | 26px  | 700    | 1.2         | 0              | Secondary heading    |
| H3      | sohne-var  | 22px  | 400    | 1.5         | 0              | Tertiary heading     |
| Body    | sohne-var  | 18px  | 400    | 1.5         | 0              | Main body text       |
| Caption | sohne-var  | 14px  | 400    | 1.5         | 0              | Small text           |
| Code    | sohne-var  | 16px  | 400    | 1.5         | 0              | Monospace for code   |

### Principles
- Consistent use of `sohne-var` across all text elements.
- Strong emphasis on hierarchy through size and weight variations.
- Adequate line heights for readability and comfort.

## 4. Component Stylings

### Buttons
**Primary Button**
```css
.button-primary {
  background-color: #533afd;
  color: #ffffff;
  border: none;
  border-radius: 4px;
  padding: 12px 0;
  font-size: 14px;
  font-weight: 400;
}
.button-primary:hover {
  background-color: rgba(40, 99, 177, 0.125);
}
```

**Secondary Button**
```css
.button-secondary {
  background-color: transparent;
  color: #061b31;
  border: 1px solid #061b31;
  border-radius: 4px;
  padding: 12px 0;
  font-size: 14px;
  font-weight: 400;
}
.button-secondary:hover {
  background-color: rgba(40, 99, 177, 0.125);
}
```

**Ghost Button**
```css
.button-ghost {
  background-color: transparent;
  color: #061b31;
  border: none;
  border-radius: 4px;
  padding: 12px 0;
  font-size: 14px;
  font-weight: 400;
}
.button-ghost:hover {
  background-color: rgba(40, 99, 177, 0.125);
}
```

### Cards & Containers
**Standard Card**
```css
.card {
  background-color: #ffffff;
  border-radius: 4px;
  box-shadow: rgba(0, 0, 0, 0.2) 0px 0px 32px 8px;
  padding: 16px;
}
```

### Inputs & Forms
**Text Input**
```css
.input-text {
  border: 1px solid #e5edf5;
  border-radius: 4px;
  padding: 12px;
  font-size: 16px;
  color: #061b31;
}
.input-text:focus {
  outline: none;
  border-color: #533afd;
}
```

**Form Label**
```css
.label {
  font-size: 14px;
  color: #273951;
}
```

**Checkbox/Radio**
```css
.checkbox, .radio {
  accent-color: #533afd;
}
```

### Navigation
**Top Navigation Bar**
```css
.navbar {
  background-color: #ffffff;
  border-bottom: 1px solid #e5edf5;
  padding: 16px 24px;
}
```

**Navigation Link**
```css
.nav-link {
  color: #061b31;
  text-decoration: none;
  padding: 8px 16px;
}
.nav-link:hover {
  color: #533afd;
}
```

**Dropdown Menu**
```css
.dropdown {
  background-color: #ffffff;
  border: 1px solid #e5edf5;
  border-radius: 4px;
}
```

### Links
**Standard Link**
```css
.link {
  color: #061b31;
  text-decoration: underline;
}
.link:hover {
  color: #533afd;
}
```

**Secondary Link**
```css
.link-secondary {
  color: #50617a;
}
.link-secondary:hover {
  color: #061b31;
}
```

### Badges
**Status Badge Variants**
```css
.badge-success {
  background-color: #e5edf5;
  color: #061b31;
}
.badge-alert {
  background-color: #ffe0d1;
  color: #061b31;
}
.badge-info {
  background-color: #f8fafd;
  color: #061b31;
}
```

## 5. Layout Principles
- **Spacing System**: Base unit of 4px, scaling up to 32px. 
  - Usage Context:
    - 4px: Small margins
    - 8px: Between text elements
    - 16px: Between sections
    - 24px: Between cards
    - 32px: Outer margins

- **Grid & Container** 
_Note: container widths and column counts are not extracted from the source. The values below are reasonable defaults inferred from the visible layout density._
  - Max width: 1200px
  - Columns: 12
  - Gutter: 16px
  - Section padding: 32px

- **Whitespace Philosophy**: Generous use of whitespace enhances readability and separates content effectively, allowing users to focus on key elements.

- **Border Radius Scale**: 
  - 4px: Buttons and inputs
  - 8px: Cards and containers
  - 100px: Circular elements

## 6. Depth & Elevation
| Level | Treatment                                   | Use                        |
|-------|---------------------------------------------|----------------------------|
| z-0   | None                                        | Base layer                 |
| z-1   | rgba(23, 23, 23, 0.06) 0px 3px 6px       | Standard elements          |
| z-2   | rgba(50, 50, 93, 0.12) 0px 16px 32px      | Dropdowns                  |
| z-3   | rgba(0, 0, 0, 0.2) 0px 0px 32px 8px      | Modals                     |

### Shadow Philosophy
Shadows are used subtly to provide depth to UI elements, enhancing the visual hierarchy without overwhelming the design.

## 7. Do's and Don'ts

### Do's
- Use **#533afd** for primary button backgrounds.
- Maintain **16px** font size for body text.
- Incorporate **24px** spacing between cards.
- Employ **sohne-var** for all typography.
- Use **4px** border radius for buttons.
- Ensure links use **#061b31** for normal state.
- Apply **rgba(0, 0, 0, 0.2)** for shadow effects on cards.
- Keep at least **32px** of padding in sections.

### Don'ts
- Never use **#e5edf5** for body text on **#ffffff** background.
- Avoid **18px** font size for headings; use **22px** or larger.
- Don’t place buttons closer than **16px** apart.
- Refrain from using **#ffffff** for text on **#f8fafd**.
- Don't use borders thicker than **1px** on inputs.
- Avoid using **#50617a** for primary action buttons.
- Don’t mix font families; stick to **sohne-var**.
- Never use less than **4px** radius on buttons.

## 8. Responsive Behavior 
_Note: breakpoints below are industry-standard recommendations, not measurements from the source. Adjust to the brand's actual media queries when implementing._

### Suggested Breakpoints
| Breakpoint Name    | Width | Key Changes                        |
|--------------------|-------|------------------------------------|
| Mobile Small       | 0     | Stack elements vertically          |
| Mobile Large       | 640   | Adjust padding and font sizes      |
| Tablet             | 940   | Introduce side-by-side layouts     |
| Desktop            | 1200  | Full-width layouts and elements    |
| Desktop Large      | 1440  | Maximize content area              |

### Touch Targets
- Minimum button size: **44px x 44px**.
- Minimum spacing between touchable elements: **8px**.

### Collapsing Strategy
- **Navigation**: Collapse into a hamburger menu on mobile.
- **Cards**: Stack vertically on smaller screens.
- **Typography**: Scale down font sizes on mobile.
- **Padding**: Reduce padding in sections on mobile.
- **Spacing**: Use smaller spacing values on mobile.

## 9. Agent Prompt Guide
- **Quick Color Reference**
  - Primary: **#533afd**
  - Accent: **#e5edf5**
  - Text: **#061b31**
  
- **Iteration Guide**
  1. Always use **sohne-var** for typography.
  2. Maintain **16px** base font size for body text.
  3. Use **4px** border radius for buttons.
  4. Ensure **#533afd** for primary button backgrounds.
  5. Keep at least **24px** spacing between cards.
  6. Scale down to **14px** for captions.
  7. Use **rgba(0, 0, 0, 0.2)** for card shadows.
  8. Apply **32px** padding in sections.
  9. Ensure links use **#061b31** for normal state.
  10. Don’t exceed **1px** border thickness on inputs.