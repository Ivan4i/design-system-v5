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

/* Фоновые цвета из Flutter кода */
--color-scaffold-dark: #12202F;      /* Color.fromARGB(255, 18, 32, 47) */
```

### Text Colors

```css
/* Текст из Tailwind CSS */
--color-text-primary: #020617;     /* slate-950 */
--color-text-secondary: #27272A;   /* zinc-800 */
```

### Accent Colors

```css
/* Акцентные цвета */
--color-accent-blue: #1D4ED8;      /* blue-700 */

/* Цвета из Flutter кода */
--color-primary-blue: #4141E6;     /* Color(0xFF4141E6) - основной синий */
--color-accent-purple: #7B61FF;    /* Color(0xFF7B61FF) - фиолетовый акцент */
```

### UI Colors

```css
/* UI элементы из Flutter кода */
--color-gray-light: #D9DDE2;       /* Color(0xFFD9DDE2) - светло-серый для разделителей */
--color-background-light: #F4F6F9; /* Color(0xFFF4F6F9) - светлый фон для inactive кнопок */

/* Цвета для карточек и контента */
--color-yellow-accent: #FFC043;    /* Color(0xFFFFC043) - желтый для скидок, CTA кнопок */
--color-green-badge: #11BB8D;      /* Color(0xFF11BB8D) - зеленый для эко-бейджей */
--color-cyan-light: #7CC5D6;       /* Color(0xFF7CC5D6) - голубой для цветовых селекторов */
--color-red-accent: #E24949;       /* Color(0xFFE24949) - красный акцент */

/* Текстовые цвета */
--color-text-tertiary: #747B84;    /* Color(0xFF747B84) - третичный текст (метаданные) */
--color-text-quaternary: #414249;  /* Color(0xFF414249) - четвертичный текст */
--color-text-dark-gray: #373940;   /* Color(0xFF373940) - темно-серый текст */

/* Overlay цвета для видео/медиа */
--color-overlay-black-30: rgba(0, 0, 0, 0.30);  /* Черный с 30% прозрачностью */

/* Цвета для графиков и charts */
--color-chart-grid: #A4ABB3;       /* Color(0xFFA4ABB3) - светло-серый для grid lines */
--color-chart-axis: #747B84;       /* Color(0xFF747B84) - темнее для осей */

/* Цвета для pagination dots и индикаторов */
--color-pagination-active: #181920;   /* Color(0xFF181920) - темный для активной точки */
--color-pagination-inactive: #FAFAFB; /* Color(0xFFFAFAFB) - светлый для неактивных точек */
```

### Shadow Colors

```css
/* Тени */
--shadow-light: rgba(240, 241, 242, 1.00);  /* из кода: shadow-[0px_1px_1px_0px_rgba(240,241,242,1.00)] */

/* Полупрозрачные цвета из Flutter кода */
--color-overlay-dark: rgba(9, 16, 29, 0.2);    /* Color(0x3309101D) */
--color-overlay-black: rgba(0, 0, 0, 0.25);    /* Colors.black.withValues(alpha: 0.25) */
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

/* Множители line-height из Flutter кода */
--line-height-multiplier: 1.40;  /* height: 1.40 - используется в TextStyle */
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

### Flutter Mobile Text Styles (из реального кода)

