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
/* Основной цвет бренда */
--color-primary: #4141E6;
--color-primary-hover: #2563EB;
--color-primary-active: #1D4ED8;
--color-primary-light: #DBEAFE;
--color-primary-dark: #1E40AF;

/* Вторичный цвет */
--color-secondary: #7B61FF;
--color-secondary-hover: #7C3AED;
--color-secondary-active: #6D28D9;
```

### Semantic Colors

```css
/* Success / Trend Up */
--color-success: #11BB8D;
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
```

### Neutral Colors

```css
/* Text */
--color-text-primary: #09101D;
--color-text-secondary: #747B84;
--color-text-tertiary: #9CA3AF;
--color-text-disabled: #D1D5DB;
--color-text-inverse: #FFFFFF;

/* Backgrounds */
--color-bg-primary: #FFFFFF;
--color-bg-secondary: #F4F6F9;
--color-bg-tertiary: #F3F4F6;
--color-bg-elevated: #FFFFFF;
--color-bg-overlay: rgba(0, 0, 0, 0.5);

/* Stroke / Borders */
--color-border-primary: #E5E7EB;
--color-border-secondary: #D1D5DB;
--color-border-focus: #3B82F6;
--color-border-disabled: #F3F4F6;

/* Shades */
--color-gray-50: #F9FAFB;
--color-gray-100: #F4F6F9;
--color-gray-200: #E5E7EB;
--color-gray-300: #D9DDE2;
--color-gray-400: #9CA3AF;
--color-gray-500: #6B7280;
--color-gray-600: #4B5563;
--color-gray-700: #414249;
--color-gray-800: #23262B;
--color-gray-900: #09101D;
```

### Accent & Decorative Colors

```css
/* Accent colors из View4 */
--color-accent-orange: #FFC043;
--color-accent-orange-light: rgba(255, 192, 67, 0.2);  /* #33FFC043 - 20% opacity */
--color-accent-brown: #905846;
--color-accent-teal: #4E9381;

/* Badge backgrounds */
--color-badge-light: #EAEEF2;
--color-badge-dark: #2A2B2F;

/* Stories colors */
--color-stories-ring-purple: #833AB4;  /* Для непрочитанных stories (Instagram-like) */
--color-stories-ring-primary: #4141E6; /* Для активных/просмотренных stories */
--color-live-red: #FD1D1D;             /* Для Live индикатора */
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

/* Градиент для оверлея изображений (View4) */
--gradient-image-overlay: linear-gradient(180deg, rgba(0, 0, 0, 0) 0%, rgba(0, 0, 0, 1) 100%);

