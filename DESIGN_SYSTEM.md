# Design System Documentation

## 📋 Содержание

1. [Основы](#основы)
2. [Цветовая палитра](#цветовая-палитра)
3. [Типографика](#типографика)
4. [Spacing & Layout](#spacing--layout)
5. [Компоненты](#компоненты)
6. [Паттерны](#паттерны)
7. [Состояния](#состояния)
8. [Иконки](#иконки)
9. [Flutter Компоненты](#flutter-компоненты-из-реального-кода)

---

## Основы

### Принципы дизайна

- **Консистентность**: Единообразие визуальных элементов и паттернов взаимодействия во всех продуктах. Используйте одинаковые отступы, цвета и компоненты для схожих задач.
- **Читаемость**: Приоритет контрасту и размерам шрифтов для обеспечения комфортного восприятия информации пользователями всех возрастов.
- **Эффективность**: Минимизация когнитивной нагрузки через понятную иерархию информации и интуитивные паттерны навигации.
- **Адаптивность**: Гибкость дизайна для работы на различных устройствах и разрешениях от мобильных телефонов до широких десктопных экранов.

### Философия

> Наша дизайн-система создана для построения современных, доступных и масштабируемых интерфейсов. Мы верим в силу консистентности и простоты, позволяя командам быстро создавать продукты высокого качества без необходимости заново изобретать базовые паттерны.

---

## Цветовая палитра

### Primary Colors

```css
/* Основной цвет бренда - из Flutter кода */
--color-primary: #7B61FF;
--color-primary-hover: #6B51EF;
--color-primary-active: #5B41DF;
--color-primary-light: #E8E3FF;
--color-primary-dark: #4B31BF;

/* Вторичный цвет */
--color-secondary: #8B5CF6;
--color-secondary-hover: #7C3AED;
--color-secondary-active: #6D28D9;
```

### Semantic Colors

```css
/* Success / Trend Up */
--color-success: #10B981;
--color-success-bg: #D1FAE5;
--color-success-border: #6EE7B7;

/* Error / Trend Down */
--color-error: #EF4444;
--color-error-bg: #FEE2E2;
--color-error-border: #FCA5A5;

/* Warning / Hot */
--color-warning: #F59E0B;
--color-warning-bg: #FEF3C7;
--color-warning-border: #FCD34D;

/* Info */
--color-info: #3B82F6;
--color-info-bg: #DBEAFE;
--color-info-border: #93C5FD;

/* Accent - из TabBar кода */
--color-accent: #4141E6;
--color-accent-hover: #3131D6;
--color-accent-active: #2121C6;
```

### Neutral Colors

```css
/* Text - из Flutter кода */
--color-text-primary: #09101D;
--color-text-secondary: #747B84;  /* Обновлено из TabBar кода */
--color-text-tertiary: #9CA3AF;
--color-text-disabled: #D1D5DB;
--color-text-inverse: #FFFFFF;

/* Backgrounds - из Flutter кода */
--color-bg-primary: #FFFFFF;
--color-bg-secondary: #EAEEF2;
--color-bg-tertiary: #F3F4F6;
--color-bg-quaternary: #F4F6F9;  /* Из TabBar кода */
--color-bg-elevated: #FFFFFF;
--color-bg-overlay: rgba(0, 0, 0, 0.5);
--color-bg-dark: #12202F;

/* Stroke / Borders */
--color-border-primary: #E5E7EB;
--color-border-secondary: #D1D5DB;
--color-border-focus: #3B82F6;
--color-border-disabled: #F3F4F6;

/* Shades */
--color-gray-50: #F9FAFB;
--color-gray-100: #F3F4F6;
--color-gray-150: #F4F6F9;  /* Из TabBar кода */
--color-gray-175: #F0F1F2;  /* Из TabBar кода - для теней */
--color-gray-200: #E5E7EB;
--color-gray-300: #D1D5DB;
--color-gray-400: #9CA3AF;
--color-gray-450: #747B84;  /* Из TabBar кода - вторичный текст */
--color-gray-500: #6B7280;
--color-gray-600: #4B5563;
--color-gray-700: #374151;
--color-gray-800: #1F2937;
--color-gray-900: #111827;
```

### Chart Colors

```css
/* Для графиков и визуализации данных */
--color-chart-1: #3B82F6;
--color-chart-2: #8B5CF6;
--color-chart-3: #EC4899;
--color-chart-4: #F59E0B;
--color-chart-5: #10B981;
--color-chart-6: #06B6D4;
--color-chart-7: #6366F1;
--color-chart-8: #F43F5E;
```

### Gradients

```css
/* Градиенты для специальных элементов */
--gradient-primary: linear-gradient(135deg, #667EEA 0%, #764BA2 100%);
--gradient-secondary: linear-gradient(135deg, #F093FB 0%, #F5576C 100%);
--gradient-accent: linear-gradient(135deg, #4FACFE 0%, #00F2FE 100%);
```

### Brand Icon Colors

```css
/* Цвета для иконок брендов и социальных сетей */
--color-brand-facebook: #1877F2;
--color-brand-twitter: #1DA1F2;
--color-brand-instagram: #E4405F;
--color-brand-linkedin: #0A66C2;
--color-brand-youtube: #FF0000;
--color-brand-github: #181717;
```

---

## Типографика

### Font Family

```css
/* Из Flutter кода - основной шрифт Archivo */
--font-primary: 'Archivo', -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Oxygen', 'Ubuntu', 'Cantarell', 'Fira Sans', 'Droid Sans', 'Helvetica Neue', sans-serif;
--font-secondary: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
--font-mono: 'JetBrains Mono', 'Fira Code', 'Monaco', 'Consolas', 'Courier New', monospace;
```

### Font Sizes

```css
--font-size-2xs: 0.625rem;    /* 10px - из TabBar кода (badge text) */
--font-size-xs: 0.75rem;      /* 12px */
--font-size-xs-plus: 0.8125rem; /* 13px - из TabBar кода (action text) */
--font-size-sm: 0.875rem;     /* 14px */
--font-size-base: 1rem;       /* 16px - из Flutter кода */
--font-size-md: 1.125rem;     /* 18px */
--font-size-lg: 1.25rem;      /* 20px */
--font-size-xl: 1.5rem;       /* 24px */
--font-size-2xl: 1.875rem;    /* 30px */
--font-size-3xl: 2.25rem;     /* 36px */
--font-size-4xl: 3rem;        /* 48px */
--font-size-5xl: 3.75rem;     /* 60px */
--font-size-6xl: 4.5rem;      /* 72px - из Flutter кода */
```

### Font Weights

```css
--font-weight-thin: 100;
--font-weight-light: 300;
--font-weight-normal: 400;
--font-weight-medium: 500;
--font-weight-semibold: 600;
--font-weight-bold: 700;
--font-weight-extrabold: 800;
--font-weight-black: 900;
```

### Line Heights

```css
--line-height-super-tight: 0.70;  /* Из Flutter кода - для больших заголовков */
--line-height-tight: 1.25;
--line-height-snug: 1.375;
--line-height-comfortable: 1.40;  /* Из Flutter кода */
--line-height-normal: 1.5;
--line-height-relaxed: 1.625;
--line-height-loose: 2;
```

### Text Styles

#### Headings

- **Display (Super H1)**: Font: 72px/4.5rem, Weight: 800 (Extrabold), Line Height: 0.70, Letter Spacing: -0.02em (Из Flutter кода)
- **H1**: Font: 48px/3rem, Weight: 700 (Bold), Line Height: 1.2, Letter Spacing: -0.02em
- **H2**: Font: 36px/2.25rem, Weight: 700 (Bold), Line Height: 1.25, Letter Spacing: -0.01em
- **H3**: Font: 30px/1.875rem, Weight: 600 (Semibold), Line Height: 1.3, Letter Spacing: -0.01em
- **H4**: Font: 24px/1.5rem, Weight: 600 (Semibold), Line Height: 1.35, Letter Spacing: 0
- **H5**: Font: 20px/1.25rem, Weight: 600 (Semibold), Line Height: 1.4, Letter Spacing: 0
- **H6**: Font: 18px/1.125rem, Weight: 600 (Semibold), Line Height: 1.45, Letter Spacing: 0

#### Body Text

- **Body Large**: Font: 18px/1.125rem, Weight: 400 (Normal), Line Height: 1.625
- **Body**: Font: 16px/1rem, Weight: 700 (Bold), Line Height: 1.40 (Из Flutter кода)
- **Body Regular**: Font: 16px/1rem, Weight: 400 (Normal), Line Height: 1.5
- **Body Small**: Font: 14px/0.875rem, Weight: 400 (Normal), Line Height: 1.5
- **Caption**: Font: 12px/0.75rem, Weight: 400 (Normal), Line Height: 1.4, Color: text-secondary

#### Tracking (Letter Spacing)

```css
--letter-spacing-tight: -0.02em;
--letter-spacing-normal: 0;
--letter-spacing-wide: 0.02em;
--letter-spacing-wider: 0.05em;
```

---

## Spacing & Layout

### Spacing Scale

```css
/* Из Flutter кода - базовые значения spacing */
--space-0: 0;
--space-0-25: 0.0625rem; /* 1px - из TabBar кода */
--space-0-5: 0.125rem;  /* 2px - из TabBar кода */
--space-1: 0.25rem;   /* 4px */
--space-1-25: 0.3125rem; /* 5px - из TabBar кода */
--space-1-5: 0.375rem;  /* 6px - из Flutter кода */
--space-2: 0.5rem;    /* 8px - из Flutter кода */
--space-2-5: 0.625rem;  /* 10px - из Flutter кода */
--space-3: 0.75rem;   /* 12px */
--space-4: 1rem;      /* 16px - из Flutter кода */
--space-5: 1.25rem;   /* 20px - из Flutter кода */
--space-6: 1.5rem;    /* 24px */
--space-8: 2rem;      /* 32px */
--space-8-5: 2.125rem;  /* 34px - из TabBar кода */
--space-10: 2.5rem;   /* 40px - из TabBar кода */
--space-12: 3rem;     /* 48px */
--space-12-5: 3.125rem;  /* 50px - из Flutter кода */
--space-16: 4rem;     /* 64px */
--space-20: 5rem;     /* 80px */
--space-24: 6rem;     /* 96px */
--space-25: 6.25rem;  /* 100px - из Flutter кода */
```

### Border Radius

```css
/* Из Flutter кода - border radius значения */
--radius-none: 0;
--radius-2xs: 0.0625rem;  /* 1px - из TabBar кода */
--radius-sm: 0.125rem;    /* 2px */
--radius-base: 0.25rem;   /* 4px */
--radius-md: 0.375rem;    /* 6px */
--radius-lg: 0.5rem;      /* 8px - из Flutter кода */
--radius-xl: 0.75rem;     /* 12px - из TabBar кода */
--radius-2xl: 1rem;       /* 16px */
--radius-3xl: 0.9375rem;  /* 15px - из Flutter кода */
--radius-badge: 1.25rem;  /* 20px - из TabBar кода (badge radius) */
--radius-4xl: 5rem;       /* 80px - из Flutter кода */
--radius-5xl: 6.25rem;    /* 100px - из Flutter кода */
--radius-full: 9999px;
```

### Shadows

#### Card Shadows

```css
--shadow-xs: 0 1px 2px 0 rgba(0, 0, 0, 0.05);
--shadow-sm: 0 1px 3px 0 rgba(0, 0, 0, 0.1), 0 1px 2px 0 rgba(0, 0, 0, 0.06);
--shadow-base: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
--shadow-md: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
--shadow-lg: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
--shadow-xl: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
```

#### Button Shadows

```css
--shadow-button: 0 1px 3px 0 rgba(0, 0, 0, 0.1), 0 1px 2px 0 rgba(0, 0, 0, 0.06);
--shadow-button-hover: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
--shadow-button-active: 0 1px 2px 0 rgba(0, 0, 0, 0.05);
```

#### Hover Shadows

```css
--shadow-hover-sm: 0 2px 4px 0 rgba(0, 0, 0, 0.1);
--shadow-hover-md: 0 8px 16px 0 rgba(0, 0, 0, 0.12);
--shadow-hover-lg: 0 12px 24px 0 rgba(0, 0, 0, 0.15);
```

#### TabBar Shadow

```css
/* Из TabBar кода - subtle top border shadow */
--shadow-tabbar: 0 -1px 0 0 #F0F1F2;
```

### Borders

#### Border Width

```css
--border-width-0: 0;
--border-width-1: 1px;
--border-width-2: 2px;
--border-width-4: 4px;
```

#### Border Offset

```css
--border-offset-0: 0;
--border-offset-1: 1px;
--border-offset-2: 2px;
```

### Opacity Scale

```css
--opacity-0: 0;
--opacity-10: 0.1;
--opacity-20: 0.2;
--opacity-30: 0.3;
--opacity-40: 0.4;
--opacity-50: 0.5;
--opacity-60: 0.6;
--opacity-70: 0.7;
--opacity-80: 0.8;
--opacity-90: 0.9;
--opacity-100: 1;
```

---

## Компоненты

### 1. Cards

#### Basic Card

- **Padding**: 24px (space-6)
- **Border Radius**: 8px (radius-lg)
- **Background**: color-bg-primary (#FFFFFF)
- **Shadow**: shadow-base
- **Border**: 1px solid color-border-primary

**Варианты:**
- **Elevated Card**: Shadow: shadow-md, No border
- **Outlined Card**: Border: 1px solid color-border-primary, Shadow: none
- **Interactive Card**: Hover: shadow-hover-md, Cursor: pointer, Transition: all 0.2s ease

#### Пример использования

```css
.card {
  padding: var(--space-6);
  border-radius: var(--radius-lg);
  background: var(--color-bg-primary);
  box-shadow: var(--shadow-base);
  border: var(--border-width-1) solid var(--color-border-primary);
  transition: all 0.2s ease;
}

.card--elevated {
  box-shadow: var(--shadow-md);
  border: none;
}

.card--interactive:hover {
  box-shadow: var(--shadow-hover-md);
  transform: translateY(-2px);
}
```

---

### 2. Buttons

#### Primary Button

- **Size**:
  - Small: Height: 32px, Padding: 8px 16px, Font: 14px
  - Medium: Height: 40px, Padding: 10px 20px, Font: 16px
  - Large: Height: 48px, Padding: 12px 24px, Font: 18px
- **Radius**: radius-md (6px)
- **States**:
  - Default: Background: color-primary, Color: white, Shadow: shadow-button
  - Hover: Background: color-primary-hover, Shadow: shadow-button-hover, Transform: translateY(-1px)
  - Active: Background: color-primary-active, Shadow: shadow-button-active, Transform: translateY(0)
  - Disabled: Background: color-gray-300, Color: color-text-disabled, Cursor: not-allowed, Opacity: 0.6

#### Secondary Button

- **Size**: Same as Primary
- **Radius**: radius-md (6px)
- **States**:
  - Default: Background: color-secondary, Color: white
  - Hover: Background: color-secondary-hover

#### Outline Button

- **Border**: 1px solid color-primary
- **Background**: transparent
- **States**:
  - Hover: Background: color-primary-light, Border-color: color-primary-hover

#### Ghost Button

- **Background**: transparent
- **States**:
  - Hover: Background: color-gray-100

---

### 3. Inputs

#### Text Input

- **Height**:
  - Small: 32px
  - Medium: 40px
  - Large: 48px
- **Padding**: 10px 12px (medium)
- **Radius**: radius-md (6px)
- **Border**: 1px solid color-border-primary
- **States**:
  - Focus: Border: 2px solid color-border-focus, Outline: none
  - Error: Border: 1px solid color-error
  - Disabled: Background: color-bg-tertiary, Cursor: not-allowed, Opacity: 0.6

#### Textarea

- **Min Height**: 80px
- **Padding**: 10px 12px
- **Radius**: radius-md (6px)
- **Resize**: vertical

#### Select

- **Height**: 40px (medium)
- **Padding**: 10px 36px 10px 12px
- **Icon**: Chevron down, Right: 12px, Size: 16px

---

### 4. Badges & Tags

#### Badge

- **Padding**: 4px 8px
- **Radius**: radius-full (9999px)
- **Font Size**: font-size-xs (12px)
- **Variants**:
  - Success: Background: color-success-bg, Color: color-success, Border: 1px solid color-success-border
  - Error: Background: color-error-bg, Color: color-error, Border: 1px solid color-error-border
  - Warning: Background: color-warning-bg, Color: color-warning, Border: 1px solid color-warning-border
  - Info: Background: color-info-bg, Color: color-info, Border: 1px solid color-info-border
  - Neutral: Background: color-gray-100, Color: color-gray-700, Border: 1px solid color-gray-300

#### Tag

- **Padding**: 6px 12px
- **Radius**: radius-base (4px)
- **Font Size**: font-size-sm (14px)
- **Close Button**: Size: 14px, Margin-left: 8px, Color: color-text-tertiary, Hover: color-text-primary

---

### 5. Forms

#### Form Layout

- **Label**:
  - Margin Bottom: space-2 (8px)
  - Font Weight: font-weight-medium (500)
  - Font Size: font-size-sm (14px)
- **Field Group**:
  - Margin Bottom: space-5 (20px)
- **Helper Text**:
  - Margin Top: space-2 (8px)
  - Font Size: font-size-sm (14px)
  - Color: color-text-secondary
- **Error Message**:
  - Color: color-error
  - Font Size: font-size-sm (14px)

---

### 6. Tables

#### Table Structure

- **Row Height**:
  - Compact: 36px
  - Default: 48px
  - Comfortable: 56px
- **Cell Padding**: 12px 16px
- **Header**:
  - Background: color-bg-secondary
  - Font Weight: font-weight-semibold (600)
  - Border Bottom: 2px solid color-border-primary
- **Row Borders**: 1px solid color-border-primary
- **Hover State**: Background: color-bg-secondary
- **Striped Rows**: Even rows: background color-gray-50

---

### 7. Navigation

#### Main Navigation

- **Height**: 64px
- **Background**: color-bg-elevated
- **Shadow**: shadow-sm
- **Item Padding**: 12px 16px
- **States**:
  - Default: Color: color-text-secondary
  - Hover: Color: color-text-primary, Background: color-bg-secondary
  - Active: Color: color-primary, Border-bottom: 2px solid color-primary

#### Sidebar Navigation

- **Width**: 256px
- **Item Height**: 40px
- **Item Padding**: 10px 16px
- **States**:
  - Hover: Background: color-gray-100
  - Active: Background: color-primary-light, Color: color-primary, Border-left: 3px solid color-primary

---

### 8. Charts

#### Line Chart

- **Line Width**: 2px
- **Point Radius**: 4px
- **Grid Lines**: Color: color-gray-200, Width: 1px
- **Colors**: Use chart colors (--color-chart-1 to --color-chart-8)

#### Bar Chart

- **Bar Spacing**: 8px
- **Border Radius**: radius-sm (2px) на верхних углах
- **Colors**: Use chart colors

#### Pie/Donut Chart

- **Border Width**: 2px (white)
- **Spacing**: 2px between segments
- **Colors**: Use chart colors

---

### 9. Avatars

#### Sizes

- **XS**: 24px × 24px
- **Small**: 32px × 32px
- **Medium**: 40px × 40px
- **Large**: 48px × 48px
- **XL**: 64px × 64px
- **2XL**: 96px × 96px

#### Styles

- **Border Radius**: radius-full (circle) или radius-md (rounded square)
- **Border**: 2px solid white (для группировки)
- **Placeholder**: Background: color-gray-300, Icon/Initials: color-gray-600
- **Status Indicator**: Size: 25% of avatar, Border: 2px solid white, Position: bottom-right

---

### 10. List Items

#### List Item

- **Height**: 48px (medium)
- **Padding**: 12px 16px
- **Border Bottom**: 1px solid color-border-primary
- **States**:
  - Hover: Background: color-bg-secondary
  - Active: Background: color-primary-light
  - Selected: Background: color-primary-light, Border-left: 3px solid color-primary

---

### 11. Messages / Notifications

#### Toast Notification

- **Width**: 320px (mobile: 100%)
- **Padding**: 16px
- **Radius**: radius-lg (8px)
- **Shadow**: shadow-lg
- **Position**: Top-right: 16px или Bottom-center
- **Variants**: Success, Error, Warning, Info (используют semantic colors)
- **Auto-dismiss**: 5 секунд (опционально)

#### Alert Banner

- **Padding**: 16px 20px
- **Border Left**: 4px solid (цвет варианта)
- **Background**: Соответствующий bg цвет (success-bg, error-bg, etc.)
- **Close Button**: Right: 12px, Top: 12px

---

### 12. Panels & Cards

#### Side Panel

- **Width**: 400px (desktop), 100% (mobile)
- **Background**: color-bg-primary
- **Shadow**: shadow-xl
- **Padding**: 24px
- **Header**:
  - Padding Bottom: 16px
  - Border Bottom: 1px solid color-border-primary

#### Modal

- **Max Width**: 600px (small), 800px (medium), 1000px (large)
- **Background**: color-bg-primary
- **Border Radius**: radius-xl (12px)
- **Shadow**: shadow-xl
- **Overlay**: Background: color-bg-overlay, Backdrop-filter: blur(4px)
- **Padding**: 24px

---

### 13. Accordion / FAQ

#### Accordion Item

- **Padding**: 16px
- **Border**: 1px solid color-border-primary
- **Border Radius**: radius-md (6px)
- **Margin Bottom**: 8px
- **States**:
  - Collapsed: Icon: chevron-right
  - Expanded: Icon: chevron-down, Background: color-bg-secondary
  - Hover: Background: color-bg-secondary (if collapsed)

---

### 14. Loading States

#### Skeleton Loader

- **Background**: Linear gradient animation от color-gray-200 до color-gray-300
- **Animation**: 1.5s ease-in-out infinite
- **Border Radius**: Matches component (text: 4px, avatar: full, card: 8px)
- **Sizes**: Match target element dimensions

#### Spinner

- **Size**: Small: 16px, Medium: 24px, Large: 32px
- **Color**: color-primary
- **Animation**: Rotate 360deg в 1s linear infinite

---

### 15. Empty States

#### Empty State Layout

- **Icon**: Size: 64px, Color: color-gray-400
- **Heading**: Font-size: xl (24px), Weight: semibold, Color: color-text-primary
- **Description**: Font-size: base (16px), Color: color-text-secondary
- **Action Button**: Primary button variant
- **Spacing**:
  - Icon → Heading: 16px
  - Heading → Description: 8px
  - Description → Button: 24px

---

### 16. Special Effects

#### Focus Ring

```css
--focus-ring: 0 0 0 3px rgba(59, 130, 246, 0.3);
```

#### Backdrop Blur

```css
--backdrop-blur-sm: blur(4px);
--backdrop-blur-base: blur(8px);
--backdrop-blur-md: blur(12px);
--backdrop-blur-lg: blur(16px);
```

---

## Паттерны

### Dashboard Layouts

#### Grid Dashboard

- **Grid**: CSS Grid с auto-fit/auto-fill
- **Card Spacing**: gap: 24px
- **Responsive**:
  - Desktop: 3-4 columns
  - Tablet: 2 columns
  - Mobile: 1 column

#### Sidebar + Content

- **Sidebar Width**: 256px (desktop), collapsible на mobile
- **Content Area**: flex-grow: 1, padding: 24px
- **Gap**: 0 (sidebar fixed)
- **Responsive**: Sidebar становится overlay drawer на < 1024px

---

### Form Patterns

#### Single Column Form

- **Max Width**: 480px
- **Field Spacing**: 20px between fields
- **Button Group**: Margin-top: 32px, Gap: 12px между кнопками
- **Layout**: Centered или left-aligned в контейнере

#### Multi Column Form

- **Grid**: 2 columns (desktop), 1 column (mobile)
- **Full Width Fields**: Span both columns (textarea, section headers)
- **Responsive**: Breakpoint: 768px

#### Wizard / Stepper Form

- **Steps Indicator**:
  - Height: 48px
  - Background: color-bg-secondary
  - Border-bottom: 1px solid color-border-primary
- **Content Area**: Padding: 32px
- **Navigation**: Bottom-right, Gap: 12px between buttons
- **Progress**: Progress bar или numbered steps

---

### Data Visualization

#### Dashboard Card with Chart

- **Header**:
  - Title: font-size-lg, font-weight-semibold
  - Subtitle: font-size-sm, color-text-secondary
  - Actions: Positioned absolute top-right
- **Chart Area**: Padding: 16px, Min-height: 300px
- **Footer**: Border-top: 1px solid color-border-primary, Padding-top: 16px

#### Table with Filters

- **Filter Bar**:
  - Height: auto (min 56px)
  - Background: color-bg-secondary
  - Padding: 12px 16px
  - Border Bottom: 1px solid color-border-primary
- **Table**: Scrollable на overflow
- **Pagination**: Height: 48px, Justify: space-between, Padding: 12px 16px

---

## Состояния

### Interactive States

#### Default
- Базовое состояние элемента без взаимодействия
- Использует основные цвета из палитры

#### Hover
- Изменение цвета/тени при наведении
- Transition: 150-200ms ease
- Cursor: pointer для кликабельных элементов

#### Active/Focus
- Focus ring для keyboard navigation (accessibility)
- Active state при клике
- Higher contrast для лучшей видимости

#### Disabled
- Opacity: 0.6
- Cursor: not-allowed
- Pointer-events: none
- Reduced contrast

#### Loading
- Spinner или skeleton loader
- Disable interactions
- Optional overlay с opacity

#### Error
- Border: color-error
- Background: color-error-bg (опционально)
- Error message ниже элемента

#### Success
- Border: color-success
- Background: color-success-bg (опционально)
- Success icon или message

---

## Иконки

### Icon System

- **Library**: Heroicons, Lucide Icons или Phosphor Icons (рекомендация)
- **Sizes**:
  - XS: 12px
  - SM: 16px
  - Base: 20px
  - MD: 24px
  - LG: 32px
  - XL: 48px
- **Stroke Width**: 1.5px (regular), 2px (medium), 2.5px (bold)
- **Style**: Outline (default), Solid (emphasis)
- **Color**: Inherit from parent или explicit (color-text-primary, color-text-secondary)

### Common Icons

| Название | Использование | Размер по умолчанию |
|----------|---------------|---------------------|
| Search | Поиск, search inputs | 20px |
| Close / X | Закрытие модалов, dismissing alerts | 20px |
| Chevron Down | Dropdowns, accordions, expandables | 16px |
| Arrow Right | Navigation, "next", CTAs | 20px |
| Check | Confirmations, success states, checkboxes | 20px |
| Alert Circle | Warnings, info messages | 20px |
| X Circle | Errors, failed states | 20px |
| Menu / Hamburger | Mobile navigation toggle | 24px |
| User | User profiles, accounts | 20px |
| Settings | Settings pages, configuration | 20px |
| Plus | Add new items, create actions | 20px |
| Trash | Delete actions | 20px |
| Edit / Pencil | Edit actions, forms | 20px |

---

## Flutter Компоненты (Из реального кода)

### 17. Loading Circle

Компонент индикатора загрузки, извлеченный из Flutter приложения.

#### Характеристики:

- **Container Size**: Width: 719px, Height: 550px
- **Background**: color-bg-primary (#FFFFFF)
- **Border Radius**: radius-5xl (100px)
- **Clip Behavior**: antiAlias

#### Заголовок

- **Text**: "Loading Circle"
- **Font**: Archivo
- **Font Size**: 72px (font-size-6xl)
- **Font Weight**: 800 (extrabold)
- **Color**: #09101D (color-text-primary)
- **Line Height**: 0.70 (line-height-super-tight)
- **Position**: Left: 100px, Top: 100px
- **Spacing**: 10px между элементами

#### Контейнеры состояний

**Контейнер 1 (Default State):**
- **Position**: Left: 100px, Top: 200px
- **Padding**: 20px (space-5)
- **Border**: 1px solid #7B61FF (color-primary)
- **Border Radius**: 15px (radius-3xl)
- **Spacing между элементами**: 100px

**Контейнер 2 (Active State):**
- **Position**: Left: 100px, Top: 386px
- **Padding**: 20px (space-5)
- **Background**: #09101D (color-text-primary)
- **Border**: 1px solid #7B61FF (color-primary)
- **Border Radius**: 15px (radius-3xl)
- **Spacing между элементами**: 100px

---

### 18. Logos Section

Секция отображения логотипов и текстовых элементов.

#### Характеристики:

- **Padding**: 100px (space-25)
- **Background**: color-bg-primary (#FFFFFF)
- **Border Radius**: radius-5xl (100px)
- **Clip Behavior**: antiAlias

#### Заголовок

- **Text**: "Logos"
- **Font**: Archivo
- **Font Size**: 72px (font-size-6xl)
- **Font Weight**: 800 (extrabold)
- **Color**: #09101D (color-text-primary)
- **Line Height**: 0.70 (line-height-super-tight)
- **Spacing**: 50px до следующего элемента

#### Контейнер логотипов

- **Padding**: 100px (space-25)
- **Background**: #EAEEF2 (color-bg-secondary)
- **Border**: 1px solid #7B61FF (color-primary)
- **Border Radius**: 15px (radius-3xl)
- **Spacing между элементами**: 50px

#### Текстовый элемент "Mountains"

**Вариант 1 (Dark Background):**
- **Text**: "Mountains"
- **Font**: Archivo
- **Font Size**: 16px (font-size-base)
- **Font Weight**: 700 (bold)
- **Color**: #09101D (color-text-primary)
- **Line Height**: 1.40 (line-height-comfortable)
- **Padding**: Horizontal: 16px, Vertical: 10px
- **Border Radius**: 8px (radius-lg)

**Вариант 2 (Light Text):**
- **Text**: "Mountains"
- **Font**: Archivo
- **Font Size**: 16px (font-size-base)
- **Font Weight**: 700 (bold)
- **Color**: #FFFFFF (color-text-inverse)
- **Line Height**: 1.40 (line-height-comfortable)
- **Padding**: Horizontal: 16px, Vertical: 10px

---

### 19. Title Section

Простая секция заголовка.

#### Характеристики:

- **Padding**: 100px (space-25)
- **Background**: color-bg-primary (#FFFFFF)
- **Border Radius**: radius-4xl (80px)
- **Clip Behavior**: antiAlias
- **Spacing**: 10px между элементами

#### Заголовок

- **Text**: "Title"
- **Font**: Archivo
- **Font Size**: 72px (font-size-6xl)
- **Font Weight**: 800 (extrabold)
- **Color**: #09101D (color-text-primary)
- **Line Height**: 0.70 (line-height-super-tight)

---

### 20. App Theme (Dark Mode)

Тема приложения, извлеченная из MaterialApp.

#### Характеристики:

- **Base Theme**: ThemeData.dark()
- **Scaffold Background**: #12202F (color-bg-dark) - RGB(18, 32, 47)

#### Использование

```dart
theme: ThemeData.dark().copyWith(
  scaffoldBackgroundColor: const Color.fromARGB(255, 18, 32, 47),
)
```

---

### 21. TabBar (Bottom Navigation)

Компонент TabBar для нижней навигации, извлеченный из Flutter приложения.

#### Характеристики контейнера:

- **Container Width**: 375px (mobile), 950px (desktop showcase)
- **Container Height**: 88px, 90px
- **Background**: color-bg-primary (#FFFFFF)
- **Shadow**: BoxShadow(color: #F0F1F2, offset: (0, -1)) - subtle top border

#### Tab структура:

**Tab Item:**
- **Height**: 54px, 56px
- **Padding**: Horizontal: 4px, Vertical: 2px (top: 4px, bottom: 2px)
- **Border Radius**: 12px (radius-xl)
- **Icon Container**: 40px × 40px, 50px × 50px
- **Icon Size**: 20px, 24px
- **Icon Padding**: 2px (radius-full container)

**Label:**
- **Text**: "Label"
- **Font**: Archivo
- **Font Size**: 12px (font-size-xs)
- **Font Weight**: 400 (normal)
- **Line Height**: 1.40 (line-height-comfortable)
- **Color Active**: #09101D (color-text-primary)
- **Color Inactive**: #747B84 (color-text-secondary)

#### Badge компонент:

**Text Badge (Notification Count):**
- **Height**: 20px
- **Padding**: Horizontal: 4px, Vertical: 2px
- **Background**: #4141E6 (color-accent)
- **Border Radius**: 20px (radius-badge)
- **Position**: Top-right of icon
- **Text**:
  - Font: Archivo
  - Size: 10px (font-size-2xs)
  - Weight: 600 (semibold)
  - Color: white (color-text-inverse)
  - Line Height: 1.40

**Dot Badge (Indicator):**
- **Size**: 5px × 5px
- **Background**: #4141E6 (color-accent)
- **Border Radius**: 20px (radius-badge)
- **Position**: Bottom-right or top-right of icon

#### Indicator (Active Tab):

- **Width**: 134px
- **Height**: 5px
- **Border Radius**: 100px (radius-full)
- **Background**: #09101D (color-text-primary)
- **Position**: Bottom, centered

#### Варианты TabBar:

**3 Tab Layout:**
- Tab width: 125px (375px / 3)
- Equal spacing

**4 Tab Layout:**
- Tab width: ~93px (375px / 4)
- Equal spacing

**5 Tab Layout:**
- Tab width: 75px (375px / 5)
- Equal spacing

#### Состояния:

- **Active**: Label color #09101D, indicator visible
- **Inactive**: Label color #747B84, no indicator
- **With Badge**: Badge positioned top-right (20px height with count) or bottom-right (5px dot)

---

### 22. Header / Section Title

Компонент заголовков секций, извлеченный из TabBar кода.

#### Характеристики:

**Title Only:**
- **Padding**: 10px (top), 16px (horizontal), 10px (vertical)
- **Background**: color-bg-primary (#FFFFFF)
- **Title**:
  - Font: Archivo
  - Size Large: 24px (font-size-xl)
  - Size Small: 16px (font-size-base)
  - Weight: 700 (bold)
  - Color: #09101D (color-text-primary)
  - Line Height: 1.40

**Title with Underline:**
- **Underline Bar**:
  - Width: 40px
  - Height: 2px
  - Color: #4141E6 (color-accent)
  - Border Radius: 1px (radius-2xs)
  - Spacing from title: 5px

**Title with Subtitle:**
- **Subtitle**:
  - Font: Archivo
  - Size Large: 14px (font-size-sm)
  - Size Small: 13px (font-size-xs-plus)
  - Weight: 400 (normal)
  - Color: #09101D (color-text-primary)
  - Line Height: 1.40
  - Spacing from title: 5px

**Title with Action Link:**
- **Action Text**:
  - Font: Archivo
  - Size Large: 14px (font-size-sm)
  - Size Small: 13px (font-size-xs-plus)
  - Weight: 600 (semibold)
  - Color: #4141E6 (color-accent)
  - Line Height: 1.40
  - Alignment: Right
  - Text: "Action"

#### Варианты:

1. **Simple Title**: Только заголовок
2. **Title + Underline**: Заголовок с подчеркиванием
3. **Title + Subtitle**: Заголовок с подзаголовком
4. **Title + Action**: Заголовок с кнопкой действия справа
5. **Title + Underline + Subtitle**: Полный вариант с подчеркиванием и подзаголовком
6. **Title + Action + Subtitle**: Заголовок с действием и подзаголовком

---

## Как использовать эту дизайн-систему

### Для дизайнеров

1. **Начните с основ**: Используйте определенные цвета, типографику и spacing из системы
2. **Используйте компоненты**: Применяйте готовые компоненты вместо создания новых с нуля
3. **Следуйте паттернам**: Применяйте проверенные layout patterns для консистентности
4. **Документируйте отклонения**: Если создаете новый компонент, задокументируйте его

### Для разработчиков

1. **Используйте CSS переменные**: Импортируйте `styles/variables.css` в свой проект
2. **Применяйте utility classes**: Используйте готовые классы для spacing, colors, typography
3. **Переиспользуйте компоненты**: Импортируйте компоненты из библиотеки вместо создания новых
4. **Accessibility first**: Все компоненты должны быть доступны (ARIA, keyboard navigation)

### Для продуктовой команды

1. **Референс для требований**: Ссылайтесь на компоненты дизайн-системы в спецификациях
2. **Ускорение разработки**: Используйте готовые паттерны для быстрого прототипирования
3. **Консистентность продукта**: Обеспечьте единый UX across всех фич
4. **Предлагайте улучшения**: Система живет и эволюционирует с обратной связью

---

## Версионирование и обновления

**Текущая версия**: v5.2.0

### Changelog

#### v5.2.0 (2025-11-19)
- Добавлены данные из TabBar компонента Flutter
- Обновлен вторичный цвет текста (#747B84)
- Добавлен accent цвет (#4141E6) для badges и действий
- Добавлен quaternary background (#F4F6F9)
- Добавлены новые font sizes: 10px (badge text), 13px (action text)
- Добавлены новые spacing: 1px, 2px, 5px, 34px, 40px
- Добавлены новые border radius: 1px, 12px, 20px (badge)
- Добавлена shadow для TabBar: 0 -1px 0 0 #F0F1F2
- Добавлены новые gray shades: 150, 175, 450
- Добавлен компонент TabBar (Bottom Navigation) с вариантами на 3-5 табов
- Добавлен компонент Header/Section Title с 6 вариантами
- Добавлена спецификация Badge компонента (text и dot варианты)

#### v5.1.0 (2025-11-19)
- Добавлены данные из реального Flutter приложения
- Обновлен основной цвет бренда (#7B61FF)
- Добавлен шрифт Archivo как основной
- Добавлены новые размеры spacing (6px, 10px, 50px, 100px)
- Добавлены новые border radius (15px, 80px, 100px)
- Добавлены Flutter компоненты: Loading Circle, Logos Section, Title Section
- Добавлен темный фон (#12202F)
- Обновлены line heights (0.70, 1.40)
- Добавлен Display heading (72px, weight 800)

#### v5.0.0 (2025-11-19)
- Первая версия дизайн-системы
- Полная цветовая палитра
- Базовые компоненты
- Layout patterns
- Иконочная система

---

## Поддержка и контакты

- **Документация**: `/docs`
- **Компоненты**: `/components`
- **Примеры**: `/examples`
- **Вопросы**: Создайте issue в репозитории

---

**© 2025 Design System v5. Все права защищены.**
