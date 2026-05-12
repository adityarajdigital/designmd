# Design System Inspired by Linear

## 1. Visual Theme & Atmosphere
Linear's visual theme is characterized by a dark mode aesthetic that emphasizes clarity and functionality. The interface utilizes a combination of dark backgrounds with contrasting text and accent colors to create a modern, tech-focused atmosphere. The layout is clean and structured, allowing users to navigate through product development tools seamlessly.

**Key Characteristics**
- Dark background palette with high-contrast text.
- Use of accent colors for interactive elements and highlights.
- Clear typography hierarchy with a focus on readability.
- Minimalistic icons and illustrations, enhancing usability.
- Subtle animations and transitions that support user interactions.

## 2. Color Palette & Roles

### Primary
- **Accent Blue (#6366f1)** — Used for primary actions and highlights.
- **Accent Red (#eb5757)** — Employed for alerts or important notifications.
- **Accent Purple (#8b5cf6)** — Additional accent for interactive elements.
- **Accent Light Blue (#5e6ad2)** — Another variant for accents.

### Accent Colors
- **Background Dark (#0f1011)** — Main dark background for sections.
- **Background Darker (#08090a)** — Used for deeper contrast areas.
  
### Interactive
- **Text Inverse (#f7f8f8)** — Primary text color on dark backgrounds.
- **Text Secondary (#62666d)** — Secondary text color for less emphasized information.

### Neutral Scale
- **Neutral Light (#e5e5e6)** — Used for subtle backgrounds and borders.
- **Neutral Dark (#383b3f)** — Darker neutral for deeper elements.

### Surface & Borders
- **Border Color (#24282c)** — Used for borders and dividers.

## 3. Typography Rules
- **Font Family**: Inter Variable, fallback: system fonts.
- **Hierarchy**:

| Role      | Font            | Size   | Weight | Line Height | Letter Spacing | Notes                |
|-----------|-----------------|--------|--------|-------------|----------------|----------------------|
| Display   | Inter Variable   | 64px   | 700    | 1.2         | Normal         | Main header          |
| H1        | Inter Variable   | 48px   | 700    | 1.2         | Normal         | Section headers      |
| H2        | Inter Variable   | 24px   | 700    | 1.2         | Normal         | Subsection headers    |
| H3        | Inter Variable   | 20px   | 400    | 1.5         | Normal         | Tertiary headers      |
| Body      | Inter Variable   | 16px   | 400    | 1.5         | Normal         | Main content text    |
| Small     | Inter Variable   | 15px   | 400    | 1.5         | Normal         | Smaller text elements |

### Principles
- Emphasize clarity through high contrast between text and background.
- Maintain consistent font weights for similar roles to enhance hierarchy.
- Use larger sizes for headings to create a clear visual structure.

## 4. Component Stylings

### Buttons
#### Primary Button
```css
.button-primary {
  background-color: #6366f1;
  color: #ffffff;
  padding: 12px 24px;
  border-radius: 9999px;
  font-size: 16px;
  font-weight: 400;
}

.button-primary:hover {
  background-color: #8b5cf6;
}
```

#### Secondary Button
```css
.button-secondary {
  border: 1px solid #8a8f98;
  color: #8a8f98;
  padding: 0px 12px;
  border-radius: 9999px;
  font-size: 13px;
  font-weight: 400;
}

.button-secondary:hover {
  color: #6366f1;
}
```

### Cards & Containers
#### Standard Card
```css
.card {
  background-color: #0f1011;
  color: #f7f8f8;
  padding: 16px;
  border-radius: 6px;
  box-shadow: rgba(0, 0, 0, 0.2) 0px 0px 12px 0px;
}
```

### Inputs & Forms
#### Text Input
```css
.input-text {
  border: 1px solid #24282c;
  border-radius: 4px;
  padding: 12px;
  font-size: 16px;
  color: #62666d;
}

.input-text:focus {
  box-shadow: 0 0 0 2px #6366f1;
}
```

### Navigation
#### Top Navigation Bar
```css
.nav-bar {
  background-color: #0f1011;
  color: #f7f8f8;
  padding: 16px;
}

.nav-link {
  color: #f7f8f8;
  padding: 12px;
}

.nav-link:hover {
  color: #6366f1;
}
```

### Links
#### Standard Link
```css
.link {
  color: #62666d;
}

.link:hover {
  color: #6366f1;
}
```

### Badges
#### Status Badge
```css
.badge-success {
  background-color: #39b350;
  color: #ffffff;
  padding: 4px 8px;
  border-radius: 12px;
}

.badge-alert {
  background-color: #eb5757;
  color: #ffffff;
  padding: 4px 8px;
  border-radius: 12px;
}
```

## 5. Layout Principles
- **Spacing System**: Base unit 4px → 4, 8, 12, 16, 20, 24, 32.
  - Usage Context:
    - 4px: Minor adjustments.
    - 8px: Gaps between icons.
    - 12px: Padding for buttons.
    - 16px: Standard padding for containers.
    - 20px: Margins for sections.
    - 24px: Gaps between larger components.
    - 32px: Major spacing for headers.

- **Grid & Container**
_Note: container widths and column counts are not extracted from the source. The values below are reasonable defaults inferred from the visible layout density._
- Max Width: 1200px
- Columns: 12
- Gutter: 16px
- Section Padding: 24px

- **Whitespace Philosophy**: Whitespace is used strategically to enhance readability and focus on content, allowing for a clear separation between elements.

- **Border Radius Scale**: 
  - 2px: Minor elements.
  - 4px: Standard components.
  - 6px: Cards and containers.
  - 12px: Modals and overlays.
  - 9999px: Circular buttons.

## 6. Depth & Elevation
| Level | Treatment                                   | Use                    |
|-------|---------------------------------------------|------------------------|
| z-0   | None                                        | Base layer             |
| z-1   | rgba(0, 0, 0, 0.03) 0px 1.2px 0px 0px    | Cards                  |
| z-3   | rgba(0, 0, 0, 0.4) 0px 2px 4px 0px        | Overlays               |
| z-50  | rgba(0, 0, 0, 0.2) 0px 0px 12px 0px inset | Modals                 |
| z-100 | rgb(35, 37, 42) 0px 0px 0px 1px inset      | Tooltips               |

**Shadow Philosophy**: Shadows are used to create depth and hierarchy, distinguishing between layers and interactive elements.

## 7. Do's and Don'ts

### Do's
- Use #6366f1 for primary buttons and highlights.
- Keep a minimum of 16px padding in containers.
- Use Inter Variable 16px for body text to ensure readability.
- Apply 24px spacing between sections for clear separation.
- Use #f7f8f8 for text on dark backgrounds for high contrast.
- Ensure all links have a hover state changing to #6366f1.
- Use 9999px border radius for circular buttons for a friendly appearance.
- Apply z-3 shadows for cards to enhance depth perception.

### Don'ts
- Never use #62666d for body text on #ffffff backgrounds; it fails contrast.
- Avoid using less than 4px spacing between icons and text.
- Do not use font sizes smaller than 15px for body text.
- Refrain from using colors that do not meet AA contrast standards.
- Do not overcrowd elements; maintain at least 24px space between cards.
- Avoid using border radius values larger than 12px for standard components.
- Do not use z-index values less than z-1 for visible elements.
- Never use #eb5757 for text; it should only be for alerts.

## 8. Responsive Behavior
_Note: breakpoints below are industry-standard recommendations, not measurements from the source. Adjust to the brand's actual media queries when implementing._
- **Suggested Breakpoints**:

| Breakpoint Name    | Width   | Key Changes                      |
|--------------------|---------|----------------------------------|
| Mobile Small       | 600px   | Stack navigation items           |
| Mobile Large       | 640px   | Adjust button sizes              |
| Tablet             | 768px   | Change card layout               |
| Desktop            | 1280px  | Show full navigation             |
| Desktop Large      | 1440px  | Optimize for larger screens      |

- **Touch Targets**
  - Minimum button height: 44px.
  - Minimum link padding: 12px.

- **Collapsing Strategy**
  - Navigation: Collapse to hamburger menu on mobile.
  - Cards: Stack vertically on smaller screens.
  - Typography: Scale down headings on mobile.
  - Padding: Reduce to 16px on smaller devices.

## 9. Agent Prompt Guide
- **Quick Color Reference**
  - Accent Blue: #6366f1
  - Accent Red: #eb5757
  - Background Dark: #0f1011
  - Text Inverse: #f7f8f8

- **Iteration Guide**
  1. Always use #6366f1 for primary buttons.
  2. Maintain font sizes at 16px for body text.
  3. Use 4px increments for spacing.
  4. Keep button heights at 44px minimum.
  5. Apply 9999px radius for circular buttons.
  6. Ensure all links change color on hover to #6366f1.
  7. Use z-3 shadows for card components.
  8. Follow the responsive breakpoints for layout adjustments.