/* Градиент для Stories Live badge (Instagram-like) */
--gradient-stories-live: linear-gradient(90deg, #833AB4 0%, #FD1D1D 50%, #FCB045 100%);
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
--font-primary: 'Archivo', -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Oxygen', 'Ubuntu', 'Cantarell', 'Fira Sans', 'Droid Sans', 'Helvetica Neue', sans-serif;
--font-secondary: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
--font-mono: 'JetBrains Mono', 'Fira Code', 'Monaco', 'Consolas', 'Courier New', monospace;
--font-display: 'Archivo', sans-serif;  /* Для заголовков и акцентов */
```

### Font Sizes

```css
--font-size-10: 0.625rem;      /* 10px - для Live badge */
--font-size-11: 0.6875rem;     /* 11px - для badge текста */
--font-size-xs: 0.75rem;       /* 12px */
--font-size-13: 0.8125rem;     /* 13px - для мелких subtitle */
--font-size-sm: 0.875rem;      /* 14px */
--font-size-15: 0.9375rem;     /* 15px - для subtitle */
--font-size-base: 1rem;        /* 16px */
--font-size-md: 1.125rem;      /* 18px */
--font-size-lg: 1.25rem;       /* 20px */
--font-size-xl: 1.5rem;        /* 24px */
--font-size-2xl: 1.875rem;     /* 30px */
--font-size-3xl: 2.25rem;      /* 36px */
--font-size-4xl: 3rem;         /* 48px */
--font-size-5xl: 3.75rem;      /* 60px */
--font-size-6xl: 4.5rem;       /* 72px - Display/Elevations заголовки */
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
--line-height-tight: 1.25;
--line-height-snug: 1.375;
--line-height-normal: 1.5;
--line-height-relaxed: 1.625;
--line-height-loose: 2;
```

### Text Styles

#### Headings

- **H1**: Font: 48px/3rem, Weight: 700 (Bold), Line Height: 1.2, Letter Spacing: -0.02em
- **H2**: Font: 36px/2.25rem, Weight: 700 (Bold), Line Height: 1.25, Letter Spacing: -0.01em
- **H3**: Font: 30px/1.875rem, Weight: 600 (Semibold), Line Height: 1.3, Letter Spacing: -0.01em
- **H4**: Font: 24px/1.5rem, Weight: 600 (Semibold), Line Height: 1.35, Letter Spacing: 0
- **H5**: Font: 20px/1.25rem, Weight: 600 (Semibold), Line Height: 1.4, Letter Spacing: 0
- **H6**: Font: 18px/1.125rem, Weight: 600 (Semibold), Line Height: 1.45, Letter Spacing: 0

#### Body Text

- **Body Large**: Font: 18px/1.125rem, Weight: 400 (Normal), Line Height: 1.625
- **Body**: Font: 16px/1rem, Weight: 400 (Normal), Line Height: 1.5
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
--space-0: 0;
--space-1: 0.25rem;    /* 4px */
--space-1-25: 0.3125rem; /* 5px - мелкие отступы */
--space-1-5: 0.375rem; /* 6px - мелкие отступы */
--space-2: 0.5rem;     /* 8px */
--space-2-5: 0.625rem; /* 10px - между элементами */
--space-3: 0.75rem;    /* 12px */
--space-4: 1rem;       /* 16px */
--space-5: 1.25rem;    /* 20px */
--space-6: 1.5rem;     /* 24px */
--space-8: 2rem;       /* 32px */
--space-10: 2.5rem;    /* 40px */
--space-12: 3rem;      /* 48px */
--space-12-5: 3.125rem; /* 50px - NavBar spacing */
--space-16: 4rem;      /* 64px */
--space-20: 5rem;      /* 80px */
--space-22-5: 5.625rem; /* 90px - Stories avatars spacing */
--space-24: 6rem;      /* 96px */
--space-25: 6.25rem;   /* 100px - основной padding */
```

### Border Radius

```css
--radius-none: 0;
--radius-sm: 0.125rem;      /* 2px */
--radius-base: 0.25rem;     /* 4px */
--radius-md: 0.375rem;      /* 6px */
--radius-lg: 0.5rem;        /* 8px */
--radius-10: 0.625rem;      /* 10px - для небольших элементов */
--radius-xl: 0.75rem;       /* 12px */
--radius-15: 0.9375rem;     /* 15px - для NavBar карточек */
--radius-2xl: 1rem;         /* 16px */
--radius-20: 1.25rem;       /* 20px - для индикаторов */
--radius-3xl: 1.875rem;     /* 30px - для карточек с elevations */
--radius-40: 2.5rem;        /* 40px - для аватаров */
--radius-80: 5rem;          /* 80px - для больших контейнеров */
--radius-4xl: 6.25rem;      /* 100px - для основных контейнеров */
--radius-full: 9999px;
```

### Shadows

#### Elevations (7 уровней)

```css
/* Elevation Level 1 */
--shadow-elevation-1: 0 1px 1px 0 rgba(0, 0, 0, 0.4);

/* Elevation Level 2 */
--shadow-elevation-2: 0 2px 10px 0 rgba(0, 0, 0, 0.1);

/* Elevation Level 3 */
--shadow-elevation-3: 0 10px 30px 0 rgba(0, 0, 0, 0.05);

/* Elevation Level 4 */
--shadow-elevation-4: 0 10px 20px 0 rgba(0, 0, 0, 0.2);

/* Elevation Level 5 */
--shadow-elevation-5: 0 15px 60px 0 rgba(0, 0, 0, 0.2);

/* Elevation Level 6 */
--shadow-elevation-6: 0 17.5px 70px 0 rgba(0, 0, 0, 0.25);

/* Elevation Level 7 */
--shadow-elevation-7: 0 35px 90px 0 rgba(0, 0, 0, 0.25);
```

#### Алиасы для удобства

```css
--shadow-xs: var(--shadow-elevation-1);
--shadow-sm: var(--shadow-elevation-2);
--shadow-base: var(--shadow-elevation-3);
--shadow-md: var(--shadow-elevation-4);
--shadow-lg: var(--shadow-elevation-5);
--shadow-xl: var(--shadow-elevation-6);
--shadow-2xl: var(--shadow-elevation-7);
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

#### Elevation Card (с тенями)

- **Size**: 160px × 160px (квадратная карточка)
- **Border Radius**: 30px (radius-3xl)
- **Background**: Поддерживает различные фоны (white, gray-100, gray-300, gray-700, gray-800)
- **Shadows**: 7 уровней elevation (от shadow-elevation-1 до shadow-elevation-7)
- **Использование**: Для демонстрации глубины и иерархии в интерфейсе

#### Content Cards (View4)

Карточки для отображения контента с изображениями, текстом и действиями.

- **Ширина**: 375px (фиксированная для мобильных экранов)
- **Border Radius**: 15px (radius-15)
- **Padding**: 16px (horizontal), 10px (vertical)
- **Варианты высот**:
  - Recipe Card: 355px
  - Hotel Card: 360px
  - Movie Card: 400px
  - Product Card: 531px
- **Компоненты внутри карточек**:
  - Badges: View4 Style (24px height)
  - Buttons: Accent Button (36px height, #FFC043)
  - Images: С градиентным оверлеем (gradient-image-overlay)
  - Text Colors: #2A2B2F (заголовки), #905846 (описание), #4E9381 (цена/особые данные)
  - Icons: 28px для действий
  - Color Picker Dots: 14.40px × 14.40px, border 2px white, radius 20px

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

/* Elevation Card - для демонстрации глубины */
.card--elevation {
  width: 160px;
  height: 160px;
  border-radius: var(--radius-3xl); /* 30px */
  background: var(--color-bg-primary);
}

.card--elevation-1 { box-shadow: var(--shadow-elevation-1); }
.card--elevation-2 { box-shadow: var(--shadow-elevation-2); }
.card--elevation-3 { box-shadow: var(--shadow-elevation-3); }
.card--elevation-4 { box-shadow: var(--shadow-elevation-4); }
.card--elevation-5 { box-shadow: var(--shadow-elevation-5); }
.card--elevation-6 { box-shadow: var(--shadow-elevation-6); }
.card--elevation-7 { box-shadow: var(--shadow-elevation-7); }
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

#### Accent Button (View4 Orange)

- **Size**: Height: 36px, Padding: 10px 16px (vertical 10px, horizontal 16px)
- **Radius**: 15px (radius-15)
- **Font Size**: 18px (font-size-md)
- **Font Weight**: 700 (bold)
- **States**:
  - Default: Background: #FFC043 (color-accent-orange), Color: white
  - Hover: Background: darken(#FFC043, 10%), Transform: translateY(-1px)
  - Active: Transform: translateY(0)

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

#### Badge (View4 Style)

- **Height**: 24px
- **Padding**: 0px 10px (horizontal padding)
- **Radius**: 10px (radius-10)
- **Font Size**: 11px (font-size-11)
- **Font Weight**: 600 (semibold)
- **Variants**:
  - Success: Background: #11BB8D, Color: white
  - Light: Background: #EAEEF2, Color: color-text-primary
  - Dark: Background: #23262B, Color: white
  - Orange (semi-transparent): Background: rgba(255, 192, 67, 0.2), Color: #FFC043
  - Custom: Background: любой цвет, Color: контрастный

#### Badge (Classic Style)

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

#### NavBar Component (44px height)

- **Container**:
  - Padding: 100px (основной контейнер)
  - Border Radius: 80px (radius-80)
  - Background: white
  - Spacing: 50px между секциями

- **Inner Card**:
  - Padding: 50px (horizontal), 40px (vertical)
  - Border Radius: 15px (radius-15)
  - Border: 1px solid #4141E6 (синий) или #7B61FF (фиолетовый)
  - Background: white или #F4F6F9 (secondary background)
  - Spacing: 50px между элементами

- **Item Height**: 44px (стандартная высота для всех элементов)
- **Item Padding**:
  - Horizontal: 16px
  - Vertical: 10px
  - Custom: 10px (top/bottom), 16px (left/right) для иконок

- **Typography**:
  - Title (крупный): 32px, weight 700, line-height 1.40
  - Title (средний): 24px, weight 700, line-height 1.40
  - Title (малый): 16px, weight 700, line-height 1.40
  - Subtitle: 14px, weight 400, line-height 1.40, color #414249 или #747B84
  - Action: 16px, weight 700, color #4141E6
  - Label: 16px, weight 400, color #4141E6
  - Name: 14px, weight 600, line-height 1.40

- **Avatar Sizes**:
  - Large: 40px × 40px (32px image + 4px offset)
  - Small: 32px × 32px (24px image + 4px offset)
  - Border Radius: 40px (круглые)
  - Placeholder: background #D9DDE2

- **Status Indicator**:
  - Size: 12px × 12px
  - Border Radius: 20px
  - Border: 2px-3px solid white
  - Color: #11BB8D (success green)
  - Padding: 4px (horizontal), 2px (vertical)

- **Icon Sizes**:
  - Standard: 24px × 24px
  - Small: 20px × 20px
  - Container padding: 2px

- **Spacing between elements**:
  - Large: 50px
  - Medium: 10px, 8px
  - Small: 6px, 5px

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

- **XS**: 24px × 24px (image 24px + 4px offset в контейнере 32px)
- **Small**: 32px × 32px (image 24px + 4px offset в контейнере 32px)
- **Medium**: 40px × 40px (image 32px + 4px offset в контейнере 40px)
- **Large**: 48px × 48px
- **XL**: 64px × 64px
- **2XL**: 96px × 96px

#### Styles

- **Border Radius**: 40px (radius-40) для круглых аватаров
- **Border**: 2px solid white (для группировки)
- **Placeholder**: Background: #D9DDE2 (color-gray-300), Icon/Initials: color-gray-600
- **Container**: Offset 4px от краев для правильного позиционирования
- **Status Indicator**:
  - Size: 12px × 12px
  - Border: 2px-3px solid white
  - Border Radius: 20px (radius-20)
  - Position: встроен в контейнер аватара
  - Color: #11BB8D (success green)

#### Stories Avatars (Instagram-like)

Компонент для отображения Stories с аватарами пользователей в стиле Instagram.

- **Container**:
  - Width: 500px
  - Height: 266px
  - Padding: 50px (space-12-5)
  - Border: 1px solid #4141E6 (primary) или #7B61FF (secondary)
  - Border Radius: 15px (radius-15)
  - Spacing between avatars: 90px (horizontal, first variant) или 20px (space-5, grid variant)

- **Story Avatar**:
  - Container Size: 56px × 56px
  - Image Size: 48px × 48px (с offset 4px от краев контейнера)
  - Border Radius: 40px (radius-40) для аватара
  - Placeholder: #D9DDE2 (color-gray-300)

- **Story Ring (непрочитанная история)**:
  - Border: 2px solid #833AB4 (stories-ring-purple) - Instagram-like gradient ring
  - Border Radius: 30px
  - Position: вокруг контейнера 56px × 56px

- **Story Ring (активная/просмотренная история)**:
  - Border: 2px solid #4141E6 (stories-ring-primary)
  - Border Radius: 30px

- **Label**:
  - Width: 50px
  - Font: Archivo, 11px (font-size-11), weight 600
  - Color: #09101D (text-primary)
  - Line Height: 1.40
  - Text Align: center
  - Spacing от аватара: 5px (space-1-25)

- **Live Badge** (для живых трансляций):
  - Size: 28px × 14px
  - Padding: 4px (horizontal), 2px (vertical)
  - Border Radius: 12px
  - Border: 1px solid white
  - Background: Linear gradient (#833AB4 → #FD1D1D → #FCB045) - gradient-stories-live
  - Text: "Live", 10px, weight 600, white color
  - Position: внизу аватара (left 0, top 36)

- **List Container**:
  - Width: 375px
  - Padding: 16px (horizontal)
  - Padding: 10px (vertical)
  - Horizontal scroll: enabled
  - Spacing between items: 20px (space-5) или 90px (space-22-5)

**Варианты отображения:**
1. **Centered Row** (3 аватара): spacing 90px
2. **Scrollable Grid** (7+ аватаров): spacing 20px, horizontal padding 16px

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
  - Base: 20px (используется в NavBar)
  - MD: 24px (стандартный размер в NavBar)
  - 28px: 28px (для действий в View4 карточках)
  - LG: 32px
  - XL: 48px
- **Container Padding**: 2px для иконок 24px
- **Stroke Width**: 1.5px (regular), 2px (medium), 2.5px (bold)
- **Style**: Outline (default), Solid (emphasis)
- **Color**: Inherit from parent или explicit (color-text-primary, color-text-secondary)
- **Border Radius**: 100px (radius-full) для круглых контейнеров иконок
- **Positioning**: Offset -2px (top/left) для правильного выравнивания в некоторых случаях

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

**Текущая версия**: v5.0.0

### Changelog

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
