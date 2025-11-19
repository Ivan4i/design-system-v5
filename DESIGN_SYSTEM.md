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

### Real Project Colors (Extracted from Flutter Code)

```css
/* Реальные цвета из проекта - Основные */
--color-bg-dark: #12202F;           /* Color.fromARGB(255, 18, 32, 47) - scaffold background */
--color-bg-light: #F4F6F9;          /* Color(0xFFF4F6F9) - light background */
--color-text-dark: #09101D;         /* Color(0xFF09101D) - dark text and border */
--color-text-gray: #747B84;         /* Color(0xFF747B84) - secondary text color */
--color-white: #FFFFFF;             /* Colors.white */
--color-border-dark: #09101D;       /* Border color dark */
--color-border-purple: #7B61FF;     /* Color(0xFF7B61FF) - purple border/accent */

/* Semantic Colors - Status States */
--color-success: #11BB8D;           /* Color(0xFF11BB8D) - green/success */
--color-success-light: #0AFB6B;     /* Color(0xFF0AFB6B) - light green indicator */
--color-success-overlay: #0C11BB8D; /* Color(0x0C11BB8D) - green with ~5% opacity (0x0C = 12) */
--color-info: #0B24FB;              /* Color(0xFF0B24FB) - blue/info */
--color-info-transparent: #0B24FBCC; /* Color(0xCC0B24FB) - blue with 80% opacity */
--color-error: #E24949;             /* Color(0xFFE24949) - red/error */
--color-warning: #FF9500;           /* Color(0xFFFF9500) - orange/warning */
--color-warning-alt: #FF9F0A;       /* Color(0xFFFF9F0A) - orange alternative */

/* Accent Colors */
--color-accent-orange: #FF6937;     /* Color(0xFFFF6937) - orange accent for labels */
--color-accent-orange-border: #FE5032; /* Color(0xFFFE5032) - orange border for buttons */
--color-accent-purple: #833AB4;     /* Color(0xFF833AB4) - purple/instagram gradient color */
--color-accent-blue: #4141E6;       /* Color(0xFF4141E6) - blue accent */

/* UI Element Colors */
--color-avatar-placeholder: #D9DDE2; /* Color(0xFFD9DDE2) - gray avatar placeholder */
--color-badge-dark: #23262B;        /* Color(0xFF23262B) - dark badge background */

/* Gradient Colors for UI */
--color-gradient-red-start: #EB001B; /* Color(0xFFEB001B) - gradient start (red) */
--color-gradient-pink-end: #DD2476;  /* Color(0xFFDD2476) - gradient end (pink) */

/* Overlay/Gradient Colors */
--color-overlay-start: #00080808;   /* Color(0x00080808) - transparent black (gradient start) */
--color-overlay-end: #7F080808;     /* Color(0x7F080808) - semi-transparent black ~50% (gradient end, 0x7F = 127) */
```

**Использование цветов в проекте:**
- **Backgrounds**: #12202F (dark theme), #F4F6F9 (light containers), #FFFFFF (white cards), #09101D (dark cards), #D9DDE2 (avatar placeholders)
- **Text**: #09101D (primary), #747B84 (secondary/placeholder), #FFFFFF (inverse), #FF6937 (orange accent)
- **Borders**: #09101D (dark), #7B61FF (purple accent), #833AB4 (purple/instagram), #4141E6 (blue), #FE5032 (orange button border), 1-2px width
- **Status Indicators**: #11BB8D (success), #0B24FB (info), #E24949 (error), #FF9500 (warning)
- **Badge dots**: 6×6px oval shapes with status colors
- **Badge backgrounds**: #23262B (dark badge), #E24949 (notification badge)
- **Overlays**: Linear gradients from transparent to semi-transparent black for image overlays
- **Tinted backgrounds**: #0C11BB8D (5% green tint)
- **Story borders**: #833AB4 (purple), #4141E6 (blue) - 2px borders for active stories
- **Button gradients**: #EB001B to #DD2476 (red to pink gradient for CTA buttons)

### Primary Colors

