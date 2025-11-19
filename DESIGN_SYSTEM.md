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
--color-text-dark-2: #2A2B2F;  /* Из CardsLight - для time slot buttons */
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
--color-bg-overlay-light: rgba(9, 16, 29, 0.1);  /* Из FinanceLight кода - 10% opacity black для navigation icons и segmented control */
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

### 29. Social Program Card (Complete Block)

Готовый блок карточки социальной программы/курса, извлеченный из Flutter приложения SocialLight. Это целостный UI-блок с галереей, информацией, участниками и действиями.

**🔧 Гибкость блока**: Количество элементов (изображения, аватары, кнопки) может быть изменено в зависимости от требований бэкенда. Например, галерея может содержать 1+4, 1+6 или только 1 изображение; аватары могут быть от 3 до неограниченного количества с горизонтальным скроллом.

#### Общая структура блока:

**Main Container:**
- **Width**: 375px (mobile)
- **Background**: White (#FFFFFF, color-bg-primary)
- **Border Radius**: 30px (top corners)
- **Clip Behavior**: antiAlias

#### 1. Status Bar (iOS-style)

**Container:**
- **Width**: 375px
- **Height**: 44px
- **Background**: #09101D (color-text-primary) - черный
- **Position**: Top of card
- **Purpose**: Имитация iOS status bar для полноэкранного модального окна

#### 2. Top Decoration (Rounded Element)

**Decoration Bar:**
- **Width**: 343px
- **Height**: 10px
- **Background**: #D9DDE2 (color-text-disabled)
- **Border Radius**: 10px (только верхние углы)
- **Position**: Left 16px, Top 1px from status bar bottom
- **Purpose**: Декоративный элемент верхней части

#### 3. Drag Handle (Modal Indicator)

**Handle:**
- **Width**: 40px
- **Height**: 3px
- **Background**: #D9DDE2 (color-text-disabled)
- **Border Radius**: 100px (fully rounded)
- **Position**: Centered horizontally (padding left/right 167px)
- **Padding Bottom**: 8px
- **Purpose**: Визуальный индикатор для свайпа/закрытия модала

#### 4. Header Section (Username)

**Header Container:**
- **Width**: Full (343px content width)
- **Height**: 44px
- **Padding**: Horizontal 16px

**Leading Icon:**
- **Size**: 24×24px
- **Padding**: 4px
- **Border Radius**: 100px (circular)
- **Background**: White
- **Purpose**: Иконка слева (например, back button или logo)

**Username:**
- **Text**: "@crossfit" (example)
- **Font**: Archivo
- **Font Size**: 16px (font-size-base)
- **Font Weight**: 700 (bold)
- **Color**: #09101D (color-text-primary)
- **Width**: 243px (center area)
- **Alignment**: Center

**Trailing Space:**
- **Width**: Flexible (для будущей иконки/меню)

**🔧 Гибкость**: Можно добавить trailing icon (меню, share, close)

#### 5. Image Gallery (Flexible Grid)

**Gallery Container:**
- **Width**: Full (343px content width)
- **Height**: 176px (171px images + 5px bottom padding)
- **Padding**: Left 16px, Right 16px, Bottom 5px
- **Spacing**: 10px between images

**Layout**: 1 Large + 4 Small Grid (2×2)

**Main Image (Large):**
- **Size**: 166.5×171px
- **Border Radius**: 20px (radius-badge)
- **Background**: #F4F6F9 (color-bg-quaternary) - placeholder
- **Position**: Left side
- **Overlay Icon**: 24×24px centered (play button for video)

**Grid Images (Small):**
- **Size**: 78.25×80.5px each
- **Count**: 4 images
- **Layout**: 2 rows × 2 columns
- **Border Radius**: 20px (radius-badge)
- **Background**: #F4F6F9 - placeholder
- **Spacing**: 10px horizontal and vertical gap
- **Overlay Icon**: 24×24px centered (for each)

**🔧 Гибкость**:
- Галерея может содержать 1+4 (default), 1+6 (3×2), или только 1 большое изображение
- Можно добавить counter badge "1/5" для навигации
- Grid может быть заменен на horizontal scroll для большего количества

#### 6. Profile Avatar with Badge

**Avatar Container:**
- **Size**: 56×56px container
- **Image**: 48×48px (offset 4px)
- **Border Radius**: 40px (circular)
- **Background**: #D9DDE2 (placeholder)
- **Padding**: Vertical 10px

**Badge (Top-Right):**
- **Text**: "Trainer" (example)
- **Size**: 20×20px container
- **Padding**: Horizontal 4px, Vertical 2px
- **Background**: #4141E6 (color-accent)
- **Border Radius**: 12px (radius-xl)
- **Font**: Archivo 10px (font-size-2xs) semibold
- **Color**: White
- **Position**: Left 36px, Top 0 (top-right corner of avatar)

**🔧 Гибкость**: Badge может отображать роль (Trainer, Admin, VIP) или статус

#### 7. Title Section

**Title:**
- **Text**: "Intro to Crossfit on Bali" (example)
- **Font**: Archivo
- **Font Size**: 18px (font-size-md)
- **Font Weight**: 700 (bold)
- **Color**: #09101D (color-text-primary)
- **Alignment**: Center
- **Padding**: Horizontal 16px
- **Spacing**: 5px gap to subtitle

**Subtitle:**
- **Text**: "4 weeks ・ 5.042 members" (example)
- **Font**: Archivo
- **Font Size**: 12px (font-size-xs)
- **Font Weight**: 400 (normal)
- **Color**: #09101D (color-text-primary)
- **Alignment**: Center
- **Width**: 343px

**🔧 Гибкость**: Subtitle может содержать различные метаданные (duration, members, price, rating)

#### 8. Participants Row (Avatar List)

**Row Container:**
- **Width**: 375px
- **Padding**: Horizontal 16px, Vertical 10px
- **Layout**: Horizontal row

**Avatar Types:**

**1. Avatar with Live Badge (×2):**
- **Container**: 56×56px
- **Image**: 48×48px, offset 4px, radius 40px
- **Live Badge**:
  - Size: 28×14px
  - Background: Instagram gradient (linear-gradient #833AB4 → #FD1D1D → #FCB045)
  - Border: 1px white
  - Border Radius: 12px (radius-xl)
  - Text: "Live", 10px semibold, white
  - Position: Left 0, Top 36px (bottom of avatar)

**2. Avatar with Active Border:**
- **Outer Container**: 56×56px
- **Border**: 2px solid #833AB4 (color-brand-instagram-gradient)
- **Border Radius**: 30px
- **Image**: 48×48px, offset 4px, radius 40px

**3. Regular Avatars (×4):**
- **Container**: 56×56px
- **Image**: 48×48px, offset 4px, radius 40px
- **Background**: #D9DDE2 (placeholder)

**🔧 Гибкость**:
- Количество аватаров: от 3 до неограниченного с horizontal scroll
- Можно показать "+25 more" badge в конце
- Live badge опционален
- Active border показывает текущего пользователя

#### 9. Action Buttons

**Buttons Container:**
- **Padding**: Vertical 10px, Horizontal 16px
- **Spacing**: 10px gap between buttons

**Primary Button (Join program):**
- **Height**: 36px
- **Padding**: Horizontal 16px, Vertical 10px
- **Background**: #09101D (color-text-primary) - черный
- **Border Radius**: 15px (radius-3xl)
- **Text**: "Join program"
- **Font**: Archivo 13px (font-size-xs-plus) semibold
- **Color**: White
- **Alignment**: SpaceBetween with 70px spacing
- **Flex**: Expanded (takes available space)

**Icon Button (Share/More):**
- **Height**: 36px
- **Width**: Auto (fits icon + padding)
- **Padding**: Horizontal 16px, Vertical 10px
- **Background**: #F4F6F9 (color-bg-quaternary) - светло-серый
- **Border Radius**: 15px (radius-3xl)
- **Icon**: 16×16px, padding 2px, radius 100px

**🔧 Гибкость**:
- Можно добавить третью кнопку (Save, Share, More)
- Primary button текст меняется в зависимости от статуса (Join, Joined, Continue)
- Icon button может быть Share, Bookmark, Menu

#### Complete Block Layout:

```
┌─────────────────────────────────────────┐
│ ███████████ Status Bar ██████████████   │ 44px
├─────────────────────────────────────────┤
│ ▓▓▓▓▓▓▓▓ Top Decoration ▓▓▓▓▓▓▓▓        │ 10px
│             ─── Handle ───               │ 3px + 8px
├─────────────────────────────────────────┤
│ [Icon]     @crossfit           [ ]       │ 44px Header
├─────────────────────────────────────────┤
│ ┌────────┐ ┌──┐ ┌──┐                    │
│ │        │ └──┘ └──┘  176px Gallery     │
│ │  Main  │ ┌──┐ ┌──┐                    │
│ │ Image  │ └──┘ └──┘                    │
│ └────────┘                               │
├─────────────────────────────────────────┤
│        [@Trainer]                        │ 56px + padding
├─────────────────────────────────────────┤
│   Intro to Crossfit on Bali             │ Title
│   4 weeks ・ 5.042 members               │ Subtitle
├─────────────────────────────────────────┤
│ [@Live] [@Live] [@*] [@] [@] [@] [@]    │ Avatars row
├─────────────────────────────────────────┤
│ [ Join program           ] [📤]         │ Buttons 36px
└─────────────────────────────────────────┘

Width: 375px (mobile)
Border Radius: 30px (top corners)
Background: White
```

#### Spacing Summary:

- **Outer Padding**: 16px horizontal (most sections)
- **Status Bar**: 44px height
- **Top Decoration**: 10px height, 1px top offset
- **Drag Handle**: 3px height, 8px bottom padding
- **Header**: 44px height
- **Gallery**: 176px height (171px + 5px bottom)
- **Image Spacing**: 10px gaps
- **Avatar**: 56×56px with 10px vertical padding
- **Title/Subtitle**: 5px gap, 16px horizontal padding
- **Avatars Row**: 10px vertical padding
- **Buttons**: 10px vertical padding, 36px height

#### Typography Summary:

- **Header Username**: 16px bold #09101D
- **Title**: 18px bold #09101D
- **Subtitle**: 12px normal #09101D
- **Button Text**: 13px semibold white
- **Badge Text**: 10px semibold white

#### Use Cases:

1. **Fitness Programs**: Crossfit classes, yoga courses, training programs
2. **Educational Courses**: Online classes, workshops, tutorials
3. **Social Events**: Meetups, conferences, group activities
4. **Community Groups**: Interest groups, clubs, communities
5. **Memberships**: Subscription programs, exclusive groups
6. **Live Streaming**: Scheduled live events with participant previews

#### Best Practices:

**Flexibility & Extensibility:**
- Image gallery is modular: support 1 main + 2-6 grid images or single image
- Avatar row can show 3-20+ participants with horizontal scroll
- Button row can accommodate 2-3 action buttons
- Title and subtitle can be multi-line with ellipsis
- Badges and statuses are optional overlays

**Responsive Behavior:**
- Fixed 375px width for mobile (can scale to 768px for tablet)
- Gallery maintains aspect ratios when scaled
- Avatar row scrolls horizontally on overflow
- Buttons stack vertically on narrow screens (<320px)

**Interactive States:**
- Drag handle indicates modal can be dismissed by swipe down
- Primary button shows hover/pressed states
- Gallery images are tappable for fullscreen view
- Avatars are tappable to show user profiles
- Live badges blink or animate to indicate active status

**Accessibility:**
- Status bar provides context for full-screen modal
- Drag handle is 44px minimum touch target (including padding)
- Button text is clear and actionable
- Image alt text describes gallery content
- Avatar badges have semantic meaning

**Design Tokens Used:**
- Colors: #09101D, #D9DDE2, #F4F6F9, #4141E6, #833AB4, White
- Border Radius: 10px, 12px, 15px, 20px, 30px, 40px, 100px
- Font Sizes: 10px, 12px, 13px, 16px, 18px
- Spacing: 3px, 5px, 8px, 10px, 16px, 44px
- Shadows: Optional card shadow for elevation

**Common Modifications:**
- **Add Price Tag**: Insert price badge in title area
- **Add Rating**: Show stars/rating below subtitle
- **Add Progress**: Show completion bar for courses
- **Add More Images**: Extend grid to 2×3 or add horizontal scroll
- **Add More Buttons**: Insert secondary actions (Save, Share, Report)
- **Add Labels**: Category, Difficulty, Duration badges
- **Add Countdown**: For limited-time events
- **Add Capacity**: Show "23/50 spots left" in subtitle

---

### 30. Movie/Event Card (Complete Block)

Готовый блок карточки фильма/события с постером, информацией о сеансах и бронированием, извлеченный из Flutter приложения CardsLight. Это целостный UI-блок с изображением, метаданными, рейтингом и временными слотами.

**🔧 Гибкость блока**: Количество элементов (временные слоты, жанровые badges, карточки) может быть изменено в зависимости от требований бэкенда. Например, временные слоты могут быть от 2 до 10+ с горизонтальным скроллом; жанровые badges от 1 до 5+; можно добавить информацию о цене, директоре, актерах.

#### Общая структура блока:

**Main Container:**
- **Width**: 375px (mobile)
- **Padding**: Vertical 30px
- **Background**: White (#FFFFFF, color-bg-primary)
- **Border Radius**: 30px (radius-card-large)
- **Layout**: Vertical column with 2 identical card structures (можно 1+)

**🔧 Гибкость**: Контейнер может содержать от 1 до неограниченного количества карточек с vertical scroll

#### 1. Movie/Event Card (Single Card)

**Card Container:**
- **Width**: 343px (full width minus padding 16px each side)
- **Height**: 400px
- **Layout**: Stack (image + overlay content)
- **Spacing**: 20px gap between cards

#### 2. Poster Section (Background Image with Overlay)

**Poster Image:**
- **Size**: 343×290px
- **Border Radius**: 15px (radius-3xl)
- **Background**: Image with gradient overlay
- **Position**: Top of card
- **Clip**: antiAlias

**Gradient Overlay:**
- **Type**: Linear gradient vertical
- **Colors**:
  - Top: Colors.black.withValues(alpha: 0) - transparent
  - Bottom: Colors.black - solid black
- **Purpose**: Обеспечивает читаемость текста поверх изображения

**Action Icon (Top-Right):**
- **Size**: 28×28px container
- **Icon**: 16×16px (bookmark/favorite)
- **Background**: Semi-transparent or solid
- **Position**: Top-right corner (padding 12px from edges)
- **Border Radius**: 100px (circular)
- **Purpose**: Bookmark, favorite, or share action

**🔧 Гибкость**:
- Icon может быть bookmark (незаполненный/заполненный), heart, share
- Можно добавить дополнительные иконки (play button для трейлера)
- Gradient может быть отключен для light posters

#### 3. Content Overlay Section (On Poster)

**Title:**
- **Text**: "The Dark Knight" (example)
- **Font**: Archivo
- **Font Size**: 16px (font-size-base)
- **Font Weight**: 700 (bold)
- **Color**: White (#FFFFFF)
- **Position**: Bottom-left on poster (padding 16px left, 10px from badges)
- **Max Lines**: 1 with ellipsis

**Description:**
- **Text**: Movie/event description (example: "Готэм-Сити находится на грани...")
- **Font**: Archivo
- **Font Size**: 14px (font-size-sm)
- **Font Weight**: 400 (normal)
- **Color**: White (#FFFFFF)
- **Position**: Below title (5px gap)
- **Max Lines**: 2 with ellipsis
- **Padding**: Left 16px, Right 16px

**🔧 Гибкость**: Description может быть скрыт или расширен до 3-4 строк

#### 4. Badges Row (Rating & Genre Tags)

**Badges Container:**
- **Layout**: Horizontal row
- **Padding**: Left 16px, Bottom 16px from poster bottom
- **Spacing**: 10px gap between badges
- **Position**: Bottom-left corner of poster

**Rating Badge:**
- **Text**: "8.9" (example)
- **Height**: 24px
- **Padding**: Horizontal 8px, Vertical 5px
- **Background**: #11BB8D (color-success-positive) - зеленый для положительной оценки
- **Border Radius**: 10px (radius-lg-plus)
- **Font**: Archivo 11px (font-size-2xs-plus) semibold
- **Color**: White (#FFFFFF)
- **Purpose**: IMDb/Kinopoisk rating

**Genre Badges (×2 or more):**
- **Text**: "Comics", "Science Fiction" (examples)
- **Height**: 24px
- **Padding**: Horizontal 8px, Vertical 5px
- **Background**: #23262B (color-text-dark) - темный
- **Border Radius**: 10px (radius-lg-plus)
- **Font**: Archivo 11px (font-size-2xs-plus) semibold
- **Color**: White (#FFFFFF)
- **Layout**: Wrap if more than 3 badges

**🔧 Гибкость**:
- Badges количество от 1 до 5+ с возможностью wrap
- Можно добавить badge для возрастного рейтинга (16+, 18+)
- Rating badge может менять цвет в зависимости от оценки:
  - 8.0+: #11BB8D (зеленый)
  - 6.0-7.9: #F59E0B (оранжевый)
  - <6.0: #E24949 (красный)

#### 5. Info Row (Location, Distance, Date)

**Info Container:**
- **Layout**: Horizontal row
- **Padding**: Top 10px from poster bottom
- **Spacing**: 10px gap between elements
- **Alignment**: Center vertically

**Distance Info:**
- **Text**: "~500m" (example)
- **Font**: Archivo
- **Font Size**: 15px (font-size-sm-plus)
- **Font Weight**: 600 (semibold)
- **Color**: #747B84 (color-text-secondary)
- **Purpose**: Distance to cinema/venue

**Location Name:**
- **Text**: "Cinema Plaza" (example)
- **Font**: Archivo
- **Font Size**: 16px (font-size-base)
- **Font Weight**: 700 (bold)
- **Color**: #09101D (color-text-primary)
- **Flex**: Expanded (takes available space)

**Date Info:**
- **Text**: "Today" (example)
- **Font**: Archivo
- **Font Size**: 16px (font-size-base)
- **Font Weight**: 700 (bold)
- **Color**: #09101D (color-text-primary)

**🔧 Гибкость**:
- Distance может быть скрыт или показывать транспортное время
- Date может быть "Today", "Tomorrow", конкретная дата "15 Nov"
- Можно добавить иконки (location pin, calendar)

#### 6. Time Slots Row (Booking Times)

**Time Slots Container:**
- **Layout**: Horizontal row with wrap
- **Padding**: Top 10px from info row
- **Spacing**: 10px gap between buttons
- **Alignment**: Start (left-aligned)

**Time Slot Button (×4 default):**
- **Text**: "23:00", "00:15", "01:30", "3:00" (examples)
- **Height**: 36px
- **Padding**: Horizontal 16px, Vertical 10px
- **Background**: #F4F6F9 (color-bg-quaternary) - светло-серый
- **Border Radius**: 15px (radius-3xl)
- **Font**: Archivo 11px (font-size-2xs-plus) semibold
- **Color**: #2A2B2F (color-text-dark-2) - темный текст на светлом фоне
- **Border**: None (default)
- **Interactive States**:
  - Default: #F4F6F9 background, #2A2B2F text
  - Hover: Slightly darker background
  - Selected: #09101D background, white text
  - Disabled/Sold Out: #D9DDE2 background, #747B84 text

**🔧 Гибкость**:
- Количество time slots от 2 до 10+ с horizontal scroll
- Можно добавить индикатор доступности мест ("23:00 • 5 left")
- Selected state для выбранного времени
- Disabled state для проданных сеансов
- Можно группировать по дням для multi-day events

#### Complete Block Layout:

```
┌─────────────────────────────────────────┐
│  ╔══════════════════════════════════╗   │
│  ║                            [♡]   ║   │
│  ║                                  ║   │
│  ║         POSTER IMAGE             ║   │ 290px
│  ║       (343 × 290px)              ║   │
│  ║                                  ║   │
│  ║  ▓▓▓▓ Gradient Overlay ▓▓▓▓▓▓▓  ║   │
│  ║  The Dark Knight                 ║   │
│  ║  Готэм-Сити находится на грани.. ║   │
│  ║  [8.9] [Comics] [Sci-Fi]         ║   │
│  ╚══════════════════════════════════╝   │
│                                          │
│  ~500m    Cinema Plaza         Today    │ Info Row
│                                          │
│  [23:00] [00:15] [01:30] [3:00]         │ Time Slots
├──────────────────────────────────────────┤ 20px gap
│  ╔══════════════════════════════════╗   │
│  ║                            [♡]   ║   │
│  ║         POSTER IMAGE #2          ║   │ Second Card
│  ║       (Same structure)           ║   │ (Optional)
│  ║                                  ║   │
│  ║  [8.5] [Drama] [Action]          ║   │
│  ╚══════════════════════════════════╝   │
│  ~1.2km   Cinema Star          Today    │
│  [18:30] [20:45] [22:00]                │
└──────────────────────────────────────────┘

Container Width: 375px
Card Width: 343px
Poster Height: 290px
Card Total Height: ~400px
Padding: 16px horizontal, 30px vertical
Background: White, Border Radius: 30px
```

#### Spacing Summary:

- **Container Padding**: Horizontal 16px (each side), Vertical 30px (top/bottom)
- **Poster Size**: 343×290px
- **Poster Border Radius**: 15px
- **Action Icon**: 28×28px, top-right 12px offset
- **Title Padding**: Left 16px, bottom 10px from badges row
- **Description Padding**: Left 16px, Right 16px, 5px gap from title
- **Badges Row**: Left 16px, Bottom 16px from poster bottom, 10px gap between badges
- **Badges Height**: 24px, padding 8px horizontal, 5px vertical
- **Info Row**: Top 10px from poster, 10px gap between elements
- **Time Slots Row**: Top 10px from info row, 10px gap between buttons
- **Time Slot Button**: 36px height, 16px horizontal padding, 10px vertical padding
- **Cards Gap**: 20px between multiple cards

#### Typography Summary:

- **Title**: 16px bold white (Archivo)
- **Description**: 14px normal white (Archivo)
- **Rating Badge**: 11px semibold white (Archivo)
- **Genre Badges**: 11px semibold white (Archivo)
- **Distance**: 15px semibold #747B84 (Archivo)
- **Location**: 16px bold #09101D (Archivo)
- **Date**: 16px bold #09101D (Archivo)
- **Time Slots**: 11px semibold #2A2B2F (Archivo)

#### Use Cases:

1. **Cinema Showtimes**: Movie listings with session times and booking
2. **Theater Events**: Theater performances, concerts, shows
3. **Sports Events**: Match schedules, ticket availability
4. **Conferences**: Event sessions, workshop schedules
5. **Exhibitions**: Museum exhibitions, art gallery events
6. **Online Events**: Webinars, virtual events with time zones

#### Best Practices:

**Flexibility & Extensibility:**
- Time slots can range from 2 to 10+ with horizontal scroll for overflow
- Genre badges can be 1-5+ with wrapping to second line
- Multiple cards can be displayed in vertical scroll container
- Rating badge color can change based on score threshold
- Additional metadata can be added (director, cast, duration, price)

**Responsive Behavior:**
- Fixed 343px card width for mobile 375px container
- Time slots wrap to multiple rows if many sessions
- Poster maintains 343:290 aspect ratio when scaled
- Cards stack vertically with consistent 20px spacing
- Horizontal scroll for time slots on overflow

**Interactive States:**
- Time slot buttons show hover, selected, disabled states
- Action icon (bookmark) toggles between saved/unsaved
- Poster can be tapped for full details or trailer
- Badges can be filtered by tapping (show only this genre)
- Smooth transitions between states (200ms ease-in-out)

**Accessibility:**
- Action icon has minimum 44×44px touch target (with padding)
- Time slot buttons have clear contrast (#2A2B2F on #F4F6F9)
- Gradient overlay ensures text readability on all poster backgrounds
- Rating and genre information is semantically labeled
- Alt text for poster images describes movie/event

**Design Tokens Used:**
- Colors: #FFFFFF, #000000, #09101D, #23262B, #2A2B2F, #747B84, #11BB8D, #F4F6F9, #D9DDE2
- Border Radius: 10px, 15px, 30px, 100px
- Font Sizes: 11px, 14px, 15px, 16px
- Font Weights: 400 (normal), 600 (semibold), 700 (bold)
- Spacing: 5px, 10px, 12px, 16px, 20px, 30px
- Shadows: Optional card shadow for elevation

**Common Modifications:**
- **Add Price**: Insert ticket price badge in badges row or below time slots
- **Add Duration**: Show movie duration "2h 15m" in info row
- **Add Age Rating**: Show "16+", "18+" badge with rating
- **Add Seat Availability**: Show "23/150 seats" below time slots
- **Add Director/Cast**: Show key cast members with small avatars
- **Add 3D/IMAX Badges**: Technology badges alongside genre
- **Add Booking Status**: Show "Booked", "In Cart" state for selected time
- **Add Multi-Day Schedule**: Group time slots by dates with date headers
- **Add Trailer Preview**: Auto-play video preview on card hover
- **Add User Rating**: Allow users to submit their own rating

---

### 31. Finance Dashboard with Performance Chart (Complete Block)

<!-- @block-id: finance-dashboard -->
<!-- @category: finance, dashboard, chart, data-visualization, analytics -->
<!-- @components: line-chart, segmented-control, stat-display, chart-tooltip, status-bar -->
<!-- @use-cases: crypto-wallet, stock-portfolio, investment-tracking, financial-analytics, performance-monitoring -->
<!-- @related-blocks: Block#29-social-program-card, Block#30-movie-event-card -->
<!-- @keywords: график, финансы, дашборд, аналитика, портфолио, инвестиции, криптовалюта, акции -->

Готовый блок финансового дашборда с графиком производительности аккаунта, извлеченный из Flutter приложения FinanceLight. Это целостный UI-блок для отображения финансовых метрик, графика изменения стоимости и выбора временного диапазона.

**🔧 Гибкость блока**: Блок модульный и может быть адаптирован для различных финансовых приложений. Можно изменять метрики (Account Value, Market Gain/Loss), добавлять дополнительные показатели, менять временные диапазоны (1D, 1M, 3M, 1Y, All time), стилизовать график под разные типы данных (линейный, area chart, candlestick для акций).

#### 📍 Куда подходит этот блок:

**Основное применение:**
1. **Crypto Wallet Apps** - отображение баланса кошелька и изменения стоимости портфеля
2. **Stock Trading Apps** - просмотр performance акционного портфеля
3. **Investment Platforms** - tracking инвестиционных доходов
4. **Banking Apps** - отображение баланса счета и истории транзакций
5. **Analytics Dashboards** - любые финансовые или числовые метрики с графиками

**Переиспользуемые компоненты:**
- **Line Chart Component** → Можно использовать отдельно в любых блоках с данными
- **Segmented Control** → Переключатель периодов времени (используется в Block#31:3207)
- **Stat Display Card** → Отображение метрик с заголовком и значением
- **Chart Tooltip** → Всплывающая подсказка для отображения точного значения на графике

**Связанные блоки:**
- Block #29 (Social Program Card) - схожая структура header с иконками навигации
- Block #30 (Movie/Event Card) - похожий pattern использования badges и info rows

#### Общая структура блока:

**Main Container:**
- **Width**: 375px (mobile)
- **Height**: 587px
- **Background**: #4141E6 (color-accent) - фирменный синий
- **Border Radius**: 30px (radius-card-large)
- **Clip**: antiAlias

#### 1. Status Bar (iOS-style)

**Status Bar:**
- **Width**: 375px
- **Height**: 44px
- **Position**: Top of block
- **Purpose**: iOS status bar для full-screen модалов или standalone экранов

**🔧 Гибкость**: Можно скрыть для Android или web версий

#### 2. Header Section (Title with Navigation)

**Header Container:**
- **Width**: 375px
- **Height**: 44px
- **Padding**: Horizontal 10px
- **Position**: Below status bar (top 44px)

**Leading Icon Button (Left):**
- **Size**: 24×24px icon container
- **Padding**: 16px horizontal, 10px vertical (total 56×44px touch target)
- **Icon**: 24×24px (back arrow or menu)
- **Border Radius**: 12px
- **Background**: Transparent

**Title:**
- **Text**: "Performance" (example)
- **Width**: 239px (center area)
- **Font**: Archivo
- **Font Size**: 16px (font-size-base)
- **Font Weight**: 700 (bold)
- **Color**: White (#FFFFFF)
- **Alignment**: Center
- **Line Height**: 1.40

**Trailing Icon Button (Right):**
- **Size**: 24×24px icon container
- **Padding**: 16px horizontal, 10px vertical (total 56×44px touch target)
- **Icon**: 24×24px (settings, more, or info)
- **Border Radius**: 12px
- **Background**: Transparent

**🔧 Гибкость**: Иконки могут быть любыми (back, close, menu, settings, info, share)

#### 3. Account Value Display (Primary Metric)

**Metric Container:**
- **Width**: 375px
- **Padding**: Horizontal 16px, Top 20px, Vertical 10px
- **Alignment**: Center

**Label:**
- **Text**: "Account Value" (example)
- **Width**: 160px
- **Font**: Archivo
- **Font Size**: 14px (font-size-sm)
- **Font Weight**: 400 (normal)
- **Color**: White (#FFFFFF)
- **Alignment**: Center
- **Line Height**: 1.40

**Value:**
- **Text**: "$28.98" (example)
- **Width**: 160px
- **Font**: Archivo
- **Font Size**: 32px (font-size-2xl-plus)
- **Font Weight**: 700 (bold)
- **Color**: White (#FFFFFF)
- **Alignment**: Center
- **Line Height**: 1.40

**🔧 Гибкость**: Можно отображать любую основную метрику (Balance, Net Worth, Total Value, Portfolio)

#### 4. Market Gain/Loss Section (Secondary Metric with Navigation)

**Section Container:**
- **Width**: 375px
- **Height**: 44px
- **Padding**: Horizontal 32px, Vertical 10px
- **Position**: Below Account Value (top 193px)

**Leading Navigation Icon:**
- **Container**: 24×24px
- **Padding**: 16px horizontal, 10px vertical (total touch target)
- **Background**: rgba(9, 16, 29, 0.1) - 10% opacity black (#1909101D)
- **Border Radius**: 100px (circular)
- **Icon**: 16×16px (chevron left or arrow)

**Metric Display (Center):**
- **Width**: 215px (expanded, takes available space)
- **Padding**: Horizontal 16px, Vertical 10px
- **Alignment**: Center

**Change Value:**
- **Text**: "+$1.47 (+0.63%)" (example)
- **Width**: 215px
- **Font**: Archivo
- **Font Size**: 13px (font-size-xs-plus)
- **Font Weight**: 600 (semibold)
- **Color**: White (#FFFFFF)
- **Alignment**: Center
- **Line Height**: 1.40

**Change Label:**
- **Text**: "Market Gain/Loss" (example)
- **Width**: 215px
- **Font**: Archivo
- **Font Size**: 10px (font-size-2xs)
- **Font Weight**: 400 (normal)
- **Color**: White (#FFFFFF)
- **Alignment**: Center
- **Line Height**: 1.40

**Trailing Navigation Icon:**
- **Container**: 24×24px
- **Padding**: 16px horizontal, 10px vertical
- **Background**: rgba(9, 16, 29, 0.1) - 10% opacity black
- **Border Radius**: 100px (circular)
- **Icon**: 16×16px (chevron right or arrow)

**🔧 Гибкость**:
- Change value цвет может быть динамическим (зеленый для прибыли, красный для убытка)
- Можно добавить дополнительные метрики (ROI, Annual Return, etc.)
- Navigation icons опциональны (для просмотра разных метрик или периодов)

#### 5. Performance Chart (Line Chart with Tooltip)

**Chart Container:**
- **Width**: 375px
- **Height**: 260px
- **Padding**: Horizontal 16px, Vertical 20px
- **Position**: Below Market Gain/Loss (top 257px)
- **Clip**: antiAlias

**Chart Line:**
- **Type**: Line chart (linear gradient path)
- **Width**: Responsive within container
- **Height**: 260px
- **Stroke**: 1px white line
- **Rotation**: -90° (vertical orientation, rotated to horizontal)
- **Position**: Right side of container (left 268px for vertical line)

**Chart Tooltip (Hover/Tap State):**
- **Position**: Left 248px, Top 257px (follows chart line on interaction)
- **Container**: Auto width × 30.16px height
- **Padding**: Horizontal 10px, Vertical 5px
- **Background**: #09101D (color-text-primary) - темный
- **Border Radius**: 8px (radius-sm)

**Tooltip Content:**
- **Value**: "$24.24" (example)
  - Font: Archivo 11px (font-size-2xs-plus) semibold
  - Color: White (#FFFFFF)
  - Line Height: 1.40
- **Time**: "12:45 PM" (example)
  - Font: Archivo 10px (font-size-2xs) normal
  - Color: White (#FFFFFF)
  - Line Height: 1.40
- **Alignment**: Center
- **Format**: Rich text with line break between value and time

**🔧 Гибкость**:
- Chart type может быть изменен (line, area, candlestick, bar)
- Можно добавить grid lines для лучшей читаемости
- Multiple lines для сравнения нескольких активов
- Tooltip может показывать дополнительные данные (volume, high/low, change)
- Chart может быть интерактивным (zoom, pan, pinch to zoom)

#### 6. Time Range Selector (Segmented Control)

**Selector Container:**
- **Width**: 375px
- **Padding**: Horizontal 16px, Vertical 20px
- **Position**: Bottom section (top 517px)

**Segmented Control:**
- **Container Padding**: 3px all sides
- **Background**: rgba(9, 16, 29, 0.1) - 10% opacity black (#1909101D)
- **Border Radius**: 10px (radius-lg-plus)
- **Layout**: Horizontal row with 5 equal segments

**Segment Button (×5):**
- **Height**: 24px
- **Padding**: Horizontal 6px
- **Spacing**: 10px gap between segments
- **Border Radius**: 10px (для selected), 11px (для unselected)
- **Font**: Archivo 11px (font-size-2xs-plus) semibold
- **Line Height**: 1.40

**Segment States:**

1. **Selected (Active) - "1D":**
   - **Background**: White (#FFFFFF)
   - **Text Color**: #23262B (color-text-dark)
   - **Border Radius**: 10px

2. **Unselected (Inactive) - "1M", "3M", "1Y", "All time":**
   - **Background**: Transparent
   - **Text Color**: White (#FFFFFF)
   - **Border Radius**: 11px

**Time Range Options:**
- **1D** - One Day (24 hours)
- **1M** - One Month (30 days)
- **3M** - Three Months (90 days)
- **1Y** - One Year (365 days)
- **All time** - Complete history

**🔧 Гибкость**:
- Количество segments от 3 до 7 (1H, 1D, 1W, 1M, 3M, 6M, 1Y, All)
- Можно добавить custom date range picker
- Можно заменить на dropdown для экономии пространства
- Labels можно локализовать (1D/1Д, 1M/1М, etc.)

#### Complete Block Layout:

```
┌─────────────────────────────────────────┐
│ ▓▓▓▓▓▓▓▓ Status Bar ▓▓▓▓▓▓▓▓▓▓▓▓        │ 44px (#4141E6 bg)
├─────────────────────────────────────────┤
│ [←]      Performance              [⋮]   │ 44px Header
├─────────────────────────────────────────┤
│                                          │
│           Account Value                  │ 20px padding
│              $28.98                      │ Primary metric
│                                          │
├─────────────────────────────────────────┤
│ [◄]    +$1.47 (+0.63%)          [►]     │ Secondary metric
│         Market Gain/Loss                 │ with navigation
├─────────────────────────────────────────┤
│                                          │
│                                   [$24.24│ 260px Chart
│              ╱╲    ╱╲            12:45PM]│ with tooltip
│         ╱╲  ╱  ╲  ╱  ╲  ╱               │
│    ╱╲  ╱  ╲╱    ╲╱    ╲╱                │
│───╱──╲╱──────────────────────────────│  │ White line
│                                          │
├─────────────────────────────────────────┤
│ ┌───────────────────────────────────┐   │
│ │ [1D] [1M] [3M] [1Y] [All time]    │   │ 24px Segmented
│ └───────────────────────────────────┘   │ Control
└─────────────────────────────────────────┘

Container: 375×587px
Background: #4141E6
Border Radius: 30px
All text: White on colored background
```

#### Spacing Summary:

- **Container**: 375×587px, 30px border radius
- **Status Bar**: 44px height
- **Header**: 44px height, 10px horizontal padding
- **Account Value**: 20px top padding, 16px horizontal padding
- **Market Gain/Loss**: 32px horizontal padding, 10px vertical padding
- **Navigation Icons**: 24×24px, rgba(9,16,29,0.1) background, 100px radius
- **Chart Area**: 260px height, 16px horizontal padding, 20px vertical padding
- **Chart Tooltip**: 8px border radius, 10px horizontal padding, 5px vertical padding
- **Segmented Control**: 20px vertical padding, 16px horizontal padding, 3px internal padding
- **Segment Buttons**: 24px height, 6px horizontal padding, 10px gap

#### Typography Summary:

- **Header Title**: 16px bold white (Archivo)
- **Account Label**: 14px normal white (Archivo)
- **Account Value**: 32px bold white (Archivo)
- **Change Value**: 13px semibold white (Archivo)
- **Change Label**: 10px normal white (Archivo)
- **Tooltip Value**: 11px semibold white (Archivo)
- **Tooltip Time**: 10px normal white (Archivo)
- **Segment Text**: 11px semibold (white/dark based on state) (Archivo)

#### Color Palette:

**Primary Background:**
- **#4141E6** - color-accent (main container background)

**Text & Icons:**
- **#FFFFFF** - White (all text and icons on colored background)
- **#23262B** - color-text-dark (selected segment text)

**Overlays:**
- **rgba(9, 16, 29, 0.1)** - 10% opacity black for navigation icons and segmented control background

**Tooltip:**
- **#09101D** - color-text-primary (tooltip background)

#### Use Cases:

1. **Cryptocurrency Wallets**: Bitcoin/Ethereum wallet balance tracking with price charts
2. **Stock Trading Apps**: Portfolio performance visualization with market data
3. **Investment Platforms**: Track ROI and investment growth over time
4. **Banking Apps**: Account balance history and transaction analytics
5. **Savings Apps**: Savings goal progress with historical data
6. **Budget Trackers**: Income/expense trends over different periods
7. **Revenue Dashboards**: Business revenue tracking for SaaS or e-commerce
8. **Analytics Platforms**: Any numerical metric with time-series data

#### Best Practices:

**Flexibility & Extensibility:**
- Chart type is interchangeable (line, area, candlestick, bar chart)
- Metrics can be customized (replace Account Value with any KPI)
- Time ranges are configurable (add/remove periods like 1H, 1W, 6M)
- Can add multiple metrics row (display 2-4 key metrics instead of one)
- Navigation icons optional (remove if no additional views needed)
- Color scheme adaptable (change #4141E6 to brand color)

**Responsive Behavior:**
- Fixed 375px width for mobile (scale proportionally for tablet/desktop)
- Chart maintains aspect ratio when scaled
- Segmented control adapts to available width (equal distribution)
- Tooltip follows touch/hover position on chart
- All touch targets meet 44px minimum (icons have padding)

**Interactive States:**
- **Chart**: Tap or hover to show tooltip with exact value and time
- **Segmented Control**: Tap segment to change time range, chart updates
- **Navigation Icons**: Tap to cycle through different metrics or views
- **Header Icons**: Back/close navigation, settings, or info modal
- **Smooth Transitions**: 200-300ms ease-in-out for state changes

**Data Visualization:**
- White line chart provides high contrast on colored background
- Tooltip appears on demand, doesn't clutter the view
- Time range selector gives quick access to different zoom levels
- Primary metric (large value) draws attention immediately
- Secondary metric provides additional context
- Chart fills available space for maximum readability

**Accessibility:**
- All interactive elements have 44×44px minimum touch targets
- High contrast white text on #4141E6 background
- Chart tooltip has dark background (#09101D) for readability
- Selected segment has clear visual distinction (white background)
- Semantic labels for screen readers ("Account Value", "Market Gain/Loss")
- Chart data should be available in alternative format (table, list)

**Design Tokens Used:**
- Colors: #4141E6, #FFFFFF, #09101D, #23262B, rgba(9,16,29,0.1)
- Border Radius: 8px, 10px, 11px, 12px, 30px, 100px
- Font Sizes: 10px, 11px, 13px, 14px, 16px, 32px
- Font Weights: 400 (normal), 600 (semibold), 700 (bold)
- Spacing: 3px, 5px, 6px, 10px, 16px, 20px, 32px
- Line Heights: 1.40 (consistent across all text)

**Common Modifications:**

**Metrics Enhancements:**
- **Add Multiple Metrics Row**: Show 3-4 key metrics in a grid below Account Value
- **Add Percentage Change Badge**: Color-coded badge (green/red) next to change value
- **Add Comparison Baseline**: Show "vs. yesterday" or "vs. last month" comparison
- **Add Goal Indicator**: Show target value or goal progress bar

**Chart Enhancements:**
- **Add Grid Lines**: Horizontal lines for value reference
- **Add Area Fill**: Fill under line with gradient for visual weight
- **Add Multiple Lines**: Compare multiple assets or metrics
- **Add Zoom Controls**: Pinch to zoom, pan chart horizontally
- **Add Volume Bars**: Show trading volume below main chart
- **Add Technical Indicators**: Moving averages, Bollinger bands, RSI

**Time Range Enhancements:**
- **Add Custom Date Picker**: "Custom" button opens date range picker
- **Add Quick Filters**: "Today", "This Week", "This Month" presets
- **Add Comparison Mode**: "Compare to last period" toggle
- **Add Hour View**: Intraday chart with hourly data

**Navigation Enhancements:**
- **Add Asset Switcher**: Navigate between different currencies/stocks
- **Add Period Comparison**: Show overlay of previous period
- **Add Notifications Badge**: Indicator for alerts or updates
- **Add Quick Actions**: Buy/Sell buttons in header

**Additional Features:**
- **Add News Feed**: Latest news affecting the asset below chart
- **Add Transaction History**: List of recent transactions
- **Add Holdings Breakdown**: Pie chart or list of assets
- **Add Performance Summary**: Daily/Weekly/Monthly/Yearly summary cards
- **Add Price Alerts**: Set alert thresholds with notification toggle

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

**Текущая версия**: v5.11.0

### Changelog

#### v5.11.0 (2025-11-19)
- Добавлен готовый **UI-блок** из Flutter приложения FinanceLight (Finance Dashboard with Performance Chart)
- **Новый формат документации**: Добавлены навигационные метки для IDE AI
- Block #31: Finance Dashboard with Performance Chart (Complete Block):
  - Финансовый дашборд с графиком производительности аккаунта (375×587px, #4141E6 background)
  - Включает 6 секций: Status Bar (44px), Header (44px), Account Value Display, Market Gain/Loss, Performance Chart (260px), Time Range Selector
  - **📍 Куда подходит блок**: Детальная секция с 5 основными применениями (Crypto Wallet, Stock Trading, Investment, Banking, Analytics)
  - **Переиспользуемые компоненты**: Line Chart, Segmented Control, Stat Display Card, Chart Tooltip
- Навигационные метки для IDE AI:
  - @block-id: finance-dashboard
  - @category: finance, dashboard, chart, data-visualization, analytics
  - @components: line-chart, segmented-control, stat-display, chart-tooltip, status-bar
  - @use-cases: crypto-wallet, stock-portfolio, investment-tracking, financial-analytics, performance-monitoring
  - @related-blocks: Block#29, Block#30
  - @keywords: график, финансы, дашборд, аналитика, портфолио, инвестиции, криптовалюта, акции
- Добавлен новый design token:
  - Background overlay: rgba(9, 16, 29, 0.1) - 10% opacity black для navigation icons и segmented control
- Компоненты блока:
  - **Header**: Title "Performance" (16px bold white) с navigation icons (24×24px)
  - **Account Value**: Label (14px) + Value "$28.98" (32px bold), centered
  - **Market Gain/Loss**: Change "+$1.47 (+0.63%)" (13px semibold) + Label (10px) + Navigation icons (rgba black 10%)
  - **Performance Chart**: 260px height, white line chart, tooltip "$24.24 / 12:45 PM" (#09101D bg, 8px radius)
  - **Segmented Control**: 5 segments (1D, 1M, 3M, 1Y, All time), 24px height, 10px radius container
- Segment states:
  - Selected: White background (#FFFFFF), dark text (#23262B)
  - Unselected: Transparent background, white text
- Interactive features:
  - Chart tooltip on hover/tap with value and timestamp
  - Segmented control для выбора временного диапазона
  - Navigation icons для переключения метрик
- Spacing:
  - Container: 30px border radius
  - Header/Account Value: 20px top padding
  - Market Gain/Loss: 32px horizontal padding
  - Chart: 16px horizontal, 20px vertical padding
  - Segmented Control: 3px internal padding, 6px segment padding
- Typography:
  - Header: 16px bold, Account Label: 14px normal, Account Value: 32px bold
  - Change: 13px semibold, Label: 10px normal
  - Tooltip: 11px semibold value + 10px normal time
  - Segments: 11px semibold
- Color Palette:
  - Primary: #4141E6 (container background)
  - Text: White (#FFFFFF) для всех элементов на цветном фоне
  - Overlay: rgba(9,16,29,0.1) для icons и control
  - Tooltip: #09101D (dark background)
- Common Modifications (17 модификаций):
  - Metrics: Multiple metrics row, percentage badge, comparison baseline, goal indicator
  - Chart: Grid lines, area fill, multiple lines, zoom controls, volume bars, technical indicators
  - Time Range: Custom date picker, quick filters, comparison mode, hour view
  - Navigation: Asset switcher, period comparison, notifications, quick actions
  - Features: News feed, transaction history, holdings breakdown, performance summary, price alerts
- Документированы 8 use cases (Crypto Wallets, Stock Trading, Investment, Banking, Savings, Budget Trackers, Revenue Dashboards, Analytics)
- Best Practices для блока:
  - Flexible chart types (line, area, candlestick, bar)
  - Customizable metrics и time ranges
  - Responsive (375px mobile → tablet/desktop scaling)
  - Interactive states (chart tooltip, segmented control, navigation)
  - Data visualization с high contrast white on color
  - Accessibility (44px touch targets, semantic labels, alternative data formats)
- ASCII-диаграмма полной структуры блока с графиком и элементами управления

#### v5.10.0 (2025-11-19)
- Добавлен готовый **UI-блок** из Flutter приложения CardsLight (Movie/Event Card)
- Block #30: Movie/Event Card (Complete Block):
  - Карточка фильма/события с постером, информацией о сеансах и бронированием
  - Включает 6 секций: Container, Poster (343×290px), Content Overlay, Badges Row, Info Row, Time Slots
  - **🔧 Гибкость блока**: Количество элементов настраивается (2-10+ time slots, 1-5+ genre badges, 1+ cards)
- Добавлен новый design token:
  - Text Dark 2: #2A2B2F (color-text-dark-2) для темного текста на светлых кнопках (time slot buttons)
- Структура блока:
  - Main Container: 375px width, 30px vertical padding, white background, 30px radius
  - Poster Section: 343×290px с gradient overlay (transparent → black), action icon 28×28px
  - Content Overlay: Title (16px bold white), Description (14px normal white, 2 lines max)
  - Badges Row: Rating badge (#11BB8D, 24px height), Genre badges (#23262B, 24px height)
  - Info Row: Distance (15px semibold #747B84), Location (16px bold #09101D), Date (16px bold #09101D)
  - Time Slots: 4 buttons default (36px height, #F4F6F9 background, #2A2B2F text, 15px radius)
- Interactive states для time slots:
  - Default: #F4F6F9 background, #2A2B2F text
  - Selected: #09101D background, white text
  - Disabled/Sold Out: #D9DDE2 background, #747B84 text
- Spacing:
  - Container padding: 16px horizontal, 30px vertical
  - Poster: 15px border radius
  - Cards gap: 20px between multiple cards
  - Info/Slots rows: 10px top padding, 10px gaps
- Typography:
  - Title: 16px bold white, Description: 14px normal white
  - Badges: 11px semibold white
  - Info: 15-16px semibold/bold #09101D/#747B84
  - Time slots: 11px semibold #2A2B2F
- Common Modifications:
  - Add price, duration, age rating, seat availability
  - Add director/cast, 3D/IMAX badges, booking status
  - Add multi-day schedule, trailer preview, user rating
- Документированы 6 use cases (Cinema, Theater, Sports, Conferences, Exhibitions, Online Events)
- Best Practices для блоков:
  - Flexible time slots (2-10+) с horizontal scroll
  - Rating badge color changes based on score (8.0+: green, 6.0-7.9: orange, <6.0: red)
  - Responsive behavior (343px mobile → scalable for tablet)
  - Interactive states (hover, selected, disabled) с 200ms transitions
  - Accessibility (44px touch targets, clear contrast, gradient readability)
- ASCII-диаграмма полной структуры блока с двумя карточками

#### v5.9.0 (2025-11-19)
- Добавлен первый готовый **UI-блок** из Flutter приложения SocialLight (Social Program Card)
- **Новый подход**: Документирование целостных блоков дизайна, а не отдельных компонентов
- Block #29: Social Program Card (Complete Block):
  - Полноэкранная карточка социальной программы/курса для модального окна
  - Включает 9 секций: Status Bar, Top Decoration, Drag Handle, Header, Image Gallery, Profile Avatar, Title, Participants Row, Action Buttons
  - **🔧 Гибкость блока**: Количество элементов настраивается (1+4 или 1+6 изображений, 3-20+ аватаров, 2-3 кнопки)
- Структура блока:
  - Status Bar: 375×44px, #09101D, iOS-style для полноэкранных модалов
  - Top Decoration: 343×10px, #D9DDE2, radius 10px (top only)
  - Drag Handle: 40×3px, #D9DDE2, radius 100px, centered
  - Header: 44px height, username "@crossfit" 16px bold, leading icon 24×24px
  - Image Gallery: 176px height, 1 large (166.5×171px) + 4 small grid (78.25×80.5px each), radius 20px, spacing 10px
  - Profile Avatar: 56×56px with "Trainer" badge (#4141E6, 10px semibold)
  - Title: "Intro to Crossfit on Bali" 18px bold, center aligned
  - Subtitle: "4 weeks ・ 5.042 members" 12px normal, center aligned
  - Participants: 7 avatars (2 with Live badges, 1 with active border, 4 regular)
  - Buttons: Primary "Join program" (#09101D, 36px, 13px semibold) + Icon button (#F4F6F9, 16×16px icon)
- Гибкость и расширяемость:
  - Gallery: 1+4 (default), 1+6 (3×2), или single image
  - Avatars: от 3 до неограниченного с horizontal scroll, "+25 more" badge
  - Buttons: 2-3 action buttons, состояния (Join/Joined/Continue)
  - Metadata: price, rating, progress, countdown, capacity
- Best Practices для блоков:
  - Модульная структура с возможностью добавления/удаления секций
  - Responsive behavior (375px mobile → 768px tablet)
  - Interactive states (drag to dismiss, tap gallery, tap avatars)
  - Accessibility (44px touch targets, semantic badges, clear CTAs)
- Документированы 6 use cases и common modifications для адаптации блока
- ASCII-диаграмма полной структуры блока с размерами

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
