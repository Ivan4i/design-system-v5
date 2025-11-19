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
```

### Text Colors

```css
/* Текст из Flutter кода */
--color-text-primary: #09101D;     /* Основной темный текст из Flutter */
--color-text-secondary: #747B84;   /* Вторичный текст из Flutter (метаданные, время) */
--color-text-tertiary: #414249;    /* Третичный текст (username, labels) */
--color-text-muted: #50555C;       /* Приглушенный текст (цены, данные) */
--color-text-disabled: #D9DDE2;    /* Disabled text из Flutter */
```

### Accent Colors

```css
/* Акцентные цвета */
--color-primary: #4141E6;          /* Основной primary цвет из Flutter */
--color-primary-border: #0B24FB;   /* Primary border variant из Flutter */
--color-accent-blue: #1D4ED8;      /* blue-700 */
--color-accent-purple: #7B61FF;    /* Фиолетовый из Flutter кода */
--color-success: #11BB8D;          /* Зеленый для success badges из Flutter */
```

### Background Colors

```css
/* Фоны для компонентов */
--color-bg-light: #F4F6F9;         /* Светлый фон из Flutter (основной для cards) */
--color-bg-dark: #18202F;          /* Темный scaffold background из Flutter */
--color-bg-overlay: rgba(0, 0, 0, 0.10);  /* Overlay для изображений */
--color-bg-card-light: #D9DDE2;    /* Светлая карточка (avatar placeholder) */
--color-bg-card-dark: #09101D;     /* Темная карточка (dark buttons, dark elements) */
```

### Shadow Colors

```css
/* Тени */
--shadow-light: rgba(240, 241, 242, 1.00);
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
--font-size-10: 0.625rem;     /* 10px */
--font-size-11: 0.6875rem;    /* 11px */
--font-size-12: 0.75rem;      /* 12px */
--font-size-13: 0.8125rem;    /* 13px */
--font-size-14: 0.875rem;     /* 14px */
--font-size-15: 0.9375rem;    /* 15px */
--font-size-16: 1rem;         /* 16px */
--font-size-18: 1.125rem;     /* 18px */
--font-size-22: 1.375rem;     /* 22px - для номеров карт */
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
--letter-spacing-1: 0.0625rem;    /* 1px */
--letter-spacing-2: 0.125rem;     /* 2px */
--letter-spacing-2-59: 0.162rem;  /* 2.59px - для номеров карт */
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
--space-0: 0;
--space-1: 0.25rem;   /* 4px */
--space-1-25: 0.3125rem; /* 5px - из Flutter spacing: 5 */
--space-2: 0.5rem;    /* 8px */
--space-3: 0.75rem;   /* 12px */
--space-4: 1rem;      /* 16px */
--space-5: 1.25rem;   /* 20px */
--space-6: 1.5rem;    /* 24px */
--space-7: 1.75rem;   /* 28px - из Flutter spacing: 7 */
--space-8: 2rem;      /* 32px */
--space-10: 2.5rem;   /* 40px - из Flutter spacing: 10 */
--space-12: 3rem;     /* 48px */
--space-16: 4rem;     /* 64px */
--space-20: 5rem;     /* 80px - из Flutter spacing: 20 */
--space-24: 6rem;     /* 96px */
--space-70: 4.375rem; /* 70px - из Flutter spacing: 70 (для Row spacing) */
```

### Gradient Colors

```css
/* Градиенты из Flutter кода */
--gradient-live-badge: linear-gradient(90deg, #833AB4 0%, #FD1D1D 50%, #FCB045 100%);
--gradient-image-overlay: linear-gradient(180deg, rgba(196, 196, 196, 0) 0%, rgba(29, 29, 29, 0.50) 100%);
```

### Border Radius

```css
--radius-none: 0;
--radius-sm: 0.25rem;     /* 4px */
--radius-base: 0.5rem;    /* 8px */
--radius-md: 0.75rem;     /* 12px - из Flutter кода (альтернативный для buttons) */
--radius-lg: 0.9375rem;   /* 15px - из Flutter кода (основной для buttons/карточек) */
--radius-xl: 1rem;        /* 16px */
--radius-2xl: 1.25rem;    /* 20px */
--radius-3xl: 1.5rem;     /* 24px */
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

### 2. Buttons (Flutter Mobile)

#### Button Sizes

- **Small (36px)**: Height: 36px, Padding: 10px 16px, Font: 13px
- **Medium (40px)**: Height: 40px, Padding: 10px 20px, Font: 16px
- **Large (48px)**: Height: 48px, Padding: 12px 24px, Font: 18px

#### Button Widths

- **Full Width (Large)**: width: 100% (double.infinity)
- **Medium**: width: 165px
- **Auto (Small)**: width: auto (wrap content)

#### Button Typography

- **Font Family**: Archivo
- **Font Size**: 13px (small buttons), 16px (medium), 18px (large)
- **Font Weight**: 600 (Semibold)
- **Line Height**: 1.40

#### Button Border Radius

- **Primary**: 15px (radius-lg)
- **Alternative**: 12px (radius-md)

#### Filled Button (Primary)

- **Background**: #4141E6 (color-primary)
- **Text Color**: #FFFFFF (white)
- **Border**: none
- **Icon Size**: 16px
- **Icon Spacing**: 8px (between icon and text)
- **States**:
  - Default: Background: #4141E6, Text: white
  - Hover: Background: lighter variant of #4141E6
  - Active: Background: darker variant of #4141E6
  - Disabled: Background: #F4F6F9, Text: #D9DDE2

#### Filled Button (Secondary)

- **Background**: #F4F6F9 (color-bg-light)
- **Text Color**: #09101D (color-text-primary)
- **Border**: none
- **States**:
  - Default: Background: #F4F6F9, Text: #09101D
  - Hover: Background: lighter/darker variant
  - Disabled: Background: #F4F6F9, Text: #D9DDE2

#### Outlined Button

- **Background**: transparent
- **Border**: 1px solid #4141E6 или #0B24FB (color-primary-border)
- **Text Color**: #4141E6 (color-primary)
- **Icon Size**: 16px
- **States**:
  - Default: Border: #4141E6 или #0B24FB, Text: #4141E6
  - Hover: Background: rgba(65, 65, 230, 0.05)
  - Active: Background: rgba(65, 65, 230, 0.1)

#### Ghost/Text Button

- **Background**: transparent или minimal background
- **Border**: none
- **Text Color**: #09101D (color-text-primary)
- **Border Radius**: 12px или 15px
- **States**:
  - Default: Background: transparent, Text: #09101D
  - Hover: Background: #F4F6F9

#### Icon Button (Icon Only)

- **Size**: 40px × 40px (icon button container)
- **Icon Size**: 16px (internal icon)
- **Padding**: 12px
- **Border Radius**: 15px (radius-lg)
- **Variants**:
  - Filled Primary: Background: #4141E6, Icon: white
  - Filled Secondary: Background: #F4F6F9, Icon: #09101D
  - Outlined: Border: 1px solid #4141E6, Icon: #4141E6, Background: transparent
  - Disabled: Background: #F4F6F9, Icon: #D9DDE2

#### Button Layout Patterns

- **With Leading Icon**: Icon (16px) + spacing (8px) + Text
- **With Trailing Icon**: Text + spacing (8px) + Icon (16px)
- **With Both Icons**: Icon (16px) + spacing (8px) + Text + spacing (8px) + Icon (16px)
- **Icon Only**: Icon (16px) centered in 40px container

#### Button Spacing in Containers

- **Container Width (Mobile)**: 375px
- **Container Horizontal Padding**: 16px
- **Effective Button Width**: 343px (for full-width buttons)
- **Spacing Between Button Groups**: 10px vertical
- **Spacing Inside Button Row**: 70px horizontal (for spaceBetween layout)

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

### 4. Badges & Tags (Flutter Mobile)

#### Live Badge (Instagram-style)

- **Size**: 28px width × 14px height
- **Padding**: 4px horizontal, 2px vertical
- **Border Radius**: 12px
- **Border**: 1px solid white
- **Background**: Linear gradient (#833AB4 → #FD1D1D → #FCB045)
- **Font**: Archivo, 10px, weight 600, line-height 1.40
- **Text Color**: white
- **Text**: "Live"
- **Использование**: Overlay на аватаре (позиция: bottom-right)

#### New Badge (Success)

- **Size**: auto width × 24px height
- **Padding**: 6px horizontal
- **Border Radius**: 11px
- **Background**: #11BB8D (color-success)
- **Font**: Archivo, 11px, weight 600, line-height 1.40
- **Text Color**: white
- **Text**: "New" или "new"
- **Использование**: Overlay на изображениях (позиция: top-left с padding 10px)

#### Badge Common Properties

- **Font Family**: Archivo
- **Font Weight**: 600 (Semibold)
- **Line Height**: 1.40
- **Text Transform**: none (сохраняет оригинальный регистр)

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

### 9. Avatars (Flutter Mobile)

#### Sizes

- **XS**: 24px × 24px
- **Small**: 32px × 32px
- **Medium**: 40px × 40px (основной размер из Flutter)
- **Medium with Container**: 48px × 48px container (40px avatar + 4px offset)
- **Large**: 48px × 48px
- **XL**: 64px × 64px
- **2XL**: 80px × 80px (из User Profile Card)
- **3XL**: 96px × 96px

#### Styles

- **Border Radius**: radius-full (40px для 40px avatar, 50px для 40px в container)
- **Border**: 2px solid white (для группировки)
- **Placeholder**: Background: #D9DDE2 (color-bg-card-light), Icon/Initials: color-gray-600
- **Image Fit**: cover

#### Avatar with Live Badge

- **Container**: 48px × 48px
- **Avatar**: 40px × 40px (позиция: left 4px, top 4px)
- **Live Badge**: 28px × 14px (позиция: bottom-right of container)
- **Badge Offset**: bottom 0, right 0
- **Usage**: Для live streaming, active users

#### Avatar Variants

- **Circle Avatar**: border-radius: 40px (для 40px avatar) или 50px (для контейнера)
- **Rounded Square**: border-radius: 15px (для profile cards)
- **With Image**: NetworkImage с fit: BoxFit.cover
- **Placeholder**: Solid color background (#D9DDE2)

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

## Mobile Card Components (Flutter)

### 1. User Card with Live Badge

**Размер**: 140px × 68px

**Структура**:
- Container: width 140px, height 68px
- Padding: 10px all
- Background: #F4F6F9
- Border Radius: 10px

**Элементы**:
- Avatar Container: 48px × 48px
  - Avatar: 40px × 40px (offset: left 4px, top 4px)
  - Border Radius: 40px
  - Placeholder: #D9DDE2
  - Live Badge: 28px × 14px (bottom-right position)
    - Gradient: #833AB4 → #FD1D1D → #FCB045
    - Border: 1px white
    - Border Radius: 12px
    - Text: "Live", 10px, weight 600, white
    - Padding: 4px/2px

- Text Section (spacing: 10px from avatar):
  - Name: "Anna S."
    - Font: Archivo 13px, weight 600
    - Color: #09101D
    - Line Height: 1.40
  - Role: "Teacher"
    - Font: Archivo 12px, weight 400
    - Color: #747B84
    - Line Height: 1.40

---

### 2. User Comment Card

**Размер**: 140px × auto height

**Структура**:
- Container: width 140px
- Padding: 10px all
- Background: #F4F6F9
- Border Radius: 10px
- Column spacing: 10px

**Элементы**:
- Header Row (spacing: 5px):
  - Avatar: 48px × 48px (40px + 4px offset)
    - Border Radius: 40px
    - Background: #D9DDE2
  - Text Column:
    - Name: "James Dowson"
      - Font: Archivo 12px, weight 900
      - Color: #09101D
      - Line Height: 1.20
    - Role: "Expert"
      - Font: Archivo 11px, weight 400
      - Color: #747B84
      - Line Height: 1.40

- Comment Text:
  - Font: Archivo 12px, weight 400
  - Color: #09101D
  - Line Height: 1.40
  - Width: 120px
  - Example: "In 1975, the market cap of gold peaked at $1.2 trillion USD..."

---

### 3. Crypto/Bitcoin Card

**Размер**: 140px × 170px

**Структура**:
- Container: width 140px, height 170px
- Padding: 15px all
- Background: #F4F6F9
- Border Radius: 10px
- Column spacing: 15px (between elements)

**Элементы**:
- Logo: 40px × 40px
  - Border Radius: 50px
  - Image: NetworkImage

- Title Section:
  - Title: "Bitcoin"
    - Font: Archivo 13px, weight 700
    - Color: #09101D
    - Line Height: 1.40
  - Price: "3,715 USD M"
    - Font: Archivo 12px, weight 400
    - Color: #50555C
    - Line Height: 1.40

- Buy Button:
  - Height: 36px
  - Padding: 16px/10px
  - Background: #09101D
  - Border Radius: 15px
  - Text: "Buy"
    - Font: Archivo 13px, weight 600
    - Color: white
    - Line Height: 1.40

---

### 4. Category Image Card

**Размер**: 166.5px × 166.5px

**Структура**:
- Container: width 166.5px, height 166.5px
- Border Radius: 16px
- Background: #F4F6F9

**Элементы**:
- Image: 166.5px × 166.5px
  - Fit: cover

- Gradient Overlay:
  - Position: bottom (от top 96px до bottom)
  - Height: 70px
  - Gradient: transparent → rgba(29, 29, 29, 0.50)

- Title:
  - Position: bottom (top 129px)
  - Padding: left 10px
  - Text: "Vegetables"
    - Font: Archivo 16px, weight 600
    - Color: white
    - Line Height: 1.40
  - Width: 157px

---

### 5. User Profile Card

**Размер**: 140px × auto height

**Структура**:
- Container: width 140px
- Background: #F4F6F9
- Border Radius: 15px
- Clip Behavior: antiAlias

**Элементы**:
- Top Section:
  - Padding: 10px (top, left, right), 5px (bottom)
  - Image: 80px × 80px
    - Border Radius: 15px
    - Fit: cover
  - Favorite Icon: 14px × 14px (top-right)
    - Padding: 8px in container
    - Border Radius: 20px

- Bottom Section:
  - Padding: bottom 10px
  - Column spacing: 5px

  - Text Section (padding: left 10px):
    - Name: "Nicole"
      - Font: Archivo 13px, weight 600
      - Color: #09101D
      - Line Height: 1.40
    - Username: "@nicole"
      - Font: Archivo 11px, weight 600
      - Color: #414249
      - Line Height: 1.40

  - Follow Button (padding: horizontal 10px):
    - Height: 36px
    - Width: 100%
    - Padding: 16px/10px
    - Background: #09101D
    - Border Radius: 15px
    - Text: "Follow"
      - Font: Archivo 11px, weight 600
      - Color: white
      - Line Height: 1.40

---

### 6. Story/Post Card

**Размер**: 140px × 190px

**Структура**:
- Container: width 140px, height 190px
- Border Radius: 15px
- Clip Behavior: antiAlias

**Элементы**:
- Background Image:
  - Size: 140px × 190px
  - Fit: cover

- Overlay:
  - Background: rgba(0, 0, 0, 0.10)
  - Padding: 10px (top, left, right), 20px (bottom)
  - Position: bottom
  - Column spacing: 2px

- Text Content:
  - Title: "Breath into it"
    - Font: Archivo 14px, weight 600
    - Color: white
    - Line Height: 1.40
  - Subtitle: "with Maria Mendez"
    - Font: Archivo 12px, weight 400
    - Color: white
    - Line Height: 1.40
  - Width: 120px

---

### 7. Product Card

**Размер**: 140px × 210px

**Структура**:
- Container: width 140px, height 210px
- Clip Behavior: none
- Column layout

**Элементы**:
- Image Section (expanded):
  - Image: cover fit
  - Border Radius: 15px

  - New Badge (padding: 10px):
    - Background: #11BB8D
    - Height: 24px
    - Padding: 6px horizontal
    - Border Radius: 11px
    - Text: "New"
      - Font: Archivo 11px, weight 600
      - Color: white
      - Line Height: 1.40

- Info Section (padding: top 5px):
  - Column spacing: 2px

  - Title: "Chuck's Donuts"
    - Font: Archivo 13px, weight 600
    - Color: #09101D
    - Line Height: 1.40
    - Width: 106px

  - Price: "1.95 USD"
    - Font: Archivo 14px, weight 600
    - Color: #09101D
    - Line Height: 1.40

  - Location: "New-York"
    - Font: Archivo 13px, weight 400
    - Color: #414249
    - Line Height: 1.40

  - Date: "31 July, 12:10 PM"
    - Font: Archivo 12px, weight 400
    - Color: #747B84
    - Line Height: 1.40

  - Action Icons (right side):
    - Size: 24px × 24px each
    - Padding: 5px-6px
    - Border Radius: 100px
    - Icon Size: internal (14px-16px)

---

### 8. Course Card

**Размер**: 140px × 150px

**Структура**:
- Container: width 140px, height 150px
- Border Radius: 16px
- Clip Behavior: antiAlias

**Элементы**:
- Image Section (expanded):
  - Height: ~92px
  - Image: cover fit
  - Border Radius: 15px

  - New Badge (padding: 10px):
    - Background: #11BB8D
    - Height: 24px
    - Padding: 6px horizontal
    - Border Radius: 11px
    - Text: "new"
      - Font: Archivo 11px, weight 600
      - Color: white
      - Line Height: 1.40

- Info Section:
  - Padding: 5px (top, right, bottom), 5px (left in text)
  - Column spacing: 2px

  - Title: "Graphic Tools"
    - Font: Archivo 16px, weight 700
    - Color: #09101D
    - Line Height: 1.40
    - Width: 130px

  - Metadata Row (spacing: 5px):
    - Duration Icon + Text:
      - Icon: 24px (padding 7px, internal 12px)
      - Text: "3h 15m"
        - Font: Archivo 11px, weight 600
        - Color: #747B84
        - Line Height: 1.40

    - Students Icon + Text:
      - Icon: 24px (padding 7px, internal 12px)
      - Text: "280"
        - Font: Archivo 11px, weight 600
        - Color: #747B84
        - Line Height: 1.40

---

## Паттерны

### Mobile Layout Patterns (Flutter)

#### Container Configuration

- **Mobile Screen Width**: 375px (стандартная ширина для мобильных экранов)
- **Container Padding**: 16px horizontal
- **Content Width**: 343px (375px - 32px padding)
- **Column Spacing**: 10px (spacing между элементами)

#### Button States Matrix (из Flutter кода)

| State | Background | Text Color | Border | Description |
|-------|------------|------------|--------|-------------|
| **Filled (Primary)** | #4141E6 | #FFFFFF | none | Основное действие |
| **Filled (Secondary)** | #F4F6F9 | #09101D | none | Вторичное действие |
| **Outlined (Primary)** | transparent | #4141E6 | 1px #0B24FB или #4141E6 | Альтернативное действие |
| **Disabled** | #F4F6F9 | #D9DDE2 | none | Неактивное состояние |
| **Ghost/Text** | transparent или minimal | #09101D | none | Минимальный акцент |

#### Button Dimensions Reference

```
Small Button (36px):
├─ Height: 36px
├─ Padding: 10px vertical, 16px horizontal
├─ Border Radius: 15px или 12px
├─ Font: Archivo 13px, Weight 600, Line-height 1.40
└─ Icon: 16px with 8px spacing

Icon Button (40px):
├─ Size: 40px × 40px
├─ Padding: 12px
├─ Border Radius: 15px
├─ Icon Size: 16px (centered)
└─ States: Filled, Outlined, Secondary, Disabled
```

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
  - SM: 16px (используется в Flutter buttons)
  - Base: 20px
  - MD: 24px
  - LG: 32px
  - XL: 48px
- **Button Icons**: 16px × 16px (из Flutter кода)
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
- Полная цветовая палитра с реальными значениями из Flutter кода:
  - Primary: #4141E6
  - Primary border: #0B24FB
  - Background light: #F4F6F9
  - Background dark: #18202F
  - Background overlay: rgba(0, 0, 0, 0.10)
  - Text primary: #09101D
  - Text secondary: #747B84
  - Text tertiary: #414249
  - Text muted: #50555C
  - Text disabled: #D9DDE2
  - Success: #11BB8D
- Градиенты:
  - Live Badge: #833AB4 → #FD1D1D → #FCB045
  - Image Overlay: transparent → rgba(29, 29, 29, 0.50)
- Компонент Button с всеми состояниями (Filled, Outlined, Ghost, Disabled)
- Icon Button (40px) с вариантами
- Badges:
  - Live Badge (Instagram-style): 28×14px, gradient background
  - New Badge: 24px height, #11BB8D background
- Avatar компонент:
  - Размеры: 40px, 48px, 80px
  - Варианты: Circle, Rounded Square, With Live Badge
  - Placeholder: #D9DDE2
- Mobile Card Components (8 готовых блоков):
  1. User Card with Live Badge (140×68px)
  2. User Comment Card (140px width)
  3. Crypto/Bitcoin Card (140×170px)
  4. Category Image Card (166.5×166.5px)
  5. User Profile Card (140px width)
  6. Story/Post Card (140×190px)
  7. Product Card (140×210px)
  8. Course Card (140×150px)
- Mobile Layout Patterns (375px width)
- Spacing values: 5px, 10px, 15px, 20px, 70px
- Border radius values: 10px, 11px, 12px, 15px, 16px
- Typography: Archivo (10px-16px, weights 400-900, line-height 1.20-1.40)
- Layout patterns и Best practices

---

## Поддержка и контакты

- **Документация**: `/docs`
- **Компоненты**: `/components`
- **Примеры**: `/examples`
- **Вопросы**: Создайте issue в репозитории

---

**© 2025 Design System v5. Все права защищены.**