```css
/* Основной цвет бренда */
--color-primary: #3B82F6;
--color-primary-hover: #2563EB;
--color-primary-active: #1D4ED8;
--color-primary-light: #DBEAFE;
--color-primary-dark: #1E40AF;

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
```

### Neutral Colors

```css
/* Text */
--color-text-primary: #111827;
--color-text-secondary: #6B7280;
--color-text-tertiary: #9CA3AF;
--color-text-disabled: #D1D5DB;
--color-text-inverse: #FFFFFF;

/* Backgrounds */
--color-bg-primary: #FFFFFF;
--color-bg-secondary: #F9FAFB;
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
--color-gray-100: #F3F4F6;
--color-gray-200: #E5E7EB;
--color-gray-300: #D1D5DB;
--color-gray-400: #9CA3AF;
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

/* Реальные градиенты из проекта */
--gradient-image-overlay: linear-gradient(180deg, rgba(8, 8, 8, 0) 0%, rgba(8, 8, 8, 0.5) 100%);
/* begin: Alignment(0.50, -0.00), end: Alignment(0.50, 1.00)
   colors: [Color(0x00080808), Color(0x7F080808)]
   Vertical gradient from transparent to 50% black */

--gradient-button-cta: linear-gradient(90deg, #EB001B 0%, #DD2476 100%);
/* begin: Alignment(-1.00, 0.00), end: Alignment(1.00, 0.00)
   colors: [Color(0xFFEB001B), Color(0xFFDD2476)]
   Horizontal gradient from red to pink for CTA/pricing buttons */
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

### Real Project Typography (Extracted from Flutter Code)

```css
/* Реальная типографика из проекта */
--font-project: 'Archivo';          /* fontFamily: 'Archivo' */
--font-size-display: 4.5rem;        /* 72px - fontSize: 72 - Display headers */
--font-size-h1: 2rem;               /* 32px - fontSize: 32 - Large card titles */
--font-size-h2: 1.625rem;           /* 26px - fontSize: 26 - Medium card titles */
--font-size-h3: 1.5rem;             /* 24px - fontSize: 24 - Card headers, section titles */
--font-size-base: 1rem;             /* 16px - fontSize: 16 - Body text, buttons */
--font-size-sm: 0.875rem;           /* 14px - fontSize: 14 - Button text, navigation */
--font-size-small-plus: 0.8125rem;  /* 13px - fontSize: 13 - Small buttons, secondary text */
--font-size-small: 0.75rem;         /* 12px - fontSize: 12 - Status bar, small text */
--font-size-xs: 0.6875rem;          /* 11px - fontSize: 11 - Captions, fine print */
--font-size-xxs: 0.625rem;          /* 10px - fontSize: 10 - Badge counter, tiny text */
--font-weight-ultra: 800;           /* fontWeight: FontWeight.w800 */
--font-weight-bold: 700;            /* fontWeight: FontWeight.w700 */
--font-weight-semibold: 600;        /* fontWeight: FontWeight.w600 */
--font-weight-normal: 400;          /* fontWeight: FontWeight.w400 */
--line-height-tight: 0.70;          /* height: 0.70 - Display headers */
--line-height-compact: 1.33;        /* height: 1.33 - Small text */
--line-height-normal: 1.40;         /* height: 1.40 - Body text, all cards */
--letter-spacing-tight: -0.05em;    /* letterSpacing: -0.05 - Tight spacing */
```

**Использование в проекте:**
- **Display Headers**: Size: 72px, Weight: 800, Line Height: 0.70, Color: #09101D
- **Large Card Titles**: Size: 32px, Weight: 700, Line Height: 1.40, Color: white (on images)
- **Medium Card Titles**: Size: 26px, Weight: 700, Line Height: 1.40, Color: white
- **Card Headers**: Size: 24px, Weight: 700, Line Height: 1.40, Color: white / #09101D
- **Body Text**: Size: 16px, Weight: 400, Line Height: 1.40, Color: white / #747B84
- **Card Labels**: Size: 16px, Weight: 700, Line Height: 1.40, Color: #FF6937 (orange accent)
- **Button Text**: Size: 14px, Weight: 600, Line Height: 1.40, Color: #09101D / white
- **Small Buttons**: Size: 13px, Weight: 600, Line Height: 1.40, Color: #09101D / white
- **Status Bar Time**: Size: 12px, Weight: 600, Line Height: 1.33, Color: #09101D / white
- **Status Bar Text**: Size: 12px, Weight: 400, Line Height: 1.33, Letter Spacing: -0.05
- **Captions**: Size: 11px, Weight: 400, Line Height: 1.40, Color: white
- **Avatar Labels**: Size: 11px, Weight: 600, Line Height: 1.40, Color: #09101D
- **Badge Counter**: Size: 10px, Weight: 600, Line Height: 1.40, Color: white

### Font Family

```css
--font-primary: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Oxygen', 'Ubuntu', 'Cantarell', 'Fira Sans', 'Droid Sans', 'Helvetica Neue', sans-serif;
--font-secondary: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
--font-mono: 'JetBrains Mono', 'Fira Code', 'Monaco', 'Consolas', 'Courier New', monospace;
--font-archivo: 'Archivo', sans-serif;  /* Project-specific font */
```

### Font Sizes

```css
--font-size-xs: 0.75rem;      /* 12px */
--font-size-sm: 0.875rem;     /* 14px */
--font-size-base: 1rem;       /* 16px */
--font-size-md: 1.125rem;     /* 18px */
--font-size-lg: 1.25rem;      /* 20px */
--font-size-xl: 1.5rem;       /* 24px */
--font-size-2xl: 1.875rem;    /* 30px */
--font-size-3xl: 2.25rem;     /* 36px */
--font-size-4xl: 3rem;        /* 48px */
--font-size-5xl: 3.75rem;     /* 60px */
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

