---
name: "Apple HIG Frontend Designer"
description: "Design professional web/mobile interfaces following Apple Human Interface Guidelines. Use for iOS/macOS style UI, Liquid Glass effects, SF Symbols, and HIG-compliant components."
dependencies: ""
---

# Apple HIG Frontend Designer

A professional-grade frontend design skill that enables Claude Code to create interfaces following Apple's Human Interface Guidelines (HIG), achieving the quality standards of Apple's design team.

## When to Use This Skill

Activate this skill when users request:
- Apple-style or iOS/macOS-style interfaces
- HIG-compliant UI components
- Liquid Glass design effects
- SF Symbols integration
- San Francisco typography implementation
- Commands: `/apple`, `/hig`, `/ios-design`

**Trigger phrases:**
- "Design an Apple-style..."
- "Create a HIG-compliant..."
- "iOS/macOS style component"
- "苹果风格的界面"
- "符合 HIG 的设计"

---

## Core Design Principles

### The Four Pillars of Apple Design

1. **Clarity (清晰)**
   - Every element has a purpose
   - Eliminate unnecessary complexity
   - Users understand immediately without instructions
   - Use clear visual hierarchy

2. **Deference (尊重内容)**
   - UI elements support, not compete with content
   - Minimize chrome and visual noise
   - Let content be the hero
   - Use subtle backgrounds and borders

3. **Depth (层次)**
   - Create clear visual hierarchy through layers
   - Use shadows, blur, and translucency purposefully
   - Motion reinforces spatial relationships
   - Z-axis communicates importance

4. **Consistency (一致性)**
   - Familiar patterns across platforms
   - Predictable interactions
   - Unified visual language
   - Respect platform conventions

---

## Design System Specifications

### Typography System

**Font Family:** San Francisco (SF Pro)

```css
/* System Font Stack for Web */
:root {
  --font-system: -apple-system, BlinkMacSystemFont, 'SF Pro Display',
                 'SF Pro Text', 'Helvetica Neue', Arial, sans-serif;
  --font-mono: 'SF Mono', SFMono-Regular, Menlo, Monaco, monospace;
}

/* Font Size Scale (iOS) */
--text-caption2: 11px;    /* Caption 2 */
--text-caption1: 12px;    /* Caption 1 */
--text-footnote: 13px;    /* Footnote */
--text-subhead: 15px;     /* Subheadline */
--text-body: 17px;        /* Body - Default */
--text-headline: 17px;    /* Headline (semibold) */
--text-title3: 20px;      /* Title 3 */
--text-title2: 22px;      /* Title 2 */
--text-title1: 28px;      /* Title 1 */
--text-large-title: 34px; /* Large Title */
```

**Typography Rules:**
- Use SF Pro Display for sizes ≥ 20pt
- Use SF Pro Text for sizes < 20pt
- Maintain consistent line-height (1.2-1.5)
- Use weight for hierarchy, not just size

### Color System

```css
/* Apple System Colors - Light Mode */
:root {
  /* Primary Colors */
  --system-blue: #007AFF;
  --system-green: #34C759;
  --system-indigo: #5856D6;
  --system-orange: #FF9500;
  --system-pink: #FF2D55;
  --system-purple: #AF52DE;
  --system-red: #FF3B30;
  --system-teal: #5AC8FA;
  --system-yellow: #FFCC00;

  /* Gray Scale */
  --system-gray: #8E8E93;
  --system-gray2: #AEAEB2;
  --system-gray3: #C7C7CC;
  --system-gray4: #D1D1D6;
  --system-gray5: #E5E5EA;
  --system-gray6: #F2F2F7;

  /* Semantic Colors */
  --label-primary: #000000;
  --label-secondary: rgba(60, 60, 67, 0.6);
  --label-tertiary: rgba(60, 60, 67, 0.3);
  --label-quaternary: rgba(60, 60, 67, 0.18);

  /* Backgrounds */
  --bg-primary: #FFFFFF;
  --bg-secondary: #F2F2F7;
  --bg-tertiary: #FFFFFF;

  /* Separators */
  --separator: rgba(60, 60, 67, 0.29);
  --separator-opaque: #C6C6C8;
}

/* Dark Mode */
@media (prefers-color-scheme: dark) {
  :root {
    --system-blue: #0A84FF;
    --system-green: #30D158;
    --system-indigo: #5E5CE6;
    --system-orange: #FF9F0A;
    --system-pink: #FF375F;
    --system-purple: #BF5AF2;
    --system-red: #FF453A;
    --system-teal: #64D2FF;
    --system-yellow: #FFD60A;

    --system-gray: #8E8E93;
    --system-gray2: #636366;
    --system-gray3: #48484A;
    --system-gray4: #3A3A3C;
    --system-gray5: #2C2C2E;
    --system-gray6: #1C1C1E;

    --label-primary: #FFFFFF;
    --label-secondary: rgba(235, 235, 245, 0.6);
    --label-tertiary: rgba(235, 235, 245, 0.3);
    --label-quaternary: rgba(235, 235, 245, 0.18);

    --bg-primary: #000000;
    --bg-secondary: #1C1C1E;
    --bg-tertiary: #2C2C2E;

    --separator: rgba(84, 84, 88, 0.6);
    --separator-opaque: #38383A;
  }
}
```

