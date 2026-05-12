# Design System Inspired by Vercel

## 1. Visual Theme & Atmosphere
Vercel's design presents a modern and dynamic environment, characterized by clean lines and a vibrant color palette. The layout is spacious, allowing for easy navigation and readability, while the use of gradients and geometric shapes adds a sense of depth and movement to the overall aesthetic.

**Key Characteristics**
- Clean, spacious layout with ample white space.
- Vibrant gradient background in the hero section.
- Geometric shapes as signature visual elements.
- High contrast text for readability.
- Consistent use of rounded corners across components.
- Monochrome and colorful accents creating visual interest.
- Minimalist iconography and typography.

## 2. Color Palette & Roles

### Primary
- **Accent Color**: #0070f3 — Used for primary actions and highlights.
  
### Accent Colors
- **Text Accent**: #0068d6 — Used for secondary text accents.
- **Text Accent**: #7820bc — Another variant for text accentuation.

### Interactive
- **Hover State**: #4d4d4d — Used for links and buttons on hover.
- **Focus State**: #171717 — Used for focus outlines on interactive elements.

### Neutral Scale
- **Background**: #ffffff — Main background color.
- **Background Light**: #fafafa — Subtle background for sections.
- **Text Primary**: #171717 — Main text color for high contrast.
- **Text Secondary**: #666666 — Used for secondary text.

### Surface & Borders
- **Border Color**: #ebebeb — Used for subtle borders and dividers.

## 3. Typography Rules
- **Font Family**: Geist, with a fallback stack of system fonts, and Geist Mono for code.
- **Hierarchy**:

| Role        | Font         | Size | Weight | Line Height | Letter Spacing | Notes                |
|-------------|--------------|------|--------|-------------|----------------|----------------------|
| Display     | Geist Mono   | 48px | 400    | 1.2         |                | Main display text.   |
| H1          | Geist Mono   | 32px | 400    | 1.2         |                | Primary heading.     |
| H2          | Geist Mono   | 24px | 400    | 1.2         |                | Secondary heading.   |
| H3          | Geist Mono   | 20px | 400    | 1.2         |                | Tertiary heading.    |
| Body        | Geist        | 14px | 400    | 1.5         |                | Main body text.      |
| Caption     | Geist        | 12px | 400    | 1.5         |                | Caption text.        |
| Code/Mono   | Geist Mono   | 14px | 400    | 1.5         |                | Code snippets.       |

### Principles
- The typography hierarchy is clear, with larger sizes for headings and smaller for body text.
- Consistent use of weights across headings and body text enhances readability.
- The font family provides a modern and technical feel, suitable for a developer audience.

## 4. Component Stylings

### Buttons
**Primary Button**
```css
.button-primary {
  background-color: #171717;
  color: #ffffff;
  border: none;
  border-radius: 100px;
  padding: 0px 14px;
  font-size: 16px;
  font-weight: 500;
  transition: background-color 0.2s;
}
.button-primary:hover {
  background-color: #0070f3;
}
.button-primary:disabled {
  opacity: 0.5;
}
```

**Secondary Button**
```css
.button-secondary {
  background-color: #ffffff;
  color: #171717;
  border: 1px solid #ebebeb;
  border-radius: 6px;
  padding: 0px 6px;
  font-size: 14px;
  font-weight: 500;
  transition: background-color 0.2s;
}
.button-secondary:hover {
  background-color: #f0f0f0;
}
.button-secondary:disabled {
  opacity: 0.5;
}
```

**Ghost Button**
```css
.button-ghost {
  background-color: transparent;
  color: #4d4d4d;
  border: 1px solid transparent;
  border-radius: 9999px;
  padding: 8px 12px;
  font-size: 14px;
  font-weight: 400;
  transition: color 0.15s;
}
.button-ghost:hover {
  color: #0070f3;
}
```

### Cards & Containers
**Standard Card**
```css
.card {
  background-color: #ffffff;
  border-radius: 6px;
  box-shadow: rgba(0, 0, 0, 0.08) 0px 0px 0px 1px, rgba(0, 0, 0, 0.04) 0px 2px 2px 0px;
  padding: 16px;
}
```

### Inputs & Forms
**Text Input**
```css
.input {
  border: 1px solid #ebebeb;
  border-radius: 4px;
  padding: 12px;
  font-size: 14px;
  color: #171717;
}
.input:focus {
  border-color: #0070f3;
}
.input.error {
  border-color: #e00;
}
```

**Form Label**
```css
.label {
  font-size: 14px;
  color: #666666;
}
```

**Checkbox/Radio**
```css
.checkbox {
  cursor: pointer;
}
.checkbox:checked {
  background-color: #0070f3;
}
```

### Navigation
**Top Navigation Bar**
```css
.navbar {
  background-color: #ffffff;
  padding: 16px;
  box-shadow: rgba(0, 0, 0, 0.1) 0px 2px 4px;
}
```

**Navigation Link**
```css
.nav-link {
  color: #4d4d4d;
  text-decoration: none;
  padding: 8px 12px;
}
.nav-link:hover {
  color: #0070f3;
}
```

**Dropdown Menu**
```css
.dropdown {
  position: relative;
}
.dropdown-menu {
  background-color: #ffffff;
  box-shadow: rgba(0, 0, 0, 0.1) 0px 2px 4px;
}
```

