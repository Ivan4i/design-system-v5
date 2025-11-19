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
--color-info-blue: #0B24FB;        /* Color(0xFF0B24FB) - синий для secondary info */
--color-link-blue: #2E5AAC;        /* Color(0xFF2E5AAC) - синий для ссылок и подчеркиваний */
```

### UI Colors

```css
/* UI элементы из Flutter кода */
--color-gray-light: #D9DDE2;       /* Color(0xFFD9DDE2) - светло-серый для разделителей */
--color-gray-lighter: #EAEEF2;     /* Color(0xFFEAEEF2) - очень светло-серый для inactive steps */
--color-background-light: #F4F6F9; /* Color(0xFFF4F6F9) - светлый фон для inactive кнопок */
--color-input-background: #FAFAFB; /* Color(0xFFFAFAFB) - очень светлый фон для input полей */

/* Цвета для карточек и контента */
--color-yellow-accent: #FFC043;    /* Color(0xFFFFC043) - желтый для скидок, CTA кнопок */
--color-green-badge: #11BB8D;      /* Color(0xFF11BB8D) - зеленый для эко-бейджей */
--color-cyan-light: #7CC5D6;       /* Color(0xFF7CC5D6) - голубой для цветовых селекторов */
--color-red-accent: #E24949;       /* Color(0xFFE24949) - красный акцент */
--color-red-validation: #DA1414;   /* Color(0xFFDA1414) - красный для validation errors */

/* Validation background colors с прозрачностью */
--color-positive-bg: rgba(17, 187, 141, 0.05);  /* Color(0x0C11BB8D) - светло-зеленый для positive state */
--color-negative-bg: rgba(218, 20, 20, 0.05);   /* Color(0x0CDA1414) - светло-красный для negative state */

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

#### Progress Stepper / Track Bar

Индикатор прогресса с шагами для multi-step процессов (оформление заказа, регистрация).

- **Container**:
  - Width: 375px (full mobile width)
  - Padding: left 32px, right 32px, bottom 10px
  - Vertical padding: 5px
  - Row height: 30px
- **Border Radius**: 10px для основного контейнера
- **Spacing между элементами**: 3px (между step indicators и progress lines)

##### Step Indicator (Active)

Активный текущий шаг.

- **Outer Circle**: 18×18px
  - Background: #09101D (black)
  - Shape: OvalBorder (круг)
- **Inner Circle**: 14×14px
  - Background: #09101D (black)
  - Border: 1px solid White
  - Position: 2px from outer edge
- **Label**: Positioned at top: 21px from outer circle
- **Использование**: Текущий активный шаг

##### Step Indicator (Inactive)

Неактивный будущий шаг.

- **Size**: 14×14px
- **Background**: #EAEEF2 (очень светло-серый)
- **Shape**: OvalBorder (круг)
- **Padding**: top 2px
- **Label Spacing**: 5px между кружком и текстом
- **Использование**: Будущие шаги, еще не достигнутые

##### Step Indicator (Completed)

Завершенный шаг с иконкой.

- **Container**: 18×18px
  - Padding top: 0.5px
  - Border radius: 3px
- **Icon**: 17×17px (checkmark/галочка)
  - clipBehavior: Clip.antiAlias
- **Label Spacing**: 3px между иконкой и текстом
- **Использование**: Пройденные шаги

##### Progress Line

Линия между шагами.

- **Height**: 4px
- **Background**: #F4F6F9 (color-background-light)
- **Border Radius**: 10px
- **Layout**: Expanded (заполняет доступное пространство между steps)
- **Использование**: Визуальная связь между шагами

##### Step Labels

Подписи шагов.

- **Font**: 10px Archivo
- **Weight**: 600 (Semibold)
- **Color**: #09101D (black)
- **Text Align**: Center
- **Line Height**: 1.40
- **Position**: Below step indicators
- **Примеры текстов**: "Shipping", "Payment", "Review"

**Состояния прогресса:**
- **State 1**: Step 1 active, Steps 2-3 inactive
- **State 2**: Step 1 completed (icon), Step 2 active, Step 3 inactive
- **State 3**: Steps 1-2 completed (icons), Step 3 active

**Использование**: Checkout flow, multi-step forms, онбординг, регистрация

#### Password Input Field

Полноценный input field для ввода пароля с validation states и show/hide функционалом.

##### Field Container

- **Width**: 375px (full mobile width)
- **Container Padding**: symmetric(horizontal: 16px, vertical: 5px)
- **Spacing**: 8px между label, input и helper text

##### Label

- **Font**: 14px Archivo
- **Weight**: 600 (Semibold)
- **Color**: #09101D (black) или #D9DDE2 (disabled)
- **Line Height**: 1.40
- **Width**: 343px
- **Spacing**: 13px справа

##### Input Field Specs

**Размеры:**
- **Width**: 343px (100% of container minus padding)
- **Height**: 36px
- **Padding**: left 16px, right 20px
- **Border Radius**: 15px

**Typography:**
- **Font**: 14px Archivo для текста, 24px для dots
- **Weight**: 400 (Regular)
- **Line Height**: 1.40
- **Text Align**: Left

**Cursor:**
- **Width**: 2px
- **Height**: 16px
- **Spacing**: 15px от текста

**Icons:**
- **Size**: 20×20px
- **Spacing**: 20px между иконками
- **Position**: Right-aligned внутри поля

##### Field States

