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

- **Консистентность**: Единообразие визуальных элементов и паттернов взаимодействия в мобильном приложении
- **Читаемость**: Приоритет контрасту и размерам шрифтов, оптимизированным для мобильных экранов
- **Эффективность**: Минимизация когнитивной нагрузки через понятную иерархию информации
- **Адаптивность**: Дизайн, оптимизированный для мобильных устройств различных размеров

### Философия

> Дизайн-система для мобильных приложений, построенная на основе типографики Archivo и минималистичной цветовой палитре.

---

## Цветовая палитра

### Base Colors

```css
/* Основные цвета из Flutter кода */
--color-white: #FFFFFF;
--color-black: #000000;
--color-black-text: #09101D;       /* Основной цвет текста */
```

### Primary Colors

```css
/* Основной акцентный цвет из Flutter */
--color-primary: #4141E6;          /* Основной синий/фиолетовый цвет */
--color-primary-light: rgba(11, 36, 251, 0.1); /* #0B24FB с opacity 0.1 */
--color-primary-dark: #221874;     /* Темно-фиолетовый для rating badge */
```

### Text Colors

```css
/* Цвета текста из Flutter кода */
--color-text-primary: #09101D;     /* Основной черный текст */
--color-text-secondary: #414249;   /* Серый текст */
--color-text-tertiary: #747B84;    /* Вторичный серый текст */
--color-text-dark: #23262B;        /* Темный текст */
--color-text-dark-2: #2A2B2F;      /* Темный текст вариант 2 */
```

### Accent Colors

```css
/* Акцентные цвета из Flutter */
--color-success: #11BB8D;          /* Зеленый для badge (Discount, Rating) */
--color-warning: #FFC043;          /* Желтый/золотой для price button */
```

### Background Colors

```css
/* Фоны для компонентов из Flutter кода */
--color-bg-light: #F4F6F9;         /* Светлый фон (основной) */
--color-bg-card-light: #D9DDE2;    /* Светлая карточка/разделитель */
--color-bg-divider: #EAEEF2;       /* Цвет разделителей */
--color-bg-card-dark: #23262B;     /* Темная карточка */
--color-bg-overlay-dark: rgba(0, 0, 0, 0.2); /* Темный overlay с opacity */
--color-bg-icon-overlay: rgba(17, 187, 141, 0.05); /* #11BB8D с opacity 0.05 */
```

### Gradient Colors

```css
/* Instagram-like градиент из Flutter кода */
--gradient-instagram-start: #833AB4;   /* Фиолетовый */
--gradient-instagram-mid: #FD1D1D;     /* Красный */
--gradient-instagram-end: #FCB045;     /* Оранжевый */
```

**Применение градиента:**
```css
background: linear-gradient(90deg,
  var(--gradient-instagram-start) 0%,
  var(--gradient-instagram-mid) 50%,
  var(--gradient-instagram-end) 100%);
```

### Shadow Colors

```css
/* Тени из Flutter кода */
--shadow-default: rgba(0, 0, 0, 0.05);      /* 0x0C000000 */
--shadow-text: rgba(0, 0, 0, 0.40);         /* Тень для текста */
--shadow-box: rgba(0, 0, 0, 0.40);          /* Тень для контейнеров */
```

---

## Типографика

### Font Family

```css
--font-primary: 'Archivo', sans-serif;
--font-ocr: 'OCR-A', monospace;             /* Для номеров карт и специальных данных */
```

