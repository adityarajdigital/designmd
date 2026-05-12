# Design System Inspired by Airbnb

## 1. Visual Theme & Atmosphere
Airbnb presents a clean and inviting interface that emphasizes user-friendliness and accessibility. The design utilizes ample white space and a straightforward layout, allowing users to navigate effortlessly through listings and information. The visual hierarchy is clear, with prominent calls to action and essential information easily accessible.

**Key Characteristics**
- Predominantly white background (#ffffff) enhances readability.
- Use of soft neutral colors for subtle contrast and background elements (#f2f2f2, #dddddd).
- Bold accent colors for key actions and highlights (#ff385c, #e00b41).
- Consistent typography with a modern sans-serif aesthetic (Airbnb Cereal VF).
- Card-based layout for property listings, providing a structured and organized feel.
- Interactive elements are highlighted with hover effects for better engagement.
- Clear visual hierarchy that guides users through content seamlessly.

## 2. Color Palette & Roles
### **Primary**
- **Accent (#e00b41)** — Used for primary actions and highlights.
- **Text Accent (#ff385c)** — Emphasizes important text and links.

### **Accent Colors**
- **Background (#f2f2f2)** — Used for secondary backgrounds and containers.
- **Neutral (#dddddd)** — Provides structural support in the layout.

### **Interactive**
- **Hover Color (#222222)** — Changes for links and buttons on hover.
- **Active Color (#ff385c)** — Used for active states of buttons and links.

### **Neutral Scale**
- **Text Primary (#222222)** — Main text color for readability.
- **Text Secondary (#6a6a6a)** — Used for less emphasized text.
- **Text Inverse (#ffffff)** — For text on darker backgrounds.

### **Surface & Borders**
- **Border (#b0b0b0)** — Light borders for card elements and inputs.

## 3. Typography Rules
- **Font Family**: Airbnb Cereal VF, with fallback to system fonts.
  
| Role   | Font                | Size  | Weight | Line Height | Letter Spacing | Notes                  |
|--------|---------------------|-------|--------|-------------|----------------|------------------------|
| H1     | Airbnb Cereal VF    | 22px  | 400    | 1.5         | normal         | Main headings          |
| H2     | Airbnb Cereal VF    | 20px  | 400    | 1.5         | normal         | Subheadings            |
| H3     | Airbnb Cereal VF    | 16px  | 400    | 1.5         | normal         | Section titles         |
| Body   | Airbnb Cereal VF    | 16px  | 400    | 1.5         | normal         | Main body text         |
| Caption| Airbnb Cereal VF    | 12px  | 400    | 1.5         | normal         | Small text elements     |
| Code   | Airbnb Cereal VF    | 14px  | 400    | 1.5         | normal         | Code blocks            |

### **Principles**
- Consistent use of a single font family enhances brand identity.
- Hierarchical font sizes create clear distinctions between content levels.
- Adequate line heights improve readability across various device sizes.

## 4. Component Stylings

### Buttons
**Primary Button**
```css
.button-primary {
    background-color: #e00b41;
    color: #ffffff;
    font-size: 14px;
    font-weight: 500;
    padding: 12px 24px;
    border-radius: 20px;
    border: none;
    box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 8px;
}

.button-primary:hover {
    background-color: #ff385c;
}

.button-primary:disabled {
    background-color: #dddddd;
    color: #b0b0b0;
}
```

**Secondary Button**
```css
.button-secondary {
    background-color: transparent;
    color: #222222;
    font-size: 14px;
    font-weight: 400;
    padding: 12px 24px;
    border: 1px solid #222222;
    border-radius: 20px;
    box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 8px;
}

.button-secondary:hover {
    color: #ff385c;
}

.button-secondary:disabled {
    color: #b0b0b0;
    border-color: #b0b0b0;
}
```

### Cards & Containers
**Standard Card**
```css
.card {
    background-color: #ffffff;
    border-radius: 16px;
    box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 8px;
    padding: 16px;
    margin: 16px;
}

.card:hover {
    box-shadow: rgba(0, 0, 0, 0.2) 0px 8px 16px;
}
```

### Inputs & Forms
**Text Input**
```css
.input-text {
    border: 1px solid #dddddd;
    border-radius: 8px;
    padding: 12px;
    font-size: 16px;
    color: #222222;
}

.input-text:focus {
    border-color: #e00b41;
    box-shadow: 0 0 0 3px rgba(224, 11, 65, 0.3);
}
```

### Navigation
**Top Navigation Bar**
```css
.navbar {
    background-color: #ffffff;
    box-shadow: rgba(0, 0, 0, 0.1) 0px 2px 4px;
    padding: 16px;
}

.nav-link {
    color: #222222;
    padding: 12px;
    text-decoration: none;
}

.nav-link:hover {
    color: #ff385c;
}
```

### Links
**Standard Link**
```css
.link {
    color: #222222;
    text-decoration: none;
}

.link:hover {
    color: #ff385c;
}
```

### Badges
**Status Badge**
```css
.badge-success {
    background-color: #8DD19E;
    color: #ffffff;
    padding: 4px 8px;
    border-radius: 12px;
}

.badge-alert {
    background-color: #ff385c;
    color: #ffffff;
    padding: 4px 8px;
    border-radius: 12px;
}
```

## 5. Layout Principles
- **Spacing System**: Base unit 4px → 4, 8, 12, 16, 20, 24, 32, 40. 
  - **Usage Context**: 
    - 4px for small elements.
    - 8px for margins between buttons.
    - 16px for card padding.
    - 32px for section spacing.

- **Grid & Container**
_Note: container widths and column counts are not extracted from the source. The values below are reasonable defaults inferred from the visible layout density._
```css
.container {
    max-width: 1200px;
    padding: 0 16px;
}
```

- **Whitespace Philosophy**: Whitespace is strategically used to separate content, enhancing readability and focus on key elements.

- **Border Radius Scale**: 
  - 8px for inputs.
  - 16px for cards.
  - 20px for primary buttons.

## 6. Depth & Elevation
| Level | Treatment                                                                 | Use                           |
|-------|---------------------------------------------------------------------------|-------------------------------|
| z-0   | box-shadow: none                                                         | Flat elements                 |
| z-1   | box-shadow: rgba(0, 0, 0, 0.02) 0px 0px 0px 1px                         | Basic elevation               |
| z-2   | box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 8px                             | Cards                         |
| z-3   | box-shadow: rgba(0, 0, 0, 0.1) 0px 8px 24px                           | Modals                        |
| z-4   | box-shadow: rgba(0, 0, 0, 0.2) 0px 4px 8px                           | Floating elements             |

### Shadow Philosophy
Shadows are used to create depth and separation between elements, enhancing the overall hierarchy and usability of the interface.

## 7. Do's and Don'ts

### Do's
- Use #e00b41 for primary buttons to draw attention.
- Ensure text color #222222 on #ffffff backgrounds for high contrast.
- Apply 16px padding in cards for comfortable spacing.
- Utilize the 20px border radius for buttons for a softer appearance.
- Maintain a font size of 16px for body text for readability.
- Use #f2f2f2 for secondary backgrounds to create subtle contrast.
- Keep 24px vertical space between consecutive Cards for visual clarity.
- Use #ff385c for hover states on links to enhance interactivity.

### Don'ts
- Never use #c1c1c1 on #f7f7f7 backgrounds; measured ratio fails AA.
- Avoid using border-radius values lower than 8px for input fields.
- Do not overcrowd elements; maintain at least 16px of spacing.
- Avoid using font sizes smaller than 12px for body text.
- Never apply #b0b0b0 for primary text; use #222222 instead.
- Do not use less than 24px for touch targets in mobile views.
- Avoid using more than 4 different colors in a single component.
- Never mix font weights in the same text block; maintain hierarchy.

## 8. Responsive Behavior
_Note: breakpoints below are industry-standard recommendations, not measurements from the source. Adjust to the brand's actual media queries when implementing._
| Breakpoint Name     | Width  | Key Changes                      |
|---------------------|--------|----------------------------------|
| Mobile Small        | 375px  | Stack cards vertically           |
| Mobile Large        | 744px  | Adjust navigation to dropdown    |
| Tablet              | 950px  | Increase card size               |
| Desktop             | 1128px | Display cards in grid layout     |
| Desktop Large       | 1440px | Maximize card width              |

### Touch Targets
- Minimum size for touch targets: 44px x 44px.
- Maintain at least 16px spacing between touch targets.

### Collapsing Strategy
- **Navigation**: Collapse into a hamburger menu on mobile.
- **Cards**: Stack vertically on mobile.
- **Typography**: Adjust font sizes down to 14px on mobile.
- **Padding**: Reduce padding to 8px on mobile views.

## 9. Agent Prompt Guide
- **Quick Color Reference**
  - Accent: #e00b41
  - Background: #ffffff
  - Neutral: #dddddd
  - Text Primary: #222222
  - Text Secondary: #6a6a6a

- **Iteration Guide**
  1. Always use #e00b41 for primary buttons.
  2. Maintain a font size of 16px for body text.
  3. Use 24px spacing between cards.
  4. Keep border radius at 20px for buttons.
  5. Use #222222 for primary text on #ffffff backgrounds.
  6. Ensure hover states use #ff385c for links.
  7. Apply 16px padding in cards for comfortable spacing.
  8. Maintain minimum touch target sizes of 44px x 44px.