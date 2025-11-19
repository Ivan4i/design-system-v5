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
--color-bg-quaternary: #FAFAFB;    /* Очень светлый серый (контейнеры) */
--color-bg-toggle: #EAEEF2;        /* Toggle switch background (inactive) */
--color-bg-dark: #12202F;          /* Темный фон */
```

### Text Colors

```css
/* Текстовые цвета */
--color-text-primary: #09101D;     /* Основной текст (заголовки) */
--color-text-secondary: #414249;   /* Вторичный текст (подзаголовки) */
--color-text-tertiary: #64748B;    /* Третичный текст */
--color-text-dark: #23262B;        /* Темный текст (emphasis) */
--color-text-placeholder: #747B84; /* Placeholder текст в inputs */
```

### Accent Colors

```css
/* Акцентные цвета */
--color-accent-blue: #4141E6;      /* Синий (stories, primary actions, buttons) */
--color-accent-pink: #FC466B;      /* Розовый (stories, highlights) */
--color-accent-purple: #7B61FF;    /* Фиолетовый (borders, decorative) */
```

### Status Colors

```css
/* Статусные цвета */
--color-status-online: #11BB8D;    /* Зеленый (online indicator) */
--color-status-success: #10B981;
--color-status-error: #EF4444;
--color-status-warning: #F59E0B;
```

### Overlay Colors

```css
/* Overlay цвета */
--color-overlay-dark: rgba(29, 29, 29, 0.5);      /* Темный overlay (50% opacity) */
--color-overlay-gradient-start: rgba(196, 196, 196, 0);  /* Прозрачный старт */
--color-overlay-gradient-end: rgba(29, 29, 29, 0.5);     /* Темный конец */
```

### Gradient Colors

```css
/* Градиенты */
--gradient-live-start: #833AB4;    /* Фиолетовый (Live badge, category borders) */
--gradient-live-middle: #FD1D1D;   /* Красный (Live badge) */
--gradient-live-end: #FCB045;      /* Оранжевый (Live badge) */