**Ссылка**: [Archivo on Google Fonts](https://fonts.google.com/specimen/Archivo#standard-styles)

**Описание**: Archivo is a grotesque sans serif typeface family originally designed for highlights and headlines. This family is reminiscent of late nineteenth century American typefaces. The technical and aesthetic characteristics of the font are both crafted for high performance typography. It was designed to be used simultaneously in print and online platforms and supports over 200 world languages.

**OCR-A**: Моноширинный шрифт для отображения номеров кредитных карт и цифровых данных.

### Font Sizes

```css
/* Размеры шрифтов из Flutter кода */
--font-size-6: 0.375rem;      /* 6px */
--font-size-7: 0.4375rem;     /* 7px */
--font-size-10: 0.625rem;     /* 10px */
--font-size-11: 0.6875rem;    /* 11px */
--font-size-12: 0.75rem;      /* 12px */
--font-size-13: 0.8125rem;    /* 13px */
--font-size-14: 0.875rem;     /* 14px */
--font-size-15: 0.9375rem;    /* 15px */
--font-size-16: 1rem;         /* 16px */
--font-size-18: 1.125rem;     /* 18px */
--font-size-19: 1.1875rem;    /* 19px */
--font-size-22: 1.375rem;     /* 22px - для номеров карт */
--font-size-23: 1.4375rem;    /* 23px */
--font-size-24: 1.5rem;       /* 24px */
--font-size-26: 1.625rem;     /* 26px */
--font-size-32: 2rem;         /* 32px */
```

### Font Weights

```css
--font-weight-regular: 400;
--font-weight-medium: 500;
--font-weight-semibold: 600;
--font-weight-bold: 700;
--font-weight-extrabold: 800;
```

### Line Heights

```css
--line-height-12: 0.75rem;    /* 12px */
--line-height-16: 1rem;       /* 16px */
--line-height-20: 1.25rem;    /* 20px */
--line-height-24: 1.5rem;     /* 24px */
--line-height-32: 2rem;       /* 32px */
--line-height-36: 2.25rem;    /* 36px */
--line-height-40: 2.5rem;     /* 40px */
--line-height-50: 3.15rem;    /* 50.4px */
```

### Text Styles (iOS Mobile)

#### Large Title
- **Bold**: Font: 32px (2rem), Weight: 700, Line Height: 40px
- **Regular**: Font: 32px (2rem), Weight: 400, Line Height: 40px

#### Title 1
- **Bold**: Font: 26px (1.625rem), Weight: 700, Line Height: 36px
- **Regular**: Font: 26px (1.625rem), Weight: 400, Line Height: 36px

#### Title 2
- **Bold**: Font: 24px (1.5rem), Weight: 700, Line Height: 32px
- **Regular**: Font: 24px (1.5rem), Weight: 400, Line Height: 32px

#### Title 3
- **Medium**: Font: 18px (1.125rem), Weight: 500, Line Height: 24px
- **Regular**: Font: 18px (1.125rem), Weight: 400, Line Height: 24px

#### Headline
- **Bold**: Font: 16px (1rem), Weight: 700, Line Height: 24px
- **Semibold Italic**: Font: 16px (1rem), Weight: 600, Style: Italic, Line Height: 24px

#### Body
- **Semibold**: Font: 16px (1rem), Weight: 600, Line Height: 24px
- **Regular**: Font: 16px (1rem), Weight: 400, Line Height: 24px

#### Callout
- **Semibold**: Font: 15px (0.9375rem), Weight: 600, Line Height: 20px
- **Regular**: Font: 15px (0.9375rem), Weight: 400, Line Height: 20px

#### Subheadline
- **Semibold**: Font: 14px (0.875rem), Weight: 600, Line Height: 20px
- **Regular**: Font: 14px (0.875rem), Weight: 400, Line Height: 20px

#### Footnote
- **Medium**: Font: 13px (0.8125rem), Weight: 500, Line Height: 20px
- **Regular**: Font: 13px (0.8125rem), Weight: 400, Line Height: 20px

#### Caption 1
- **Medium**: Font: 12px (0.75rem), Weight: 500, Line Height: 16px
- **Regular**: Font: 12px (0.75rem), Weight: 400, Line Height: 16px

#### Caption 2
- **Semibold**: Font: 11px (0.6875rem), Weight: 600, Line Height: 16px
- **Regular**: Font: 11px (0.6875rem), Weight: 400, Line Height: 16px

#### Caption 3
- **Semibold**: Font: 10px (0.625rem), Weight: 600, Line Height: 12px

### Letter Spacing

```css
/* Межбуквенные интервалы из Flutter кода */
--letter-spacing-0-21: 0.01313rem;  /* 0.21px */
--letter-spacing-0-33: 0.02063rem;  /* 0.33px */
--letter-spacing-0-46: 0.02875rem;  /* 0.46px */
--letter-spacing-0-58: 0.03625rem;  /* 0.58px */
--letter-spacing-0-70: 0.04375rem;  /* 0.70px */
--letter-spacing-1: 0.0625rem;      /* 1px */
--letter-spacing-2: 0.125rem;       /* 2px */
--letter-spacing-2-59: 0.162rem;    /* 2.59px - для номеров карт */
```

### OCR-A Text Styles (для карточек и цифровых данных)

#### Card Number
- **Font**: OCR-A, 22px (1.375rem)
- **Weight**: 400 (Regular)
- **Line Height**: 1.40
- **Letter Spacing**: 2.59px
- **Shadow**: 0 1px 1px rgba(0, 0, 0, 0.40)

#### Card Data (имя, дата)
- **Font**: OCR-A, 11px (0.6875rem)
- **Weight**: 400 (Regular)
- **Line Height**: 1.40
- **Letter Spacing**: 1px - 2px
- **Shadow**: 0 1px 1px rgba(0, 0, 0, 0.40)

---

## Spacing & Layout

### Spacing Scale

```css
/* Отступы из Flutter кода (padding/margin) */
--space-0: 0;
--space-0-5: 0.125rem;   /* 2px */
--space-1: 0.25rem;      /* 4px */
--space-1-25: 0.3125rem; /* 5px */
--space-1-5: 0.375rem;   /* 6px */
--space-2: 0.5rem;       /* 8px */
--space-2-5: 0.625rem;   /* 10px */
--space-3: 0.75rem;      /* 12px */
--space-3-25: 0.8125rem; /* 13px */
--space-4: 1rem;         /* 16px */
--space-5: 1.25rem;      /* 20px */
--space-6: 1.5rem;       /* 24px */
--space-7: 1.75rem;      /* 28px */
--space-8: 2rem;         /* 32px */
--space-10: 2.5rem;      /* 40px */
--space-12: 3rem;        /* 48px */
--space-16: 4rem;        /* 64px */
--space-20: 5rem;        /* 80px */
--space-24: 6rem;        /* 96px */
--space-167: 10.4375rem; /* 167px - для центрирования элементов */
```

### Border Radius

```css
/* Радиусы скругления из Flutter кода */
--radius-none: 0;
--radius-xs: 0.125rem;     /* 2px */
--radius-sm: 0.3125rem;    /* 5px - для маленьких карточек */
--radius-badge: 0.4375rem; /* 7px - для badge компонентов */
--radius-md: 0.5rem;       /* 8px */
--radius-base: 0.75rem;    /* 12px */
--radius-lg: 0.9375rem;    /* 15px - основной для кнопок и больших карточек */
--radius-xl: 1.25rem;      /* 20px */
--radius-2xl: 1.875rem;    /* 30px - для больших контейнеров */
--radius-3xl: 2.5rem;      /* 40px */
--radius-full: 9999px;     /* Полный круг */
```

### Shadows

#### Shadows из Flutter кода

```css
/* Основная тень из Flutter BoxShadow */
--shadow-primary: 0 -2px 4px 0 rgba(0, 0, 0, 0.05);

/* Стандартные тени */
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
/* Прозрачность из Flutter кода */
--opacity-0: 0;
--opacity-10: 0.1;     /* Используется в коде */
--opacity-20: 0.2;     /* Используется в коде */
--opacity-25: 0.25;    /* Используется в коде */
--opacity-30: 0.3;     /* Используется в коде */
--opacity-40: 0.4;     /* Используется в коде */
--opacity-50: 0.5;
--opacity-60: 0.6;
--opacity-70: 0.7;
--opacity-80: 0.8;
--opacity-90: 0.9;
--opacity-100: 1;
```

---

## Размеры компонентов из Flutter

### Mobile Screen

```css
/* Размеры экрана из Flutter кода */
--screen-width: 375px;     /* Ширина мобильного экрана (iPhone) */
--screen-height: 812px;    /* Высота мобильного экрана */
```

### Buttons (из Flutter кода)

```css
/* Высота кнопок */
--button-height-sm: 36px;      /* Маленькая кнопка */
--button-height-md: 44px;      /* Основная высота кнопок */
--button-height-lg: 48px;      /* Большая кнопка */

/* Горизонтальный padding кнопок */
--button-padding-x: 16px;      /* Основной padding */
--button-padding-y: 10px;      /* Вертикальный padding */
```

### Avatars (из Flutter кода)

```css
/* Размеры аватаров */
--avatar-xs: 28px;        /* Badge аватар */
--avatar-sm: 40px;        /* Маленький аватар */
--avatar-md: 48px;        /* Средний аватар */
--avatar-lg: 56px;        /* Большой аватар */
```

### Icons (из Flutter кода)

```css
/* Размеры иконок */
--icon-xs: 12px;
--icon-sm: 15px;        /* Маленькие иконки в карточках */
--icon-md: 20px;        /* Размер 21x20 округлен до 20px */
--icon-lg: 24px;        /* Иконка overlay */
--icon-xl: 30px;        /* Большая иконка избранного */
--icon-2xl: 32px;
```

### Cards Sizes (из Flutter кода)

```css
/* Размеры карточек */
--card-image-width-lg: 120px;   /* Ширина изображения большой карточки */
--card-image-height-lg: 202px;  /* Высота изображения большой карточки */
--card-image-width-sm: 120px;   /* Ширина изображения маленькой карточки */
--card-image-height-sm: 107px;  /* Высота изображения маленькой карточки */
```

### Containers & Panels

```css
/* Высота элементов */
--status-bar-height: 44px;     /* Высота status bar */
--handle-height: 3px;          /* Высота handle для bottom sheets */
--handle-width: 40px;          /* Ширина handle */
--divider-height: 1px;         /* Высота разделителя */
--home-indicator: 5px;         /* Высота home indicator */
--home-indicator-width: 134px; /* Ширина home indicator */
```

### Spacing между элементами

```css
/* Spacing из Flutter кода (spacing property) */
--spacing-2: 2px;
--spacing-5: 5px;
--spacing-7: 7px;
--spacing-8: 8px;
--spacing-10: 10px;
--spacing-12: 12px;
--spacing-15: 15px;
--spacing-16: 16px;
--spacing-70: 70px;  /* Между элементами в Row */
```

---

## Компоненты

### 1. Cards (из Flutter кода)

#### Hotel Card Large

- **Layout**: Row с изображением слева и контентом справа
- **Container Width**: 375px
- **Padding**: 16px horizontal, 5px vertical
- **Spacing**: 5px между изображением и контентом

**Image Container:**
- **Width**: 120px
- **Height**: 202px (динамическая)
- **Border Radius**: 15px (radius-lg)
- **Image Fit**: cover

**Content Container:**
- **Padding**: 10px
- **Border Radius**: 15px (radius-lg)
- **Background**: #F4F6F9 (color-bg-light)
- **Spacing**: 5px между элементами

**Elements:**
- Title: 11px, weight 600, color #09101D
- Location: 10px, weight 400, color #09101D
- Rating badge: 10px, background #221874
- Review text: 10px, weight 600/400
- Tags: 8px, background #11BB8D, radius 5px
- Price button: 11px, background #FFC043, radius 15px, height 36px

#### Hotel Card Small

- **Layout**: Row с изображением слева и контентом справа
- **Container Width**: 375px
- **Padding**: 16px horizontal, 5px vertical
- **Spacing**: 5px между изображением и контентом

**Image Container:**
- **Width**: 120px
- **Height**: 107px (динамическая)
- **Border Radius**: 5px (radius-sm)
- **Image Fit**: cover

**Content Container:**
- **Padding**: 10px
- **Border Radius**: 5px (radius-sm)
- **Background**: #F4F6F9 (color-bg-light)
- **Spacing**: 5px между элементами

**Elements:**
- Title: 11px, weight 600, color #09101D
- Badge: 8px, background #23262B, radius 7px
- Rating badge: 10px, background #11BB8D, radius 7px
- Description: 11px, weight 400, color #747B84

---

### 2. Buttons (из Flutter кода)

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

#### Price Button (Из Flutter кода)

- **Height**: 36px
- **Padding**: 16px horizontal, 10px vertical
- **Radius**: 15px (radius-lg)
- **Background**: #FFC043 (color-warning)
- **Color**: #09101D (color-text-primary)
- **Font Size**: 11px
- **Font Weight**: 600 (semibold) для цены, 400 (regular) для валюты
- **Text Format**: "235 USD" (цена bold, валюта regular)

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

### 4. Badges & Tags (из Flutter кода)

#### Badge Variants

**Rating Badge (Темный)**
- **Padding**: 3px horizontal, 3px vertical
- **Radius**: 5px (radius-sm) или 7px (radius-badge)
- **Font Size**: 10px (font-size-10)
- **Font Weight**: 600 (semibold)
- **Background**: #221874 (color-primary-dark)
- **Color**: white
- **Использование**: Рейтинг отелей/мест

**Success Badge (Зеленый)**
- **Padding**: 5px horizontal, 3px vertical
- **Radius**: 5px (radius-sm) или 7px (radius-badge)
- **Font Size**: 8px или 10px
- **Font Weight**: 600 (semibold)
- **Background**: #11BB8D (color-success)
- **Color**: white
- **Использование**: Discount, Secret Deal, Good rating

**Dark Badge**
- **Padding**: 5px horizontal, 3px vertical
- **Radius**: 7px (radius-badge)
- **Font Size**: 8px
- **Font Weight**: 600 (semibold)
- **Background**: #23262B (color-bg-card-dark)
- **Color**: white
- **Использование**: Native speaker

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

**Текущая версия**: v5.0.2

### Changelog

#### v5.0.2 (2025-11-19)
- Добавлены акцентные цвета: success (#11BB8D), warning (#FFC043)
- Добавлен темно-фиолетовый primary-dark (#221874) для rating badge
- Добавлены overlay цвета с прозрачностью
- Обновлены border radius: добавлены 5px и 7px для badge
- Добавлены размеры карточек: Large (120x202) и Small (120x107)
- Обновлены размеры иконок: 15px, 30px
- Добавлены реальные Badge компоненты из кода (Rating, Success, Dark)
- Добавлены Hotel Card Large и Small с полным описанием
- Добавлен Price Button компонент (#FFC043)

#### v5.0.1 (2025-11-19)
- Обновлены цвета из реального Flutter кода
- Добавлены все размеры шрифтов (6px - 32px)
- Добавлены letterSpacing значения из кода (0.21px - 2.59px)
- Обновлены Border Radius значения (2px - 100px)
- Расширены Spacing значения с дробными размерами
- Добавлены реальные размеры компонентов из Flutter
- Добавлен Instagram-like градиент
- Добавлены размеры мобильного экрана (375x812)
- Добавлены размеры кнопок, аватаров и иконок из кода

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
