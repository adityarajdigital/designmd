# Design System Inspired by Notion

## 1. Visual Theme & Atmosphere
The visual atmosphere of Notion is characterized by a clean, modern aesthetic that emphasizes usability and clarity. The combination of dark and light backgrounds creates a striking contrast, while the use of vibrant accent colors adds a playful touch. The layout is structured, allowing for easy navigation and interaction, which enhances the overall user experience.

**Key Characteristics**
- Dark and light themes with high contrast.
- Vibrant accent colors for highlights and interactive elements.
- Clean typography with a focus on readability.
- Structured layout emphasizing functionality and ease of use.
- Use of icons and illustrations to enhance visual communication.
- Subtle shadows adding depth to components.
- Generous whitespace creating a balanced composition.

## 2. Color Palette & Roles

### Primary
- **#02093a** — Used as a primary accent color in various UI elements.
- **#62aef0** — Bright blue accent, utilized for links and buttons.
- **#455dd3** — Deeper blue accent, enhancing text and interactive elements.
- **#ffc95e** — Yellow accent, used for highlights and alerts.

### Accent Colors
- **#0075de** — Text accent, often used for links and interactive text.
- **#097fe8** — Another blue text accent, providing a vibrant touch.
- **#f77463** — Coral accent, used for alerts or notifications.
- **#ad6ded** — Soft purple accent, used in illustrations and highlights.

### Interactive
- **#000000** — Primary text color against light backgrounds.
- **#f6f5f4** — Text color for dark backgrounds, ensuring readability.
- **#615d59** — Muted text color for secondary information.

### Neutral Scale
- **#ffffff** — Base background color for light themes.
- **#f6f5f4** — Light background color used for sections and cards.
- **#000000** — Dark background for contrast and emphasis.

### Surface & Borders
- **#a39e98** — Used for subtle borders and text elements.

## 3. Typography Rules
- **Font Family**: NotionInter, Lyon Text, fallback: sans-serif.
- **Hierarchy**:

| Role       | Font        | Size  | Weight | Line Height | Letter Spacing | Notes                   |
|------------|-------------|-------|--------|-------------|----------------|-------------------------|
| Display    | NotionInter | 54px  | 700    | 1.2         | 0              | Large display headings   |
| H1         | NotionInter | 42px  | 700    | 1.2         | 0              | Main headings           |
| H2         | NotionInter | 26px  | 700    | 1.2         | 0              | Sub-headings            |
| Body       | NotionInter | 16px  | 400    | 1.5         | -0.015625rem    | Primary body text       |
| Caption    | NotionInter | 14px  | 400    | 1.5         | 0              | Small captions          |
| Code       | NotionInter | 16px  | 400    | 1.5         | 0              | Monospace for code      |

### Principles
- Emphasis on legibility with clear distinctions between headings and body text.
- Consistent use of weights to create a visual hierarchy.
- Generous line heights enhance readability across all text elements.

## 4. Component Stylings

### Buttons
**Primary Button**
```css
.button-primary {
    background-color: #000000;
    color: #ffffff;
    padding: 12px 24px;
    border-radius: 4px;
    font-size: 20px;
    font-weight: 400;
    transition: background-color 0.3s;
}
.button-primary:hover {
    background-color: #005bab;
}
.button-primary:disabled {
    background-color: #f6f5f4;
    color: #a39e98;
    cursor: not-allowed;
}
```

**Secondary Button**
```css
.button-secondary {
    background-color: transparent;
    color: #0075de;
    padding: 10px 20px;
    border: 1px solid #0075de;
    border-radius: 4px;
    font-size: 16px;
    font-weight: 400;
    transition: color 0.3s, border-color 0.3s;
}
.button-secondary:hover {
    color: #005bab;
    border-color: #005bab;
}
.button-secondary:disabled {
    color: #a39e98;
    border-color: #f6f5f4;
    cursor: not-allowed;
}
```

### Cards & Containers
**Standard Card**
```css
.card {
    background-color: #f6f5f4;
    border-radius: 8px;
    box-shadow: rgba(0, 0, 0, 0.01) 0px 0.175px 1.041px 0px, rgba(0, 0, 0, 0.02) 0px 0.8px 2.925px 0px;
    padding: 16px;
}
```

### Inputs & Forms
**Text Input**
```css
.input-text {
    border: 1px solid #d4d3cf;
    border-radius: 4px;
    padding: 12px;
    font-size: 16px;
    transition: box-shadow 0.3s;
}
.input-text:focus {
    box-shadow: rgba(35, 131, 226, 0.57) 0px 0px 0px 1px inset;
}
```

### Navigation
**Top Navigation Bar**
```css
.navbar {
    background-color: #ffffff;
    padding: 16px;
    box-shadow: rgba(0, 0, 0, 0.04) 0px 4px 18px 0px;
}
```