#### Info Bar Text
- **Font**: 11px (0.6875rem), Archivo
- **Weight**: 400
- **Color**: White (#FFFFFF)
- **Line Height**: 1.40
- **Использование**: Market info bar, статусные сообщения

#### Info Text Medium
- **Font**: 12px (0.75rem), Archivo
- **Weight**: 400
- **Color**: White (#FFFFFF)
- **Line Height**: 1.40
- **Использование**: Информационные панели, вторичный текст

#### Button Text
- **Font**: 13px (0.8125rem), Archivo
- **Weight**: 600 (Semibold)
- **Color**: White (#FFFFFF) на primary фоне, Black (#09101D) на light фоне
- **Line Height**: 1.40
- **Использование**: Текст на кнопках, активные элементы

#### Body Text
- **Font**: 14px (0.875rem), Archivo
- **Weight**: 400
- **Color**: White (#FFFFFF)
- **Line Height**: 1.40
- **Использование**: Основной текст уведомлений

#### Heading Text
- **Font**: 16px (1rem), Archivo
- **Weight**: 700 (Bold)
- **Color**: White (#FFFFFF)
- **Line Height**: 1.40
- **Использование**: Заголовки уведомлений, важные сообщения (например, "Price is up!")

#### Micro Text (Badge Text)
- **Font**: 9px (0.5625rem), Archivo
- **Weight**: 600 (Semibold)
- **Color**: White (#FFFFFF) на темном фоне
- **Line Height**: 1.40
- **Использование**: Маленькие бейджи ("New", "Join Life"), статусы

#### Mini Text (Avatar Counter)
- **Font**: 10px (0.625rem), Archivo
- **Weight**: 600 (Semibold)
- **Color**: White (#FFFFFF)
- **Line Height**: 1.40
- **Text Align**: Center
- **Использование**: Счетчики в аватарах ("1k"), малые индикаторы

#### Video Badge Text
- **Font**: 11px (0.6875rem), Archivo
- **Weight**: 600 (Semibold)
- **Color**: White (#FFFFFF)
- **Line Height**: 1.40
- **Использование**: Продолжительность видео, статистика просмотров

#### Metadata Text
- **Font**: 13px (0.8125rem), Archivo
- **Weight**: 400 (Regular)
- **Color**: #747B84 (tertiary gray)
- **Line Height**: 1.40
- **Использование**: Даты, время чтения, дополнительная информация

#### Card Title (Medium)
- **Font**: 16px (1rem), Archivo
- **Weight**: 700 (Bold)
- **Color**: #09101D (black)
- **Line Height**: 1.40
- **Использование**: Заголовки блог-карточек, видео-карточек

#### Card Title (Large)
- **Font**: 18px (1.125rem), Archivo
- **Weight**: 700 (Bold)
- **Color**: #09101D (black)
- **Line Height**: 1.40
- **Использование**: Заголовки товарных карточек, крупные заголовки

#### Chart Label (Small)
- **Font**: 8px (0.5rem), Archivo
- **Weight**: 700 (Bold)
- **Color**: #09101D (black)
- **Line Height**: 1.40
- **Text Align**: Center
- **Использование**: Метки на осях графиков, маленькие подписи

#### Chart Label (Medium)
- **Font**: 10px (0.625rem), Archivo
- **Weight**: 600 (Semibold)
- **Color**: #09101D (black)
- **Line Height**: 1.40
- **Text Align**: Center
- **Padding**: horizontal 5px
- **Использование**: Стандартные метки на графиках

#### Page Title (Hero)
- **Font**: 72px (4.5rem), Archivo
- **Weight**: 800 (Extrabold)
- **Color**: #09101D (black)
- **Line Height**: 0.70
- **Использование**: Главные заголовки страниц, hero titles

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

### Flutter Mobile Spacing (из реального кода)

```css
/* Padding values используемые в Flutter приложении */
--padding-xs: 0.375rem;     /* 6px */
--padding-sm: 0.5rem;       /* 8px */
--padding-md: 0.625rem;     /* 10px */
--padding-lg: 0.75rem;      /* 12px */
--padding-xl: 1rem;         /* 16px */
--padding-2xl: 1.25rem;     /* 20px */
--padding-3xl: 3.125rem;    /* 50px - outer container padding */

/* Spacing между элементами (gap/spacing в Column/Row) */
--gap-sm: 0.625rem;         /* 10px */
--gap-md: 1rem;             /* 16px */
--gap-lg: 1.25rem;          /* 20px */

/* Специфичные размеры для mobile layout */
--mobile-width: 375px;      /* Стандартная ширина мобильного экрана */
--mobile-height: 812px;     /* Стандартная высота мобильного экрана (iPhone) */
--status-bar-height: 44px;  /* Высота статус бара iOS */

/* Размеры карточек */
--card-width-small: 170px;  /* Узкая карточка (продукты) */
--card-width-medium: 230px; /* Средняя карточка (стандарт) */

/* Размеры изображений в карточках */
--card-image-small: 170px;  /* Изображение для узкой карточки */
--card-image-medium: 230px; /* Изображение для средней карточки */

/* Размеры аватаров */
--avatar-size-small: 24px;  /* Маленький аватар */
--avatar-size-medium: 32px; /* Средний аватар */
--avatar-size-large: 40px;  /* Большой аватар */

/* Размеры иконок */
--icon-size-small: 16px;    /* Маленькая иконка */
--icon-size-medium: 24px;   /* Средняя иконка */
--icon-size-large: 30px;    /* Большая иконка */
```

### Border Radius

```css
--radius-none: 0;
--radius-sm: 0.125rem;    /* 2px */
--radius-base: 0.25rem;   /* 4px */
--radius-md: 0.375rem;    /* 6px */
--radius-lg: 0.5rem;      /* 8px */
--radius-xl: 0.75rem;     /* 12px */
--radius-2xl: 1rem;       /* 16px */
--radius-full: 9999px;
```

### Flutter Mobile Border Radius (из реального кода)

```css
/* Border radius используемые в мобильном приложении */
--radius-mobile-xs: 0.3125rem;    /* 5px - мелкие элементы, badges */
--radius-mobile-sm: 0.625rem;     /* 10px - маленькие элементы, video badges */
--radius-mobile-md: 0.9375rem;    /* 15px - карточки, контейнеры, иконки */
--radius-mobile-lg: 1.875rem;     /* 30px - bottom sheets, модальные окна, avatars */
--radius-mobile-xl: 2.5rem;       /* 40px - крупные аватары */
--radius-mobile-pill: 6.25rem;    /* 100px - полностью скругленные элементы (pill) */
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

### 16. Mobile Components (Flutter)

#### Info Bar

Горизонтальная информационная панель для отображения маркет данных.

- **Width**: 375px (full mobile width)
- **Background**: #4141E6 (color-primary-blue)
- **Padding**: symmetric(vertical: 10px)
- **Text Style**:
  - Font: 11px Archivo
  - Weight: 400
  - Color: White
  - Line Height: 1.40
- **Layout**: Row с spacing: 20px между элементами
- **Separator**: '・' (средняя точка)
- **Использование**: Market Pairs, ETH Gas, Market Cap, 24h Volume

#### Bottom Sheet

Модальное окно снизу экрана с закругленными верхними углами.

- **Width**: 375px (full mobile width)
- **Background**: #4141E6 (color-primary-blue) или White
- **Border Radius**:
  - topLeft: 30px (radius-mobile-lg)
  - topRight: 30px (radius-mobile-lg)
- **Content Padding**: symmetric(vertical: 20px)
- **Handle Area**:
  - Padding: symmetric(horizontal: 167px, vertical: 8px)
  - Background: White

#### Bottom Sheet Handle

Индикатор для drag-to-dismiss жеста.

- **Width**: 40px
- **Height**: 3px
- **Background**: #D9DDE2 (color-gray-light)
- **Border Radius**: 100px (полностью скругленный)
- **Position**: Centered horizontally в handle area

#### Notification Card

Карточка уведомления с иконкой и текстом.

- **Width**: 375px (full mobile width)
- **Background**: #4141E6 (color-primary-blue)
- **Border Radius**:
  - topLeft: 30px (radius-mobile-lg)
  - topRight: 30px (radius-mobile-lg)
- **Layout**:
  - Icon area padding-right: 10px
  - Content padding: symmetric(vertical: 12px)
  - Action button padding: symmetric(horizontal: 16px)
- **Icon**:
  - Size: 40px × 40px
  - Border Radius: 15px (radius-mobile-md)
  - Placeholder: NetworkImage или local asset
- **Text**:
  - Title: 16px Bold, White, Line Height: 1.40
  - Subtitle: 14px Regular, White, Line Height: 1.40
- **Action Button**:
  - Size: 44px × 44px (touch target)
  - Icon size: 24px
  - Background: rgba(9, 16, 29, 0.2) с border-radius: 100px

#### Container with Border

Контейнер с цветной рамкой для демонстрации компонентов.

- **Border**: 1px solid #7B61FF (color-accent-purple)
- **Border Radius**: 15px (radius-mobile-md)
- **Padding**: 50px (padding-3xl)
- **Clip**: antiAlias
- **Spacing**: 20px между дочерними элементами (Column spacing)

#### Divider / Separator Bar

Горизонтальный разделитель с закругленными верхними углами.

- **Width**: 343px (mobile-width - 32px horizontal padding)
- **Height**: 10px
- **Background**: #D9DDE2 (color-gray-light)
- **Border Radius**:
  - topLeft: 10px (radius-mobile-sm)
  - topRight: 10px (radius-mobile-sm)
- **Margin**: 16px horizontal (from screen edges)

#### Mobile Screen Container

Контейнер имитирующий мобильный экран.

- **Width**: 375px (mobile-width)
- **Height**: 812px (mobile-height) - iPhone dimensions
- **Background**:
  - Variant 1: rgba(0, 0, 0, 0.25) - темный с прозрачностью
  - Variant 2: rgba(217, 221, 226, 0.25) - светлый с прозрачностью
- **Border Radius**: 30px (для preview) или 40px
- **Status Bar**: Height: 44px на верху экрана

#### Button (Mobile)

Кнопка для мобильного интерфейса с двумя вариантами.

- **Height**: 36px
- **Padding**: symmetric(horizontal: 16px, vertical: 10px)
- **Border Radius**: 15px (radius-mobile-md)
- **Text Style**:
  - Font: 13px Archivo
  - Weight: 600 (Semibold)
  - Line Height: 1.40
- **Spacing**: 8px между иконкой и текстом (если есть иконка)
- **States/Variants**:
  - **Primary (Active)**:
    - Background: #4141E6 (color-primary-blue)
    - Text Color: White (#FFFFFF)
    - Использование: Активная выбранная кнопка
  - **Secondary (Inactive)**:
    - Background: #F4F6F9 (color-background-light)
    - Text Color: Black (#09101D)
    - Использование: Неактивные кнопки, secondary actions
- **Layout**: Обычно в группах с padding: 16px horizontal от краев экрана

#### iOS Home Indicator

Индикатор домашнего жеста iOS (появляется внизу экрана).

- **Width**: 134px
- **Height**: 5px
- **Border Radius**: 100px (полностью скругленный pill)
- **Color**:
  - White (#FFFFFF) на темном фоне
  - Black (#09101D) на светлом фоне
- **Container Height**: 34px (общая высота области индикатора)
- **Position**:
  - Centered horizontally
  - 21px from top of container (13px from bottom)
- **Использование**: Навигационный индикатор на iPhone без физической кнопки Home

#### Badge System (Complete)

Полная система бейджей с различными вариантами.

##### Text Badge

Бейдж с текстовой меткой.

- **Height**: 16px
- **Padding**: symmetric(horizontal: 4px, vertical: 2px)
- **Background**: #4141E6 (primary-blue)
- **Border Radius**: 12px
- **Text Style**:
  - Font: 10px Archivo
  - Weight: 600 (Semibold)
  - Color: White
  - Line Height: 1.40
- **Использование**: Текстовые метки, категории, статусы

##### Time Badge

Бейдж с отображением времени.

- **Height**: 16px
- **Padding**: symmetric(horizontal: 4px, vertical: 2px)
- **Background**: #4141E6 (primary-blue)
- **Border Radius**: 12px
- **Text**: "35:12" формат (10px Semibold White)
- **Использование**: Продолжительность, таймеры

##### Counter Badge

Бейдж со счетчиком.

- **Height**: 20px
- **Padding**: symmetric(horizontal: 4px, vertical: 2px)
- **Background**: #4141E6 (primary-blue)
- **Border Radius**: 20px (pill shape)
- **Text**:
  - Font: 10px Semibold White
  - Text Align: Center
  - Line Height: 1.40
- **Использование**: Уведомления, количество элементов ("11", "99+")

##### Notification Dot with Icon

Бейдж-точка с иконкой внутри.

- **Size**: 14×14px
- **Background**: #4141E6 (primary-blue)
- **Border**: 1px solid White
- **Border Radius**: 20px (круг)
- **Inner Icon**: 12×12px (padding: 2px)
- **Использование**: Индикаторы с иконкой, статус с действием

##### Status Dot (Primary)

Маленькая цветная точка-индикатор.

- **Size**: 12×12px
- **Padding**: symmetric(horizontal: 4px, vertical: 2px)
- **Background**: #4141E6 (primary-blue)
- **Border**: 2px solid White
- **Border Radius**: 20px (круг)
- **Использование**: Статус онлайн, активность

##### Status Dot (Success)

Зеленая точка успеха.

- **Size**: 12×12px
- **Padding**: symmetric(horizontal: 4px, vertical: 2px)
- **Background**: #11BB8D (green-badge)
- **Border**: 2px solid White
- **Border Radius**: 20px (круг)
- **Использование**: Успешный статус, доступность

##### Status Dot (Error)

Красная точка ошибки.

- **Size**: 12×12px
- **Padding**: symmetric(horizontal: 4px, vertical: 2px)
- **Background**: #E24949 (red-accent)
- **Border**: 2px solid White
- **Border Radius**: 20px (круг)
- **Использование**: Ошибка, недоступность, критичный статус

##### Legacy Badges (from previous versions)

- **New Badge**: 9px Semibold, #09101D background, может содержать emoji "🔥 New", 5px border-radius
- **Join Life Badge**: 9px Semibold, #11BB8D background, "Join Life" text, 5px border-radius
- **Strikethrough Price**: 14px Regular, #D9DDE2 color, текст с перечеркиванием

#### Discount Badge

Большой бейдж со скидкой и ценой.

- **Width**: 70px
- **Border Radius**: 10px (radius-mobile-sm)
- **Background**: #FFC043 (yellow)
- **Padding**: spacing: 4px между элементами
- **Content**:
  - Price: 14px Regular Black
  - Расположен над изображением товара
- **Использование**: Отображение скидочной цены на карточках товаров

#### Avatar (Small)

Маленький круглый аватар для списков.

- **Size**: 24px × 24px (inner), 32px × 32px (with border)
- **Border**: 4px solid White
- **Border Radius**: 30px или 40px (круг)
- **Image**: Border Radius 10px или 40px (для изображения)
- **Placeholder**: Background #D9DDE2
- **Использование**: Avatar groups, социальные индикаторы

#### Avatar Group

Группа наложенных аватаров с счетчиком.

- **Avatar Size**: 32px × 32px (with 4px white border)
- **Spacing**: 10px между аватарами
- **Counter Avatar**:
  - Background: #D9DDE2
  - Text: "1k" (10px Semibold White, centered)
  - Border: 4px White
- **Layout**: Horizontal Row
- **Использование**: Показ участников, лайков, просмотров

#### Avatar with Info

Крупный аватар с текстовой информацией.

- **Avatar Size**: 40px × 40px
- **Border Radius**: 40px (круг)
- **Spacing**: 6px между аватаром и текстом
- **Text Layout**:
  - Name: 13px Semibold Black (#09101D)
  - Role/Subtitle: 12px Regular Dark Gray (#373940)
- **Использование**: Автор видео, профили пользователей

#### Color Selector

Цветовые круги для выбора цвета товара.

- **Size**: 24px × 24px (inner: 14.4px × 14.4px)
- **Padding**: 6px
- **Border**: 2px solid White
- **Border Radius**: 20px (круг)
- **Colors**: Различные (black #09101D, cyan #7CC5D6, etc.)
- **Spacing**: Нет gap (плотное размещение)
- **Использование**: Выбор цвета в карточках товаров

#### Favorite Button

Кнопка "избранное" для карточек.

- **Size**: 30px × 30px
- **Padding**: 8px
- **Background**: White
- **Border Radius**: 100px (круг)
- **Icon**: 14px × 14px (heart icon)
- **Position**: Top-left corner карточки с padding 10px
- **Использование**: Добавление в избранное

#### Video Stats Badge

Бейдж с информацией о видео (продолжительность, просмотры).

- **Height**: 24px
- **Padding**: left 5px, right 10px
- **Background**: rgba(0, 0, 0, 0.30) - черный с 30% прозрачностью
- **Border Radius**: 10px (radius-mobile-sm)
- **Icon**: 24px × 24px (padding 8px)
- **Text**: 11px Semibold White
- **Spacing**: Иконка + текст в ряд
- **Варианты**:
  - Duration: Clock icon + "2:12"
  - Views: Eye icon + "1.342"
- **Position**: Top corners на изображении видео
- **Использование**: Метаданные видео

---

### 17. Hero Image Carousel (Flutter)

Система каруселей для hero-изображений с различными форматами и аспект-рацио.

#### Carousel Container (Mobile)

Основной контейнер для карусели изображений.

- **Width**: 375px (full mobile width)
- **Padding**: symmetric(vertical: 10px)
- **Border Radius**: 30px (для внутренних элементов)
- **Image Background**: #F4F6F9 (color-background-light)
- **Spacing**:
  - Между изображениями: 10px horizontal
  - Вертикальный padding: 10px
- **Layout**: Horizontal scroll с Row, spacing: 10px
- **Clip Behavior**: antiAlias

#### Hero Image Formats

Различные форматы изображений для разных типов контента.

##### Portrait Format (3:4 Ratio)

Вертикальный формат для портретных изображений.

- **Image Size**: 327×450px
- **Container**: 375px width, 470px height
- **Aspect Ratio**: 0.727 (3:4 portrait)
- **Использование**: Fashion lookbooks, портреты, вертикальный контент

##### Square Format

Квадратный формат для универсального контента.

- **Варианты размеров**:
  - **Standard**: 327×330px (с left padding)
  - **Full Width**: 375×330px (на всю ширину)
  - **With Padding**: 343×330px (с 16px horizontal padding)
- **Container**: 375px width, 350px height
- **Aspect Ratio**: ~1.0 (квадрат)
- **Использование**: Продуктовые фото, посты в социальных сетях

##### Landscape Format (16:9 Ratio)

Горизонтальный формат для широких изображений.

- **Варианты размеров**:
  - **Standard**: 327×240px (с left padding)
  - **Full Width**: 375×240px (на всю ширину)
  - **With Padding**: 343×240px (с 16px horizontal padding)
- **Container**: 375px width, 260px height
- **Aspect Ratio**: ~1.56 (16:9 landscape)
- **Использование**: Видео-превью, панорамы, широкоформатный контент

#### Pagination Dots

Индикаторы текущей позиции в карусели.

- **Dot Size**: 8×8px (OvalBorder - круги)
- **Spacing**: 16px между центрами точек (8px gap)
- **Container**: 56px width, 8px height (для 4 точек)
- **Colors**:
  - **Active**: #181920 (темный)
  - **Inactive**: #FAFAFB (светлый)
- **Position**: Bottom center карусели
- **Padding**:
  - Top: 10px
  - Horizontal: 16px
  - Bottom: 20px (portrait), 15px (landscape)
- **Layout**: Row с фиксированными позициями (left: 0, 16, 32, 48)

#### Desktop Layout Container

Контейнер для desktop версии с несколькими каруселями.

- **Width**: 2315px
- **Padding**: 50px
- **Border**: 1px solid #7B61FF (accent-purple)
- **Border Radius**: 15px
- **Background**: White
- **Spacing**: 100px между carousel секциями
- **Layout**: Row с mainAxisAlignment: spaceBetween

**Использование**: Hero секции на главной, image galleries, продуктовые слайдеры

---

### 18. Card Patterns (Flutter)

Полноценные паттерны карточек для различных типов контента.

#### Product Card with Discount (230px width)

Карточка товара со скидкой и социальными индикаторами.

**Структура:**
- **Container**: Width: 230px, spacing: 5px между секциями
- **Discount Badge Section** (spacing: 10px horizontal):
  - Discount Badge: 70px wide, #FFC043 background, 10px border-radius
  - Price Text: $26.99 (14px Regular Black)
  - Old Price: $35.99 (14px Regular, #D9DDE2, strikethrough) - spacing 10px
- **Product Image**: 230×230px, border-radius 15px
- **Content Section** (padding: 5px horizontal and 10px bottom, spacing: 5px):
  - Avatar Group: 5 avatars (32×32 with 4px white border), spacing 10px, последний показывает "1k"
  - Title: 18px Bold Black, 220px max-width
  - CTA Button: "BUY ON ALIEXPRESS"
    - Height: 36px
    - Padding: 16px horizontal, 10px vertical
    - Background: #FFC043
    - Text: 13px Semibold Black
    - Border Radius: 15px
    - Icon: 16×16 (spacing 8px)

**Использование**: E-commerce карточки с социальным proof, акционные товары

#### Blog Card (230px width)

Карточка блог-поста с категорией и метаданными.

**Структура:**
- **Container**: Width: 230px, Height: 370px, border-radius 16px
- **Image**: 230×230px, border-radius 15px
- **Content Section** (padding: 5px, spacing: 5px):
  - Category Badge:
    - Avatar: 32×32 with 10px border-radius (or 24×24 image inside)
    - Label: "Landscape design" (13px Semibold Black)
    - Spacing: 5px между аватаром и текстом
  - Title: 16px Bold Black, 220px max-width
  - Metadata Row (spacing: 10px):
    - Date: Icon 24×24 + "31 July" (13px Regular #747B84)
    - Reading Time: Icon 24×24 + "15 min to read" (13px Regular #747B84)

**Использование**: Блог-посты, статьи, образовательный контент

#### Product Card Vertical - Variant A (170px width)

Компактная вертикальная карточка товара (Nike shoes).

**Структура:**
- **Container**: Width: 170px, Height: 360px, border-radius 15px
- **Image Section**: 170×253px, border-radius 5px
  - Favorite Button: 30×30px circle, white background, top-left 10px padding
  - Status Badge: Bottom-left 5px padding
    - "🔥 New": 9px Semibold White, #09101D background, 5px border-radius
    - Padding: 5px horizontal, 3px vertical
- **Content Section** (padding: 10px top, 5px left, 10px right/bottom, spacing: 5px):
  - Rating: "👌 4.8 (130)" (13px, rating Semibold, count Regular #747B84)
  - Details (spacing: 4px):
    - Price: "$350" (14px Semibold Black)
    - Brand: "Nike 👟" (14px, "Nike" Semibold, emoji Regular)
    - Sizes: "36 ・ 37・ 38・ 39" (13px Regular #747B84)
    - Spacing: 2px между price и brand

**Использование**: Product listings, узкие сетки товаров

#### Product Card Vertical - Variant B (170px width)

Компактная вертикальная карточка товара с выбором цвета (H&M).

**Структура:**
- **Container**: Width: 170px, Height: 380px, border-radius 15px
- **Image Section**: 170×259px, border-radius 5px, spacing 192px между элементами
  - Favorite Button: top-left (30×30px circle)
  - Eco Badge: Bottom-left 5px padding
    - "Join Life": 9px Semibold White, #11BB8D background, 5px border-radius
- **Content Section** (padding: 5px top, 10px right/bottom):
  - Color Selector: 2 circles (24×24, 2px white border, colors: #09101D, #7CC5D6)
  - Product Name: "CONTRAST PRINT T-SHIRT" (14px Regular #414249)
  - Details (spacing: 2px):
    - Price: "USD 30" (14px Semibold Black)
    - Brand: "H&M" (14px Semibold Black)

**Использование**: Fashion товары с вариантами цветов

#### Video Card (230px width)

Карточка видео с автором и статистикой.

**Структура:**
- **Container**: Width: 230px, Height: 400px, border-radius 16px
- **Video Thumbnail**: 230×230px, border-radius 15px
  - Video Stats Badges (top corners, padding 10px, spacing 90px between):
    - Duration Badge: "2:12" (11px Semibold White, black 30% opacity, 10px border-radius)
    - Views Badge: "1.342" (same style)
    - Badge structure: Icon 24×24 + text, left padding 5px, right padding 10px
- **Content Section** (padding: 5px, spacing: 5px):
  - Avatar Group: 5 avatars (32×32), последний "1k"
  - Title: "Home fitness program, 2 minutes per day" (16px Bold Black, 220px max-width)
  - Author Section (spacing: 6px):
    - Avatar: 40×40px, border-radius 40px
    - Info:
      - Name: "Nicole Dowson" (13px Semibold Black)
      - Role: "Fitness App Team" (12px Regular #373940)

**Использование**: Видео-контент, уроки, туториалы

---

### 19. Chart & Graph Components (Flutter)

Компоненты для построения графиков и визуализаций данных.

#### Grid Line (Vertical)

Вертикальная линия сетки графика.

- **Width**: 1px
- **Color**: #A4ABB3 (chart-grid) - основная сетка
- **Transform**: rotateZ(-1.57) - поворот на 90° для вертикальной ориентации
- **Height**: 346px (или по высоте графика)
- **Stroke Align**: Center
- **Использование**: Вертикальные линии сетки на графиках

#### Grid Line (Horizontal)

Горизонтальная линия сетки графика.

- **Width**: 1px
- **Color**: #747B84 (chart-axis) - для основных делений
- **Stroke Align**: Center
- **Использование**: Горизонтальные линии сетки, основные деления

#### Axis Line (Thin)

Тонкая линия для вспомогательных делений.

- **Width**: 0.5px
- **Color**: #747B84 (chart-axis)
- **Stroke Align**: Center
- **Использование**: Вспомогательные деления, minor grid lines

#### Chart Label

Текстовая метка на графике.

**Варианты размеров:**
- **Small**: 8px Bold, padding horizontal 5px (optional)
- **Medium**: 10px Semibold, padding horizontal 5px

**Общие характеристики:**
- **Border Radius**: 10px
- **Text Align**: Center
- **Color**: #09101D (black)
- **Line Height**: 1.40
- **Spacing**: 1px между строками (если многострочный)

**Позиционирование:**
- **Bottom**: Под осью X с spacing 5px
- **Left**: Слева от оси Y
- **Right**: Справа от оси Y
- **Top**: Над графиком

**Использование**: Метки значений на осях графиков, легенда

#### Chart Container

Контейнер для графика.

- **Height**: 446px (стандартная высота)
- **Padding**: 50px
- **Border**: 1px solid #7B61FF (accent-purple) - для демо
- **Border Radius**: 15px
- **Spacing**:
  - Между элементами: 50px, 20px, 10px
  - Внутри labels: 5px

**Варианты layout:**
- **Horizontal Grid**: Row layout с вертикальными линиями
- **Vertical Grid**: Column layout с горизонтальными линиями
- **Combined**: Grid с обеими осями

**Использование**: Контейнер для размещения графиков и chart elements

---

### 20. Special Effects

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

**Текущая версия**: v5.6.0

### Changelog

#### v5.6.0 (2025-11-19)
- 🖼️ Добавлена **полная система Hero Image Carousel**
- 🎨 Новые цвета для pagination индикаторов:
  - Pagination Active (#181920) - темный для активной точки
  - Pagination Inactive (#FAFAFB) - светлый для неактивных точек
- 📐 Добавлена новая секция **Hero Image Carousel (Flutter)** с тремя форматами:
  - **Portrait Format** (3:4 ratio) - 327×450px
    - Container: 375px width, 470px height
    - Использование: Fashion lookbooks, портреты
  - **Square Format** (~1:1 ratio)
    - Варианты: 327×330px, 375×330px (full width), 343×330px (with padding)
    - Container: 375px width, 350px height
    - Использование: Продуктовые фото, социальные посты
  - **Landscape Format** (16:9 ratio)
    - Варианты: 327×240px, 375×240px, 343×240px (with padding)
    - Container: 375px width, 260px height
    - Использование: Видео-превью, панорамы
- 🎯 Добавлены **Pagination Dots спецификации**:
  - Dot Size: 8×8px круги
  - Spacing: 16px между центрами (8px gap)
  - Container: 56px width для 4 точек
  - Colors: #181920 (active), #FAFAFB (inactive)
  - Position: Bottom center с padding 10/20px
- 🖥️ Добавлен **Desktop Layout Container**:
  - Width: 2315px, Padding: 50px
  - Border: 1px solid #7B61FF
  - Spacing: 100px между секциями
- 📊 Все данные извлечены из реального Flutter кода hero image системы

#### v5.5.0 (2025-11-19)
- 🏷️ Добавлена **полная система Badge Components**
- 📝 Добавлен новый текстовый стиль **Page Title (Hero)**:
  - Font Size: 72px
  - Font Weight: Extrabold (800)
  - Line Height: 0.70
  - Цвет: #09101D (черный)
- 🎨 Новая секция **Badge System (Complete)** с 7 вариантами бейджей:
  - **Text Badge** (16px height, 12px border-radius)
    - Padding: 4px horizontal, 2px vertical
    - Background: Primary Blue (#4141E6)
    - Text: 10px Semibold White
  - **Time Badge** (16px height, 4px border-radius)
    - Формат времени: "35:12"
    - Background: Overlay Black 30%
    - Text: 10px Semibold White
  - **Counter Badge** (20px height, pill shape)
    - Padding: 4px horizontal, 2px vertical
    - Border Radius: 20px
    - Background: Red Accent (#E24949)
    - Text: 12px Semibold White ("11" формат)
  - **Notification Dot with Icon** (14×14px)
    - Background: Primary Blue (#4141E6)
    - Иконка: белая, размер 10px
  - **Status Dot - Primary** (12×12px)
    - Background: Primary Blue (#4141E6)
    - Border: 2px solid White
    - Используется для индикации статуса "активно"
  - **Status Dot - Success** (12×12px)
    - Background: Green Badge (#11BB8D)
    - Border: 2px solid White
    - Используется для положительного статуса
  - **Status Dot - Error** (12×12px)
    - Background: Red Accent (#E24949)
    - Border: 2px solid White
    - Используется для ошибок и предупреждений
- 📊 Все данные извлечены из реального Flutter кода badge системы

#### v5.4.0 (2025-11-19)
- 📊 Добавлена **система для графиков и визуализаций данных**
- 🎨 Новые цвета для графиков:
  - Chart Grid (#A4ABB3) - светло-серый для grid lines
  - Chart Axis (#747B84) - для осей и основных делений
- 📝 Добавлены **текстовые стили для chart labels**:
  - Chart Label Small (8px Bold) - маленькие метки
  - Chart Label Medium (10px Semibold) - стандартные метки
- 📐 Добавлены **спецификации линий**:
  - Grid Line 1px (#A4ABB3) - основная сетка
  - Axis Line 0.5px (#747B84) - вспомогательные деления
- 📈 Новая секция **Chart & Graph Components**:
  - **Grid Line (Vertical)** - 1px, transform rotateZ(-1.57)
  - **Grid Line (Horizontal)** - 1px для основных делений
  - **Axis Line (Thin)** - 0.5px для вспомогательных делений
  - **Chart Label** - два размера (8px, 10px) с различным позиционированием
  - **Chart Container** - 446px height, spacing 50/20/10px
- 🎯 Все данные извлечены из реального Flutter кода элементов графиков

#### v5.3.0 (2025-11-19)
- 🎨 Добавлены **новые цвета** для карточек и контента:
  - Yellow Accent (#FFC043) - скидки, CTA кнопки
  - Green Badge (#11BB8D) - эко-бейджи
  - Cyan Light (#7CC5D6) - цветовые селекторы
  - Red Accent (#E24949)
  - Текстовые цвета: Tertiary (#747B84), Quaternary (#414249), Dark Gray (#373940)
  - Overlay Black 30%
- 📝 Добавлены **новые текстовые стили**:
  - Micro Text (9px) - для бейджей
  - Mini Text (10px) - для счетчиков аватаров
  - Video Badge Text (11px)
  - Metadata Text (13px)
  - Card Title Medium (16px) и Large (18px)
- 📐 Добавлены **размеры карточек и элементов**:
  - Card widths: 170px, 230px
  - Avatar sizes: 24px, 32px, 40px
  - Icon sizes: 16px, 24px, 30px
- 🔄 Обновлены **border radius** значения: добавлен 5px и 40px
- 🎭 Добавлены **вспомогательные компоненты**:
  - Badge (Status/Label) - статусные бейджи
  - Discount Badge - бейдж со скидкой
  - Avatar (Small) - маленький аватар
  - Avatar Group - группа аватаров с счетчиком
  - Avatar with Info - аватар с текстом
  - Color Selector - выбор цвета товара
  - Favorite Button - кнопка избранного
  - Video Stats Badge - бейдж с метаданными видео
- 📦 Добавлена новая секция **Card Patterns** с полноценными паттернами карточек:
  - **Product Card with Discount** (230px) - товар со скидкой и социальными индикаторами
  - **Blog Card** (230px) - блог-пост с категорией и метаданными
  - **Product Card Vertical - Variant A** (170px) - компактная карточка товара (Nike)
  - **Product Card Vertical - Variant B** (170px) - карточка товара с выбором цвета (H&M)
  - **Video Card** (230px) - видео с автором и статистикой
- 📊 Все данные извлечены из реального Flutter кода готовых дизайн-макетов

#### v5.2.0 (2025-11-19)
- 🔘 Добавлены **спецификации мобильных кнопок** из Flutter кода
- 🎨 Новый цвет: Background Light (#F4F6F9) для inactive кнопок
- 📝 Добавлен **Button Text Style** (13px, Semibold, line-height 1.40)
- 📱 Новые мобильные компоненты:
  - **Button (Mobile)** с Primary и Secondary вариантами
    - Height: 36px
    - Padding: 16px horizontal, 10px vertical
    - Border Radius: 15px
    - Text: 13px Semibold
  - **iOS Home Indicator** (134×5px, pill shape)
    - Контейнер: 34px height
    - Цвета: White/Black в зависимости от фона
- 🔄 Все данные извлечены из реального Flutter кода кнопочных компонентов

#### v5.1.0 (2025-11-19)
- ✨ Добавлены **реальные данные из Flutter мобильного приложения**
- 🎨 Дополнена цветовая палитра:
  - Primary Blue (#4141E6)
  - Accent Purple (#7B61FF)
  - Scaffold Dark (#12202F)
  - UI Gray Light (#D9DDE2)
  - Overlay colors с alpha-каналами
- 📝 Добавлены **Flutter Mobile Text Styles** с реальными размерами (11px, 12px, 14px, 16px)
- 📐 Добавлены **Flutter Mobile Spacing** values (padding, gap, mobile dimensions)
- 🔄 Добавлены **Flutter Mobile Border Radius** (10px, 15px, 30px, 100px)
- 📱 Добавлена новая секция **Mobile Components (Flutter)**:
  - Info Bar
  - Bottom Sheet с Handle индикатором
  - Notification Card
  - Container with Border
  - Divider / Separator Bar
  - Mobile Screen Container (375×812px)
- 📊 Все данные извлечены из реального Flutter кода приложения

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