### Links
**Standard Link**
```css
.link {
  color: #0070f3;
  text-decoration: none;
}
.link:hover {
  text-decoration: underline;
}
```

**Secondary Link**
```css
.link-secondary {
  color: #4d4d4d;
}
.link-secondary:hover {
  color: #0070f3;
}
```

### Badges
**Status Badge**
```css
.badge-success {
  background-color: #28a745;
  color: #ffffff;
  border-radius: 4px;
  padding: 4px 8px;
}
.badge-alert {
  background-color: #dc3545;
  color: #ffffff;
  border-radius: 4px;
  padding: 4px 8px;
}
.badge-info {
  background-color: #17a2b8;
  color: #ffffff;
  border-radius: 4px;
  padding: 4px 8px;
}
```

## 5. Layout Principles
- **Spacing System**: Base unit of 4px, scaling to 4, 8, 12, 16, 24, 32, 40, 48, 64.
  - **Usage Context**:
    - 4px: Small margins.
    - 8px: Standard padding.
    - 16px: Section spacing.
    - 24px: Card spacing.
    - 32px: Header/footer spacing.

- **Grid & Container**
_Note: container widths and column counts are not extracted from the source. The values below are reasonable defaults inferred from the visible layout density._
  - Max width: 1400px.
  - Columns: 12.
  - Gutter: 16px.
  - Section padding: 32px.

- **Whitespace Philosophy**: Vercel utilizes whitespace effectively to create a spacious layout, enhancing readability and user interaction.

- **Border Radius Scale**: 
  - 2px: Subtle elements.
  - 4px: Buttons and inputs.
  - 6px: Cards.
  - 9999px: Circular elements.

## 6. Depth & Elevation
| Level | Treatment                                                                 | Use                          |
|-------|---------------------------------------------------------------------------|------------------------------|
| z-0   | None                                                                      | Base layer                   |
| z-1   | rgba(0, 0, 0, 0.08) 0px 0px 0px 1px, rgba(0, 0, 0, 0.04) 0px 2px 2px 0px | Cards                        |
| z-2   | rgba(0, 0, 0, 0.08) 0px 0px 0px 1px, rgb(250, 250, 250) 0px 0px 0px 1px  | Modals                       |
| z-100 | rgba(0, 0, 0, 0.1) 0px 2px 4px                                          | Navigation bar               |
| z-1000| rgba(0, 0, 0, 0.1) 0px 4px 8px                                          | Popups                       |

**Shadow Philosophy**: Shadows are used to create depth and separation between layers, enhancing the visual hierarchy and guiding the user's attention.

## 7. Do's and Don'ts

### Do's
- Use #0070f3 for primary buttons to ensure visibility.
- Maintain 16px padding around cards for consistent spacing.
- Use Display 48/400 for main headings to create emphasis.
- Keep at least 32px of vertical space between sections for clarity.
- Use the 4px border radius on buttons for a modern look.
- Ensure body text is set at 14px for readability.
- Use #171717 for text on #ffffff backgrounds for high contrast.
- Always use the Primary Button for key actions to guide users.

### Don'ts
- Never use #666666 for body text on #fafafa backgrounds; it fails AA contrast.
- Avoid using less than 16px padding on inputs to maintain usability.
- Do not apply a border radius of 0 on cards; it disrupts the design language.
- Refrain from using H1 weight on body text; it creates hierarchy confusion.
- Don't overcrowd elements; maintain at least 24px between buttons.
- Avoid using more than 3 colors in a single section to maintain focus.
- Do not use #4d4d4d for text on #ffffff backgrounds; it reduces legibility.
- Never mix font sizes within the same heading level; maintain consistency.

## 8. Responsive Behavior
_Note: breakpoints below are industry-standard recommendations, not measurements from the source. Adjust to the brand's actual media queries when implementing._
- **Suggested Breakpoints**:

| Breakpoint Name     | Width  | Key Changes                             |
|---------------------|--------|-----------------------------------------|
| Mobile Small        | 600px  | Stack elements vertically                |
| Mobile Large        | 640px  | Adjust padding to fit smaller screens    |
| Tablet              | 768px  | Change layout to two columns             |
| Desktop             | 961px  | Utilize full grid layout                 |
| Desktop Large       | 1440px | Expand content width for readability     |

- **Touch Targets**: Minimum sizes should be 44px for buttons and links.

- **Collapsing Strategy**:
  - Navigation: Collapse into a hamburger menu on mobile.
  - Cards: Stack vertically on smaller screens.
  - Typography: Scale down headings for smaller devices.
  - Padding: Reduce padding to 16px on mobile.
  - Spacing: Use 8px spacing between elements on mobile.

## 9. Agent Prompt Guide
- **Quick Color Reference**:
  - Primary: #0070f3
  - Background: #ffffff
  - Text: #171717
  - Accent: #0068d6

- **Iteration Guide**:
  1. Always use #0070f3 for primary buttons.
  2. Maintain 16px font size for body text.
  3. Use 24px spacing between sections.
  4. Apply 4px border radius for buttons.
  5. Ensure headings use Geist Mono for consistency.
  6. Use z-1 for card elevation.
  7. Set minimum touch targets to 44px.
  8. Use the gradient background at 135deg for hero sections.