### Spacing System

**8pt Grid System:**
```css
:root {
  --space-1: 4px;   /* Extra small */
  --space-2: 8px;   /* Small */
  --space-3: 12px;  /* Medium-small */
  --space-4: 16px;  /* Medium */
  --space-5: 20px;  /* Medium-large */
  --space-6: 24px;  /* Large */
  --space-8: 32px;  /* Extra large */
  --space-10: 40px; /* 2X large */
  --space-12: 48px; /* 3X large */
}
```

**Touch Target Requirements:**
- **iOS:** Minimum 44×44 points
- **visionOS:** Minimum 60 points tap area
- Always add sufficient padding for small visual elements

### Border Radius (Concentric Design)

```css
:root {
  /* Base radius values */
  --radius-sm: 8px;
  --radius-md: 12px;
  --radius-lg: 16px;
  --radius-xl: 20px;
  --radius-2xl: 24px;
  --radius-full: 9999px; /* Capsule */
}

/* Concentric Rule: inner_radius + padding = outer_radius */
/* Example: 8px inner + 8px padding = 16px outer */
```

---

## Component Patterns

### Buttons

```css
/* Primary Button - Capsule Style */
.btn-primary {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  min-height: 44px;
  padding: 12px 24px;
  font-family: var(--font-system);
  font-size: 17px;
  font-weight: 600;
  color: #FFFFFF;
  background: var(--system-blue);
  border: none;
  border-radius: var(--radius-full);
  cursor: pointer;
  transition: transform 0.1s ease, opacity 0.1s ease;
}

.btn-primary:hover {
  opacity: 0.9;
}

.btn-primary:active {
  transform: scale(0.98);
}

/* Secondary Button */
.btn-secondary {
  min-height: 44px;
  padding: 12px 24px;
  font-family: var(--font-system);
  font-size: 17px;
  font-weight: 600;
  color: var(--system-blue);
  background: rgba(0, 122, 255, 0.1);
  border: none;
  border-radius: var(--radius-full);
  cursor: pointer;
}
```

### Liquid Glass Effect (2025)

```css
/* Liquid Glass Background */
.glass-panel {
  background: rgba(255, 255, 255, 0.7);
  backdrop-filter: blur(20px) saturate(180%);
  -webkit-backdrop-filter: blur(20px) saturate(180%);
  border: 1px solid rgba(255, 255, 255, 0.3);
  border-radius: var(--radius-xl);
  box-shadow:
    0 4px 6px rgba(0, 0, 0, 0.02),
    0 12px 24px rgba(0, 0, 0, 0.04);
}

@media (prefers-color-scheme: dark) {
  .glass-panel {
    background: rgba(28, 28, 30, 0.7);
    border: 1px solid rgba(255, 255, 255, 0.1);
  }
}
```

### Cards

```css
.card {
  background: var(--bg-tertiary);
  border-radius: var(--radius-lg);
  padding: var(--space-4);
  box-shadow:
    0 1px 3px rgba(0, 0, 0, 0.04),
    0 4px 12px rgba(0, 0, 0, 0.04);
}

/* Card with Grouped Style */
.card-grouped {
  background: var(--bg-secondary);
  border-radius: var(--radius-xl);
  overflow: hidden;
}

.card-grouped-item {
  background: var(--bg-tertiary);
  padding: var(--space-4);
  border-bottom: 1px solid var(--separator);
}

.card-grouped-item:last-child {
  border-bottom: none;
}
```

### Input Fields

```css
.input-field {
  width: 100%;
  min-height: 44px;
  padding: 12px 16px;
  font-family: var(--font-system);
  font-size: 17px;
  color: var(--label-primary);
  background: var(--bg-secondary);
  border: none;
  border-radius: var(--radius-md);
  outline: none;
  transition: box-shadow 0.2s ease;
}

.input-field:focus {
  box-shadow: 0 0 0 4px rgba(0, 122, 255, 0.3);
}

.input-field::placeholder {
  color: var(--label-tertiary);
}
```