/* Применение Live gradient */
--gradient-live: linear-gradient(90deg, #833AB4 0%, #FD1D1D 50%, #FCB045 100%);

/* Image overlay gradient (для карточек) */
--gradient-overlay: linear-gradient(180deg, rgba(196, 196, 196, 0) 0%, rgba(29, 29, 29, 0.5) 100%);
```

### Border Colors

```css
/* Цвета границ */
--color-border-primary: #E5E7EB;
--color-border-secondary: #D1D5DB;
--color-border-stories-blue: #4141E6;     /* Border для непросмотренных stories */
--color-border-stories-pink: #FC466B;     /* Border для highlighted stories */
--color-border-category-blue: #4141E6;    /* Border для активных категорий (синий) */
--color-border-category-purple: #833AB4;  /* Border для категорий (фиолетовый) */
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
--font-size-72: 4.5rem;       /* 72px */
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
--line-height-tight: 0.70;    /* 70% (relative) - для больших заголовков */
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

#### Display Heading (Extra Large)
- **Font Size**: 72px (4.5rem)
- **Font Weight**: 800 (Extrabold)
- **Font Family**: 'Archivo'
- **Line Height**: 0.70 (50.4px)
- **Color**: #09101D (--color-text-primary)
- **Использование**: Большие заголовки секций, главные экраны
- **Пример**: Заголовок "Badges" на главном экране

#### Mixed Text Style (Bold + Regular)
- **Font Size**: 12px (0.75rem)
- **Font Family**: 'Archivo'
- **Line Height**: 1.40 (16.8px)
- **Color**: #09101D (--color-text-primary) или #414249 (--color-text-secondary)
- **Использование**: Комбинированный текст с выделением (например, "98+ **Playlists** on Napster")
- **Структура**:
  - Часть 1: Font Weight 700 (Bold)
  - Часть 2: Font Weight 400 (Regular)
- **Пример CSS**:
```css
.mixed-text {
  font-size: 12px;
  font-family: 'Archivo';
  line-height: 1.40;
  color: var(--color-text-primary);
}

.mixed-text__bold {
  font-weight: 700;
}

.mixed-text__regular {
  font-weight: 400;
}
```

#### Input Placeholder Text
- **Font Size**: 15px (0.9375rem)
- **Font Weight**: 400 (Regular)
- **Font Family**: 'Archivo'
- **Line Height**: 1.40 (21px)
- **Color**: #747B84 (--color-text-placeholder)
- **Использование**: Placeholder текст в input полях ("Message", "Search", etc.)

#### Input Filled Text
- **Font Size**: 15px (0.9375rem)
- **Font Weight**: 400 (Regular)
- **Font Family**: 'Archivo'
- **Line Height**: 1.40 (21px)
- **Color**: #09101D (--color-text-primary)
- **Использование**: Введенный пользователем текст в input полях ("Hello!", etc.)

#### Form Label (Search/Input Label)
- **Font Size**: 14px (0.875rem)
- **Font Weight**: 600 (Semibold)
- **Font Family**: 'Archivo'
- **Line Height**: 1.40 (19.6px)
- **Color**: #09101D (--color-text-primary) normal, #D9DDE2 (--color-bg-tertiary) disabled
- **Использование**: Label для search input и form fields ("Enabled", "Focus", "Complete")

#### Form Helper Text
- **Font Size**: 14px (0.875rem)
- **Font Weight**: 400 (Regular)
- **Font Family**: 'Archivo'
- **Line Height**: 1.40 (19.6px)
- **Color**: #747B84 (--color-text-placeholder) normal, #D9DDE2 (--color-bg-tertiary) disabled
- **Использование**: Вспомогательный текст под input полями ("Helper", инструкции, подсказки)

#### Search Placeholder Text
- **Font Size**: 14px (0.875rem)
- **Font Weight**: 400 (Regular)
- **Font Family**: 'Archivo'
- **Line Height**: 1.40 (19.6px)
- **Color**: #747B84 (--color-text-placeholder)
- **Использование**: Placeholder текст в search полях ("Search here...", "Type to search...")

#### Search Filled Text
- **Font Size**: 14px (0.875rem)
- **Font Weight**: 400 (Regular)
- **Font Family**: 'Archivo'
- **Line Height**: 1.40 (19.6px)
- **Color**: #09101D (--color-text-primary)
- **Использование**: Введенный текст в search полях ("Request", "Text", поисковые запросы)

#### Form Top Helper Text
- **Font Size**: 10px (0.625rem)
- **Font Weight**: 600 (Semibold)
- **Font Family**: 'Archivo'
- **Line Height**: 1.40 (14px)
- **Color**: #09101D (--color-text-primary) основной, #4141E6 (--color-accent-blue) для secondary info
- **Использование**: Балансы, дополнительная информация над input ("Balance: 0.10025 BTC", "~6.984$")

#### Form Field Two-Line (Label + Value)
- **Label (Top Line)**: 12px, weight 400, color #747B84, line-height 1.40
- **Value (Bottom Line)**: 14px, weight 600, color #09101D или #23262B, line-height 1.40
- **Использование**: Двухстрочный контент в input ("Your email" / "you@awesome.com")

#### Form Bottom Helper Success
- **Font Size**: 14px (0.875rem)
- **Font Weight**: 400 (Regular)
- **Font Family**: 'Archivo'
- **Line Height**: 1.40 (19.6px)
- **Color**: #11BB8D (--color-status-online) для success state
- **Emoji Support**: Да (например: "👍🏻")
- **Использование**: Успешная валидация, позитивный feedback ("Good name 👍🏻")

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
--radius-category-inner: 0.625rem;   /* 10px - Category card inner */
--radius-icon: 0.625rem;             /* 10px - Icon containers */
--radius-category: 0.75rem;          /* 12px - Category card outer */
--radius-xl: 0.75rem;                /* 12px - Live badge */
--radius-category-border: 0.875rem;  /* 14px - Category card with border */
--radius-badge: 0.9375rem;           /* 15px - Badge containers, Buttons */
--radius-2xl: 1rem;                  /* 16px */
--radius-notification: 1.25rem;      /* 20px - Notification badge */
--radius-stories: 1.875rem;          /* 30px - Stories border */
--radius-avatar: 2.5rem;             /* 40px - Avatar */
--radius-full: 9999px;               /* Полностью круглый */
```

**Применение из Flutter кода:**
- `radius-category (12px)`: Category card outer border radius
- `radius-category-border (14px)`: Category card с border (2px border)
- `radius-category-inner (10px)`: Category card inner image
- `radius-avatar (40px)`: Основной border radius для аватаров
- `radius-stories (30px)`: Border radius для stories border вокруг аватара
- `radius-notification (20px)`: Notification badge
- `radius-badge (15px)`: Стандартные badge контейнеры, Buttons
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

#### Category Card (из реального Flutter кода)

**Спецификация из кода:**
- **Size**: 100px × 120px
- **Border Radius**: 12px (outer container)
- **Image fit**: cover
- **Использование**: Карточки категорий/сервисов с изображением и текстом

**Структура Category Card:**

```
Container: 100×120 (border-radius: 12px)
├─ Outer Border Container: 100×120 (optional)
│  ├─ Border: 2px solid
│  ├─ Border Radius: 14px
│  └─ Border Colors: #4141E6 (blue), #833AB4 (purple)
│
├─ Inner Image Container: 92×112 (position: 4px, 4px)
│  ├─ Border Radius: 10px
│  ├─ Image: fit cover
│  └─ Background: white
│
├─ Gradient Overlay: 92×112 (или 100×120 без border)
│  ├─ Height: 64.84px (или 70px)
│  ├─ Position: top 50px (или 51.16px)
│  ├─ Gradient: linear-gradient(180deg, transparent 0%, rgba(29,29,29,0.5) 100%)
│  └─ Border Radius: bottom corners 10px
│
└─ Text Container: (position: 83.08px from top)
   ├─ Padding: 10px left, 10px bottom (optional 10px right)
   ├─ Width: 80px (text) или 90px
   └─ Text:
      ├─ Font: 10px, weight 600
      ├─ Color: white
      ├─ Line Height: 1.40 (14px)
      ├─ Font Family: 'Archivo'
      └─ Multi-line support
```

**Варианты Category Card:**

**1. Default (без border)**
```
Size: 100×120
Border Radius: 12px
Image: cover, 100×120
Overlay: gradient from top 50px
Text: bottom, white
```

**2. With Blue Border (активная категория)**
```
Outer Container: 100×120, border-radius 14px
Border: 2px solid #4141E6
Inner Image: 92×112, position 4×4, border-radius 10px
Overlay: gradient from top 51.16px, height 64.84px
Text: bottom, white, padding 10px
```

**3. With Purple Border**
```
Border: 2px solid #833AB4
Other specs: same as blue border variant
```

**Spacing & Layout (из кода):**
- **Card spacing**: 10px (horizontal gap между карточками)
- **Container padding**: 10px top/bottom, 16px left
- **Text padding**: 10px left, 10px bottom, 10px right (optional)
- **Text width**: 80px

**Typography:**
- **Font Size**: 10px (0.625rem)
- **Font Weight**: 600 (Semibold)
- **Font Family**: 'Archivo'
- **Line Height**: 1.40 (14px)
- **Color**: #FFFFFF (white)
- **Multi-line**: Поддержка 2+ строк

**CSS пример:**

```css
.category-card {
  width: 100px;
  height: 120px;
  border-radius: var(--radius-category); /* 12px */
  overflow: hidden;
  position: relative;
}

.category-card--bordered {
  border: var(--border-width-2) solid var(--color-border-category-blue);
  border-radius: var(--radius-category-border); /* 14px */
}

.category-card--bordered.purple {
  border-color: var(--color-border-category-purple);
}

.category-card__image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: var(--radius-category-inner); /* 10px */
}

.category-card--bordered .category-card__image {
  width: 92px;
  height: 112px;
  position: absolute;
  left: 4px;
  top: 4px;
}

.category-card__overlay {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 70px;
  background: var(--gradient-overlay);
}