### Real Project Spacing (Extracted from Flutter Code)

```css
/* Реальные отступы из проекта */
--space-project-0-75: 0.1875rem; /* 3px - Column spacing (stories label) */
--space-project-1: 0.25rem;     /* 4px - Row spacing, vertical padding, Column spacing */
--space-project-1-25: 0.3125rem; /* 5px - left padding, Column spacing, badge padding */
--space-project-1-75: 0.4375rem; /* 7px - vertical padding */
--space-project-2: 0.5rem;      /* 8px - padding, Row/Column spacing */
--space-project-xs: 0.625rem;   /* 10px - spacing: 10, EdgeInsets.all(10), Row/Column spacing, padding, stories */
--space-project-2-5: 0.75rem;   /* 12px - badge border radius, small element radius */
--space-project-sm: 1rem;       /* 16px - horizontal padding, positioning, icon padding */
--space-project-md: 1.25rem;    /* 20px - padding: 20, all sides */
--space-project-button: 1.875rem; /* 30px - button border radius */
--space-project-lg: 2rem;       /* 32px - padding: 32, all sides */
--space-project-xl: 3.125rem;   /* 50px - container padding, Row/Column gap */
--space-project-2xl: 4.375rem;  /* 70px - Row spacing */
--space-project-3xl: 6.25rem;   /* 100px - padding: 100, Row/Column gap, positioning */
--space-project-4xl: 12.5rem;   /* 200px - top: 200 */
--space-project-5xl: 14.75rem;  /* 236px - Column spacing (for large gaps) */
```

**Использование в проекте:**
- **Micro**: 3px (stories label spacing), 4px (Row/Column spacing), 5px (padding, badge vertical padding), 8px (spacing, padding)
- **Small**: 10px (gap, EdgeInsets, Row/Column spacing, stories), 12px (badge border radius, small elements)
- **Medium**: 16px (horizontal padding, icon padding), 20px (padding all sides, card padding), 30px (button border radius)
- **Large**: 32px (padding all sides), 50px (container padding)
- **XLarge**: 70px (Row spacing between elements), 100px (padding all, Row/Column gap, positioning)
- **XXLarge**: 200px (top positioning), 236px (Column spacing for large gaps)

### Spacing Scale