---

## Animation Guidelines

### Timing Functions

```css
:root {
  /* Apple's preferred easing */
  --ease-default: cubic-bezier(0.25, 0.1, 0.25, 1);
  --ease-in: cubic-bezier(0.42, 0, 1, 1);
  --ease-out: cubic-bezier(0, 0, 0.58, 1);
  --ease-in-out: cubic-bezier(0.42, 0, 0.58, 1);

  /* Spring-like easing */
  --ease-spring: cubic-bezier(0.175, 0.885, 0.32, 1.275);
}
```

### Duration Scale

```css
:root {
  --duration-instant: 100ms;  /* Micro-interactions */
  --duration-fast: 200ms;     /* Hover, focus states */
  --duration-normal: 300ms;   /* Standard transitions */
  --duration-slow: 500ms;     /* Complex animations */
}
```

### Interaction Feedback

```css
/* Press feedback */
.interactive {
  transition: transform var(--duration-instant) var(--ease-out);
}

.interactive:active {
  transform: scale(0.97);
}

/* Hover glow */
.interactive:hover {
  box-shadow: 0 0 0 4px rgba(0, 122, 255, 0.15);
}
```

---

## SF Symbols Integration

### Rendering Modes

1. **Monochrome:** Single color for all layers
2. **Hierarchical:** Opacity variations for depth
3. **Palette:** Custom colors per layer
4. **Multicolor:** Apple's intrinsic symbol colors

### Usage Guidelines

- **Toolbar/Navigation:** Use outline variant
- **Tab Bar:** Use fill variant
- **Match text size:** Symbols auto-align with SF font
- **Provide text alternatives:** Always include aria-label

### Web Implementation (Icon Font Alternative)

```html
<!-- Using SF Symbols via system font -->
<span class="sf-symbol" aria-label="Settings">􀣋</span>

<!-- Or use equivalent system icons -->
<svg class="icon" aria-hidden="true">
  <use href="#icon-gear"></use>
</svg>
```

---

## Accessibility Requirements

### Color Contrast
- **Normal text:** 4.5:1 minimum (WCAG AA)
- **Large text:** 3:1 minimum
- **Interactive elements:** Clearly distinguishable states

### Motion
```css
@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
  }
}
```

### Semantic HTML
```html
<!-- Always use semantic elements -->
<button type="button">Action</button>
<nav aria-label="Main navigation">...</nav>
<main role="main">...</main>
```

---

## Output Format

When generating Apple-style UI code, always include:

1. **Complete, runnable code** (CSS/React/Vue)
2. **Light/Dark mode support** via CSS custom properties
3. **Design rationale** explaining HIG compliance
4. **Responsive breakpoints** for different devices
5. **Accessibility attributes** (aria-*, role, etc.)

### Example Output Structure

```jsx
/**
 * Apple HIG Compliant Component
 *
 * Design Decisions:
 * - Uses SF Pro system font stack for native feel
 * - 44pt minimum touch target for accessibility
 * - Capsule shape for primary actions (HIG recommendation)
 * - Liquid Glass effect for modern depth
 * - Supports prefers-color-scheme for auto theming
 */

const AppleButton = ({ children, variant = 'primary', ...props }) => {
  return (
    <button
      className={`btn btn-${variant}`}
      {...props}
    >
      {children}
    </button>
  );
};
```

---

## Best Practices Checklist

Before finalizing any design output, verify:

- [ ] **Typography:** Using SF Pro with correct size thresholds
- [ ] **Colors:** System colors with Light/Dark variants
- [ ] **Spacing:** Following 8pt grid
- [ ] **Touch targets:** Minimum 44×44pt
- [ ] **Border radius:** Concentric relationships maintained
- [ ] **Animations:** Using Apple-standard easing curves
- [ ] **Accessibility:** WCAG AA compliant, reduced motion support
- [ ] **Consistency:** Matches platform conventions

---

## Resources

- [Apple Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines)
- [Apple Design Resources](https://developer.apple.com/design/resources/)
- [SF Symbols](https://developer.apple.com/sf-symbols/)
- [Apple Fonts](https://developer.apple.com/fonts/)
- [WWDC25: Get to know the new design system](https://developer.apple.com/videos/play/wwdc2025/356/)

---

*This skill ensures Claude Code produces interfaces that meet Apple's exacting design standards, creating cohesive, accessible, and beautiful user experiences.*
