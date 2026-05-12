# Design System Inspired by Mercury

## 1. Visual Theme & Atmosphere
Mercury's visual design combines dark backgrounds with vibrant accent colors, creating a modern and engaging atmosphere. The use of imagery and subtle animations enhances the user experience, making it feel dynamic and interactive. The overall aesthetic is grounded in a tech-centric approach, appealing to startups and entrepreneurs.

**Key Characteristics**
- Dark color scheme with deep neutrals (#1e1e2a, #171721).
- Vibrant accent colors (#5266eb, #9cb4e8) that stand out against the background.
- Clear hierarchy with large display text and bold headings.
- Smooth animations and transitions for interactive elements.
- Use of photography to create a narrative-driven experience.

## 2. Color Palette & Roles
- **Primary**:
  - Accent Blue (#5266eb) — Used for primary buttons and key call-to-action elements.
  - Light Blue (#9cb4e8) — Used for highlights and secondary accents.
  
- **Accent Colors**:
  - Light Purple (#cdddff) — Used in various UI elements for emphasis.
  
- **Interactive**:
  - Hover State (#5266eb29) — Applied on buttons for hover effects.

- **Neutral Scale**:
  - Dark Gray (#1e1e2a) — Primary background color.
  - Medium Gray (#afb2ce) — Used for text and borders.
  - Light Gray (#ededf3) — Used for text on dark backgrounds.

- **Surface & Borders**:
  - Border Color (#272735) — Used for subtle borders and dividers.

## 3. Typography Rules
- **Font Family**: 
  - Primary: `arcadia`, fallback: `ui-sans-serif`.

| Role        | Font      | Size   | Weight | Line Height | Letter Spacing | Notes          |
|-------------|-----------|--------|--------|-------------|----------------|-----------------|
| Display     | arcadia   | 65px   | 700    | 1.2         | 0              | Main display text|
| H1          | arcadia   | 42px   | 700    | 1.2         | 0              | Major headings   |
| H2          | arcadia   | 28px   | 700    | 1.2         | 0              | Subheadings      |
| Body        | arcadia   | 16px   | 400    | 1.5         | 0              | Standard text    |
| Caption     | arcadia   | 12px   | 400    | 1.5         | 0              | Small text       |

**Principles**
- Use larger sizes for headings to establish hierarchy.
- Maintain consistent weight across body text for readability.
- Utilize ample line height for improved legibility.

## 4. Component Stylings

### Buttons
**Primary Button**
```css
.button-primary {
  background-color: #5266eb;
  color: #ffffff;
  padding: 0px 20px;
  border-radius: 32px;
  font-weight: 420;
  font-size: 16px;
}
.button-primary:hover {
  background-color: #5266eb29;
}
.button-primary:disabled {
  background-color: #272735;
  color: #70707d;
}
```

**Secondary Button**
```css
.button-secondary {
  background-color: transparent;
  color: #ededf3;
  border: 1px solid #ededf3;
  padding: 0px 20px;
  border-radius: 40px;
  font-weight: 420;
  font-size: 16px;
}
.button-secondary:hover {
  background-color: #5266eb29;
}
.button-secondary:disabled {
  background-color: #272735;
  color: #70707d;
}
```

### Cards & Containers
**Standard Card**
```css
.card {
  background-color: #171721;
  border-radius: 12px;
  padding: 24px;
  box-shadow: rgba(0, 0, 0, 0.05) 0px 8px 12px;
}
```

### Inputs & Forms
**Text Input**
```css
.input {
  background-color: #ededf3;
  border: 1px solid #272735;
  border-radius: 8px;
  padding: 12px;
  font-size: 16px;
}
.input:focus {
  outline: 2px solid #5266eb;
}
.input:disabled {
  background-color: #f4f5f9;
  color: #70707d;
}
```

### Navigation
**Top Navigation Bar**
```css
.navbar {
  background-color: #1e1e2a;
  padding: 16px;
  display: flex;
  justify-content: space-between;
}
```

**Navigation Link**
```css
.nav-link {
  color: #ffffff;
  padding: 8px 16px;
}
.nav-link:hover {
  color: #9cb4e8;
}
```

### Links
**Standard Link**
```css
.link {
  color: #5266eb;
  text-decoration: none;
}
.link:hover {
  text-decoration: underline;
}
```

### Badges
**Status Badge**
```css
.badge-success {
  background-color: #9cb4e8;
  color: #ffffff;
  border-radius: 4px;
  padding: 4px 8px;
}
.badge-alert {
  background-color: #d03275;
  color: #ffffff;
  border-radius: 4px;
  padding: 4px 8px;
}
```

## 5. Layout Principles
- **Spacing System**: Base unit 4px → 4, 8, 12, 16, 20, 24, 32, 40, 48, 64, 80.
  - **Usage Context**: 
    - 4px: Margins between small elements.
    - 16px: Standard padding for containers.
    - 32px: Section spacing.
  
- **Grid & Container**
_Note: container widths and column counts are not extracted from the source. The values below are reasonable defaults inferred from the visible layout density._
```css
.container {
  max-width: 1200px;
  padding: 0 20px;
}
```

- **Whitespace Philosophy**: Whitespace is used strategically to separate content, ensuring clarity and focus on key elements.

- **Border Radius Scale**: 
  - Small: 4px (buttons)
  - Medium: 12px (cards)
  - Large: 40px (primary buttons)

## 6. Depth & Elevation
| Level | Treatment | Use |
|-------|-----------|-----|
| z-0   | None      | Base elements |
| z-1   | No shadow | Standard elements |
| z-2   | 0 0 0 0 0 | Overlays |
| z-3   | 0 0 0 0 0 | Modals |
| z-5   | 0 0 0 0 0 | Tooltips |

**Shadow Philosophy**: Shadows are used subtly to create depth, primarily for modals and cards.

## 7. Do's and Don'ts

### Do's
- Use #5266eb for primary button backgrounds.
- Apply 16px font size for body text.
- Maintain at least 24px spacing between sections.
- Use #1e1e2a for background colors of sections.
- Utilize 12px radius for input fields.
- Ensure headings use arcadia at 42px weight 700.
- Use #9cb4e8 for accent colors in highlights.
- Keep at least 16px padding in card components.

### Don'ts
- Don't use body text smaller than 16px.
- Avoid using #70707d for primary text.
- Never place buttons closer than 12px apart.
- Don't use #ffffff on dark backgrounds without sufficient contrast.
- Avoid using inconsistent border radii across components.
- Don't use more than 3 different font sizes in a single section.
- Never use #c3c3cc for primary call-to-action elements.
- Avoid low contrast combinations like #ededf3 on #9cb4e8.

## 8. Responsive Behavior
_Note: breakpoints below are industry-standard recommendations, not measurements from the source. Adjust to the brand's actual media queries when implementing._

| Breakpoint Name | Width | Key Changes |
|------------------|-------|-------------|
| Mobile Small     | 320px | Stack layout, single column |
| Mobile Large     | 480px | Slightly larger buttons |
| Tablet           | 768px | Introduce grid layout |
| Desktop          | 1024px| Full layout with sidebars |
| Desktop Large    | 1440px| Enhanced visuals and spacing |

- **Touch Targets**: Minimum button size of 44px x 44px.
- **Collapsing Strategy**: 
  - Navigation: Collapse to a hamburger menu on mobile.
  - Cards: Stack vertically on smaller screens.
  - Typography: Maintain legibility with responsive text sizes.

## 9. Agent Prompt Guide
- **Quick Color Reference**
  - Primary: #5266eb
  - Accent: #9cb4e8
  - Neutral: #1e1e2a

- **Iteration Guide**
  1. Always use #5266eb for primary actions.
  2. Maintain typography hierarchy with specified sizes.
  3. Use 4px increments for spacing.
  4. Ensure button heights are consistent at 40px.
  5. Apply 12px border radius for inputs.
  6. Use 16px padding for card content.
  7. Ensure hover states are defined for all buttons.
  8. Use responsive breakpoints for layout adjustments.
  9. Maintain contrast ratios above 4.5:1 for text.
  10. Use #1e1e2a for backgrounds in dark mode.