```css
--space-0: 0;
--space-1: 0.25rem;   /* 4px */
--space-2: 0.5rem;    /* 8px */
--space-2-5: 0.625rem;  /* 10px - Project-specific */
--space-3: 0.75rem;   /* 12px */
--space-4: 1rem;      /* 16px */
--space-5: 1.25rem;   /* 20px */
--space-6: 1.5rem;    /* 24px */
--space-8: 2rem;      /* 32px */
--space-10: 2.5rem;   /* 40px */
--space-12: 3rem;     /* 48px */
--space-16: 4rem;     /* 64px */
--space-20: 5rem;     /* 80px */
--space-24: 6rem;     /* 96px */
--space-25: 6.25rem;  /* 100px - Project-specific */
--space-50: 12.5rem;  /* 200px - Project-specific */
```

### Border Radius

#### Real Project Border Radius (Extracted from Flutter Code)

```css
/* Реальные border radius из проекта */
--radius-project-xs: 0.625rem;        /* 10px - BorderRadius.circular(10) - story images */
--radius-project-xxs: 0.75rem;        /* 12px - BorderRadius.circular(12) - small badges, notification badges */
--radius-project-sm: 0.8125rem;       /* 13px - BorderRadius.circular(13) - story containers with border */
--radius-project-base: 0.9375rem;     /* 15px - BorderRadius.circular(15) - containers, search bars, buttons */
--radius-project-md: 1.25rem;         /* 20px - BorderRadius.circular(20) - cards, images */
--radius-project-button: 1.875rem;    /* 30px - BorderRadius.circular(30) - CTA buttons, pricing buttons */
--radius-project-lg: 2rem;            /* 32px - BorderRadius.circular(32) - badges, pills */
--radius-project-xl: 2.5rem;          /* 40px - BorderRadius.circular(40) - phone container */
--radius-project-2xl: 6.25rem;        /* 100px - BorderRadius.circular(100) - main container, icons */
```

**Использование в проекте:**
- **Story Images**: BorderRadius.circular(10) = 10px radius
- **Small Badges**: BorderRadius.circular(12) = 12px radius (notification badges)
- **Story Containers with Border**: BorderRadius.circular(13) = 13px radius
- **Buttons/Search**: BorderRadius.circular(15) = 15px radius
- **Cards/Images**: BorderRadius.circular(20) = 20px radius (most common for content cards)
- **CTA Buttons**: BorderRadius.circular(30) = 30px radius (pricing buttons, gradient buttons)
- **Badges/Pills**: BorderRadius.circular(32) = 32px radius
- **Phone Container**: BorderRadius.circular(40) = 40px radius
- **Main Container/Icons**: BorderRadius.circular(100) = 100px radius (fully rounded)

#### Standard Border Radius

```css
--radius-none: 0;
--radius-sm: 0.125rem;    /* 2px */
--radius-base: 0.25rem;   /* 4px */
--radius-md: 0.375rem;    /* 6px */
--radius-lg: 0.5rem;      /* 8px */
--radius-xl: 0.75rem;     /* 12px */
--radius-2xl: 1rem;       /* 16px */
--radius-3xl: 2.5rem;     /* 40px - Project-specific */
--radius-4xl: 6.25rem;    /* 100px - Project-specific */
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

### Borders

#### Border Width

##### Real Project Border Width (Extracted from Flutter Code)

```css
/* Реальные border width из проекта */
--border-width-story: 2px;     /* width: 2 - story container border */
--border-width-phone: 15px;    /* width: 15 - phone container border */
```

**Использование в проекте:**
- **Story Border**: width: 2px, strokeAlign: BorderSide.strokeAlignCenter, colors: #833AB4 / #4141E6
- **Phone Container Border**: width: 15px, strokeAlign: BorderSide.strokeAlignOutside, color: #09101D

##### Standard Border Width

```css
--border-width-0: 0;
--border-width-1: 1px;
--border-width-2: 2px;  /* Project-specific - stories */
--border-width-4: 4px;
--border-width-8: 8px;
--border-width-15: 15px;  /* Project-specific - phone */
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

