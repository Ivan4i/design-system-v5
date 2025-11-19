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
/* Текст из Tailwind CSS */
--color-text-primary: #020617;     /* slate-950 */
--color-text-secondary: #27272A;   /* zinc-800 */
--color-text-dark: #09101D;        /* Основной темный текст (Flutter) */
--color-text-gray: #373940;        /* Серый текст для подписей (Flutter) */
```

### Accent Colors

```css
/* Акцентные цвета */
--color-accent-blue: #1D4ED8;      /* blue-700 */
--color-accent-purple: #7B61FF;    /* Фиолетовый из Flutter кода */
--color-link-blue: #4141E6;        /* Синий для ссылок и активных элементов */
```

### Background Colors

```css
/* Фоны для компонентов */
--color-bg-light: #F4F6F9;         /* Светлый фон */
--color-bg-card-light: #D9DDE2;    /* Светлая карточка */
--color-bg-card-dark: #23262B;     /* Темная карточка */
```

### Overlay & Shadow Colors

```css
/* Overlay цвета для Flutter компонентов */
--overlay-black-30: rgba(0, 0, 0, 0.30);    /* Черный overlay 30% для бейджей и play button */
--overlay-white-50: rgba(255, 255, 255, 0.50); /* Белый overlay 50% для текстовых блоков */

/* Тени */
--shadow-light: rgba(240, 241, 242, 1.00);
--shadow-text: rgba(0, 0, 0, 0.40);         /* Тень для текста */
--shadow-box: rgba(0, 0, 0, 0.40);          /* Тень для контейнеров */
```

### Gradients

```css
/* Градиенты для Flutter компонентов */
--gradient-black-vertical: linear-gradient(to bottom, rgba(0, 0, 0, 0), rgba(0, 0, 0, 1));
/* Используется в карточках категорий для затемнения снизу */
/* Alignment: начало (0.50, -0.00), конец (0.50, 1.00) */
```

**Flutter код градиента:**
```dart
gradient: LinearGradient(
  begin: Alignment(0.50, -0.00),
  end: Alignment(0.50, 1.00),
  colors: [Colors.black.withValues(alpha: 0), Colors.black],
)
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
--space-2: 0.5rem;    /* 8px */
--space-3: 0.75rem;   /* 12px */
--space-4: 1rem;      /* 16px */
--space-5: 1.25rem;   /* 20px */
--space-6: 1.5rem;    /* 24px */
--space-7: 1.75rem;   /* 28px - из Flutter spacing: 7 */
--space-8: 2rem;      /* 32px */
--space-10: 2.5rem;   /* 40px */
--space-12: 3rem;     /* 48px */
--space-16: 4rem;     /* 64px */
--space-20: 5rem;     /* 80px */
--space-24: 6rem;     /* 96px */
```

**Flutter Spacing Values (из кода):**
- `spacing: 2` → 2px - минимальный отступ между элементами
- `spacing: 5` → 5px - отступ в заголовках
- `spacing: 6` → 6px - отступ между аватаром и текстом
- `spacing: 7` → 7px - отступ в layout
- `spacing: 10` → 10px - стандартный отступ между секциями

### Border Radius

```css
--radius-none: 0;
--radius-sm: 0.25rem;     /* 4px */
--radius-base: 0.5rem;    /* 8px */
--radius-md: 0.75rem;     /* 12px */
--radius-lg: 0.9375rem;   /* 15px - из Flutter кода (основной для карточек) */
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

#### Flutter Mobile Cards

Специальные карточки для мобильного приложения, извлеченные из Flutter кода.

##### Category Card with Gradient (Tall)
- **Size**: 230px × 330px
- **Border Radius**: 16px
- **Background**: Image with gradient overlay
- **Gradient**: Linear gradient (top to bottom): `rgba(0, 0, 0, 0)` → `rgba(0, 0, 0, 1)`
- **Padding**:
  - Top: 15px
  - Left: 15px, Right: 10px, Bottom: 30px
