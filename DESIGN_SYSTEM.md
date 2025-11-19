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

/* Success (Form Validation) - из SmallLeadingSelector кода */
--color-success-positive: #11BB8D;
--color-success-positive-bg: rgba(17, 187, 141, 0.05);

/* Error / Trend Down */
--color-error: #EF4444;
--color-error-bg: #FEE2E2;
--color-error-border: #FCA5A5;

/* Error (Form Validation) - из SmallLeadingSelector кода */
--color-error-negative: #DA1414;
--color-error-negative-bg: rgba(218, 20, 20, 0.05);

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

/* Price/Value Display - из ContentTextTopHelperNoBottomHelperNoStateDisabled кода */
--color-price-primary: #0B24FB;
--color-price-secondary: #4141E6;

/* Sale/Discount - из InformationCardSlider кода */
--color-sale: #F7B68A;
--color-sale-hover: #F6A678;
--color-sale-active: #F59668;

/* Danger/Alert - из InformationCardSlider кода */
--color-danger: #E24949;
--color-danger-hover: #D93939;
--color-danger-active: #C92929;
```

### Neutral Colors

```css
/* Text - из Flutter кода */
--color-text-primary: #09101D;
--color-text-secondary: #747B84;  /* Обновлено из TabBar кода */
--color-text-dark: #23262B;  /* Из InformationCardSlider - для badge */
--color-text-muted: #414249;  /* Из InformationCardSlider - для secondary info */
--color-text-subtitle: #373940;  /* Из InformationCardSlider - для subtitle */
--color-text-tertiary: #9CA3AF;
--color-text-disabled: #D9DDE2;  /* Обновлено из InformationCardSlider */
--color-text-inverse: #FFFFFF;