### Real Project Components (Extracted from Flutter Code)

#### Grid Container
- **Size**: 575px × 1112px
- **Background**: white (#FFFFFF)
- **Border Radius**: 100px (circular(100))
- **Clip Behavior**: Clip.antiAlias
- **Description**: Основной контейнер для grid layout

#### Phone/Device Container
- **Size**: 375px × 812px (стандартный размер iPhone)
- **Background**: white (#FFFFFF)
- **Border**: 15px solid #09101D (strokeAlignOutside)
- **Border Radius**: 40px (circular(40))
- **Clip Behavior**: Clip.antiAlias
- **Position**: left: 100px, top: 200px
- **Description**: Контейнер с border для имитации устройства

#### Content Container
- **Size**: 343px × 812px
- **Padding**: 10px (EdgeInsets.all)
- **Clip Behavior**: Clip.antiAlias
- **Position**: left: 16px, top: 0
- **Description**: Внутренний контейнер для контента

#### Grid Title
- **Text**: "Grid"
- **Font**: 'Archivo'
- **Size**: 72px
- **Weight**: 800 (extrabold)
- **Line Height**: 0.70
- **Color**: #09101D
- **Position**: left: 100px, top: 100px
- **Alignment**: crossAxisAlignment: start
- **Spacing**: 10px (gap между элементами колонки)

#### Status Bar Container (iPhone X or Newer)
- **Size**: 950px × 614px
- **Background**: #F4F6F9
- **Border**: 1px solid #7B61FF
- **Border Radius**: 15px (circular(15))
- **Clip Behavior**: Clip.antiAlias
- **Content**: Multiple status bar variants at different positions

#### Status Bar
- **Size**: 375px × 44px (full height) / 375px × 20px (content)
- **Background**: transparent
- **Components**:
  - **Time Display**: "9:41 AM", Font: 'Archivo', Size: 12px, Weight: 600, Color: #09101D / white, Position: center (left: 164px)
  - **Battery Percentage**: "100%", Font: 'Archivo', Size: 12px, Weight: 400, Align: right, Position: right (left: 308-309px)
  - **Carrier Text**: "MTT", Font: 'Archivo', Size: 12px, Weight: 400, Letter Spacing: -0.05, Position: left (left: 4px)
  - **Icons**: 14×14px, spacing: 4px
- **Variants**: Light (dark text #09101D) and Dark (white text)

#### Status Badge/Pill
- **Size**: 54px × 21px
- **Border Radius**: 32px (circular(32))
- **Position**: left: 21px, top: 12px (inside status bar container)
- **Color Variants**:
  - **Success**: #11BB8D (solid background)
  - **Info**: #0B24FBCC (blue with 80% opacity)
  - **Error**: #E24949 (red solid)
  - **Default**: transparent (no background)

#### Status Indicator Dot
- **Size**: 6px × 6px
- **Shape**: OvalBorder() (perfect circle)
- **Position**: left: 298px, top: 8px (inside status bar)
- **Colors**:
  - **Warning**: #FF9500 / #FF9F0A (orange)
  - **Success**: #11BB8D / #0AFB6B (green)

#### Search Bar
- **Container Size**: 375px × 44px
- **Background**: white (#FFFFFF)
- **Input Field**:
  - **Height**: 36px (with 4px vertical padding)
  - **Background**: #F4F6F9
  - **Border Radius**: 15px (circular(15))
  - **Padding**: horizontal: 8px, vertical: 7px
  - **Inner Padding**: left: 5px, right: 10px
  - **Icon**: 14×14px
  - **Placeholder**: "Search", Font: 'Archivo', Size: 16px, Weight: 400, Color: #747B84, Line Height: 1.40
  - **Icon-Text Spacing**: 10px

#### Search Bar with Cancel Button
- **Container**: Same as Search Bar
- **Cancel Button**:
  - **Text**: "Cancel"
  - **Font**: 'Archivo', Size: 16px, Weight: 400, Color: #0B24FB, Line Height: 1.40
  - **Align**: Right
  - **Padding**: left: 10px, right: 16px
- **Layout**: Row with search field (Expanded) + Cancel button

#### Main Demo Container
- **Size**: 950px × variable height
- **Background**: #F4F6F9
- **Border**: 1px solid #7B61FF
- **Border Radius**: 15px (circular(15))
- **Padding**: 50px (all sides)
- **Content Layout**: Column/Row with spacing: 50px, 100px
- **Clip Behavior**: Clip.antiAlias

#### Big Vertical Card (Image Card with Overlay)
- **Container Size**: 375px width, 430px height
- **Padding**: horizontal: 16px, vertical: 10px
- **Border Radius**: 20px (circular(20))
- **Image Card**:
  - **Size**: 343px × 430px (Expanded)
  - **Border Radius**: 20px
  - **Image Fit**: BoxFit.cover
  - **Layout**: Column with spaceBetween alignment, spacing: 236px
- **Top Section** (padding: 20px):
  - **Title**: "Open your eyes", Font: 'Archivo', Size: 24px, Weight: 700, Color: white
  - **Label**: "Serial", Font: 'Archivo', Size: 16px, Weight: 700, Color: #FF6937 (orange)
  - **Spacing**: 4px between title and label
- **Bottom Section** (padding: 20px):
  - **Button Row**: spacing: 10px, alignment: end
  - **Icon Button**: Height: 44px, Background: #747B84 (gray), Border Radius: 15px, Padding: 16×10, Icon: 20×20px
  - **Text Button**: "Save", Height: 44px, Background: #747B84, Border Radius: 15px, Padding: 16×10, Font: 'Archivo', Size: 16px, Weight: 700, Color: white

#### Medium Card with Gradient Overlay
- **Container**: 375px × 420px, padding: 16×10, Border Radius: 20px
- **Image**: 343px × 400px, Border Radius: 20px
- **Gradient Overlay**: Linear gradient (0.50, -0.00) to (0.50, 1.00), colors: #00080808 to #7F080808
- **Content Container** (positioned over gradient):
  - **Width**: 343px, clipBehavior: Clip.antiAlias, spacing: 5px
  - **Title**: "Get your Kitchen Crew recipe", Size: 32px, Weight: 700, Color: white, padding-left: 10px
  - **CTA Section**: Background: #0C11BB8D (5% green tint), padding: 20px
    - **Description**: "Join 1M+ Kitchen Crew community...", Size: 11px, Weight: 400, Color: white, Width: 239px
    - **Button**: "Get", Height: 36px, Background: #F4F6F9, Border Radius: 15px, Padding: 16×10, Font: Size: 13px, Weight: 600, Color: #09101D

#### Article Card with Gradient
- **Container**: 375px × 380px, padding: 16×10
- **Image**: 343px × 360px, Border Radius: 20px
- **Gradient Overlay**: Same as medium card (#00080808 to #7F080808)
- **Content** (positioned at bottom, padding: 10px, spacing: 5px):
  - **Title**: "4 Muscle Recovery Smoothies...", Size: 26px, Weight: 700, Color: white, Width: 323px
  - **Excerpt**: "After a grueling gym session...", Size: 16px, Weight: 400, Color: white, Width: 323px

#### Promotional Card (Dark Background)
- **Container**: 375px width, padding: 16×10, Border Radius: 20px
- **Top Section**: Background: #09101D, padding: 32px, Border Radius: top-left/top-right: 20px
  - **Title**: "New program", Size: 24px, Weight: 700, Color: white, Align: center
  - **Subtitle**: "Try our new crossfit program...", Size: 13px, Weight: 400, Color: white, Align: center
  - **Spacing**: 20px between sections, 4px between title/subtitle
  - **Button**: "Learn more", Height: 36px, Background: white, Border Radius: 15px, Padding: 16×10, Icon: 16×16px, Font: Size: 13px, Weight: 600, Color: #09101D
- **Bottom Section**: Image 343px × 174px, Border Radius: bottom-left/bottom-right: 20px

#### Button Variants from Cards
- **Icon Button**: Height: 44px, Background: #747B84, Border Radius: 15px, Padding: 16×10, Icon: 20×20px (rounded: 100px)
- **Text Button**: Height: 44px, Background: #747B84, Border Radius: 15px, Padding: 16×10, Font: 16px/700
- **Small Button**: Height: 36px, Background: white/#F4F6F9, Border Radius: 15px, Padding: 16×10, Font: 13px/600
- **Button with Icon**: Icon: 16×16px (padding: 2px, rounded: 100px), spacing: 8px

#### Master Stories (Text Outside) - Complete Component Block

**Container Layout:**
- **Padding**: 50px (all sides)
- **Border**: 1px solid #7B61FF
- **Border Radius**: 15px (circular(15))
- **Clip Behavior**: Clip.antiAlias
- **Layout**: Row with spacing: 100px

**Story Card Variants:**

1. **Vertical Portrait Story (Standard)**
   - **Container**: Column, spacing: 10px
   - **Image**: 100px × 120px, Border Radius: 10px (circular(10)), BoxFit.cover
   - **Label Section**: Column, spacing: 3px
     - **Container**: width: 100px, padding-left: 10px
     - **Text**: "Category or service", Font: 'Archivo', Size: 13px, Weight: 700, Color: #09101D, Line Height: 1.40, Width: 90px

2. **Vertical Portrait Story (With Purple Border - Active)**
   - **Container**: Column, spacing: 10px
   - **Border Container**: 100px × 120px, Background: white, Border: 2px solid #833AB4, Border Radius: 13px (circular(13)), strokeAlign: center
   - **Image**: 94px × 114px (positioned inside), Border Radius: 10px, BoxFit.cover
   - **Label**: Same as standard

3. **Vertical Portrait Story (With Blue Border - Active)**
   - **Container**: Column, spacing: 10px
   - **Border Container**: 100px × 120px, Background: white, Border: 2px solid #4141E6, Border Radius: 13px, strokeAlign: center
   - **Image**: 94px × 114px, Border Radius: 10px, BoxFit.cover
   - **Label**: Same as standard

4. **Horizontal Landscape Story (Standard)**
   - **Container**: Column, spacing: 10px
   - **Image**: 130px × 80px, Border Radius: 10px, BoxFit.cover
   - **Label Section**: Column, spacing: 3px
     - **Container**: padding-left: 10px
     - **Text**: "Category or service", Font: 'Archivo', Size: 13px, Weight: 700, Color: #09101D, Width: 110px

5. **Horizontal Landscape Story (With Purple Border - Active)**
   - **Container**: Column, spacing: 10px
   - **Border Container**: 130px × 80px, Background: white, Border: 2px solid #833AB4, Border Radius: 13px, strokeAlign: center
   - **Image**: 124px × 74px, Border Radius: 10px, BoxFit.cover
   - **Label**: Same as standard

6. **Horizontal Landscape Story (With Blue Border - Active)**
   - **Container**: Column, spacing: 10px
   - **Border Container**: 130px × 80px, Background: white, Border: 2px solid #4141E6, Border Radius: 13px, strokeAlign: center
   - **Image**: 124px × 74px, Border Radius: 10px, BoxFit.cover
   - **Label**: Same as standard

**Story Border Colors:**
- **Purple**: #833AB4 - Instagram gradient style (for active/viewed stories)
- **Blue**: #4141E6 - Alternative active state

**Usage Notes:**
- Border reduces image size by 6px on each side (100→94, 120→114, 130→124, 80→74)
- Border uses strokeAlign: center positioning
- Spacing between stories in row: 100px
- Label text always 13px/700 with 10px left padding
- Internal spacing in label column: 3px

#### Navigation Bars - Complete Component Block

**Container Layout:**
- **Padding**: 50px (all sides)
- **Border**: 1px solid #7B61FF
- **Border Radius**: 15px (circular(15))
- **Clip Behavior**: Clip.antiAlias
- **Layout**: Column with spacing: 50px

**Component Variants:**

1. **Navigation Header (with Notification Badge)**
   - **Container**: 375px width, height: 44px
   - **Background**: white (#FFFFFF)
   - **Layout**: Row with mainAxisAlignment: spaceBetween, crossAxisAlignment: center
   - **Title Section**:
     - **Container**: height: 44px, padding: horizontal 16px, vertical 10px
     - **Text**: "Following", Font: 'Archivo', Size: 24px, Weight: 700, Color: #09101D, Line Height: 1.40
   - **Notification Badge**:
     - **Container**: 12px × 12px (positioned right: 16px, top: 16px)
     - **Background**: #E24949 (error red)
     - **Border**: 2px solid white
     - **Border Radius**: 12px (circular(12))
     - **Clip Behavior**: Clip.antiAlias

2. **Avatar with Badge Counter**
   - **Container**: Column, spacing: 10px
   - **Avatar Container**: 56px × 56px
     - **Inner Circle**: 48px × 48px, Border Radius: 40px/50px
     - **Background**: #D9DDE2 (gray placeholder)
     - **Image**: 48px × 48px, BoxFit.cover
     - **Clip Behavior**: Clip.antiAlias
   - **Badge Counter**:
     - **Container**: 20px × 20px (positioned top-right of avatar)
     - **Background**: #23262B (dark badge)
     - **Border**: 2px solid white
     - **Border Radius**: 12px (circular(12))
     - **Text**: "2", Font: 'Archivo', Size: 10px, Weight: 600, Color: white, Align: center
   - **Label Section**: Column, spacing: 5px
     - **Container**: padding-left: 10px
     - **Text**: "User name", Font: 'Archivo', Size: 11px, Weight: 600, Color: #09101D, Line Height: 1.40

3. **Gradient Pricing Button (with Save Badge)**
   - **Container**: height: 44px, Border Radius: 30px (circular(30))
   - **Background**: linear-gradient(90deg, #EB001B 0%, #DD2476 100%)
   - **Padding**: horizontal: 16px, vertical: 10px
   - **Layout**: Row with mainAxisAlignment: center, spacing: 8px
   - **Clip Behavior**: Clip.antiAlias
   - **Price Text**:
     - **Text**: "$86.99/Year", Font: 'Archivo', Size: 14px, Weight: 600, Color: white, Line Height: 1.40
   - **Save Badge**:
     - **Container**: height: 20px, Border Radius: 12px (circular(12))
     - **Background**: white (#FFFFFF)
     - **Padding**: horizontal: 8px, vertical: 5px
     - **Text**: "Save 23%", Font: 'Archivo', Size: 11px, Weight: 600, Color: #09101D, Line Height: 1.40

4. **Outlined Pricing Button**
   - **Container**: height: 44px, Border Radius: 30px (circular(30))
   - **Background**: white (#FFFFFF)
   - **Border**: 1px solid #FE5032 (orange border)
   - **Padding**: horizontal: 16px, vertical: 10px
   - **Clip Behavior**: Clip.antiAlias
   - **Text**: "$9.49/Month", Font: 'Archivo', Size: 14px, Weight: 600, Color: #09101D, Line Height: 1.40, Align: center

5. **Home Indicator**
   - **Container**: 134px × 5px
   - **Background**: #09101D (dark)
   - **Border Radius**: 100px (circular(100))
   - **Position**: center horizontal, bottom (typically with bottom spacing)

**Color Usage:**
- **Navigation Background**: #FFFFFF (white)
- **Avatar Placeholder**: #D9DDE2 (gray)
- **Badge Background**: #23262B (dark), #E24949 (notification red)
- **Gradient**: #EB001B to #DD2476 (red to pink)
- **Border**: #FE5032 (orange accent), white (badge borders)
- **Text**: #09101D (primary), white (on gradient/badges)

**Usage Notes:**
- Navigation header height: 44px standard
- Avatar size: 56×56px container with 48×48px image
- Badge counter size: 20×20px with 2px white border
- Button height: 44px with 30px border radius
- Save badge uses white background with dark text for contrast
- Home indicator: 134×5px with full rounding (100px radius)
- Spacing between navigation elements: 50px
- Internal badge padding: horizontal 8px, vertical 5px

---

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
