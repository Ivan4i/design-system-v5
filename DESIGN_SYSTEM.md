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
9. [Charts & Graphs](#charts--graphs)
10. [Date & Time Pickers](#date--time-pickers)
11. [Progress Indicators & Steppers](#progress-indicators--steppers)
12. [Input Fields](#input-fields)
13. [Snackbars & Toasts](#snackbars--toasts)
14. [Mobile Screens & Layouts](#mobile-screens--layouts)
15. [Shopping & Orders](#shopping--orders)
16. [Cards & Listings](#cards--listings)

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
--color-black: #09101D;
```

### Background Colors

```css
/* Фоновые цвета */
--color-bg-primary: #FFFFFF;           /* Основной фон */
--color-bg-secondary: #D9DDE2;         /* Вторичный фон с opacity 0.25 */
--color-bg-overlay: rgba(217, 221, 226, 0.25);  /* Overlay фон */
```

### Text Colors

```css
/* Цвета текста из Flutter кода */
--color-text-primary: #09101D;         /* Основной текст */
--color-text-primary-alt: #23262B;     /* Альтернативный основной (чуть светлее) */
--color-text-secondary: #414249;       /* Вторичный текст */
--color-text-tertiary: #747B84;        /* Третичный текст (подписи) */
```

### Accent Colors

```css
/* Акцентные цвета */
--color-primary: #4141E6;              /* Primary синий/фиолетовый */
--color-primary-alt: #0B24FB;          /* Альтернативный синий для прогресса */
--color-primary-light: rgba(11, 36, 251, 0.10);  /* #0B24FB с 10% opacity */
--color-success: #11BB8D;              /* Зеленый для успеха/рейтингов */
--color-error: #E24949;                /* Красный для выходных/ошибок */
```

### Border Colors

```css
/* Цвета границ */
--color-border-primary: #EAEEF2;       /* Основной цвет разделителей */
--color-border-secondary: #D9DDE2;     /* Вторичный цвет границ */
```

### Shadow Colors

```css
/* Тени из Flutter кода */
--shadow-primary: rgba(101, 99, 255, 0.40);  /* #6563FF с 40% opacity для теней кнопок */
```

### Gradient Colors

```css
/* Градиенты из TinyCards компонентов */

/* Сине-фиолетовый градиент */
--gradient-purple-blue-start: #7F7FD5;
--gradient-purple-blue-end: #86A8E7;

/* Светло-голубой градиент */
--gradient-light-blue-start: #E0EAFC;
--gradient-light-blue-end: #CFDEF3;

/* Темный сине-серый градиент */
--gradient-dark-blue-start: #141E30;
--gradient-dark-blue-end: #243B55;
```

### Additional UI Colors

```css
/* Дополнительные цвета для UI элементов */
--color-border-accent: #7B61FF;            /* Фиолетовая граница для контейнеров */
--color-bg-card: #F4F6F9;                  /* Фон для карточек */
--color-bg-icon-button: #EAEEF2;           /* Фон для иконочных кнопок */
--color-border-white-transparent: rgba(255, 255, 255, 0.07);  /* Белая граница с прозрачностью */
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
/* Из Flutter кода используется единый line height */
--line-height-base: 1.40;     /* Универсальное значение для всех текстов */

/* Дополнительные значения */
--line-height-12: 0.75rem;    /* 12px */
--line-height-16: 1rem;       /* 16px */
--line-height-20: 1.25rem;    /* 20px */
--line-height-24: 1.5rem;     /* 24px */
--line-height-32: 2rem;       /* 32px */
--line-height-36: 2.25rem;    /* 36px */
--line-height-40: 2.5rem;     /* 40px */
```

### Text Styles (из Flutter приложения)

#### Heading 1 (Accounts, Title)
- **Bold**: Font: 24px (1.5rem), Weight: 700, Line Height: 1.40, Family: Archivo
- Используется для основных заголовков страниц и секций

#### Heading 2 (Dialog Titles)
- **Bold**: Font: 24px (1.5rem), Weight: 700, Line Height: 1.40, Family: Archivo
- Используется для заголовков модальных окон

#### Body Large (Menu Items, Settings)
- **Semibold**: Font: 16px (1rem), Weight: 600, Line Height: 1.40, Family: Archivo
- **Regular**: Font: 16px (1rem), Weight: 400, Line Height: 1.40, Family: Archivo
- Используется для пунктов меню, настроек

#### Body Medium (Ratings, Buttons)
- **Semibold**: Font: 16px (1rem), Weight: 600, Line Height: 1.40, Family: Archivo
- **Bold**: Font: 16px (1rem), Weight: 700, Line Height: 1.40, Family: Archivo
- Используется для рейтингов, значений, кнопок

#### Callout (Primary Buttons)
- **Semibold**: Font: 15px (0.9375rem), Weight: 600, Line Height: 1.40, Family: Archivo
- Используется для текста на основных кнопках

#### Body Small (List Items, Labels)
- **Semibold**: Font: 14px (0.875rem), Weight: 600, Line Height: 1.40, Family: Archivo
- **Regular**: Font: 14px (0.875rem), Weight: 400, Line Height: 1.40, Family: Archivo
- Используется для элементов списков, меток, описаний

#### Caption Large (Tags, Badges)
- **Semibold**: Font: 13px (0.8125rem), Weight: 600, Line Height: 1.40, Family: Archivo
- **Regular**: Font: 13px (0.8125rem), Weight: 400, Line Height: 1.40, Family: Archivo
- Используется для небольших меток, тегов, подписей

---

## Spacing & Layout

### Spacing Scale (из Flutter кода)

```css
/* Основные значения из реального приложения */
--space-0: 0;
--space-1: 0.125rem;  /* 2px */
--space-2: 0.5rem;    /* 8px */
--space-2-5: 0.625rem;/* 10px */
--space-3: 0.75rem;   /* 12px */
--space-4: 1rem;      /* 16px */
--space-5: 1.25rem;   /* 20px */
--space-6: 1.5rem;    /* 24px */
--space-7-5: 1.875rem;/* 30px */
--space-8: 2rem;      /* 32px */
--space-10: 2.5rem;   /* 40px */

/* Специфичные значения для мобильного интерфейса */
--space-handle: 0.3125rem;   /* 5px - для handle индикатора */
--space-badge: 0.8125rem;    /* 13px - для padding в badge */
```

### Border Radius (из Flutter кода)

```css
/* Значения из реального приложения */
--radius-none: 0;
--radius-xs: 0.0625rem;   /* 1px - для тонких разделителей */
--radius-base: 0.9375rem; /* 15px - для кнопок и карточек */
--radius-lg: 1.25rem;     /* 20px - для bottom sheets */
--radius-xl: 1.875rem;    /* 30px - для верхних углов модальных окон */
--radius-2xl: 2.5rem;     /* 40px - для больших закруглений */
--radius-full: 6.25rem;   /* 100px - для кругов */
```

### Shadows (из Flutter кода)

#### Button Shadows

```css
/* Тень для primary кнопки */
--shadow-button-primary: 0 0 20px 0 rgba(101, 99, 255, 0.40);
```

#### Additional Shadows

```css
/* Стандартные тени для элементов */
--shadow-xs: 0 1px 2px 0 rgba(0, 0, 0, 0.05);
--shadow-sm: 0 1px 3px 0 rgba(0, 0, 0, 0.1), 0 1px 2px 0 rgba(0, 0, 0, 0.06);
--shadow-base: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
--shadow-md: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
--shadow-lg: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
--shadow-xl: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
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
/* Значения opacity из Flutter приложения */
--opacity-0: 0;
--opacity-10: 0.1;     /* Используется для light backgrounds (#0B24FB с 10% opacity) */
--opacity-25: 0.25;    /* Используется для overlay backgrounds (#D9DDE2 с 25% opacity) */
--opacity-40: 0.40;    /* Используется для теней кнопок */
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

## Мобильные компоненты (из Flutter приложения)

### 1. Bottom Sheet

Bottom sheet - модальное окно, которое выдвигается снизу экрана.

**Структура:**
- **Width**: 375px (полная ширина экрана)
- **Background**: #FFFFFF
- **Border Radius**: 20px (только верхние углы - topLeft, topRight: 30px)
- **Border**: 1px solid #FFFFFF

**Handle (Индикатор сверху):**
- **Size**: 40px × 3px
- **Color**: #D9DDE2
- **Border Radius**: 100px (полное закругление)
- **Position**: По центру, padding: 8px по вертикали, 167px по горизонтали

**Padding внутри:**
- Horizontal: 16px
- Vertical: 10px

#### Варианты использования
1. **Accounts Sheet** - список аккаунтов
2. **Trust Dialog** - диалог подтверждения
3. **Expiration Period Selector** - выбор периода
4. **Settings Menu** - меню настроек
5. **Rating Sheet** - форма рейтинга

---

### 2. List Items

Элементы списка для различных целей (аккаунты, настройки, меню).

**Стандартный List Item:**
- **Height**: auto (min 48px с padding 12px vertical)
- **Padding**: 12px vertical, 16px horizontal
- **Background**: #FFFFFF
- **Border**: 1px solid #FFFFFF

**С иконкой:**
- **Icon Size**: 40px × 40px
- **Icon Background**: rgba(11, 36, 251, 0.10) - светло-синий
- **Icon Border Radius**: 100px (круг)
- **Icon Padding**: 13px внутри
- **Gap между иконкой и текстом**: 12px

**Текст:**
- **Title**: 14px, Weight: 600, Color: #09101D
- **Subtitle**: 14px, Weight: 400, Color: #414249 (если есть)
- **Value справа**: 14px, Weight: 600, Color: #09101D

**Trailing элементы:**
- **Chevron**: 24px × 24px

---

### 3. Buttons

#### Primary Button
- **Height**: 44px
- **Padding**: 10px horizontal, 16px vertical
- **Background**: #4141E6 (синий/фиолетовый)
- **Color**: #FFFFFF (белый текст)
- **Border Radius**: 15px
- **Font**: 15px, Weight: 600, Family: Archivo
- **Shadow**: 0 0 20px 0 rgba(101, 99, 255, 0.40)

**Пример**: "No, Go back", "Vote"

#### Secondary Button
- **Height**: 44px
- **Padding**: 10px horizontal, 16px vertical
- **Background**: transparent или #09101D (dark)
- **Color**: #09101D или #FFFFFF
- **Border Radius**: 15px
- **Font**: 14px или 16px, Weight: 600-700, Family: Archivo

**Пример**: "Appk" (темная версия)

---

### 4. Badges & Tags

#### Badge "New"
- **Height**: 36px
- **Padding**: 10px vertical, 16px horizontal
- **Background**: rgba(11, 36, 251, 0.10) - светло-синий с 10% opacity
- **Border Radius**: 15px
- **Font**: 13px, Weight: 600, Color: #4141E6
- **Icon + Text**: Gap 8px между иконкой (16px) и текстом

---

### 5. Radio Buttons / Selection

Используются для выбора опций (например, периода истечения).

**Selected State:**
- **Outer Circle**: 12px × 12px
- **Border**: 3px solid #4141E6
- **Inner Dot**: 6px × 6px, Background: #4141E6
- **Position**: Centered

**Unselected State:**
- **Outer Circle**: 12px × 12px
- **Border**: 3px solid #EAEEF2
- **Background**: rgba(11, 36, 251, 0.10)

**Padding**: 10px vertical, 2px внутри

---

### 6. Dividers

Горизонтальные разделители между элементами.

**Standard Divider:**
- **Height**: 1px
- **Color**: #EAEEF2
- **Padding**: 5px vertical (в контейнере с 10px vertical)
- **Width**: 100% (full width)

**Accent Divider (для активных элементов):**
- **Height**: 2px
- **Width**: 40px
- **Color**: #4141E6
- **Border Radius**: 1px

---

### 7. Headers & Titles

#### Section Header (внутри Bottom Sheet)
- **Font**: 24px, Weight: 700, Color: #09101D, Family: Archivo
- **Line Height**: 1.40
- **Padding**: 12px vertical

**С кнопкой справа:**
- **Title**: слева
- **Action Button/Badge**: справа (например, "New" badge)

#### Dialog Title
- **Font**: 24px, Weight: 700, Color: #09101D
- **Description**: 14px, Weight: 400, Color: #414249
- **Icon**: 40px × 40px (опционально слева)
- **Gap**: 12px между иконкой и текстом

---

### 8. Rating Component

Компонент для отображения рейтинга.

**Rating Circle:**
- **Size**: 56px × 56px (outer), 48px × 48px (inner)
- **Background**: #11BB8D (зеленый)
- **Border Radius**: 40px (круг)
- **Text**: 16px, Weight: 600, Color: #FFFFFF
- **Value**: "4.6" (пример)

**Rating Layout:**
- **Icon/Circle**: 56px слева
- **Content**: справа
  - Title: 24px, Weight: 700, "Rating 👌🏻"
  - Subtitle: 14px, Weight: 400, "You are in a good hands"
- **Gap**: 12px между кругом и контентом

**Stars/Icons:**
- **Size**: 44px × 44px each
- **Layout**: Horizontal row, centered
- **Padding**: 10px top, 30px bottom

---

### 9. Screen Dimensions

**Стандартный размер экрана (iPhone):**
- **Width**: 375px
- **Height**: 812px

**Status Bar:**
- **Height**: 44px
- **Elements inside**: Time, battery, signal indicators

**Home Indicator (Bottom):**
- **Width**: 134px
- **Height**: 5px
- **Position**: Bottom center (21px from bottom)
- **Color**: #09101D
- **Border Radius**: 100px

---

### 10. Icon Sizes

**Из реального приложения:**
- **XS**: 14.40px (positioned icons)
- **SM**: 16px (badges, small UI elements)
- **Base**: 16.80px (standard icons)
- **MD**: 24px (trailing icons, chevrons)
- **LG**: 40px (list item icons)
- **XL**: 44px (rating stars, action buttons)

---

## Tiny Cards (компактные карточки для desktop/tablet)

Система компактных карточек различных размеров для отображения информации, статистики, продуктов и профилей.

### Container Wrapper

**Основной контейнер для коллекции карточек:**
- **Width**: 2950px (широкий контейнер)
- **Height**: 460px
- **Padding**: 100px (все стороны)
- **Border**: 1px solid #7B61FF (фиолетовая рамка)
- **Border Radius**: 15px
- **Layout**: Row с spacing 100px между карточками

---

### 1. Product Card (с градиентом)

**Размер**: 160px × 160px

**Стили:**
- **Padding**: 10px
- **Border Radius**: 20px
- **Gradient**: Linear (#7F7FD5 → #86A8E7)
- **Direction**: Horizontal (left to right)

**Изображение продукта:**
- **Size**: 98.77px × 98.77px
- **Border Radius**: 15px
- **Position**: Top left

**Иконка действия:**
- **Size**: 24px × 24px
- **Padding**: 8px контейнер, 2px внутри
- **Border Radius**: 20px контейнер, 100px иконка
- **Position**: Top right

**Текст описания:**
- **Font**: 16px, Weight: 400, Color: #FFFFFF
- **Line Height**: 1.40
- **Max Width**: 140px
- **Position**: Bottom

**Пример**: "Select delivery by drone"

---

### 2. Product Card (светлая)

**Размер**: 160px × 160px

**Стили:**
- **Padding**: 15px
- **Background**: #F4F6F9
- **Border**: 0.50px solid rgba(255, 255, 255, 0.07)
- **Border Radius**: 20px

**Изображение продукта:**
- **Size**: 79.01px × 79.01px
- **Border Radius**: 15px
- **Fit**: Cover

**Иконка действия:**
- **Size**: 14px × 14px
- **Padding**: 8px контейнер
- **Position**: Top right

**Текст:**
- **Title**: 16px, Weight: 700, Color: #09101D
- **Subtitle**: 14px, Weight: 400, Color: #747B84
- **Gap**: 8px между title и subtitle
- **Max Width**: 130px

**Пример**: "Apple Watch" / "Add in wishlist"

---

### 3. Balance Card

**Размер**: 160px × 120px

**Стили:**
- **Padding**: 12px
- **Background**: #F4F6F9
- **Border**: 0.50px solid rgba(255, 255, 255, 0.07)
- **Border Radius**: 20px

**Структура:**
1. **Дата**: 13px, Weight: 400, Color: #D9DDE2
2. **Заголовок**: 18px, Weight: 700, Color: #09101D
3. **Значение**: 14px, Weight: 600, Color: #09101D

**Пример**: "Jun 28, 2021" / "Balance" / "1452$"

---

### 4. User Profile Card (с градиентом)

**Размер**: 160px × 120px

**Стили:**
- **Padding**: 12px
- **Gradient**: Linear (#E0EAFC → #CFDEF3)
- **Border**: 0.50px solid rgba(255, 255, 255, 0.07)
- **Border Radius**: 20px

**Header:**
- **Name**: 16px, Weight: 700, Color: #09101D
- **Location**: 12px, Weight: 400, Color: #09101D
- **Icon**: 14px, Padding: 5px

**Avatar:**
- **Size**: 56px × 56px (outer), 48px × 48px (inner)
- **Border Radius**: 40px (круг)
- **Background fallback**: #D9DDE2

**Gap**: 5px между header и avatar

---

### 5. Product Card Dark (горизонтальная)

**Размер**: 160px × 80px

**Стили:**
- **Padding**: 10px top/bottom, 15px left
- **Gradient**: Linear (#141E30 → #243B55) - темный
- **Border**: 0.50px solid rgba(255, 255, 255, 0.07)
- **Border Radius**: 20px

**Layout**: Horizontal row

**Текст:**
- **Font**: 14px, Weight: 600, Color: #FFFFFF
- **Max Width**: 67.50px

**Изображение:**
- **Size**: 60px × 60px
- **Border Radius**: 15px
- **Fit**: Contain
- **Position**: Right side

**Пример**: "Apple Watch"

---

### 6. Growth Indicator Card

**Размер**: 160px × 60px

**Стили:**
- **Padding**: 10px
- **Background**: #F4F6F9
- **Border**: 0.50px solid rgba(255, 255, 255, 0.07)
- **Border Radius**: 20px

**Иконка:**
- **Container**: 40px × 40px, Padding: 8px
- **Background**: #EAEEF2
- **Border Radius**: 20px
- **Icon Size**: 24px × 24px

**Текст:**
- **Value**: 18px, Weight: 700, Color: #11BB8D (зеленый)
- **Label**: 13px, Weight: 600, Color: #09101D
- **Max Width**: 90px

**Gap**: 10px между иконкой и текстом

**Пример**: "21%" / "Growth"

---

### 7. Icon Label Card

**Размер**: 160px × 60px

**Стили:**
- **Padding**: 10px
- **Background**: #F4F6F9
- **Border Radius**: 15px

**Иконка:**
- **Container**: 40px × 40px, Padding: 8px
- **Background**: rgba(11, 36, 251, 0.10) - светло-синий
- **Border Radius**: 30px
- **Icon Size**: 24px × 24px, Padding: 4px внутри

**Текст:**
- **Font**: 14px, Weight: 600, Color: #09101D

**Gap**: 10px между иконкой и текстом

**Пример**: "Database"

---

### 8. User Info Card (вертикальная)

**Размер**: 160px × auto (минимум 50px)

**Стили:**
- **Padding**: 10px top/bottom, 15px left, 10px right
- **Background**: #F4F6F9
- **Border**: 0.50px solid rgba(255, 255, 255, 0.07)
- **Border Radius**: 20px

**Текст:**
- **Name**: 16px, Weight: 700, Color: #09101D
- **Location**: 14px, Weight: 400, Color: #414249
- **Max Width**: 135px

**Gap**: 8px между name и location

---

### 9. Avatar with Status

**Компонент для отображения аватара со статусом.**

**Avatar:**
- **Size**: 56px × 56px (outer), 48px × 48px (inner)
- **Border Radius**: 40px (круг)
- **Background fallback**: #D9DDE2

**Status Indicator:**
- **Size**: 12px × 12px
- **Padding**: 2px horizontal, 4px vertical (внутри)
- **Background**: #4141E6
- **Border**: 2px solid #FFFFFF
- **Border Radius**: 20px
- **Position**: Bottom right of avatar

**Text Label:**
- **Font**: 13px, Weight: 400, Color: #09101D
- **Text Align**: Center

**Layout:**
- Avatar сверху
- Gap 5px
- Status indicator + Name снизу (horizontal row, gap 5px)

---

### Общие параметры для Tiny Cards

**Размеры карточек:**
- **Extra Small**: 160px × 60px
- **Small**: 160px × 80px
- **Medium**: 160px × 120px
- **Large**: 160px × 160px

**Border Radius:**
- **Card**: 15px или 20px
- **Images**: 15px
- **Avatars**: 40px (круг)
- **Icon buttons**: 20px или 30px
- **Small elements**: 100px (полный круг)

**Spacing:**
- **Card padding**: 10px, 12px, 15px (зависит от размера)
- **Between cards**: 100px
- **Internal gaps**: 5px, 8px, 10px

**Border:**
- **Standard**: 0.50px solid rgba(255, 255, 255, 0.07)
- **Accent**: 1px solid #7B61FF

**Gradients:**
Все градиенты - Linear, Horizontal (0° to 180°):
- Purple-Blue: #7F7FD5 → #86A8E7
- Light-Blue: #E0EAFC → #CFDEF3
- Dark-Blue: #141E30 → #243B55

---

## Charts & Graphs

Система визуализации данных на основе bar chart компонентов для мобильных экранов.

### Bar Chart (Hourly View)

Вертикальный bar chart для отображения почасовых данных с 60 точками измерений.

#### Container

**Размеры:**
- **Width**: 375px (полная ширина мобильного экрана)
- **Height**: auto (зависит от высоты баров)

**Padding варианты:**
1. **Вариант 1** (компактный):
   - Horizontal: 16px
   - Vertical: 10px
2. **Вариант 2** (расширенный):
   - Horizontal: 16px
   - Top: 40px
   - Bottom: 10px (или auto)

#### Bar Specifications

**Структура:**
- **Количество баров**: 60 (Expanded widgets)
- **Layout**: Horizontal Row
- **Alignment**: `crossAxisAlignment.end` (выравнивание по нижнему краю)
- **Spacing**: 1px между барами

**Стили баров:**
- **Color**: #D9DDE2 (светло-серый)
- **Border Radius**:
  - Вариант 1: 1px (минимальное закругление)
  - Вариант 2: 4px (заметное закругление)
- **Shape**: `RoundedRectangleBorder`

**Высоты баров:**
Вариативные высоты от 38px до 155px в зависимости от данных.

Полный набор высот (60 значений):
```
60, 96, 63, 70, 100, 118, 96, 63, 38, 118,
96, 63, 70, 79, 155, 96, 63, 38, 118, 96,
63, 70, 79, 155, 96, 63, 70, 79, 118, 96,
63, 38, 79, 96, 63, 70, 100, 118, 96, 63,
38, 118, 96, 63, 70, 79, 155, 96, 63, 38,
118, 96, 63, 70, 79, 155, 96, 63, 38, 118
```

#### Layout Patterns

**Pattern 1: Компактный график (малый padding)**
- Используется для карточек с ограниченным пространством
- Vertical padding: 10px
- Высота баров визуально занимает большую часть карточки
- BorderRadius: 1px для более "плотного" вида

**Pattern 2: Расширенный график (большой padding)**
- Используется для полноэкранных view или секций с акцентом
- Top padding: 40px (пространство для заголовков)
- BorderRadius: 4px для более "мягкого" вида
- Больше визуального пространства вокруг графика

#### Использование в UI

**Контекст применения:**
- Отображение почасовых метрик (просмотры, активность, трафик)
- Краткосрочные тренды (последний час, текущий день)
- Мониторинг реального времени
- Компактные дашборды на мобильных устройствах

**CSS Variables:**

```css
/* Bar Chart Colors */
--chart-bar-color-primary: #D9DDE2;

/* Bar Chart Dimensions */
--chart-bar-gap: 1px;
--chart-bar-radius-compact: 1px;
--chart-bar-radius-comfortable: 4px;

/* Bar Chart Container */
--chart-container-width-mobile: 375px;
--chart-padding-horizontal: 16px;
--chart-padding-vertical-compact: 10px;
--chart-padding-vertical-expanded: 40px;
```

#### Интерактивность

**Рекомендации для взаимодействия:**
- **Tap/Click**: Показать tooltip с точным значением
- **Hover** (desktop): Highlight бара при наведении
- **Animation**: Анимация появления баров снизу вверх (0.3s ease-out)
- **Loading state**: Skeleton loader с серыми барами одинаковой высоты

#### Адаптивность

**Mobile (375px):**
- Полная ширина контейнера
- 60 баров с gap 1px
- Horizontal scroll при необходимости

**Tablet (768px+):**
- Может использоваться та же компоновка
- Или увеличение количества баров для большей детализации

**Desktop (1024px+):**
- Рассмотреть альтернативные визуализации (line chart, area chart)
- Или группировка нескольких bar charts side-by-side

#### Accessibility

**Доступность графиков:**
- **ARIA Label**: `aria-label="Hourly data visualization chart"`
- **Role**: `role="img"` для всего графика
- **Alt description**: Текстовое описание данных для screen readers
- **Keyboard navigation**: Tab для перемещения между барами (если интерактивные)
- **Color contrast**: Цвет #D9DDE2 на белом фоне - достаточный контраст

#### Примеры кода

**Вариант 1 (Компактный):**
```css
.bar-chart-container {
  width: var(--chart-container-width-mobile);
  padding: var(--chart-padding-vertical-compact) var(--chart-padding-horizontal);
  display: flex;
  flex-direction: row;
  align-items: flex-end;
  gap: var(--chart-bar-gap);
}

.bar-chart-item {
  flex: 1;
  background: var(--chart-bar-color-primary);
  border-radius: var(--chart-bar-radius-compact);
  min-height: 38px;
  max-height: 155px;
}
```

**Вариант 2 (Расширенный):**
```css
.bar-chart-container--expanded {
  width: var(--chart-container-width-mobile);
  padding: var(--chart-padding-vertical-expanded) var(--chart-padding-horizontal) var(--chart-padding-vertical-compact);
  display: flex;
  flex-direction: row;
  align-items: flex-end;
  gap: var(--chart-bar-gap);
}

.bar-chart-item--rounded {
  flex: 1;
  background: var(--chart-bar-color-primary);
  border-radius: var(--chart-bar-radius-comfortable);
  transition: opacity 0.2s ease;
}

.bar-chart-item--rounded:hover {
  opacity: 0.8;
}
```

---

## Date & Time Pickers

Система компонентов для выбора даты и времени в мобильном приложении.

### Time Slots Grid (Сетка выбора времени)

Компонент для выбора временных слотов с интервалом 30 минут.

#### Container

**Размеры:**
- **Width**: 375px (полная ширина мобильного экрана)
- **Padding**: 16px horizontal, 10px vertical

**Layout:**
- **Spacing между рядами**: 5px (между rows), 10px (внутри Column)
- **Grid**: 5 columns per row
- **Gap между слотами**: 10px

#### Time Slot Button

**Размеры:**
- **Height**: 40px
- **Padding**: 10px (all sides)
- **Border Radius**: 15px
- **Width**: Expanded (равномерное распределение)

**Typography:**
- **Font**: 12px, Weight: 400, Family: Archivo, Line height: 1.40
- **Text Format**: "HH:MM" (например, "10:00", "10:30")

**States:**

1. **Selected (выбранное время):**
   - Background: #09101D (темный)
   - Text Color: #FFFFFF (белый)
   - Пример: "10:00"

2. **Available (доступное время):**
   - Background: #F4F6F9 (светло-серый)
   - Text Color: #09101D (темный)
   - Пример: "10:30", "11:00", "11:30" и т.д.

3. **Disabled (недоступное время):**
   - Background: transparent
   - Text Color: #D9DDE2 (серый)
   - Text Decoration: line-through (зачеркнутый)
   - Пример: "20:30", "21:00", "21:30", "22:00"

**Time Range:**
- От 10:00 до 22:00
- Интервал: 30 минут
- Всего слотов: 25 (5 рядов × 5 колонок)

**CSS Variables:**

```css
/* Time Slot Dimensions */
--time-slot-height: 40px;
--time-slot-padding: 10px;
--time-slot-radius: 15px;
--time-slot-gap: 10px;

/* Time Slot Colors */
--time-slot-bg-selected: #09101D;
--time-slot-text-selected: #FFFFFF;
--time-slot-bg-available: #F4F6F9;
--time-slot-text-available: #09101D;
--time-slot-text-disabled: #D9DDE2;
```

---

### Horizontal Date Picker (Горизонтальный выбор дат)

Компонент для прокрутки и выбора даты в горизонтальной полосе.

#### Container

**Размеры:**
- **Width**: 375px (полная ширина экрана)
- **Padding**: bottom 10px
- **Layout**: Horizontal Row
- **Spacing**: 2px между карточками

#### Date Card

**Размеры:**
- **Width**: 50px (фиксированная)
- **Height**: auto
- **Padding**: 14px horizontal, 8px vertical
- **Border Radius**: 15px

**Структура:**
- **Day Label** (верхняя строка): SAT, SUN, MON, TUE, WEN, THU, FRI
- **Date Number** (нижняя строка): 12, 13, 14, 15, 16, 17, 18, 19

**Typography:**

1. **Day Label:**
   - Font: 10px, Weight: 600, Family: Archivo, Line height: 1.40
   - Text Align: Center
   - Text Transform: Uppercase

2. **Date Number:**
   - Font: 14px, Weight: 600, Family: Archivo, Line height: 1.40
   - Text Align: Center

**Internal Spacing:**
- **Gap между Day и Date**: 2px

**States:**

1. **Selected (выбранная дата):**
   - Background: #09101D (темный)
   - Day Label Color: #FFFFFF (белый)
   - Date Number Color: #FFFFFF (белый)
   - Пример: "TUE 15"

2. **Available Weekday (доступный будний день):**
   - Background: #FFFFFF (белый)
   - Day Label Color: #09101D (темный)
   - Date Number Color: #09101D (темный)
   - Пример: "MON 14", "WEN 16"

3. **Available Weekend (доступные выходные):**
   - Background: #FFFFFF (белый)
   - Day Label Color: #E24949 (красный)
   - Date Number Color: #09101D (темный)
   - Пример: "SAT 12", "SUN 13", "SAT 19"

4. **Disabled (недоступная дата):**
   - Background: #FFFFFF (белый)
   - Day Label Color: #D9DDE2 (серый)
   - Date Number Color: #D9DDE2 (серый)
   - Пример: "THU 17", "FRI 18"

**CSS Variables:**

```css
/* Date Card Dimensions */
--date-card-width: 50px;
--date-card-padding-horizontal: 14px;
--date-card-padding-vertical: 8px;
--date-card-radius: 15px;
--date-card-gap: 2px;

/* Date Card Colors */
--date-card-bg-selected: #09101D;
--date-card-text-selected: #FFFFFF;
--date-card-bg-available: #FFFFFF;
--date-card-text-weekday: #09101D;
--date-card-text-weekend: #E24949;
--date-card-text-disabled: #D9DDE2;
```

---

### Monthly Calendar (Месячный календарь)

Полноценный месячный календарь с выбором дат, диапазонов и отображением событий.

#### Container

**Размеры:**
- **Width**: 375px (полная ширина экрана)
- **Padding**: 16px horizontal, 10px vertical
- **Spacing**: 30px (между header и calendar grid)

#### Month/Year Header

**Layout:**
- **Container Padding**: 14px horizontal
- **Height**: 40px (для navigation)
- **Structure**: Left Arrow | Month Year | Right Arrow

**Elements:**

1. **Navigation Arrows:**
   - Size: 24px × 24px
   - Position: Left and Right edges

2. **Month Text:**
   - Font: 14px, Weight: 700, Family: Archivo, Line height: 1.40
   - Color: #09101D
   - Padding: top 5px, right 5px, bottom 5px
   - Пример: "February"

3. **Year Text:**
   - Font: 14px, Weight: 700, Family: Archivo, Line height: 1.40
   - Color: #09101D
   - Width: 40px
   - Padding: top 5px, right 5px, bottom 5px
   - Пример: "2022"

#### Day Names Row

**Размеры:**
- **Height**: 40px
- **Padding**: 5px per cell
- **Layout**: 7 equal columns (Mon-Sun)

**Typography:**
- **Font**: 12px, Weight: 400, Family: Archivo, Line height: 1.40
- **Color**: #09101D
- **Text Align**: Center
- **Days**: Mon, Tue, Wen, Thu, Fri, Sat, Sun

#### Calendar Grid

**Layout:**
- **Structure**: 7 columns (дни недели) × 5-6 rows (недели)
- **Row Padding**: 4px vertical
- **Cell**: Expanded width × 40px height

#### Calendar Cell (Date)

**Размеры:**
- **Size**: auto width (Expanded) × 40px height
- **Padding**: 5px (standard) или 10px (selected/range)
- **Border Radius**: 15px (для selected и range)

**Typography:**
- **Date Number**: 12px, Weight: 400, Family: Archivo, Line height: 1.40
- **Event Value**: 7px, Weight: 600, Family: Archivo, Line height: 1.40

**States:**

1. **Current/Selected Date (текущая выбранная дата):**
   - Background: #09101D (темный)
   - Text Color: #FFFFFF (белый)
   - Border Radius: 15px
   - Padding: 10px
   - Пример: "11", "14", "15", "16", "26"

2. **Date Range (диапазон дат):**
   - Background: #F4F6F9 (светло-серый)
   - Text Color: #09101D (темный)
   - Border Radius: Conditional
     - **Start of range**: borderRadius только слева (topLeft: 15px, bottomLeft: 15px)
     - **Middle of range**: без borderRadius
     - **End of range**: borderRadius только справа (topRight: 15px, bottomRight: 15px)
   - Пример: "14-16" (3 дня), "26-28" + next month "1-2" (5 дней)

3. **Date with Event/Value (дата с событием):**
   - Date number: 12px, Weight: 400, Color: #09101D
   - Event value below (в отдельном контейнере):
     - Font: 7px, Weight: 600
     - Color: #11BB8D (зеленый для активных событий)
     - Color: #747B84 (серый для прошедших)
     - Height: 12px, Padding top: 2px
   - Примеры значений: "1 141", "1 610"
   - Пример: дата "1" с событием "1 141"

4. **Date with Dot Indicator (дата с точкой-индикатором):**
   - Date number: standard (12px, Weight: 400)
   - Dot below:
     - Character: "•"
     - Font: 13px, Weight: 600
     - Color: #09101D
     - Container: 12px height
   - Пример: дата "6" с точкой

5. **Other Month Dates (даты другого месяца):**
   - Text Color: #D9DDE2 (серый)
   - Padding: 5px
   - Пример: "27", "28", "29", "30", "31" (предыдущий месяц)

6. **Disabled Date (недоступная дата):**
   - Text Color: #D9DDE2 (серый)
   - Padding: 5px
   - Пример: "5", "7", "13"

7. **Available Date (обычная доступная дата):**
   - Background: transparent
   - Text Color: #09101D (темный)
   - Padding: 5px
   - Пример: "17", "18", "19", "20", "21", "22", "23", "24", "25"

**Complex Cell Structures:**

**Date Cell with Event (40px height):**
```
┌─────────────┐
│     Date    │ ← 28px (date number container)
│   "1 141"   │ ← 12px (event value container, padding top 2px)
└─────────────┘
```

**Date Cell in Range (40px height):**
```
Selected date inside range:
┌─────────────┐
│     14      │ ← Dark background (#09101D), white text
└─────────────┘

Middle date in range:
┌─────────────┐
│     15      │ ← Light gray background (#F4F6F9), no radius
└─────────────┘

End date in range:
┌─────────────┐
│     16      │ ← Light gray background, radius only right side
└─────────────┘
```

**CSS Variables:**

```css
/* Calendar Dimensions */
--calendar-width: 375px;
--calendar-padding-horizontal: 16px;
--calendar-padding-vertical: 10px;
--calendar-cell-height: 40px;
--calendar-cell-padding: 5px;
--calendar-cell-padding-selected: 10px;

/* Calendar Header */
--calendar-header-height: 40px;
--calendar-header-spacing: 30px;
--calendar-nav-icon-size: 24px;

/* Calendar Colors */
--calendar-bg-selected: #09101D;
--calendar-text-selected: #FFFFFF;
--calendar-bg-range: #F4F6F9;
--calendar-text-range: #09101D;
--calendar-text-other-month: #D9DDE2;
--calendar-text-disabled: #D9DDE2;
--calendar-event-color-active: #11BB8D;
--calendar-event-color-past: #747B84;

/* Calendar Cell Radius */
--calendar-cell-radius: 15px;
```

---

### Использование Date & Time Pickers

#### Time Slots Grid

**Когда использовать:**
- Бронирование встреч/услуг
- Выбор времени доставки
- Планирование событий
- Выбор из предопределенных временных слотов

**Best Practices:**
- Показывать доступные слоты для выбранной даты
- Четко обозначать недоступные времена (зачеркивание)
- Использовать темный фон для выбранного слота
- Ограничить количество слотов на экране (5×5 оптимально)

#### Horizontal Date Picker

**Когда использовать:**
- Быстрый выбор ближайших дат
- Просмотр доступности на несколько дней вперед
- Booking интерфейсы
- Компактное отображение календаря

**Best Practices:**
- Выделять выходные красным цветом
- Показывать 7-8 дат одновременно
- Поддерживать горизонтальную прокрутку
- Четко выделять выбранную дату

#### Monthly Calendar

**Когда использовать:**
- Выбор дат далеко в будущем/прошлом
- Просмотр событий/занятости на месяц
- Выбор диапазона дат
- Планирование с визуализацией

**Best Practices:**
- Показывать события под датами (value или dot)
- Поддерживать выбор диапазона дат
- Выделять текущую дату
- Серым цветом обозначать даты другого месяца
- Использовать цветовую кодировку для событий

#### Accessibility

**Для всех компонентов:**
- **ARIA Labels**: `aria-label="Select date"`, `aria-label="Select time slot"`
- **Role**: `role="button"` для каждого slot/date
- **Selected State**: `aria-selected="true"` для выбранных элементов
- **Disabled State**: `aria-disabled="true"` для недоступных
- **Keyboard Navigation**:
  - Arrow keys для перемещения между датами/слотами
  - Enter/Space для выбора
  - Tab для навигации между секциями
- **Screen Reader**: Объявлять выбранную дату/время полностью

#### Примеры кода

**Time Slot (Available):**
```css
.time-slot {
  height: var(--time-slot-height);
  padding: var(--time-slot-padding);
  background: var(--time-slot-bg-available);
  color: var(--time-slot-text-available);
  border-radius: var(--time-slot-radius);
  font: 400 12px/1.4 'Archivo', sans-serif;
  text-align: center;
  cursor: pointer;
  transition: background 0.2s ease;
}

.time-slot--selected {
  background: var(--time-slot-bg-selected);
  color: var(--time-slot-text-selected);
}

.time-slot--disabled {
  background: transparent;
  color: var(--time-slot-text-disabled);
  text-decoration: line-through;
  cursor: not-allowed;
}
```

**Date Card (Horizontal):**
```css
.date-card {
  width: var(--date-card-width);
  padding: var(--date-card-padding-vertical) var(--date-card-padding-horizontal);
  background: var(--date-card-bg-available);
  border-radius: var(--date-card-radius);
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: var(--date-card-gap);
}

.date-card__day {
  font: 600 10px/1.4 'Archivo', sans-serif;
  color: var(--date-card-text-weekday);
  text-transform: uppercase;
}

.date-card__day--weekend {
  color: var(--date-card-text-weekend);
}

.date-card__number {
  font: 600 14px/1.4 'Archivo', sans-serif;
  color: var(--date-card-text-weekday);
}

.date-card--selected {
  background: var(--date-card-bg-selected);
}

.date-card--selected .date-card__day,
.date-card--selected .date-card__number {
  color: var(--date-card-text-selected);
}
```

**Calendar Cell:**
```css
.calendar-cell {
  height: var(--calendar-cell-height);
  padding: var(--calendar-cell-padding);
  font: 400 12px/1.4 'Archivo', sans-serif;
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.calendar-cell--selected {
  background: var(--calendar-bg-selected);
  color: var(--calendar-text-selected);
  border-radius: var(--calendar-cell-radius);
  padding: var(--calendar-cell-padding-selected);
}

.calendar-cell--range {
  background: var(--calendar-bg-range);
  color: var(--calendar-text-range);
}

.calendar-cell--range-start {
  border-radius: var(--calendar-cell-radius) 0 0 var(--calendar-cell-radius);
}

.calendar-cell--range-end {
  border-radius: 0 var(--calendar-cell-radius) var(--calendar-cell-radius) 0;
}

.calendar-cell__event {
  font: 600 7px/1.4 'Archivo', sans-serif;
  color: var(--calendar-event-color-active);
  margin-top: 2px;
}
```

---

## Progress Indicators & Steppers

Система компонентов для отображения прогресса выполнения задач и многошаговых процессов.

### Step Indicators (Индикаторы шагов)

Точечные индикаторы для отображения прогресса в многошаговых процессах.

#### Container

**Размеры:**
- **Общий контейнер**: 18px × 18px
- **Внутренний круг**: 14px × 14px
- **Padding**: 2px top (для некоторых вариантов)
- **Border Radius**: 3px или 6px (для контейнера)

#### Step Dot

**Typography (Label):**
- **Font**: 10px, Weight: 600, Family: Archivo, Line height: 1.40
- **Color**: #09101D (темный)
- **Text Align**: Center
- **Content**: "Step name"
- **Position**: Below the dot (spacing 5px или 3px)

**States:**

1. **Active (текущий шаг):**
   - Dot: 14px × 14px, Background: #4141E6 (синий круг)
   - Container: 18px × 18px, padding top 2px
   - Label: visible below

2. **Completed (завершенный шаг):**
   - Outer circle: 18px × 18px, Background: #4141E6
   - Inner circle: 14px × 14px, Background: #4141E6
   - Border: 1px solid #FFFFFF (белая обводка внутри)
   - Position: 2px offset from outer
   - Label: visible below

3. **Inactive/Default (неактивный шаг):**
   - Dot: 14px × 14px, Background: #EAEEF2 (светло-серый)
   - Container: 18px × 18px, padding top 2px
   - Label: visible below

4. **Error (шаг с ошибкой):**
   - Dot: 14px × 14px, Background: #E24949 (красный)
   - Container: 18px × 18px, offset 2px
   - Label: visible below

5. **With Icon (с иконкой):**
   - Container: 17px × 17px (для иконки)
   - Position: 0.50px top padding
   - Spacing: 3px before label

**CSS Variables:**

```css
/* Step Indicator Dimensions */
--step-indicator-size: 18px;
--step-indicator-dot-size: 14px;
--step-indicator-padding: 2px;
--step-indicator-radius: 3px;
--step-indicator-spacing: 5px; /* spacing to label */

/* Step Indicator Colors */
--step-indicator-active: #4141E6;
--step-indicator-completed: #4141E6;
--step-indicator-completed-border: #FFFFFF;
--step-indicator-inactive: #EAEEF2;
--step-indicator-error: #E24949;
--step-indicator-label-color: #09101D;
```

---

### Circular Progress Indicators (Круговые прогресс-бары)

Круговые индикаторы прогресса с отображением процентов или времени внутри.

#### Sizes & Specifications

**Extra Large (64px):**
- **Size**: 64px × 64px
- **Border Width**: 5px
- **Background Ring**: #F4F6F9 (светло-серый)
- **Progress Ring**: #4141E6 (синий)
- **Text Inside**: 13px, Weight: 600, Family: Archivo
- **Text Position**: Centered (19px left, 23px top для "1:35")
- **Text Examples**: "1:35" (время), "15%" (процент)

**Large (48px):**
- **Size**: 48px × 48px
- **Border Width**: 4px
- **Background Ring**: #F4F6F9
- **Progress Ring**: #4141E6
- **Text Inside**: 11px, Weight: 600, Family: Archivo
- **Text Position**: Centered (12.33px left, 16px top)
- **Text Examples**: "1:35", "48%"

**Medium (36px):**
- **Size**: 36px × 36px
- **Border Width**: 3px
- **Background Ring**: #F4F6F9
- **Progress Ring**: #4141E6
- **Text Inside**: 10px, Weight: 600, Family: Archivo
- **Text Position**: Centered (7.67px left, 11px top)
- **Text Examples**: "1:35", "72%"

**Small (24px):**
- **Size**: 24px × 24px
- **Border Width**: 2px
- **Background Ring**: #F4F6F9
- **Progress Ring**: #4141E6
- **Text Inside**: 7px, Weight: 600, Family: Archivo
- **Text Position**: Centered (5px left, 7px top)
- **Text Examples**: "1:35", "85%"

**Structure:**
- **Background Ring**: Полный круг (360°), светло-серый фон
- **Progress Ring**: Частичный круг (0-360° в зависимости от прогресса), синий
- **OvalBorder**: Border side с указанным width

**CSS Variables:**

```css
/* Circular Progress Dimensions */
--circular-progress-xl-size: 64px;
--circular-progress-xl-border: 5px;
--circular-progress-lg-size: 48px;
--circular-progress-lg-border: 4px;
--circular-progress-md-size: 36px;
--circular-progress-md-border: 3px;
--circular-progress-sm-size: 24px;
--circular-progress-sm-border: 2px;

/* Circular Progress Colors */
--circular-progress-bg: #F4F6F9;
--circular-progress-fill: #4141E6;
--circular-progress-text-color: #000000; /* черный для контраста */

/* Circular Progress Text Sizes */
--circular-progress-text-xl: 13px;
--circular-progress-text-lg: 11px;
--circular-progress-text-md: 10px;
--circular-progress-text-sm: 7px;
```

---

### Linear Progress Bars (Линейные прогресс-бары)

Вертикальные или горизонтальные линейные индикаторы прогресса.

#### Vertical Linear Progress

**Размеры:**
- **Width**: 60px
- **Height**: 2px
- **Border Radius**: 10px (на концах)
- **Spacing между барами**: 58px

**States:**

1. **Active (полная заливка):**
   - Background: #0B24FB (синий, solid)
   - BorderRadius:
     - First bar: topLeft + bottomLeft: 10px
     - Middle bars: без radius
     - Last bar: topRight + bottomRight: 10px
   - Opacity: 1.0

2. **Partial Active (частично активный):**
   - Background: rgba(11, 36, 251, 0.30) - 30% opacity
   - BorderRadius: topRight + bottomRight: 10px (если последний в группе)
   - Opacity: 0.30

3. **Inactive (неактивный):**
   - Background: rgba(9, 16, 29, 0.10) - 10% opacity
   - BorderRadius: topRight + bottomRight: 10px (если последний в группе)
   - Opacity: 0.10

**Layout:**
- **Container**: Column с spacing 58px между барами
- **Padding**: 50px (all sides) в контейнере

#### Horizontal Linear Progress

**Размеры:**
- **Height**: 4px
- **Width**: Expanded (растягивается)
- **Border Radius**: 10px
- **Spacing между барами**: 50px

**States:**

1. **Filled (заполненный):**
   - Background: #4141E6 (синий)
   - BorderRadius: 10px

2. **Unfilled (незаполненный):**
   - Background: #F4F6F9 (светло-серый)
   - BorderRadius: 10px

**CSS Variables:**

```css
/* Linear Progress Dimensions */
--linear-progress-height-vertical: 2px;
--linear-progress-width-vertical: 60px;
--linear-progress-height-horizontal: 4px;
--linear-progress-radius: 10px;

/* Linear Progress Colors */
--linear-progress-active: #0B24FB; /* solid blue */
--linear-progress-partial: rgba(11, 36, 251, 0.30); /* 30% opacity */
--linear-progress-inactive: rgba(9, 16, 29, 0.10); /* 10% opacity */
--linear-progress-filled: #4141E6;
--linear-progress-unfilled: #F4F6F9;
```

---

### Stepper Progress (Пошаговый индикатор)

Горизонтальный степпер с точками и соединяющими линиями для многошаговых процессов.

#### Container

**Размеры:**
- **Width**: 375px (мобильный экран)
- **Padding**: 32px horizontal, 5px vertical
- **Height**: 30px (для step row)

#### Step Structure

**Elements:**
- **Step Dot**: 14px × 14px круг
- **Connector Line**: 4px height, Expanded width
- **Spacing between elements**: 3px

**Step Dot Container:**
- **Size**: 18px × 18px
- **Padding**: 2px top (для большинства)
- **Border Radius**: 3px (для контейнера)

**Connector Line:**
- **Height**: 4px
- **Width**: Expanded (автоматическое заполнение)
- **Border Radius**: 10px
- **Shape**: RoundedRectangleBorder

#### States

1. **Completed Step:**
   - **Dot**: 14px × 14px, Background: #4141E6 (синий)
   - **Connector Line**: Background: #4141E6 (синий)
   - Пример: первые 4 шага

2. **Active/Current Step:**
   - **Outer Circle**: 18px × 18px, Background: #4141E6
   - **Inner Circle**: 14px × 14px, Background: #4141E6
   - **Border**: 1px solid #FFFFFF (белая обводка)
   - **Connector Line After**: Background: #4141E6 (если текущий прогресс завершен)
   - Пример: 1-й шаг (с белой обводкой)

3. **Inactive/Future Step:**
   - **Dot**: 14px × 14px, Background: #F4F6F9 (светло-серый)
   - **Connector Line**: Background: #F4F6F9 (светло-серый)
   - Пример: последние 3 шага

**Layout Pattern:**
```
[Dot] —Line— [Dot] —Line— [Dot] —Line— [Dot] —Line— [Dot] —Line— [Dot] —Line— [Dot]
```

**Example Configuration (7 steps):**
- Step 1: Active (с белой обводкой) + синяя линия
- Steps 2-4: Completed (синие точки + синие линии)
- Step 5: Transition (последняя синяя точка + серая линия)
- Steps 6-7: Inactive (серые точки + серые линии)

**CSS Variables:**

```css
/* Stepper Dimensions */
--stepper-container-width: 375px;
--stepper-padding-horizontal: 32px;
--stepper-padding-vertical: 5px;
--stepper-dot-size: 14px;
--stepper-dot-container-size: 18px;
--stepper-line-height: 4px;
--stepper-line-radius: 10px;
--stepper-element-spacing: 3px;

/* Stepper Colors */
--stepper-completed-dot: #4141E6;
--stepper-completed-line: #4141E6;
--stepper-active-outer: #4141E6;
--stepper-active-inner: #4141E6;
--stepper-active-border: #FFFFFF;
--stepper-inactive-dot: #F4F6F9;
--stepper-inactive-line: #F4F6F9;
```

---

### Использование Progress Indicators

#### Step Indicators

**Когда использовать:**
- Обзор многошагового процесса
- Навигация между шагами
- Отображение статуса выполнения
- Простая визуализация прогресса (3-5 шагов)

**Best Practices:**
- Использовать для 3-7 шагов максимум
- Четко обозначать текущий шаг
- Показывать завершенные шаги отдельным цветом/стилем
- Добавлять метки под каждой точкой
- Использовать красный цвет для шагов с ошибками

#### Circular Progress

**Когда использовать:**
- Загрузка файлов
- Таймеры и обратный отсчет
- Процент выполнения задачи
- Компактная визуализация прогресса

**Best Practices:**
- Показывать текст внутри (проценты или время)
- Использовать анимацию при изменении прогресса
- Выбирать размер в зависимости от контекста:
  - 64px - для крупных акцентов
  - 48px - для карточек
  - 36px - для списков
  - 24px - для компактных UI
- Контрастный цвет для текста (черный на светлом фоне)

#### Linear Progress

**Когда использовать:**
- Загрузка контента
- Заполнение форм
- Прогресс установки/обновления
- Последовательные действия

**Best Practices:**
- Вертикальные - для вертикальных списков или боковых панелей
- Горизонтальные - для полноэкранного прогресса или верхней панели
- Использовать скругленные концы
- Анимировать переходы между состояниями
- Показывать несколько уровней активности (active, partial, inactive)

#### Stepper Progress

**Когда использовать:**
- Регистрация/онбординг
- Оформление заказа
- Многошаговые формы
- Прогресс настройки

**Best Practices:**
- Показывать все шаги сразу (макс 7-8)
- Соединять шаги линиями
- Четко выделять текущий шаг (белая обводка)
- Использовать разные цвета для completed/active/inactive
- Добавлять названия шагов при наличии места

#### Accessibility

**Для всех индикаторов:**
- **ARIA Labels**: `aria-label="Progress: 48%"`, `aria-label="Step 3 of 7"`
- **Role**: `role="progressbar"` для progress indicators
- **aria-valuenow**: Текущее значение (например, 48)
- **aria-valuemin**: Минимальное значение (обычно 0)
- **aria-valuemax**: Максимальное значение (обычно 100)
- **aria-current**: `aria-current="step"` для текущего шага
- **Live Region**: `aria-live="polite"` для объявления изменений прогресса
- **Color Contrast**: Достаточный контраст между прогрессом и фоном
- **Text Alternative**: Текстовое описание для screen readers

#### Примеры кода

**Step Indicator (Active):**
```css
.step-indicator {
  width: var(--step-indicator-size);
  height: var(--step-indicator-size);
  border-radius: var(--step-indicator-radius);
  position: relative;
}

.step-indicator__dot {
  width: var(--step-indicator-dot-size);
  height: var(--step-indicator-dot-size);
  border-radius: 50%;
  background: var(--step-indicator-inactive);
  margin-top: var(--step-indicator-padding);
}

.step-indicator__dot--active {
  background: var(--step-indicator-active);
}

.step-indicator__dot--completed {
  background: var(--step-indicator-completed);
  border: 1px solid var(--step-indicator-completed-border);
  box-shadow: 0 0 0 4px var(--step-indicator-completed);
}

.step-indicator__label {
  font: 600 10px/1.4 'Archivo', sans-serif;
  color: var(--step-indicator-label-color);
  text-align: center;
  margin-top: var(--step-indicator-spacing);
}
```

**Circular Progress:**
```css
.circular-progress {
  position: relative;
  width: var(--circular-progress-lg-size);
  height: var(--circular-progress-lg-size);
}

.circular-progress__bg {
  width: 100%;
  height: 100%;
  border-radius: 50%;
  border: var(--circular-progress-lg-border) solid var(--circular-progress-bg);
}

.circular-progress__fill {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border-radius: 50%;
  border: var(--circular-progress-lg-border) solid var(--circular-progress-fill);
  clip-path: polygon(50% 50%, 50% 0%, 100% 0%, 100% 100%, 0% 100%, 0% 0%, 50% 0%);
  transform: rotate(calc(3.6deg * var(--progress-value)));
}

.circular-progress__text {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font: 600 var(--circular-progress-text-lg)/1.4 'Archivo', sans-serif;
  color: var(--circular-progress-text-color);
}
```

**Stepper Progress:**
```css
.stepper {
  width: var(--stepper-container-width);
  padding: var(--stepper-padding-vertical) var(--stepper-padding-horizontal);
  display: flex;
  align-items: center;
  gap: var(--stepper-element-spacing);
}

.stepper__dot {
  width: var(--stepper-dot-size);
  height: var(--stepper-dot-size);
  border-radius: 50%;
  background: var(--stepper-inactive-dot);
  flex-shrink: 0;
}

.stepper__dot--completed {
  background: var(--stepper-completed-dot);
}

.stepper__dot--active {
  background: var(--stepper-active-inner);
  border: 1px solid var(--stepper-active-border);
  box-shadow: 0 0 0 2px var(--stepper-active-outer);
}

.stepper__line {
  height: var(--stepper-line-height);
  flex: 1;
  border-radius: var(--stepper-line-radius);
  background: var(--stepper-inactive-line);
}

.stepper__line--completed {
  background: var(--stepper-completed-line);
}
```

---

## Input Fields

Система полей ввода для мобильного приложения с поддержкой различных конфигураций, иконок и вспомогательных элементов.

### Container Specifications

```css
--input-container-width: 375px;
--input-container-padding-h: 16px;
--input-container-padding-v: 5px;
--input-element-spacing: 8px;
```

**Структура**:
- **Container**: 375px width, padding 16px horizontal / 5px vertical
- **Spacing**: 8px между элементами (title, field, helper message)
- **Layout**: Vertical Column с consistent gap

### Input Field Components

#### 1. Input Title (Заголовок поля)

Текстовый label над полем ввода.

```css
/* Typography */
--input-title-font-size: 14px;
--input-title-font-weight: 600;
--input-title-font-family: 'Archivo';
--input-title-line-height: 1.40;
--input-title-color: #09101D;
```

**Характеристики**:
- **Font**: 14px / 600 Archivo
- **Color**: #09101D (Primary Text)
- **Line Height**: 1.40 (19.6px)
- **Spacing**: 8px margin-bottom

#### 2. Input Field (Поле ввода)

Основное поле для ввода текста с опциональными иконками.

```css
/* Field Container */
--input-field-height: 36px;
--input-field-border-radius: 15px;
--input-field-bg: #F4F6F9;

/* Padding Variations */
--input-field-padding-left: 16px;
--input-field-padding-right-default: 20px;
--input-field-padding-right-with-icon: 10px;

/* Typography */
--input-text-font-size: 14px;
--input-text-font-family: 'Archivo';
--input-text-line-height: 1.40;

/* Text Colors */
--input-placeholder-color: #747B84;     /* Placeholder state */
--input-placeholder-weight: 400;
--input-text-color: #09101D;            /* Filled state */
--input-text-weight: 600;               /* Filled text is bold */
```

**Характеристики**:
- **Container**: 36px height, borderRadius 15px
- **Background**: #F4F6F9 (Secondary Background)
- **Padding**:
  - Base: 16px left, 20px right
  - With right icon: 16px left, 10px right
- **Placeholder Text**: 14px / 400 Archivo, color #747B84
- **Entered Text**: 14px / 600 Archivo, color #09101D (bold when filled!)

#### 3. Icons in Input Fields

##### Left Icon (Префиксная иконка)

Иконка слева внутри поля ввода.

```css
--input-icon-size: 20px;
--input-icon-padding: 2px;
--input-icon-border-radius: 100px;
--input-icon-spacing: 10px;  /* Space between icon and text */
```

**Характеристики**:
- **Size**: 20px × 20px
- **Padding**: 2px (internal)
- **Border Radius**: 100px (круглая)
- **Position**: Left side, 16px from container edge
- **Spacing**: 10px gap to text

##### Right Trailing Icon(s) (Суффиксная иконка)

Одна или несколько иконок справа от текста.

```css
--input-trailing-icon-size: 20px;
--input-trailing-icon-border-radius: 100px;
--input-trailing-icon-spacing: 10px;  /* Between multiple icons */
```

**Характеристики**:
- **Size**: 20px × 20px
- **Border Radius**: 100px (круглая)
- **Position**: Right side, 10px from container edge
- **Multiple Icons**: 10px spacing between them
- **Use Cases**: Clear button, visibility toggle, search icon

##### Flag Icon (Иконка флага страны)

Специальная иконка для выбора страны (обычно для телефонных номеров).

```css
--input-flag-width: 22px;
--input-flag-height: 16px;
--input-flag-border-radius: 2px;
```

**Характеристики**:
- **Size**: 22px × 16px (прямоугольная)
- **Border Radius**: 2px (скругленные углы)
- **Content**: Country flag image
- **Usage**: Country/phone number selector

#### 4. Helper Message (Вспомогательное сообщение)

Текст под полем ввода для подсказок или ошибок.

```css
--input-helper-font-size: 14px;
--input-helper-font-weight: 400;
--input-helper-font-family: 'Archivo';
--input-helper-line-height: 1.40;
--input-helper-color: #747B84;
```

**Характеристики**:
- **Font**: 14px / 400 Archivo
- **Color**: #747B84 (Tertiary Text)
- **Line Height**: 1.40 (19.6px)
- **Spacing**: 8px margin-top
- **Use Cases**: Hints, validation errors, character count

### Layout Variations

#### Single Full-Width Input

Стандартное одиночное поле ввода на всю ширину.

```css
/* Single Input Layout */
.input-wrapper {
  width: 375px;
  padding: 5px 16px;
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.input-field {
  width: 100%;
  height: 36px;
  padding: 0 20px 0 16px;
  background: #F4F6F9;
  border-radius: 15px;
  border: none;
}
```

#### Dual Input Layout (Two Side-by-Side)

Два поля рядом (например, флаг + номер телефона).

```css
/* Dual Input Layout */
.input-row {
  display: flex;
  gap: 10px;  /* Может быть 10px, 15px, или 20px */
}

/* Example: Flag + Phone Number */
.input-field--flag {
  width: auto;  /* Compact size for flag selector */
  padding: 0 10px 0 16px;
}

.input-field--phone {
  flex: 1;  /* Takes remaining space */
  padding: 0 20px 0 16px;
}
```

**Spacing Variations**:
- **Tight**: 10px gap between fields
- **Medium**: 15px gap between fields
- **Comfortable**: 20px gap between fields

### Input States

#### Empty State (Placeholder)

```css
.input-field::placeholder {
  color: var(--input-placeholder-color);
  font-weight: var(--input-placeholder-weight);
  font-size: 14px;
  line-height: 1.40;
}
```

**Визуальные характеристики**:
- Placeholder text: #747B84
- Font weight: 400
- Background: #F4F6F9

#### Filled State

```css
.input-field:not(:placeholder-shown) {
  color: var(--input-text-color);
  font-weight: var(--input-text-weight);
}
```

**Визуальные характеристики**:
- Text color: #09101D
- Font weight: 600 (bold!)
- Background: #F4F6F9

### Accessibility

```html
<!-- Input Field with Label -->
<div class="input-wrapper">
  <label for="input-id" class="input-title">
    Input title
  </label>
  <input
    id="input-id"
    type="text"
    class="input-field"
    placeholder="Text"
    aria-describedby="helper-id"
  />
  <span id="helper-id" class="input-helper">
    Helper message
  </span>
</div>
```

**ARIA Guidelines**:
- Используйте `<label>` с `for` атрибутом
- Связывайте helper text через `aria-describedby`
- Добавляйте `aria-invalid="true"` для состояния ошибки
- Используйте правильные `type` атрибуты (text, email, tel, etc.)

### Best Practices

1. **Typography Consistency**:
   - Title и Helper используют одинаковый размер (14px), но разный weight
   - Placeholder: 400 weight (light)
   - Filled text: 600 weight (semibold) — важно!

2. **Spacing**:
   - Всегда 8px между title, field, и helper
   - Consistent padding внутри полей
   - Gap между иконками: 10px

3. **Icon Usage**:
   - Левая иконка: для визуальной категоризации (search, email, etc.)
   - Правая иконка: для actions (clear, visibility, submit)
   - Flag иконка: только для country/region selection

4. **Color Semantics**:
   - #747B84 (Tertiary) — для placeholder и helper текста
   - #09101D (Primary) — для заполненного текста и labels
   - #F4F6F9 — стандартный фон поля

5. **Responsive Behavior**:
   - Container width фиксирован на 375px (iPhone)
   - Dual layouts используют flex для адаптивности
   - Icon sizes остаются фиксированными

### Example CSS Implementation

```css
/* CSS Variables */
:root {
  --input-container-width: 375px;
  --input-container-padding-h: 16px;
  --input-container-padding-v: 5px;
  --input-element-spacing: 8px;

  --input-field-height: 36px;
  --input-field-border-radius: 15px;
  --input-field-bg: #F4F6F9;

  --input-title-font-size: 14px;
  --input-title-font-weight: 600;
  --input-title-color: #09101D;

  --input-placeholder-color: #747B84;
  --input-placeholder-weight: 400;
  --input-text-color: #09101D;
  --input-text-weight: 600;

  --input-helper-color: #747B84;

  --input-icon-size: 20px;
  --input-flag-width: 22px;
  --input-flag-height: 16px;
}

/* Input Container */
.input-container {
  width: var(--input-container-width);
  padding: var(--input-container-padding-v) var(--input-container-padding-h);
  display: flex;
  flex-direction: column;
  gap: var(--input-element-spacing);
}

/* Input Title */
.input-title {
  font-family: 'Archivo', sans-serif;
  font-size: var(--input-title-font-size);
  font-weight: var(--input-title-font-weight);
  color: var(--input-title-color);
  line-height: 1.40;
}

/* Input Field */
.input-field {
  height: var(--input-field-height);
  padding: 0 20px 0 16px;
  background: var(--input-field-bg);
  border-radius: var(--input-field-border-radius);
  border: none;

  font-family: 'Archivo', sans-serif;
  font-size: 14px;
  line-height: 1.40;
  color: var(--input-text-color);
  font-weight: var(--input-text-weight);
}

.input-field::placeholder {
  color: var(--input-placeholder-color);
  font-weight: var(--input-placeholder-weight);
}

.input-field:focus {
  outline: none;
  /* Add focus style if needed */
}

/* Input with Left Icon */
.input-field--with-left-icon {
  padding-left: calc(16px + var(--input-icon-size) + 10px);
}

/* Input with Right Icon */
.input-field--with-right-icon {
  padding-right: calc(10px + var(--input-icon-size) + 10px);
}

/* Helper Message */
.input-helper {
  font-family: 'Archivo', sans-serif;
  font-size: 14px;
  font-weight: 400;
  color: var(--input-helper-color);
  line-height: 1.40;
}

/* Icon Styles */
.input-icon {
  width: var(--input-icon-size);
  height: var(--input-icon-size);
  border-radius: 100px;
  padding: 2px;
}

.input-flag {
  width: var(--input-flag-width);
  height: var(--input-flag-height);
  border-radius: 2px;
}

/* Dual Input Layout */
.input-row {
  display: flex;
  gap: 10px;
}

.input-row .input-field {
  flex: 1;
}
```

### Advanced Input Field Variants

Расширенные варианты полей ввода с borders, разными размерами, состояниями и сложными layout-ами.

#### Container Padding Variation

```css
--input-container-padding-v-alt: 10px;  /* Alternative vertical padding (10px instead of 5px) */
```

#### Field Heights

```css
--input-field-height-small: 44px;   /* Compact height */
--input-field-height-medium: 46px;  /* Standard height */
```

**Два варианта высоты**:
- **Small (44px)**: для компактных UI, минимальный padding
- **Medium (46px)**: стандартная высота, комфортный touch target

#### Visible Borders

```css
/* Border Configuration */
--input-field-border-width: 2px;
--input-field-border-color: #F4F6F9;  /* Same as background, creates subtle depth */
```

**Применение**:
- Border width: 2px
- Border color: #F4F6F9 (совпадает с фоном для subtle эффекта)
- Creates depth without visual contrast

#### Field Padding Variation

```css
/* Asymmetric Padding */
--input-field-padding-top: 4px;
--input-field-padding-left: 20px;
--input-field-padding-right: 15px;
--input-field-padding-bottom: 4px;
```

**Характеристики**:
- Asymmetric: 20px left, 15px right
- Vertical: минимальный 4px top/bottom
- Оптимизировано для text alignment

#### Typography Variations

##### Small Text (Compact Fields)

```css
--input-text-small-size: 12px;
--input-text-small-weight: 400;
--input-text-small-color: #747B84;      /* For placeholder */
--input-text-small-filled-color: #09101D; /* For filled text */
```

**Использование**: компактные поля, secondary information

##### Medium Text (Standard Fields)

```css
--input-text-medium-size: 14px;
--input-text-medium-weight: 600;
--input-text-medium-color: #09101D;
```

**Использование**: основные поля ввода

##### Special Text Color

```css
--input-text-special-color: #23262B;  /* Slightly lighter than primary black */
```

**Использование**: альтернативный цвет для filled text в специальных случаях

#### Element Spacing

```css
--input-element-spacing-tight: 5px;  /* Tight spacing between title/field/helper */
```

**Применение**: альтернатива стандартным 8px для более компактных layouts

### Field State Variations

#### Success State

Положительная валидация с визуальной обратной связью.

```css
--input-success-color: #11BB8D;
--input-success-message-size: 12px;
--input-success-message-weight: 400;
--input-success-emoji-size: 14px;
```

**Характеристики**:
- Helper message: 12px / 400 Archivo
- Color: #11BB8D (Success Green)
- Optional emoji: 14px font size
- Padding: 10px horizontal

**Example**:
```html
<div class="input-container" style="padding: 10px 16px;">
  <div class="input-field" style="height: 46px;">
    <input value="First name" />
  </div>
  <div class="input-helper-success" style="padding: 0 10px; color: #11BB8D;">
    <span>Name is correct</span>
    <span style="font-size: 14px;">👌</span>
  </div>
</div>
```

#### Error State

Негативная валидация с error message.

```css
--input-error-color: #E24949;
--input-error-message-size: 12px;
--input-error-message-weight: 400;
```

**Характеристики**:
- Helper message: 12px / 400 Archivo
- Color: #E24949 (Error Red)
- Padding: 10px left (asymmetric)

**Example**:
```html
<div class="input-container">
  <div class="input-field" style="height: 46px;">
    <input value="@johnsmith" style="font-size: 14px; font-weight: 600;" />
  </div>
  <div class="input-helper-error" style="padding-left: 10px; color: #E24949;">
    Username already taken
  </div>
</div>
```

#### Two-Line Field (Label + Value)

Поле с label над значением внутри одного input контейнера.

```css
/* Two-Line Field */
--input-two-line-label-size: 12px;
--input-two-line-label-weight: 400;
--input-two-line-label-color: #747B84;
--input-two-line-value-size: 14px;
--input-two-line-value-weight: 600;
--input-two-line-value-color: #09101D;
```

**Layout**:
- Top line (label): 12px / 400, color #747B84
- Bottom line (value): 14px / 600, color #09101D
- Vertical stack с минимальным spacing

**Use Cases**:
- Email display: "Your email" → "you@awesome.com"
- Name display: "Your name" → "John"
- Currency display: "~38058.93$" → "38069.01"

### Complex Field Types

#### Field with Top Label and Balance Info

Поле с заголовком, balance информацией и USD конвертацией.

```css
/* Top Label with Balance */
--input-label-font-size: 14px;
--input-label-font-weight: 600;
--input-label-color: #09101D;
--input-balance-font-size: 10px;
--input-balance-font-weight: 600;
--input-balance-color: #09101D;
--input-usd-font-size: 10px;
--input-usd-font-weight: 600;
--input-usd-color-blue: #0B24FB;
--input-usd-color-purple: #4141E6;
```

**Structure**:
```html
<div style="padding: 0 10px; display: flex; justify-content: space-between; align-items: flex-end;">
  <span style="font: 600 14px/1.4 Archivo; color: #09101D;">From</span>
  <div style="display: flex; gap: 10px;">
    <span style="font: 600 10px/1.4 Archivo; color: #09101D;">Balance: 1.01 ETH</span>
    <span style="font: 600 10px/1.4 Archivo; color: #0B24FB;">~4.043$</span>
  </div>
</div>
<div class="input-field" style="height: 46px;">
  <input placeholder="Enter amount" />
</div>
```

**Характеристики**:
- Label: 14px/600 на baseline alignment с balance info
- Balance: 10px/600, черный текст
- USD price: 10px/600, синий (#0B24FB) или фиолетовый (#4141E6)
- Spacing: 10px gap между balance элементами

#### Field with Avatar

Поле с аватаром слева от текста.

```css
/* Avatar Specifications */
--input-avatar-size: 30px;
--input-avatar-border-radius-circle: 50px;  /* Circular avatar */
--input-avatar-border-radius-rounded: 10px; /* Rounded square avatar */
--input-avatar-spacing: 10px;               /* Space to text */
```

**Avatar Variants**:
1. **Circular (OvalBorder)**: borderRadius 50px
2. **Rounded Square**: borderRadius 10px

**Layout**:
```html
<div class="input-field" style="height: 46px; display: flex; gap: 10px; align-items: center;">
  <img src="avatar.jpg" style="width: 30px; height: 30px; border-radius: 50px;" />
  <span style="font: 400 12px/1.4 Archivo; color: #747B84;">Helen Smith</span>
  <img src="icon.svg" style="width: 24px; height: 24px; margin-left: auto;" />
</div>
```

**Use Cases**:
- User selection fields
- Contact picker
- Account switcher
- Service/app selection (e.g., "Netflix", "Dropbox")

#### Field with Multiple Icons

Поле с несколькими иконками справа.

```css
/* Icon Sizes */
--input-icon-24: 24px;
--input-icon-padding-2: 2px;
--input-icon-padding-4: 4px;
--input-icon-padding-6: 6px;
--input-icon-inner-14: 14.40px;  /* 24px container with 6px padding */
--input-icon-inner-19: 19.20px;  /* 24px container with 4px padding */
```

**Icon Spacing**: 5px gap между иконками справа

**Example Layout**:
```html
<!-- Currency Field with Avatar, Label and Dropdown -->
<div class="input-field" style="height: 46px; display: flex; align-items: center; gap: 5px;">
  <span style="flex: 1; font: 600 14px/1.4 Archivo;">0.109367206519394123</span>
  <img src="btc-avatar.png" style="width: 30px; height: 30px; border-radius: 50px;" />
  <span style="font: 600 13px/1.4 Archivo; color: #09101D;">BTC</span>
  <div style="width: 24px; height: 24px; padding: 4px;">
    <img src="dropdown-icon.svg" style="width: 19.2px; height: 19.2px;" />
  </div>
</div>
```

#### Field with Left and Right Content

Сложное поле с контентом с обеих сторон.

```css
/* Typography for Currency/Balance Display */
--input-currency-label-size: 13px;
--input-currency-label-weight: 600;
--input-currency-label-color: #09101D;
```

**Example: Search Icon Left + Clear Icon Right**:
- Left icon: 24px × 24px, 10px gap to text
- Placeholder: 12px/400
- Right icon: 24px × 24px

**Example: Avatar Left + Value Right**:
- Left: 30px avatar + two-line text
- Right: numeric value + subtitle
- Gap: 10px between sections

#### Field with Right-Aligned Text Column

```html
<div class="input-field" style="height: 46px; display: flex; justify-content: space-between;">
  <div style="display: flex; gap: 10px; align-items: center;">
    <img src="avatar.png" style="width: 30px; height: 30px; border-radius: 50px;" />
    <img src="icon.svg" style="width: 24px; height: 24px;" />
  </div>
  <div style="text-align: right;">
    <div style="font: 600 14px/1.4 Archivo; color: #09101D;">63498.45</div>
    <div style="font: 400 12px/1.4 Archivo; color: #747B84;">United States Dollar</div>
  </div>
</div>
```

### Advanced CSS Implementation

```css
/* Extended Variables */
:root {
  /* Alternative Heights */
  --input-field-height-small: 44px;
  --input-field-height-medium: 46px;

  /* Visible Border */
  --input-field-border-width: 2px;
  --input-field-border-color: #F4F6F9;

  /* Asymmetric Padding */
  --input-field-padding: 4px 15px 4px 20px;

  /* Small Text Variant */
  --input-text-small: 400 12px/1.4 'Archivo';
  --input-text-small-color: #747B84;
  --input-text-small-filled: #09101D;

  /* Special Color */
  --input-text-special: #23262B;

  /* Tight Spacing */
  --input-spacing-tight: 5px;

  /* State Colors */
  --input-success: #11BB8D;
  --input-error: #E24949;

  /* Label with Balance */
  --input-label-text: 600 14px/1.4 'Archivo';
  --input-balance-text: 600 10px/1.4 'Archivo';
  --input-usd-blue: #0B24FB;
  --input-usd-purple: #4141E6;

  /* Avatar */
  --input-avatar-size: 30px;
  --input-avatar-radius-circle: 50px;
  --input-avatar-radius-rounded: 10px;

  /* Currency Label */
  --input-currency-label: 600 13px/1.4 'Archivo';

  /* Icon Sizes */
  --input-icon-24: 24px;
  --input-icon-14: 14.40px;
  --input-icon-19: 19.20px;
}

/* Field with Visible Border */
.input-field--bordered {
  height: var(--input-field-height-medium);
  padding: var(--input-field-padding);
  background: var(--input-field-bg);
  border: var(--input-field-border-width) solid var(--input-field-border-color);
  border-radius: var(--input-field-border-radius);
}

/* Small Text Variant */
.input-field--small-text {
  font: var(--input-text-small);
  color: var(--input-text-small-color);
}

.input-field--small-text:not(:placeholder-shown) {
  color: var(--input-text-small-filled);
}

/* Two-Line Field */
.input-field--two-line {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.input-field__label {
  font: 400 12px/1.4 'Archivo';
  color: var(--input-text-tertiary);
}

.input-field__value {
  font: 600 14px/1.4 'Archivo';
  color: var(--input-text-primary);
}

/* Success State */
.input-helper--success {
  font: 400 12px/1.4 'Archivo';
  color: var(--input-success);
  padding: 0 10px;
  display: flex;
  align-items: center;
  gap: 13px;
}

.input-helper--success .emoji {
  font-size: 14px;
}

/* Error State */
.input-helper--error {
  font: 400 12px/1.4 'Archivo';
  color: var(--input-error);
  padding-left: 10px;
}

/* Field with Avatar */
.input-field--with-avatar {
  display: flex;
  align-items: center;
  gap: 10px;
}

.input-field__avatar {
  width: var(--input-avatar-size);
  height: var(--input-avatar-size);
  flex-shrink: 0;
}

.input-field__avatar--circle {
  border-radius: var(--input-avatar-radius-circle);
}

.input-field__avatar--rounded {
  border-radius: var(--input-avatar-radius-rounded);
}

/* Label with Balance */
.input-label-row {
  padding: 0 10px;
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  margin-bottom: 5px;
}

.input-label-row__title {
  font: var(--input-label-text);
  color: var(--input-label-color);
}

.input-label-row__balance {
  display: flex;
  gap: 10px;
  align-items: flex-end;
}

.input-label-row__balance-amount {
  font: var(--input-balance-text);
  color: var(--input-balance-color);
}

.input-label-row__usd {
  font: var(--input-balance-text);
}

.input-label-row__usd--blue {
  color: var(--input-usd-blue);
}

.input-label-row__usd--purple {
  color: var(--input-usd-purple);
}

/* Currency Field */
.input-field--currency {
  display: flex;
  align-items: center;
  gap: 5px;
}

.input-field__currency-label {
  font: var(--input-currency-label);
  color: var(--input-currency-label-color);
}
```

### Usage Examples

```html
<!-- Basic Single Input -->
<div class="input-container">
  <label class="input-title">Email Address</label>
  <input type="email" class="input-field" placeholder="Enter your email" />
  <span class="input-helper">We'll never share your email</span>
</div>

<!-- Input with Flag and Phone Number -->
<div class="input-container">
  <label class="input-title">Phone Number</label>
  <div class="input-row">
    <div class="input-field" style="width: auto; padding: 0 10px 0 16px;">
      <img src="flag-ru.png" class="input-flag" alt="Russia" />
    </div>
    <input type="tel" class="input-field" placeholder="+7 (900) 123-45-67" />
  </div>
  <span class="input-helper">For verification purposes</span>
</div>

<!-- Input with Icons -->
<div class="input-container">
  <label class="input-title">Search</label>
  <div style="position: relative;">
    <img src="search-icon.svg" class="input-icon"
         style="position: absolute; left: 16px; top: 8px;" />
    <input type="text" class="input-field input-field--with-left-icon"
           placeholder="Search..." />
    <img src="clear-icon.svg" class="input-icon"
         style="position: absolute; right: 10px; top: 8px; cursor: pointer;" />
  </div>
  <span class="input-helper">Type to search</span>
</div>
```

---

## Snackbars & Toasts

Система уведомлений snackbar/toast для мобильного приложения с поддержкой различных layouts, иконок, аватаров и action buttons.

### Container Specifications

```css
/* Snackbar Container */
--snackbar-container-width: 375px;
--snackbar-container-padding: 16px;
--snackbar-border-radius: 15px;

/* Success/Positive Snackbar */
--snackbar-success-bg: rgba(5, 148, 79, 0.90);  /* #05944F с 90% opacity */
--snackbar-text-color: #FFFFFF;
```

**Структура**:
- **Container**: 375px width, padding 16px
- **Border Radius**: 15px для всех элементов
- **Background**: rgba(5, 148, 79, 0.90) для positive/success snackbar
- **Text Color**: White (#FFFFFF)

### Typography

```css
/* Snackbar Message Text */
--snackbar-message-font-size: 14px;
--snackbar-message-font-weight: 600;
--snackbar-message-font-family: 'Archivo';
--snackbar-message-line-height: 1.40;
--snackbar-message-color: #FFFFFF;

/* Action Button Text */
--snackbar-action-font-size: 13px;
--snackbar-action-font-weight: 600;
--snackbar-action-font-family: 'Archivo';
--snackbar-action-line-height: 1.40;
--snackbar-action-color: #FFFFFF;
```

**Характеристики**:
- **Message Text**: 14px / 600 Archivo, white color
- **Action Button Text**: 13px / 600 Archivo, white color
- **Line Height**: 1.40 для всех текстов

### Snackbar Elements

#### 1. Icon Element

Иконка слева от сообщения.

```css
--snackbar-icon-size: 24px;
--snackbar-icon-padding: 16px;
```

**Характеристики**:
- **Size**: 24px × 24px
- **Padding**: 16px вокруг иконки
- **Position**: Left side of message
- **Use Case**: Status icons (success, error, info, warning)

#### 2. Avatar Element

Аватар пользователя слева от сообщения.

```css
/* Avatar Specifications */
--snackbar-avatar-container: 56px;
--snackbar-avatar-image: 48px;
--snackbar-avatar-offset: 4px;
--snackbar-avatar-border-radius: 40px;
--snackbar-avatar-bg: #FFFFFF;
--snackbar-avatar-padding: 16px;
```

**Структура**:
- **Container**: 56px × 56px
- **Image**: 48px × 48px
- **Offset**: 4px от краев контейнера (создает white border эффект)
- **Border Radius**: 40px (highly rounded)
- **Background**: White (#FFFFFF) под изображением
- **Padding**: 16px вокруг avatar container

**Visual Effect**:
- 48px image positioned at 4px offset creates visible white background
- Appears as 48px image with 4px white border

#### 3. Close Icon

Иконка закрытия справа.

```css
/* Close Icon */
--snackbar-close-icon-size: 20px;
--snackbar-close-height-small: 36px;
--snackbar-close-height-large: 44px;
--snackbar-close-padding-h: 16px;
--snackbar-close-padding-v: 10px;
```

**Характеристики**:
- **Icon Size**: 20px × 20px
- **Container Height**: 36px или 44px
- **Padding**: 16px horizontal, 10px vertical
- **Border Radius**: 15px
- **Position**: Right side, vertically centered

#### 4. Action Button

Кнопка действия справа от сообщения.

```css
/* Action Button */
--snackbar-action-height-small: 36px;
--snackbar-action-height-large: 44px;
--snackbar-action-padding-h: 16px;
--snackbar-action-padding-v: 10px;
--snackbar-action-border-radius: 15px;
--snackbar-action-text-color: #FFFFFF;
```

**Характеристики**:
- **Height**: 36px (compact) или 44px (comfortable)
- **Padding**: 16px horizontal, 10px vertical
- **Border Radius**: 15px
- **Text**: "Action", 13px / 600, white
- **Background**: Transparent (inherit from snackbar)
- **Hover/Press**: Add visual feedback

### Snackbar Layout Variants

#### Variant 1: Simple Message

Простое текстовое сообщение без дополнительных элементов.

```css
/* Simple Layout */
.snackbar--simple {
  padding: 16px;
}

.snackbar__message--simple {
  width: 311px;  /* Max width for simple message */
}
```

**Structure**:
```html
<div class="snackbar snackbar--simple" style="width: 375px; padding: 16px; background: rgba(5, 148, 79, 0.90); border-radius: 15px;">
  <span style="font: 600 14px/1.4 Archivo; color: white;">Message that takes 2 lines to explain and goes on</span>
</div>
```

#### Variant 2: Icon + Message

Иконка слева + текстовое сообщение.

```css
.snackbar--with-icon {
  display: flex;
  align-items: center;
}

.snackbar__icon-wrapper {
  padding: 16px;
}

.snackbar__message--with-icon {
  padding: 16px 16px 16px 0;
  width: 271px;
}
```

**Structure**:
- Icon container: padding 16px all sides
- Message: padding 16px top/right/bottom
- Message width: 271px

#### Variant 3: Icon + Message + Close

Иконка слева + сообщение + close icon справа.

```css
.snackbar--with-icon-close {
  display: flex;
  align-items: center;
}

.snackbar__message--with-close {
  flex: 1;
  padding: 16px 0;
  width: 235px;
}

.snackbar__close {
  height: 44px;
  padding: 10px 16px;
}
```

**Structure**:
- Icon: padding 16px
- Message: vertical padding 16px, width 235px
- Close: height 44px, padding 10px/16px

#### Variant 4: Avatar + Message

Avatar слева + текстовое сообщение.

```css
.snackbar--with-avatar {
  display: flex;
  align-items: center;
}

.snackbar__avatar-wrapper {
  padding: 16px;
}

.snackbar__message--with-avatar {
  padding: 16px 16px 16px 0;
  width: 239px;
}
```

**Structure**:
- Avatar container: padding 16px
- Message: padding 16px top/right/bottom
- Message width: 239px

#### Variant 5: Avatar + Message + Close

Avatar + сообщение + close icon справа.

```css
.snackbar--with-avatar-close {
  display: flex;
  align-items: center;
}

.snackbar__message--avatar-close {
  flex: 1;
  padding: 16px 0;
  width: 203px;
}
```

**Structure**:
- Avatar: padding 16px
- Message: vertical padding 16px, width 203px
- Close: height 44px, padding 10px/16px

#### Variant 6: Message + Action

Сообщение + action button справа.

```css
.snackbar--with-action {
  display: flex;
  align-items: center;
  padding-right: 16px;
}

.snackbar__message--with-action {
  flex: 1;
  padding: 16px;
  width: 267px;
}

.snackbar__action {
  height: 36px;
  padding: 10px 16px;
  border-radius: 15px;
}
```

**Structure**:
- Container: padding-right 16px
- Message: padding 16px, width 267px (or less)
- Action: height 36px, padding 10px/16px

#### Variant 7: Icon + Message + Action

Иконка + сообщение + action button.

```css
.snackbar--icon-action {
  display: flex;
  align-items: center;
  padding-right: 16px;
}

.snackbar__message--icon-action {
  flex: 1;
  padding: 16px 8px 16px 0;
  width: 223px;
}
```

**Structure**:
- Icon: padding 16px
- Message: padding 16px/8px/16px/0, width 223px
- Action: height 36px

#### Variant 8: Avatar + Message + Action

Avatar + сообщение + action button.

```css
.snackbar--avatar-action {
  display: flex;
  align-items: center;
  padding-right: 16px;
}

.snackbar__message--avatar-action-2line {
  flex: 1;
  padding: 16px 0;
  width: 159px;  /* For 3-line message */
}

.snackbar__message--avatar-action {
  width: 191px;  /* For 2-line message */
}
```

**Structure**:
- Avatar: padding 16px
- Message: variable width based on lines (159px for 3-line, 191px for 2-line)
- Action: height 36px

### Accessibility

```html
<!-- Success Snackbar with ARIA -->
<div class="snackbar"
     role="status"
     aria-live="polite"
     aria-atomic="true">
  <img src="success-icon.svg" alt="" aria-hidden="true" />
  <span class="snackbar__message">Operation completed successfully</span>
  <button class="snackbar__close" aria-label="Close notification">
    <img src="close-icon.svg" alt="" />
  </button>
</div>

<!-- Snackbar with Action -->
<div class="snackbar"
     role="alert"
     aria-live="assertive"
     aria-atomic="true">
  <span class="snackbar__message">Changes saved</span>
  <button class="snackbar__action" onclick="undoChanges()">
    Undo
  </button>
</div>
```

**ARIA Guidelines**:
- Use `role="status"` для информационных уведомлений
- Use `role="alert"` для важных уведомлений с действиями
- `aria-live="polite"` для обычных уведомлений
- `aria-live="assertive"` для срочных уведомлений
- `aria-atomic="true"` для чтения всего сообщения целиком
- `aria-label` для close кнопки
- Icons должны иметь `aria-hidden="true"`

### Best Practices

1. **Duration & Timing**:
   - Информационные snackbars: 3-4 seconds auto-dismiss
   - Snackbars с action: 7-10 seconds или manual dismiss
   - Error messages: manual dismiss only

2. **Positioning**:
   - Bottom center для мобильных приложений (стандарт)
   - Top center для desktop web
   - Avoid blocking important content

3. **Content**:
   - Краткие сообщения: 1-3 строки максимум
   - Clear, actionable language
   - Avoid technical jargon

4. **Visual Hierarchy**:
   - Avatar используйте для user-specific notifications
   - Icon используйте для status/category indicators
   - Action button только для reversible actions или важных переходов

5. **Color Coding** (будущие варианты):
   - Success: rgba(5, 148, 79, 0.90) - зеленый
   - Error: rgba(226, 73, 73, 0.90) - красный (#E24949)
   - Warning: желтый/оранжевый
   - Info: синий (#4141E6)

### CSS Implementation

```css
/* CSS Variables */
:root {
  /* Container */
  --snackbar-width: 375px;
  --snackbar-padding: 16px;
  --snackbar-border-radius: 15px;

  /* Colors */
  --snackbar-success-bg: rgba(5, 148, 79, 0.90);
  --snackbar-text-white: #FFFFFF;

  /* Typography */
  --snackbar-message-text: 600 14px/1.4 'Archivo';
  --snackbar-action-text: 600 13px/1.4 'Archivo';

  /* Elements */
  --snackbar-icon-size: 24px;
  --snackbar-avatar-container: 56px;
  --snackbar-avatar-image: 48px;
  --snackbar-avatar-offset: 4px;
  --snackbar-avatar-radius: 40px;
  --snackbar-close-icon: 20px;
  --snackbar-action-height-sm: 36px;
  --snackbar-action-height-lg: 44px;
}

/* Base Snackbar */
.snackbar {
  width: var(--snackbar-width);
  padding: var(--snackbar-padding);
  background: var(--snackbar-success-bg);
  border-radius: var(--snackbar-border-radius);
  display: flex;
  align-items: center;
}

/* Message */
.snackbar__message {
  font: var(--snackbar-message-text);
  color: var(--snackbar-text-white);
}

/* Icon */
.snackbar__icon {
  width: var(--snackbar-icon-size);
  height: var(--snackbar-icon-size);
  padding: var(--snackbar-padding);
  flex-shrink: 0;
}

/* Avatar */
.snackbar__avatar-wrapper {
  width: var(--snackbar-avatar-container);
  height: var(--snackbar-avatar-container);
  padding: var(--snackbar-padding);
  flex-shrink: 0;
  position: relative;
}

.snackbar__avatar-bg {
  position: absolute;
  left: var(--snackbar-avatar-offset);
  top: var(--snackbar-avatar-offset);
  width: var(--snackbar-avatar-image);
  height: var(--snackbar-avatar-image);
  background: var(--snackbar-text-white);
  border-radius: var(--snackbar-avatar-radius);
}

.snackbar__avatar-image {
  position: absolute;
  left: var(--snackbar-avatar-offset);
  top: var(--snackbar-avatar-offset);
  width: var(--snackbar-avatar-image);
  height: var(--snackbar-avatar-image);
  border-radius: var(--snackbar-avatar-radius);
  object-fit: cover;
}

/* Close Button */
.snackbar__close {
  height: var(--snackbar-action-height-lg);
  padding: 10px 16px;
  border-radius: var(--snackbar-border-radius);
  background: transparent;
  border: none;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
}

.snackbar__close-icon {
  width: var(--snackbar-close-icon);
  height: var(--snackbar-close-icon);
}

/* Action Button */
.snackbar__action {
  height: var(--snackbar-action-height-sm);
  padding: 10px 16px;
  border-radius: var(--snackbar-border-radius);
  background: transparent;
  border: none;
  cursor: pointer;
  font: var(--snackbar-action-text);
  color: var(--snackbar-text-white);
  white-space: nowrap;
}

.snackbar__action:hover {
  background: rgba(255, 255, 255, 0.1);
}

.snackbar__action:active {
  background: rgba(255, 255, 255, 0.2);
}

/* Layout Variants */
.snackbar--simple {
  padding: var(--snackbar-padding);
}

.snackbar--with-icon .snackbar__message,
.snackbar--with-avatar .snackbar__message {
  padding: 16px 16px 16px 0;
  flex: 1;
}

.snackbar--with-close .snackbar__message,
.snackbar--with-action .snackbar__message {
  flex: 1;
  padding: 16px 0;
}

.snackbar--with-action {
  padding-right: 16px;
}
```

### Usage Examples

```html
<!-- Simple Success Message -->
<div class="snackbar snackbar--simple">
  <span class="snackbar__message">Message that takes 2 lines to explain and goes on</span>
</div>

<!-- With Icon -->
<div class="snackbar snackbar--with-icon">
  <div class="snackbar__icon">
    <img src="success-icon.svg" alt="" />
  </div>
  <span class="snackbar__message">Message that takes 2 lines to explain and goes on</span>
</div>

<!-- With Avatar and Close -->
<div class="snackbar snackbar--with-avatar snackbar--with-close">
  <div class="snackbar__avatar-wrapper">
    <div class="snackbar__avatar-bg"></div>
    <img class="snackbar__avatar-image" src="avatar.jpg" alt="User avatar" />
  </div>
  <span class="snackbar__message">Message that takes 2 lines to explain and goes on</span>
  <button class="snackbar__close" aria-label="Close">
    <img class="snackbar__close-icon" src="close-icon.svg" alt="" />
  </button>
</div>

<!-- With Action Button -->
<div class="snackbar snackbar--with-action">
  <span class="snackbar__message">Message that takes 2 lines to explain and goes on</span>
  <button class="snackbar__action">Action</button>
</div>

<!-- Icon + Message + Action -->
<div class="snackbar snackbar--with-icon snackbar--with-action">
  <div class="snackbar__icon">
    <img src="info-icon.svg" alt="" />
  </div>
  <span class="snackbar__message">Changes saved successfully</span>
  <button class="snackbar__action">View</button>
</div>
```

---

## Mobile Screens & Layouts

Готовые макеты экранов для мобильного приложения с модульными компонентами, которые можно гибко комбинировать и расширять.

> **Принцип модульности**: Каждый экран состоит из переиспользуемых блоков. Вы можете добавлять, удалять или дублировать блоки в зависимости от требований backend или бизнес-логики.

### Screen Container Specifications

```css
/* Mobile Screen Container */
--screen-width: 375px;
--screen-border-radius: 30px;         /* Large radius for whole screen */
--screen-bg-white: #FFFFFF;
--screen-bg-light: #FAFAFB;           /* Light gray background */
```

**Характеристики**:
- **Width**: 375px (iPhone standard)
- **Border Radius**: 30px (большое скругление для всего экрана)
- **Backgrounds**: White (#FFFFFF) или Light Gray (#FAFAFB)
- **Heights**: Variable (368px, 363px, 286px и т.д.)

### Screen Typography

#### Large Titles (Welcome Screens)

```css
/* Large Screen Titles */
--screen-title-large-size: 32px;
--screen-title-large-weight: 700;
--screen-title-large-line-height: 1.40;
--screen-title-large-color: #09101D;
--screen-title-large-spacing: 10px;   /* Space to subtitle */

/* Medium Screen Titles */
--screen-title-medium-size: 24px;
--screen-title-medium-weight: 700;
--screen-title-medium-line-height: 1.40;
```

**Использование**:
- **32px/700**: Главные welcome/onboarding заголовки
- **24px/700**: Вторичные заголовки на onboarding screens

#### Subtitles with Letter Spacing

```css
/* Screen Subtitles */
--screen-subtitle-size: 16px;
--screen-subtitle-weight: 400;
--screen-subtitle-line-height: 1.40;
--screen-subtitle-letter-spacing: 1px;    /* Important! */
--screen-subtitle-color: #09101D;
--screen-subtitle-color-dimmed: rgba(9, 16, 29, 0.40);  /* 40% opacity */
```

**Характеристики**:
- Font: 16px / 400 Archivo
- Letter spacing: 1px (для читаемости)
- Colors: обычный #09101D или dimmed с opacity 0.40

#### Colored Accent Text

Выделение ключевых слов цветом внутри заголовков и подзаголовков.

```css
--screen-accent-color: #4141E6;       /* Primary purple for accents */
```

**Использование**:
- Выделение ключевых слов в заголовках
- Выделение brand terms в описаниях
- Создание visual hierarchy

**Example**:
```html
<h1 style="font: 700 32px/1.4 Archivo; text-align: center;">
  One app for<br/>
  <span style="color: #4141E6;">any currencies</span>
</h1>
```

### Screen Elements

#### 1. Home Indicator (iPhone-style)

Индикатор нижней части экрана (как на iPhone).

```css
/* Home Indicator */
--home-indicator-width: 134px;
--home-indicator-height: 5px;
--home-indicator-border-radius: 100px;
--home-indicator-color: #09101D;
--home-indicator-margin-top: 21px;
```

**Характеристики**:
- **Size**: 134px × 5px
- **Border Radius**: 100px (pill shape)
- **Color**: #09101D (black)
- **Position**: Bottom center, 21px от верхнего края контейнера
- **Container Height**: 34px total

**CSS**:
```css
.home-indicator {
  width: var(--home-indicator-width);
  height: var(--home-indicator-height);
  background: var(--home-indicator-color);
  border-radius: var(--home-indicator-border-radius);
  margin: 21px auto 0;
}
```

#### 2. Progress Bar (Multi-segment)

Прогресс-бар из нескольких сегментов для onboarding/stepper screens.

```css
/* Progress Bar */
--progress-bar-height: 3px;
--progress-bar-segment-spacing: 10px;
--progress-bar-active-color: #4141E6;
--progress-bar-inactive-color: rgba(11, 36, 251, 0.20);
--progress-bar-border-radius: 10px;
```

**Структура**:
- **Container**: padding 16px horizontal, 10px vertical
- **Height**: 3px
- **Segments**: 5 сегментов (или любое количество)
- **Spacing**: 10px между сегментами
- **Colors**:
  - Active: #4141E6 (primary purple)
  - Inactive: rgba(11, 36, 251, 0.20) - 20% opacity
- **Border Radius**:
  - First segment: topLeft/bottomLeft 10px
  - Last segment: topRight/bottomRight 10px
  - Middle segments: no radius

**Модульность**: Количество сегментов можно менять (3, 4, 5, 6 и т.д.)

**CSS**:
```css
.progress-bar {
  display: flex;
  gap: var(--progress-bar-segment-spacing);
  height: var(--progress-bar-height);
  padding: 10px 16px;
}

.progress-bar__segment {
  flex: 1;
  height: 100%;
  background: var(--progress-bar-inactive-color);
}

.progress-bar__segment--active {
  background: var(--progress-bar-active-color);
}

.progress-bar__segment:first-child {
  border-radius: var(--progress-bar-border-radius) 0 0 var(--progress-bar-border-radius);
}

.progress-bar__segment:last-child {
  border-radius: 0 var(--progress-bar-border-radius) var(--progress-bar-border-radius) 0;
}
```

#### 3. Back Button

Кнопка назад для navigation.

```css
/* Back Button */
--back-button-height: 44px;
--back-button-icon-size: 24px;
--back-button-icon-bg: rgba(9, 16, 29, 0.20);  /* 20% opacity */
--back-button-icon-padding: 6px;
--back-button-icon-radius: 100px;
--back-button-container-padding: 16px 10px;
```

**Структура**:
- **Container**: height 44px, padding 16px/10px
- **Icon Container**: 24px × 24px, borderRadius 100px
- **Icon Background**: rgba(9, 16, 29, 0.20) - 20% opacity black
- **Icon**: 14.40px × 14.40px (с padding 6px = 24px total)

**CSS**:
```css
.back-button {
  height: var(--back-button-height);
  padding: var(--back-button-container-padding);
  background: transparent;
  border: none;
}

.back-button__icon-wrapper {
  width: var(--back-button-icon-size);
  height: var(--back-button-icon-size);
  background: var(--back-button-icon-bg);
  border-radius: var(--back-button-icon-radius);
  padding: var(--back-button-icon-padding);
  display: flex;
  align-items: center;
  justify-content: center;
}

.back-button__icon {
  width: 14.40px;
  height: 14.40px;
}
```

#### 4. Button Groups

Группы кнопок (рядом или вертикально) для actions на экранах.

##### Dual Buttons (Side by Side)

Две кнопки рядом друг с другом.

```css
/* Dual Button Row */
--button-row-spacing: 10px;
--button-height-large: 52px;
--button-padding: 16px 10px;
--button-border-radius: 15px;
--button-font: 600 16px/1.4 'Archivo';
```

**Структура**:
- **Container**: padding 16px horizontal
- **Row**: две кнопки с spacing 10px
- **Button Height**: 52px
- **Button Padding**: 16px horizontal, 10px vertical
- **Border Radius**: 15px
- **Text**: 16px / 600 Archivo

**Variants**:
1. **Outline + Filled**:
   - Left: border 1px #09101D, text #09101D
   - Right: background #09101D, text white

2. **Custom Colors**:
   - Left: border 1px #4141E6, text #4141E6
   - Right: background #4141E6, text white

**Модульность**: Можно делать 1, 2 или 3 кнопки в ряд с adjustable widths

##### Stacked Buttons (Vertical)

Две или более кнопок вертикально.

```css
/* Stacked Button Column */
--button-stack-spacing: 10px;
--button-height-medium: 44px;
```

**Структура**:
- **Container**: padding 16px horizontal, 10px vertical
- **Column**: spacing 10px между кнопками
- **Button Height**: 44px (немного меньше чем dual row)
- **Full Width**: каждая кнопка на всю ширину

**Variants**:
1. **Filled + Outline**:
   - Top: background #4141E6, text white
   - Bottom: border 1px #4141E6, text #4141E6

2. **All Outlined**
3. **All Filled**

**Модульность**: Можно добавлять 3, 4, 5+ кнопок вертикально

### Screen Layouts

#### Layout 1: Welcome Screen (White Background)

Простой welcome screen с заголовком, подзаголовком и двумя кнопками.

```css
/* Welcome Screen */
--welcome-padding-v: 50px;
--welcome-padding-h: 16px;
--welcome-content-width: 343px;      /* Max width for text */
--welcome-text-spacing: 10px;
```

**Структура**:
```
┌─────────────────────────────────────┐
│                                     │ 50px padding top
│     "Welcome to Appka Studio"       │ 32px/700 title
│                                     │ 10px spacing
│   "Design made simple for your...   │ 16px/400 subtitle (dimmed)
│                                     │
│   [Sign in]    [Register]           │ Dual buttons (52px)
│                                     │
│         ────────                    │ Home indicator
└─────────────────────────────────────┘
```

**Характеристики**:
- Background: white
- Padding: 50px vertical, 16px horizontal (для текста)
- Title: 32px/700, center, color #09101D
- Subtitle: 16px/400, center, color rgba(9,16,29,0.40), letter-spacing 1
- Buttons: dual row, 52px height
  - "Sign in": outline (border #09101D)
  - "Register": filled (bg #09101D)
- Home indicator: внизу

**Модульность**:
- ✅ Можно изменить текст заголовка/подзаголовка
- ✅ Можно заменить dual buttons на single button или stacked
- ✅ Можно убрать home indicator

#### Layout 2: Onboarding with Accent (Light Background)

Onboarding screen с цветными акцентами в тексте.

```css
/* Onboarding Accent Screen */
--onboarding-padding-top: 10px;
--onboarding-padding-bottom: 20px;
--onboarding-bg: #FAFAFB;
```

**Структура**:
```
┌─────────────────────────────────────┐
│                                     │ 10px padding top
│       "One app for                  │ 32px/700 title
│      any currencies"                │ (purple accent)
│                                     │ 10px spacing
│   "Own your limits with custom...   │ 16px/400 subtitle
│   ...spending smarter"              │ (with purple accents)
│                                     │
│                                     │ 20px spacing
│          [Sign in]                  │ Filled button (44px)
│     [Create an account]             │ Outline button (44px)
│                                     │
│         ────────                    │ Home indicator
└─────────────────────────────────────┘
```

**Характеристики**:
- Background: #FAFAFB (light gray)
- Padding: 10px vertical, 16px horizontal
- Title: 32px/700, center
  - Mixed colors: #09101D + #4141E6 accents
- Subtitle: 16px/400, center, letter-spacing 1
  - Mixed colors: #09101D + #4141E6 accents
- Buttons: stacked vertical, 44px height, spacing 10px
  - "Sign in": filled (bg #4141E6, text white)
  - "Create an account": outline (border #4141E6, text #4141E6)
- Home indicator: внизу

**Модульность**:
- ✅ Можно добавить/убрать цветные акценты
- ✅ Можно заменить на dual buttons вместо stacked
- ✅ Можно добавить 3-ю кнопку вертикально

#### Layout 3: Progress Screen with Content

Screen с progress bar, back button и контентом.

```css
/* Progress Screen */
--progress-screen-content-padding-top: 30px;
--progress-screen-height: 286px;     /* Компактный вариант */
```

**Структура**:
```
┌─────────────────────────────────────┐
│ ← Back                              │ 44px back button
│                                     │
│ ▮▮▮▮▯                               │ Progress bar (3px)
│                                     │
│                                     │ 30px padding
│   "Blockchains like Ethereum...     │ 24px/700 title
│   ...can have difficulty scaling."  │ (with purple accent)
│                                     │
└─────────────────────────────────────┘
```

**Характеристики**:
- Background: white
- Back button: top left, 44px height, icon 24px
- Progress bar: 3px height, 5 segments (4 active, 1 inactive)
- Content padding: 30px top, 16px horizontal, 10px bottom
- Title: 24px/700, center
  - Mixed colors: #09101D + #4141E6 accent

**Модульность**:
- ✅ Можно изменить количество сегментов progress bar (3, 4, 5, 6...)
- ✅ Можно добавить subtitle под title
- ✅ Можно добавить buttons внизу (1, 2 или stacked)
- ✅ Можно убрать back button

### Modular Components Matrix

Таблица совместимости компонентов для быстрого проектирования:

| Component          | Welcome Screen | Onboarding Screen | Progress Screen | Can Add More? |
|--------------------|----------------|-------------------|-----------------|---------------|
| Large Title (32px) | ✅             | ✅                | ❌              | ✅            |
| Medium Title (24px)| ❌             | ❌                | ✅              | ✅            |
| Subtitle (16px)    | ✅             | ✅                | ❌              | ✅            |
| Colored Accents    | ❌             | ✅                | ✅              | ✅            |
| Dual Buttons (52px)| ✅             | ❌                | ❌              | ✅            |
| Stacked Buttons (44px)| ❌          | ✅                | ❌              | ✅            |
| Home Indicator     | ✅             | ✅                | ❌              | ✅            |
| Progress Bar       | ❌             | ❌                | ✅              | ✅            |
| Back Button        | ❌             | ❌                | ✅              | ✅            |

### Extensibility Guide

Как расширять готовые блоки под требования backend:

#### Пример 1: Добавить 3-ю кнопку

**Исходный макет**: 2 кнопки вертикально

**Требование backend**: Нужна 3-я кнопка "Skip"

**Решение**:
```html
<!-- Original -->
<div class="button-stack">
  <button class="button button--filled">Sign in</button>
  <button class="button button--outline">Create an account</button>
</div>

<!-- Extended -->
<div class="button-stack">
  <button class="button button--filled">Sign in</button>
  <button class="button button--outline">Create an account</button>
  <button class="button button--text">Skip</button>  <!-- Added -->
</div>
```

#### Пример 2: Увеличить progress segments

**Исходный макет**: 5 сегментов progress bar

**Требование backend**: Нужно 7 шагов onboarding

**Решение**:
```html
<!-- Original (5 segments) -->
<div class="progress-bar">
  <div class="progress-bar__segment progress-bar__segment--active"></div>
  <div class="progress-bar__segment progress-bar__segment--active"></div>
  <div class="progress-bar__segment progress-bar__segment--active"></div>
  <div class="progress-bar__segment progress-bar__segment--active"></div>
  <div class="progress-bar__segment"></div>
</div>

<!-- Extended (7 segments) -->
<div class="progress-bar">
  <div class="progress-bar__segment progress-bar__segment--active"></div>
  <div class="progress-bar__segment progress-bar__segment--active"></div>
  <div class="progress-bar__segment progress-bar__segment--active"></div>
  <div class="progress-bar__segment progress-bar__segment--active"></div>
  <div class="progress-bar__segment"></div>
  <div class="progress-bar__segment"></div>  <!-- Added -->
  <div class="progress-bar__segment"></div>  <!-- Added -->
</div>
```

Segments автоматически распределяются равномерно через `flex: 1`.

#### Пример 3: Добавить дополнительные элементы

**Исходный макет**: Title + Subtitle + Buttons

**Требование**: Добавить image/illustration между title и subtitle

**Решение**:
```html
<div class="screen-content">
  <h1 class="screen-title-large">Welcome to Appka Studio</h1>

  <!-- Added illustration -->
  <img src="welcome-illustration.svg" class="screen-illustration"
       style="width: 200px; margin: 20px auto;" />

  <p class="screen-subtitle">Design made simple...</p>
  <div class="button-row">...</div>
</div>
```

### Complete CSS Implementation

```css
/* Screen Container Variables */
:root {
  /* Container */
  --screen-width: 375px;
  --screen-border-radius: 30px;
  --screen-bg-white: #FFFFFF;
  --screen-bg-light: #FAFAFB;

  /* Typography */
  --screen-title-large: 700 32px/1.4 'Archivo';
  --screen-title-medium: 700 24px/1.4 'Archivo';
  --screen-subtitle: 400 16px/1.4 'Archivo';
  --screen-subtitle-letter-spacing: 1px;

  /* Colors */
  --screen-text-primary: #09101D;
  --screen-text-dimmed: rgba(9, 16, 29, 0.40);
  --screen-accent: #4141E6;

  /* Elements */
  --home-indicator-width: 134px;
  --home-indicator-height: 5px;
  --progress-bar-height: 3px;
  --back-button-height: 44px;
  --button-height-large: 52px;
  --button-height-medium: 44px;
}

/* Screen Container */
.screen {
  width: var(--screen-width);
  border-radius: var(--screen-border-radius);
  background: var(--screen-bg-white);
  overflow: hidden;
}

.screen--light {
  background: var(--screen-bg-light);
}

/* Screen Typography */
.screen-title-large {
  font: var(--screen-title-large);
  color: var(--screen-text-primary);
  text-align: center;
}

.screen-title-medium {
  font: var(--screen-title-medium);
  color: var(--screen-text-primary);
  text-align: center;
}

.screen-subtitle {
  font: var(--screen-subtitle);
  color: var(--screen-text-primary);
  letter-spacing: var(--screen-subtitle-letter-spacing);
  text-align: center;
}

.screen-subtitle--dimmed {
  color: var(--screen-text-dimmed);
}

.text-accent {
  color: var(--screen-accent);
}

/* Home Indicator */
.home-indicator {
  width: var(--home-indicator-width);
  height: var(--home-indicator-height);
  background: var(--screen-text-primary);
  border-radius: 100px;
  margin: 21px auto 0;
}

/* Progress Bar */
.progress-bar {
  display: flex;
  gap: 10px;
  height: var(--progress-bar-height);
  padding: 10px 16px;
}

.progress-bar__segment {
  flex: 1;
  height: 100%;
  background: rgba(11, 36, 251, 0.20);
}

.progress-bar__segment--active {
  background: var(--screen-accent);
}

.progress-bar__segment:first-child,
.progress-bar__segment:first-child.progress-bar__segment--active {
  border-radius: 10px 0 0 10px;
}

.progress-bar__segment:last-child,
.progress-bar__segment:last-child.progress-bar__segment--active {
  border-radius: 0 10px 10px 0;
}

/* Back Button */
.back-button {
  height: var(--back-button-height);
  padding: 10px 16px;
  background: transparent;
  border: none;
  cursor: pointer;
}

.back-button__icon-wrapper {
  width: 24px;
  height: 24px;
  background: rgba(9, 16, 29, 0.20);
  border-radius: 100px;
  padding: 6px;
  display: flex;
  align-items: center;
  justify-content: center;
}

/* Button Groups */
.button-row {
  display: flex;
  gap: 10px;
  padding: 0 16px;
}

.button-row .button {
  flex: 1;
}

.button-stack {
  display: flex;
  flex-direction: column;
  gap: 10px;
  padding: 10px 16px;
}

.button {
  height: var(--button-height-medium);
  padding: 10px 16px;
  border-radius: 15px;
  font: 600 16px/1.4 'Archivo';
  cursor: pointer;
  border: none;
  display: flex;
  align-items: center;
  justify-content: center;
}

.button--large {
  height: var(--button-height-large);
}

.button--filled {
  background: var(--screen-text-primary);
  color: white;
}

.button--filled-accent {
  background: var(--screen-accent);
  color: white;
}

.button--outline {
  background: transparent;
  border: 1px solid var(--screen-text-primary);
  color: var(--screen-text-primary);
}

.button--outline-accent {
  background: transparent;
  border: 1px solid var(--screen-accent);
  color: var(--screen-accent);
}
```

### Usage Examples

```html
<!-- Welcome Screen -->
<div class="screen">
  <div style="padding: 50px 16px;">
    <h1 class="screen-title-large">Welcome to Appka Studio</h1>
    <p class="screen-subtitle screen-subtitle--dimmed">
      Design made simple for your business, idea, app and more
    </p>
  </div>

  <div class="button-row">
    <button class="button button--large button--outline">Sign in</button>
    <button class="button button--large button--filled">Register</button>
  </div>

  <div style="height: 34px;">
    <div class="home-indicator"></div>
  </div>
</div>

<!-- Onboarding with Accent -->
<div class="screen screen--light">
  <div style="padding: 10px 16px;">
    <h1 class="screen-title-large">
      One app for<br/>
      <span class="text-accent">any currencies</span>
    </h1>
    <p class="screen-subtitle">
      Own your limits with <span class="text-accent">custom budgets</span>
      and save more by <span class="text-accent">spending smarter</span>
    </p>
  </div>

  <div class="button-stack">
    <button class="button button--filled-accent">Sign in</button>
    <button class="button button--outline-accent">Create an account</button>
  </div>

  <div style="height: 34px;">
    <div class="home-indicator"></div>
  </div>
</div>

<!-- Progress Screen -->
<div class="screen">
  <button class="back-button">
    <div class="back-button__icon-wrapper">
      <img src="back-icon.svg" alt="Back" />
    </div>
  </button>

  <div class="progress-bar">
    <div class="progress-bar__segment progress-bar__segment--active"></div>
    <div class="progress-bar__segment progress-bar__segment--active"></div>
    <div class="progress-bar__segment progress-bar__segment--active"></div>
    <div class="progress-bar__segment progress-bar__segment--active"></div>
    <div class="progress-bar__segment"></div>
  </div>

  <div style="padding: 30px 16px 10px;">
    <h2 class="screen-title-medium">
      Blockchains like Ethereum & Bitcoin offer security and decentralization,
      but <span class="text-accent">can have difficulty scaling</span>.
    </h2>
  </div>
</div>
```

---

## Shopping & Orders

Модульная система компонентов для e-commerce приложений: списки товаров, корзина покупок, подтверждение заказа. Все компоненты можно комбинировать и расширять в зависимости от требований backend и бизнес-логики.

### Принцип модульности

**Каждый экран покупок состоит из переиспользуемых блоков:**
- Section Header (заголовок + описание)
- Icon Action Buttons (круглые кнопки с иконками)
- Product List Items (товары с изображением и инфо)
- Quantity Stepper (контрол изменения количества)
- List Dividers (разделители между элементами)

Эти блоки можно свободно комбинировать, добавлять или удалять для создания различных экранов: корзина, список заказов, подтверждение, история покупок и т.д.

### Container Specifications

```css
/* Screen Container */
--shopping-screen-width: 375px;
--shopping-screen-border-radius: 30px;
--shopping-screen-bg: #FFFFFF;
--shopping-screen-padding-v: 30px;

/* Content Padding */
--shopping-content-padding-h: 16px;  /* Standard horizontal padding */
--shopping-action-padding-h: 32px;   /* For action buttons row */
```

### Typography System

```css
/* Section Header Typography */
--shopping-header-title: 700 24px/1.40 'Archivo';
--shopping-header-title-color: #09101D;
--shopping-header-subtitle: 400 14px/1.40 'Archivo';
--shopping-header-subtitle-color: #747B84;  /* Gray subtitle text */
--shopping-header-subtitle-width: 343px;     /* Max width for readability */

/* Product Typography */
--shopping-product-title: 600 15px/1.40 'Archivo';
--shopping-product-title-color: #09101D;
--shopping-product-price: 600 13px/1.40 'Archivo';
--shopping-product-price-color: #09101D;
--shopping-product-meta: 400 14px/1.40 'Archivo';
--shopping-product-meta-color: #414249;      /* Dark gray for quantity/weight */

/* Action Button Typography */
--shopping-action-label: 600 13px/1.40 'Archivo';
--shopping-action-label-color: #09101D;

/* Stepper Typography */
--shopping-stepper-number: 500 12px/1.40 'Archivo';
--shopping-stepper-number-color: #2A2B2F;    /* Dark text for numbers */
```

**Новые цвета для палитры:**
```css
--color-subtitle-gray: #747B84;     /* Для subtitles и secondary text */
--color-meta-gray: #414249;         /* Для quantity/weight информации */
--color-stepper-text: #2A2B2F;      /* Для чисел в stepper */
--color-divider-line: #EAEEEF2;     /* Для разделительных линий */
```

### 1. Section Header Component

Centered title и subtitle для заголовков секций (Order confirmed, Your Cart, и т.д.)

**Specifications:**
```css
/* Container */
--section-header-padding-h: 16px;
--section-header-padding-v: 10px;
--section-header-spacing: 5px;      /* Between title and subtitle */
--section-header-bg: #FFFFFF;

/* Title */
--section-header-title-font: 700 24px/1.40 'Archivo';
--section-header-title-color: #09101D;
--section-header-title-align: center;

/* Subtitle */
--section-header-subtitle-font: 400 14px/1.40 'Archivo';
--section-header-subtitle-color: #747B84;
--section-header-subtitle-width: 343px;
--section-header-subtitle-align: center;
```

**Visual Structure:**
```
┌─────────────────────────────────────────┐
│           Section Header                │
│  ┌───────────────────────────────────┐  │
│  │     Order confirmed (24px/700)    │  │ ← Title
│  ├───────────────────────────────────┤  │
│  │ You can add or edit items until   │  │ ← Subtitle (343px width)
│  │      shopping begins (14px/400)   │  │
│  └───────────────────────────────────┘  │
└─────────────────────────────────────────┘
     Padding: 16px H × 10px V
     Spacing: 5px between elements
```

### 2. Icon Action Buttons

Круглые кнопки с иконкой сверху и текстовым label снизу. Используются для главных действий (Add items, Reshedule, More и т.д.)

**Specifications:**
```css
/* Button Group Container */
--action-buttons-padding-top: 10px;
--action-buttons-padding-bottom: 20px;
--action-buttons-padding-h: 32px;
--action-buttons-spacing: 10px;              /* Between buttons */
--action-buttons-distribution: space-between; /* Equal spacing */

/* Single Button Container */
--action-button-padding-top: 10px;
--action-button-padding-h: 10px;
--action-button-padding-bottom: 5px;
--action-button-border-radius: 15px;
--action-button-spacing: 5px;                /* Between icon and label */

/* Icon Container - Active State */
--action-icon-active-size: 44px;
--action-icon-active-padding: 12px;          /* Icon 20px × 20px */
--action-icon-active-bg: #4141E6;            /* Primary blue */
--action-icon-active-border-radius: 30px;    /* Fully rounded */

/* Icon Container - Inactive State */
--action-icon-inactive-size: 44px;
--action-icon-inactive-padding: 14px;        /* Icon 16px × 16px (smaller) */
--action-icon-inactive-bg: #F4F6F9;          /* Light gray */
--action-icon-inactive-border-radius: 30px;

/* Label Text */
--action-label-font: 600 13px/1.40 'Archivo';
--action-label-color: #09101D;
```

**Visual Structure:**
```
┌──────────────────────────────────────────────────────────────────┐
│              Action Buttons Row (padding 32px H)                 │
│  ┌─────────────┐      ┌──────────────┐      ┌──────────────┐    │
│  │  ┌───────┐  │      │  ┌────────┐  │      │  ┌────────┐  │    │
│  │  │ 🎯    │  │      │  │  📅    │  │      │  │  ⋯     │  │    │
│  │  │ 44px  │  │      │  │ 44px   │  │      │  │ 44px   │  │    │ ← Icon
│  │  └───────┘  │      │  └────────┘  │      │  └────────┘  │    │   circles
│  │ Add items  │      │ Reshedule   │      │   More      │    │ ← Labels
│  │ (13px/600) │      │ (13px/600)  │      │ (13px/600)  │    │   (13px)
│  └─────────────┘      └──────────────┘      └──────────────┘    │
└──────────────────────────────────────────────────────────────────┘
      Active (#4141E6)   Inactive (#F4F6F9)   Inactive (#F4F6F9)
         Padding 12px       Padding 14px         Padding 14px
```

**States:**
- **Active**: Background #4141E6 (primary blue), icon padding 12px (icon 20px)
- **Inactive**: Background #F4F6F9 (light gray), icon padding 14px (icon 16px - меньше!)

### 3. Product List Item

Компонент для отображения товара в списке: изображение, название, цена/вес, quantity selector

**Specifications:**
```css
/* List Item Layout */
--product-item-padding-left: 16px;
--product-item-padding-right: 16px;
--product-item-bg: #FFFFFF;

/* Product Image */
--product-image-size: 40px;
--product-image-border-radius: 15px;
--product-image-bg: #F4F6F9;             /* Background for image container */
--product-image-padding-v: 10px;
--product-image-padding-right: 10px;

/* Product Info Area */
--product-info-padding-v: 12px;
--product-info-width: 160px;             /* Max width for title/price */

/* Product Title */
--product-title-font: 600 15px/1.40 'Archivo';
--product-title-color: #09101D;

/* Product Details (Price + Meta) */
--product-price-font: 600 13px/1.40 'Archivo';
--product-price-color: #09101D;
--product-meta-font: 400 14px/1.40 'Archivo';
--product-meta-color: #414249;           /* Quantity/weight text */
--product-meta-separator: ' ・ ';         /* Middle dot separator */

/* Quantity Selector Positioning */
--product-quantity-padding-h: 16px;
```

**Visual Structure:**
```
┌────────────────────────────────────────────────────────────────────┐
│  [16] [Image] [10] │ Title + Price/Meta │ [16] [Stepper] [16]     │
│  px   40×40   px   │   (Expanded)        │ px              px      │
└────────────────────────────────────────────────────────────────────┘

Detailed breakdown:
┌────────────────────────────────────────────────────────────────────┐
│ 16px │ ┌────┐ │ Toasts Bread (15px/600)         │ 16px │ ┌──────┐ │
│      │ │🍞  │ │ $0.75 ・ 280 g                  │      │ │ - 1 +│ │
│      │ └────┘ │ 13px/600   14px/400             │      │ └──────┘ │
│      │ 40×40  │                                  │      │ Stepper  │
└────────────────────────────────────────────────────────────────────┘
         10px →     ← 160px max width →                 ← 16px
```

**Examples:**
1. **Toasts Bread**: $0.75 ・ 280 g (quantity: 1)
2. **Itambe Milk**: $0.95 ・ 33 Oz (quantity: 2)
3. **Avocado**: $2.50 ・ 2 pcs (quantity: 1)

### 4. Quantity Stepper Component

Pill-shaped контрол для изменения количества товара с кнопками минус/плюс и числом посередине

**Specifications:**
```css
/* Stepper Container */
--stepper-padding: 2px;
--stepper-border-radius: 20px;
--stepper-bg: #F4F6F9;                   /* Light gray pill */
--stepper-spacing: 15px;                 /* Between minus, number, plus */

/* Minus/Plus Buttons */
--stepper-button-size: 24px;
--stepper-button-padding: 4px;           /* Icon size: 16px × 16px */
--stepper-button-bg: #4141E6;            /* Primary blue */
--stepper-button-border-radius: 20px;    /* Fully rounded */
--stepper-button-icon-size: 16px;

/* Number Display */
--stepper-number-font: 500 12px/1.40 'Archivo';
--stepper-number-color: #2A2B2F;
--stepper-number-spacing: 2px;           /* Internal spacing */
```

**Visual Structure:**
```
┌─────────────────────────────────────┐
│  Stepper (pill bg #F4F6F9)          │
│  ┌────┐  [15px]  ┌──┐  [15px] ┌────┐│
│  │ −  │          │ 1│          │ +  ││ ← Total height: 28px
│  │24px│          └──┘          │24px││   (24px buttons + 2px padding × 2)
│  └────┘   12px/500/2A2B2F      └────┘│
│  #4141E6                       #4141E6
└─────────────────────────────────────┘
   Padding 4px                 Padding 4px
   Icon 16×16                  Icon 16×16
```

**Layout breakdown:**
- Outer padding: 2px
- Minus button: 24px circle, blue (#4141E6), icon 16×16
- Spacing: 15px
- Number: 12px/500, color #2A2B2F
- Spacing: 15px
- Plus button: 24px circle, blue (#4141E6), icon 16×16

### 5. List Dividers

Разделительные линии между товарами в списке

**Specifications:**
```css
/* Divider Container */
--divider-container-padding-h: 16px;
--divider-container-padding-v: 10px;
--divider-inner-padding-v: 5px;

/* Divider Line */
--divider-line-height: 1px;
--divider-line-color: #EAEEEF2;          /* Light gray line */
--divider-line-width: 100%;
```

**Visual Structure:**
```
┌────────────────────────────────────────┐
│  Padding 16px H × 10px V               │
│    ┌────────────────────────────────┐  │
│    │ Inner padding 5px V            │  │
│    ├────────────────────────────────┤  │ ← 1px line (#EAEEEF2)
│    │ Inner padding 5px V            │  │
│    └────────────────────────────────┘  │
└────────────────────────────────────────┘
```

### Complete Layout: Order Confirmation Screen

**Полная структура экрана подтверждения заказа:**

```
┌───────────────────────────────────────────────────────┐
│  Screen Container (375px, borderRadius 30px)          │
│  Padding: 30px V                                      │
│  ┌─────────────────────────────────────────────────┐  │
│  │ Section Header (padding 16px H × 10px V)        │  │
│  │   Order confirmed (24px/700, center)            │  │
│  │   You can add or edit items... (14px/400)       │  │
│  └─────────────────────────────────────────────────┘  │
│  ┌─────────────────────────────────────────────────┐  │
│  │ Action Buttons (padding 32px H, 10px T, 20px B) │  │
│  │  [Add items]  [Reshedule]  [More]               │  │
│  │   Active       Inactive     Inactive            │  │
│  └─────────────────────────────────────────────────┘  │
│  ┌─────────────────────────────────────────────────┐  │
│  │ Product Item #1                                  │  │
│  │  [🍞] Toasts Bread  $0.75 ・ 280 g  [- 1 +]     │  │
│  └─────────────────────────────────────────────────┘  │
│  ───────────────────────────────────────────────────  │ ← Divider
│  ┌─────────────────────────────────────────────────┐  │
│  │ Product Item #2                                  │  │
│  │  [🥛] Itambe Milk  $0.95 ・ 33 Oz  [- 2 +]      │  │
│  └─────────────────────────────────────────────────┘  │
│  ───────────────────────────────────────────────────  │ ← Divider
│  ┌─────────────────────────────────────────────────┐  │
│  │ Product Item #3                                  │  │
│  │  [🥑] Avocado  $2.50 ・ 2 pcs  [- 1 +]          │  │
│  └─────────────────────────────────────────────────┘  │
└───────────────────────────────────────────────────────┘
```

**Компоненты в этом layout:**
1. Section Header (title + subtitle)
2. Icon Action Buttons Row (3 кнопки)
3. Product List Item × 3
4. List Dividers × 2 (между товарами)

### Modular Components Matrix

Таблица показывает, какие компоненты используются в разных экранах и можно ли их добавлять:

| Component              | Order Confirm | Shopping Cart | Order History | Can Add More? |
|------------------------|---------------|---------------|---------------|---------------|
| Section Header         | ✅            | ✅            | ✅            | ✅            |
| Icon Action Buttons    | ✅ (3 шт)     | ✅ (2 шт)     | ❌            | ✅ Flexible   |
| Product List Item      | ✅ (3 шт)     | ✅ (5+ шт)    | ✅ (10+ шт)   | ✅ Dynamic    |
| Quantity Stepper       | ✅            | ✅            | ❌            | ✅ Conditional|
| List Dividers          | ✅            | ✅            | ✅            | ✅ Auto       |
| Total Price Section    | ❌            | ✅            | ✅            | ✅            |
| Checkout Button        | ❌            | ✅            | ❌            | ✅            |

**Гибкость:**
- **Icon Action Buttons**: можно добавить 4-ю, 5-ю кнопку или убрать до 2-х
- **Product List Items**: количество динамическое (от 1 до бесконечности)
- **Quantity Stepper**: показывать только на редактируемых экранах
- **List Dividers**: автоматически между каждым item

### Extensibility Guide

Практические примеры расширения компонентов для различных сценариев:

#### Example 1: Добавление 4-й Action Button

Если нужно добавить дополнительное действие (например, "Share order"), просто добавьте кнопку в Row:

```html
<div class="action-buttons">
  <div class="action-button action-button--active">
    <div class="action-icon action-icon--active">
      <svg class="icon-20"><!-- Add icon --></svg>
    </div>
    <span class="action-label">Add items</span>
  </div>
  <div class="action-button">
    <div class="action-icon action-icon--inactive">
      <svg class="icon-16"><!-- Calendar icon --></svg>
    </div>
    <span class="action-label">Reshedule</span>
  </div>
  <div class="action-button">
    <div class="action-icon action-icon--inactive">
      <svg class="icon-16"><!-- More icon --></svg>
    </div>
    <span class="action-label">More</span>
  </div>
  <!-- NEW: 4-я кнопка -->
  <div class="action-button">
    <div class="action-icon action-icon--inactive">
      <svg class="icon-16"><!-- Share icon --></svg>
    </div>
    <span class="action-label">Share</span>
  </div>
</div>
```

**Note:** При 4-х кнопках используйте `display: grid; grid-template-columns: repeat(4, 1fr);` вместо `justify-content: space-between`.

#### Example 2: Добавление Total Price Section

Если нужно показать итоговую цену (для корзины), добавьте секцию после списка товаров:

```html
<!-- After product list items -->
<div class="divider-container">
  <div class="divider-line"></div>
</div>

<!-- NEW: Total Price Section -->
<div class="total-section">
  <div class="total-row">
    <span class="total-label">Subtotal</span>
    <span class="total-value">$4.20</span>
  </div>
  <div class="total-row">
    <span class="total-label">Delivery fee</span>
    <span class="total-value">$2.99</span>
  </div>
  <div class="total-row total-row--final">
    <span class="total-label total-label--bold">Total</span>
    <span class="total-value total-value--bold">$7.19</span>
  </div>
</div>

<div class="checkout-button-container">
  <button class="button button--filled button--large">
    Proceed to checkout
  </button>
</div>
```

**CSS для Total Section:**
```css
.total-section {
  padding: 20px 16px;
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.total-row {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.total-label {
  font: 400 14px/1.40 'Archivo';
  color: var(--color-black);
}

.total-value {
  font: 600 14px/1.40 'Archivo';
  color: var(--color-black);
}

.total-row--final {
  padding-top: 12px;
  border-top: 1px solid var(--color-divider-line);
}

.total-label--bold {
  font-weight: 600;
  font-size: 16px;
}

.total-value--bold {
  font-size: 18px;
  color: var(--color-primary);
}
```

#### Example 3: Убрать Quantity Stepper (для Order History)

Если показываете историю заказов (не редактируемая), уберите stepper и покажите только количество:

```html
<div class="product-item">
  <div class="product-image">
    <img src="toast.jpg" alt="Toasts Bread">
  </div>
  <div class="product-info">
    <div class="product-title">Toasts Bread</div>
    <div class="product-details">
      <span class="product-price">$0.75</span>
      <span class="product-meta"> ・ 280 g</span>
    </div>
  </div>
  <!-- REMOVE stepper, ADD quantity display -->
  <div class="product-quantity-static">
    <span class="quantity-text">Qty: 1</span>
  </div>
</div>
```

**CSS для Static Quantity:**
```css
.product-quantity-static {
  padding: 0 16px;
  display: flex;
  align-items: center;
}

.quantity-text {
  font: 500 13px/1.40 'Archivo';
  color: var(--color-meta-gray);
}
```

#### Example 4: Динамическое добавление товаров

Товары в списке генерируются динамически из backend. При добавлении новых товаров автоматически добавляются dividers:

```javascript
// Example: Adding products dynamically
const products = [
  { name: 'Toasts Bread', price: 0.75, meta: '280 g', qty: 1, img: 'toast.jpg' },
  { name: 'Itambe Milk', price: 0.95, meta: '33 Oz', qty: 2, img: 'milk.jpg' },
  { name: 'Avocado', price: 2.50, meta: '2 pcs', qty: 1, img: 'avocado.jpg' },
  // Backend добавил новый товар:
  { name: 'Butter', price: 3.20, meta: '200 g', qty: 1, img: 'butter.jpg' }
];

const productList = document.getElementById('product-list');

products.forEach((product, index) => {
  // Add product item
  const item = createProductItem(product);
  productList.appendChild(item);

  // Add divider (except after last item)
  if (index < products.length - 1) {
    const divider = createDivider();
    productList.appendChild(divider);
  }
});
```

**Результат:** Система автоматически адаптируется под любое количество товаров.

### CSS Implementation

Complete CSS для всех компонентов Shopping & Orders:

```css
/* ==================== */
/* Shopping Screen Container */
/* ==================== */

.shopping-screen {
  width: 375px;
  padding: 30px 0;
  background: #FFFFFF;
  border-radius: 30px;
  overflow: hidden;
}

/* ==================== */
/* Section Header */
/* ==================== */

.section-header {
  padding: 10px 16px;
  background: #FFFFFF;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 5px;
}

.section-header__title {
  font: 700 24px/1.40 'Archivo';
  color: #09101D;
  text-align: center;
}

.section-header__subtitle {
  max-width: 343px;
  font: 400 14px/1.40 'Archivo';
  color: #747B84;
  text-align: center;
}

/* ==================== */
/* Action Buttons Row */
/* ==================== */

.action-buttons {
  padding: 10px 32px 20px;
  display: flex;
  justify-content: space-between;
  gap: 10px;
}

.action-button {
  padding: 10px 10px 5px;
  border-radius: 15px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 5px;
  cursor: pointer;
  transition: background-color 0.2s;
}

.action-button:hover {
  background-color: rgba(0, 0, 0, 0.02);
}

/* Icon Container - Active State */
.action-icon--active {
  width: 44px;
  height: 44px;
  padding: 12px; /* Icon 20×20 */
  background: #4141E6;
  border-radius: 30px;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.2s;
}

/* Icon Container - Inactive State */
.action-icon--inactive {
  width: 44px;
  height: 44px;
  padding: 14px; /* Icon 16×16 */
  background: #F4F6F9;
  border-radius: 30px;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.2s;
}

.action-icon--active svg {
  width: 20px;
  height: 20px;
  color: #FFFFFF;
}

.action-icon--inactive svg {
  width: 16px;
  height: 16px;
  color: #09101D;
}

.action-label {
  font: 600 13px/1.40 'Archivo';
  color: #09101D;
}

/* ==================== */
/* Product List Item */
/* ==================== */

.product-item {
  background: #FFFFFF;
  display: flex;
  align-items: center;
}

.product-item__spacer-left {
  width: 16px;
}

.product-item__image-container {
  padding: 10px 10px 10px 0;
}

.product-image {
  width: 40px;
  height: 40px;
  background: #F4F6F9;
  border-radius: 15px;
  overflow: hidden;
}

.product-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.product-info {
  flex: 1;
  padding: 12px 0;
  display: flex;
  flex-direction: column;
}

.product-title {
  max-width: 160px;
  font: 600 15px/1.40 'Archivo';
  color: #09101D;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

.product-details {
  max-width: 160px;
  font: 400 14px/1.40 'Archivo';
}

.product-price {
  font-weight: 600;
  font-size: 13px;
  color: #09101D;
}

.product-meta {
  font-weight: 400;
  font-size: 14px;
  color: #414249;
}

.product-item__spacer-right {
  width: 16px;
}

.product-item__quantity-container {
  padding: 0 16px;
}

/* ==================== */
/* Quantity Stepper */
/* ==================== */

.quantity-stepper {
  padding: 2px;
  background: #F4F6F9;
  border-radius: 20px;
  display: flex;
  align-items: center;
  gap: 15px;
}

.stepper-button {
  width: 24px;
  height: 24px;
  padding: 4px; /* Icon 16×16 */
  background: #4141E6;
  border-radius: 20px;
  border: none;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: background-color 0.2s;
}

.stepper-button:hover {
  background: #3333D1;
}

.stepper-button:active {
  background: #2626BC;
}

.stepper-button svg {
  width: 16px;
  height: 16px;
  color: #FFFFFF;
}

.stepper-number {
  min-width: 16px;
  font: 500 12px/1.40 'Archivo';
  color: #2A2B2F;
  text-align: center;
}

/* ==================== */
/* List Divider */
/* ==================== */

.divider-container {
  padding: 10px 16px;
}

.divider-line {
  width: 100%;
  height: 1px;
  background: #EAEEEF2;
}

/* ==================== */
/* Responsive Behaviors */
/* ==================== */

/* For 4 action buttons, use grid instead of space-between */
.action-buttons--four-items {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
  justify-items: center;
}

/* For very long product lists, add scroll */
.product-list-container {
  max-height: 500px;
  overflow-y: auto;
}

/* ==================== */
/* Hover & Active States */
/* ==================== */

.product-item:hover {
  background: rgba(0, 0, 0, 0.01);
}

.action-button--active .action-icon--inactive {
  background: #4141E6;
}

.action-button--active .action-icon--inactive svg {
  color: #FFFFFF;
}
```

### Usage Examples

#### Example 1: Basic Order Confirmation Screen

```html
<div class="shopping-screen">
  <!-- Section Header -->
  <div class="section-header">
    <h2 class="section-header__title">Order confirmed</h2>
    <p class="section-header__subtitle">
      You can add or edit items until shopping begins
    </p>
  </div>

  <!-- Action Buttons -->
  <div class="action-buttons">
    <div class="action-button action-button--active">
      <div class="action-icon action-icon--active">
        <svg class="icon-20"><!-- Plus icon --></svg>
      </div>
      <span class="action-label">Add items</span>
    </div>
    <div class="action-button">
      <div class="action-icon action-icon--inactive">
        <svg class="icon-16"><!-- Calendar icon --></svg>
      </div>
      <span class="action-label">Reshedule</span>
    </div>
    <div class="action-button">
      <div class="action-icon action-icon--inactive">
        <svg class="icon-16"><!-- More icon --></svg>
      </div>
      <span class="action-label">More</span>
    </div>
  </div>

  <!-- Product List -->
  <div class="product-list">
    <!-- Item 1 -->
    <div class="product-item">
      <div class="product-item__spacer-left"></div>
      <div class="product-item__image-container">
        <div class="product-image">
          <img src="toast.jpg" alt="Toasts Bread">
        </div>
      </div>
      <div class="product-info">
        <div class="product-title">Toasts Bread</div>
        <div class="product-details">
          <span class="product-price">$0.75</span>
          <span class="product-meta"> ・ 280 g</span>
        </div>
      </div>
      <div class="product-item__spacer-right"></div>
      <div class="product-item__quantity-container">
        <div class="quantity-stepper">
          <button class="stepper-button" aria-label="Decrease quantity">
            <svg><!-- Minus icon --></svg>
          </button>
          <span class="stepper-number">1</span>
          <button class="stepper-button" aria-label="Increase quantity">
            <svg><!-- Plus icon --></svg>
          </button>
        </div>
      </div>
    </div>

    <!-- Divider -->
    <div class="divider-container">
      <div class="divider-line"></div>
    </div>

    <!-- Item 2 -->
    <div class="product-item">
      <div class="product-item__spacer-left"></div>
      <div class="product-item__image-container">
        <div class="product-image">
          <img src="milk.jpg" alt="Itambe Milk">
        </div>
      </div>
      <div class="product-info">
        <div class="product-title">Itambe Milk</div>
        <div class="product-details">
          <span class="product-price">$0.95</span>
          <span class="product-meta"> ・ 33 Oz</span>
        </div>
      </div>
      <div class="product-item__spacer-right"></div>
      <div class="product-item__quantity-container">
        <div class="quantity-stepper">
          <button class="stepper-button" aria-label="Decrease quantity">
            <svg><!-- Minus icon --></svg>
          </button>
          <span class="stepper-number">2</span>
          <button class="stepper-button" aria-label="Increase quantity">
            <svg><!-- Plus icon --></svg>
          </button>
        </div>
      </div>
    </div>

    <!-- Divider -->
    <div class="divider-container">
      <div class="divider-line"></div>
    </div>

    <!-- Item 3 -->
    <div class="product-item">
      <div class="product-item__spacer-left"></div>
      <div class="product-item__image-container">
        <div class="product-image">
          <img src="avocado.jpg" alt="Avocado">
        </div>
      </div>
      <div class="product-info">
        <div class="product-title">Avocado</div>
        <div class="product-details">
          <span class="product-price">$2.50</span>
          <span class="product-meta"> ・ 2 pcs</span>
        </div>
      </div>
      <div class="product-item__spacer-right"></div>
      <div class="product-item__quantity-container">
        <div class="quantity-stepper">
          <button class="stepper-button" aria-label="Decrease quantity">
            <svg><!-- Minus icon --></svg>
          </button>
          <span class="stepper-number">1</span>
          <button class="stepper-button" aria-label="Increase quantity">
            <svg><!-- Plus icon --></svg>
          </button>
        </div>
      </div>
    </div>
  </div>
</div>
```

#### Example 2: Shopping Cart with Total

```html
<div class="shopping-screen">
  <!-- Section Header -->
  <div class="section-header">
    <h2 class="section-header__title">Shopping Cart</h2>
    <p class="section-header__subtitle">
      3 items ready for checkout
    </p>
  </div>

  <!-- No Action Buttons in Cart view -->

  <!-- Product List (same as above) -->
  <div class="product-list">
    <!-- Products here... -->
  </div>

  <!-- Total Section -->
  <div class="divider-container">
    <div class="divider-line"></div>
  </div>

  <div class="total-section">
    <div class="total-row">
      <span class="total-label">Subtotal</span>
      <span class="total-value">$4.20</span>
    </div>
    <div class="total-row">
      <span class="total-label">Delivery fee</span>
      <span class="total-value">$2.99</span>
    </div>
    <div class="total-row total-row--final">
      <span class="total-label total-label--bold">Total</span>
      <span class="total-value total-value--bold">$7.19</span>
    </div>
  </div>

  <!-- Checkout Button -->
  <div class="checkout-button-container" style="padding: 0 16px 20px;">
    <button class="button button--filled button--large" style="width: 100%; height: 52px;">
      Proceed to checkout
    </button>
  </div>
</div>
```

#### Example 3: Order History (Read-only)

```html
<div class="shopping-screen">
  <!-- Section Header -->
  <div class="section-header">
    <h2 class="section-header__title">Order #12345</h2>
    <p class="section-header__subtitle">
      Delivered on March 15, 2025
    </p>
  </div>

  <!-- No Action Buttons -->

  <!-- Product List (without steppers) -->
  <div class="product-list">
    <div class="product-item">
      <div class="product-item__spacer-left"></div>
      <div class="product-item__image-container">
        <div class="product-image">
          <img src="toast.jpg" alt="Toasts Bread">
        </div>
      </div>
      <div class="product-info">
        <div class="product-title">Toasts Bread</div>
        <div class="product-details">
          <span class="product-price">$0.75</span>
          <span class="product-meta"> ・ 280 g</span>
        </div>
      </div>
      <!-- Static Quantity (no stepper) -->
      <div class="product-quantity-static">
        <span class="quantity-text">Qty: 1</span>
      </div>
    </div>

    <!-- More items... -->
  </div>

  <!-- Total (same as cart) -->
</div>
```

---

<!-- ============================================================================ -->
<!-- SECTION: Cards & Listings                                                   -->
<!-- FILE REFERENCE: design-system.md#cards--listings                            -->
<!-- USAGE: Hotel cards, property listings, travel bookings, featured content    -->
<!-- COMPONENTS: hotel-card, rating-badge, amenity-list, price-button            -->
<!-- AI NAVIGATION: Search for "COMPONENT:" tags to find specific components     -->
<!-- ============================================================================ -->

## Cards & Listings

Модульная система карточек для отображения контента: отели, рестораны, недвижимость, товары. Все компоненты можно комбинировать и расширять для различных типов listings.

### Принцип модульности

**Каждая карточка состоит из переиспользуемых блоков:**
- Card Image (изображение с overlay badges)
- Card Content Container (контейнер с информацией)
- Rating Display (рейтинг в виде звезд и числа)
- Rating Badge (цветной badge с оценкой)
- Tags Row (теги типа "Discount", "Secret Deal")
- Amenities List (удобства с иконками)
- Price Button (кнопка с ценой)

Эти блоки можно свободно комбинировать для создания различных типов карточек: hotel cards, restaurant cards, property cards, product cards и т.д.

### Container Specifications

```css
/* ========================================== */
/* COMPONENT: Card Container                  */
/* CATEGORY: Layout                           */
/* ========================================== */

/* Screen Container */
--card-screen-width: 375px;
--card-screen-padding-v: 30px;
--card-screen-border-radius: 30px;
--card-screen-bg: #FFFFFF;

/* Card Layout */
--card-container-padding-h: 16px;
--card-container-padding-v: 5px;
--card-spacing: 5px;                     /* Spacing between image and content */

/* Card Orientation */
--card-layout: horizontal;               /* Image + Content side by side */
```

### Typography System

```css
/* ========================================== */
/* COMPONENT: Card Typography                 */
/* CATEGORY: Text Styles                      */
/* ========================================== */

/* Card Title */
--card-title-font: 600 11px/1.40 'Archivo';
--card-title-color: #09101D;
--card-title-max-width: 128px;

/* Card Location */
--card-location-font: 400 10px/1.40 'Archivo';
--card-location-color: #09101D;
--card-location-max-width: 198px;

/* Rating Text */
--card-rating-number-font: 600 10px/1.40 'Archivo';
--card-rating-number-color: #FFFFFF;

--card-rating-label-font: 600 10px/1.40 'Archivo';
--card-rating-label-color: #09101D;

--card-rating-count-font: 400 10px/1.40 'Archivo';
--card-rating-count-color: #747B84;

/* Tag Text */
--card-tag-font: 600 8px/1.40 'Archivo';
--card-tag-color: #FFFFFF;

/* Amenity Text */
--card-amenity-font: 400 10px/1.40 'Archivo';
--card-amenity-color: #747B84;

/* Price Text */
--card-price-number-font: 600 11px/1.40 'Archivo';
--card-price-number-color: #09101D;

--card-price-currency-font: 400 11px/1.40 'Archivo';
--card-price-currency-color: #09101D;
```

**Новые цвета для палитры:**
```css
/* ========================================== */
/* COLORS: Cards & Listings Palette           */
/* ========================================== */

--color-rating-badge: #221874;          /* Dark purple для rating badge */
--color-price-button: #FFC043;          /* Yellow/gold для price button */
--color-badge-overlay: rgba(17, 187, 141, 0.05);  /* Очень светлый green для image overlay badge */
```

<!-- ============================================================================ -->
<!-- COMPONENT: Card Image Section                                               -->
<!-- USAGE: Left side of horizontal card with image and overlay badge            -->
<!-- VARIANTS: with-badge, no-badge, multiple-images                             -->
<!-- ============================================================================ -->

### 1. Card Image Component

Левая часть карточки - изображение с опциональным badge overlay в верхнем левом углу.

**Specifications:**
```css
/* ========================================== */
/* COMPONENT: Card Image                      */
/* FILE: cards-image.css                      */
/* ========================================== */

/* Image Container */
--card-image-width: 120px;
--card-image-height: 202px;              /* Aspect ratio ~1:1.68 (vertical) */
--card-image-border-radius: 15px;
--card-image-fit: cover;

/* Overlay Badge (top-left corner) */
--card-badge-overlay-size: 30px;
--card-badge-overlay-padding: 8px;       /* Icon 14×14px */
--card-badge-overlay-bg: rgba(17, 187, 141, 0.05);  /* 5% opacity green */
--card-badge-overlay-border: 0.10px solid #FFFFFF;
--card-badge-overlay-border-radius: 100px;  /* Circle */
--card-badge-overlay-position-top: 10px;
--card-badge-overlay-position-left: 10px;
```

**Visual Structure:**
```
┌────────────────────────┐
│  ┌──┐  Image           │ ← Badge overlay (30×30px)
│  │✓ │  120px × 202px   │   Top-left: 10px × 10px
│  └──┘                  │   Background: rgba(17,187,141,0.05)
│                        │   Border: 0.10px white
│                        │   BorderRadius: 100px (circle)
│      Hotel/Resort      │
│         Image          │
│                        │
│                        │
│                        │
│                        │
└────────────────────────┘
   BorderRadius: 15px
```

**Badge types:**
- **Favorite/Saved**: heart icon, indicates user saved this item
- **Verified**: checkmark icon, indicates verified listing
- **Featured**: star icon, indicates premium/featured content
- **New**: badge for new listings

<!-- ============================================================================ -->
<!-- COMPONENT: Card Content Container                                           -->
<!-- USAGE: Right side of horizontal card with all text info                     -->
<!-- VARIANTS: compact, detailed, with-amenities, without-amenities              -->
<!-- ============================================================================ -->

### 2. Card Content Container

Правая часть карточки - контейнер с padding, background и всей информацией о listing.

**Specifications:**
```css
/* ========================================== */
/* COMPONENT: Card Content Container          */
/* FILE: cards-content.css                    */
/* ========================================== */

/* Content Container */
--card-content-padding: 10px;
--card-content-bg: #F4F6F9;              /* Light gray background */
--card-content-border-radius: 15px;
--card-content-spacing: 5px;             /* Spacing between child elements */

/* Content Layout */
--card-content-flex: 1;                  /* Takes remaining width */
--card-content-flex-direction: column;
--card-content-align-items: flex-start;
```

**Visual Structure:**
```
┌──────────────────────────────┐
│  Content Container           │
│  Padding: 10px               │
│  Background: #F4F6F9          │
│  BorderRadius: 15px          │
│  ┌────────────────────────┐  │
│  │ Title + Stars          │  │ ← Spacing 5px
│  ├────────────────────────┤  │
│  │ Location               │  │ ← Spacing 5px
│  ├────────────────────────┤  │
│  │ Rating Badge + Text    │  │ ← Spacing 5px
│  ├────────────────────────┤  │
│  │ Tags (Discount, etc.)  │  │ ← Spacing 5px
│  ├────────────────────────┤  │
│  │ Amenities List         │  │ ← Spacing 5px
│  ├────────────────────────┤  │
│  │ Price Button           │  │
│  └────────────────────────┘  │
└──────────────────────────────┘
```

<!-- ============================================================================ -->
<!-- COMPONENT: Title & Star Rating Row                                          -->
<!-- USAGE: First row in card content - title and star rating                    -->
<!-- VARIANTS: 1-5 stars, with-title-only, compact                               -->
<!-- ============================================================================ -->

### 3. Title & Star Rating Component

Первая строка в content - название (left) и звезды (right).

**Specifications:**
```css
/* ========================================== */
/* COMPONENT: Title & Star Rating Row         */
/* FILE: cards-title-rating.css               -->
/* ========================================== */

/* Title */
--card-title-font: 600 11px/1.40 'Archivo';
--card-title-color: #09101D;
--card-title-max-width: 128px;
--card-title-overflow: hidden;
--card-title-text-overflow: ellipsis;

/* Star Rating */
--card-star-size: 15px;
--card-star-padding: 2px;
--card-star-border-radius: 100px;
--card-star-color: #FFC043;              /* Gold color for filled stars */
--card-star-spacing: 0px;                /* No spacing between stars */

/* Row Layout */
--title-rating-display: flex;
--title-rating-justify: space-between;
--title-rating-align: flex-start;
--title-rating-spacing: 10px;
```

**Visual Structure:**
```
┌────────────────────────────────────────────────┐
│  Planta Luxury...  [★][★][★][★][☆]           │
│  (128px max)       15px × 4 = 60px             │
│  11px/600          Gold #FFC043                │
└────────────────────────────────────────────────┘
   ← spacing 10px →
```

**Star states:**
- **Filled**: gold color (#FFC043), indicates active star
- **Empty**: gray color (#E0E0E0), indicates inactive star
- **Half**: can use icon or gradient for half-stars

<!-- ============================================================================ -->
<!-- COMPONENT: Location Text                                                    -->
<!-- USAGE: Shows location/address below title                                   -->
<!-- VARIANTS: with-icon, text-only, truncated                                   -->
<!-- ============================================================================ -->

### 4. Location Component

Второй элемент - местоположение (город, страна).

**Specifications:**
```css
/* ========================================== */
/* COMPONENT: Location Text                   -->
/* FILE: cards-location.css                   */
/* ========================================== */

/* Location Text */
--card-location-font: 400 10px/1.40 'Archivo';
--card-location-color: #09101D;
--card-location-max-width: 198px;

/* Optional: Location with Icon */
--location-icon-size: 12px;
--location-icon-color: #747B84;
--location-icon-spacing: 4px;
```

**Visual Structure:**
```
┌──────────────────────┐
│  Bali, Indonesia     │
│  10px/400            │
│  #09101D             │
│  Max width: 198px    │
└──────────────────────┘

OR with icon:
┌──────────────────────┐
│  📍 Bali, Indonesia  │
│  12px  10px/400      │
└──────────────────────┘
```

<!-- ============================================================================ -->
<!-- COMPONENT: Rating Badge & Text                                              -->
<!-- USAGE: Shows numerical rating with badge and review text                    -->
<!-- VARIANTS: badge-only, with-reviews, excellent/good/average                  -->
<!-- ============================================================================ -->

### 5. Rating Badge & Text Component

Рейтинг с цветным badge, label и количеством отзывов.

**Specifications:**
```css
/* ========================================== */
/* COMPONENT: Rating Badge & Text             */
/* FILE: cards-rating.css                     */
/* ========================================== */

/* Rating Badge */
--rating-badge-padding: 3px;
--rating-badge-bg: #221874;              /* Dark purple (NEW COLOR!) */
--rating-badge-border-radius: 5px;
--rating-badge-font: 600 10px/1.40 'Archivo';
--rating-badge-color: #FFFFFF;

/* Rating Label */
--rating-label-font: 600 10px/1.40 'Archivo';
--rating-label-color: #09101D;

/* Review Count */
--rating-count-font: 400 10px/1.40 'Archivo';
--rating-count-color: #747B84;
--rating-count-separator: ' | ';         /* Separator between label and count */

/* Row Layout */
--rating-row-spacing: 5px;               /* Between badge and text */
--rating-row-align: center;
```

**Visual Structure:**
```
┌──────────────────────────────────────────┐
│  [4.9]  Excellent | 41 reviews          │
│   ^^^   ^^^^^^^^^ ^^^^^^^^^^            │
│  Badge   Label     Count                │
│  3px     10/600    10/400               │
│  #221874 #09101D   #747B84              │
└──────────────────────────────────────────┘
   Spacing: 5px between elements
```

**Badge color variations (for future):**
- **Excellent (9.0-10.0)**: #221874 (dark purple)
- **Very Good (8.0-8.9)**: #4141E6 (primary blue)
- **Good (7.0-7.9)**: #11BB8D (success green)
- **Average (6.0-6.9)**: #FFC043 (yellow)
- **Below Average (<6.0)**: #E24949 (error red)

<!-- ============================================================================ -->
<!-- COMPONENT: Tags Row                                                         -->
<!-- USAGE: Shows promotional tags like "Discount", "Secret Deal"                -->
<!-- VARIANTS: 1-tag, 2-tags, 3+tags, different-colors                           -->
<!-- ============================================================================ -->

### 6. Tags Component

Цветные теги для промо-информации (Discount, Secret Deal, New, и т.д.).

**Specifications:**
```css
/* ========================================== */
/* COMPONENT: Tags Row                        */
/* FILE: cards-tags.css                       */
/* ========================================== */

/* Tag Container */
--card-tag-padding-h: 5px;
--card-tag-padding-v: 3px;
--card-tag-border-radius: 5px;
--card-tag-font: 600 8px/1.40 'Archivo';
--card-tag-color: #FFFFFF;

/* Tag Colors (by type) */
--tag-discount-bg: #11BB8D;              /* Success green */
--tag-secret-deal-bg: #11BB8D;           /* Success green */
--tag-new-bg: #4141E6;                   /* Primary blue */
--tag-featured-bg: #FFC043;              /* Gold yellow */
--tag-limited-bg: #E24949;               /* Error red */

/* Tags Row Layout */
--tags-row-spacing: 5px;                 /* Between tags */
--tags-row-display: flex;
--tags-row-wrap: wrap;
```

**Visual Structure:**
```
┌─────────────────────────────────┐
│  [Discount] [Secret Deal]       │
│   8px/600    8px/600            │
│   #11BB8D    #11BB8D            │
│   Padding: 5px H × 3px V        │
│   BorderRadius: 5px             │
└─────────────────────────────────┘
   Spacing: 5px between tags
```

**Tag types:**
1. **Discount** - green (#11BB8D), shows price discount available
2. **Secret Deal** - green (#11BB8D), special members-only offer
3. **New** - blue (#4141E6), new listing (< 30 days)
4. **Featured** - yellow (#FFC043), premium placement
5. **Limited** - red (#E24949), limited availability

<!-- ============================================================================ -->
<!-- COMPONENT: Amenities List                                                   -->
<!-- USAGE: Shows facilities/features with icons (WiFi, Pool, etc.)              -->
<!-- VARIANTS: 1-column, 2-columns, icon-only, with-text                         -->
<!-- ============================================================================ -->

### 7. Amenities List Component

Список удобств с иконками (WiFi, Pool, Sea food, и т.д.).

**Specifications:**
```css
/* ========================================== */
/* COMPONENT: Amenities List                  */
/* FILE: cards-amenities.css                  */
/* ========================================== */

/* Amenity Item */
--amenity-item-spacing: 5px;             /* Between icon and text */
--amenity-row-spacing: 0px;              /* Between rows (can add for vertical spacing) */

/* Amenity Icon */
--amenity-icon-size: 21px;               /* Container size */
--amenity-icon-padding: 5px;             /* Icon actual size ~11×10px */
--amenity-icon-border-radius: 100px;
--amenity-icon-color: #747B84;

/* Amenity Text */
--amenity-text-font: 400 10px/1.40 'Archivo';
--amenity-text-color: #747B84;

/* List Layout */
--amenities-list-display: flex;
--amenities-list-direction: column;
--amenities-list-gap: 0px;               /* Compact layout */
```

**Visual Structure:**
```
┌─────────────────────────┐
│  [🍤]  Sea food         │ ← Icon 21×21px, text 10px/400
│  [📶]  Free Wi-Fi       │   Spacing: 5px between icon and text
│  [🏊]  Pool             │   Color: #747B84 for both
│  [🍴]  Restaurant       │
└─────────────────────────┘
   Vertical spacing: 0px (compact)
```

**Common amenity icons:**
- **WiFi**: 📶 signal icon
- **Pool**: 🏊 swimming icon
- **Restaurant**: 🍴 utensils icon
- **Parking**: 🅿️ parking icon
- **Sea food**: 🍤 seafood icon
- **Beach**: 🏖️ beach icon
- **Gym**: 💪 dumbbell icon
- **Spa**: 🧖 spa icon

<!-- ============================================================================ -->
<!-- COMPONENT: Price Button                                                     -->
<!-- USAGE: Prominent button showing price at bottom of card                     -->
<!-- VARIANTS: with-currency, price-only, from-price, per-night                  -->
<!-- ============================================================================ -->

### 8. Price Button Component

Кнопка с ценой в нижней части карточки. Яркий акцент золотого/желтого цвета.

**Specifications:**
```css
/* ========================================== */
/* COMPONENT: Price Button                    */
/* FILE: cards-price-button.css               */
/* ========================================== */

/* Button Container */
--price-button-height: 36px;
--price-button-padding-h: 16px;
--price-button-padding-v: 10px;
--price-button-bg: #FFC043;              /* Yellow/gold (NEW COLOR!) */
--price-button-border-radius: 15px;
--price-button-border: none;

/* Price Text */
--price-number-font: 600 11px/1.40 'Archivo';
--price-number-color: #09101D;

--price-currency-font: 400 11px/1.40 'Archivo';
--price-currency-color: #09101D;

/* Price Layout */
--price-text-spacing: 8px;               /* Between number and currency */
--price-text-align: center;

/* Button States */
--price-button-hover-bg: #F5B639;        /* Slightly darker gold */
--price-button-active-bg: #EBAA2F;       /* Even darker gold */
```

**Visual Structure:**
```
┌──────────────────────┐
│   235   USD          │ ← Height: 36px
│  11/600  11/400      │   Padding: 16px H × 10px V
│  #09101D #09101D     │   Background: #FFC043
│                      │   BorderRadius: 15px
└──────────────────────┘
   Spacing: 8px between price and currency
```

**Price format variations:**
1. **Simple**: "235 USD"
2. **From price**: "From 199 USD"
3. **Per night**: "235 USD / night"
4. **Discounted**: ~~"300"~~ "235 USD"
5. **Range**: "235 - 450 USD"

### Complete Layout: Hotel Card

**Полная структура hotel card:**

```
┌───────────────────────────────────────────────────────────────┐
│  Container (375px, padding 16px H × 5px V)                    │
│  ┌──────────┬──────────────────────────────────────────────┐  │
│  │  Image   │  Content Container (#F4F6F9, padding 10px)  │  │
│  │  120×202 │  ┌────────────────────────────────────────┐  │  │
│  │  ┌──┐    │  │ Planta Luxury... [★][★][★][★][☆]    │  │  │ ← Title + Stars
│  │  │✓ │    │  ├────────────────────────────────────────┤  │  │
│  │  └──┘    │  │ Bali, Indonesia                        │  │  │ ← Location
│  │          │  ├────────────────────────────────────────┤  │  │
│  │  Hotel   │  │ [4.9] Excellent | 41 reviews           │  │  │ ← Rating
│  │  Image   │  ├────────────────────────────────────────┤  │  │
│  │          │  │ [Discount] [Secret Deal]               │  │  │ ← Tags
│  │          │  ├────────────────────────────────────────┤  │  │
│  │          │  │ 🍤 Sea food                            │  │  │
│  │          │  │ 📶 Free Wi-Fi                          │  │  │ ← Amenities
│  │          │  ├────────────────────────────────────────┤  │  │
│  │          │  │      [235 USD]                         │  │  │ ← Price Button
│  │          │  └────────────────────────────────────────┘  │  │
│  └──────────┴──────────────────────────────────────────────┘  │
└───────────────────────────────────────────────────────────────┘
     Spacing: 5px between image and content
```

**Компоненты в этом layout:**
1. Card Image (120×202px) with overlay badge
2. Card Content Container (#F4F6F9 background)
3. Title & Star Rating Row (11px title + 15px stars)
4. Location Text (10px)
5. Rating Badge & Text (badge + "Excellent | 41 reviews")
6. Tags Row (Discount, Secret Deal)
7. Amenities List (2 items with icons)
8. Price Button (36px height, #FFC043 background)

### Modular Components Matrix

Таблица показывает, какие компоненты используются в разных типах карточек:

| Component              | Hotel Card | Restaurant | Property | Product | Can Add More? |
|------------------------|------------|------------|----------|---------|---------------|
| Card Image             | ✅ (120px) | ✅ (120px) | ✅ (120px) | ✅ (80px) | ✅ Flexible |
| Overlay Badge          | ✅         | ✅         | ❌       | ❌      | ✅ Optional   |
| Title & Star Rating    | ✅         | ✅         | ✅       | ❌      | ✅ Contextual |
| Location               | ✅         | ✅         | ✅       | ❌      | ✅ Optional   |
| Rating Badge & Text    | ✅         | ✅         | ❌       | ⚠️ Review | ✅ Conditional|
| Tags Row               | ✅         | ✅         | ✅       | ✅      | ✅ Dynamic    |
| Amenities List         | ✅         | ✅         | ✅       | ❌      | ✅ Conditional|
| Price Button           | ✅         | ⚠️ Order  | ✅       | ✅      | ✅ Always     |

**Гибкость:**
- **Card Image**: можно менять размер (80px для product, 120px для hotel, 150px для property)
- **Overlay Badge**: опциональный, можно добавить/убрать
- **Tags Row**: количество динамическое (от 0 до бесконечности)
- **Amenities List**: показывать только для hotel/restaurant/property
- **Price Button**: всегда внизу, но текст может меняться ("Order", "Book", "Buy")

### Extensibility Guide

Практические примеры расширения компонентов для различных сценариев:

#### Example 1: Добавление больше amenities

Если у отеля больше удобств (например, 5 вместо 2), просто добавьте строки:

```html
<!-- ========================================== -->
<!-- USAGE EXAMPLE: Extended Amenities List     -->
<!-- ========================================== -->

<div class="amenities-list">
  <div class="amenity-item">
    <div class="amenity-icon">🍤</div>
    <span class="amenity-text">Sea food</span>
  </div>
  <div class="amenity-item">
    <div class="amenity-icon">📶</div>
    <span class="amenity-text">Free Wi-Fi</span>
  </div>
  <!-- NEW: Additional amenities -->
  <div class="amenity-item">
    <div class="amenity-icon">🏊</div>
    <span class="amenity-text">Pool</span>
  </div>
  <div class="amenity-item">
    <div class="amenity-icon">🏖️</div>
    <span class="amenity-text">Beach access</span>
  </div>
  <div class="amenity-item">
    <div class="amenity-icon">🧖</div>
    <span class="amenity-text">Spa</span>
  </div>
</div>
```

**Note:** Для длинных списков можно использовать двухколоночный layout:
```css
.amenities-list--two-columns {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 5px;
}
```

#### Example 2: Product Card (без amenities)

Если создаете product card, уберите amenities и измените размер изображения:

```html
<!-- ========================================== -->
<!-- USAGE EXAMPLE: Product Card Variant        -->
<!-- ========================================== -->

<div class="card-container">
  <!-- Smaller image for products -->
  <div class="card-image" style="width: 80px; height: 120px;">
    <img src="product.jpg" alt="Product">
    <!-- No overlay badge for products -->
  </div>

  <div class="card-content">
    <!-- Title only (no stars for products) -->
    <div class="card-title">Product Name</div>

    <!-- No location for products -->

    <!-- Optional: Review badge -->
    <div class="rating-row">
      <div class="rating-badge">4.5</div>
      <span class="rating-label">Very Good</span>
      <span class="rating-count">| 128 reviews</span>
    </div>

    <!-- Tags still work -->
    <div class="tags-row">
      <div class="tag tag--discount">Sale</div>
      <div class="tag tag--limited">Limited</div>
    </div>

    <!-- NO amenities for products -->

    <!-- Price button with different text -->
    <div class="price-button">
      <span class="price-number">49</span>
      <span class="price-currency">USD</span>
    </div>
  </div>
</div>
```

#### Example 3: Restaurant Card (с "Order" button)

Для ресторанов измените price button на "Order" или "Reserve":

```html
<!-- ========================================== -->
<!-- USAGE EXAMPLE: Restaurant Card Variant     -->
<!-- ========================================== -->

<div class="card-container">
  <div class="card-image">
    <img src="restaurant.jpg" alt="Restaurant">
    <div class="card-badge-overlay">
      <svg class="icon-verified"><!-- Verified icon --></svg>
    </div>
  </div>

  <div class="card-content">
    <!-- Title + Stars -->
    <div class="title-rating-row">
      <h3 class="card-title">Fine Dining Restaurant</h3>
      <div class="star-rating">★★★★★</div>
    </div>

    <!-- Location -->
    <div class="card-location">Downtown, New York</div>

    <!-- Rating -->
    <div class="rating-row">
      <div class="rating-badge">4.8</div>
      <span class="rating-label">Excellent</span>
      <span class="rating-count">| 234 reviews</span>
    </div>

    <!-- Tags -->
    <div class="tags-row">
      <div class="tag tag--featured">Featured</div>
      <div class="tag tag--new">New</div>
    </div>

    <!-- Amenities (cuisine types) -->
    <div class="amenities-list">
      <div class="amenity-item">
        <div class="amenity-icon">🍝</div>
        <span class="amenity-text">Italian</span>
      </div>
      <div class="amenity-item">
        <div class="amenity-icon">🍷</div>
        <span class="amenity-text">Wine bar</span>
      </div>
    </div>

    <!-- Action Button (not price) -->
    <button class="action-button action-button--order">
      <span class="action-text">Reserve table</span>
    </button>
  </div>
</div>
```

**CSS для action button:**
```css
/* ========================================== */
/* VARIANT: Action Button (non-price)         */
/* ========================================== */

.action-button--order {
  height: 36px;
  padding: 10px 16px;
  background: #4141E6;               /* Primary blue instead of gold */
  border-radius: 15px;
  border: none;
  cursor: pointer;
  transition: background-color 0.2s;
}

.action-button--order:hover {
  background: #3333D1;
}

.action-text {
  font: 600 11px/1.40 'Archivo';
  color: #FFFFFF;
}
```

#### Example 4: Vertical Card Layout

Если нужен вертикальный layout (изображение сверху, контент снизу):

```html
<!-- ========================================== -->
<!-- USAGE EXAMPLE: Vertical Card Layout        -->
<!-- ========================================== -->

<div class="card-container card-container--vertical">
  <!-- Image on top (full width) -->
  <div class="card-image card-image--vertical">
    <img src="hotel.jpg" alt="Hotel">
    <div class="card-badge-overlay">
      <svg class="icon-heart"><!-- Heart icon --></svg>
    </div>
  </div>

  <!-- Content below -->
  <div class="card-content card-content--vertical">
    <!-- Same content as horizontal -->
    <div class="title-rating-row">...</div>
    <div class="card-location">...</div>
    <!-- etc. -->
  </div>
</div>
```

**CSS для vertical layout:**
```css
/* ========================================== */
/* VARIANT: Vertical Card Layout              */
/* ========================================== */

.card-container--vertical {
  flex-direction: column;            /* Stack vertically instead of horizontal */
  padding: 0;                        /* Remove horizontal padding */
}

.card-image--vertical {
  width: 100%;                       /* Full width */
  height: 200px;                     /* Fixed height */
  border-radius: 15px 15px 0 0;      /* Round only top corners */
}

.card-content--vertical {
  border-radius: 0 0 15px 15px;      /* Round only bottom corners */
}
```

### CSS Implementation

Complete CSS для всех компонентов Cards & Listings:

```css
/* ============================================================================ */
/* FILE: cards-listings.css                                                     */
/* SECTION: Cards & Listings - Complete Stylesheet                             */
/* COMPONENTS: All card components with IDE AI navigation markers              */
/* ============================================================================ */

/* ========================================== */
/* COMPONENT: Screen Container                */
/* AI-TAG: card-screen-container              */
/* ========================================== */

.card-screen {
  width: 375px;
  padding: 30px 0;
  background: #FFFFFF;
  border-radius: 30px;
  overflow: hidden;
}

/* ========================================== */
/* COMPONENT: Card Container                  */
/* AI-TAG: card-container-horizontal          */
/* ========================================== */

.card-container {
  padding: 5px 16px;
  display: flex;
  gap: 5px;                          /* Spacing between image and content */
}

/* ========================================== */
/* COMPONENT: Card Image                      */
/* AI-TAG: card-image-with-overlay            */
/* ========================================== */

.card-image {
  position: relative;
  width: 120px;
  height: 202px;
  border-radius: 15px;
  overflow: hidden;
  flex-shrink: 0;
}

.card-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

/* Overlay Badge (top-left corner) */
.card-badge-overlay {
  position: absolute;
  top: 10px;
  left: 10px;
  width: 30px;
  height: 30px;
  padding: 8px;                      /* Icon 14×14px */
  background: rgba(17, 187, 141, 0.05);  /* 5% opacity green */
  border: 0.10px solid #FFFFFF;
  border-radius: 100px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.card-badge-overlay svg {
  width: 14px;
  height: 14px;
  color: #11BB8D;
}

/* ========================================== */
/* COMPONENT: Card Content Container          */
/* AI-TAG: card-content-container             */
/* ========================================== */

.card-content {
  flex: 1;
  padding: 10px;
  background: #F4F6F9;
  border-radius: 15px;
  display: flex;
  flex-direction: column;
  gap: 5px;
}

/* ========================================== */
/* COMPONENT: Title & Star Rating Row         */
/* AI-TAG: card-title-rating-row              */
/* ========================================== */

.title-rating-row {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  gap: 10px;
}

.card-title {
  max-width: 128px;
  font: 600 11px/1.40 'Archivo';
  color: #09101D;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}

.star-rating {
  display: flex;
  gap: 0px;
  flex-shrink: 0;
}

.star-rating__star {
  width: 15px;
  height: 15px;
  padding: 2px;
  border-radius: 100px;
}

.star-rating__star svg {
  width: 11px;
  height: 11px;
  color: #FFC043;                    /* Gold for filled stars */
}

.star-rating__star--empty svg {
  color: #E0E0E0;                    /* Gray for empty stars */
}

/* ========================================== */
/* COMPONENT: Location Text                   */
/* AI-TAG: card-location-text                 */
/* ========================================== */

.card-location {
  max-width: 198px;
  font: 400 10px/1.40 'Archivo';
  color: #09101D;
}

/* Optional: Location with icon */
.card-location--with-icon {
  display: flex;
  align-items: center;
  gap: 4px;
}

.location-icon {
  width: 12px;
  height: 12px;
  color: #747B84;
}

/* ========================================== */
/* COMPONENT: Rating Badge & Text             */
/* AI-TAG: card-rating-badge-text             */
/* ========================================== */

.rating-row {
  display: flex;
  align-items: center;
  gap: 5px;
}

.rating-badge {
  padding: 3px;
  background: #221874;               /* Dark purple (NEW COLOR) */
  border-radius: 5px;
  font: 600 10px/1.40 'Archivo';
  color: #FFFFFF;
  flex-shrink: 0;
}

.rating-label {
  font: 600 10px/1.40 'Archivo';
  color: #09101D;
}

.rating-count {
  font: 400 10px/1.40 'Archivo';
  color: #747B84;
}

/* Rating badge color variations */
.rating-badge--excellent {
  background: #221874;               /* Dark purple (9.0-10.0) */
}

.rating-badge--very-good {
  background: #4141E6;               /* Primary blue (8.0-8.9) */
}

.rating-badge--good {
  background: #11BB8D;               /* Success green (7.0-7.9) */
}

.rating-badge--average {
  background: #FFC043;               /* Yellow (6.0-6.9) */
}

.rating-badge--below-average {
  background: #E24949;               /* Error red (<6.0) */
}

/* ========================================== */
/* COMPONENT: Tags Row                        */
/* AI-TAG: card-tags-row                      */
/* ========================================== */

.tags-row {
  display: flex;
  flex-wrap: wrap;
  gap: 5px;
}

.tag {
  padding: 3px 5px;
  border-radius: 5px;
  font: 600 8px/1.40 'Archivo';
  color: #FFFFFF;
}

/* Tag type variations */
.tag--discount,
.tag--secret-deal {
  background: #11BB8D;               /* Success green */
}

.tag--new {
  background: #4141E6;               /* Primary blue */
}

.tag--featured {
  background: #FFC043;               /* Gold yellow */
}

.tag--limited {
  background: #E24949;               /* Error red */
}

/* ========================================== */
/* COMPONENT: Amenities List                  */
/* AI-TAG: card-amenities-list                */
/* ========================================== */

.amenities-list {
  display: flex;
  flex-direction: column;
  gap: 0px;                          /* Compact layout */
}

.amenity-item {
  display: flex;
  align-items: center;
  gap: 5px;
}

.amenity-icon {
  width: 21px;
  height: 20px;
  padding: 5px;
  border-radius: 100px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
}

.amenity-icon svg {
  width: 11px;
  height: 10px;
  color: #747B84;
}

.amenity-text {
  font: 400 10px/1.40 'Archivo';
  color: #747B84;
}

/* Two-column layout for long lists */
.amenities-list--two-columns {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 5px;
}

/* ========================================== */
/* COMPONENT: Price Button                    */
/* AI-TAG: card-price-button                  */
/* ========================================== */

.price-button {
  height: 36px;
  padding: 10px 16px;
  background: #FFC043;               /* Yellow/gold (NEW COLOR) */
  border-radius: 15px;
  border: none;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
  cursor: pointer;
  transition: background-color 0.2s;
  align-self: flex-start;
}

.price-button:hover {
  background: #F5B639;               /* Slightly darker gold */
}

.price-button:active {
  background: #EBAA2F;               /* Even darker gold */
}

.price-number {
  font: 600 11px/1.40 'Archivo';
  color: #09101D;
}

.price-currency {
  font: 400 11px/1.40 'Archivo';
  color: #09101D;
}

/* ========================================== */
/* VARIANT: Action Button (non-price)         */
/* AI-TAG: card-action-button                 */
/* ========================================== */

.action-button {
  height: 36px;
  padding: 10px 16px;
  border-radius: 15px;
  border: none;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: background-color 0.2s;
}

.action-button--order {
  background: #4141E6;               /* Primary blue */
}

.action-button--order:hover {
  background: #3333D1;
}

.action-button--reserve {
  background: #11BB8D;               /* Success green */
}

.action-button--reserve:hover {
  background: #0FA87D;
}

.action-text {
  font: 600 11px/1.40 'Archivo';
  color: #FFFFFF;
}

/* ========================================== */
/* VARIANT: Vertical Card Layout              */
/* AI-TAG: card-container-vertical            */
/* ========================================== */

.card-container--vertical {
  flex-direction: column;
  padding: 0;
  gap: 0;
}

.card-image--vertical {
  width: 100%;
  height: 200px;
  border-radius: 15px 15px 0 0;      /* Round only top corners */
}

.card-content--vertical {
  border-radius: 0 0 15px 15px;      /* Round only bottom corners */
}

/* ========================================== */
/* VARIANT: Product Card (smaller image)      */
/* AI-TAG: card-product-variant               */
/* ========================================== */

.card-image--product {
  width: 80px;
  height: 120px;
}

.card-content--product .card-title {
  max-width: 100%;                   /* Full width for product titles */
}

/* ========================================== */
/* Responsive & State Behaviors               */
/* ========================================== */

.card-container:hover .card-content {
  background: #E8ECF1;               /* Slightly darker gray on hover */
}

/* For grid layouts (multiple cards) */
.cards-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(343px, 1fr));
  gap: 16px;
  padding: 16px;
}

/* For list layouts (stacked cards) */
.cards-list {
  display: flex;
  flex-direction: column;
  gap: 10px;
}
```

### Usage Examples

<!-- ============================================================================ -->
<!-- USAGE EXAMPLE: Basic Hotel Card                                            -->
<!-- AI-TAG: example-hotel-card-basic                                            -->
<!-- ============================================================================ -->

#### Example 1: Basic Hotel Card

```html
<div class="card-screen">
  <div class="card-container">
    <!-- Card Image -->
    <div class="card-image">
      <img src="hotel-planta.jpg" alt="Planta Luxury Boutique Resort">
      <div class="card-badge-overlay">
        <svg class="icon-checkmark"><!-- Verified checkmark --></svg>
      </div>
    </div>

    <!-- Card Content -->
    <div class="card-content">
      <!-- Title + Star Rating -->
      <div class="title-rating-row">
        <h3 class="card-title">Planta Luxury Boutique Resort</h3>
        <div class="star-rating">
          <div class="star-rating__star">
            <svg><!-- Star filled --></svg>
          </div>
          <div class="star-rating__star">
            <svg><!-- Star filled --></svg>
          </div>
          <div class="star-rating__star">
            <svg><!-- Star filled --></svg>
          </div>
          <div class="star-rating__star">
            <svg><!-- Star filled --></svg>
          </div>
          <div class="star-rating__star star-rating__star--empty">
            <svg><!-- Star empty --></svg>
          </div>
        </div>
      </div>

      <!-- Location -->
      <div class="card-location">Bali, Indonesia</div>

      <!-- Rating Badge & Text -->
      <div class="rating-row">
        <div class="rating-badge rating-badge--excellent">4.9</div>
        <span class="rating-label">Excellent</span>
        <span class="rating-count">| 41 reviews</span>
      </div>

      <!-- Tags -->
      <div class="tags-row">
        <div class="tag tag--discount">Discount</div>
        <div class="tag tag--secret-deal">Secret Deal</div>
      </div>

      <!-- Amenities -->
      <div class="amenities-list">
        <div class="amenity-item">
          <div class="amenity-icon">
            <svg><!-- Seafood icon --></svg>
          </div>
          <span class="amenity-text">Sea food</span>
        </div>
        <div class="amenity-item">
          <div class="amenity-icon">
            <svg><!-- WiFi icon --></svg>
          </div>
          <span class="amenity-text">Free Wi-Fi</span>
        </div>
      </div>

      <!-- Price Button -->
      <div class="price-button">
        <span class="price-number">235</span>
        <span class="price-currency">USD</span>
      </div>
    </div>
  </div>
</div>
```

<!-- ============================================================================ -->
<!-- USAGE EXAMPLE: Restaurant Card with Reserve Button                         -->
<!-- AI-TAG: example-restaurant-card                                             -->
<!-- ============================================================================ -->

#### Example 2: Restaurant Card

```html
<div class="card-container">
  <div class="card-image">
    <img src="restaurant.jpg" alt="Fine Dining Restaurant">
    <div class="card-badge-overlay">
      <svg class="icon-star"><!-- Featured star --></svg>
    </div>
  </div>

  <div class="card-content">
    <div class="title-rating-row">
      <h3 class="card-title">Fine Dining Restaurant</h3>
      <div class="star-rating">
        <!-- 5 filled stars -->
      </div>
    </div>

    <div class="card-location--with-icon">
      <svg class="location-icon"><!-- Pin icon --></svg>
      <span>Downtown, New York</span>
    </div>

    <div class="rating-row">
      <div class="rating-badge rating-badge--excellent">4.8</div>
      <span class="rating-label">Excellent</span>
      <span class="rating-count">| 234 reviews</span>
    </div>

    <div class="tags-row">
      <div class="tag tag--featured">Featured</div>
      <div class="tag tag--new">New</div>
    </div>

    <div class="amenities-list">
      <div class="amenity-item">
        <div class="amenity-icon">
          <svg><!-- Italian food icon --></svg>
        </div>
        <span class="amenity-text">Italian</span>
      </div>
      <div class="amenity-item">
        <div class="amenity-icon">
          <svg><!-- Wine icon --></svg>
        </div>
        <span class="amenity-text">Wine bar</span>
      </div>
    </div>

    <!-- Action Button instead of Price -->
    <button class="action-button action-button--reserve">
      <span class="action-text">Reserve table</span>
    </button>
  </div>
</div>
```

<!-- ============================================================================ -->
<!-- USAGE EXAMPLE: Product Card (compact variant)                              -->
<!-- AI-TAG: example-product-card                                                -->
<!-- ============================================================================ -->

#### Example 3: Product Card (Compact)

```html
<div class="card-container">
  <div class="card-image card-image--product">
    <img src="product.jpg" alt="Product Name">
    <!-- No overlay badge for products -->
  </div>

  <div class="card-content card-content--product">
    <!-- Title only (no stars) -->
    <h3 class="card-title">Wireless Headphones</h3>

    <!-- Optional review badge -->
    <div class="rating-row">
      <div class="rating-badge rating-badge--very-good">4.5</div>
      <span class="rating-label">Very Good</span>
      <span class="rating-count">| 128 reviews</span>
    </div>

    <!-- Tags -->
    <div class="tags-row">
      <div class="tag tag--discount">Sale</div>
      <div class="tag tag--limited">Limited</div>
    </div>

    <!-- No amenities for products -->

    <!-- Price -->
    <div class="price-button">
      <span class="price-number">49</span>
      <span class="price-currency">USD</span>
    </div>
  </div>
</div>
```

<!-- ============================================================================ -->
<!-- USAGE EXAMPLE: Vertical Card Layout for Grid                               -->
<!-- AI-TAG: example-vertical-card-grid                                          -->
<!-- ============================================================================ -->

#### Example 4: Vertical Cards in Grid

```html
<div class="cards-grid">
  <!-- Card 1 -->
  <div class="card-container card-container--vertical">
    <div class="card-image card-image--vertical">
      <img src="hotel1.jpg" alt="Hotel 1">
      <div class="card-badge-overlay">
        <svg class="icon-heart"><!-- Saved --></svg>
      </div>
    </div>
    <div class="card-content card-content--vertical">
      <!-- Same content structure as horizontal -->
    </div>
  </div>

  <!-- Card 2 -->
  <div class="card-container card-container--vertical">
    <div class="card-image card-image--vertical">
      <img src="hotel2.jpg" alt="Hotel 2">
    </div>
    <div class="card-content card-content--vertical">
      <!-- ... -->
    </div>
  </div>

  <!-- Card 3 -->
  <div class="card-container card-container--vertical">
    <!-- ... -->
  </div>
</div>
```

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
- **Добавлена новая секция "Cards & Listings"** - модульная система карточек для hotels, restaurants, properties, products с IDE AI navigation markers:
  - **Принцип модульности**: каждая карточка состоит из 8 переиспользуемых блоков
  - **IDE AI Navigation Markers**: добавлены комментарии <!-- AI-TAG: --> для быстрой навигации
  - **Container Specifications**:
    - Screen: 375px width, borderRadius 30px, padding 30px V
    - Card layout: horizontal (image 120×202px + content), spacing 5px
  - **Typography System** (8 text styles):
    - Card Title: 11px / 600 Archivo, max-width 128px
    - Location: 10px / 400 Archivo, max-width 198px
    - Rating Number: 10px / 600 white на badge
    - Rating Label: 10px / 600 #09101D
    - Rating Count: 10px / 400 #747B84
    - Tag: 8px / 600 white
    - Amenity: 10px / 400 #747B84
    - Price: 11px / 600 для number, 11px / 400 для currency
  - **8 Modular Components** (каждый с AI-TAG):
    - **Card Image** (AI-TAG: card-image-with-overlay): 120×202px, borderRadius 15px, aspect ratio 1:1.68
    - **Overlay Badge** (AI-TAG: card-badge-overlay): 30×30px circle, top-left 10×10px, rgba(17,187,141,0.05) bg, 0.10px white border
    - **Content Container** (AI-TAG: card-content-container): padding 10px, bg #F4F6F9, borderRadius 15px, spacing 5px
    - **Title & Star Rating Row** (AI-TAG: card-title-rating-row): 11px title + 15px stars (gold #FFC043), spacing 10px
    - **Location** (AI-TAG: card-location-text): 10px/400, optional with 12px icon
    - **Rating Badge & Text** (AI-TAG: card-rating-badge-text): badge #221874 (новый!), "Excellent | 41 reviews"
    - **Tags Row** (AI-TAG: card-tags-row): 8px/600, 5 типов (Discount, Secret Deal, New, Featured, Limited)
    - **Amenities List** (AI-TAG: card-amenities-list): 21×20px icons, 10px/400 text, compact layout (gap 0px)
    - **Price Button** (AI-TAG: card-price-button): 36px height, bg #FFC043 (новый!), hover/active states
  - **Complete Layout: Hotel Card** с ASCII diagram и breakdown всех 8 компонентов
  - **Modular Components Matrix**: таблица совместимости для 4 типов cards (Hotel, Restaurant, Property, Product)
  - **Extensibility Guide** с 4 практическими примерами:
    - Добавление больше amenities (2-column grid layout)
    - Product Card variant (80×120px image, без amenities)
    - Restaurant Card (action button "Reserve" вместо price)
    - Vertical Card Layout (image сверху, content снизу)
  - **Новые цвета в палитру**:
    - #221874 - rating badge (dark purple для excellent ratings)
    - #FFC043 - price button (yellow/gold, уже был в использовании)
    - rgba(17,187,141,0.05) - badge overlay (5% opacity green)
  - **Badge Color Variations** (для будущего):
    - Excellent (9.0-10.0): #221874 dark purple
    - Very Good (8.0-8.9): #4141E6 primary blue
    - Good (7.0-7.9): #11BB8D success green
    - Average (6.0-6.9): #FFC043 yellow
    - Below Average (<6.0): #E24949 error red
  - **Complete CSS Implementation** (400+ lines) с IDE AI-TAG markers:
    - AI-TAG: card-screen-container, card-container-horizontal, card-image-with-overlay
    - AI-TAG: card-content-container, card-title-rating-row, card-location-text
    - AI-TAG: card-rating-badge-text, card-tags-row, card-amenities-list
    - AI-TAG: card-price-button, card-action-button, card-container-vertical
    - AI-TAG: card-product-variant
  - **4 Usage Examples** с AI-TAG markers:
    - AI-TAG: example-hotel-card-basic (полная разметка)
    - AI-TAG: example-restaurant-card (с Reserve button)
    - AI-TAG: example-product-card (compact variant)
    - AI-TAG: example-vertical-card-grid (grid layout)
  - **Section Navigation Markers**:
    - <!-- SECTION: Cards & Listings -->
    - <!-- FILE REFERENCE: design-system.md#cards--listings -->
    - <!-- USAGE: Hotel cards, property listings, travel bookings, featured content -->
    - <!-- COMPONENTS: hotel-card, rating-badge, amenity-list, price-button -->
    - <!-- AI NAVIGATION: Search for "COMPONENT:" tags to find specific components -->

#### v5.10.0 (2025-11-19)
- **Добавлена новая секция "Shopping & Orders"** - модульная система компонентов для e-commerce приложений:
  - **Принцип модульности**: каждый экран покупок состоит из переиспользуемых блоков
  - **Container Specifications**:
    - Screen: 375px width, borderRadius 30px, padding 30px V
    - Content padding: 16px H (standard), 32px H (action buttons)
  - **Typography System**:
    - Section Header Title: 24px / 700 Archivo, color #09101D, center
    - Section Header Subtitle: 14px / 400 Archivo, color #747B84 (новый), max-width 343px
    - Product Title: 15px / 600 Archivo
    - Product Price: 13px / 600 Archivo
    - Product Meta: 14px / 400 Archivo, color #414249 (новый)
    - Action Label: 13px / 600 Archivo
    - Stepper Number: 12px / 500 Archivo, color #2A2B2F (новый)
  - **5 Modular Components**:
    - **Section Header**: centered title + subtitle, padding 16px H × 10px V, spacing 5px
    - **Icon Action Buttons**:
      - Container: padding 32px H, 10px T, 20px B, distribution space-between
      - Active state: 44px icon, padding 12px (icon 20×20), bg #4141E6
      - Inactive state: 44px icon, padding 14px (icon 16×16 меньше!), bg #F4F6F9
      - Label: 13px/600, spacing 5px from icon
    - **Product List Item**:
      - Image: 40px × 40px, borderRadius 15px, bg #F4F6F9
      - Title: 15px/600, max-width 160px
      - Price + Meta: "$0.75 ・ 280 g" (separator " ・ " middle dot)
      - Layout: 16px spacer + image + 10px + info (flex) + 16px spacer + stepper + 16px
    - **Quantity Stepper** (новый компонент):
      - Container: padding 2px, borderRadius 20px, bg #F4F6F9, spacing 15px
      - Buttons: 24px × 24px circles, padding 4px (icon 16×16), bg #4141E6
      - Number: 12px/500, color #2A2B2F
    - **List Dividers**: 1px height, color #EAEEEF2 (новый), padding 16px H × 10px V
  - **Complete Layout: Order Confirmation Screen** с ASCII diagram и breakdown компонентов
  - **Modular Components Matrix**: совместимость компонентов в различных экранах (Order Confirm, Shopping Cart, Order History)
  - **Extensibility Guide** с 4 практическими примерами:
    - Добавление 4-й action button (grid layout)
    - Добавление Total Price Section для корзины
    - Убрать Quantity Stepper для read-only Order History
    - Динамическое добавление товаров из backend
  - **Новые цвета в палитру**:
    - #747B84 - subtitle gray (для subtitles и secondary text)
    - #414249 - meta gray (для quantity/weight информации)
    - #2A2B2F - stepper text (для чисел в stepper)
    - #EAEEEF2 - divider line (для разделительных линий)
  - **Complete CSS Implementation** (450+ lines):
    - Shopping Screen Container
    - Section Header
    - Action Buttons Row (active/inactive states, hover)
    - Product List Item (с spacers, image, info, quantity)
    - Quantity Stepper (с hover/active states)
    - List Divider
    - Responsive Behaviors (4-button grid, scrollable lists)
  - **3 Usage Examples**:
    - Basic Order Confirmation Screen (полная разметка)
    - Shopping Cart with Total (с Total Section и Checkout Button)
    - Order History Read-only (без steppers, static quantity)

#### v5.9.0 (2025-11-19)
- **Добавлена новая секция "Mobile Screens & Layouts"** - система модульных экранов для onboarding и других flow:
  - **Принцип модульности**: каждый экран состоит из переиспользуемых блоков, которые можно комбинировать и расширять
  - **Screen Container Specifications**:
    - Container: 375px width (standard mobile), border-radius 30px
    - Backgrounds: white (#FFFFFF) для welcome screens, light gray (#FAFAFB) для onboarding
    - Padding: 50px для welcome, 35px/30px для onboarding с navigation
  - **Typography System**:
    - Large Title: 32px / 700 Archivo для hero screens
    - Medium Title: 24px / 700 Archivo для content screens
    - Subtitle: 16px / 400 Archivo с letter-spacing 1px
    - Subtitle Dimmed: rgba(9,16,29,0.40) для secondary text
    - Colored Accent Text: #4141E6 для выделения ключевых слов
  - **Modular Screen Elements** (4 переиспользуемых компонента):
    - **Home Indicator**: 134px × 5px, pill shape, black color (iPhone-style)
    - **Progress Bar**: 5 segments, 3px height, 10px spacing, active #4141E6, inactive rgba(11,36,251,0.20)
    - **Back Button**: 44px height, 24px icon, rgba(9,16,29,0.20) background
    - **Button Groups**:
      - Dual Buttons (row): 52px height, 10px spacing, side-by-side layout
      - Stacked Buttons: 44px height, 10px spacing, vertical layout
  - **3 Complete Screen Layouts** с ASCII diagrams:
    - Welcome Screen (white bg, large title 32px, dual buttons 52px)
    - Onboarding with Accent (light gray bg, colored text accents, stacked buttons 44px)
    - Progress Screen (back button, 5-segment progress bar, medium title 24px)
  - **Modular Components Matrix**: таблица совместимости компонентов (Large Title, Dual Buttons, Progress Bar и т.д.)
  - **Extensibility Guide** с 3 практическими примерами:
    - Добавление 3-й кнопки в стек (когда по дизайну 2, но нужно 3)
    - Расширение progress bar с 5 до 7 сегментов
    - Добавление иллюстрации между элементами
  - **Complete CSS Implementation** с variables, 3 screen layouts, button variants
  - **Usage Examples** для всех 3 screen layouts с модификациями

#### v5.8.0 (2025-11-19)
- **Добавлена новая секция "Snackbars & Toasts"** - система уведомлений для мобильного приложения:
  - **Container Specifications**:
    - Container: 375px width, padding 16px
    - Border radius: 15px для всех элементов
    - Background: rgba(5, 148, 79, 0.90) для success snackbar (#05944F с 90% opacity)
    - Text color: white (#FFFFFF)
  - **Typography**:
    - Message text: 14px / 600 Archivo, white
    - Action button text: 13px / 600 Archivo, white
    - Line height: 1.40 для всех текстов
  - **Snackbar Elements**:
    - Icon Element: 24px × 24px, padding 16px, для status icons
    - Avatar Element:
      - Container: 56px × 56px
      - Image: 48px × 48px с offset 4px (создает white border эффект)
      - Border radius: 40px (highly rounded)
      - Background: white (#FFFFFF)
    - Close Icon: 20px × 20px, height 36px/44px, padding 16px/10px
    - Action Button: height 36px/44px, text "Action" 13px/600, padding 16px/10px
  - **8 Layout Variants**:
    1. Simple Message (311px text width)
    2. Icon + Message (271px text width)
    3. Icon + Message + Close (235px text width)
    4. Avatar + Message (239px text width)
    5. Avatar + Message + Close (203px text width)
    6. Message + Action (267px text width)
    7. Icon + Message + Action (223px text width)
    8. Avatar + Message + Action (159px/191px text width для 3/2 lines)
  - **Accessibility Guidelines**:
    - ARIA roles: `role="status"` или `role="alert"`
    - ARIA live regions: `aria-live="polite"` или `aria-live="assertive"`
    - `aria-atomic="true"` для полного чтения сообщения
    - `aria-label` для close кнопки
    - Icons с `aria-hidden="true"`
  - **Best Practices**:
    - Duration & Timing: 3-4s для info, 7-10s для action, manual для errors
    - Positioning: bottom center для mobile, top center для desktop
    - Content: 1-3 строки максимум, clear actionable language
    - Visual Hierarchy: avatar для user notifications, icon для status
    - Color Coding: success/error/warning/info варианты
  - **Complete CSS Implementation** с variables, layout variants, hover/active states
  - **Usage Examples** для всех 8 layout вариантов

#### v5.7.0 (2025-11-19)
- **Расширена секция "Input Fields"** с Advanced Variants, State Variations и Complex Field Types:
  - **Advanced Input Field Variants**:
    - Container Padding Variation: 10px vertical (альтернатива 5px)
    - Field Heights: 44px (small/compact) и 46px (medium/standard)
    - Visible Borders: 2px width, color #F4F6F9 (subtle depth)
    - Field Padding: асимметричный 4px/20px/15px/4px (top/left/right/bottom)
    - Typography Variations:
      - Small Text: 12px/400 для compact fields и secondary info
      - Medium Text: 14px/600 для standard fields
      - Special Text Color: #23262B (альтернатива primary black)
    - Element Spacing Tight: 5px между элементами (альтернатива 8px)
  - **Field State Variations**:
    - Success State: helper 12px/400 #11BB8D, emoji 14px, padding 10px horizontal
    - Error State: helper 12px/400 #E24949, asymmetric padding 10px left
    - Two-Line Field: label 12px/400 #747B84 + value 14px/600 #09101D
  - **Complex Field Types**:
    - Field with Top Label and Balance Info:
      - Label: 14px/600, Balance: 10px/600, USD price: 10px/600
      - USD colors: #0B24FB (blue) или #4141E6 (purple)
      - Spacing: 10px gap между balance элементами
    - Field with Avatar:
      - Avatar size: 30px × 30px
      - Variants: circular (borderRadius 50px) и rounded square (borderRadius 10px)
      - Spacing: 10px gap to text
      - Use cases: user selection, contact picker, account switcher, service selection
    - Field with Multiple Icons:
      - Icon sizes: 24px container с padding 2px/4px/6px
      - Inner icon sizes: 14.40px и 19.20px
      - Icon spacing: 5px gap между иконками справа
    - Field with Left and Right Content:
      - Currency label: 13px/600 #09101D
      - Complex layouts: search icon + text + clear icon
      - Avatar + two-line text + numeric value
    - Field with Right-Aligned Text Column:
      - Top text: 14px/600 #09101D
      - Bottom text: 12px/400 #747B84
      - Text alignment: right
  - **Advanced CSS Implementation**:
    - Extended CSS variables для всех новых вариантов
    - Utility classes для bordered, small-text, two-line variants
    - Success/Error state styles с emoji support
    - Avatar variants (circle/rounded)
    - Label with Balance row components
    - Currency field layouts
- **Расширена цветовая палитра**:
  - `--color-text-primary-alt: #23262B` - альтернативный основной цвет текста (чуть светлее #09101D)

#### v5.6.0 (2025-11-19)
- **Добавлена новая секция "Input Fields"** - система полей ввода для мобильного приложения:
  - **Container Specifications**:
    - Container: 375px width, padding 16px horizontal / 5px vertical
    - Spacing: 8px между элементами (title, field, helper message)
    - Layout: Vertical Column с consistent gap
  - **Input Title** - заголовок поля:
    - Font: 14px / 600 Archivo
    - Color: #09101D (Primary Text)
    - Line Height: 1.40
  - **Input Field** - основное поле ввода:
    - Container: 36px height, borderRadius 15px, background #F4F6F9
    - Padding: 16px left, 20px right (10px right при наличии иконки)
    - Placeholder Text: 14px / 400 Archivo, color #747B84
    - Entered Text: 14px / 600 Archivo, color #09101D (bold when filled!)
  - **Icons in Input Fields**:
    - Left Icon: 20px × 20px, borderRadius 100px, padding 2px, spacing 10px to text
    - Right Trailing Icon(s): 20px × 20px, borderRadius 100px, 10px spacing between multiple icons
    - Flag Icon: 22px × 16px, borderRadius 2px (для country/phone selection)
  - **Helper Message** - вспомогательное сообщение:
    - Font: 14px / 400 Archivo
    - Color: #747B84 (Tertiary Text)
  - **Layout Variations**:
    - Single Full-Width Input - стандартное одиночное поле
    - Dual Input Layout - два поля рядом (например, флаг + телефон)
    - Spacing variations: 10px, 15px, 20px gap
  - **Input States**:
    - Empty State: placeholder #747B84, weight 400
    - Filled State: text #09101D, weight 600 (bold!)
  - **CSS переменные** для всех компонентов input fields
  - **Accessibility** рекомендации: `<label>` с `for`, `aria-describedby` для helper text, `aria-invalid` для ошибок
  - **Best Practices**: Typography Consistency, Spacing, Icon Usage, Color Semantics, Responsive Behavior
  - **Примеры CSS кода** и HTML разметки для всех вариантов

#### v5.5.0 (2025-11-19)
- **Добавлена новая секция "Progress Indicators & Steppers"** - система индикаторов прогресса:
  - **Step Indicators** - точечные индикаторы для многошаговых процессов:
    - Container: 18px × 18px, Dot: 14px × 14px
    - 5 состояний: Active (#4141E6), Completed (с белой обводкой), Inactive (#EAEEF2), Error (#E24949), With Icon
    - Label: 10px/600, spacing 5px below dot
  - **Circular Progress Indicators** - круговые прогресс-бары:
    - 4 размера: 64px (5px border), 48px (4px border), 36px (3px border), 24px (2px border)
    - Background ring: #F4F6F9, Progress ring: #4141E6
    - Текст внутри: 13px, 11px, 10px, 7px соответственно
    - Примеры значений: время ("1:35") или проценты ("15%", "48%", "72%", "85%")
  - **Linear Progress Bars** - линейные прогресс-бары:
    - Vertical: 60px × 2px, borderRadius 10px, spacing 58px
    - Horizontal: 4px height, Expanded width, borderRadius 10px
    - 3 состояния: Active (#0B24FB solid), Partial (30% opacity), Inactive (10% opacity)
    - Conditional borderRadius на начале/конце
  - **Stepper Progress** - пошаговый индикатор с линиями:
    - Container: 375px width, padding 32px/5px
    - Dot: 14px × 14px, Connector line: 4px height
    - Spacing: 3px between elements
    - 3 состояния: Completed (#4141E6), Active (с белой обводкой), Inactive (#F4F6F9)
    - Layout: [Dot] —Line— [Dot] pattern
  - **CSS переменные** для всех компонентов
  - **Accessibility** рекомендации: ARIA attributes, live regions
  - **Best Practices** для каждого типа индикатора
  - **Примеры CSS кода** для всех состояний
- **Расширена цветовая палитра**:
  - `--color-primary-alt: #0B24FB` - альтернативный синий для прогресс-баров

#### v5.4.0 (2025-11-19)
- **Добавлена новая секция "Date & Time Pickers"** - система компонентов для выбора даты и времени:
  - **Time Slots Grid** - сетка выбора времени с интервалом 30 минут:
    - Container: 375px × auto, padding 16px/10px
    - Slot Button: 40px height, borderRadius 15px, padding 10px
    - 3 состояния: Selected (#09101D bg), Available (#F4F6F9 bg), Disabled (transparent, strikethrough)
    - Layout: 5 columns × 5 rows = 25 временных слотов
    - Диапазон: 10:00 - 22:00
  - **Horizontal Date Picker** - горизонтальный выбор дат:
    - Date Card: 50px width, padding 14px/8px, borderRadius 15px
    - День недели: 10px/600, Дата: 14px/600
    - Gap между элементами: 2px
    - 4 состояния: Selected, Available Weekday, Available Weekend (#E24949 красный), Disabled
  - **Monthly Calendar** - полноценный месячный календарь:
    - Container: 375px × auto, padding 16px/10px
    - Month/Year Header: 40px height, navigation arrows 24px
    - Day Names Row: 40px height, 7 columns
    - Calendar Grid: 7 columns × 5-6 rows
    - Cell: 40px height, padding 5px or 10px
    - 7 состояний ячеек: Selected, Range, With Event, With Dot, Other Month, Disabled, Available
    - Date Range с conditional borderRadius (start/middle/end)
    - Event indicators: 7px font, colors #11BB8D (active) / #747B84 (past)
    - Dot indicator: "•" character, 13px font
  - **CSS переменные** для всех компонентов
  - **Accessibility** рекомендации: ARIA labels, keyboard navigation, screen readers
  - **Best Practices** для каждого компонента
  - **Примеры CSS кода** для всех состояний
- **Расширена цветовая палитра**:
  - `--color-error: #E24949` - красный для выходных дней и ошибок

#### v5.3.0 (2025-11-19)
- **Добавлена новая секция "Charts & Graphs"** - система визуализации данных для мобильных экранов:
  - Bar Chart (Hourly View) для отображения почасовых метрик
  - 60 вертикальных баров с высотами от 38px до 155px
  - Два варианта padding: компактный (10px vertical) и расширенный (40px top)
  - Два варианта border-radius: 1px (компактный) и 4px (комфортный)
  - Цвет баров: #D9DDE2
  - Gap между барами: 1px
  - Container: 375px width (мобильный экран)
  - Alignment: по нижнему краю (flex-end)
  - Рекомендации по интерактивности, адаптивности и accessibility
  - Примеры CSS кода для обоих вариантов
- **Добавлены CSS переменные для графиков**:
  - `--chart-bar-color-primary: #D9DDE2`
  - `--chart-bar-gap: 1px`
  - `--chart-bar-radius-compact: 1px`
  - `--chart-bar-radius-comfortable: 4px`
  - `--chart-container-width-mobile: 375px`
  - Padding переменные для компактного и расширенного режимов

#### v5.2.0 (2025-11-19)
- **Добавлены градиенты** из TinyCards компонентов:
  - Purple-Blue (#7F7FD5 → #86A8E7)
  - Light-Blue (#E0EAFC → #CFDEF3)
  - Dark-Blue (#141E30 → #243B55)
- **Расширена цветовая палитра**:
  - Border accent (#7B61FF)
  - Card background (#F4F6F9)
  - Icon button background (#EAEEF2)
  - White transparent border (rgba(255, 255, 255, 0.07))
- **Добавлена новая секция "Tiny Cards"** (компактные карточки для desktop/tablet):
  - 9 типов карточек: Product (gradient & light), Balance, User Profile, Product Dark, Growth Indicator, Icon Label, User Info, Avatar with Status
  - Размеры: 160px × 60px, 80px, 120px, 160px
  - Полная спецификация всех параметров: padding, borders, typography, spacing
  - Container wrapper с фиолетовой рамкой

#### v5.1.0 (2025-11-19)
- **Обновлена цветовая палитра** с реальными данными из Flutter приложения
- **Дополнена типографика** с фактическими размерами и весами шрифтов
- **Обновлены spacing и border radius** с точными значениями из кода
- **Добавлены мобильные компоненты**:
  - Bottom Sheet с handle индикатором
  - List Items с иконками
  - Primary и Secondary кнопки
  - Badges & Tags
  - Radio Buttons / Selection
  - Dividers (стандартные и акцентные)
  - Headers & Titles
  - Rating Component
  - Screen Dimensions
  - Icon Sizes
- **Обновлены shadows** с реальными значениями из приложения
- **Добавлены opacity значения** (10%, 25%, 40%)

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