/* Backgrounds - из Flutter кода */
--color-bg-primary: #FFFFFF;
--color-bg-secondary: #EAEEF2;
--color-bg-tertiary: #F3F4F6;
--color-bg-quaternary: #F4F6F9;  /* Из TabBar кода */
--color-bg-light: #FAFAFB;  /* Из Message кода - showcase background */
--color-bg-pressed: #EAEFF2;  /* Из SmallLeadingSelector кода - pressed state */
--color-bg-elevated: #FFFFFF;
--color-bg-overlay: rgba(0, 0, 0, 0.5);
--color-bg-dark: #12202F;
--color-bg-message-outgoing: #303239;  /* Из Message кода - outgoing message bubble */

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
--color-gray-250: #D9DDE2;  /* Из InformationCardSlider - disabled/placeholder */
--color-gray-300: #D1D5DB;
--color-gray-400: #9CA3AF;
--color-gray-450: #747B84;  /* Из TabBar кода - вторичный текст */
--color-gray-500: #6B7280;
--color-gray-550: #414249;  /* Из InformationCardSlider - muted text */
--color-gray-575: #373940;  /* Из InformationCardSlider - subtitle */
--color-gray-600: #4B5563;
--color-gray-650: #23262B;  /* Из InformationCardSlider - dark text */
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
--gradient-instagram: linear-gradient(90deg, #833AB4 0%, #FD1D1D 50%, #FCB045 100%); /* Из Basic кода - Live badge */
```

### Brand Icon Colors

```css
/* Цвета для иконок брендов и социальных сетей */
--color-brand-facebook: #1877F2;
--color-brand-twitter: #1DA1F2;
--color-brand-instagram: #E4405F;
--color-brand-instagram-gradient: #833AB4;  /* Из StoriesTextOutside - Instagram purple gradient */
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
--font-size-2xs-plus: 0.6875rem; /* 11px - из InformationCardSlider кода */
--font-size-xs: 0.75rem;      /* 12px */
--font-size-xs-plus: 0.8125rem; /* 13px - из TabBar кода (action text) */
--font-size-sm: 0.875rem;     /* 14px */
--font-size-sm-plus: 0.9375rem; /* 15px - из InformationCardSlider кода */
--font-size-base: 1rem;       /* 16px - из Flutter кода */
--font-size-md: 1.125rem;     /* 18px */
--font-size-lg: 1.25rem;      /* 20px */
--font-size-xl: 1.5rem;       /* 24px */
--font-size-2xl: 1.875rem;    /* 30px */
--font-size-2xl-plus: 2rem;   /* 32px - из Basic кода (profile title) */
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
--radius-base-plus: 0.3125rem; /* 5px - из InformationCardSlider кода */
--radius-md: 0.375rem;    /* 6px */
--radius-lg: 0.5rem;      /* 8px - из Flutter кода */
--radius-lg-plus: 0.625rem; /* 10px - из InformationCardSlider кода */
--radius-reaction: 0.6875rem; /* 11px - из Message кода (reaction badges) */
--radius-xl: 0.75rem;     /* 12px - из TabBar кода */
--radius-xl-plus: 0.8125rem; /* 13px - из StoriesTextOutside кода (active story border) */
--radius-2xl: 1rem;       /* 16px */
--radius-3xl: 0.9375rem;  /* 15px - из Flutter кода */
--radius-badge: 1.25rem;  /* 20px - из TabBar кода (badge radius) */
--radius-avatar: 2.5rem;  /* 40px - из InformationCardSlider кода (avatar) */
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

#### Badge Shadow

```css
/* Из Basic кода - subtle badge shadow */
--shadow-badge: 0 1px 1px 0 rgba(0, 0, 0, 0.4);
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

### 23. Information Cards (Slider Component)

Компонент слайдера информационных карточек, извлеченный из Flutter приложения InformationCardSlider.

#### Характеристики Image Slider:

- **Image Size**: Width: 327px, Height: 200px
- **Border Radius**: 20px (radius-badge)
- **Scroll Direction**: Horizontal
- **Spacing**: Between cards in carousel

#### Badge Component:

**Badge Container:**
- **Padding**: Horizontal: 6px, Vertical: 3px
- **Border Radius**: 5px (radius-base-plus)
- **Font**: Archivo
- **Font Size**: 11px (font-size-2xs-plus)
- **Font Weight**: 600 (semibold)
- **Line Height**: 1.40

**Badge Variants:**

1. **Covid-free Badge**:
   - Background: white (color-bg-primary)
   - Text Color: #23262B (color-text-dark)
   - Text: "Covid-free"

2. **New Place Badge**:
   - Background: white (color-bg-primary)
   - Text Color: #23262B (color-text-dark)
   - Text: "New place"

3. **Beginner Level Badge**:
   - Background: white (color-bg-primary)
   - Text Color: #23262B (color-text-dark)
   - Text: "Beginner level"

4. **Sale Badge**:
   - Background: #F7B68A (color-sale)
   - Text Color: white (color-text-inverse)
   - Text: "25%"

5. **Category Badge**:
   - Background: white (color-bg-primary)
   - Text Color: #23262B (color-text-dark)
   - Examples: "Hotels", "Restaurants", "Entertainment"

#### Avatar Component:

**Avatar Container:**
- **Size**: 40px × 40px
- **Border Radius**: 10px (radius-lg-plus)
- **Padding**: 4px (creates inner spacing)

**Avatar Image:**
- **Size**: 32px × 32px (внутри 40px контейнера)
- **Border Radius**: Inherited from container

#### Card Variants:

**1. Hotel Card:**
- **Image**: 327px × 200px with 20px border radius
- **Badge**: "Covid-free" (white bg)
- **Title**:
  - Font: Archivo
  - Size: 15px (font-size-sm-plus)
  - Weight: 600 (semibold)
  - Color: #09101D (color-text-primary)
  - Line Height: 1.40
- **Subtitle**:
  - Font: Archivo
  - Size: 13px (font-size-xs-plus)
  - Weight: 400 (normal)
  - Color: #373940 (color-text-subtitle)
  - Line Height: 1.40
- **Rating**: Stars + count text
- **Price**: Primary color emphasis

**2. Experience Card:**
- **Image**: 327px × 200px with 20px border radius
- **Badge**: "New place" (white bg)
- **Title**: Same as Hotel Card
- **Subtitle**: Same as Hotel Card
- **Category Badge**: "Entertainment"
- **Additional Info**: Duration, level, etc.

**3. Restaurant Card:**
- **Image**: 327px × 200px with 20px border radius
- **Badge**: Category badge (white bg)
- **Title**: Same as Hotel Card
- **Subtitle**: Same as Hotel Card
- **Secondary Info**:
  - Font: Archivo
  - Size: 11px (font-size-2xs-plus)
  - Weight: 400 (normal)
  - Color: #414249 (color-text-muted)
  - Line Height: 1.40

**4. Video Card:**
- **Image**: 327px × 200px with 20px border radius
- **Badge**: "25%" sale badge (#F7B68A bg)
- **Title**: Same as Hotel Card
- **Avatar**: 40px container with 32px image (10px radius)
- **Video Duration**: Overlay on image
- **Like/Save Icons**: Top-right corner

#### Card Layout Structure:

```
┌─────────────────────────────────┐
│                                 │
│   Image (327×200, radius 20)    │
│   ┌──────────┐                  │
│   │ Badge    │                  │
│   └──────────┘                  │
│                                 │
├─────────────────────────────────┤
│ Title (15px, semibold)          │
│ Subtitle (13px, normal)         │
│ Secondary Info (11px, muted)    │
│                                 │
│ [Avatar] Additional Details     │
└─────────────────────────────────┘
```

#### Spacing:

- **Card Padding**: 10px, 12px, 16px (внутренние отступы)
- **Badge to Image**: 10px from edges
- **Title to Subtitle**: 4px
- **Subtitle to Additional Info**: 6px (space-1-5)
- **Between Cards**: Horizontal scroll spacing

#### States:

- **Default**: Standard appearance
- **Hover**: Subtle scale or shadow effect (interactive)
- **Active**: Pressed state for card selection
- **Disabled**: Reduced opacity (#D9DDE2 for disabled text)

---

### 24. Stories (Text Outside)

Компонент Stories с текстовыми подписями снаружи, извлеченный из Flutter приложения StoriesTextOutside.

#### Характеристики Showcase Container:

- **Width**: 1290px
- **Height**: 322px
- **Padding**: 50px (all sides)
- **Border**: 1px solid #7B61FF (color-primary)
- **Border Radius**: 15px (radius-3xl)
- **Clip Behavior**: antiAlias
- **Content Spacing**: 200px between story variants

#### Variant 1: Vertical Stories (Portrait)

**Container:**
- **Width**: 375px
- **Padding**: Top: 10px, Left: 16px, Bottom: 20px
- **Item Spacing**: 10px horizontal

**Story Item:**
- **Image Size**: Width: 100px, Height: 120px
- **Border Radius**: 10px (radius-lg-plus)
- **Aspect Ratio**: 5:6 (portrait)
- **Spacing from Label**: 10px

**Active Story Border:**
- **Container Size**: 100px × 120px
- **Border**: 2px solid #833AB4 (color-brand-instagram-gradient)
- **Border Radius**: 13px (radius-xl-plus)
- **Inner Image**: 94px × 114px (accounts for 2px border + 3px padding)
- **Inner Border Radius**: 10px (radius-lg-plus)

**Story Label:**
- **Container Width**: 100px
- **Text Width**: 90px (with 10px left padding)
- **Font**: Archivo
- **Font Size**: 13px (font-size-xs-plus)
- **Font Weight**: 700 (bold)
- **Color**: #09101D (color-text-primary)
- **Line Height**: 1.40
- **Spacing from Image**: 3px internal
- **Text**: "Category or service"

#### Variant 2: Horizontal Stories (Landscape)

**Container:**
- **Width**: 375px
- **Padding**: Top: 10px, Left: 16px, Bottom: 20px
- **Item Spacing**: 10px horizontal

**Story Item:**
- **Image Size**: Width: 130px, Height: 80px
- **Border Radius**: 10px (radius-lg-plus)
- **Aspect Ratio**: 13:8 (landscape)
- **Spacing from Label**: 10px

**Active Story Border:**
- **Container Size**: 130px × 80px
- **Border**: 2px solid #833AB4 (color-brand-instagram-gradient)
- **Border Radius**: 13px (radius-xl-plus)
- **Inner Image**: 124px × 74px (accounts for 2px border + 3px padding)
- **Inner Border Radius**: 10px (radius-lg-plus)

**Story Label:**
- **Container Width**: 130px
- **Text Width**: 110px (with 10px left padding)
- **Font**: Archivo
- **Font Size**: 13px (font-size-xs-plus)
- **Font Weight**: 700 (bold)
- **Color**: #09101D (color-text-primary)
- **Line Height**: 1.40
- **Spacing from Image**: 3px internal
- **Text**: "Category or service"

#### Layout Structure:

**Vertical (Portrait) Layout:**
```
┌──────────────────────────────────────┐
│ [100×120] [100×120] [100×120] [100×120]
│   Label     Label     Label     Label │
└──────────────────────────────────────┘
Spacing: 10px between items
```

**Horizontal (Landscape) Layout:**
```
┌──────────────────────────────────────┐
│ [130×80] [130×80] [130×80] [130×80] │
│  Label    Label    Label    Label   │
└──────────────────────────────────────┘
Spacing: 10px between items
```

#### States:

**Default (Inactive) Story:**
- Image with radius 10px
- No border
- Label below with 3px spacing

**Active (Viewed/Current) Story:**
- White container with 2px purple border (#833AB4)
- Border radius 13px on container
- Image scaled to fit inside (accounts for border width)
- Purple gradient indicates active/viewed state
- Label below remains same

**Row Configuration:**
- 4 stories per row (both variants)
- Horizontal scroll if more items
- Equal spacing between all items

#### Use Cases:

1. **Categories/Services**: Display categories with visual preview
2. **Instagram-style Stories**: Social media story highlights
3. **Content Preview**: Quick visual navigation to content sections
4. **User Stories**: Personal or brand story collections

#### Best Practices:

- Use portrait (100×120) for vertical content, people, products
- Use landscape (130×80) for wide content, scenes, events
- Active border indicates viewed or current story
- Keep labels concise (2-3 words max)
- Maintain 10px spacing for visual consistency
- Text outside reduces visual clutter on images

---

### 25. User Profile Cards

Компонент User Profile Cards с различными вариантами отображения профиля пользователя, извлеченный из Flutter приложения Basic.

#### Variant 1: Basic Profile Card

**Container:**
- **Width**: Full width
- **Background**: White (color-bg-primary)
- **Padding**: Right: 10px, Left: 16px, Vertical: 12px
- **Clip Behavior**: antiAlias

**Avatar:**
- **Container Size**: 56px × 56px
- **Image Size**: 48px × 48px
- **Border Radius**: 40px (circular)
- **Background**: #D9DDE2 (color-text-disabled) - placeholder
- **Position**: Offset 4px from container edges

**Badge (Bottom-Right):**
- **Container**: 20px × 20px, border-radius 15px
- **Inner Badge**: 14px × 14px
- **Background**: #4141E6 (color-accent)
- **Border**: 1px solid white
- **Border Radius**: 20px (circular)
- **Icon Container**: 12px × 12px, padding 2px
- **Position**: Left: 0, Top: 36px (bottom of avatar)

**Profile Text:**
- **Title**: "Hi, I'm Jack"
  - Font: Archivo
  - Size: 32px (font-size-2xl-plus)
  - Weight: 700 (bold)
  - Color: #09101D (color-text-primary)
  - Line Height: 1.40
- **Subtitle**: "And I've joined in 2021. Feel free to ask me any questions ✌🏻"
  - Font: Archivo
  - Size: 14px (font-size-sm)
  - Weight: 400 (normal)
  - Color: #414249 (color-text-muted)
  - Line Height: 1.40

#### Variant 2: Avatar Group / Row

**Container:**
- **Width**: Full width
- **Padding**: Horizontal: 16px, Vertical: 10px
- **Clip Behavior**: antiAlias

**Avatar Row Configuration:**
- **Spacing**: 5px vertical between avatars
- **Layout**: Horizontal row
- **Items**: 5 avatars displayed

**Avatar Types:**

**Empty Avatar (Placeholder):**
- **Size**: 48px × 48px
- **Border**: 1.2px solid #D9DDE2 (color-text-disabled)
- **Border Radius**: 40px (circular)
- **Position**: Offset 4px from 56px container

**Avatar with Image:**
- **Container**: 56px × 56px
- **Image**: 48px × 48px
- **Border Radius**: 40px (circular)
- **Background**: #D9DDE2 placeholder

**Avatar with Badge (Top-Right):**
- **Avatar**: 48px × 48px, radius 40px
- **Badge Container**: 20px × 20px
- **Badge**: 20px × 20px (outer), 14px inner with icon
- **Badge Background**: #23262B (color-text-dark)
- **Badge Border**: 1px solid white
- **Badge Border Radius**: 20px (circular)
- **Shadow**: 0 1px 1px 0 rgba(0, 0, 0, 0.4) (shadow-badge)
- **Position**: Left: 36px, Top: 0 (top-right corner)

#### Variant 3: Profile Card with Live Badge and Toggle

**Container:**
- **Background**: None (transparent)
- **Layout**: Full width row

**Avatar with Live Badge:**
- **Avatar**: 56px × 56px container, 48px × 48px image
- **Border Radius**: 40px (circular)
- **Position**: Offset 4px

**Live Badge:**
- **Size**: 28px × 14px
- **Padding**: Horizontal: 4px, Vertical: 2px
- **Background**: Instagram gradient (gradient-instagram)
  - Colors: #833AB4 → #FD1D1D → #FCB045
  - Direction: Horizontal (90deg)
- **Border**: 1px solid white
- **Border Radius**: 12px (radius-xl)
- **Text**: "Live"
  - Font: Archivo
  - Size: 10px (font-size-2xs)
  - Weight: 600 (semibold)
  - Color: White (color-text-inverse)
  - Line Height: 1.40
- **Position**: Left: 0, Top: 36px (bottom of avatar)

**Profile Text:**
- **Username**: "@mikkey"
  - Font: Archivo
  - Size: 16px (font-size-base)
  - Weight: 700 (bold)
  - Color: #09101D (color-text-primary)
  - Line Height: 1.40
- **Description**: "100+ Playlists on Napster"
  - Font: Archivo
  - Size: 12px (font-size-xs)
  - "100+": Weight 700 (bold), Color #414249
  - " Playlists on Napster": Weight 400 (normal), Color #414249
  - Line Height: 1.40

**Toggle Switch:**
- **Container**: 52px × 31px
- **Background**: #4141E6 (color-accent)
- **Border Radius**: 40px (circular)
- **Knob**: 31px × 31px
- **Knob Background**: White
- **Knob Border**: 2px solid #4141E6
- **Knob Border Radius**: 40px (circular)
- **Position**: Aligned right (end of row)
- **State**: Active/On (knob on the right)

#### Layout Structure:

**Profile Card Layout:**
```
┌─────────────────────────────────────────┐
│ [Avatar]  Title (32px bold)             │
│  +Badge   Subtitle (14px normal)        │
└─────────────────────────────────────────┘
Padding: 16px left, 10px right, 12px vertical
```

**Avatar Group Layout:**
```
┌─────────────────────────────────────────┐
│ [A] [A] [A] [A] [A]                     │
│      +Badge variations                  │
└─────────────────────────────────────────┘
Padding: 16px horizontal, 10px vertical
Spacing: 5px between avatars
```

**Profile with Live & Toggle:**
```
┌─────────────────────────────────────────┐
│ [Avatar]  @username          [Toggle]   │
│  +Live    Description text              │
└─────────────────────────────────────────┘
```

#### Badge Positions:

- **Bottom-Right**: Left: 0-36px from avatar left, Top: 36px from avatar top
- **Top-Right**: Left: 36px from avatar left, Top: 0 from avatar top

#### Use Cases:

1. **User Profiles**: Display user information with avatar and bio
2. **Live Streaming**: Indicate live status with gradient badge
3. **Avatar Groups**: Show multiple users in a compact row
4. **Settings Toggle**: Profile cards with interactive controls
5. **Social Features**: Online status, notifications badges

#### Best Practices:

- Use 56×56px container for avatars (48×48px actual image with 4px offset)
- Badge sizes: 14px for small indicators, 20px for icon badges
- Keep profile titles under 50 characters for readability
- Use Instagram gradient for Live badges to indicate real-time activity
- Toggle switches should be 52×31px for optimal touch targets
- Avatar placeholder background: #D9DDE2 (disabled color)
- Maintain 1px white border on badges for visibility on all backgrounds

---

### 26. Chat Messages

Компонент Chat Messages для отображения сообщений в чате, извлеченный из Flutter приложения Message.

#### Характеристики Showcase Container:

- **Width**: 929px
- **Height**: 970px
- **Padding**: 50px (all sides)
- **Background**: #FAFAFB (color-bg-light)
- **Border**: 1px solid #7B61FF (color-primary)
- **Border Radius**: 15px (radius-3xl)
- **Clip Behavior**: antiAlias
- **Message Spacing**: 98px between messages

#### Variant 1: Incoming Message with Header (Large Avatar)

**Container:**
- **Width**: 375px
- **Padding**: Horizontal: 16px

**Avatar:**
- **Container Size**: 40px × 40px
- **Image Size**: 32px × 32px
- **Border Radius**: 40px (circular)
- **Background**: #D9DDE2 (color-text-disabled) - placeholder
- **Position**: Offset 4px from container edges
- **Spacing**: 6px от аватара до содержимого

**Message Header:**
- **Container Width**: 147px (auto)
- **Name**: "Helena"
  - Font: Archivo
  - Size: 14px (font-size-sm)
  - Weight: 600 (semibold)
  - Color: #4141E6 (color-accent)
  - Line Height: 1.40
- **Timestamp**: "14:40 PM"
  - Font: Archivo
  - Size: 10px (font-size-2xs)
  - Weight: 400 (normal)
  - Color: #747B84 (color-text-secondary)
  - Line Height: 1.40
  - Padding bottom: 1px
- **Spacing**: 5px между именем и временем

**Message Content:**
- **Text**: "Hi I want to book some desk, is it possible?"
  - Font: Archivo
  - Size: 14px (font-size-sm)
  - Weight: 400 (normal)
  - Color: #09101D (color-text-primary)
  - Line Height: 1.40
  - Max Width: 293px

**Reaction Section:**
- **Padding**: Vertical: 5px
- **Spacing**: 10px between reactions

**Reaction Badge:**
- **Height**: 24px
- **Padding**: Horizontal: 6px
- **Background**: #F4F6F9 (color-bg-quaternary)
- **Border Radius**: 11px (radius-reaction)
- **Text**: "🌱 1"
  - Font: Archivo
  - Size: 11px (font-size-2xs-plus)
  - Weight: 600 (semibold)
  - Color: #414249 (color-text-muted)
  - Line Height: 1.40

**Reaction Icon Button:**
- **Size**: 24px × 24px
- **Padding**: 6px
- **Background**: #F4F6F9 (color-bg-quaternary)
- **Border Radius**: 11px (radius-reaction)
- **Icon Size**: 12px × 12px (after 6px padding)

#### Variant 2: Incoming Message Bubble (Small Avatar)

**Container:**
- **Width**: 375px
- **Padding**: Left: 16px

**Avatar:**
- **Container Size**: 32px × 32px
- **Image Size**: 24px × 24px
- **Border Radius**: 40px (circular)
- **Position**: Offset 4px
- **Spacing**: 4px от аватара до bubble

**Message Bubble:**
- **Width**: 248px
- **Padding**: 10px (all sides)
- **Background**: #F4F6F9 (color-bg-quaternary)
- **Border Radius**: 15px (radius-3xl)
- **Spacing**: 5px внутренний

**Message Text:**
- **Text**: "Hi I want to book some desk, is it possible?"
  - Font: Archivo
  - Size: 16px (font-size-base)
  - Weight: 400 (normal)
  - Color: #09101D (color-text-primary)
  - Line Height: 1.40
  - Max Width: 228px (with 10px padding)

**Timestamp:**
- **Icon Container**: 16px × 16px, padding 2px
- **Text**: "3:00PM"
  - Font: Archivo
  - Size: 11px (font-size-2xs-plus)
  - Weight: 400 (normal)
  - Color: #747B84 (color-text-secondary)
  - Alignment: Right
  - Spacing: 3px от иконки

#### Variant 3: Incoming Message Bubble (No Avatar)

**Message Bubble:**
- **Width**: 248px
- **Padding**: 10px
- **Background**: #F4F6F9 (color-bg-quaternary)
- **Border Radius**: 15px (radius-3xl)
- **Positioned**: Left aligned (16px from container edge)
- Same text and timestamp styling as Variant 2

#### Variant 4: Outgoing Message (With Avatar)

**Container:**
- **Width**: 375px
- **Padding**: Right: 16px
- **Alignment**: Right (end)

**Avatar:**
- **Container Size**: 32px × 32px
- **Image Size**: 24px × 24px
- **Border Radius**: 40px (circular)
- **Position**: Offset 4px, right side
- **Spacing**: 5px от bubble

**Message Bubble:**
- **Width**: 260px
- **Padding**: Horizontal: 16px, Vertical: 10px
- **Background**: #303239 (color-bg-message-outgoing)
- **Border Radius**: 15px (radius-3xl)
- **Alignment**: Right
- **Spacing**: 5px внутренний

**Message Text:**
- **Text**: "Yes of course, we have a huge amount of desks and offices"
  - Font: Archivo
  - Size: 16px (font-size-base)
  - Weight: 400 (normal)
  - Color: white (color-text-inverse)
  - Line Height: 1.40
  - Max Width: 228px

**Timestamp:**
- **Text**: "3:00PM"
  - Font: Archivo
  - Size: 11px (font-size-2xs-plus)
  - Weight: 400 (normal)
  - Color: white (color-text-inverse)
  - Alignment: Right
  - Spacing: 3px

#### Variant 5: Outgoing Message (No Avatar)

**Message Bubble:**
- **Width**: 260px
- **Padding**: Horizontal: 16px, Vertical: 10px
- **Background**: #303239 (color-bg-message-outgoing)
- **Border Radius**: 15px (radius-3xl)
- **Alignment**: Right (16px from edge)
- Same text and timestamp styling as Variant 4

#### Layout Structure:

**Incoming Message with Header:**
```
┌──────────────────────────────────────────┐
│ [40px Avatar]  Name          Time        │
│                Message text...           │
│                [🌱 1] [+]                │
└──────────────────────────────────────────┘
Padding: 16px horizontal, 10px from avatar
```

**Incoming Message Bubble:**
```
┌──────────────────────────────────────────┐
│ [32px] ┌────────────────────┐            │
│        │ Message text...    │            │
│        │ [icon] 3:00PM      │            │
│        └────────────────────┘            │
└──────────────────────────────────────────┘
Width: 248px, Padding: 10px, Radius: 15px
```

**Outgoing Message:**
```
┌──────────────────────────────────────────┐
│            ┌────────────────────┐ [32px] │
│            │ Message text...    │        │
│            │          3:00PM    │        │
│            └────────────────────┘        │
└──────────────────────────────────────────┘
Width: 260px, Background: #303239, Aligned right
```

#### Avatar Sizes:

- **Large Avatar (with header)**: 40px × 40px container, 32px × 32px image
- **Small Avatar (in bubble)**: 32px × 32px container, 24px × 24px image
- Both use 4px offset and 40px border radius (circular)

#### Message Bubble Widths:

- **Incoming**: 248px
- **Outgoing**: 260px
- **Max text width**: 228px (accounting for padding)

#### Color Scheme:

**Incoming Messages:**
- Background: #F4F6F9 (color-bg-quaternary) - light gray
- Text: #09101D (color-text-primary) - dark
- Timestamp: #747B84 (color-text-secondary) - gray

**Outgoing Messages:**
- Background: #303239 (color-bg-message-outgoing) - dark gray
- Text: white (color-text-inverse)
- Timestamp: white (color-text-inverse)

**Reactions:**
- Background: #F4F6F9 (color-bg-quaternary)
- Text: #414249 (color-text-muted)
- Border radius: 11px (radius-reaction)

#### Use Cases:

1. **Chat Applications**: One-on-one or group messaging
2. **Support Chat**: Customer service conversations
3. **Comments/Replies**: Threaded discussions
4. **Collaborative Tools**: Team communication
5. **Social Messaging**: Direct messages in social apps

#### Best Practices:

- Use large avatar (40px) with header for first message in sequence
- Use small avatar (32px) for subsequent messages from same user
- Remove avatar for consecutive messages from same user
- Incoming messages aligned left, outgoing aligned right
- Maintain 248px/260px bubble widths for consistency
- Use reactions sparingly, max 2-3 per message
- Include timestamps for context (11px Archivo)
- Light background (#F4F6F9) for received, dark (#303239) for sent
- Message spacing: 98px between different conversations
- Border radius: 15px for bubbles, 11px for reactions
- Avatar placeholder: #D9DDE2 (disabled color)

---

### 27. Form Input with Small Leading Selector

Компонент Form Input с ведущим селектором (dropdown), извлеченный из Flutter приложения SmallLeadingSelector.

#### Характеристики Showcase Container:

- **Width**: 840px
- **Height**: 710px
- **Padding**: 50px (all sides)
- **Border**: 1px solid #7B61FF (color-primary)
- **Border Radius**: 15px (radius-3xl)
- **Clip Behavior**: antiAlias
- **Layout**: Two column grid (2 columns of states)
- **Column Spacing**: Horizontal gap between columns

#### Form Group Container:

- **Width**: 375px
- **Padding**: Horizontal: 16px, Vertical: 5px
- **Spacing**: 8px between form elements
- **Clip Behavior**: antiAlias

#### Label:

- **Text**: "Label"
- **Font**: Archivo
- **Font Size**: 14px (font-size-sm)
- **Font Weight**: 600 (semibold)
- **Color**: #09101D (color-text-primary)
- **Line Height**: 1.40
- **Margin Bottom**: 8px

#### Input Container:

**Base Container:**
- **Height**: 36px
- **Border Radius**: 15px (radius-3xl)
- **Layout**: Horizontal row (leading selector + text input)
- **Spacing**: 0 (no gap between selector and input)

**Leading Selector (Dropdown):**
- **Width**: Auto (fits content)
- **Padding**: Left: 16px, Right: 10px
- **Vertical Padding**: Centered
- **Text**: "Ms."
- **Font**: Archivo
- **Font Size**: 14px (font-size-sm)
- **Font Weight**: 600 (semibold)
- **Color**: #09101D (color-text-primary)
- **Line Height**: 1.40
- **Dropdown Icon**: 20px × 20px chevron down
- **Icon Spacing**: 2px from text

**Text Input Field:**
- **Flex**: Expands to fill remaining space
- **Height**: 36px
- **Padding**: Left: 16px, Right: 20px
- **Font**: Archivo
- **Font Size**: 14px (font-size-sm)
- **Font Weight**: 400 (normal)
- **Color**: #09101D (color-text-primary)
- **Line Height**: 1.40
- **Placeholder Color**: #747B84 (color-text-secondary)

**Action Icons:**
- **Clear Icon**: 20px × 20px
- **Position**: Right edge, 10px from right
- **Padding**: 2px (for touch target)
- **Icon Color**: #747B84 (color-text-secondary)

**Cursor:**
- **Width**: 2px
- **Height**: 16px
- **Color**: #09101D (color-text-primary)
- **Animation**: Blinking

#### Helper Text:

- **Text**: "Helper text"
- **Font**: Archivo
- **Font Size**: 14px (font-size-sm)
- **Font Weight**: 400 (normal)
- **Color**: #747B84 (color-text-secondary)
- **Line Height**: 1.40
- **Margin Top**: 8px

#### State Variants:

**1. Enabled (Default State):**
- **Background**: #F4F6F9 (color-bg-quaternary)
- **Border**: None
- **Text**: Placeholder "Enter text"
- **Selector**: Active, "Ms." visible
- **Helper Text**: Displayed below

**2. Focus:**
- **Background**: White (color-bg-primary)
- **Border**: 2px solid #09101D (color-text-primary)
- **Cursor**: Visible, blinking at text position
- **Text**: Placeholder visible
- **Selector**: Active, "Ms." visible
- **Helper Text**: Displayed below
- **Transition**: Border appears smoothly

**3. Complete (Filled):**
- **Background**: #F4F6F9 (color-bg-quaternary)
- **Border**: None
- **Text**: "Emily" (actual value, 14px Archivo normal)
- **Selector**: Active, "Ms." visible
- **Clear Icon**: 20×20px visible on right
- **Helper Text**: Displayed below

**4. Positive (Success Validation):**
- **Background**: rgba(17, 187, 141, 0.05) (color-success-positive-bg)
- **Border**: 2px solid #11BB8D (color-success-positive)
- **Text**: Placeholder visible
- **Selector**: Active, "Ms." visible
- **Helper Text**: Success message below
- **Helper Text Color**: #11BB8D

**5. Pressed (Active Click):**
- **Background**: #EAEFF2 (color-bg-pressed)
- **Border**: None
- **Text**: Placeholder visible
- **Selector**: Active, "Ms." visible
- **State**: Button press state before focus

**6. Active - Typing:**
- **Background**: White (color-bg-primary)
- **Border**: 2px solid #09101D (color-text-primary)
- **Text**: "Em" (partial input)
- **Cursor**: Visible after "Em"
- **Selector**: Active, "Ms." visible
- **Helper Text**: Displayed below

**7. Incomplete:**
- **Background**: #F4F6F9 (color-bg-quaternary)
- **Border**: None
- **Text**: Empty (no value)
- **Selector**: Active, "Ms." visible
- **Clear Icon**: 20×20px visible (even though empty)
- **Helper Text**: Displayed below

**8. Negative (Error Validation):**
- **Background**: rgba(218, 20, 20, 0.05) (color-error-negative-bg)
- **Border**: 2px solid #DA1414 (color-error-negative)
- **Text**: Placeholder visible
- **Selector**: Active, "Ms." visible
- **Helper Text**: Error message below
- **Helper Text Color**: #DA1414

**9. Disabled:**
- **Background**: #F4F6F9 (color-bg-quaternary)
- **Border**: None
- **Text Color**: #747B84 (color-text-secondary)
- **Selector**: Disabled, text color #747B84
- **Dropdown Icon**: Disabled color #747B84
- **Helper Text**: Disabled color #747B84
- **Cursor**: not-allowed
- **Opacity**: 0.6

#### Layout Structure:

```
┌─────────────────────────────────────────┐
│ Label (14px semibold)                   │
│ ┌───────────────────────────────────┐   │
│ │ Ms. ▾ │ Enter text          [×] │   │
│ └───────────────────────────────────┘   │
│ Helper text (14px normal, secondary)    │
└─────────────────────────────────────────┘

Selector: 16px L padding, 10px R padding
Input: 16px L padding, 20px R padding
Height: 36px, Radius: 15px
```

**Two Column Showcase Layout:**
```
┌───────────────────┬───────────────────┐
│ 1. Enabled        │ 6. Active-Typing  │
│ 2. Focus          │ 7. Incomplete     │
│ 3. Complete       │ 8. Negative       │
│ 4. Positive       │ 9. Disabled       │
│ 5. Pressed        │                   │
└───────────────────┴───────────────────┘
```

#### Spacing:

- **Label to Input**: 8px
- **Input to Helper Text**: 8px
- **Between Form Groups**: 5px vertical padding
- **Selector Text to Icon**: 2px
- **Icon Padding**: 2px for touch target

#### Border Specifications:

- **Default State**: No border
- **Focus/Typing**: 2px solid #09101D
- **Positive**: 2px solid #11BB8D
- **Negative**: 2px solid #DA1414
- **Border Radius**: 15px (all states)

#### Typography:

**Label:**
- Archivo 14px semibold, #09101D

**Selector:**
- Archivo 14px semibold, #09101D (enabled)
- Archivo 14px semibold, #747B84 (disabled)

**Input Text:**
- Archivo 14px normal, #09101D (value)
- Archivo 14px normal, #747B84 (placeholder)

**Helper Text:**
- Archivo 14px normal, #747B84 (default)
- Archivo 14px normal, #11BB8D (success)
- Archivo 14px normal, #DA1414 (error)

#### Use Cases:

1. **User Registration Forms**: Name input with title/prefix selector
2. **Contact Forms**: Phone number with country code selector
3. **E-commerce**: Product quantity with unit selector
4. **Multi-step Forms**: Validation states guide user input
5. **Settings Pages**: Configuration inputs with category selectors
6. **Profile Editing**: Personal info with prefix/suffix options

#### Best Practices:

- Use 36px height for optimal touch targets on mobile
- Maintain 15px border radius for visual consistency
- 2px border width for focus and validation states for clear visual feedback
- Success validation (#11BB8D) for correct input
- Error validation (#DA1414) for invalid input with helpful error message
- Pressed state (#EAEFF2) provides tactile feedback before focus
- Disabled state uses 0.6 opacity with secondary text color
- Clear icon (20×20px) only appears when input has value (except Incomplete state)
- Cursor (2px width) indicates typing position
- Helper text provides context, instructions, or validation feedback
- Selector stays visible and active in all non-disabled states
- Use semibold (600) for selector text to distinguish from input value
- Placeholder uses secondary color (#747B84) for reduced prominence
- Leading selector (dropdown) for related categorization of input
- Keep selector options concise (2-4 characters ideal: "Ms.", "Mr.", "+1")
- Validation backgrounds use subtle 5% opacity for non-intrusive feedback
- Focus state removes default background for cleaner appearance
- Border transitions should be smooth (150-200ms ease)

---

### 28. Text Input Fields (Disabled States with Variants)

Компонент Text Input Fields с различными вариантами отображения disabled состояния, helper text, labels и иконками, извлеченный из Flutter приложения ContentTextTopHelperNoBottomHelperNoStateDisabled.

#### Общие характеристики:

**Container:**
- **Width**: 375px
- **Padding**: Horizontal: 16px, Vertical: 10px
- **Clip Behavior**: antiAlias

**Input Field:**
- **Height**: 44px, 46px (varies by variant)
- **Padding**: Top: 4px, Left: 20px, Right: 15px, Bottom: 4px
- **Background**: #F4F6F9 (color-bg-quaternary)
- **Border**: 2px solid #F4F6F9 (invisible border, same as background)
- **Border Radius**: 15px (radius-3xl)
- **Text Color (Disabled)**: #D9DDE2 (color-text-disabled)

#### Variant 1: Simple Placeholder (Email)

**Input:**
- **Height**: 44px
- **Text**: "Your email"
- **Font**: Archivo
- **Font Size**: 12px (font-size-xs)
- **Font Weight**: 400 (normal)
- **Color**: #D9DDE2 (color-text-disabled)
- **Line Height**: 1.40
- **Text Width**: 308px

#### Variant 2: Input with Success Helper Text

**Input:**
- **Height**: 46px
- **Text**: "First name"
- **Font**: Archivo 12px normal
- **Color**: #D9DDE2 (color-text-disabled)

**Helper Text:**
- **Text**: "Name is correct 👌"
- **Font**: Archivo
- **Font Size**: 12px (text), 14px (emoji)
- **Font Weight**: 400 (normal)
- **Color**: #11BB8D (color-success-positive)
- **Line Height**: 1.40
- **Padding**: Horizontal: 10px
- **Spacing**: 13px gap
- **Width**: 309px (text), 5px spacing before emoji

#### Variant 3: Input with Top Label and Balance Info

**Top Label Row:**
- **Padding**: Horizontal: 10px
- **Spacing**: 13px gap
- **Alignment**: Space between

**Label:**
- **Text**: "From"
- **Font**: Archivo
- **Font Size**: 14px (font-size-sm)
- **Font Weight**: 600 (semibold)
- **Color**: #09101D (color-text-primary)
- **Line Height**: 1.40
- **Width**: 189px

**Balance Info:**
- **Balance**: "Balance: 1.01 ETH"
  - Font: Archivo 10px (font-size-2xs) semibold
  - Color: #09101D (color-text-primary)
  - Line Height: 1.40
- **Price**: "~4.043$"
  - Font: Archivo 10px (font-size-2xs) semibold
  - Color: #0B24FB (color-price-primary)
  - Line Height: 1.40
  - Spacing: 10px from balance

**Input:**
- **Height**: 46px
- **Text**: "Enter amount "
- **Font**: Archivo 12px normal
- **Color**: #D9DDE2 (color-text-disabled)

#### Variant 4: Input with Trailing Icon (Location)

**Input:**
- **Height**: 46px
- **Text**: "Location"
- **Font**: Archivo 12px normal
- **Color**: #D9DDE2 (color-text-disabled)
- **Text Width**: 276px

**Trailing Icon:**
- **Size**: 24px × 24px
- **Padding**: 2px (container padding)
- **Border Radius**: 100px (circular)
- **Spacing**: 5px gap from text
- **Position**: Right edge

#### Variant 5: Input with Leading Icon (Search)

**Input:**
- **Height**: 46px
- **Spacing**: 10px between icon and text

**Leading Icon:**
- **Size**: 24px × 24px
- **Padding**: 2px (container padding)
- **Border Radius**: 100px (circular)
- **Position**: Left side before text

**Text:**
- **Text**: "Search"
- **Font**: Archivo 12px normal
- **Color**: #D9DDE2 (color-text-disabled)
- **Width**: 274px

#### Variant 6: Input with Leading Avatar and Trailing Icon

**Input:**
- **Height**: 46px
- **Spacing**: 10px between avatar and text

**Leading Avatar:**
- **Size**: 30px × 30px
- **Border Radius**: 50px (circular)
- **Background**: #F4F6F9 (color-bg-quaternary)
- **Image**: 30×30px network image
- **Shape**: Oval border
- **Position**: Left side

**Text:**
- **Text**: "Helen Smith"
- **Font**: Archivo 12px normal
- **Color**: #D9DDE2 (color-text-disabled)
- **Width**: 236px

**Trailing Icon:**
- **Size**: 24px × 24px
- **Padding**: 2px
- **Border Radius**: 100px (circular)
- **Spacing**: 5px gap
- **Position**: Right edge

#### Variant 7: Input with Bold Value (Email)

**Input:**
- **Height**: 44px
- **Text**: "you@awesome.com"
- **Font**: Archivo
- **Font Size**: 14px (font-size-sm)
- **Font Weight**: 600 (semibold)
- **Color**: #D9DDE2 (color-text-disabled)
- **Line Height**: 1.40
- **Text Width**: 308px

#### Variant 8: Input with Bottom Helper Text (Username)

**Input:**
- **Height**: 46px
- **Text**: "@johnsmith"
- **Font**: Archivo 14px semibold
- **Color**: #D9DDE2 (color-text-disabled)
- **Text Width**: 308px

**Helper Text:**
- **Text**: "Helper message"
- **Font**: Archivo
- **Font Size**: 14px (font-size-sm)
- **Font Weight**: 400 (normal)
- **Color**: #D9DDE2 (color-text-disabled)
- **Line Height**: 1.40
- **Padding**: Horizontal: 10px
- **Width**: 323px

#### Variant 9: Input with Top Label (To/Estimated)

**Top Label Row:**
- **Padding**: Horizontal: 10px
- **Alignment**: Space between

**Label:**
- **Text**: "To (Estimated)"
- **Font**: Archivo 14px semibold
- **Color**: #09101D (color-text-primary)
- **Width**: 172px

**Balance Info:**
- **Balance**: "Balance: 0.10025 BTC"
  - Font: Archivo 10px semibold
  - Color: #09101D (color-text-primary)
- **Price**: "~6.984$"
  - Font: Archivo 10px semibold
  - Color: #4141E6 (color-accent)
  - Spacing: 10px from balance

**Input:**
- **Height**: 46px
- **Text**: "Enter amount"
- **Font**: Archivo 14px semibold
- **Color**: #D9DDE2 (color-text-disabled)

#### Variant 10: Input with Value and Trailing Clear Icon

**Input:**
- **Height**: 46px
- **Text**: "you@awesome.com"
- **Font**: Archivo 14px semibold
- **Color**: #D9DDE2 (color-text-disabled)
- **Text Width**: 276px

**Trailing Clear Icon:**
- **Size**: 24px × 24px
- **Padding**: 2px
- **Border Radius**: 100px (circular)
- **Spacing**: 5px gap
- **Position**: Right edge

#### Layout Structure:

**Basic Input:**
```
┌─────────────────────────────────────┐
│ [Padding 20px L, 15px R]            │
│  Your email                         │
│                                     │
└─────────────────────────────────────┘
Height: 44px or 46px, Radius: 15px
```

**With Top Label & Balance:**
```
┌─────────────────────────────────────┐
│ From      Balance: 1.01 ETH ~4.043$ │
│ ┌─────────────────────────────────┐ │
│ │ Enter amount                    │ │
│ └─────────────────────────────────┘ │
└─────────────────────────────────────┘
Label: 14px semibold, Balance: 10px semibold
```

**With Helper Text:**
```
┌─────────────────────────────────────┐
│ ┌─────────────────────────────────┐ │
│ │ First name                      │ │
│ └─────────────────────────────────┘ │
│ Name is correct 👌                  │
└─────────────────────────────────────┘
Helper: 12px Archivo, success green
```

**With Icons:**
```
┌─────────────────────────────────────┐
│ ┌─────────────────────────────────┐ │
│ │ [icon] Search              [×]  │ │
│ └─────────────────────────────────┘ │
└─────────────────────────────────────┘
Icons: 24×24px, 2px padding, circular
```

**With Avatar:**
```
┌─────────────────────────────────────┐
│ ┌─────────────────────────────────┐ │
│ │ [@] Helen Smith            [×]  │ │
│ └─────────────────────────────────┘ │
└─────────────────────────────────────┘
Avatar: 30×30px circular
```

#### Typography Summary:

**Placeholder/Value Text:**
- **12px normal**: Basic placeholders (#D9DDE2)
- **14px semibold**: Bold values, usernames (#D9DDE2)

**Labels:**
- **14px semibold**: Field labels (#09101D)

**Helper Text:**
- **12px normal**: Success messages (#11BB8D)
- **14px normal**: Helper messages (#D9DDE2)

**Balance/Price Info:**
- **10px semibold**: Balance amounts (#09101D)
- **10px semibold**: Price values (#0B24FB, #4141E6)

#### Icon Sizes:

- **24×24px**: Action icons (search, clear, location)
- **30×30px**: User avatars
- **16×16px**: Embedded icons (within larger containers)

#### Spacing:

- **Container Padding**: 16px horizontal, 10px vertical
- **Input Padding**: 20px left, 15px right, 4px top/bottom
- **Helper Text Padding**: 10px horizontal
- **Icon Spacing**: 5px gap, 10px for avatar
- **Balance Info Spacing**: 10px between balance and price
- **Helper Text Spacing**: 13px gap from input

#### Color Palette:

**Text:**
- Disabled: #D9DDE2 (all disabled input text)
- Primary: #09101D (labels, balance info)
- Success: #11BB8D (success helper text)
- Price Primary: #0B24FB (price display)
- Price Secondary: #4141E6 (price display alternative)

**Background:**
- Input: #F4F6F9 (disabled state background)
- Avatar Placeholder: #F4F6F9

#### Use Cases:

1. **Email Inputs**: Simple placeholder or filled value with semibold text
2. **Username Fields**: With @ prefix and helper text
3. **Search Fields**: Leading icon for visual indication
4. **Location Fields**: Trailing icon for additional actions
5. **Amount/Currency Fields**: Top labels with balance and price info
6. **User Selection**: Avatar display with name
7. **Form Validation**: Success helper text with emoji feedback
8. **Multi-info Inputs**: Labels, balance, price, and helper text combinations

#### Best Practices:

- Use 12px for placeholders in compact fields
- Use 14px semibold for actual values to distinguish from placeholders
- Top labels (14px semibold) provide context for complex inputs
- Balance info (10px semibold) displays related data without cluttering
- Price display uses distinct colors (#0B24FB or #4141E6) for visibility
- Helper text provides validation feedback or additional instructions
- Success messages (#11BB8D) with emoji add friendly confirmation
- Icons (24×24px) provide visual affordances for actions
- Avatars (30×30px) help identify users in selection fields
- Disabled state (#D9DDE2) maintains readability while indicating non-interactivity
- Input heights: 44px for simple fields, 46px for fields with icons/avatars
- Border radius: 15px maintains visual consistency
- Padding: 20px left, 15px right ensures comfortable reading
- All disabled inputs use same background (#F4F6F9) for consistency

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

**Текущая версия**: v5.8.0

### Changelog

#### v5.8.0 (2025-11-19)
- Добавлены данные из ContentTextTopHelperNoBottomHelperNoStateDisabled компонента Flutter (Text Input Fields - Disabled States)
- Добавлены новые design tokens для отображения цен:
  - Price Primary: #0B24FB (color-price-primary) для основного отображения цен
  - Price Secondary: #4141E6 (color-price-secondary) для альтернативного отображения
- Добавлен компонент Text Input Fields (Disabled States with Variants) с 10 вариантами:
  - Variant 1: Simple Placeholder (Email) - "Your email", 12px, 44px height
  - Variant 2: Input with Success Helper Text - "First name" + success message (#11BB8D) с emoji
  - Variant 3: Input with Top Label and Balance Info - "From" label + balance + price (#0B24FB)
  - Variant 4: Input with Trailing Icon (Location) - 24×24px trailing icon
  - Variant 5: Input with Leading Icon (Search) - 24×24px leading icon
  - Variant 6: Input with Leading Avatar and Trailing Icon - 30×30px avatar + name + icon
  - Variant 7: Input with Bold Value (Email) - "you@awesome.com", 14px semibold
  - Variant 8: Input with Bottom Helper Text (Username) - "@johnsmith" + helper message
  - Variant 9: Input with Top Label (To/Estimated) - label + balance + price (#4141E6)
  - Variant 10: Input with Value and Trailing Clear Icon - value + 24×24px clear icon
- Input спецификации:
  - Heights: 44px (simple), 46px (with icons/avatars)
  - Padding: 20px left, 15px right, 4px top/bottom
  - Border radius: 15px
  - Background: #F4F6F9 (disabled state)
  - Border: 2px solid #F4F6F9 (invisible border)
- Typography:
  - Placeholders: 12px normal (#D9DDE2)
  - Values: 14px semibold (#D9DDE2)
  - Labels: 14px semibold (#09101D)
  - Helper text: 12px/14px normal (#11BB8D success, #D9DDE2 default)
  - Balance/Price: 10px semibold (#09101D balance, #0B24FB/#4141E6 price)
- Icon & Avatar sizes:
  - Action icons: 24×24px
  - User avatars: 30×30px circular
  - Embedded icons: 16×16px
- Spacing:
  - Container: 16px horizontal, 10px vertical
  - Helper text: 10px horizontal padding, 13px gap from input
  - Icon spacing: 5px gap, 10px for avatar
  - Balance info: 10px between balance and price
- Документированы 8 use cases и comprehensive best practices для различных типов полей

#### v5.7.0 (2025-11-19)
- Добавлены данные из SmallLeadingSelector компонента Flutter (Form Input with Leading Selector)
- Добавлены новые design tokens для валидации форм:
  - Success Positive: #11BB8D (color-success-positive) для успешной валидации
  - Success Positive Background: rgba(17, 187, 141, 0.05) (color-success-positive-bg)
  - Error Negative: #DA1414 (color-error-negative) для ошибок валидации
  - Error Negative Background: rgba(218, 20, 20, 0.05) (color-error-negative-bg)
  - Pressed Background: #EAEFF2 (color-bg-pressed) для состояния нажатия
- Добавлен компонент Form Input with Small Leading Selector с 9 состояниями:
  - Enabled (Default): #F4F6F9 background, no border
  - Focus: White background, 2px solid #09101D border, cursor visible
  - Complete (Filled): #F4F6F9 background, value "Emily", clear icon visible
  - Positive (Success): rgba(17, 187, 141, 0.05) background, 2px solid #11BB8D border
  - Pressed: #EAEFF2 background (active click state)
  - Active - Typing: White background, 2px border, cursor after partial text "Em"
  - Incomplete: #F4F6F9 background, empty value with clear icon
  - Negative (Error): rgba(218, 20, 20, 0.05) background, 2px solid #DA1414 border
  - Disabled: #F4F6F9 background, 0.6 opacity, secondary text color
- Input спецификации:
  - Height: 36px, Border radius: 15px
  - Leading Selector: "Ms." text, 14px semibold, 16px L / 10px R padding
  - Text Input: 14px normal, 16px L / 20px R padding, expandable
  - Label: 14px semibold, 8px margin bottom
  - Helper Text: 14px normal, secondary/success/error color, 8px margin top
  - Clear Icon: 20×20px, positioned right
  - Cursor: 2px width, 16px height, blinking
- Showcase container: 840×710px, two column layout для демонстрации всех состояний
- Border specifications: 2px для focus/validation states, 0 для default states
- Validation backgrounds: 5% opacity для subtle visual feedback
- Документированы use cases и best practices для Form Input компонентов

#### v5.6.0 (2025-11-19)
- Добавлены данные из Message компонента Flutter (Chat Messages)
- Добавлены новые design tokens:
  - Background: #FAFAFB (color-bg-light) для showcase containers
  - Background: #303239 (color-bg-message-outgoing) для исходящих сообщений
  - Border radius: 11px (radius-reaction) для reaction badges
- Добавлен компонент Chat Messages с 5 вариантами:
  - Incoming Message with Header: Large avatar 40×40px (32×32px image), name + timestamp header
  - Incoming Message Bubble: Small avatar 32×32px (24×24px image), 248px bubble
  - Incoming Message Bubble (No Avatar): 248px bubble without avatar
  - Outgoing Message with Avatar: 260px bubble, dark background (#303239)
  - Outgoing Message (No Avatar): 260px bubble without avatar
- Avatar sizes:
  - Large: 40×40px container, 32×32px image (for message headers)
  - Small: 32×32px container, 24×24px image (for bubbles)
- Message bubbles:
  - Incoming: 248px width, #F4F6F9 background, 15px radius
  - Outgoing: 260px width, #303239 background, 15px radius, white text
- Reaction badges: 24px height, 11px radius, #F4F6F9 background
- Showcase container: 929×970px, #FAFAFB background, 50px padding
- Документированы use cases и best practices для Chat Messages

#### v5.5.0 (2025-11-19)
- Добавлены данные из Basic компонента Flutter (User Profile Cards)
- Добавлены новые design tokens:
  - Font size: 32px (font-size-2xl-plus) для заголовков профиля
  - Instagram gradient: #833AB4 → #FD1D1D → #FCB045 для Live badges
  - Badge shadow: 0 1px 1px 0 rgba(0, 0, 0, 0.4)
- Добавлен компонент User Profile Cards с 3 вариантами:
  - Basic Profile Card: Avatar 56×56px (48×48px image), title 32px, subtitle 14px
  - Avatar Group/Row: Horizontal row из 5 аватаров с различными badge вариантами
  - Profile Card with Live Badge and Toggle: Live badge с Instagram gradient, toggle switch 52×31px
- Avatar спецификации:
  - Container: 56×56px, Image: 48×48px, Offset: 4px
  - Border radius: 40px (circular)
  - Placeholder background: #D9DDE2
- Badge позиции и размеры:
  - Bottom-right: 20×20px container, 14×14px badge
  - Top-right: 20×20px с shadow, accent/dark background
- Toggle Switch: 52×31px container, 31×31px knob, accent color background
- Live Badge: 28×14px с Instagram gradient, white border, 12px radius
- Документированы use cases и best practices для User Profile Cards

#### v5.4.0 (2025-11-19)
- Добавлены данные из StoriesTextOutside компонента Flutter
- Добавлен Instagram gradient цвет (#833AB4) для активных stories
- Добавлен новый border radius:
  - 13px (radius-xl-plus) для активного контейнера stories
- Добавлен компонент Stories (Text Outside):
  - Vertical Stories (Portrait): 100×120px изображения
  - Horizontal Stories (Landscape): 130×80px изображения
  - Active story border: 2px solid Instagram gradient (#833AB4)
  - Story labels: 13px Archivo bold, text outside images
  - 4 stories per row layout с 10px spacing
  - Showcase container: 1290×322px с 50px padding
- Документированы 2 варианта компонента с детальными спецификациями
- Добавлены use cases и best practices для Stories компонента

#### v5.3.0 (2025-11-19)
- Добавлены данные из InformationCardSlider компонента Flutter
- Добавлены новые цвета:
  - Sale/Discount цвет (#F7B68A) для скидок и промо
  - Danger/Alert цвет (#E24949) для критических уведомлений
- Обновлены цвета текста:
  - text-dark (#23262B) для темного текста на светлом фоне
  - text-muted (#414249) для второстепенной информации
  - text-subtitle (#373940) для подзаголовков
  - text-disabled обновлен до #D9DDE2
- Добавлены новые gray shades: 250, 550, 575, 650
- Добавлены новые font sizes:
  - 11px (font-size-2xs-plus) для мелкого текста
  - 15px (font-size-sm-plus) для заголовков карточек
- Добавлены новые border radius:
  - 5px (radius-base-plus) для badge компонентов
  - 10px (radius-lg-plus) для avatar компонентов
  - 40px (radius-avatar) для больших аватаров
- Добавлен компонент Information Cards (Slider Component):
  - 4 варианта карточек: Hotel, Experience, Restaurant, Video
  - Image Slider спецификации (327px × 200px, 20px radius)
  - Badge компонент с 5 вариантами (covid-free, new-place, beginner-level, sale, category)
  - Avatar компонент (40px контейнер, 32px изображение, 10px radius)
  - Детальные спецификации typography для карточек (15px title, 13px subtitle, 11px secondary info)

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