.category-card__text {
  position: absolute;
  bottom: 10px;
  left: 10px;
  width: 80px;
  color: white;
  font-size: 10px;
  font-weight: 600;
  line-height: 1.40;
}
```

---

### 2. Buttons (из реального Flutter кода)

#### Pill Button (Small Button)

**Спецификация из кода:**
- **Height**: 36px
- **Padding**: 16px horizontal, 10px vertical
- **Border Radius**: 15px (--radius-badge)
- **Typography**:
  - Font: 13px (0.8125rem)
  - Weight: 600 (Semibold)
  - Font Family: 'Archivo'
  - Line Height: 1.40 (18.2px)
- **Icon Spacing**: 8px (между иконкой и текстом)
- **Icon Size**: 16×16 (padding: 2px, border-radius: 100px)
- **Варианты позиций иконки**:
  - Left: Icon → Text
  - Right: Text → Icon
  - Both: Icon → Text → Icon
  - Icon Only: Только icon в кнопке

**Варианты Pill Button:**

**1. Primary (Blue Filled)**
```
Background: #4141E6 (--color-accent-blue)
Text Color: #FFFFFF (white)
Border: none
```

**2. Secondary (Light Gray Filled)**
```
Background: #F4F6F9 (--color-bg-secondary)
Text Color: #09101D (--color-text-primary)
Border: none
```

**3. Outlined (Blue Border)**
```
Background: transparent
Text Color: #4141E6 (--color-accent-blue)
Border: 1px solid #4141E6
Border Radius: 15px
```

**4. Disabled**
```
Background: #F4F6F9 (--color-bg-secondary)
Text Color: #D9DDE2 (--color-bg-tertiary) - low contrast
Border: none
Cursor: not-allowed
```

**5. Ghost (Transparent)**
```
Background: transparent
Text Color: #09101D (--color-text-primary)
Border: none
```

#### Icon Button (Square)

**Спецификация из кода:**
- **Size**: 40×40
- **Padding**: 12px (icon становится 16×16)
- **Border Radius**: 15px (--radius-badge)
- **Icon Size**: 16×16 (centered)

**Варианты Icon Button:**

**1. Primary (Blue Filled)**
```
Background: #4141E6 (--color-accent-blue)
Icon Color: white
Border: none
```

**2. Secondary (Light Gray Filled)**
```
Background: #F4F6F9 (--color-bg-secondary)
Icon Color: #09101D (--color-text-primary)
Border: none
```

**3. Outlined (Blue Border)**
```
Background: transparent
Icon Color: #4141E6 (--color-accent-blue)
Border: 1px solid #4141E6
Border Radius: 15px
```

**4. Disabled**
```
Background: #F4F6F9 (--color-bg-secondary)
Icon Color: #D9DDE2 (--color-bg-tertiary)
Border: none
Cursor: not-allowed
```

**5. Ghost (Transparent)**
```
Background: transparent
Icon Color: #09101D (--color-text-primary)
Border: none
```

#### Button Spacing (из кода)

- **Horizontal spacing** (между кнопками): ~162px
- **Vertical spacing** (между кнопками): ~90px
- **Icon button spacing**: 34px (в вертикальном списке)

#### Button States

**Interactive States для всех кнопок:**

- **Default**: Базовое состояние
- **Hover**:
  - Primary: Lighter shade of blue (#5858E9)
  - Secondary: Darker gray (#E8EAED)
  - Outlined: Light blue background (#F0F2FF)
  - Ghost: Light gray background (#F4F6F9)
  - Transition: 150ms ease
- **Active/Pressed**:
  - Transform: scale(0.98)
  - Opacity: 0.9
  - Transition: 100ms ease
- **Focus**:
  - Outline: 2px solid #4141E6
  - Outline offset: 2px
- **Disabled**:
  - Cursor: not-allowed
  - Pointer events: none
  - Opacity: 0.6 (для всех элементов)

#### Usage Guidelines

- **Primary**: Main actions, CTAs (Confirm, Submit, Save)
- **Secondary**: Less prominent actions (Cancel, Back)
- **Outlined**: Alternative actions, filters, selections
- **Ghost**: Tertiary actions, minimal visual weight
- **Icon Button**: Compact actions, toolbars, navigation

---

### 3. Toggle Switch (из реального Flutter кода)

#### Toggle Switch Specification

**Спецификация из кода:**
- **Size**: 52px × 31px
- **Border Radius**: 40px (--radius-avatar)
- **Background (inactive)**: #EAEEF2 (--color-bg-toggle)
- **Background (active)**: #4141E6 (--color-accent-blue)
- **Transition**: 200ms ease

**Toggle Circle:**
- **Size**: 31px × 31px
- **Background**: #FFFFFF (white)
- **Border**: 2px solid #EAEEF2 (inactive) or #4141E6 (active)
- **Border Radius**: 40px
- **Position (inactive)**: left: 0
- **Position (active)**: left: 21px (52px - 31px)
- **Transition**: left 200ms ease

**Структура Toggle Switch:**

```
Container: 52×31 (border-radius: 40px)
├─ Background (inactive): #EAEEF2
├─ Background (active): #4141E6
└─ Toggle Circle: 31×31 (position: left 0 or 21px)
   ├─ Background: white
   ├─ Border: 2px solid (matches container bg)
   └─ Border Radius: 40px
```

**States:**

**1. Inactive (Off)**
```
Container Background: #EAEEF2 (--color-bg-toggle)
Circle Position: left 0
Circle Border: 2px solid #EAEEF2
```

**2. Active (On)**
```
Container Background: #4141E6 (--color-accent-blue)
Circle Position: left 21px
Circle Border: 2px solid #4141E6
```

**3. Disabled (Off)**
```
Container Background: #EAEEF2
Circle Border: 2px solid #EAEEF2
Opacity: 0.5
Cursor: not-allowed
```

**4. Disabled (On)**
```
Container Background: #4141E6
Circle Border: 2px solid #4141E6
Opacity: 0.5
Cursor: not-allowed
```

**CSS пример:**

```css
.toggle-switch {
  width: 52px;
  height: 31px;
  border-radius: var(--radius-avatar); /* 40px */
  background: var(--color-bg-toggle); /* #EAEEF2 */
  position: relative;
  cursor: pointer;
  transition: background-color 200ms ease;
}

.toggle-switch--active {
  background: var(--color-accent-blue); /* #4141E6 */
}

.toggle-switch__circle {
  width: 31px;
  height: 31px;
  background: white;
  border: var(--border-width-2) solid var(--color-bg-toggle);
  border-radius: var(--radius-avatar); /* 40px */
  position: absolute;
  left: 0;
  top: 0;
  transition: left 200ms ease, border-color 200ms ease;
}

.toggle-switch--active .toggle-switch__circle {
  left: 21px;
  border-color: var(--color-accent-blue);
}