**Navigation Link**
```css
.nav-link {
    color: #000000;
    padding: 8px 16px;
    text-decoration: none;
    transition: color 0.3s;
}
.nav-link:hover {
    color: #0075de;
}
```

### Links
**Standard Link**
```css
.link {
    color: #0075de;
    text-decoration: underline;
}
.link:hover {
    color: #005bab;
}
```

### Badges
**Status Badge**
```css
.badge-success {
    background-color: #1aae39;
    color: #ffffff;
    padding: 4px 8px;
    border-radius: 12px;
}
.badge-alert {
    background-color: #ffc95e;
    color: #000000;
    padding: 4px 8px;
    border-radius: 12px;
}
```

## 5. Layout Principles
- **Spacing System**: Base unit 4px → 4, 8, 12, 16, 20, 24, 32, 40, 48, 64, 80.
  - Usage Context: 
    - 4px: Small margins
    - 8px: Element padding
    - 16px: Section spacing
    - 32px: Major section gaps
- **Grid & Container**: _Note: container widths and column counts are not extracted from the source. The values below are reasonable defaults inferred from the visible layout density._
  - Max width: 1200px, 12 columns, 20px gutter, 40px section padding.
- **Whitespace Philosophy**: Whitespace is used generously to create a spacious and uncluttered interface, allowing users to focus on content without distractions.
- **Border Radius Scale**: 
  - 4px: Minor elements
  - 8px: Standard elements
  - 12px: Cards and buttons

## 6. Depth & Elevation
| Level | Treatment                                                                 | Use                     |
|-------|---------------------------------------------------------------------------|-------------------------|
| z-0   | None                                                                      | Base elements           |
| z-1   | rgba(0, 0, 0, 0.01) 0px 0.175px 1.041px 0px                            | Icon buttons            |
| z-2   | rgba(0, 0, 0, 0.02) 0px 1px 3px 0px                                    | Header                  |
| z-3   | rgba(0, 0, 0, 0.04) 0px 4px 18px 0px                                   | Floating elements       |
| z-4   | rgba(0, 0, 0, 0.05) 0px 14px 28px 0px                                  | Modal dialogs           |

### Shadow Philosophy
Shadows are used subtly to create depth and separate layers of content without overwhelming the visual hierarchy. Lighter shadows are applied to base elements, while more pronounced shadows are reserved for interactive components.

## 7. Do's and Don'ts

### Do's
- Use #000000 for primary text on #ffffff backgrounds.
- Maintain 16px font size for body text to ensure readability.
- Apply 24px vertical spacing between sections for clarity.
- Utilize the Primary Button with a background of #000000 for CTAs.
- Ensure links use #0075de for visibility against backgrounds.
- Use 8px border radius for buttons to maintain consistency.
- Keep at least 16px padding around cards for aesthetic balance.
- Use #f6f5f4 for backgrounds of secondary elements to differentiate.

### Don'ts
- Never use #f6f5f4 for text over #ffffff; measured ratio 1.09 fails AA.
- Avoid using 14px font size for body text; it may reduce readability.
- Don't place elements closer than 16px; it creates clutter.
- Avoid using #a39e98 for primary buttons; it lacks contrast.
- Never use #ffffff for text on #f6f5f4; it fails contrast requirements.
- Don't use inconsistent border radius values; stick to 4px or 8px.
- Never crowd elements; maintain at least 24px spacing.
- Avoid using #f77463 for text; it may not be legible on light backgrounds.

## 8. Responsive Behavior
_Note: breakpoints below are industry-standard recommendations, not measurements from the source. Adjust to the brand's actual media queries when implementing._
- **Suggested Breakpoints**:

| Breakpoint Name    | Width | Key Changes                      |
|--------------------|-------|----------------------------------|
| Mobile Small       | 375px | Single-column layout             |
| Mobile Large       | 600px | Introduction of side menus       |
| Tablet             | 712px | Multi-column layout              |
| Desktop            | 1080px| Full navigation bar              |
| Desktop Large      | 1440px| Enhanced visuals and spacing     |

- **Touch Targets**: Minimum sizes/spacing of 44px for interactive elements.
- **Collapsing Strategy**: 
  - Navigation: Collapse into a hamburger menu on mobile.
  - Cards: Stack vertically on smaller screens.
  - Typography: Scale down headings for mobile views.
  - Padding: Reduce section padding to 20px on mobile.

## 9. Agent Prompt Guide
- **Quick Color Reference**:
  - Primary: #02093a
  - Accent: #62aef0
  - Background: #ffffff
  - Text: #000000

- **Iteration Guide**:
  1. Always use #000000 for primary text.
  2. Maintain a font size of 16px for body text.
  3. Use 24px spacing between sections.
  4. Ensure buttons have a border radius of 4px.
  5. Keep links in #0075de for visibility.
  6. Use #f6f5f4 for secondary background elements.
  7. Maintain a consistent color palette throughout.
  8. Use responsive breakpoints for layout adjustments.