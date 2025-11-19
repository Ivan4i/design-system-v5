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
--color-text-secondary: #414249;       /* Вторичный текст */
--color-text-tertiary: #747B84;        /* Третичный текст (подписи) */
```

### Accent Colors

```css
/* Акцентные цвета */
--color-primary: #4141E6;              /* Primary синий/фиолетовый */
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

**Текущая версия**: v5.4.0

### Changelog

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