**1. Enabled (Default)**
- Background: #F4F6F9 (background-light)
- Border: None
- Placeholder: "Create a password…" (#747B84)
- Helper text: "Helper" (#747B84)

**2. Focus**
- Background: #F4F6F9
- Border: 2px solid #09101D (black)
- Placeholder: "Create a password…" (#747B84)
- Icons: Eye icon visible (20×20px)

**3. Pressed**
- Background: #EAEEF2 (gray-lighter)
- Border: None
- Placeholder: "Create a password…" (#747B84)

**4. Active - Typing - Show**
- Background: #F4F6F9
- Border: None
- Text: "CaTsSayMeoW!23" (#09101D, 14px)
- Icons: 2 icons (eye-off + icon)
- Cursor: visible (2px, 16px)

**5. Active - Typing - Hide**
- Background: #F4F6F9
- Border: None
- Text: "••••••••••••••••••••" (#09101D, 24px - larger dots)
- Icons: 2 icons (eye + icon)
- Cursor: visible after dots

**6. Complete - Hide**
- Background: #F4F6F9
- Border: None
- Text: "••••••••••••••••••••" (#09101D, 24px)
- Icons: 1 icon (eye)

**7. Incomplete**
- Background: #F4F6F9
- Border: None
- Placeholder: "Create a password…" (#747B84)
- Icons: 1 icon (eye)

**8. Positive - Show**
- Background: rgba(17, 187, 141, 0.05) - light green
- Border: 2px solid #11BB8D (green-badge)
- Text: "CaTsSayMeoW!23" (#09101D, 14px)
- Icons: 2 icons (eye-off + checkmark)
- Cursor: visible
- Helper: "Helper" (#747B84)

**9. Positive - Hide**
- Background: rgba(17, 187, 141, 0.05)
- Border: 2px solid #11BB8D
- Text: "••••••••••••••••••••" (#09101D, 24px)
- Icons: 2 icons (eye + checkmark)
- Cursor: visible

**10. Negative - Show**
- Background: rgba(218, 20, 20, 0.05) - light red
- Border: 2px solid #DA1414 (red-validation)
- Text: "CaTsSay" (#09101D, 14px)
- Icons: 2 icons (eye-off + error)
- Cursor: visible
- Helper: "You need to use "A, a, !, 1" symbols" (#E24949 red)

**11. Negative - Hide**
- Background: rgba(218, 20, 20, 0.05)
- Border: 2px solid #DA1414
- Text: "••••••••••••••" (#09101D, 24px)
- Icons: 2 icons (eye + error)
- Cursor: visible
- Helper: "You need to use "A, a, !, 1" symbols" (#E24949)

**12. Disabled - Show/Hide**
- Background: #F4F6F9
- Border: None
- Text: "WoOfLikEaDOg345" or dots (#D9DDE2 gray)
- Label: #D9DDE2
- Helper: #D9DDE2
- Icons: 1 icon disabled state

##### Password Masking

**Visible mode:**
- Text: 14px Regular, normal characters
- Example: "CaTsSayMeoW!23"

**Hidden mode:**
- Text: 24px, bullet points "•"
- Each character replaced with "•"
- Example: "••••••••••••••••••••"

##### Helper Text

- **Font**: 14px Archivo
- **Weight**: 400 (Regular)
- **Line Height**: 1.40
- **Width**: 343px
- **Colors**:
  - Default: #747B84 (tertiary)
  - Error: #E24949 (red-accent)
  - Disabled: #D9DDE2 (gray-light)

**Использование**: Password fields, authentication forms, registration, security settings

#### Text Input Field

Универсальный компонент text input с различными вариантами использования (email, username, search, amount).

##### Base Specs

**Dimensions:**
- **Container Width**: 375px (full mobile width)
- **Container Padding**: symmetric(horizontal: 16px, vertical: 10px)
- **Input Height**: 44px (base) или 46px (с helper text)
- **Border**: 2px solid #4141E6 (primary-blue) - focus state
- **Border Radius**: 15px
- **Internal Padding**: top 4px, left 20px, right 15px, bottom 4px

**Typography:**
- **Placeholder**: 12px Regular #747B84 (tertiary)
- **Input Text**: 14px Semibold #09101D (black)
- **Label**: 14px Semibold #09101D
- **Helper Text**: 12px Regular
  - Success: #11BB8D (green-badge)
  - Error: #E24949 (red-accent)
- **Secondary Info**: 10px Semibold
  - Default: #09101D
  - Accent: #0B24FB (info-blue)

**Cursor:**
- Character: "|" (pipe)
- Color: #09101D (black)
- Font: 12px Regular
- Position: before placeholder или after text

**Spacing:**
- Between elements: 5px vertical
- Label to input: 5px
- Input to helper: 5px
- Icon spacing: 8px, 10px between elements

##### Field Variants

**1. Basic Input with Cursor**
- Border: 2px solid #4141E6
- Placeholder: "|Your email" (cursor + placeholder)
- Cursor visible before placeholder text
- No icons, no helper

**2. Input with Positive Validation**
- Border: 2px solid #4141E6
- Placeholder: "|First name"
- Helper Bottom: "Name is correct 👌" (#11BB8D green)
- Emoji: 👌 (14px, #11BB8D)
- Helper padding: horizontal 10px

**3. Input with Top Label & Balance Info**
- Top Label Row:
  - Left: "From" (14px Semibold #09101D), width 189px
  - Right: "Balance: 1.01 ETH" (10px Semibold #09101D) + "~4.043$" (#0B24FB info-blue)
  - Spacing: 10px между balance и price
- Border: 2px solid #4141E6
- Placeholder: "|Enter amount"
- Top label padding: horizontal 10px

**4. Input with Right Icon**
- Border: 2px solid #4141E6
- Placeholder: "|Location" (width 276px)
- Right Icon: 24×24px (2px padding, 100px border-radius container)
- Spacing: 8px text to icon

**5. Input with Left Icon**
- Left Icon: 24×24px (2px padding, 100px border-radius)
- Placeholder: "|Search" (width 274px)
- Icon-to-text spacing: 10px

**6. Input with Avatar & Delete Button**
- Left Avatar: 30×30px circle
  - Background: #F4F6F9 за placeholder image
  - Image: NetworkImage, OvalBorder
  - Icon overlay: 16×16px centered
- Text: "Helen Smith|" (#747B84 placeholder + cursor)
- Width: 236px для текста
- Right Delete Button:
  - Container: 24×24px, #F4F6F9 background
  - Border radius: 10px
  - Icon: 24×24px (2px padding)
- Spacing: 10px avatar to text, 8px текста к кнопке

**7. Filled Input (Email)**
- Border: 2px solid #4141E6
- Text: "you@awesome.com" (14px Semibold #09101D)
- Width: 308px для текста
- No placeholder, no cursor (filled state)
- Container height: 44px

**8. Input with Negative Validation**
- Border: 2px solid #4141E6
- Text: "@johnsmith" (14px Semibold #09101D)
- Helper Bottom: "Username already taken" (#E24949 red-accent)
- Helper padding: horizontal 10px
- Helper width: 323px
- Container height: 46px (с helper)

##### Icons & Avatars

**Icons:**
- **Size**: 24×24px standard
- **Container**: 2px padding, border-radius 100px
- **Position**: Left или right внутри input
- **Spacing**: 8-10px от текста

**Avatars:**
- **Size**: 30×30px circle
- **Shape**: OvalBorder
- **Background**: #F4F6F9 (placeholder)
- **Image**: NetworkImage, fit: cover
- **Icon overlay**: 16×16px centered

**Delete/Action Buttons:**
- **Container**: 24×24px
- **Background**: #F4F6F9
- **Border radius**: 10px
- **Icon**: 24×24px (2px padding)

##### Helper Text Layout

**Success Helper:**
- Color: #11BB8D (green-badge)
- Text: left-aligned, width 309px
- Emoji: right-aligned, spacing 13px, optional 👌
- Padding: horizontal 10px
- Font: 12px Regular

**Error Helper:**
- Color: #E24949 (red-accent)
- Text: left-aligned, full width (323px)
- Padding: horizontal 10px
- Font: 12px Regular

##### Top Label with Info

**Structure:**
- Container padding: horizontal 10px
- Row layout: spaceBetween
- Alignment: end (bottom-aligned)

**Left Section:**
- Label: 14px Semibold #09101D
- Width: 189px

**Right Section:**
- Primary info: 10px Semibold #09101D (e.g., "Balance: 1.01 ETH")
- Secondary info: 10px Semibold #0B24FB (e.g., "~4.043$")
- Spacing: 10px между элементами
- Row layout: spacing 10px

**Использование**: Email inputs, username fields, search bars, amount inputs, location pickers, contact selectors, authentication forms

#### Toggle Switch

Переключатель вкл/выкл для настроек и preferences.

**Dimensions:**
- **Container Width**: 51px
- **Container Height**: 31px
- **Border Radius**: 40px (pill shape)

**Toggle Circle:**
- **Size**: 31×31px
- **Border**: 2px solid (matches background color)
- **Border Radius**: 40px (полный круг)
- **Background**: White

**States:**

**Active (On):**
- Background: #11BB8D (green-badge)
- Circle position: Right-aligned
- Circle border: 2px solid #11BB8D

**Inactive (Off):**
- Background: #D9DDE2 (gray-light) или #EAEEF2 (gray-lighter)
- Circle position: Left-aligned
- Circle border: 2px solid background color

**Usage with Label:**
- Layout: Row with spaceBetween
- Label: 12px Medium #09101D
- Spacing: Auto (spaceBetween pushes switch to right)
- Container padding: horizontal 16px, vertical 10px

**Animation:**
- Transition: Circle slides from left to right (или наоборот)
- Duration: ~200-300ms
- Easing: ease-in-out

**Accessibility:**
- Tap target: Full 51×31px area
- Visual feedback: Circle moves immediately
- Color contrast: Meets WCAG AA standards

**Использование**: Settings toggles, feature flags, remember me checkboxes, preferences, notifications on/off

#### Floating Action Button

Круглая плавающая кнопка для быстрых действий (share, favorite, download, etc).

**Dimensions:**
- **Container Size**: 44×44px
- **Border Radius**: 30px (circular)
- **Padding**: 14px (all sides)
- **Icon Size**: 16×16px (44px - 14px×2)

**Visual Style:**
- **Background**: #FFFFFF (white)
- **Shadow**: BoxShadow
  - Color: rgba(0, 0, 0, 0.3)
  - Blur Radius: 10px
  - Offset: (0, 2)

**Icon:**
- Size: 16×16px (centered)
- Color: Usually #09101D (text-primary) or themed color
- Padding: 14px around icon создает touch target 44×44px

**Usage:**
- Action buttons в gallery blocks (share, favorite, download, info)
- Floating quick actions над контентом
- Row/Grid arrangements: spacing 10-16px between buttons
- Usually appears in groups of 2-6 buttons

**Typical Actions:**
- Share (share icon)
- Favorite/Like (heart icon)
- Download (download icon)
- Info (info icon)
- Edit (edit/pencil icon)
- Delete (trash icon)

**Interaction:**
- Tap target: Full 44×44px
- Hover state: Может добавляться тень побольше
- Active state: Scale down slightly (0.95)

**Accessibility:**
- Minimum touch target: 44×44px ✓
- High contrast: White button с тенью хорошо видна на любом фоне
- Icon должна быть понятной (standard iconography)

**Использование**: Gallery actions, quick share buttons, floating toolbars, card actions, media controls

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

<!-- AI_COMPONENT: RatingComponents -->
### 21. Rating Components {#rating-components}

**[Component Category: Rating & Reviews]**

Компоненты для отображения рейтингов, отзывов и оценок качества.

#### Rating Progress Bar

**[Component: RatingProgressBar]** - Segmented horizontal progress bar для детального отображения рейтинга (используется в reviews, ratings breakdown).

**Dimensions:**
- **Height**: 3px
- **Total Width**: ~234px (адаптивная, 6 segments по 39.08px)
- **Segments**: 6 (для 5-star rating из расчета 5 filled + 1 unfilled max)
- **Segment Width**: 39.08px each
- **Border Radius**: 10px (на концах - topLeft/bottomLeft для первого, topRight/bottomRight для последнего)

**Visual Style:**
- **Filled Segments**: #09101D (color-text-primary)
- **Unfilled Segments**: rgba(9, 16, 29, 0.1) или #1909101D (~10% opacity)
- **No Spacing**: Сегменты идут вплотную друг к другу

**Structure:**
```dart
Row(
  children: [
    // Filled segments (left-aligned)
    Container(width: 39.08, height: 3,
      decoration: ShapeDecoration(
        color: Color(0xFF09101D),
        shape: RoundedRectangleBorder(
          borderRadius: BorderRadius.only(
            topLeft: Radius.circular(10),
            bottomLeft: Radius.circular(10),
          ),
        ),
      ),
    ),
    // ... more filled segments (no border-radius)
    // Unfilled segment (right-aligned)
    Container(width: 39.08, height: 3,
      decoration: ShapeDecoration(
        color: Color(0x1909101D), // rgba(9,16,29,0.1)
        shape: RoundedRectangleBorder(
          borderRadius: BorderRadius.only(
            topRight: Radius.circular(10),
            bottomRight: Radius.circular(10),
          ),
        ),
      ),
    ),
  ]
)
```

**Calculation:**
- 5.0 rating = 6 filled segments (100%)
- 4.7 rating = 5 filled + partial (~83%)
- 4.5 rating = 5 filled + partial (~75%)
- Формула: `(rating / 5.0) * totalSegments`

**Layout with Label & Score:**
```
[Label]           [■■■■■■░] [Score]
Location          ▰▰▰▰▰▱    4.7
  (11px Regular)  (3px bar) (10px Semibold)
```

**Spacing:**
- Container padding: top 5.5px, left 5.5px, bottom 5.5px
- Right spacing: 5px между bar и score
- Row spacing: 15px между rating rows

**Typography (сопутствующая):**
- **Category Label** (left): 11px Regular #09101D
- **Score Value** (right): 10px Semibold #09101D

**Использование**: Rating breakdowns, category scores, review summaries, detailed ratings, quality metrics

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

## UI Blocks & Screen Patterns (Flutter)

Готовые UI блоки для мобильных экранов - комплексные паттерны, которые можно гибко адаптировать под конкретные нужды проекта.

> **Гибкость блоков**: Все блоки можно расширять/модифицировать. Например, если в блоке 2 input поля, но по backend требуется 3 - просто добавьте еще одно поле с теми же стилями.

### Start Screen Blocks

Блоки для onboarding, регистрации и welcome screens.

#### Start Screen - Onboarding

Стартовый экран с hero-текстом и призывом к действию.

**Dimensions:**
- Screen: 375×412px
- Border Radius: 30px (screen corners)
- Background: White

**Structure (top to bottom):**

1. **Gradient Overlay Section**
   - Gradient: `LinearGradient(begin: (0.50, 0.00), end: (0.50, 1.00))`
   - Colors: `[Colors.white.withValues(alpha: 0), Colors.white, Colors.white]`
   - Fade effect from transparent to solid white

2. **Logo/Image Section** (top padding: 60px, bottom: 10px)
   - Height: 80px
   - Border radius: 15px
   - Shadow: `BoxShadow(color: rgba(0, 0, 0, 0.1), blurRadius: 10, offset: (0, 2))`
   - Image: NetworkImage, fit: cover
   - Spacing below: 4px

3. **Hero Text Section** (padding: top 10px, horizontal 16px, bottom 20px)
   - Width: 343px
   - Text: Mixed style TextSpan
     - Regular part: 32px Bold #09101D "Get a rental car in "
     - Accent part: 32px Bold #7CC5D6 "15 minutes"
   - Text Align: Center
   - Line Height: 1.40
   - Spacing below: 20px

4. **CTA Buttons Section** (top: 10px spacing)

   **Primary Button:**
   - Width: 343px (full width minus padding)
   - Height: 44px
   - Background: #7CC5D6 (cyan-light)
   - Border Radius: 15px
   - Padding: horizontal 16px, vertical 10px
   - Text: "Sign up" (16px Semibold White)
   - Spacing below: 10px

   **Secondary Button:**
   - Width: 343px
   - Height: 44px
   - Background: Transparent
   - Border Radius: 15px
   - Padding: horizontal 16px, vertical 10px
   - Text: "Log in" (14px Semibold #09101D)

5. **iOS Home Indicator**
   - Width: 134px
   - Height: 5px
   - Background: #09101D (black)
   - Border Radius: 100px (pill shape)
   - Position: Center bottom (34px container height, positioned at top: 21px)

**Flexible elements:**
- Можно добавить больше кнопок (social login, etc.)
- Изменить hero text на любой другой
- Добавить subtitle под hero text
- Заменить logo section на другой content

**Usage:** Onboarding, welcome screens, app intro, marketing landing

---

#### Start Screen - Sign Up Form

Экран регистрации с формой ввода и toggle switch.

**Dimensions:**
- Screen: 375×496px
- Border Radius: 30px
- Background: White

**Structure (top to bottom):**

1. **Top Status Bar** (0-44px)
   - Height: 44px
   - Close button right-aligned:
     - Icon: 24×24px
     - Padding: horizontal 16px, vertical 10px

2. **Close Button Row** (44-88px)
   - Height: 44px
   - Right-aligned icon: 24×24px (2px padding, border-radius 100px)

3. **Page Title Section** (88-172px, padding: top 40px, horizontal 16px)
   - Title: "Create account"
     - Font: 32px Bold #09101D
     - Width: 343px
     - Line Height: 1.40

4. **Subtitle with Link** (172-218px, padding: top 5px, horizontal 16px, vertical 10px)
   - Text: Mixed style TextSpan
     - Regular: "Have an account? " (15px Regular #09101D)
     - Link: "Sign in" (15px Regular #2E5AAC, underlined)
   - Width: 343px

5. **Email Input Field** (218-320px, padding: top 20px)
   - Label: "Your email" (13px Semibold #09101D)
   - Input Container:
     - Width: 343px
     - Height: 46px
     - Background: #FAFAFB (input-background)
     - Border Radius: 15px
     - Padding: left 16px, right 20px
   - Placeholder: "|you@awesome.com" (16px Regular rgba(9, 16, 29, 0.2))
   - Cursor: 2×16px
   - Spacing: 8px (label to input)

6. **Toggle Switch Row** (320-372px, padding: top 5px, bottom 10px)
   - Container: horizontal 16px padding
   - Layout: Row with spaceBetween

   **Label (left):**
   - Text: "Remember sign in details"
   - Font: 12px Medium #09101D
   - Width: 292px

   **Toggle Switch (right):**
   - Container Width: 51px
   - Container Height: 31px
   - Background: #11BB8D (green, active state)
   - Border Radius: 40px (pill)
   - Toggle Circle:
     - Size: 31×31px
     - Background: White
     - Border: 2px solid #11BB8D
     - Border Radius: 40px
     - Position: Right-aligned (active)

7. **Primary Button** (372-436px, padding: vertical 10px, horizontal 16px)
   - Width: 343px
   - Height: 44px
   - Background: #09101D (black)
   - Border Radius: 15px
   - Padding: horizontal 16px, vertical 10px
   - Text: "Confirm & Continue" (14px Semibold White)
   - Inner padding: horizontal 10px

8. **Legal Footer Text** (436-496px, padding: top 10px, horizontal 16px, bottom 20px)
   - Width: 343px
   - Text: Mixed style TextSpan (11px Regular)
     - Regular: "By continuing, you agree to Appka's " (#747B84)
     - Link: "Privacy Policy" (11px Semibold #2E5AAC)
     - Regular: " and " (#747B84)
     - Link: "Terms of Service" (11px Semibold #2E5AAC)
   - Line Height: 1.40

**Flexible elements:**
- Добавить больше input полей (password, name, phone)
- Добавить social login buttons
- Изменить toggle на checkbox
- Добавить validation errors под inputs
- Добавить "Forgot password?" link

**Usage:** Sign up, registration, account creation, user onboarding

---

#### Start Screen - Gallery Preview

Экран с каруселью изображений (preview mode).

**Dimensions:**
- Screen: 375×488px
- Border Radius: 30px
- Background: White

**Structure:**

1. **Top Spacer** (0-44px)
   - Empty space for status bar

2. **Image Carousel** (44-424px, padding: vertical 20px)
   - Layout: Horizontal Row, spacing: 15px
   - Alignment: Center

   **Side Image (Left):**
   - Size: 143×310px
   - Border Radius: 15px
   - Image: NetworkImage, fit: cover
   - Clip: antiAlias

   **Center Image (Featured):**
   - Size: 166.5×360px
   - Border Radius: 15px
   - Image: NetworkImage, fit: contain (важно!)
   - Clip: antiAlias
   - Emphasis: Larger size для focus

   **Side Image (Right):**
   - Size: 143×310px
   - Border Radius: 15px
   - Image: NetworkImage, fit: cover
   - Clip: antiAlias

**Spacing:**
- Between images: 15px
- Vertical padding: 20px
- Side images aligned to center vertically

**Flexible elements:**
- Изменить количество images (2, 4, 5)
- Добавить pagination dots внизу
- Добавить swipe gesture indicators
- Изменить размеры под разные aspect ratios
- Добавить captions под images

**Usage:** Onboarding gallery, feature showcase, portfolio preview, image selection

---

#### Gallery Block with Action Buttons

Блок с сеткой изображений и плавающими action кнопками (share, like, save, etc).

**Dimensions:**
- Screen: 375×290px
- Border Radius: 30px
- Background: White

**Structure:**

1. **Gallery Grid** (padding: horizontal 16px, vertical 20px)

   **Layout:** 2 columns, spacing: 10px

   **Left Column:**
   - Image: 166.5×250px (full height)
   - Background: #F4F6F9 (placeholder)
   - Border Radius: 20px
   - Image fit: cover
   - Clip: antiAlias

   **Right Column:**
   - Layout: 2 images stacked, spacing: 10px
   - Each Image: 166.5×120px
   - Background: #F4F6F9 (placeholder)
   - Border Radius: 20px
   - Image fit: cover
   - Clip: antiAlias

2. **Floating Action Buttons Row** (positioned at top: 194px from container top)
   - Container Padding: top 10px, horizontal 32px, bottom 20px
   - Layout: Row (4 buttons)
   - Alignment: Center

   **Each Button:**
   - Outer Container Padding: 10px
   - Button Size: 44×44px
   - Background: White
   - Border Radius: 30px (круг)
   - Shadow: `BoxShadow(color: rgba(0, 0, 0, 0.3), blurRadius: 10, offset: (0, 2))`
   - Icon Padding: 14px (icon area 16×16px)
   - Icon Size: ~19px

   **Buttons можно использовать для:**
   - Share (поделиться)
   - Like/Favorite (избранное)
   - Save/Bookmark (сохранить)
   - Download (скачать)
   - Edit (редактировать)
   - More actions (меню)

**Shadow Specification:**
```dart
BoxShadow(
  color: Color(0x4C000000),  // rgba(0, 0, 0, 0.3)
  blurRadius: 10,
  offset: Offset(0, 2),
  spreadRadius: 0,
)
```

**Grid Variants:**
- **1+2 Layout**: 1 большое слева + 2 маленьких справа (текущий)
- **2+1 Layout**: 2 маленьких слева + 1 большое справа
- **2+2 Layout**: 4 равных изображения (2×2 grid)
- **3 Column**: 3 вертикальных изображения
- **Masonry**: Разные высоты в колонках

**Button Count Variants:**
- **2 buttons**: Primary actions (like, share)
- **3 buttons**: Add download
- **4 buttons**: Full action set (текущий)
- **5+ buttons**: Scrollable row

**Flexible elements:**
- Изменить количество изображений (2, 4, 6, 8)
- Изменить grid layout (1+2, 2+2, 3 columns, masonry)
- Изменить количество action buttons (2-6+)
- Добавить image captions/labels
- Добавить selection checkboxes
- Добавить pagination dots
- Изменить button style (filled, outlined, text)

**Usage:** Photo gallery, product images, portfolio grid, media selection, image viewer, social post layout

---

<!-- AI_UI_BLOCK: RatingSummaryCard -->
#### Rating Summary Card {#rating-summary-card}

**[UI Block: Rating Summary Card]** - Карточка с общим рейтингом и детальным breakdown по категориям.

**Dimensions:**
- Screen: 375×317px
- Background: #FAFAFB (color-input-background)
- Border Radius: 30px
- Clip: antiAlias

**Structure:**

1. **Header Section** (0-44px)
   - Height: 44px
   - Navigation icons (optional): 24×24px icons
   - Left padding: 21px, Top padding: 12px
   - Icon border-radius: 32px

2. **Action Buttons Row** (44-88px)
   - Height: 44px
   - Layout: Row, spaceBetween
   - Spacing: 8px between buttons
   - Padding: horizontal 16px, vertical 10px

   **Each Button:**
   - Icon: 24×24px, padding 2px
   - Border-radius: 100px (circular)
   - Container padding: horizontal 16px, vertical 10px
   - Border-radius: 12px

3. **Overall Rating Display** (88-152px)
   - Padding: top 10px, horizontal 16px, bottom 20px
   - Layout: Row, spacing 10px

   **Star Icon:**
   - Size: 24×24px
   - Color: Typically gold/yellow для filled star

   **Rating Text:**
   - Font: 24px Bold (Archivo)
   - Color: #09101D (text-primary)
   - Format: "4.59 (32 reviews)"
   - Line height: 1.40

4. **Rating Breakdown** (152-317px)
   - Padding: top 10px, horizontal 16px, bottom 30px
   - Layout: 3 columns (Label | Progress Bar | Score)
   - Spacing: 5px between columns
   - Row spacing: 15px между category rows

   **Categories (5 rows):**
   - Location: 4.7
   - Check-in: 4.6
   - Cleanliness: 4.5
   - Accuracy: 4.8
   - Communication: 4.9

   **Per Row:**
   - **Left Column** (Category Label):
     - Font: 11px Regular (Archivo)
     - Color: #09101D
     - Align: left

   - **Middle Column** (Progress Bar):
     - Component: Rating Progress Bar (see ### 21. Rating Components)
     - Height: 3px
     - Width: ~234px (6 segments × 39.08px)
     - Filled: #09101D
     - Unfilled: rgba(9, 16, 29, 0.1)
     - Border-radius: 10px (ends)
     - Padding: top 5.5px, left 5.5px, bottom 5.5px

   - **Right Column** (Score Value):
     - Font: 10px Semibold (Archivo)
     - Color: #09101D
     - Align: right
     - Format: "4.7" (one decimal)

**Visual Example:**
```
┌─────────────────────────────────────┐
│  [Header Area - 44px]               │  Navigation/Close
├─────────────────────────────────────┤
│  [○]                         [○]    │  Action Buttons
├─────────────────────────────────────┤
│  ★ 4.59 (32 reviews)                │  Overall Rating
├─────────────────────────────────────┤
│  Location      ▰▰▰▰▰▱   4.7         │
│  Check-in      ▰▰▰▰▰▱   4.6         │  Rating Breakdown
│  Cleanliness   ▰▰▰▰▰▱   4.5         │
│  Accuracy      ▰▰▰▰▰▱   4.8         │
│  Communication ▰▰▰▰▰▰   4.9         │
└─────────────────────────────────────┘
```

**Color Palette Used:**
- Background: #FAFAFB (color-input-background) - очень светлый серый
- Text: #09101D (color-text-primary) - темный текст
- Progress Filled: #09101D - темный
- Progress Unfilled: rgba(9, 16, 29, 0.1) - прозрачный светлый

**Typography:**
- Overall Rating: 24px Bold #09101D, line-height 1.40
- Category Labels: 11px Regular #09101D, line-height 1.40
- Score Values: 10px Semibold #09101D, line-height 1.40

**Spacing:**
- Section padding: 16px horizontal (consistent)
- Top/bottom padding varies by section (10-30px)
- Row spacing: 15px между rating categories
- Column spacing: 5px между элементами row

**Related Components:**
- **Rating Progress Bar** (см. ### 21. Rating Components)
- **Star Icon** (24×24px) - можно добавить filled/outlined states
- **Action Buttons** (см. Buttons section)

**Flexible elements:**
- Изменить количество категорий (3-10+ categories)
- Добавить фильтры по rating (5 stars, 4 stars, etc)
- Добавить "See all reviews" кнопку
- Изменить overall rating display (star icons, numeric only)
- Добавить time period filter (Last month, Last year)
- Добавить reviewer count breakdown
- Изменить progress bar style (gradient, colored segments)

**Usage:** Product reviews, service ratings, property ratings (Airbnb-style), app store ratings, course ratings, restaurant reviews, hotel ratings

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

**Текущая версия**: v5.12.0

### Changelog

#### v5.12.0 (2025-11-19)
- ⭐ Добавлена новая секция **### 21. Rating Components** с AI навигацией
- 📊 Добавлен **Rating Progress Bar** компонент:
  - Height: 3px, segmented progress bar
  - Width: ~234px (6 segments × 39.08px)
  - Filled color: #09101D (text-primary)
  - Unfilled color: rgba(9, 16, 29, 0.1) - прозрачный светлый
  - Border-radius: 10px на концах (topLeft/bottomLeft, topRight/bottomRight)
  - Используется для rating breakdown по категориям
- 📱 Добавлен **Rating Summary Card** UI Block:
  - Dimensions: 375×317px
  - Background: #FAFAFB (input-background)
  - Border-radius: 30px
  - 4 секции: Header (44px), Action Buttons (44px), Overall Rating (64px), Breakdown (165px)
  - Overall Rating: 24px Bold "4.59 (32 reviews)" с star icon 24×24px
  - 5 rating categories: Location, Check-in, Cleanliness, Accuracy, Communication
  - Typography: 11px Regular labels, 10px Semibold scores
  - Layout: 3 columns (Label | Progress Bar | Score), spacing 5px
- 🤖 **AI Navigation Markers** добавлены для IDE AI:
  - HTML комментарии: `<!-- AI_COMPONENT: RatingComponents -->`, `<!-- AI_UI_BLOCK: RatingSummaryCard -->`
  - Якоря для навигации: `{#rating-components}`, `{#rating-summary-card}`
  - Категория теги: `**[Component Category: Rating & Reviews]**`
  - Компонент теги: `**[Component: RatingProgressBar]**`, `**[UI Block: Rating Summary Card]**`
- 🔗 **Related Components** ссылки между компонентами для легкой навигации
- 📊 Все данные извлечены из реального Flutter кода RatingLight компонента

#### v5.11.0 (2025-11-19)
- 🖼️ Добавлен **Gallery Block with Action Buttons** в UI Blocks секцию
- 📸 **Gallery Block структура**:
  - Grid layout: 2 columns, spacing 10px
  - Left: 166.5×250px image
  - Right: 2× 166.5×120px images stacked
  - Total: 343×250px gallery area
  - Border radius: 10px на всех изображениях
- 🎯 **Floating Action Buttons Row**:
  - 4 buttons: Share, Favorite, Download, Info
  - Size: 44×44px circular buttons
  - White background (#FFFFFF)
  - Shadow: rgba(0,0,0,0.3), blur 10px, offset (0,2)
  - Spacing: 10-16px между кнопками
- 🔘 Добавлен **Floating Action Button** компонент:
  - Dimensions: 44×44px, border-radius 30px (circular)
  - Padding: 14px (icon size 16×16px)
  - Background: White с BoxShadow
  - Shadow specs: rgba(0,0,0,0.3), blur 10px, offset (0,2)
  - Typical actions: Share, Favorite, Download, Info, Edit, Delete
  - Touch target: 44×44px ✓ accessibility
- 🎨 **Gallery варианты**:
  - Layout options: 1+2, 2+1, 2+2, 3-column, masonry
  - Button count: 2-6+ buttons depending on actions
  - Flexible: можно менять layout, количество images, добавлять captions
- 📊 Все данные извлечены из реального Flutter кода gallery блока с ButtonsLight

#### v5.10.0 (2025-11-19)
- 🎨 Добавлена новая секция **UI Blocks & Screen Patterns** - готовые комплексные блоки UI
- 📱 Добавлены **3 Start Screen блока** с гибкой структурой:
  1. **Start Screen - Onboarding** (375×412px)
     - Gradient overlay (white fade effect)
     - Logo section (80px, shadow)
     - Hero text: Mixed style (32px Bold, акцент #7CC5D6)
     - Primary button: #7CC5D6 background, "Sign up"
     - Secondary button: Transparent, "Log in"
     - iOS Home Indicator
  2. **Start Screen - Sign Up Form** (375×496px)
     - Close button (top-right)
     - Page title "Create account" (32px Bold)
     - Subtitle с link "Have an account? Sign in"
     - Email input field (#FAFAFB background)
     - Toggle switch "Remember sign in details"
     - Primary button "Confirm & Continue" (черный)
     - Legal footer text (Privacy Policy, Terms of Service)
  3. **Start Screen - Gallery Preview** (375×488px)
     - 3-image carousel (center focus)
     - Side images: 143×310px
     - Center image: 166.5×360px (larger, fit: contain)
     - Spacing: 15px между images
- 🔘 Добавлен **Toggle Switch** компонент:
  - Dimensions: 51×31px
  - Active: #11BB8D green background
  - Inactive: #D9DDE2/#EAEEF2 gray
  - Circle: 31×31px white, 2px border
  - Animation: ~200-300ms slide
- 🎨 Новые цвета:
  - Link Blue (#2E5AAC) - для ссылок и underline
  - Input Background (#FAFAFB) - очень светлый для input полей
- ✨ **Гибкость блоков**: Все UI блоки можно расширять/модифицировать (добавлять input поля, кнопки, менять контент)
- 📊 Все данные извлечены из реального Flutter кода start screen блоков

#### v5.9.0 (2025-11-19)
- 📝 Добавлен **Text Input Field** компонент с универсальными вариантами
- 🎨 Новый цвет для secondary info:
  - Info Blue (#0B24FB) - синий для дополнительной информации (цены, балансы)
- 🔧 Добавлена полная спецификация **Text Input Field** с 8 вариантами:
  1. **Basic Input with Cursor** - базовое поле с курсором
  2. **Input with Positive Validation** - успешная валидация с emoji 👌
  3. **Input with Top Label & Balance Info** - с label и balance/price info
  4. **Input with Right Icon** - иконка справа (24px)
  5. **Input with Left Icon** - иконка слева (24px)
  6. **Input with Avatar & Delete Button** - аватар 30px + action button
  7. **Filled Input** - заполненное поле (email)
  8. **Input with Negative Validation** - ошибка валидации
- 📐 **Base Specs**:
  - Dimensions: 375px container, 44-46px height
  - Border: 2px solid #4141E6 (primary-blue) focus state
  - Border radius: 15px
  - Internal padding: top 4px, left 20px, right 15px, bottom 4px
- 📋 **Typography**:
  - Placeholder: 12px Regular #747B84
  - Input Text: 14px Semibold #09101D
  - Helper: 12px Regular (#11BB8D success, #E24949 error)
  - Label: 14px Semibold
  - Secondary Info: 10px Semibold (#09101D, #0B24FB)
- 🎯 **Icons & Avatars**:
  - Icons: 24×24px, 2px padding, border-radius 100px
  - Avatar: 30×30px circle, OvalBorder, #F4F6F9 background
  - Delete Button: 24×24px, #F4F6F9 bg, 10px border-radius
- 💬 **Cursor**: "|" pipe character, 12px Regular #09101D
- 📊 Все данные извлечены из реального Flutter кода text input системы

#### v5.8.0 (2025-11-19)
- 🔐 Добавлен **Password Input Field** компонент с полной системой состояний
- 🎨 Новые цвета для validation states:
  - Red Validation (#DA1414) - для validation errors
  - Positive Background rgba(17, 187, 141, 0.05) - светло-зеленый для success
  - Negative Background rgba(218, 20, 20, 0.05) - светло-красный для errors
- 📝 Добавлена полная документация **Password Input Field** с 12 состояниями:
  1. **Enabled (Default)** - пустое поле с placeholder
  2. **Focus** - фокус с 2px черной обводкой
  3. **Pressed** - нажатие, серый background (#EAEEF2)
  4. **Active - Typing - Show** - ввод видимого пароля
  5. **Active - Typing - Hide** - ввод скрытого пароля (dots)
  6. **Complete - Hide** - заполнено, скрыто
  7. **Incomplete** - неполный ввод
  8. **Positive - Show** - успешная валидация, видимый (зеленая обводка)
  9. **Positive - Hide** - успешная валидация, скрытый
  10. **Negative - Show** - ошибка валидации, видимый (красная обводка)
  11. **Negative - Hide** - ошибка валидация, скрытый
  12. **Disabled** - выключенное состояние (серый текст)
- 👁️ **Password Masking спецификации**:
  - Visible mode: 14px Regular text
  - Hidden mode: 24px bullet points "•"
- 🔧 **Field спецификации**:
  - Dimensions: 343px width, 36px height
  - Border radius: 15px
  - Padding: left 16px, right 20px
  - Icons: 20×20px (eye, checkmark, error)
  - Cursor: 2px width, 16px height
- 📋 **Label & Helper Text**:
  - Label: 14px Semibold (#09101D или #D9DDE2 disabled)
  - Helper: 14px Regular (#747B84 default, #E24949 error, #D9DDE2 disabled)
  - Spacing: 8px между элементами
- 📊 Все данные извлечены из реального Flutter кода password input системы

#### v5.7.0 (2025-11-19)
- 📊 Добавлен **Progress Stepper / Track Bar** компонент
- 🎨 Новый цвет для UI элементов:
  - Gray Lighter (#EAEEF2) - очень светло-серый для inactive steps
- 🔄 Добавлена полная спецификация **Progress Stepper** компонента:
  - **Step Indicator (Active)** - 18×18px черный с белой обводкой
    - Outer circle: 18×18px (#09101D)
    - Inner circle: 14×14px с 1px white border
  - **Step Indicator (Inactive)** - 14×14px светло-серый
    - Background: #EAEEF2 (gray-lighter)
  - **Step Indicator (Completed)** - 17×17px с иконкой checkmark
    - Container: 18×18px, padding top 0.5px
  - **Progress Line** - 4px height, #F4F6F9 background
    - Border radius: 10px
    - Layout: Expanded между steps
  - **Step Labels** - 10px Semibold Archivo
    - Position: Below indicators
    - Text align: Center
- 🎯 Документированы **3 состояния прогресса**:
  - State 1: Step 1 active, Steps 2-3 inactive
  - State 2: Step 1 completed, Step 2 active, Step 3 inactive
  - State 3: Steps 1-2 completed, Step 3 active
- 📱 Container specs: 375px width, 32px horizontal padding, 30px row height
- 📊 Все данные извлечены из реального Flutter кода track bar системы

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
