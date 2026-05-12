# Design System Inspired by Figma

## 1. Visual Theme & Atmosphere
Figma's visual theme is characterized by a modern, clean interface that emphasizes collaboration and creativity. The use of bright accent colors against a neutral background creates an inviting atmosphere suitable for design work. The layout is structured to facilitate easy navigation and access to tools, with ample whitespace that enhances readability and user focus.

**Key Characteristics**
- Bright accent colors (#4d49fc, #00b6ff) against a white background (#ffffff).
- Clear typography hierarchy using the "figmaSans" font family.
- Ample whitespace that provides a clean, uncluttered look.
- Interactive elements with subtle hover effects for better user engagement.
- Use of rounded corners (8px) on buttons and containers to soften the visual presentation.

## 2. Color Palette & Roles

### **Primary**
- **White (#ffffff)** — Used as the primary background color.
- **Black (#000000)** — Used for text and dark backgrounds.

### **Accent Colors**
- **Accent Purple (#4d49fc)** — Used for buttons and interactive elements.
- **Accent Blue (#00b6ff)** — Highlights and links.
- **Accent Green (#24cb71)** — Additional highlights.
- **Accent Yellow (#e4ff97)** — Used for notifications or alerts.
- **Accent Light Green (#f3ffe3)** — Backgrounds for sections.

### **Interactive**
- **Hover State** — Maintains text-decoration-color as initial on hover for links.
- **Active/Disabled States** — Elements become transparent or change opacity when disabled.

### **Neutral Scale**
- **Light Gray (#e6e6e6)** — Used for borders and subtle backgrounds.
- **Dark Gray (#697485)** — Used for secondary text.

## 3. Typography Rules
- **Font Family**: 
  - Primary: `figmaSans`, sans-serif; fallback: system-ui.
  - Monospace: `figmaMono`, monospace.

| Role      | Font      | Size  | Weight | Line Height | Letter Spacing | Notes                  |
|-----------|-----------|-------|--------|-------------|----------------|------------------------|
| Display   | figmaSans | 72px  | 700    | 1.2         | 0              | Main headings          |
| H1        | figmaSans | 56px  | 700    | 1.2         | 0              | Major section headings  |
| H2        | figmaSans | 24px  | 700    | 1.2         | 0              | Subheadings            |
| Body      | figmaSans | 18px  | 330    | 1.5         | 0              | Main text              |
| Body      | figmaSans | 16px  | 330    | 1.5         | 0              | Secondary text         |
| Caption   | figmaSans | 12px  | 330    | 1.5         | 0              | Small text             |
| Code      | figmaMono | 16px  | 400    | 1.5         | 0              | Code blocks            |

### **Principles**
- Use varying weights to establish a clear visual hierarchy.
- Maintain consistent line heights for readability.
- Utilize larger font sizes for headings to draw attention.

## 4. Component Stylings

### Buttons
```css
.btn-primary {
  background-color: #4d49fc;
  color: #ffffff;
  border: none;
  border-radius: 8px;
  padding: 12px 21px;
  font-size: 16px;
  font-weight: 400;
  transition: background 0.4s cubic-bezier(0.8, 0, 0.2, 1);
}

.btn-primary:hover {
  background-color: #3b3bcf;
}

.btn-secondary {
  background-color: #ffffff;
  color: #000000;
  border: 1px solid #000000;
  border-radius: 8px;
  padding: 12px 21px;
  font-size: 16px;
  font-weight: 400;
}

.btn-secondary:hover {
  background-color: rgba(0, 0, 0, 0.08);
}
```

### Cards & Containers
```css
.card {
  background-color: #ffffff;
  border: 1px solid #e6e6e6;
  border-radius: 8px;
  box-shadow: rgba(0, 0, 0, 0.1) 0px 1px 2px;
  padding: 24px;
}

.card:hover {
  box-shadow: rgba(0, 0, 0, 0.2) 0px 4px 8px;
}
```

### Inputs & Forms
```css
.input-text {
  background-color: rgba(0, 0, 0, 0.08);
  border: 1px solid #e6e6e6;
  border-radius: 4px;
  padding: 12px;
  font-size: 16px;
}

.input-text:focus {
  outline: 2px solid #4d49fc;
}

.checkbox {
  accent-color: #4d49fc;
}
```

### Navigation
```css
.navbar {
  background-color: #ffffff;
  border-bottom: 1px solid #e6e6e6;
  padding: 16px 0;
}

.nav-link {
  color: #000000;
  padding: 8px 16px;
  text-decoration: none;
}

.nav-link:hover {
  text-decoration-color: initial;
}
```

### Links
```css
.link {
  color: #4d49fc;
  text-decoration: underline;
}

.link:hover {
  text-decoration-color: initial;
}

.link-secondary {
  color: #000000;
}
```

### Badges
```css
.badge-success {
  background-color: #24cb71;
  color: #ffffff;
  border-radius: 16px;
  padding: 4px 8px;
}

.badge-alert {
  background-color: #ff7237;
  color: #ffffff;
  border-radius: 16px;
  padding: 4px 8px;
}

.badge-info {
  background-color: #00b6ff;
  color: #ffffff;
  border-radius: 16px;
  padding: 4px 8px;
}
```

## 5. Layout Principles
- **Spacing System**: Base unit of 4px, scaling to 4, 8, 12, 16, 20, 24, 32, 40, 48, 64.
  - **Usage Context**: 
    - 4px: Small margins.
    - 8px: Between buttons.
    - 12px: Card padding.
    - 16px: Section spacing.
    - 24px: Larger element separation.
  
- **Grid & Container** 
_Note: container widths and column counts are not extracted from the source. The values below are reasonable defaults inferred from the visible layout density._
  - Max width: 1440px
  - Columns: 12
  - Gutter: 16px
  - Section padding: 32px

- **Whitespace Philosophy**: Whitespace is utilized to create visual separation between sections and elements, enhancing focus and readability.

- **Border Radius Scale**: 
  - 0px: Sharp corners (buttons).
  - 2px: Slightly rounded edges (inputs).
  - 4px: Standard rounding (cards).
  - 8px: Moderate rounding (modals).
  - 16px: Soft rounding (badges).

## 6. Depth & Elevation
| Level | Treatment                                      | Use                    |
|-------|------------------------------------------------|------------------------|
| z-0   | None                                           | Base elements          |
| z-1   | rgba(0, 0, 0, 0.08) 0px 1px 0px              | Subtle shadows         |
| z-2   | rgba(0, 0, 0, 0.1) 0px 24px 70px              | Elevated cards         |
| z-10  | rgb(255, 255, 255) 0px 0px 0px 1px inset     | Input fields           |
| z-20  | None                                           | Modals and popups      |

### Shadow Philosophy
Shadows are used to create depth, distinguishing elements such as cards and modals from the background. Subtle shadows enhance usability without overwhelming the visual hierarchy.

## 7. Do's and Don'ts

### Do's
- Use #4d49fc for primary buttons; ensure they stand out against #ffffff.
- Maintain a minimum of 24px between consecutive Cards for clarity.
- Use 16px font size for body text to ensure readability against #ffffff backgrounds.
- Ensure links use #4d49fc; hover state should maintain text-decoration.
- Use #ffffff for button text on #4d49fc backgrounds for contrast.
- Apply 8px border-radius on buttons to soften their appearance.
- Use 12px padding in inputs for comfortable interaction.
- Maintain 32px section padding to enhance layout clarity.

### Don'ts
- Never use #000000 text on #e6e6e6 backgrounds; it fails contrast requirements.
- Avoid using font sizes smaller than 16px for body text to maintain readability.
- Do not overcrowd elements; keep at least 24px spacing between buttons.
- Avoid using sharp corners on buttons; use at least 4px radius.
- Never use #000000 for primary button backgrounds; it reduces visibility.
- Do not use colors with low contrast ratios, such as #33dfdf on #ffffff.
- Avoid inconsistent font weights; use only specified weights for headings.
- Do not use non-standard spacing values; stick to the defined scale.

## 8. Responsive Behavior
_Note: breakpoints below are industry-standard recommendations, not measurements from the source. Adjust to the brand's actual media queries when implementing._
| Breakpoint Name | Width | Key Changes               |
|------------------|-------|---------------------------|
| Mobile Small     | 0-559 | Single-column layout      |
| Mobile Large     | 560+  | Two-column layout         |
| Tablet           | 768+  | Three-column layout       |
| Desktop          | 960+  | Standard grid layout      |
| Desktop Large    | 1280+ | Enhanced spacing          |

### Touch Targets
- Minimum size for buttons: 44px x 44px.
- Minimum spacing between touch targets: 16px.

### Collapsing Strategy
- **Navigation**: Collapse top-level links into a hamburger menu on mobile.
- **Cards**: Stack vertically on mobile.
- **Typography**: Scale down font sizes on mobile.
- **Padding**: Reduce section padding on mobile to 16px.
- **Spacing**: Maintain consistent spacing throughout.

## 9. Agent Prompt Guide
- **Quick Color Reference**
  - Background: #ffffff
  - Text: #000000
  - Accent: #4d49fc

- **Iteration Guide**
  1. Always use #4d49fc for primary buttons.
  2. Maintain font size at 16px for body text.
  3. Use only the 4 / 8 / 16 / 24 / 32 px values from the spacing scale.
  4. Ensure buttons have at least 8px border radius.
  5. Keep a minimum of 24px vertical space between Cards.
  6. Use #ffffff for text on #4d49fc backgrounds.
  7. Apply 12px padding in inputs for comfortable interaction.
  8. Use defined shadow values for elevation effects.