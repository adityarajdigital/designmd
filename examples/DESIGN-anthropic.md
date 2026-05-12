# Design System Inspired by Anthropic

## 1. Visual Theme & Atmosphere
Anthropic's visual theme is characterized by a sophisticated use of dark and light contrasts, primarily featuring a dark background that enhances readability and focus on content. The layout employs ample white space, allowing for a clean presentation of information and a sense of openness. The typography combines modern sans-serif and serif fonts, contributing to a professional yet approachable atmosphere.

- Key Characteristics:
  - Dark background (#141413) with light text for high contrast.
  - Use of light neutrals (#faf9f5, #e3dacc) for backgrounds and text.
  - Prominent typography hierarchy with varying weights and sizes.
  - Clean layout with ample whitespace.
  - Subtle use of imagery and icons to support content.
  - Interactive elements that respond to user actions (hover, focus).

## 2. Color Palette & Roles
### Primary
- **Dark Background (#141413)** — Used for main backgrounds to provide a strong contrast with text.
- **Light Neutral (#faf9f5)** — Utilized for text and background sections for readability.

### Accent Colors
- **Text Color (#b0aea5)** — Applied for secondary text elements.
- **Inverse Text Color (#e8e6dc)** — Used for text on dark backgrounds.

### Interactive
- **Link Hover Color (#3d3d3a)** — Changes color on hover for links.
- **Button Hover Color (#0055d4)** — Background color change for buttons on hover.

### Neutral Scale
- **Medium Neutral (#e3dacc)** — Used in various text elements and backgrounds.
- **Light Neutral (#f0eee6)** — For subtle backgrounds and card elements.

### Surface & Borders
- **Border Color (#1414131a)** — Used for subtle borders and outlines.

## 3. Typography Rules
- **Font Family**: 
  - Primary: `Anthropic Sans`, sans-serif
  - Monospace: `Anthropic Mono`, monospace

| Role      | Font            | Size  | Weight | Line Height | Letter Spacing | Notes                     |
|-----------|-----------------|-------|--------|-------------|----------------|---------------------------|
| Display H1| Anthropic Sans  | 91px  | 700    | 1.2         | 0              | Main heading              |
| Display H2| Anthropic Sans  | 61px  | 700    | 1.2         | 0              | Sub-heading               |
| H2        | Anthropic Sans  | 24px  | 700    | 1.2         | 0              | Section titles            |
| H3        | Anthropic Sans  | 20px  | 400    | 1.5         | 0              | Sub-section headings      |
| Body      | Anthropic Sans  | 18px  | 400    | 1.5         | 0              | Main body text            |
| Body      | Anthropic Sans  | 16px  | 400    | 1.5         | 0              | Secondary body text       |
| Caption   | Anthropic Sans  | 12px  | 400    | 1.5         | 0              | Captions and notes        |
| Code      | Anthropic Mono  | 16px  | 400    | 1.5         | 0              | Code snippets             |

### Principles
- Emphasis on readability with ample line height and appropriate font sizes.
- Distinct hierarchy achieved through varying weights and sizes.
- Consistent use of a sans-serif font for a modern look.

## 4. Component Stylings

### Buttons
#### Primary Button
```css
.button {
  background-color: transparent;
  color: #141413;
  border: 1px solid #141413;
  border-radius: 0;
  padding: 22.4px 12px;
  font-size: 20px;
  font-weight: 400;
}
.button:hover {
  background-color: rgb(0, 85, 212);
  box-shadow: rgba(8, 8, 8, 0.08) 0px 1px 1px, rgba(8, 8, 8, 0.2) 0px 1px 1px, rgba(255, 255, 255, 0.12) 0px 6px 12px inset;
}
```

#### Secondary Button
```css
.button-secondary {
  background-color: transparent;
  color: #b0aea5;
  border: 1px solid #b0aea5;
  border-radius: 0;
  padding: 22.4px 12px;
  font-size: 20px;
  font-weight: 400;
}
.button-secondary:hover {
  background-color: #e3dacc;
}
```

### Cards & Containers
#### Standard Card
```css
.card {
  background-color: #faf9f5;
  border-radius: 8px;
  padding: 16px;
  box-shadow: none;
}
```

### Inputs & Forms
#### Text Input
```css
.input-text {
  border: 1px solid #141413;
  padding: 12px;
  border-radius: 8px;
}
.input-text:focus {
  outline: none;
  border-color: rgb(0, 85, 212);
}
```

### Navigation
#### Top Navigation Bar
```css
.navbar {
  background-color: #141413;
  padding: 16px;
  display: flex;
  justify-content: space-between;
}
.nav-link {
  color: #faf9f5;
  text-decoration: none;
}
.nav-link:hover {
  color: #3d3d3a;
}
```

### Links
#### Standard Link
```css
.link {
  color: #141413;
  text-decoration: none;
}
.link:hover {
  color: #3d3d3a;
}
```

## 5. Layout Principles
- **Spacing System**: Base unit of 4px, scaling to 8, 12, 16, 20, 32, 48, 64, 80, 96.
  - Usage Context:
    - 4px: Small margins
    - 8px: Standard padding
    - 16px: Section margins
    - 32px: Larger element spacing

- **Grid & Container** 
  _Note: container widths and column counts are not extracted from the source. The values below are reasonable defaults inferred from the visible layout density._
  
- **Max Width**: 1200px
- **Columns**: 12
- **Gutter**: 16px
- **Section Padding**: 32px

- **Whitespace Philosophy**: Whitespace is used strategically to create a clean and organized layout, enhancing readability and visual hierarchy.

- **Border Radius Scale**: 
  - 8px: Standard corner rounding
  - 16px: Used for card elements
  - 24px: Used for larger containers

## 6. Depth & Elevation
| Level | Treatment | Use |
|-------|-----------|-----|
| z-0   | none      | Flat elements |
| z-1   | none      | Nav elements |
| z-2   | box-shadow: rgba(0, 0, 0, 0.1) 0px 2px 4px | Dropdowns |
| z-3   | box-shadow: rgba(0, 0, 0, 0.2) 0px 4px 8px | Cards |
| z-4   | box-shadow: rgba(0, 0, 0, 0.3) 0px 8px 16px | Modals |

### Shadow Philosophy
Shadows are used minimally to provide depth to interactive elements, enhancing usability without overwhelming the visual hierarchy.

## 7. Do's and Don'ts

### Do's
- Use #141413 for main text on #faf9f5 backgrounds.
- Maintain 32px padding around sections for breathing space.
- Apply 8px border radius to all card elements.
- Use #b0aea5 for secondary text against dark backgrounds.
- Ensure buttons have 22.4px vertical padding for consistency.
- Use 20px font size for primary buttons to ensure visibility.
- Implement hover states with a color change for links.
- Keep at least 16px spacing between text blocks.

### Don'ts
- Never use #faf9f5 for text on #f0eee6 backgrounds; measured ratio 3.85 fails AA.
- Avoid using font sizes smaller than 12px for body text.
- Do not use non-rounded corners on buttons; keep radius at 0 or 8px.
- Avoid overcrowding sections; maintain at least 32px vertical space.
- Do not use #b0aea5 for primary text on #141413 backgrounds.
- Avoid using less than 20px font size for headings.
- Do not mix font weights inconsistently; use 400 for body text.
- Avoid using more than 4 different colors in a single section.

## 8. Responsive Behavior
_Note: breakpoints below are industry-standard recommendations, not measurements from the source. Adjust to the brand's actual media queries when implementing._
| Breakpoint Name       | Width | Key Changes                      |
|-----------------------|-------|----------------------------------|
| Mobile Small          | 480px | Stack navigation links           |
| Mobile Large          | 768px | Adjust card layout               |
| Tablet                | 991px | Change grid layout               |
| Desktop               | 1200px| Full-width sections              |

### Touch Targets
- Minimum button height: 44px
- Minimum link touch area: 48px

### Collapsing Strategy
- Navigation: Collapse into a hamburger menu on mobile.
- Cards: Stack vertically on smaller screens.
- Typography: Scale down headings on mobile.
- Padding: Reduce section padding to 16px on mobile.

## 9. Agent Prompt Guide
- **Quick Color Reference**:
  - Dark Background: #141413
  - Light Neutral: #faf9f5
  - Text Color: #b0aea5

- **Iteration Guide**:
  1. Always use 20px for primary button text.
  2. Maintain a border radius of 8px on cards.
  3. Ensure at least 32px padding around sections.
  4. Use #141413 for main text on light backgrounds.
  5. Keep headings at a minimum of 20px font size.
  6. Use 22.4px padding on buttons.
  7. Ensure links change color on hover.
  8. Use responsive breakpoints for layout adjustments.