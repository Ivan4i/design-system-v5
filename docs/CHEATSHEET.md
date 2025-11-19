# Design System v5 - Cheatsheet

Быстрая шпаргалка по основным классам и переменным.

## 🎨 Цвета

### CSS Variables

```css
/* Primary */
--color-primary
--color-primary-hover
--color-primary-active

/* Semantic */
--color-success
--color-error
--color-warning
--color-info

/* Text */
--color-text-primary
--color-text-secondary
--color-text-tertiary

/* Background */
--color-bg-primary
--color-bg-secondary
--color-bg-tertiary

/* Borders */
--color-border-primary
--color-border-secondary
```

### Utility Classes

```css
.text-primary
.text-secondary
.text-tertiary
.bg-primary
.bg-secondary
```

## 🔘 Buttons

```html
<!-- Variants -->
<button class="btn btn--md btn--primary">Primary</button>
<button class="btn btn--md btn--secondary">Secondary</button>
<button class="btn btn--md btn--outline">Outline</button>
<button class="btn btn--md btn--ghost">Ghost</button>

<!-- Sizes -->
<button class="btn btn--sm btn--primary">Small</button>
<button class="btn btn--md btn--primary">Medium</button>
<button class="btn btn--lg btn--primary">Large</button>
```

## 📝 Inputs

```html
<!-- Text Input -->
<input class="input input--md" type="text">
<input class="input input--sm" type="text">
<input class="input input--lg" type="text">

<!-- With Error -->
<input class="input input--md input--error" type="text">

<!-- Textarea -->
<textarea class="input textarea"></textarea>
```

## 🃏 Cards

```html
<div class="card">Basic Card</div>
<div class="card card--elevated">Elevated</div>
<div class="card card--outlined">Outlined</div>
<div class="card card--interactive">Interactive</div>
```

## 🏷️ Badges

```html
<span class="badge badge--success">Success</span>
<span class="badge badge--error">Error</span>
<span class="badge badge--warning">Warning</span>
<span class="badge badge--info">Info</span>
<span class="badge badge--neutral">Neutral</span>
```

## 🔖 Tags

```html
<span class="tag">
  Tag Text
  <span class="tag__close">×</span>
</span>
```

## ⚠️ Alerts

```html
<div class="alert alert--success">Success message</div>
<div class="alert alert--error">Error message</div>
<div class="alert alert--warning">Warning message</div>
<div class="alert alert--info">Info message</div>
```

## 👤 Avatars

```html
<div class="avatar avatar--xs"><img src="..."></div>
<div class="avatar avatar--sm"><img src="..."></div>
<div class="avatar avatar--md"><img src="..."></div>
<div class="avatar avatar--lg"><img src="..."></div>
<div class="avatar avatar--xl"><img src="..."></div>
<div class="avatar avatar--2xl"><img src="..."></div>
```

## ⏳ Loaders

```html
<div class="spinner spinner--sm"></div>
<div class="spinner spinner--md"></div>
<div class="spinner spinner--lg"></div>
```

## 📏 Spacing

### CSS Variables

```css
--space-0   /* 0 */
--space-1   /* 4px */
--space-2   /* 8px */
--space-3   /* 12px */
--space-4   /* 16px */
--space-5   /* 20px */
--space-6   /* 24px */
--space-8   /* 32px */
--space-10  /* 40px */
--space-12  /* 48px */
--space-16  /* 64px */
```

### Utility Classes

```css
.mb-0, .mb-2, .mb-4, .mb-6, .mb-8  /* margin-bottom */
.mt-0, .mt-2, .mt-4, .mt-6, .mt-8  /* margin-top */
```

## 📐 Border Radius

```css
--radius-none   /* 0 */
--radius-sm     /* 2px */
--radius-base   /* 4px */
--radius-md     /* 6px */
--radius-lg     /* 8px */
--radius-xl     /* 12px */
--radius-2xl    /* 16px */
--radius-full   /* 9999px */
```

## 🌑 Shadows

```css
--shadow-xs
--shadow-sm
--shadow-base
--shadow-md
--shadow-lg
--shadow-xl

--shadow-button
--shadow-button-hover
--shadow-button-active

--shadow-hover-sm
--shadow-hover-md
--shadow-hover-lg
```

## ✍️ Typography

### Font Sizes

```css
--font-size-xs    /* 12px */
--font-size-sm    /* 14px */
--font-size-base  /* 16px */
--font-size-md    /* 18px */
--font-size-lg    /* 20px */
--font-size-xl    /* 24px */
--font-size-2xl   /* 30px */
--font-size-3xl   /* 36px */
--font-size-4xl   /* 48px */
--font-size-5xl   /* 60px */
```

### Font Weights

```css
--font-weight-thin       /* 100 */
--font-weight-light      /* 300 */
--font-weight-normal     /* 400 */
--font-weight-medium     /* 500 */
--font-weight-semibold   /* 600 */
--font-weight-bold       /* 700 */
--font-weight-extrabold  /* 800 */
--font-weight-black      /* 900 */
```

### Utility Classes

```css
.text-xs, .text-sm, .text-base, .text-lg, .text-xl

.font-normal
.font-medium
.font-semibold
.font-bold
```

## 📦 Layout Utilities

```css
/* Display */
.flex
.inline-flex
.grid
.block
.inline-block
.hidden

/* Flex */
.items-center
.items-start
.items-end
.justify-center
.justify-between
.justify-end

/* Gap */
.gap-2
.gap-4
.gap-6
```

## 📋 Forms

```html
<div class="form-group">
  <label class="form-label">Label</label>
  <input type="text" class="input input--md">
  <div class="form-helper">Helper text</div>
  <div class="form-error">Error message</div>
</div>
```

## 🎯 Quick Examples

### Button with Icon

```html
<button class="btn btn--md btn--primary flex items-center gap-2">
  <svg>...</svg>
  Click me
</button>
```

### Input with Label and Error

```html
<div class="form-group">
  <label class="form-label">Email</label>
  <input type="email" class="input input--md input--error">
  <div class="form-error">Invalid email</div>
</div>
```

### Card with Badge

```html
<div class="card">
  <div class="flex items-center justify-between mb-4">
    <h3>Title</h3>
    <span class="badge badge--success">Active</span>
  </div>
  <p class="text-secondary">Content</p>
</div>
```

### Alert with Icon

```html
<div class="alert alert--success flex items-start gap-3">
  <svg>...</svg>
  <div>Success message</div>
</div>
```

---

**Полная документация**: [DESIGN_SYSTEM.md](../DESIGN_SYSTEM.md)
