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
/* Основные цвета */
--color-white: #FFFFFF;
--color-black: #09101D;
--color-scaffold-bg: #12202F;      /* Темный фон приложения */
```

### Background Colors

```css
/* Фоновые цвета */
--color-bg-primary: #FFFFFF;
--color-bg-secondary: #F4F6F9;     /* Светлый серо-голубой */
--color-bg-tertiary: #D9DDE2;      /* Светло-серый (аватары, плейсхолдеры) */
--color-bg-dark: #12202F;          /* Темный фон */
```

### Text Colors

```css
/* Текстовые цвета */
--color-text-primary: #09101D;     /* Основной текст (заголовки) */
--color-text-secondary: #414249;   /* Вторичный текст (подзаголовки) */
--color-text-tertiary: #64748B;    /* Третичный текст */
```

### Accent Colors

```css
/* Акцентные цвета */
--color-accent-blue: #4141E6;      /* Синий (stories, primary actions) */
--color-accent-pink: #FC466B;      /* Розовый (stories, highlights) */
```

### Status Colors

```css
/* Статусные цвета */
--color-status-online: #11BB8D;    /* Зеленый (online indicator) */
--color-status-success: #10B981;
--color-status-error: #EF4444;
--color-status-warning: #F59E0B;
```

### Gradient Colors

```css
/* Градиенты */
--gradient-live-start: #833AB4;    /* Фиолетовый (Live badge) */
--gradient-live-middle: #FD1D1D;   /* Красный (Live badge) */
--gradient-live-end: #FCB045;      /* Оранжевый (Live badge) */