- **Title**:
  - Font: Archivo Bold
  - Size: 32px
  - Color: White (#FFFFFF)
  - Line Height: 1.40
- **Usage**: Категории (BBQ, и т.д.)

```dart
Container(
  width: 230,
  height: 330,
  decoration: ShapeDecoration(
    gradient: LinearGradient(
      begin: Alignment(0.50, -0.00),
      end: Alignment(0.50, 1.00),
      colors: [Colors.black.withValues(alpha: 0), Colors.black],
    ),
    shape: RoundedRectangleBorder(borderRadius: BorderRadius.circular(15)),
  ),
)
```

##### Category Card (Square)
- **Size**: 230px × 230px
- **Border Radius**: 15px
- **Background**: Image with gradient overlay
- **Gradient**: Linear gradient (top to bottom): `rgba(0, 0, 0, 0)` → `rgba(0, 0, 0, 1)`
- **Padding**: 10px
- **Title**:
  - Font: Archivo Bold
  - Size: 26px
  - Color: White (#FFFFFF)
  - Line Height: 1.40
- **Usage**: Локации (Berlin, и т.д.)

##### Info Card with Semi-transparent Overlay
- **Size**: 230px × 230px
- **Border Radius**: 16px
- **Background**: Image (BoxFit.cover)
- **Overlay**: White with 50% opacity (`rgba(255, 255, 255, 0.50)`)
- **Padding**: 20px
- **Text**:
  - Font: Archivo SemiBold
  - Size: 13px
  - Color: Dark (#09101D)
  - Line Height: 1.40
  - Max Width: 190px
- **Usage**: Информационные блоки с описанием

```dart
Container(
  padding: const EdgeInsets.all(20),
  decoration: BoxDecoration(
    color: Colors.white.withValues(alpha: 0.50),
  ),
)
```

##### Recipe Card with Author
- **Size**: 270px × 300px
- **Border Radius**: 15px
- **Image**: 270px × 203px (top section)
- **Badges**:
  - Two badges on image (views/likes count, duration)
  - Height: 24px
  - Padding: left 5px, right 10px
  - Background: `rgba(0, 0, 0, 0.30)`
  - Border Radius: 10px
  - Text: White, 11px, Archivo SemiBold
- **Title**:
  - Font: Archivo SemiBold
  - Size: 15px
  - Color: #09101D
  - Line Height: 1.40
  - Padding Top: 10px
- **Author Section**:
  - Avatar: 40px container with 32px image
  - Avatar Border Radius: 10px
  - Name: Color #4141E6, 13px, Archivo Regular
  - Role: Color #373940, 12px, Archivo Regular
  - Spacing: 6px between avatar and text
- **Usage**: Карточки рецептов с информацией об авторе

##### Video Card with Play Button
- **Size**: 260px × 200px
- **Border Radius**: 15px
- **Image**: 260px × 168px
- **Play Button**:
  - Size: 40px × 40px
  - Padding: 12px
  - Background: `rgba(0, 0, 0, 0.30)`
  - Border Radius: 100px (circle)
  - Position: Centered on image
- **Badges**: Similar to Recipe Card (14k views, 10 min)
- **Title**:
  - Font: Archivo Bold
  - Size: 16px
  - Color: #09101D
  - Line Height: 1.40
  - Padding: 5px
- **Usage**: Видео контент

##### Full Image Card with Gradient Text
- **Size**: 230px × 330px
- **Border Radius**: 16px
- **Background**: Full image (230px × 330px)
- **Gradient Overlay**: Linear gradient at bottom
  - From: `rgba(0, 0, 0, 0)`
  - To: `rgba(0, 0, 0, 1)`
- **Text**:
  - Font: Archivo SemiBold
  - Size: 13px
  - Color: White (#FFFFFF)
  - Line Height: 1.40
  - Max Width: 190px
  - Padding: 20px
- **Usage**: Промо карточки с текстом поверх изображения

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

#### Flutter Overlay Badges

Бейджи для отображения на изображениях (из Flutter кода).

- **Height**: 24px
- **Padding**: Left 5px, Right 10px
- **Border Radius**: 10px
- **Background**: `rgba(0, 0, 0, 0.30)` (черный с 30% прозрачностью)
- **Icon**:
  - Size: 24px × 24px
  - Padding: 8px
  - Border Radius: 100px (circle)
- **Text**:
  - Font: Archivo SemiBold
  - Size: 11px
  - Color: White (#FFFFFF)
  - Line Height: 1.40
- **Examples**: '134', '30 min', '14k', '10 min'
- **Usage**: Счетчики просмотров, лайков, продолжительность видео/рецептов

```dart
Container(
  height: 24,
  padding: const EdgeInsets.only(left: 5, right: 10),
  decoration: ShapeDecoration(
    color: Colors.black.withValues(alpha: 0.30),
    shape: RoundedRectangleBorder(borderRadius: BorderRadius.circular(10)),
  ),
  child: Row(
    children: [
      Container(
        width: 24,
        height: 24,
        padding: const EdgeInsets.all(8),
        // Icon here
      ),
      Text(
        '134',
        style: TextStyle(
          color: Colors.white,
          fontSize: 11,
          fontFamily: 'Archivo',
          fontWeight: FontWeight.w600,
          height: 1.40,
        ),
      ),
    ],
  ),
)
```

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

#### Flutter Avatar (Recipe Author)

Avatar компонент из Flutter кода для карточек рецептов.

- **Outer Container**: 40px × 40px
- **Inner Image**: 32px × 32px
  - Position: Left 4px, Top 4px
- **Border Radius**: 10px (rounded square)
- **Placeholder Background**: #D9DDE2
- **Image Fit**: BoxFit.cover

```dart
Container(
  width: 40,
  height: 40,
  child: Stack(
    children: [
      Positioned(
        left: 4,
        top: 4,
        child: Container(
          width: 32,
          height: 32,
          decoration: ShapeDecoration(
            color: const Color(0xFFD9DDE2),
            shape: RoundedRectangleBorder(borderRadius: BorderRadius.circular(10)),
          ),
        ),
      ),
      Positioned(
        left: 4,
        top: 4,
        child: Container(
          width: 32,
          height: 32,
          decoration: ShapeDecoration(
            image: DecorationImage(
              image: NetworkImage("https://placehold.co/32x32"),
              fit: BoxFit.cover,
            ),
            shape: RoundedRectangleBorder(borderRadius: BorderRadius.circular(10)),
          ),
        ),
      ),
    ],
  ),
)
```

**Author Info Layout:**
- **Spacing**: 6px between avatar and text
- **Name**:
  - Font: Archivo Regular
  - Size: 13px
  - Color: #4141E6 (link blue)
  - Line Height: 1.40
- **Role**:
  - Font: Archivo Regular
  - Size: 12px
  - Color: #373940 (gray)
  - Line Height: 1.40

---

### 10. Media Controls (Flutter)

#### Play Button Overlay

Кнопка воспроизведения для видео карточек из Flutter кода.

- **Size**: 40px × 40px
- **Padding**: 12px (внутри кнопки для иконки)
- **Border Radius**: 100px (perfect circle)
- **Background**: `rgba(0, 0, 0, 0.30)` (черный с 30% прозрачностью)
- **Position**: Center of video thumbnail
- **Icon Size**: 16px × 16px (after padding)
- **Usage**: Overlay на превью видео

```dart
Container(
  width: 40,
  height: 40,
  padding: const EdgeInsets.all(12),
  decoration: ShapeDecoration(
    color: Colors.black.withValues(alpha: 0.30),
    shape: RoundedRectangleBorder(borderRadius: BorderRadius.circular(100)),
  ),
  child: Row(
    mainAxisSize: MainAxisSize.min,
    mainAxisAlignment: MainAxisAlignment.center,
    crossAxisAlignment: CrossAxisAlignment.center,
    spacing: 10,
    children: [
      // Play icon here (16px × 16px)
    ],
  ),
)
```

**Позиционирование на Video Card:**
- Position: Absolute
- Left: 110px (centered on 260px width)
- Top: 64px (centered on 168px height)

---

### 11. List Items

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

**Текущая версия**: v5.1.0

### Changelog

#### v5.1.0 (2025-11-19)
- **Добавлены Flutter Mobile компоненты:**
  - Category Card with Gradient (Tall) - 230×330px
  - Category Card (Square) - 230×230px
  - Info Card with Semi-transparent Overlay - 230×230px
  - Recipe Card with Author - 270×300px
  - Video Card with Play Button - 260×200px
  - Full Image Card with Gradient Text - 230×330px
- **Новые цвета:**
  - `#4141E6` - Синий для ссылок и активных элементов
  - `#09101D` - Основной темный текст
  - `#373940` - Серый текст для подписей
  - Overlay цвета: `rgba(0, 0, 0, 0.30)` и `rgba(255, 255, 255, 0.50)`
- **Градиенты:**
  - Linear gradient (черный вертикальный) для карточек категорий
- **Flutter компоненты:**
  - Overlay Badges (24px height, полупрозрачный черный фон)
  - Play Button Overlay (40×40px, круглая кнопка)
  - Flutter Avatar для карточек рецептов (40px outer, 32px inner)
- **Spacing values:** Добавлены spacing значения из Flutter (2px, 5px, 6px, 7px, 10px)

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