.toggle-switch:disabled {
  opacity: 0.5;
  cursor: not-allowed;
  pointer-events: none;
}
```

**Usage Guidelines:**
- **Label Position**: Left or right of toggle (8-12px spacing)
- **Accessibility**: Include ARIA attributes (role="switch", aria-checked)
- **Keyboard**: Support Space/Enter for toggling
- **Использование**: Settings toggles, feature on/off, binary choices

---

### 4. Inputs (из реального Flutter кода)

#### Text Input Field Specification

**Спецификация из кода (iOS style):**
- **Container Size**: 375px × 44px (стандартный iOS input)
- **Background**: #F4F6F9 (--color-bg-secondary) или white
- **Border Radius**: 15px (--radius-badge)
- **Inner Padding**: 8px (для текстового поля)
- **Outer Padding**: 10px horizontal, 5px vertical
- **Shadow**: rgba(0, 0, 0, 0.05) / box-shadow: 0 -1px 0 rgba(0,0,0,0.05)
- **Row Spacing**: 5px (между элементами в input)

**Typography (Placeholder):**
- **Font Size**: 15px (0.9375rem)
- **Font Weight**: 400 (Regular)
- **Font Family**: 'Archivo'
- **Line Height**: 1.40 (21px)
- **Color**: #747B84 (--color-text-placeholder)
- **Использование**: Placeholder текст "Message"

**Typography (Filled Text):**
- **Font Size**: 15px (0.9375rem)
- **Font Weight**: 400 (Regular)
- **Font Family**: 'Archivo'
- **Line Height**: 1.40 (21px)
- **Color**: #09101D (--color-text-primary)
- **Использование**: Введенный текст "Hello!"

**Структура Input Field:**

```
Container: 375×44 (background: white or #F4F6F9)
├─ Shadow: 0 -1px 0 rgba(0,0,0,0.05)
└─ Row Container: padding 10px/5px
   ├─ Spacing: 5px between elements
   └─ Input Field Container: Expanded
      ├─ Background: #F4F6F9 or white
      ├─ Border Radius: 15px
      ├─ Padding: 8px
      └─ Text: 15px, weight 400
```

**Варианты Input Field:**

**1. Basic Input (Default - Filled Background)**
```
Container background: white
Input field:
- Background: #F4F6F9 (--color-bg-secondary)
- Border: none
- Border Radius: 15px
- Padding: 8px
- Text color: #747B84 (placeholder) or #09101D (filled)
```

**2. Basic Input (Light Background)**
```
Container background: #F4F6F9
Input field:
- Background: white
- Border: none
- Border Radius: 15px
- Padding: 8px
```

**3. Input with Outlined Border**
```
Input field:
- Background: transparent
- Border: 1px solid #D9DDE2 (strokeAlign: outside)
- Border Radius: 15px
- Padding: 8px
```

**4. Input with Action Buttons (Left/Right)**
```
Row layout:
├─ Left icon button(s): 34×34 (optional)
├─ Input field: Expanded, background #F4F6F9
└─ Right icon button(s): 34×34 (1-3 buttons)

Action Button specs:
- Size: 34×34
- Background: #F4F6F9 (--color-bg-secondary)
- Border Radius: 15px
- Icon Size: 23×23
- Padding horizontal: 5px
- Spacing between buttons: 5px
```

**5. Input with Multiple Action Buttons**
```
Left side:
- Icon button 1: 34×34
- Icon button 2: 34×34
- Icon button 3: 34×34

Center:
- Input field: Expanded

Right side:
- Icon button: 34×34
```

**6. Input with Continuous Background**
```
Left icon button + Input field имеют одинаковый background:
- Combined background: #F4F6F9
- Border Radius: 15px
- Icon button padding: 5px horizontal
- Input padding: 8px left only
- Creates seamless look
```

**Container Backgrounds (из кода):**
- **White**: Для input полей с filled background (#F4F6F9)
- **Light Gray (#F4F6F9)**: Для input полей с white background
- **Transparent/None**: Для inputs с только border

**Action Icon Button:**
- **Size**: 34×34 (compact, smaller than standard 40×40)
- **Background**: #F4F6F9 (default), transparent (variant)
- **Border Radius**: 15px
- **Icon Size**: 23×23
- **Icon Placeholder**: 23×23 empty container (для SVG/icon)
- **Padding**: 5px horizontal (для иконок)
- **Spacing**: 5px (между кнопками)
- **Alignment**: Center vertical

**CSS пример:**

```css
.input-container {
  width: 375px;
  height: 44px;
  background: white; /* или #F4F6F9 */
  box-shadow: 0 -1px 0 rgba(0, 0, 0, 0.05);
  padding: 5px 10px;
  display: flex;
  align-items: flex-end;
  gap: 5px;
}

.input-field {
  flex: 1;
  height: 100%;
  padding: 8px;
  background: var(--color-bg-secondary); /* #F4F6F9 */
  border: none;
  border-radius: var(--radius-badge); /* 15px */
  font-family: 'Archivo';
  font-size: 15px;
  font-weight: 400;
  line-height: 1.40;
  color: var(--color-text-primary);
}

.input-field::placeholder {
  color: var(--color-text-placeholder); /* #747B84 */
}

.input-field--outlined {
  background: transparent;
  border: 1px solid var(--color-bg-tertiary); /* #D9DDE2 */
}

.input-field--white {
  background: white;
}

.input-action-button {
  width: 34px;
  height: 34px;
  background: var(--color-bg-secondary); /* #F4F6F9 */
  border: none;
  border-radius: var(--radius-badge); /* 15px */
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0 5px;
  cursor: pointer;
}

.input-action-button--transparent {
  background: transparent;
}

.input-action-button__icon {
  width: 23px;
  height: 23px;
}
```

**Usage Guidelines:**
- **Basic Input**: Simple text entry (messages, search)
- **With Border**: Emphasized input, form fields
- **With Action Buttons**: Quick actions (send, attach, emoji, voice)
- **Icon Buttons**: 1-4 icons total, balanced left/right
- **Background Variants**: Match with container background for visual hierarchy
- **Accessibility**: Label, placeholder, focus states, keyboard support

#### Search Input Field Specification

**Спецификация из кода:**
- **Field Size**: 375px × 36px (компактнее стандартного input 44px)
- **Container Padding**: 16px horizontal, 5px vertical
- **Field Padding**: 16px left, 20px right
- **Background**: #F4F6F9 (--color-bg-secondary) enabled
- **Background Pressed/Disabled**: #EAEEF2 (--color-bg-toggle)
- **Border Radius**: 15px (--radius-badge)
- **Focus Border**: 2px solid #09101D (--color-text-primary)
- **Spacing**: 8px (между label, input и helper text)

**Typography (Label):**
- **Font Size**: 14px (0.875rem)
- **Font Weight**: 600 (Semibold)
- **Font Family**: 'Archivo'
- **Line Height**: 1.40 (19.6px)
- **Color**: #09101D (--color-text-primary) normal, #D9DDE2 (--color-bg-tertiary) disabled
- **Использование**: "Enabled", "Focus", "Complete"

**Typography (Placeholder):**
- **Font Size**: 14px (0.875rem)
- **Font Weight**: 400 (Regular)
- **Font Family**: 'Archivo'
- **Line Height**: 1.40 (19.6px)
- **Color**: #747B84 (--color-text-placeholder)
- **Использование**: "Search here..."

**Typography (Filled Text):**
- **Font Size**: 14px (0.875rem)
- **Font Weight**: 400 (Regular)
- **Font Family**: 'Archivo'
- **Line Height**: 1.40 (19.6px)
- **Color**: #09101D (--color-text-primary)
- **Использование**: "Request", "Text"

**Typography (Helper Text):**
- **Font Size**: 14px (0.875rem)
- **Font Weight**: 400 (Regular)
- **Font Family**: 'Archivo'
- **Line Height**: 1.40 (19.6px)
- **Color**: #747B84 (--color-text-placeholder) normal, #D9DDE2 (--color-bg-tertiary) disabled
- **Использование**: "Helper"

**Icons:**
- **Search Icon**: 20×20 (left side)
- **Clear Button Icon**: 20×20 (right side, появляется при filled/incomplete)
- **Icon Spacing**: 20px (row spacing), 15px (между icon и text)

**Cursor:**
- **Size**: 2px × 16px
- **Color**: #09101D (--color-text-primary)
- **Position**: After text (blinking vertical bar)

**Структура Search Input:**

```
Container: 375px width, padding 16px/5px
├─ Spacing: 8px vertical
│
├─ Label: 14px, weight 600, color #09101D
│  └─ Text: "Enabled", "Focus", "Complete", etc.
│
├─ Search Field: 375×36
│  ├─ Background: #F4F6F9 or #EAEEF2
│  ├─ Border: 2px solid #09101D (focus only)
│  ├─ Border Radius: 15px
│  ├─ Padding: 16px left, 20px right
│  │
│  └─ Row Layout:
│     ├─ Search Icon: 20×20 (spacing: 20px)
│     ├─ Text/Placeholder: 14px, weight 400
│     │  └─ Cursor: 2×16 (when active)
│     └─ Clear Button: 20×20 (right, optional)
│
└─ Helper Text: 14px, weight 400, color #747B84
   └─ Text: "Helper"
```

**States:**

**1. Enabled (Default)**
```
Label: #09101D, weight 600
Field Background: #F4F6F9
Border: none
Search Icon: 20×20 (left)
Placeholder: "Search here...", #747B84
Clear Button: hidden
Helper: #747B84
```

**2. Focus**
```
Label: #09101D, weight 600
Field Background: #F4F6F9
Border: 2px solid #09101D
Search Icon: 20×20 (left)
Placeholder: "Search here...", #747B84
Cursor: 2×16 visible
Clear Button: hidden
Helper: #747B84
```

**3. Pressed**
```
Label: #09101D, weight 600
Field Background: #EAEEF2 (darker)
Border: none
Search Icon: 20×20 (left)
Placeholder: "Search here...", #747B84
Clear Button: hidden
Helper: #747B84
```

**4. Active - Typing**
```
Label: #09101D, weight 600
Field Background: #F4F6F9
Border: 2px solid #09101D
Search Icon: 20×20 (left)
Text: "Text", #09101D
Cursor: 2×16 at end of text
Clear Button: 20×20 visible (right)
Helper: #747B84
```

**5. Complete (Filled)**
```
Label: #09101D, weight 600
Field Background: #F4F6F9
Border: none
Search Icon: 20×20 (left)
Text: "Request", #09101D
Clear Button: 20×20 visible (right)
Helper: #747B84
```

**6. Incomplete (Placeholder + Clear)**
```
Label: #09101D, weight 600
Field Background: #F4F6F9
Border: none
Search Icon: 20×20 (left)
Placeholder: "Search here...", #747B84
Clear Button: 20×20 visible (right)
Helper: #747B84
```

**7. Disabled**
```
Label: #D9DDE2 (disabled color)
Field Background: #EAEEF2
Border: none
Search Icon: 20×20 (left, disabled)
Placeholder: "Search here...", #747B84
Clear Button: hidden
Helper: #D9DDE2 (disabled color)
Cursor: not-allowed
```

**CSS пример:**

```css
.search-input-container {
  width: 375px;
  padding: 5px 16px;
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.search-input__label {
  font-family: 'Archivo';
  font-size: 14px;
  font-weight: 600;
  line-height: 1.40;
  color: var(--color-text-primary); /* #09101D */
}

.search-input__label--disabled {
  color: var(--color-bg-tertiary); /* #D9DDE2 */
}

.search-input__field {
  width: 100%;
  height: 36px;
  padding: 0 20px 0 16px;
  background: var(--color-bg-secondary); /* #F4F6F9 */
  border: none;
  border-radius: var(--radius-badge); /* 15px */
  display: flex;
  align-items: center;
  gap: 15px;
  transition: background 150ms, border 150ms;
}

.search-input__field--focus,
.search-input__field--active {
  border: 2px solid var(--color-text-primary); /* #09101D */
  padding: 0 18px 0 14px; /* Adjust for 2px border */
}

.search-input__field--pressed,
.search-input__field--disabled {
  background: var(--color-bg-toggle); /* #EAEEF2 */
}

.search-input__field--disabled {
  cursor: not-allowed;
}

.search-input__icon {
  width: 20px;
  height: 20px;
  flex-shrink: 0;
}

.search-input__text {
  flex: 1;
  font-family: 'Archivo';
  font-size: 14px;
  font-weight: 400;
  line-height: 1.40;
  color: var(--color-text-primary);
  border: none;
  background: transparent;
  outline: none;
}

.search-input__text::placeholder {
  color: var(--color-text-placeholder); /* #747B84 */
}

.search-input__cursor {
  width: 2px;
  height: 16px;
  background: var(--color-text-primary);
  animation: blink 1s infinite;
}

@keyframes blink {
  0%, 50% { opacity: 1; }
  51%, 100% { opacity: 0; }
}

.search-input__clear {
  width: 20px;
  height: 20px;
  flex-shrink: 0;
  cursor: pointer;
  display: none;
}

.search-input__field--filled .search-input__clear,
.search-input__field--incomplete .search-input__clear {
  display: block;
}

.search-input__helper {
  font-family: 'Archivo';
  font-size: 14px;
  font-weight: 400;
  line-height: 1.40;
  color: var(--color-text-placeholder); /* #747B84 */
}

.search-input__helper--disabled {
  color: var(--color-bg-tertiary); /* #D9DDE2 */
}
```

**Usage Guidelines:**
- **Search Field**: Global search, filter lists, quick find
- **Label**: Always include descriptive label for accessibility
- **Helper Text**: Provide context or instructions ("Start typing to search...")
- **Clear Button**: Show when user has entered text (filled/incomplete states)
- **Focus State**: Strong 2px border for clear visual feedback
- **Disabled State**: Use disabled colors for label and helper
- **Icon Size**: 20×20 for compact design
- **Height**: 36px (более компактный чем стандартный 44px)
- **Accessibility**: Label, aria-label, keyboard support (Enter to search, Esc to clear)

#### Advanced Input Field Specification (Form Fields)

**Спецификация из кода:**
- **Field Size**: 375px × 46px (больше чем standard 44px и search 36px)
- **Container Padding**: 16px horizontal, 10px vertical
- **Field Padding**: 4px top, 20px left, 15px right, 4px bottom
- **Border**: 2px solid #4141E6 (--color-accent-blue) focused/active
- **Border Radius**: 15px (--radius-badge)
- **Spacing**: 5px (между элементами column)

**Typography (Top Helper):**
- **Font Size**: 10px (0.625rem)
- **Font Weight**: 600 (Semibold)
- **Line Height**: 1.40
- **Color**: #09101D (normal) или #4141E6 (blue accent для secondary info)
- **Использование**: "Balance: 0.10025 BTC", "~6.984$"

**Typography (Field Label/Value Two-Line):**
- **Top Line (Label)**: 12px, weight 400, color #747B84
- **Bottom Line (Value)**: 14px, weight 600, color #09101D или #23262B (--color-text-dark)
- **Использование**: "Your email" / "you@awesome.com", "Company" / "Dropbox"

**Typography (Bottom Helper - Success):**
- **Font Size**: 14px (0.875rem)
- **Font Weight**: 400 (Regular)
- **Color**: #11BB8D (--color-status-online) для success state
- **Emoji**: Поддержка emoji ("👍🏻")
- **Использование**: "Good name 👍🏻"

**Icon Specifications:**
- **Large Icon**: 30×30
  - Square: border-radius 10px
  - Circle: border-radius 50px
  - Background: #F4F6F9 (placeholder)
- **Medium Icon**: 24×24 (actions, indicators)
- **Small Icon**: ~12×12 (в 24px контейнере с padding 6px)

**Структура Advanced Input:**

```
Container: 375px, padding 16px/10px
├─ Spacing: 5px vertical
│
├─ Top Helper (optional): 10px, weight 600
│  ├─ Main text: color #09101D
│  └─ Secondary text: color #4141E6 (blue accent)
│
├─ Field: 375×46
│  ├─ Border: 2px solid #4141E6
│  ├─ Border Radius: 15px
│  ├─ Padding: 4px/20px/4px/15px
│  │
│  └─ Row Layout:
│     ├─ Left Icon (optional): 30×30 (square/circle)
│     ├─ Content: Expanded
│     │  ├─ Single Line: 14px, weight 600
│     │  └─ Two Lines:
│     │     ├─ Top: 12px, weight 400, #747B84
│     │     └─ Bottom: 14px, weight 600, #09101D
│     └─ Right Icons (optional): 24×24 or 30×30
│
└─ Bottom Helper (optional): 14px, weight 400
   └─ Success: color #11BB8D (green) + emoji support
```

**Variants:**

**1. With Top Helper (Balance Info)**
```
Top Helper: "Balance: 0.10025 BTC" + "~6.984$" (blue)
Field: "Enter amount" (14px/600)
```

**2. Single Line with Icon**
```
Left Icon: 30×30 (square/circle)
Text: "Netflix" or "you@awesome.com" (14px/600)
Right Icon: 24×24 (optional)
```

**3. Two-Line Content**
```
Top: "Company" or "Your email" (12px/400, #747B84)
Bottom: "Dropbox" or "you@awesome.com" (14px/600, #09101D)
Icons: 30×30 left, 24×24 right (optional)
```

**4. With Bottom Helper Success**
```
Field: "John" (14px/600)
Bottom Helper: "Good name 👍🏻" (14px/400, #11BB8D green)
```

**5. Multiple Icons**
```
Left: Icon 24×24 + Icon 30×30
Center: Text
Right: Multiple icons or dropdown indicator
```

**6. Currency/Crypto Display**
```
Left Icon: 30×30 (coin/currency logo)
Center: Value + Currency amount
Right: Icon 30×30 + Text label "BTC" + Icon 24×24
```

**Usage Guidelines:**
- **Field Height**: 46px для форм с иконками и двумя строками
- **Top Helper**: Балансы, дополнительная информация, constraints
- **Bottom Helper**: Validation (error/success), hints, character count
- **Two-Line**: Label вверху, value внизу для filled states
- **Icons**: 30×30 для coin/logo/avatar, 24×24 для actions
- **Success State**: Зеленый helper text #11BB8D + emoji для позитивного feedback
- **Emoji Support**: Можно использовать emoji в helper text

---

### 5. Bottom Sheet Components (из реального Flutter кода)

#### Bottom Sheet Container Specification

**Спецификация из кода:**
- **Container Width**: 375px
- **Border Radius**: 30px (top corners)
- **Background**: #FFFFFF (--color-bg-primary)
- **Clip Behavior**: antiAlias

**Pull Indicator (Drag Handle):**
- **Size**: 40px × 3px
- **Background**: #D9DDE2 (--color-bg-tertiary)
- **Border Radius**: 100px (fully rounded)
- **Container Padding**: 167px horizontal, 8px bottom (центрирование)
- **Top Spacing**: 10px

**Top Rounded Area (Decorative):**
- **Size**: 343px × 10px
- **Background**: #D9DDE2 (--color-bg-tertiary)
- **Border Radius**: 10px (только top-left и top-right)
- **Position**: 16px from left, 1px from top
- **Использование**: Декоративный элемент для визуального разделения

**Структура Bottom Sheet:**

```
Container: 375px, border-radius 30px (top)
├─ Status Bar Area: 375×44, background #09101D (optional)
│
├─ Top Rounded Decoration: 343×10, #D9DDE2
│  └─ Position: 16px left, 1px top
│
├─ Pull Indicator Container: padding 167px/8px
│  └─ Drag Handle: 40×3, #D9DDE2, border-radius 100px
│
└─ Content Area:
   ├─ Header (optional)
   ├─ Search (optional)
   └─ Main Content
```

**CSS пример:**

```css
.bottom-sheet {
  width: 375px;
  background: var(--color-bg-primary); /* white */
  border-radius: 30px 30px 0 0;
  clip-path: inset(0 round 30px 30px 0 0);
  overflow: hidden;
}

.bottom-sheet__top-decoration {
  width: 343px;
  height: 10px;
  margin: 1px 0 0 16px;
  background: var(--color-bg-tertiary); /* #D9DDE2 */
  border-radius: 10px 10px 0 0;
}

.bottom-sheet__pull-indicator-container {
  padding: 0 167px 8px;
  background: white;
  display: flex;
  justify-content: center;
}

.bottom-sheet__drag-handle {
  width: 40px;
  height: 3px;
  background: var(--color-bg-tertiary); /* #D9DDE2 */
  border-radius: 100px;
}

.bottom-sheet__content {
  background: white;
  padding: 0;
}
```

**Usage Guidelines:**
- **Pull Indicator**: Всегда включать для bottom sheet, чтобы показать drag interaction
- **Top Decoration**: Опциональный декоративный элемент для визуального разделения
- **Border Radius**: 30px для modern iOS-style bottom sheet
- **Background**: Всегда white для contrast с затемненным фоном
- **Accessibility**: Поддержка swipe down для закрытия, tap outside для dismiss

#### Section Title (Medium Heading)

**Спецификация из кода:**
- **Font Size**: 18px (1.125rem)
- **Font Weight**: 700 (Bold)
- **Font Family**: 'Archivo'
- **Line Height**: 1.40 (25.2px)
- **Color**: #09101D (--color-text-primary)
- **Padding**: 16px horizontal, 10px top
- **Spacing**: 10px bottom (column spacing)
- **Использование**: Заголовки секций внутри bottom sheet или content areas ("Select training date", "Choose category")

**CSS пример:**

```css
.section-title {
  font-family: 'Archivo';
  font-size: 18px;
  font-weight: 700;
  line-height: 1.40;
  color: var(--color-text-primary); /* #09101D */
  padding: 10px 16px 0;
}

.section-title + * {
  margin-top: 10px; /* spacing after title */
}
```

---

### 6. User/Trainer Card Grid (из реального Flutter кода)

#### User Card Grid Specification

**Спецификация из кода:**
- **Container Padding**: 16px horizontal
- **Row Padding**: 10px vertical
- **Horizontal Spacing**: 10px (между карточками)
- **Vertical Spacing**: 5px (между рядами) или 10px (между секциями)
- **Cards per Row**: 4 (равномерно Expanded)
- **Grid Layout**: Flexible wrap, responsive

**User/Trainer Card:**
- **Padding**: 10px (all sides)
- **Background**: #F4F6F9 (--color-bg-secondary)
- **Border Radius**: 15px (--radius-badge)
- **Spacing**: 5px (между avatar и name)
- **Layout**: Column (center aligned)

**Avatar Container:**
- **Outer Size**: 56×56
- **Inner Avatar Size**: 48×48
- **Inner Position**: left 4px, top 4px (создает padding 4px)
- **Background Placeholder**: #D9DDE2 (--color-bg-tertiary)
- **Border Radius**: 40px (--radius-avatar)
- **Image Fit**: cover
- **Использование**: User/trainer photos, team members, contacts

**Name Label:**
- **Font Size**: 11px (0.6875rem)
- **Font Weight**: 600 (Semibold)
- **Font Family**: 'Archivo'
- **Line Height**: 1.40 (15.4px)
- **Color**: #09101D (--color-text-primary)
- **Text Align**: center
- **Max Width**: 50px (с overflow ellipsis)

**Структура User Card:**

```
Card Container: padding 10px, background #F4F6F9
├─ Spacing: 5px vertical
│
├─ Avatar Container: 56×56
│  ├─ Background padding area: 4px
│  └─ Avatar: 48×48
│     ├─ Placeholder: #D9DDE2
│     ├─ Image: cover fit
│     └─ Border Radius: 40px
│
└─ Name Label: 11px, weight 600, centered
   └─ Max width: 50px
```

**Grid Layout:**

```
Container: padding 16px horizontal
└─ Row: padding 10px vertical, spacing 10px
   ├─ Card 1: Expanded (flex 1)
   ├─ Card 2: Expanded (flex 1)
   ├─ Card 3: Expanded (flex 1)
   └─ Card 4: Expanded (flex 1)
```

**CSS пример:**

```css
.user-card-grid {
  padding: 0 16px;
}

.user-card-row {
  display: flex;
  gap: 10px;
  padding: 10px 0;
}

.user-card {
  flex: 1;
  padding: 10px;
  background: var(--color-bg-secondary); /* #F4F6F9 */
  border-radius: var(--radius-badge); /* 15px */
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 5px;
}

.user-card__avatar-container {
  width: 56px;
  height: 56px;
  position: relative;
}

.user-card__avatar {
  width: 48px;
  height: 48px;
  position: absolute;
  left: 4px;
  top: 4px;
  background: var(--color-bg-tertiary); /* #D9DDE2 */
  border-radius: var(--radius-avatar); /* 40px */
  object-fit: cover;
}

.user-card__name {
  max-width: 50px;
  font-family: 'Archivo';
  font-size: 11px;
  font-weight: 600;
  line-height: 1.40;
  color: var(--color-text-primary);
  text-align: center;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
```

**Usage Guidelines:**
- **4 Cards per Row**: Стандартная сетка для mobile 375px
- **Avatar Padding**: 4px создает визуальный breathing room
- **Name Truncation**: Используйте ellipsis для длинных имен
- **Background**: Светлый #F4F6F9 для subtle emphasis на карточках
- **Spacing**: 10px horizontal, 5px между avatar и name
- **Accessibility**: Touch target 56×56 для avatar, tap на всю card для selection

#### Story Badge (Instagram-style Indicator)

**Спецификация из кода:**
- **Size**: 20×20
- **Position**: Top-right corner (left 36px, top 0 относительно 56×56 контейнера)
- **Border**: 2px solid #F4F6F9 (цвет фона карточки для отделения)
- **Border Radius**: 20px (--radius-notification)
- **Background**: Linear gradient #833AB4 → #FD1D1D → #FCB045 (Instagram colors)
- **Gradient Direction**: horizontal (0.00, 0.50) → (1.00, 0.50)

**Inner Icon Container:**
- **Size**: 12×12
- **Border Radius**: 100px
- **Padding**: 4px (container padding)
- **Icon Size**: 14.40×14.40 (внутри 12×12 container, с offset -1.20)
- **Использование**: Plus icon, play icon для story indicator

**Структура Story Badge:**

```
Avatar Container: 56×56 (relative positioning)
└─ Story Badge: 20×20, position absolute
   ├─ Position: left 36px, top 0 (right-top corner)
   ├─ Border: 2px solid #F4F6F9
   ├─ Gradient Background: #833AB4 → #FD1D1D → #FCB045
   └─ Icon Container: 12×12
      ├─ Border Radius: 100px
      └─ Icon: 14.40×14.40 (centered)
```

**CSS пример:**

```css
.user-card__avatar-container {
  width: 56px;
  height: 56px;
  position: relative;
}

.user-card__story-badge {
  width: 20px;
  height: 20px;
  position: absolute;
  left: 36px;
  top: 0;
  border: 2px solid var(--color-bg-secondary); /* #F4F6F9 - matches card bg */
  border-radius: var(--radius-notification); /* 20px */
  background: linear-gradient(90deg, #833AB4 0%, #FD1D1D 50%, #FCB045 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 1;
}

.user-card__story-badge__icon-container {
  width: 12px;
  height: 12px;
  border-radius: 100px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.user-card__story-badge__icon {
  width: 14.40px;
  height: 14.40px;
  /* Plus or play icon SVG */
}
```

**Варианты Story Badge:**

**1. Active Story (Gradient)**
```
Background: linear-gradient(90deg, #833AB4, #FD1D1D, #FCB045)
Border: 2px solid (background color)
Icon: Plus или Play (white or dark)
```

**2. Viewed Story (Gray)**
```
Background: #D9DDE2 (--color-bg-tertiary)
Border: 2px solid (background color)
Icon: Check или empty
```

**3. Live Story (Red)**
```
Background: #FC466B (--color-accent-pink)
Border: 2px solid (background color)
Icon: Camera или Live icon
```

**Usage Guidelines:**
- **Position**: Всегда top-right corner avatar для consistency
- **Border Color**: Должен совпадать с фоном карточки для visual separation
- **Gradient**: Instagram-style gradient для active/unwatched stories
- **Size**: 20×20 достаточно заметный, но не overwhelming
- **Z-Index**: Должен быть выше avatar
- **Accessibility**: Указать в aria-label "Has active story" или similar

---

### 7. Calendar Component (из реального Flutter кода)

#### Calendar Specification (Date Picker)

**Спецификация из кода:**
- **Container Padding**: 16px horizontal, 10px vertical
- **Layout**: Column с spacing 30px (?)
- **Grid**: 7 columns (days of week) × 5-6 rows

**Calendar Header:**
- **Height**: 40px
- **Month Text**: "February", 14px, weight 700, color #09101D
- **Month Container Padding**: 5px top/right/bottom
- **Spacing**: 10px между элементами
- **Year Container**: 40×40, padding 5px
- **Year Text**: "2022", 14px, weight 700, color #09101D
- **Dropdown Icon**: 24×24
- **Alignment**: Left-aligned month, year, icon в одной строке

**Calendar Cell (Day):**
- **Size**: 40×40
- **Text**: 12px (0.75rem), weight 500, line-height 1.40
- **Padding**: 5px (default state) или 10px (selected filled state)
- **Border Radius**: 15px (selected states only)

**Date States:**

**1. Other Month (Disabled/Inactive)**
```
Text: 12px, weight 500, no color (transparent/gray)
Background: transparent
Padding: 5px
Использование: Даты предыдущего/следующего месяца
```

**2. Current Month (Default)**
```
Text: #09101D (--color-text-primary)
Background: transparent
Padding: 5px
Cursor: pointer
```

**3. Unavailable (Disabled)**
```
Text: #D9DDE2 (--color-bg-tertiary)
Background: transparent
Padding: 5px
Cursor: not-allowed
Использование: Прошедшие даты или недоступные слоты
```

**4. Selected Outline (Hover/Focus)**
```
Border: 2px solid #09101D (--color-text-primary)
Border Radius: 15px
Text: #09101D
Background: transparent
Padding: adjusted for border (to maintain size)
```

**5. Selected Filled (Active/Confirmed)**
```
Background: #09101D (--color-text-primary)
Text: white
Border Radius: 15px
Padding: 10px
No border
```

**Структура Calendar:**

```
Calendar Container: padding 16px/10px
│
├─ Header: 40px height
│  ├─ Month: "February", 14px/700, padding 5px
│  ├─ Year: "2022", 14px/700, container 40×40
│  └─ Icon: 24×24 (dropdown)
│
└─ Grid: 7 columns
   ├─ Row padding: 4px vertical
   │
   └─ Cell: 40×40
      ├─ Default: padding 5px
      ├─ Selected outline: border 2px #09101D, radius 15px
      └─ Selected filled: padding 10px, bg #09101D, radius 15px
```

**CSS пример:**

```css
.calendar {
  padding: 10px 16px;
}

.calendar__header {
  height: 40px;
  display: flex;
  align-items: center;
  gap: 0;
}

.calendar__month {
  padding: 5px 5px 5px 0;
  font-family: 'Archivo';
  font-size: 14px;
  font-weight: 700;
  color: var(--color-text-primary);
}

.calendar__year {
  width: 40px;
  height: 40px;
  padding: 5px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: 'Archivo';
  font-size: 14px;
  font-weight: 700;
  color: var(--color-text-primary);
}

.calendar__dropdown-icon {
  width: 24px;
  height: 24px;
  margin-left: auto;
}

.calendar__grid {
  display: grid;
  grid-template-columns: repeat(7, 1fr);
  gap: 4px 0; /* 4px vertical, 0 horizontal */
}

.calendar__cell {
  width: 40px;
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 5px;
  font-family: 'Archivo';
  font-size: 12px;
  font-weight: 500;
  line-height: 1.40;
  text-align: center;
  cursor: pointer;
  transition: all 150ms;
}

.calendar__cell--current-month {
  color: var(--color-text-primary); /* #09101D */
}

.calendar__cell--other-month {
  color: transparent;
  cursor: default;
}

.calendar__cell--unavailable {
  color: var(--color-bg-tertiary); /* #D9DDE2 */
  cursor: not-allowed;
}

.calendar__cell--selected-outline {
  border: 2px solid var(--color-text-primary); /* #09101D */
  border-radius: 15px;
  padding: 3px; /* 5px - 2px border */
}

.calendar__cell--selected-filled {
  background: var(--color-text-primary); /* #09101D */
  color: white;
  border-radius: 15px;
  padding: 10px;
}

.calendar__cell:not(.calendar__cell--unavailable):not(.calendar__cell--other-month):hover {
  border: 2px solid var(--color-text-primary);
  border-radius: 15px;
  padding: 3px;
}
```

**Usage Guidelines:**
- **Cell Size**: 40×40 для comfortable touch target
- **Selected Outline**: Для hover/focus состояния
- **Selected Filled**: Для confirmed/active выбора
- **Unavailable Dates**: Светло-серый #D9DDE2 для past dates или disabled slots
- **Border Radius**: 15px matching input field style
- **Spacing**: 4px vertical между рядами для density
- **Month/Year**: Bold 14px для clear hierarchy
- **Accessibility**: Keyboard navigation (arrow keys), ARIA labels для dates
- **Range Selection**: Можно расширить для date range picker с start/end states

---

### 8. Badges & Tags (из реального Flutter кода)

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