/* Применение Live gradient */
--gradient-live: linear-gradient(90deg, #833AB4 0%, #FD1D1D 50%, #FCB045 100%);
```

### Border Colors

```css
/* Цвета границ */
--color-border-primary: #E5E7EB;
--color-border-secondary: #D1D5DB;
--color-border-stories-blue: #4141E6;   /* Border для непросмотренных stories */
--color-border-stories-pink: #FC466B;   /* Border для highlighted stories */
```

### Shadow Colors

```css
/* Тени */
--shadow-light: rgba(240, 241, 242, 1.00);
--shadow-dark: rgba(0, 0, 0, 0.1);
```

---

## Типографика

### Font Family

```css
--font-primary: 'Archivo', sans-serif;
```

**Ссылка**: [Archivo on Google Fonts](https://fonts.google.com/specimen/Archivo#standard-styles)

**Описание**: Archivo is a grotesque sans serif typeface family originally designed for highlights and headlines. This family is reminiscent of late nineteenth century American typefaces. The technical and aesthetic characteristics of the font are both crafted for high performance typography. It was designed to be used simultaneously in print and online platforms and supports over 200 world languages.

### Font Sizes

```css
--font-size-10: 0.625rem;     /* 10px */
--font-size-11: 0.6875rem;    /* 11px */
--font-size-12: 0.75rem;      /* 12px */
--font-size-13: 0.8125rem;    /* 13px */
--font-size-14: 0.875rem;     /* 14px */
--font-size-15: 0.9375rem;    /* 15px */
--font-size-16: 1rem;         /* 16px */
--font-size-18: 1.125rem;     /* 18px */
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

### Text Styles (Flutter Components - из реального кода)

#### User List Item Title
- **Font Size**: 16px (1rem)
- **Font Weight**: 700 (Bold)
- **Font Family**: 'Archivo'
- **Line Height**: 1.40 (22.4px)
- **Color**: #09101D (--color-text-primary)
- **Использование**: Заголовки в списках пользователей, основной текст в карточках

#### User List Item Subtitle
- **Font Size**: 14px (0.875rem)
- **Font Weight**: 400 (Regular)
- **Font Family**: 'Archivo'
- **Line Height**: 1.40 (19.6px)
- **Color**: #414249 (--color-text-secondary)
- **Использование**: Подзаголовки, дополнительная информация

#### Avatar Initials
- **Font Size**: 16px (1rem)
- **Font Weight**: 600 (Semibold)
- **Font Family**: 'Archivo'
- **Line Height**: 1.40 (22.4px)
- **Color**: #FFFFFF (white)
- **Text Align**: Center
- **Использование**: Инициалы в аватарах без фото

#### Notification Badge
- **Font Size**: 10px (0.625rem)
- **Font Weight**: 600 (Semibold)
- **Font Family**: 'Archivo'
- **Line Height**: 1.40 (14px)
- **Color**: #FFFFFF (white)
- **Text Align**: Center
- **Использование**: Цифры уведомлений, счетчики

#### Live Badge
- **Font Size**: 10px (0.625rem)
- **Font Weight**: 600 (Semibold)
- **Font Family**: 'Archivo'
- **Line Height**: 1.40 (14px)
- **Color**: #FFFFFF (white)
- **Использование**: "Live" badge, статусные метки

---

## Spacing & Layout

### Spacing Scale

```css
--space-0: 0;
--space-1: 0.25rem;   /* 4px */
--space-2: 0.5rem;    /* 8px */
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
```

### Border Radius

```css
--radius-none: 0;
--radius-sm: 0.125rem;    /* 2px */
--radius-base: 0.25rem;   /* 4px */
--radius-md: 0.375rem;    /* 6px */
--radius-lg: 0.5rem;      /* 8px */
--radius-icon: 0.625rem;  /* 10px - Icon containers */
--radius-xl: 0.75rem;     /* 12px - Live badge */
--radius-badge: 0.9375rem; /* 15px - Badge containers */
--radius-2xl: 1rem;       /* 16px */
--radius-notification: 1.25rem;  /* 20px - Notification badge */
--radius-stories: 1.875rem;      /* 30px - Stories border */
--radius-avatar: 2.5rem;         /* 40px - Avatar */
--radius-full: 9999px;           /* Полностью круглый */
```

**Применение из Flutter кода:**
- `radius-avatar (40px)`: Основной border radius для аватаров
- `radius-stories (30px)`: Border radius для stories border вокруг аватара
- `radius-notification (20px)`: Notification badge
- `radius-badge (15px)`: Стандартные badge контейнеры
- `radius-xl (12px)`: Live badge
- `radius-icon (10px)`: Icon containers
- `radius-full`: Online indicator, круглые элементы

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

```css
--border-width-0: 0;
--border-width-1: 1px;    /* Online indicator, Live badge border */
--border-width-2: 2px;    /* Stories border */
--border-width-4: 4px;
```

**Применение из Flutter кода:**
- `border-width-2 (2px)`: Stories border вокруг аватара
- `border-width-1 (1px)`: Online indicator border (white), Live badge border (white)

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

### 4. Badges & Tags (из реального Flutter кода)

#### Notification Badge (Counter)

**Спецификация из кода:**
- **Size**: 20px × 20px
- **Background**: #4141E6 (--color-accent-blue)
- **Border Radius**: 20px (--radius-notification)
- **Padding**: 4px horizontal, 2px vertical
- **Position**: Top-right corner of avatar (left: 36px, top: 0)
- **Typography**:
  - Font: 10px (0.625rem)
  - Weight: 600 (Semibold)
  - Color: white
  - Text Align: center
- **Использование**: Счетчики уведомлений на аватарах
- **Пример контента**: "11", "99+", "3"

#### Online Status Indicator

**Спецификация из кода:**
- **Size**: 14px × 14px
- **Background**: #11BB8D (--color-status-online)
- **Border**: 1px solid white (--border-width-1)
- **Border Radius**: circle (--radius-full)
- **Position**: Bottom-right corner of avatar (left: 0, top: 36px)
- **Использование**: Индикатор онлайн-статуса пользователя
- **Варианты**:
  - Online: Background #11BB8D (зеленый)
  - Offline: Background #9CA3AF (серый)
  - Away: Background #F59E0B (оранжевый)
  - DND: Background #EF4444 (красный)

#### Live Badge

**Спецификация из кода:**
- **Size**: 28px × 14px
- **Background**: Linear gradient
  - Start: #833AB4 (фиолетовый)
  - Middle: #FD1D1D (красный)
  - End: #FCB045 (оранжевый)
  - Direction: 90deg (horizontal)
- **Border**: 1px solid white (--border-width-1)
- **Border Radius**: 12px (--radius-xl)
- **Padding**: 4px horizontal, 2px vertical
- **Position**: Bottom-center of avatar (left: 0, top: 36px)
- **Typography**:
  - Font: 10px (0.625rem)
  - Weight: 600 (Semibold)
  - Color: white
  - Text Width: 20px
  - Content: "Live"
- **Использование**: Индикатор live-трансляций

```css
/* Live Badge Gradient */
background: linear-gradient(90deg,
  var(--gradient-live-start) 0%,
  var(--gradient-live-middle) 50%,
  var(--gradient-live-end) 100%
);
```

#### General Badge Variants

- **Padding**: 4px 8px
- **Radius**: radius-full (9999px)
- **Font Size**: font-size-xs (12px)
- **Variants**:
  - Success: Background: color-success-bg, Color: color-success, Border: 1px solid color-success-border
  - Error: Background: color-error-bg, Color: color-error, Border: 1px solid color-error-border
  - Warning: Background: color-warning-bg, Color: color-warning, Border: 1px solid color-warning-border
  - Info: Background: color-info-bg, Color: color-info, Border: 1px solid color-info-border
  - Neutral: Background: color-gray-100, Color: color-gray-700, Border: 1px solid color-gray-300
  - Primary: Background: #4141E6, Color: white (из кода)

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

### 9. Avatars (из реального Flutter кода)

#### Sizes

- **XS**: 24px × 24px
- **Small**: 32px × 32px
- **Medium**: 40px × 40px
- **Large**: 48px × 48px (основной размер из кода)
- **XL**: 64px × 64px
- **2XL**: 96px × 96px

#### Avatar Container Structure (из кода)

**Базовый аватар:**
- **Outer Container**: 56px × 56px
- **Avatar Image**: 48px × 48px
- **Position**: left: 4px, top: 4px (отступ от контейнера)
- **Background (placeholder)**: #D9DDE2 (--color-bg-tertiary)
- **Border Radius**: 40px (--radius-avatar)
- **Image fit**: cover

#### Варианты аватаров

**1. Simple Avatar (без border)**
```
Container: 56×56
└─ Avatar: 48×48 (position: 4px, 4px)
   ├─ Background: #D9DDE2
   ├─ Border Radius: 40px
   └─ Image: NetworkImage (плейсхолдер)
```

**2. Avatar with Stories Border (Blue - непросмотренные)**
```
Container: 56×56
├─ Stories Border: 56×56 (position: 0, 0)
│  ├─ Border: 2px solid #4141E6
│  └─ Border Radius: 30px
└─ Avatar: 48×48 (position: 4px, 4px)
   ├─ Background: #D9DDE2
   └─ Border Radius: 40px
```

**3. Avatar with Stories Border (Pink - highlighted)**
```
Container: 56×56
├─ Stories Border: 56×56 (position: 0, 0)
│  ├─ Border: 2px solid #FC466B
│  └─ Border Radius: 30px
└─ Avatar: 48×48 (position: 4px, 4px)
```

**4. Avatar with Icon**
```
Row (spacing: 8px)
├─ Avatar: 48×48
└─ Icon Container: 24×24
   ├─ Background: #F4F6F9
   └─ Border Radius: 10px
```

**5. Avatar with Text (User List Item)**
```
Row (spacing: 8px)
├─ Avatar: 48×48
└─ Column
   ├─ Title: "Title"
   │  ├─ Font: 16px, weight: 700
   │  └─ Color: #09101D
   └─ Subtitle: "Subtitle"
      ├─ Font: 14px, weight: 400
      └─ Color: #414249
```

**6. Avatar with Top Badge (Notification Counter)**
```
Container: 56×56
├─ Avatar: 48×48 (position: 4px, 4px)
└─ Notification Badge: 20×20 (position: 36px, 0)
   ├─ Background: #4141E6
   ├─ Border Radius: 20px
   ├─ Padding: 4px horizontal, 2px vertical
   └─ Text: "11"
      ├─ Font: 10px, weight: 600
      ├─ Color: white
      └─ Align: center
```

**7. Avatar with Bottom Badge (Online Indicator)**
```
Container: 56×56
├─ Avatar: 48×48 (position: 4px, 4px)
└─ Online Indicator: 14×14 (position: 0, 36px - bottom-right)
   ├─ Background: #11BB8D
   ├─ Border: 1px solid white
   ├─ Border Radius: 20px (circle)
   └─ Size: 14×14
```

**8. Avatar with Live Badge**
```
Container: 56×56
├─ Avatar: 48×48 (position: 4px, 4px)
└─ Live Badge: 28×14 (position: 0, 36px - bottom)
   ├─ Gradient: #833AB4 → #FD1D1D → #FCB045
   ├─ Border: 1px solid white
   ├─ Border Radius: 12px
   ├─ Padding: 4px horizontal, 2px vertical
   └─ Text: "Live"
      ├─ Font: 10px, weight: 600
      ├─ Color: white
      └─ Width: 20px
```

**9. Avatar with Initials (без фото)**
```
Container: 56×56
└─ Avatar: 48×48 (position: 4px, 4px)
   ├─ Background: #D9DDE2
   ├─ Border Radius: 40px
   └─ Text: "AH" (position: 4px, 17px)
      ├─ Font: 16px, weight: 600
      ├─ Color: white
      ├─ Align: center
      └─ Width: 48px
```

**10. Avatar with Icon Placeholder**
```
Container: 56×56
└─ Avatar: 48×48 (position: 4px, 4px)
   ├─ Background: #D9DDE2
   ├─ Border Radius: 40px
   └─ Icon: 24×24 (centered, padding: 12px horizontal)
```

#### Spacing & Layout (из кода)

- **Row spacing between elements**: 8px
- **Row internal spacing**: 10px
- **Avatar position offset**: 4px (left, top)
- **Badge position (top-right)**: left: 36px, top: 0
- **Badge position (bottom)**: left: 0, top: 36px

#### Stories Border Specification

- **Border Width**: 2px
- **Border Radius**: 30px
- **Blue Border Color**: #4141E6 (--color-border-stories-blue) - для непросмотренных stories
- **Pink Border Color**: #FC466B (--color-border-stories-pink) - для highlighted stories
- **Container Size**: 56×56 (на 8px больше чем аватар для вмещения border)

#### Badges on Avatars

**Notification Badge (Top-Right):**
- Size: 20×20
- Background: #4141E6 (--color-accent-blue)
- Border Radius: 20px
- Position: top: 0, right: 0 (relative to 56×56 container)
- Text: Font 10px, weight 600, color white

**Online Indicator (Bottom-Right):**
- Size: 14×14
- Background: #11BB8D (--color-status-online)
- Border: 1px solid white
- Border Radius: circle
- Position: bottom: 0, right: 0

**Live Badge (Bottom-Center):**
- Size: 28×14
- Gradient: linear-gradient(90deg, #833AB4, #FD1D1D, #FCB045)
- Border: 1px solid white
- Border Radius: 12px
- Text: "Live", Font 10px, weight 600, color white

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
