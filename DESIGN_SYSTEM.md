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
--color-text-charcoal: #23262B;    /* Очень темный серый для основного текста */
--color-text-meta: #303239;        /* Темно-серый для метаданных (даты, авторы) */
--color-text-gray: #373940;        /* Серый текст для подписей (Flutter) */
--color-text-subtitle: #414249;    /* Темно-серый для subtitle/вторичного текста в списках */
--color-text-muted: #747B84;       /* Приглушенный серый для timestamps и метаданных */
```

### Accent Colors

```css
/* Акцентные цвета */
--color-accent-blue: #1D4ED8;      /* blue-700 */
--color-accent-navy: #46467F;      /* Темно-синий для флагов и декоративных элементов */
--color-accent-purple: #7B61FF;    /* Фиолетовый из Flutter кода */
--color-accent-purple-dark: #5E38BA; /* Темно-фиолетовый для premium badges */
--color-link-blue: #4141E6;        /* Синий для ссылок и активных элементов */
--color-accent-cyan: #7CC5D6;      /* Светло-голубой для calendar appointments */
--color-accent-peach: #F7B68A;     /* Персиковый для calendar appointments */
--color-success-green: #11BB8D;    /* Зеленый для активного toggle и success состояний */
--color-error-red: #E24949;        /* Красный для ошибок и негативных значений */
--color-error-border: #DA1414;     /* Темно-красный для error borders */
--color-accent-yellow: #FFC043;    /* Желтый для date dividers */
--color-accent-dark-green: #05944F; /* Темно-зеленый для date dividers */
--color-accent-orange: #FF6937;    /* Оранжевый для date dividers и new messages */
```

### Background Colors

```css
/* Фоны для компонентов */
--color-bg-light: #F4F6F9;         /* Светлый фон */
--color-bg-ultralight: #F8F8FA;    /* Очень светлый фон для иконок и плейсхолдеров */
--color-bg-card-light: #D9DDE2;    /* Светлая карточка */
--color-bg-card-dark: #23262B;     /* Темная карточка */
--color-bg-teal: #B7D5D5;          /* Бирюзовый фон для декоративных элементов */
```

### Border & Control Colors

```css
/* Цвета для границ и контролов */
--color-border-light: #EAEEF2;     /* Светлая граница для неактивных элементов (Radio, Toggle, Checkbox) */
--color-control-inactive: #EAEEF2; /* Неактивные form controls */
```

### Overlay & Shadow Colors

```css
/* Overlay цвета для Flutter компонентов */
--overlay-black-30: rgba(0, 0, 0, 0.30);    /* Черный overlay 30% для бейджей и play button */
--overlay-black-50: rgba(29, 29, 29, 0.50); /* Черный overlay 50% (#7F1D1D1D) для градиентов на карточках */
--overlay-white-50: rgba(255, 255, 255, 0.50); /* Белый overlay 50% для текстовых блоков */
--overlay-yellow-40: rgba(255, 192, 67, 0.40); /* Желтый overlay 40% (#66FFC043) для points badge */

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

<!-- COMPONENT: Flutter Video/Content Card | CATEGORY: Cards, Media, Social | TAGS: video, content, social-proof, avatars, badges, author | RELATED: Flutter Overlay Badges, Flutter Avatar Groups, Flutter Author Info -->
##### Video/Content Card with Social Proof

Карточка видео/контента с социальными элементами: бейджи метрик, группа аватаров, информация об авторе.

**Card Container:**
- **Size**: 230px × 400px
- **Border Radius**: 16px
- **Content Padding**: 5px

**Image Section:**
- **Size**: 230px × 230px (full width)
- **Border Radius**: 15px
- **Overlay Badges**: Positioned at top with 10px padding

**Overlay Badges (Duration & Views):**
- **Height**: 24px
- **Padding**: Left 5px, Right 10px
- **Background**: rgba(0, 0, 0, 0.30) - black 30% opacity
- **Border Radius**: 10px
- **Icon Container**: 24×24px, padding 8px, border-radius 100px
- **Icon Size**: ~10px (positioned with -0.80 offset)
- **Typography**: 11px Archivo SemiBold (w600) white, line-height 1.40
- **Content**: "2:12" (duration left), "1.342" (views right)
- **Layout**: Space-between with 90px spacing
- **Usage**: Показывает длительность контента и количество просмотров

**Avatar Group (Overlapping with Border):**
- **Container Spacing**: 10px between avatars in Row
- **Each Avatar**:
  - Outer: 32×32px
  - Border: 4px solid white, border-radius 30px
  - Inner Background: #D9DDE2, 24×24px (positioned at 4px offset)
  - Image: 24×24px, border-radius 40px
- **Counter Avatar** (last item showing "1k"):
  - Same structure but with text instead of image
  - Text: "1k", 10px Archivo SemiBold (w600) white
  - Text positioned at top 7px (centered)
  - Container: 24×24px, height 18px for text
- **Total Display**: 5 avatars (4 images + 1 counter)
- **Usage**: Социальный proof - показывает участников/подписчиков

**Title:**
- **Width**: 220px (constrained)
- **Text**: "Home fitness program, 2 minutes per day"
- **Typography**: 16px Archivo Bold (w700) #09101D, line-height 1.40
- **Usage**: Заголовок контента

**Author Info:**
- **Avatar Outer**: 40×40px
- **Avatar Inner**: 32×32px (positioned at 4px offset), #D9DDE2 background
- **Avatar Image**: 32×32px, border-radius 40px
- **Name**: "Nicole Dowson", 13px Archivo SemiBold (w600) #09101D, line-height 1.40
- **Team/Role**: "Fitness App Team", 12px Archivo Regular (w400) #373940, line-height 1.40
- **Spacing**: 6px between avatar and text column

**Content Spacing:**
- Between avatar group and title: 10px
- Between sections within content: 5px
- Between title and author: 5px

```dart
// Video/Content Card - Full Structure
Container(
  width: 230,
  height: 400,
  clipBehavior: Clip.antiAlias,
  decoration: ShapeDecoration(
    shape: RoundedRectangleBorder(
      borderRadius: BorderRadius.circular(16),
    ),
  ),
  child: Column(
    children: [
      // Image with overlay badges
      Container(
        width: double.infinity,
        height: 230,
        decoration: ShapeDecoration(
          image: DecorationImage(
            image: NetworkImage("https://placehold.co/230x230"),
            fit: BoxFit.cover,
          ),
          shape: RoundedRectangleBorder(
            borderRadius: BorderRadius.circular(15),
          ),
        ),
        child: Row(
          mainAxisAlignment: MainAxisAlignment.spaceBetween,
          crossAxisAlignment: CrossAxisAlignment.start,
          children: [
            // Duration badge
            Container(
              padding: const EdgeInsets.all(10),
              child: Container(
                height: 24,
                padding: const EdgeInsets.only(left: 5, right: 10),
                decoration: ShapeDecoration(
                  color: Colors.black.withValues(alpha: 0.30),
                  shape: RoundedRectangleBorder(
                    borderRadius: BorderRadius.circular(10),
                  ),
                ),
                child: Row(
                  children: [
                    Container(width: 24, height: 24, padding: const EdgeInsets.all(8)),
                    Text(
                      '2:12',
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
              ),
            ),
            // Views badge
            Container(
              padding: const EdgeInsets.all(10),
              child: Container(
                height: 24,
                padding: const EdgeInsets.only(left: 5, right: 10),
                decoration: ShapeDecoration(
                  color: Colors.black.withValues(alpha: 0.30),
                  shape: RoundedRectangleBorder(
                    borderRadius: BorderRadius.circular(10),
                  ),
                ),
                child: Row(
                  children: [
                    Container(width: 24, height: 24, padding: const EdgeInsets.all(8)),
                    Text(
                      '1.342',
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
              ),
            ),
          ],
        ),
      ),
      // Content section
      Container(
        width: double.infinity,
        padding: const EdgeInsets.all(5),
        child: Column(
          spacing: 5,
          children: [
            // Avatar group
            Row(
              spacing: 10,
              children: [
                // Avatar with white border (repeated 4 times)
                Container(
                  width: 32,
                  height: 32,
                  child: Stack(
                    children: [
                      Container(
                        width: 32,
                        height: 32,
                        decoration: ShapeDecoration(
                          shape: RoundedRectangleBorder(
                            side: BorderSide(width: 4, color: Colors.white),
                            borderRadius: BorderRadius.circular(30),
                          ),
                        ),
                      ),
                      Positioned(
                        left: 4,
                        top: 4,
                        child: Container(
                          width: 24,
                          height: 24,
                          decoration: ShapeDecoration(
                            image: DecorationImage(
                              image: NetworkImage("https://placehold.co/24x24"),
                              fit: BoxFit.cover,
                            ),
                            shape: RoundedRectangleBorder(
                              borderRadius: BorderRadius.circular(40),
                            ),
                          ),
                        ),
                      ),
                    ],
                  ),
                ),
                // Counter avatar
                Container(
                  width: 32,
                  height: 32,
                  child: Stack(
                    children: [
                      Container(
                        decoration: ShapeDecoration(
                          shape: RoundedRectangleBorder(
                            side: BorderSide(width: 4, color: Colors.white),
                            borderRadius: BorderRadius.circular(30),
                          ),
                        ),
                      ),
                      Positioned(
                        left: 4,
                        top: 7,
                        child: Text(
                          '1k',
                          textAlign: TextAlign.center,
                          style: TextStyle(
                            color: Colors.white,
                            fontSize: 10,
                            fontFamily: 'Archivo',
                            fontWeight: FontWeight.w600,
                            height: 1.40,
                          ),
                        ),
                      ),
                    ],
                  ),
                ),
              ],
            ),
            // Title
            SizedBox(
              width: 220,
              child: Text(
                'Home fitness program, 2 minutes per day',
                style: TextStyle(
                  color: const Color(0xFF09101D),
                  fontSize: 16,
                  fontFamily: 'Archivo',
                  fontWeight: FontWeight.w700,
                  height: 1.40,
                ),
              ),
            ),
            // Author info
            Row(
              spacing: 6,
              children: [
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
                            image: DecorationImage(
                              image: NetworkImage("https://placehold.co/32x32"),
                              fit: BoxFit.cover,
                            ),
                            shape: RoundedRectangleBorder(
                              borderRadius: BorderRadius.circular(40),
                            ),
                          ),
                        ),
                      ),
                    ],
                  ),
                ),
                Column(
                  crossAxisAlignment: CrossAxisAlignment.start,
                  children: [
                    Text(
                      'Nicole Dowson',
                      style: TextStyle(
                        color: const Color(0xFF09101D),
                        fontSize: 13,
                        fontFamily: 'Archivo',
                        fontWeight: FontWeight.w600,
                        height: 1.40,
                      ),
                    ),
                    Text(
                      'Fitness App Team',
                      style: TextStyle(
                        color: const Color(0xFF373940),
                        fontSize: 12,
                        fontFamily: 'Archivo',
                        fontWeight: FontWeight.w400,
                        height: 1.40,
                      ),
                    ),
                  ],
                ),
              ],
            ),
          ],
        ),
      ),
    ],
  ),
)
```

**Usage Notes:**
- Карточка объединяет несколько паттернов: медиа контент + социальные элементы + авторство
- Avatar group с белой обводкой создает визуальный "стек" участников
- Counter avatar показывает общее количество когда слишком много для отображения
- Overlay badges используют одинаковую структуру для consistency
- Author info внизу добавляет credibility контенту
- Ideal для: видео уроков, фитнес программ, курсов, туториалов

<!-- CROSS-REFERENCE: See also "Flutter Overlay Badges" for badge variations, "Flutter Avatar Groups" for avatar patterns, "Flutter Author Info" for creator details -->

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

#### Flutter Text Input Fields

Текстовые поля ввода из Flutter кода с полным набором состояний для мобильного приложения.

**Общие спецификации:**
- **Container Width**: 375px
- **Container Padding**: Horizontal 16px, Vertical 5px
- **Input Height**: 36px
- **Input Padding**: Left 16px, Right 20px
- **Border Radius**: 15px
- **Icon Size**: 20px × 20px
- **Cursor Width**: 2px, Height: 16px
- **Spacing**: 8px between label/input/helper

**Typography:**
- **Label**: 14px, Archivo SemiBold (w600), Line Height: 1.40
- **Input Text**: 14px, Archivo Regular (w400), Line Height: 1.40
- **Helper Text**: 14px, Archivo Regular (w400), Line Height: 1.40
- **Error Message**: 14px, Archivo Regular (w400), Line Height: 1.40

##### States:

**1. Enabled (Default)**
- **Background**: #F4F6F9 (light gray)
- **Border**: none
- **Label Color**: #09101D
- **Placeholder**: "00.00", color #747B84
- **Helper Color**: #747B84
- **Left Icon**: 20px, color depends on icon
- **Usage**: Начальное состояние, поле готово к вводу

```dart
Container(
  width: double.infinity,
  height: 36,
  padding: const EdgeInsets.only(left: 16, right: 20),
  decoration: ShapeDecoration(
    color: const Color(0xFFF4F6F9),
    shape: RoundedRectangleBorder(
      borderRadius: BorderRadius.circular(15),
    ),
  ),
)
```

**2. Focus**
- **Background**: #F4F6F9 (light gray)
- **Border**: 2px solid #09101D (dark)
- **Label Color**: #09101D
- **Placeholder**: "00.00", color #747B84
- **Helper Color**: #747B84
- **Cursor**: Visible (2px × 16px)
- **Usage**: Поле получило фокус, готово к вводу

**3. Active - Typing**
- **Background**: #F4F6F9 (light gray)
- **Border**: 2px solid #09101D (dark)
- **Label Color**: #09101D
- **Input Text**: "00.00", color #747B84
- **Helper Color**: #747B84
- **Cursor**: Visible (2px × 16px)
- **Right Icon**: 20px (close/clear icon)
- **Usage**: Активный ввод текста, возможность очистить

**4. Pressed**
- **Background**: #EAEEF2 (darker gray)
- **Border**: none
- **Label Color**: #09101D
- **Placeholder**: "00.00", color #747B84
- **Helper Color**: #747B84
- **Usage**: Момент нажатия на поле

**5. Complete**
- **Background**: #F4F6F9 (light gray)
- **Border**: none
- **Label Color**: #09101D
- **Input Text**: "14.95", color #09101D (dark, not placeholder)
- **Helper Color**: #747B84
- **Right Icon**: 20px (checkmark icon)
- **Usage**: Поле успешно заполнено

**6. Incomplete**
- **Background**: #F4F6F9 (light gray)
- **Border**: none
- **Label Color**: #09101D
- **Placeholder**: "00.00", color #747B84
- **Helper Color**: #747B84
- **Right Icon**: 20px (warning icon)
- **Usage**: Поле требует заполнения

**7. Positive (Success)**
- **Background**: rgba(17, 187, 141, 0.05) - #11BB8D with 5% opacity
- **Border**: 2px solid #11BB8D (success green)
- **Label Color**: #09101D
- **Input Text**: "14.95", color #09101D
- **Helper Color**: #747B84
- **Cursor**: Visible (2px × 16px)
- **Usage**: Успешная валидация значения

```dart
Container(
  decoration: ShapeDecoration(
    color: const Color(0x0C11BB8D), // rgba(17, 187, 141, 0.05)
    shape: RoundedRectangleBorder(
      side: BorderSide(width: 2, color: const Color(0xFF11BB8D)),
      borderRadius: BorderRadius.circular(15),
    ),
  ),
)
```

**8. Negative (Error)**
- **Background**: rgba(218, 20, 20, 0.05) - #DA1414 with 5% opacity
- **Border**: 2px solid #DA1414 (error red)
- **Label Color**: #09101D
- **Input Text**: "99.999", color #747B84
- **Helper Text**: "Error message", color #E24949 (error red)
- **Cursor**: Visible (2px × 16px)
- **Usage**: Ошибка валидации, некорректное значение

```dart
Container(
  decoration: ShapeDecoration(
    color: const Color(0x0CDA1414), // rgba(218, 20, 20, 0.05)
    shape: RoundedRectangleBorder(
      side: BorderSide(width: 2, color: const Color(0xFFDA1414)),
      borderRadius: BorderRadius.circular(15),
    ),
  ),
)
```

**9. Disabled**
- **Background**: #EAEEF2 (gray)
- **Border**: none
- **Label Color**: #D9DDE2 (light gray)
- **Placeholder**: "00.00", color #747B84
- **Helper Color**: #D9DDE2 (light gray)
- **Usage**: Поле отключено, ввод невозможен

**Usage Notes:**
- Используйте Positive state для подтверждения корректного ввода
- Negative state всегда с error message внизу
- Complete state показывает успешное заполнение без валидации
- Active - Typing включает иконку очистки справа
- Focus отличается от Active наличием введенного текста

---

#### Flutter Dropdown/Select Fields

Поля выбора (dropdown/select) из Flutter кода для мобильного приложения с различными вариантами компоновки.

**Общие спецификации:**
- **Container Width**: 375px
- **Container Padding**: Horizontal 16px, Vertical 10px
- **Input Height**: 46px (выше чем у text input!)
- **Input Padding**: Top 4px, Bottom 4px, Left 20px, Right 15px
- **Border Radius**: 15px
- **Border**: 2px solid #F4F6F9 (disabled state)
- **Icon Size**: 30px × 30px (квадратные и круглые)
- **Chevron Icon**: 24px × 24px
- **Spacing**: 5px, 8px, 10px между элементами

**Typography:**
- **Label**: 12px, Archivo Regular (w400), Line Height: 1.67
- **Value Text**: 14px, Archivo SemiBold (w600), Line Height: 1.43
- **Helper Text**: 12px, Archivo Regular (w400), Line Height: 1.67

**Icon Specifications:**
- **Square Icons**: 30×30px, border-radius 10px
- **Circle Icons**: 30×30px, border-radius 50% (full circle)
- **Chevron Icons**: 24×24px, positioned right

##### Variants:

**1. Single Line with Square Icon**
- **Layout**: Square icon (30px) + Single line text
- **Text Color**: #D9DDE2 (disabled)
- **Example**: Netflix service selector
- **Icon**: Square with 10px border-radius
- **Spacing**: 8px between icon and text

**2. Two-Line with Circle Icon + Chevron**
- **Layout**: Circle icon (30px) + Label + Value + Chevron (24px)
- **Label**: 12px, positioned above value
- **Value**: 14px SemiBold, main text
- **Text Color**: #D9DDE2 (disabled)
- **Example**: Company/Dropbox selector
- **Icon**: Circle (border-radius 50px)
- **Spacing**: 5px between label and value, 8px between icon and text

```dart
Container(
  width: 375,
  padding: const EdgeInsets.symmetric(horizontal: 16, vertical: 10),
  decoration: BoxDecoration(color: Colors.white),
  child: Container(
    height: 46,
    padding: const EdgeInsets.only(top: 4, bottom: 4, left: 20, right: 15),
    decoration: ShapeDecoration(
      color: const Color(0xFFF4F6F9),
      shape: RoundedRectangleBorder(
        side: BorderSide(width: 2, color: const Color(0xFFF4F6F9)),
        borderRadius: BorderRadius.circular(15),
      ),
    ),
    child: Row(
      children: [
        // Circle icon 30×30
        Container(
          width: 30,
          height: 30,
          decoration: ShapeDecoration(
            shape: OvalBorder(),
          ),
        ),
        SizedBox(width: 8),
        // Label + Value
        Expanded(
          child: Column(
            crossAxisAlignment: CrossAxisAlignment.start,
            mainAxisAlignment: MainAxisAlignment.center,
            children: [
              Text('Company', style: TextStyle(fontSize: 12)), // Label
              SizedBox(height: 5),
              Text('Dropbox', style: TextStyle(fontSize: 14, fontWeight: FontWeight.w600)), // Value
            ],
          ),
        ),
        // Chevron icon 24×24
        Container(width: 24, height: 24),
      ],
    ),
  ),
)
```

**3. Two-Line without Icon**
- **Layout**: Label + Value only
- **Label**: 12px, positioned above value
- **Value**: 14px SemiBold, main text
- **Text Color**: #D9DDE2 (disabled)
- **Example**: Your email field
- **Spacing**: 5px between label and value

**4. Two-Line without Icon + Helper Text**
- **Layout**: Label + Value with helper text below container
- **Label**: 12px, positioned above value
- **Value**: 14px SemiBold, main text
- **Helper**: 12px, positioned below input, color #747B84
- **Text Color**: #D9DDE2 (disabled)
- **Example**: Your name field with helper
- **Spacing**: 5px between label and value, 8px after container

**5. Two-Line with Square Icon + Chevron**
- **Layout**: Square icon (30px) + Label + Value + Chevron (24px)
- **Label**: 12px, positioned above value
- **Value**: 14px SemiBold, main text
- **Text Color**: #D9DDE2 (disabled)
- **Example**: Crypto amount selector
- **Icon**: Square with 10px border-radius
- **Spacing**: 5px between label and value, 8px between icon and text

**6. Two-Line with Circle Icon + Chevron (Crypto)**
- **Layout**: Circle icon (30px) + Label + Value + Chevron (24px)
- **Label**: 12px, positioned above value
- **Value**: 14px SemiBold, main text
- **Text Color**: #D9DDE2 (disabled)
- **Example**: Bitcoin amount selector
- **Icon**: Circle (border-radius 50px)
- **Spacing**: 5px between label and value, 8px between icon and text

**7. Single Line Long Text + Circle Icon + Ticker + Chevron**
- **Layout**: Circle icon (30px) + Long text value + Ticker + Chevron (24px)
- **Value**: 14px SemiBold, truncated if needed
- **Ticker**: Small badge/label
- **Text Color**: #D9DDE2 (disabled)
- **Example**: Bitcoin address selector
- **Icon**: Circle (border-radius 50px)
- **Spacing**: 8px between elements

**8. Circle Icon Only + Chevron on Left**
- **Layout**: Chevron left (24px) + Circle icon (30px) + Chevron right (24px)
- **Text**: Minimal or icon-based (e.g., BTC ticker)
- **Text Color**: #D9DDE2 (disabled)
- **Example**: Currency switcher
- **Icon**: Circle (border-radius 50px)
- **Special**: Chevrons on both sides for navigation

**9. Circle Icon with Two Chevrons**
- **Layout**: Circle icon (30px) + Chevrons for conversion
- **Text Color**: #D9DDE2 (disabled)
- **Example**: Currency conversion selector
- **Icon**: Circle (border-radius 50px)
- **Special**: Indicates conversion or exchange functionality

**10. Circle Icon + Chevron + Two-Line Right-Aligned**
- **Layout**: Circle icon (30px) + Chevron + Label + Value (right-aligned)
- **Label**: 12px, positioned above value, right-aligned
- **Value**: 14px SemiBold, right-aligned
- **Text Color**: #D9DDE2 (disabled)
- **Example**: Price conversion display
- **Icon**: Circle (border-radius 50px)
- **Spacing**: 5px between label and value

```dart
Container(
  width: 375,
  padding: const EdgeInsets.symmetric(horizontal: 16, vertical: 10),
  decoration: BoxDecoration(color: Colors.white),
  child: Container(
    height: 46,
    padding: const EdgeInsets.only(top: 4, bottom: 4, left: 20, right: 15),
    decoration: ShapeDecoration(
      color: const Color(0xFFF4F6F9),
      shape: RoundedRectangleBorder(
        side: BorderSide(width: 2, color: const Color(0xFFF4F6F9)),
        borderRadius: BorderRadius.circular(15),
      ),
    ),
    child: Row(
      children: [
        // Circle icon 30×30
        Container(
          width: 30,
          height: 30,
          decoration: ShapeDecoration(
            shape: OvalBorder(),
          ),
        ),
        SizedBox(width: 8),
        // Chevron icon 24×24
        Container(width: 24, height: 24),
        SizedBox(width: 8),
        // Right-aligned Label + Value
        Expanded(
          child: Column(
            crossAxisAlignment: CrossAxisAlignment.end,
            mainAxisAlignment: MainAxisAlignment.center,
            children: [
              Text('Label', style: TextStyle(fontSize: 12)), // Label
              SizedBox(height: 5),
              Text('Value', style: TextStyle(fontSize: 14, fontWeight: FontWeight.w600)), // Value
            ],
          ),
        ),
      ],
    ),
  ),
)
```

**Usage Notes:**
- Input height 46px отличается от text input (36px) для лучшей читаемости dropdown содержимого
- В disabled state все тексты используют цвет #D9DDE2
- Квадратные иконки с border-radius 10px, круглые с border-radius 50px
- Chevron иконки всегда 24×24px для унификации
- Двухстрочные варианты (label + value) используют spacing 5px между строками
- Container padding 10px vertical (больше чем у text input) для dropdown content
- Border 2px в disabled state совпадает с background color (#F4F6F9)

---

#### Flutter Form Controls

Компоненты форм из Flutter кода для мобильного приложения.

##### Radio Button

- **Size**: 24px × 24px (outer container)
- **Padding**: 2px
- **Radio Circle**: 20px × 20px
- **Border Width**: 3px

**States:**
- **Unchecked**:
  - Border Color: #EAEEF2
  - Background: transparent

- **Checked**:
  - Border Color: #4141E6
  - Inner Circle: 10px × 10px, Color: #4141E6

- **Disabled**:
  - Border Color: #0B24FB with 33% opacity (rgba(11, 36, 251, 0.33))
  - Inner Circle: 10px × 10px, Color: #0B24FB with 33% opacity

```dart
// Checked Radio Button
Container(
  width: 24,
  height: 24,
  padding: const EdgeInsets.all(2),
  child: Row(
    mainAxisSize: MainAxisSize.min,
    children: [
      Container(
        width: 20,
        height: 20,
        decoration: ShapeDecoration(
          shape: OvalBorder(
            side: BorderSide(width: 3, color: const Color(0xFF4141E6)),
          ),
        ),
      ),
      Container(
        width: 10,
        height: 10,
        decoration: ShapeDecoration(
          color: const Color(0xFF4141E6),
          shape: OvalBorder(),
        ),
      ),
    ],
  ),
)
```

##### Toggle Switch

Два размера переключателей из Flutter кода.

**Large Toggle (51px × 31px):**
- **Track Width**: 51px
- **Track Height**: 31px (height не указан явно, определяется thumb)
- **Track Border Radius**: 40px (fully rounded)
- **Thumb Size**: 31px × 31px
- **Thumb Border**: 2px solid (matches track color)
- **Thumb Border Radius**: 40px

**Small Toggle (32px × 20px):**
- **Track Width**: 32px
- **Track Height**: 20px (height не указан явно, определяется thumb)
- **Track Border Radius**: 40px (fully rounded)
- **Thumb Size**: 20px × 20px
- **Thumb Border**: 2px solid (matches track color)
- **Thumb Border Radius**: 40px

**States (для обоих размеров):**
- **Off State**:
  - Track Color: #EAEEF2
  - Thumb Color: White (#FFFFFF)
  - Thumb Border: #EAEEF2
  - Alignment: Left (mainAxisAlignment: start)
  - Spacing: 10px (для small toggle)

- **On State (Active)**:
  - Track Color: #11BB8D (зеленый для active state)
  - Thumb Color: White (#FFFFFF)
  - Thumb Border: #11BB8D
  - Alignment: Right (mainAxisAlignment: end)

- **On State (Alternative - Blue)**:
  - Track Color: #4141E6
  - Thumb Color: White (#FFFFFF)
  - Thumb Border: #4141E6
  - Alignment: Right (mainAxisAlignment: end)

- **Disabled State**:
  - Opacity: 0.30
  - Track Color: #11BB8D или #4141E6
  - Thumb Color: #F4F6F9
  - Thumb Border: matches track color
  - Spacing: 10px

```dart
// Large Toggle - On State (Active/Green)
Container(
  width: 51,
  decoration: ShapeDecoration(
    color: const Color(0xFF11BB8D),
    shape: RoundedRectangleBorder(borderRadius: BorderRadius.circular(40)),
  ),
  child: Row(
    mainAxisSize: MainAxisSize.min,
    mainAxisAlignment: MainAxisAlignment.end,
    children: [
      Container(
        width: 31,
        height: 31,
        decoration: ShapeDecoration(
          color: Colors.white,
          shape: RoundedRectangleBorder(
            side: BorderSide(width: 2, color: const Color(0xFF11BB8D)),
            borderRadius: BorderRadius.circular(40),
          ),
        ),
      ),
    ],
  ),
)
```

##### Checkbox

- **Outer Container**: 24px × 24px
- **Checkbox Box**: 18px × 18px
- **Position**: Left 3.21px, Top 3px (centered)
- **Border Width**: 2px (strokeAlign: center)
- **Border Radius**: 2px

**States:**
- **Unchecked**:
  - Border Color: #EAEEF2
  - Background: transparent

- **Checked**:
  - Background Color: #4141E6 (предположительно)
  - Border Color: #4141E6
  - Checkmark Icon: White

- **Disabled**:
  - Opacity: 0.30 (предположительно)

```dart
// Unchecked Checkbox
Container(
  width: 24,
  height: 24,
  child: Stack(
    children: [
      Positioned(
        left: 3.21,
        top: 3,
        child: Container(
          width: 18,
          height: 18,
          decoration: ShapeDecoration(
            shape: RoundedRectangleBorder(
              side: BorderSide(
                width: 2,
                strokeAlign: BorderSide.strokeAlignCenter,
                color: const Color(0xFFEAEEF2),
              ),
              borderRadius: BorderRadius.circular(2),
            ),
          ),
        ),
      ),
    ],
  ),
)
```

**Radio Button Group Container:**
- **Width**: 371.50px
- **Height**: 140px
- **Padding**: 50px
- **Border**: 1px solid #4141E6
- **Border Radius**: 15px
- **Spacing**: 50px between radio buttons

---

#### Flutter Navigation Header

Навигационный заголовок для социального/сервисного приложения с аватаром и бейджами.

**Общие спецификации:**
- **Container Height**: 44px
- **Background**: White (#FFFFFF)
- **Layout**: Horizontal row with space-between alignment

**Компоненты:**

**1. Avatar Section:**
- **Container**: Padding left 16px, top/bottom 10px
- **Avatar Outer**: 32px × 32px
- **Avatar Inner**: 24px × 24px (positioned at 4px offset)
- **Avatar Border Radius**: 40px (full circle)
- **Avatar Background**: #D9DDE2 (placeholder)
- **Avatar Image**: 24px × 24px, border-radius 40px

**2. Premium Badge ("Get $5"):**
- **Container Height**: 24px (calculated from 44px - 10px padding × 2)
- **Padding**: 10px horizontal
- **Background**: #5E38BA (темно-фиолетовый)
- **Border Radius**: 11px
- **Typography**: 11px, Archivo SemiBold (w600), white, line-height 1.40
- **Text**: "Get $5"
- **Spacing**: 6px (internal spacing for content)

```dart
Container(
  height: 24,
  padding: const EdgeInsets.symmetric(horizontal: 10),
  decoration: ShapeDecoration(
    color: const Color(0xFF5E38BA),
    shape: RoundedRectangleBorder(
      borderRadius: BorderRadius.circular(11),
    ),
  ),
  child: Row(
    mainAxisSize: MainAxisSize.min,
    mainAxisAlignment: MainAxisAlignment.center,
    crossAxisAlignment: CrossAxisAlignment.center,
    spacing: 6,
    children: [
      Text(
        'Get \$5',
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

**3. Points Badge:**
- **Container Height**: 36px
- **Container Padding**: 16px horizontal, 10px vertical (outer container)
- **Badge Padding**: 10px horizontal, 5px vertical
- **Background**: #FFC043 with 40% opacity (0x66FFC043)
- **Border Radius**: 15px
- **Icon**: 24px × 24px, padding 2px, border-radius 100px
- **Typography**: 16px, Archivo ExtraBold (w800), #23262B, line-height 1.40
- **Text**: "Points"
- **Spacing**: 6px between icon and text

```dart
Container(
  height: 36,
  padding: const EdgeInsets.symmetric(horizontal: 10, vertical: 5),
  decoration: ShapeDecoration(
    color: const Color(0x66FFC043), // 40% opacity
    shape: RoundedRectangleBorder(
      borderRadius: BorderRadius.circular(15),
    ),
  ),
  child: Row(
    mainAxisSize: MainAxisSize.min,
    mainAxisAlignment: MainAxisAlignment.center,
    crossAxisAlignment: CrossAxisAlignment.center,
    spacing: 6,
    children: [
      Container(
        width: 24,
        height: 24,
        padding: const EdgeInsets.all(2),
        decoration: ShapeDecoration(
          shape: RoundedRectangleBorder(
            borderRadius: BorderRadius.circular(100),
          ),
        ),
      ),
      Text(
        'Points',
        style: TextStyle(
          color: const Color(0xFF23262B),
          fontSize: 16,
          fontFamily: 'Archivo',
          fontWeight: FontWeight.w800,
          height: 1.40,
        ),
      ),
    ],
  ),
)
```

**Usage Notes:**
- Premium badge (#5E38BA) используется для промо-акций и специальных предложений
- Points badge с полупрозрачным желтым фоном для визуального акцента без яркости
- Avatar 32×32px (outer) стандартный размер для compact headers
- Все бейджи используют rounded углы для мягкого дизайна

---

#### Flutter Search Input

Поисковое поле для мобильного приложения.

**Общие спецификации:**
- **Container Height**: 44px
- **Container Padding**: Horizontal 16px, Vertical 4px
- **Input Container Height**: 36px (calculated: 44 - 4×2)
- **Input Padding**: Horizontal 8px, Vertical 7px
- **Background**: #F4F6F9 (light gray)
- **Border Radius**: 15px
- **Border**: none

**Внутренний контент:**
- **Content Padding**: Left 5px, Right 10px
- **Icon**: 14px × 14px
- **Text**: "Search", #747B84 (placeholder gray)
- **Typography**: 16px, Archivo Regular (w400), line-height 1.40
- **Spacing**: 10px between icon and text

```dart
Container(
  width: double.infinity,
  height: 44,
  padding: const EdgeInsets.symmetric(horizontal: 16, vertical: 4),
  child: Row(
    mainAxisSize: MainAxisSize.min,
    mainAxisAlignment: MainAxisAlignment.start,
    crossAxisAlignment: CrossAxisAlignment.center,
    children: [
      Expanded(
        child: Container(
          height: double.infinity,
          padding: const EdgeInsets.symmetric(horizontal: 8, vertical: 7),
          decoration: ShapeDecoration(
            color: const Color(0xFFF4F6F9),
            shape: RoundedRectangleBorder(
              borderRadius: BorderRadius.circular(15),
            ),
          ),
          child: Row(
            mainAxisSize: MainAxisSize.min,
            mainAxisAlignment: MainAxisAlignment.start,
            crossAxisAlignment: CrossAxisAlignment.center,
            children: [
              Expanded(
                child: Container(
                  padding: const EdgeInsets.only(left: 5, right: 10),
                  child: Row(
                    mainAxisSize: MainAxisSize.min,
                    mainAxisAlignment: MainAxisAlignment.start,
                    crossAxisAlignment: CrossAxisAlignment.center,
                    spacing: 10,
                    children: [
                      Container(
                        width: 14,
                        height: 14,
                      ),
                      Text(
                        'Search',
                        style: TextStyle(
                          color: const Color(0xFF747B84),
                          fontSize: 16,
                          fontFamily: 'Archivo',
                          fontWeight: FontWeight.w400,
                          height: 1.40,
                        ),
                      ),
                    ],
                  ),
                ),
              ),
            ],
          ),
        ),
      ),
    ],
  ),
)
```

**Usage Notes:**
- Input height 36px (меньше чем у dropdown 46px) для компактного search поля
- Icon 14×14px меньше стандартных 20×20px для визуального баланса
- Placeholder text 16px для лучшей читаемости
- Отсутствие border для минималистичного дизайна

---

#### Flutter Category Cards (Horizontal Scroll)

Горизонтальная прокручиваемая галерея карточек категорий для сервисного приложения.

**Общие спецификации:**
- **Container Padding**: Top 10px, Left 16px, Bottom 10px
- **Card Size**: 100px × 120px
- **Border Radius**: 12px
- **Card Spacing**: 10px between cards
- **Scroll Direction**: Horizontal

**Card Variants:**

**1. Selected State (Active Card):**
- **Border**: 2px solid #4141E6 (blue)
- **Container**: 100px × 120px
- **Inner Padding**: 4px (from border to image)
- **Image Size**: 92px × 112px (100 - 4×2 padding)
- **Image Border Radius**: 10px (inner)
- **Gradient Overlay**: Starts at 51.16px from top, height 64.84px
- **Gradient Colors**: transparent (#00C4C4C4) → semi-dark (#7F1D1D1D - 50% opacity)
- **Text Position**: 83.08px from top, 10px padding left/bottom
- **Text Width**: 80px
- **Text**: 10px, Archivo SemiBold (w600), white, line-height 1.40
- **Example**: "Manicure"

```dart
Container(
  width: 100,
  height: 120,
  clipBehavior: Clip.antiAlias,
  decoration: ShapeDecoration(
    color: Colors.white,
    shape: RoundedRectangleBorder(
      borderRadius: BorderRadius.circular(12),
    ),
  ),
  child: Stack(
    children: [
      // Border container
      Container(
        width: 100,
        height: 120,
        decoration: ShapeDecoration(
          color: Colors.white,
          shape: RoundedRectangleBorder(
            side: BorderSide(
              width: 2,
              color: const Color(0xFF4141E6),
            ),
            borderRadius: BorderRadius.circular(14),
          ),
        ),
      ),
      // Image with 4px offset
      Positioned(
        left: 4,
        top: 4,
        child: Container(
          width: 92,
          height: 112,
          decoration: ShapeDecoration(
            image: DecorationImage(
              image: NetworkImage("https://placehold.co/92x112"),
              fit: BoxFit.cover,
            ),
            shape: RoundedRectangleBorder(
              borderRadius: BorderRadius.circular(10),
            ),
          ),
        ),
      ),
      // Gradient overlay
      Positioned(
        left: 4,
        top: 51.16,
        child: Container(
          width: 92,
          height: 64.84,
          decoration: ShapeDecoration(
            gradient: LinearGradient(
              begin: Alignment(0.50, -0.00),
              end: Alignment(0.50, 1.00),
              colors: [const Color(0x00C4C4C4), const Color(0x7F1D1D1D)],
            ),
            shape: RoundedRectangleBorder(
              borderRadius: BorderRadius.only(
                bottomLeft: Radius.circular(10),
                bottomRight: Radius.circular(10),
              ),
            ),
          ),
        ),
      ),
      // Text label
      Positioned(
        left: 0,
        top: 83.08,
        child: Container(
          width: 100,
          height: 36.92,
          padding: const EdgeInsets.only(left: 10, right: 10, bottom: 10),
          child: Row(
            children: [
              SizedBox(
                width: 80,
                child: Text(
                  'Manicure',
                  style: TextStyle(
                    color: Colors.white,
                    fontSize: 10,
                    fontFamily: 'Archivo',
                    fontWeight: FontWeight.w600,
                    height: 1.40,
                  ),
                ),
              ),
            ],
          ),
        ),
      ),
    ],
  ),
)
```

**2. Normal State (Unselected Card):**
- **Border**: none
- **Image Size**: 100px × 120px (full card size)
- **Image Border Radius**: 12px (matches card)
- **Gradient Overlay**: Starts at 50px from top, height 70px
- **Gradient Colors**: transparent (#00C4C4C4) → semi-dark (#7F1D1D1D - 50% opacity)
- **Text Position**: 83.08px from top, 10px padding left, bottom 10px
- **Text Width**: 90px
- **Text**: 10px, Archivo SemiBold (w600), white, line-height 1.40
- **Examples**: "Pedicure", "Makeup", "Hair cut", "Category or\nservice"

```dart
Container(
  width: 100,
  height: 120,
  clipBehavior: Clip.antiAlias,
  decoration: ShapeDecoration(
    color: Colors.white,
    shape: RoundedRectangleBorder(
      borderRadius: BorderRadius.circular(12),
    ),
  ),
  child: Stack(
    children: [
      // Full image
      Container(
        width: 100,
        height: 120,
        decoration: BoxDecoration(
          image: DecorationImage(
            image: NetworkImage("https://placehold.co/100x120"),
            fit: BoxFit.cover,
          ),
        ),
      ),
      // Gradient overlay
      Positioned(
        left: 0,
        top: 50,
        child: Container(
          width: 100,
          height: 70,
          decoration: BoxDecoration(
            gradient: LinearGradient(
              begin: Alignment(0.50, -0.00),
              end: Alignment(0.50, 1.00),
              colors: [const Color(0x00C4C4C4), const Color(0x7F1D1D1D)],
            ),
          ),
        ),
      ),
      // Text label
      Positioned(
        left: 0,
        top: 83.08,
        child: Container(
          width: 100,
          height: 36.92,
          padding: const EdgeInsets.only(left: 10, bottom: 10),
          child: Row(
            children: [
              SizedBox(
                width: 90,
                child: Text(
                  'Pedicure',
                  style: TextStyle(
                    color: Colors.white,
                    fontSize: 10,
                    fontFamily: 'Archivo',
                    fontWeight: FontWeight.w600,
                    height: 1.40,
                  ),
                ),
              ),
            ],
          ),
        ),
      ),
    ],
  ),
)
```

**Category Examples:**
1. Manicure (selected with border)
2. Pedicure
3. Makeup
4. Hair cut
5. Category or service (двухстрочный текст)

**Usage Notes:**
- Selected card имеет border 2px #4141E6 и уменьшенное изображение (92×112px) из-за padding
- Normal cards используют полное изображение 100×120px без border
- Gradient overlay начинается примерно на 42-50% высоты карточки для читаемости текста
- Text label всегда белый цвет поверх темного gradient
- Horizontal scroll с padding left 16px для первой карточки
- Spacing 10px между карточками для визуального разделения
- Small text 10px оптимален для компактных карточек
- Поддержка многострочного текста в label ("Category or\nservice")

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

<!-- COMPONENT: Flutter Avatar Groups | CATEGORY: Avatar, Social, User Interface | TAGS: avatar, group, stack, counter, social-proof, participants | RELATED: Flutter Video/Content Card, Flutter Author Info, Avatar -->
#### Flutter Avatar Groups

Группы аватаров с белой обводкой для отображения участников/подписчиков с визуальным стеком.

**Avatar with White Border:**
- **Outer Size**: 32×32px
- **Border**: 4px solid white (#FFFFFF)
- **Border Radius**: 30px (circular)
- **Inner Background**: #D9DDE2 (24×24px positioned at 4px offset)
- **Image**: 24×24px, border-radius 40px
- **Image Position**: Left 4px, Top 4px

**Counter Avatar (Overflow Indicator):**
- **Same Structure**: 32×32px outer with 4px white border
- **Content**: Text instead of image
- **Text**: "1k" (or any count format)
- **Typography**: 10px Archivo SemiBold (w600) white, line-height 1.40
- **Text Position**: Left 4px, Top 7px (slightly lower than image for centering)
- **Text Container**: 24×24px width, 18px height
- **Usage**: Показывает общее количество когда слишком много участников для отображения

**Group Layout:**
- **Spacing**: 10px between avatars
- **Direction**: Horizontal Row
- **Typical Count**: 4-5 avatars (4 images + 1 counter)
- **Alignment**: Center

**Color Specifications:**
- Border: #FFFFFF (white) - creates visual separation on any background
- Placeholder: #D9DDE2 (light gray)
- Text: #FFFFFF (white) for counter

```dart
// Avatar with white border
Container(
  width: 32,
  height: 32,
  child: Stack(
    children: [
      // White border container
      Container(
        width: 32,
        height: 32,
        decoration: ShapeDecoration(
          shape: RoundedRectangleBorder(
            side: BorderSide(width: 4, color: Colors.white),
            borderRadius: BorderRadius.circular(30),
          ),
        ),
      ),
      // Background
      Positioned(
        left: 4,
        top: 4,
        child: Container(
          width: 24,
          height: 24,
          decoration: ShapeDecoration(
            color: const Color(0xFFD9DDE2),
            shape: RoundedRectangleBorder(
              borderRadius: BorderRadius.circular(40),
            ),
          ),
        ),
      ),
      // Image
      Positioned(
        left: 4,
        top: 4,
        child: Container(
          width: 24,
          height: 24,
          decoration: ShapeDecoration(
            image: DecorationImage(
              image: NetworkImage("https://placehold.co/24x24"),
              fit: BoxFit.cover,
            ),
            shape: RoundedRectangleBorder(
              borderRadius: BorderRadius.circular(40),
            ),
          ),
        ),
      ),
    ],
  ),
)

// Counter avatar (showing "1k")
Container(
  width: 32,
  height: 32,
  child: Stack(
    children: [
      Container(
        width: 32,
        height: 32,
        decoration: ShapeDecoration(
          shape: RoundedRectangleBorder(
            side: BorderSide(width: 4, color: Colors.white),
            borderRadius: BorderRadius.circular(30),
          ),
        ),
      ),
      Positioned(
        left: 4,
        top: 4,
        child: Container(
          width: 24,
          height: 24,
          decoration: ShapeDecoration(
            color: const Color(0xFFD9DDE2),
            shape: RoundedRectangleBorder(
              borderRadius: BorderRadius.circular(40),
            ),
          ),
        ),
      ),
      Positioned(
        left: 4,
        top: 7,
        child: Container(
          width: 24,
          height: 18,
          child: Text(
            '1k',
            textAlign: TextAlign.center,
            style: TextStyle(
              color: Colors.white,
              fontSize: 10,
              fontFamily: 'Archivo',
              fontWeight: FontWeight.w600,
              height: 1.40,
            ),
          ),
        ),
      ),
    ],
  ),
)

// Full group
Row(
  spacing: 10,
  children: [
    // Avatar 1
    // Avatar 2
    // Avatar 3
    // Avatar 4
    // Counter avatar
  ],
)
```

**Usage Notes:**
- Белая обводка 4px создает визуальное разделение на любом фоне
- Counter avatar позволяет показать больше участников без перегрузки UI
- Spacing 10px обеспечивает читаемость без overlapping
- Используется для социального proof на карточках контента
- Ideal для: участники курса, подписчики, команда проекта, реакции пользователей

**Variants:**
- **4 avatars + counter**: Стандартная группа для social proof
- **Only avatars**: Без counter если количество участников небольшое
- **Different sizes**: Можно масштабировать пропорционально (сохраняя border 4px)

<!-- CROSS-REFERENCE: Used in "Flutter Video/Content Card", see also "Flutter Author Info" for single author display -->

---

<!-- COMPONENT: Flutter Author Info | CATEGORY: User Interface, Content, Author | TAGS: author, creator, user-info, avatar, credentials | RELATED: Flutter Video/Content Card, Flutter Avatar Groups -->
#### Flutter Author Info

Компонент информации об авторе/создателе контента с аватаром и описанием.

**Avatar Section:**
- **Outer Container**: 40×40px
- **Inner Avatar**: 32×32px (positioned at 4px offset)
- **Background**: #D9DDE2 (placeholder)
- **Image**: 32×32px, border-radius 40px (circle)
- **Position**: Left 4px, Top 4px

**Text Section:**
- **Layout**: Vertical Column, cross-axis start (left-aligned)
- **Spacing**: 6px between avatar and text

**Name (Primary):**
- **Text**: "Nicole Dowson"
- **Typography**: 13px Archivo SemiBold (w600) #09101D, line-height 1.40
- **Color**: #09101D (dark black)
- **Usage**: Имя автора/создателя

**Team/Role (Secondary):**
- **Text**: "Fitness App Team"
- **Typography**: 12px Archivo Regular (w400) #373940, line-height 1.40
- **Color**: #373940 (gray)
- **Usage**: Команда, роль, компания, или дополнительная информация

**Layout:**
- **Direction**: Horizontal Row with avatar + text column
- **Alignment**: Center (vertical alignment)
- **Spacing**: 6px gap between avatar and text

```dart
// Flutter Author Info Component
Row(
  spacing: 6,
  children: [
    // Avatar
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
                shape: RoundedRectangleBorder(
                  borderRadius: BorderRadius.circular(40),
                ),
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
                shape: RoundedRectangleBorder(
                  borderRadius: BorderRadius.circular(40),
                ),
              ),
            ),
          ),
        ],
      ),
    ),
    // Text info
    Column(
      crossAxisAlignment: CrossAxisAlignment.start,
      children: [
        Text(
          'Nicole Dowson',
          style: TextStyle(
            color: const Color(0xFF09101D),
            fontSize: 13,
            fontFamily: 'Archivo',
            fontWeight: FontWeight.w600,
            height: 1.40,
          ),
        ),
        Text(
          'Fitness App Team',
          style: TextStyle(
            color: const Color(0xFF373940),
            fontSize: 12,
            fontFamily: 'Archivo',
            fontWeight: FontWeight.w400,
            height: 1.40,
          ),
        ),
      ],
    ),
  ],
)
```

**Usage Notes:**
- Avatar 40×40px outer (32×32px inner) больше чем в avatar group для акцента на авторе
- Двухстрочная структура текста обеспечивает полную информацию в компактном формате
- Name в SemiBold (w600) для выделения, Team/Role в Regular (w400) для иерархии
- Spacing 6px оптимален для визуальной связи между avatar и текстом
- Используется на карточках контента для credibility и атрибуции

**Variants:**
- **With verification badge**: Можно добавить иконку верификации после имени
- **Single line**: Только имя без team/role для минимализма
- **Interactive**: Может быть кликабельным для перехода на профиль автора
- **With stats**: Можно добавить количество подписчиков или постов

**Color Specifications:**
- Primary text (Name): #09101D - dark black for prominence
- Secondary text (Team): #373940 - gray for hierarchy
- Avatar placeholder: #D9DDE2 - light gray

<!-- CROSS-REFERENCE: Used in "Flutter Video/Content Card", companion to "Flutter Avatar Groups" for social elements -->

---

<!-- COMPONENT: Flutter Calendar/Schedule | CATEGORY: Calendar, Schedule, Time Management | TAGS: calendar, schedule, timetable, appointments, time-grid, resources | RELATED: Flutter Online Status Badge, Flutter Appointment Blocks -->
### 4.5. Calendar/Schedule Components

Компоненты календаря и расписания для систем бронирования, тайм-менеджмента и планирования.

#### Flutter Time Grid with Labels

Временная сетка с метками времени и разделительными линиями для календарного view.

**Time Label:**
- **Padding**: 8px horizontal, 5px vertical
- **Border Radius**: 10px
- **Typography**: 11px Archivo Regular (w400) #09101D, line-height 1.40
- **Text**: "10:00", "11:00", "12:00" и т.д.
- **Alignment**: Center

**Divider Line:**
- **Width**: 442px (или flexible для responsive)
- **Border**: 0.5px solid #D9DDE2
- **Stroke Align**: Center
- **Position**: После time label

**Row Layout:**
- **Spacing**: 10px между label и line
- **Direction**: Horizontal
- **Row Spacing**: 15px между rows (vertical)

```dart
// Time Grid Row
Row(
  spacing: 10,
  children: [
    // Time label
    Container(
      padding: const EdgeInsets.symmetric(horizontal: 8, vertical: 5),
      decoration: ShapeDecoration(
        shape: RoundedRectangleBorder(
          borderRadius: BorderRadius.circular(10),
        ),
      ),
      child: Text(
        '10:00',
        textAlign: TextAlign.center,
        style: TextStyle(
          color: const Color(0xFF09101D),
          fontSize: 11,
          fontFamily: 'Archivo',
          fontWeight: FontWeight.w400,
          height: 1.40,
        ),
      ),
    ),
    // Divider line
    Container(
      width: 442,
      decoration: ShapeDecoration(
        shape: RoundedRectangleBorder(
          side: BorderSide(
            width: 0.50,
            strokeAlign: BorderSide.strokeAlignCenter,
            color: const Color(0xFFD9DDE2),
          ),
        ),
      ),
    ),
  ],
)
```

**Usage Notes:**
- Используется как фоновая сетка для календаря
- Time labels могут быть sticky для прокрутки
- Интервалы обычно 1 час (может быть 30 мин, 15 мин)
- Border 0.5px создает subtle разделение

---

<!-- COMPONENT: Flutter Resource Column Header | CATEGORY: Calendar, Schedule, User Interface | TAGS: calendar, staff, resource, avatar, header | RELATED: Flutter Online Status Badge, Flutter Avatar Groups -->
#### Flutter Resource/Staff Column Headers

Заголовки колонок с аватарами специалистов/ресурсов для календаря бронирования.

**Header Container:**
- **Padding**: 10px vertical
- **Spacing**: 5px internal, 10px between headers

**Avatar Variants:**

**1. Large Avatar (без статуса):**
- **Outer Size**: 56×56px
- **Inner Avatar**: 48×48px (positioned at 4px offset)
- **Background**: #D9DDE2 (placeholder)
- **Image**: 48×48px, border-radius 40px
- **Usage**: Для основного специалиста или без online status

**2. Medium Avatar (со статусом):**
- **Size**: 48×48px (full image)
- **Border Radius**: 38.40px
- **Online Status Badge**: 14×14px at bottom-left (see Flutter Online Status Badge)

**Name Label:**
- **Width**: 50px
- **Typography**: 11px Archivo SemiBold (w600) #09101D, line-height 1.40
- **Alignment**: Center
- **Text**: "Molly", "Jimmy", "Daniel"

**Header Spacing:**
- **Avatar to Name**: 5px
- **Between Headers**: 10px (in horizontal layout)

```dart
// Resource Column Header - Large Avatar
Column(
  spacing: 5,
  children: [
    // Avatar
    Container(
      width: 56,
      height: 56,
      child: Stack(
        children: [
          Positioned(
            left: 4,
            top: 4,
            child: Container(
              width: 48,
              height: 48,
              decoration: ShapeDecoration(
                color: const Color(0xFFD9DDE2),
                shape: RoundedRectangleBorder(
                  borderRadius: BorderRadius.circular(40),
                ),
              ),
            ),
          ),
          Positioned(
            left: 4,
            top: 4,
            child: Container(
              width: 48,
              height: 48,
              decoration: ShapeDecoration(
                image: DecorationImage(
                  image: NetworkImage("https://placehold.co/48x48"),
                  fit: BoxFit.cover,
                ),
                shape: RoundedRectangleBorder(
                  borderRadius: BorderRadius.circular(40),
                ),
              ),
            ),
          ),
        ],
      ),
    ),
    // Name
    SizedBox(
      width: 50,
      child: Text(
        'Molly',
        textAlign: TextAlign.center,
        style: TextStyle(
          color: const Color(0xFF09101D),
          fontSize: 11,
          fontFamily: 'Archivo',
          fontWeight: FontWeight.w600,
          height: 1.40,
        ),
      ),
    ),
  ],
)

// Resource Column Header - With Online Status
Column(
  spacing: 5,
  children: [
    // Avatar with status badge
    Container(
      width: 48,
      height: 48,
      child: Stack(
        children: [
          Container(
            width: 48,
            height: 48,
            decoration: ShapeDecoration(
              image: DecorationImage(
                image: NetworkImage("https://placehold.co/48x48"),
                fit: BoxFit.cover,
              ),
              shape: RoundedRectangleBorder(
                borderRadius: BorderRadius.circular(38.40),
              ),
            ),
          ),
          // Online status badge
          Positioned(
            left: 0,
            top: 34,
            child: Container(
              width: 14,
              height: 14,
              decoration: ShapeDecoration(
                color: const Color(0xFF11BB8D),
                shape: RoundedRectangleBorder(
                  side: BorderSide(width: 3, color: Colors.white),
                  borderRadius: BorderRadius.circular(19.20),
                ),
              ),
            ),
          ),
        ],
      ),
    ),
    // Name
    SizedBox(
      width: 50,
      child: Text(
        'Jimmy',
        textAlign: TextAlign.center,
        style: TextStyle(
          color: const Color(0xFF09101D),
          fontSize: 11,
          fontFamily: 'Archivo',
          fontWeight: FontWeight.w600,
          height: 1.40,
        ),
      ),
    ),
  ],
)
```

**Usage Notes:**
- Large avatar (56px) для акцента на главном специалисте
- Medium avatar (48px) со статусом для показа availability
- Name label ограничен 50px width для компактности
- Online status badge позиционируется bottom-left для видимости

---

<!-- COMPONENT: Flutter Online Status Badge | CATEGORY: Status, Indicator, User Interface | TAGS: online, status, availability, badge, indicator | RELATED: Flutter Resource Column Header, Avatar -->
#### Flutter Online Status Badge

Индикатор онлайн статуса для аватаров в календаре и профилях.

**Badge Specifications:**
- **Size**: 14×14px
- **Background**: #11BB8D (success green) - online status
- **Border**: 3px solid white (#FFFFFF)
- **Border Radius**: 19.20px (full circle)
- **Position**: Bottom-left corner of avatar (left 0, top 34 for 48px avatar)

**Positioning:**
- **For 48×48px avatar**: left 0, top 34
- **For other sizes**: Adjust top = avatar_height - badge_height - border

```dart
// Online Status Badge
Container(
  width: 14,
  height: 14,
  decoration: ShapeDecoration(
    color: const Color(0xFF11BB8D),
    shape: RoundedRectangleBorder(
      side: BorderSide(width: 3, color: Colors.white),
      borderRadius: BorderRadius.circular(19.20),
    ),
  ),
)

// Positioned on avatar
Stack(
  children: [
    // Avatar 48×48px
    Container(width: 48, height: 48, ...),
    // Status badge
    Positioned(
      left: 0,
      top: 34,
      child: /* Online Status Badge */,
    ),
  ],
)
```

**Color Variants:**
- **Online**: #11BB8D (green) - currently used
- **Busy/In Meeting**: #E24949 (red) - can be used
- **Away**: #FFC043 (yellow) - can be used
- **Offline**: #D9DDE2 (gray) - can be used

**Usage Notes:**
- Border 3px white создает visual separation от avatar
- Позиция bottom-left стандартная для status indicators
- Размер 14px оптимален для visibility без overlapping
- Можно использовать разные цвета для разных статусов

---

<!-- COMPONENT: Flutter Appointment Block | CATEGORY: Calendar, Schedule, Events | TAGS: appointment, event, booking, calendar-block, time-slot | RELATED: Flutter Calendar/Schedule, Flutter Available Slot -->
#### Flutter Appointment Blocks

Блоки событий/встреч для календарного расписания с поддержкой multi-slot appointments.

**Block Specifications:**
- **Size**: 130px width × 40px height (per time slot)
- **Padding**: Top 4px, Left 2px, Right 5px, Bottom 6px (for blocks with content)
- **Spacing**: 5px internal between avatar and text

**Single Slot Appointment:**
- **Border Radius**: 15px (all corners)
- **Content**: Avatar + Time + Name

**Multi-Slot Appointment (spanning multiple hours):**
- **Top Block**: topLeft and topRight radius 15px, bottom squared
- **Middle Blocks**: No border radius (squared all sides)
- **Bottom Block**: bottomLeft and bottomRight radius 15px, top squared

**Color Palette:**
- **#5E38BA**: Темно-фиолетовый (purple) - premium appointments
- **#7CC5D6**: Светло-голубой (cyan) - standard appointments
- **#F7B68A**: Персиковый (peach) - wellness appointments
- **#4141E6**: Синий (blue) - regular appointments
- **#E24949**: Красный (red) - urgent/priority appointments

**Content Layout:**
- **Avatar**: 32×32px outer, 24×24px image at 4px offset
- **Time**: 11px Archivo Regular (w400) white
- **Client/Name**: 10px Archivo SemiBold (w600) white
- **Spacing**: 5px between avatar and text column

```dart
// Single Slot Appointment (1 hour)
Container(
  width: 130,
  height: 40,
  padding: const EdgeInsets.only(top: 4, left: 2, right: 5, bottom: 6),
  decoration: ShapeDecoration(
    color: const Color(0xFF5E38BA), // Purple
    shape: RoundedRectangleBorder(
      borderRadius: BorderRadius.circular(15),
    ),
  ),
  child: Row(
    spacing: 5,
    children: [
      // Avatar
      Container(
        width: 32,
        height: 32,
        child: Stack(
          children: [
            Positioned(
              left: 4,
              top: 4,
              child: Container(
                width: 24,
                height: 24,
                decoration: ShapeDecoration(
                  image: DecorationImage(
                    image: NetworkImage("https://placehold.co/24x24"),
                    fit: BoxFit.cover,
                  ),
                  shape: RoundedRectangleBorder(
                    borderRadius: BorderRadius.circular(40),
                  ),
                ),
              ),
            ),
          ],
        ),
      ),
      // Text info
      Column(
        crossAxisAlignment: CrossAxisAlignment.start,
        children: [
          Text(
            '10:00 - 11:00',
            style: TextStyle(
              color: Colors.white,
              fontSize: 11,
              fontFamily: 'Archivo',
              fontWeight: FontWeight.w400,
              height: 1.40,
            ),
          ),
          Text(
            'Helena',
            style: TextStyle(
              color: Colors.white,
              fontSize: 10,
              fontFamily: 'Archivo',
              fontWeight: FontWeight.w600,
              height: 1.40,
            ),
          ),
        ],
      ),
    ],
  ),
)

// Multi-Slot Appointment - Top Block
Container(
  width: 130,
  height: 40,
  padding: const EdgeInsets.only(top: 4, left: 2, right: 5, bottom: 6),
  decoration: ShapeDecoration(
    color: const Color(0xFF4141E6), // Blue
    shape: RoundedRectangleBorder(
      borderRadius: BorderRadius.only(
        topLeft: Radius.circular(15),
        topRight: Radius.circular(15),
      ),
    ),
  ),
  child: /* Same content */,
)

// Multi-Slot Appointment - Middle Block
Container(
  width: 130,
  height: 40,
  padding: const EdgeInsets.symmetric(horizontal: 5, vertical: 6),
  decoration: BoxDecoration(color: const Color(0xFF4141E6)), // No border radius
)

// Multi-Slot Appointment - Bottom Block
Container(
  width: 130,
  height: 40,
  padding: const EdgeInsets.symmetric(horizontal: 5, vertical: 6),
  decoration: ShapeDecoration(
    color: const Color(0xFF4141E6),
    shape: RoundedRectangleBorder(
      borderRadius: BorderRadius.only(
        bottomLeft: Radius.circular(15),
        bottomRight: Radius.circular(15),
      ),
    ),
  ),
)
```

**Usage Notes:**
- Single slot appointments (1 hour): full 15px border radius
- Multi-slot appointments: top block с top radius, middle без radius, bottom с bottom radius
- Цвета используются для категоризации: premium, standard, wellness, regular, urgent
- Avatar 24×24px достаточно для identification в компактном view
- White text обеспечивает contrast на всех background colors
- Padding варьируется: blocks с content имеют asymmetric padding, middle blocks symmetric

**Color Usage Guidelines:**
- **Purple (#5E38BA)**: VIP clients, premium services
- **Cyan (#7CC5D6)**: Standard appointments, consultations
- **Peach (#F7B68A)**: Wellness, spa, relaxation services
- **Blue (#4141E6)**: Regular appointments, meetings
- **Red (#E24949)**: Urgent, priority, critical appointments

---

<!-- COMPONENT: Flutter Available Time Slot | CATEGORY: Calendar, Schedule, Availability | TAGS: available, free-slot, booking, calendar, add-appointment | RELATED: Flutter Appointment Block, Calendar/Schedule -->
#### Flutter Available Time Slot

Индикатор доступного времени для бронирования в календаре.

**Slot Specifications:**
- **Size**: 130px width × 40px height
- **Padding**: Top 6px, Left 10px, Right 5px, Bottom 6px
- **Background**: #F4F6F9 (light gray)
- **Border Radius**: 15px
- **Icon**: 24×24px (plus icon or add indicator)

```dart
// Available Time Slot
Container(
  width: 130,
  height: 40,
  padding: const EdgeInsets.only(top: 6, left: 10, right: 5, bottom: 6),
  decoration: ShapeDecoration(
    color: const Color(0xFFF4F6F9),
    shape: RoundedRectangleBorder(
      borderRadius: BorderRadius.circular(15),
    ),
  ),
  child: Row(
    mainAxisAlignment: MainAxisAlignment.center,
    crossAxisAlignment: CrossAxisAlignment.center,
    spacing: 5,
    children: [
      Container(
        width: 24,
        height: 24,
        // Plus icon placeholder
      ),
    ],
  ),
)
```

**Interaction States:**
- **Default**: #F4F6F9 background с plus icon
- **Hover**: Можно добавить slightly darker background
- **Active/Clicked**: Открывает форму добавления appointment

**Usage Notes:**
- Light gray background (#F4F6F9) контрастирует с colored appointments
- Plus icon 24×24px центрирован в slot
- Clicking opens appointment creation dialog
- Можно показывать только на hover для cleaner view
- Border radius 15px соответствует appointment blocks

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

#### Flutter Avatar Variants

Avatar компоненты из Flutter кода с двухслойной структурой (outer container + inner image).

**Flutter Avatar Small (40×40):**
- **Outer Container**: 40px × 40px
- **Inner Image**: 32px × 32px
  - Position: Left 4px, Top 4px
- **Border Radius**: 10px (rounded square) или 40px (circle)
- **Placeholder Background**: #D9DDE2
- **Image Fit**: BoxFit.cover
- **Usage**: Карточки рецептов, компактные списки

**Flutter Avatar Medium (48×48):**
- **Outer Container**: 48px × 48px
- **Inner Image**: 40px × 40px
  - Position: Left 4px, Top 4px
- **Border Radius**: 40px (circle)
- **Placeholder Background**: #D9DDE2
- **Image Fit**: BoxFit.cover
- **Usage**: Списки криптовалют, активов, стандартные list items

**Flutter Avatar Large (56×56):**
- **Outer Container**: 56px × 56px
- **Inner Image**: 48px × 48px
  - Position: Left 4px, Top 4px
- **Border Radius**: 40px (circle)
- **Placeholder Background**: #D9DDE2
- **Image Fit**: BoxFit.cover
- **Usage**: Follow lists, социальные списки с действиями

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

#### List Item (Flutter Mobile)

Полноценные элементы списка из Flutter кода с integrated form controls.

**Container:**
- **Width**: 375px (full mobile width)
- **Background**: White (#FFFFFF)
- **Padding**: Horizontal 16px
- **Spacing**: 10px between items

**Layout Structure:**
- **Control Area** (left):
  - Padding Right: 16px (для toggle)
  - Padding Right: 10px (для radio/checkbox)
  - Vertical: full height

- **Content Area** (right):
  - Padding: Vertical 10px
  - Expanded: true (fills remaining space)

**Text Content:**
- **Title**:
  - Font: Archivo SemiBold
  - Size: 14px
  - Color: #09101D
  - Line Height: 1.40
  - Width: 276px (для toggle items), 309px (для radio/checkbox items)

- **Subtitle**:
  - Font: Archivo Regular
  - Size: 13px
  - Color: #414249
  - Line Height: 1.40
  - States: "Active", "Default", "Selected", "Disabled"
  - Spacing: 16px horizontal from title

**Divider:**
- **Width**: Full width
- **Height**: 1px
- **Color**: #EAEEF2
- **Padding**:
  - Top: 5px
  - Left: 64px (для toggle), 36px (для radio/checkbox)
  - Bottom: 5px
  - Right: 16px (для radio/checkbox)

**Integrated Controls:**
1. **Toggle Switch List Item**:
   - Control: 51px × 31px toggle
   - Control Padding Right: 16px
   - Title width: 276px
   - Active color: #11BB8D

2. **Radio Button List Item**:
   - Control: 24px × 24px radio
   - Control Padding Right: 10px
   - Title width: 309px
   - Divider left offset: 36px

3. **Checkbox List Item**:
   - Control: 24px × 24px checkbox
   - Control Padding Right: 10px
   - Title width: 309px
   - Divider left offset: 36px

```dart
// List Item with Toggle (Active State)
Container(
  width: 375,
  child: Column(
    children: [
      Container(
        padding: const EdgeInsets.symmetric(horizontal: 16),
        decoration: BoxDecoration(color: Colors.white),
        child: Column(
          children: [
            Row(
              children: [
                Container(
                  padding: const EdgeInsets.only(right: 16),
                  child: Container(
                    width: 51,
                    decoration: ShapeDecoration(
                      color: const Color(0xFF11BB8D),
                      shape: RoundedRectangleBorder(
                        borderRadius: BorderRadius.circular(40),
                      ),
                    ),
                    child: Row(
                      mainAxisAlignment: MainAxisAlignment.end,
                      children: [
                        Container(
                          width: 31,
                          height: 31,
                          decoration: ShapeDecoration(
                            color: Colors.white,
                            shape: RoundedRectangleBorder(
                              side: BorderSide(width: 2, color: const Color(0xFF11BB8D)),
                              borderRadius: BorderRadius.circular(40),
                            ),
                          ),
                        ),
                      ],
                    ),
                  ),
                ),
                Expanded(
                  child: Container(
                    padding: const EdgeInsets.symmetric(vertical: 10),
                    child: Column(
                      crossAxisAlignment: CrossAxisAlignment.start,
                      children: [
                        SizedBox(
                          width: 276,
                          child: Text(
                            'Toggle',
                            style: TextStyle(
                              color: const Color(0xFF09101D),
                              fontSize: 14,
                              fontFamily: 'Archivo',
                              fontWeight: FontWeight.w600,
                              height: 1.40,
                            ),
                          ),
                        ),
                        SizedBox(
                          width: 276,
                          child: Text(
                            'Active',
                            style: TextStyle(
                              color: const Color(0xFF414249),
                              fontSize: 13,
                              fontFamily: 'Archivo',
                              fontWeight: FontWeight.w400,
                              height: 1.40,
                            ),
                          ),
                        ),
                      ],
                    ),
                  ),
                ),
              ],
            ),
            Container(
              padding: const EdgeInsets.only(top: 5, left: 64, bottom: 5),
              child: Container(
                width: double.infinity,
                height: 1,
                decoration: BoxDecoration(color: const Color(0xFFEAEEF2)),
              ),
            ),
          ],
        ),
      ),
    ],
  ),
)
```

**Usage:** Списки с настройками, переключателями, выбором опций в мобильном приложении.

---

#### Advanced List Item Variants

Расширенные варианты list items из Flutter кода для различных сценариев использования.

##### 1. Range Slider List Item

List item с двойным ползунком для выбора диапазона значений.

**Container:**
- **Width**: 375px
- **Padding**: Horizontal 16px, Vertical 20px
- **Background**: White (#FFFFFF)

**Header:**
- **Title**: "Title", 16px, Archivo Bold (w700), color #09101D
- **Value Display**: "\$0 - \$98", 16px, Archivo SemiBold (w600), color #09101D
- **Subtitle**: "Subtitle", 14px, Archivo Regular (w400), color #414249
- **Spacing**: 8px between title and value, 24px sections

**Slider:**
- **Track Height**: 4px
- **Track Color**: #F4F6F9 (inactive)
- **Active Track Color**: #4141E6
- **Track Border Radius**: 40px
- **Thumb Size**: 20px × 20px
- **Thumb Color**: #4141E6
- **Thumb Border**: 4px solid rgba(11, 36, 251, 0.25) - #0B24FB with 25% opacity
- **Thumb Border Radius**: 40px
- **Position**: Top 64.01px from container

**Value Tooltip:**
- **Padding**: Horizontal 16px, Vertical 12px
- **Background**: #09101D (dark)
- **Border Radius**: 5px
- **Text**: White, 13px, Archivo Bold (w700)
- **Line Height**: 1.40
- **Examples**: "1\$", "50\$"

**Usage:** Фильтры по цене, настройки диапазонов значений.

---

##### 2. Section Header List Item

Простой заголовок секции с разделителем.

**Container:**
- **Width**: 375px (327px content)
- **Padding**: Horizontal 16px, Vertical 20px
- **Spacing**: 10px between content and divider, 5px around content

**Content:**
- **Title**: 16px, Archivo Bold (w700), color #09101D
- **Subtitle**: 14px, Archivo Regular (w400), color #414249, width 327px
- **Spacing**: 5px between title and subtitle

**Divider:**
- **Height**: 1px
- **Color**: #EAEEF2
- **Vertical Padding**: 5px

**Usage:** Разделители секций в длинных списках.

---

##### 3. User Follow List Item

List item с аватаром пользователя и кнопкой действия.

**Container:**
- **Width**: 375px
- **Padding**: Horizontal 16px, Vertical 10px
- **Spacing**: 10px between avatar and content

**Avatar:**
- **Outer**: 56px × 56px
- **Inner**: 48px × 48px (left 4px, top 4px)
- **Border Radius**: 40px (circle)
- **Background**: #D9DDE2

**Text Content:**
- **Name (Bold Part)**: "Name Surname", 14px, Archivo SemiBold (w600), color #09101D
- **Action Text (Regular)**: "started following you", 14px, Rubik Regular (w400), color #09101D
- **Combined Width**: 195px
- **Label**: "label", 12px, Archivo Regular (w400), color #747B84

**Follow Button:**
- **Height**: 36px
- **Padding**: Horizontal 16px, Vertical 10px
- **Background**: #4141E6
- **Border Radius**: 15px
- **Text**: "Follow", White, 13px, Archivo SemiBold (w600)

**Divider:**
- **Height**: 1px
- **Color**: #EAEEF2
- **Vertical Padding**: 5px

```dart
Container(
  height: 36,
  padding: const EdgeInsets.symmetric(horizontal: 16, vertical: 10),
  decoration: ShapeDecoration(
    color: const Color(0xFF4141E6),
    shape: RoundedRectangleBorder(
      borderRadius: BorderRadius.circular(15),
    ),
  ),
  child: Text(
    'Follow',
    style: TextStyle(
      color: Colors.white,
      fontSize: 13,
      fontFamily: 'Archivo',
      fontWeight: FontWeight.w600,
      height: 1.40,
    ),
  ),
)
```

**Usage:** Социальные списки, уведомления о подписчиках.

---

##### 4. Crypto/Asset List Item

List item для отображения криптовалют и активов с графиком.

**Container:**
- **Width**: 375px
- **Padding**: Horizontal 16px, Vertical 10px
- **Height**: 50px

**Avatar:**
- **Outer**: 48px × 48px
- **Inner**: 40px × 40px (left 4px, top 4px)
- **Border Radius**: 40px (circle)

**Left Section:**
- **Title**: "Bitcoin", 13px, Archivo Bold (w700), color #09101D
- **Badge Container**: Padding 5px horizontal, 2px vertical, background #EAEEF2, border-radius 4px
  - **Badge Text**: "1", 10px, Archivo SemiBold (w600), color #09101D
- **Ticker**: "BTC", 11px, Archivo SemiBold (w600), color #747B84
- **Percentage**: "3,24 %", 11px, Archivo SemiBold (w600), color #E24949 (negative)
- **Spacing**: 5px between badge and ticker, 10px between ticker group

**Chart Area:**
- **Width**: 60px
- **Height**: 40px
- **Position**: Between left and right sections

**Right Section:**
- **Price**: "54 256.73 ", 13px, Archivo Bold (w700), color #09101D, right aligned
- **Market Cap**: "MCAP 1.9 T", 11px, Archivo Regular (w400), color #303239, right aligned
- **Spacing**: 5px between price and market cap

**Spacing**: 20px between sections

**Usage:** Списки криптовалют, акций, торговых активов.

---

##### 5. Simple Asset List Item

Упрощенная версия для отображения активов с процентным изменением.

**Container:**
- **Width**: 375px
- **Padding**: Horizontal 16px, Vertical 10px
- **Height**: 50px

**Avatar:**
- **Outer**: 48px × 48px
- **Inner**: 40px × 40px

**Content:**
- **Title**: "Bitcoin", 13px, Archivo Regular (w400), color #09101D
- **Label**: "Label", 11px, Archivo Regular (w400), color #D9DDE2
- **Spacing**: 5px vertical between title and label

**Right Section:**
- **Percentage**: "-1.13 %", 13px, Archivo Bold (w700), color #E24949, right aligned

**Spacing**: 20px between avatar and content

**Usage:** Компактные списки активов, портфолио.

---

##### 6. Expandable/Accordion List Item

Раскрывающийся list item с иконкой действия.

**Container:**
- **Width**: 375px
- **Padding**: Horizontal 16px, Vertical 20px
- **Height**: 41px (collapsed)
- **Spacing**: 20px between content sections

**Content:**
- **Subtitle**: "Subtitle", 14px, Archivo Regular (w400), color #414249
- **Title**: "What exactly navigation is and how it works", 14px, Archivo SemiBold (w600), color #09101D, width 235px
- **Spacing**: 20px between subtitle and title

**Icon Button:**
- **Container**: 40px width
- **Icon**: 24px × 24px
- **Padding**: 2px
- **Border Radius**: 12px

**Divider:**
- **Height**: 1px
- **Color**: #EAEEF2
- **Vertical Padding**: 5px

**Usage:** FAQ секции, раскрывающиеся списки, аккордеоны.

---

##### 7. File/Document List Item

List item для файлов и материалов с метаданными.

**Container:**
- **Width**: 375px
- **Padding**: Horizontal 16px, Vertical 20px

**Icon Container:**
- **Size**: 64px × 64px
- **Background**: #F8F8FA
- **Border Radius**: 16px
- **Icon**: 28px × 24px with 4px horizontal padding

**Content:**
- **Title**: "Materials", 16px, Archivo SemiBold (w600), color #09101D
- **Author**: "Allysa Goodman", 12px, Archivo SemiBold (w600), color #303239, line-height 1.67
- **Separator**: "•", 12px, Archivo SemiBold (w600), color #414249
- **Date**: "8 March 2021", 12px, Archivo SemiBold (w600), color #303239
- **Spacing**: 2px between title and metadata, 4px between metadata items

**Action Button:**
- **Icon**: 24px × 24px
- **Padding**: Horizontal 8px, Vertical 9px

**Spacing**: 10px between icon and content

**Usage:** Списки файлов, документов, материалов курсов.

---

##### 8. Photo Grid List Item

List item с сеткой фотографий.

**Container:**
- **Width**: 375px
- **Padding**: Horizontal 16px, Vertical 20px

**Grid:**
- **Layout**: 3 columns × 2 rows
- **Photo Size**: 100px × 100px each
- **Border Radius**: 16px
- **Spacing**: 10px between photos (horizontal and vertical)
- **Total Grid**: 6 positions

**Photo:**
- **Image Fit**: BoxFit.cover
- **Border Radius**: 16px

**Last Item (Add More):**
- **Size**: 100px × 100px
- **Background**: #F8F8FA
- **Border Radius**: 16px
- **Plus Icon**: 24px × 24px centered
- **Icon Container**: 37.50px × 37.50px

**Usage:** Галереи фотографий, альбомы, портфолио.

---

##### 9. Grid Icon List Item

List item с мини-сеткой иконок.

**Container:**
- **Width**: 343px (375px - 32px padding)
- **Padding**: Horizontal 16px, Vertical 10px
- **Spacing**: 20px vertical

**Icon Grid:**
- **Layout**: 2 × 2 grid
- **Icon Size**: 25px × 25px each
- **Background**: #F8F8FA
- **Border Radius**: 5px
- **Spacing**: 5px between icons (horizontal and vertical)

**Content:**
- **Title**: "Title", 16px, Archivo Bold (w700), color #09101D, width 122px
- **Label**: "Label", 14px, Archivo Regular (w400), color #D9DDE2, right aligned
- **Icon Button**: 24px
- **Subtitle**: "Subtitle", 14px, Archivo Regular (w400), color #414249, width 278px
- **Spacing**: 5px between title/label and subtitle

**Divider:**
- **Height**: 1px
- **Color**: #EAEEF2
- **Vertical Padding**: 5px

**Usage:** Списки с категориями, теги, группировки.

---

##### 10. Icon List Item

Компактный list item с одной иконкой слева.

**Container:**
- **Width**: 375px (expanded)
- **Padding**: Horizontal 16px, Vertical 10px

**Icon Container:**
- **Size**: 40px × 40px
- **Background**: #F4F6F9
- **Border Radius**: 15px
- **Icon**: 20px × 20px (positioned at 9.75px, 9.85px)

**Content:**
- **Title**: "Title", 16px, Archivo Bold (w700), color #09101D, width 129.50px
- **Label**: "Label", 14px, Archivo Regular (w400), color #D9DDE2, right aligned
- **More Icon**: 24px
- **Spacing**: 5px between elements

**Usage:** Настройки, меню, навигация.

---

##### 11. Product/Album List Item

List item с крупным изображением продукта или альбома.

**Container:**
- **Width**: 343px (375px - 32px padding)
- **Padding**: Horizontal 16px, Vertical 10px
- **Spacing**: 20px vertical

**Image Container:**
- **Size**: 90px × 90px
- **Background**: #B7D5D5 (или другой декоративный цвет)
- **Border Radius**: 10px
- **Padding**: 10px
- **Inner Image**: 60px × 60px, border-radius 10px, fit: cover

**Content:**
- **Subtitle**: "Subtitle", 14px, Archivo Regular (w400), color #414249, width 243px
- **Title**: "Title", 16px, Archivo Bold (w700), color #09101D, width 243px
- **Label**: "Label", 14px, Archivo Regular (w400), color #D9DDE2, right aligned, width 75.50px
- **Spacing**: 5px between elements

**Action Buttons:**
- **Size**: 24px × 24px each
- **Count**: 2 buttons
- **Padding**: 2px
- **Border Radius**: 100px (circle)
- **Spacing**: 10px between label and buttons

**Divider:**
- **Height**: 1px
- **Color**: #EAEEF2
- **Vertical Padding**: 5px

**Usage:** Списки альбомов, продуктов, медиа контента.

---

##### 12. Filter/Sort Header

Header с кнопками фильтра и сортировки.

**Container:**
- **Width**: 375px
- **Padding**: Horizontal 16px, Vertical 10px

**Left Section (Filter):**
- **Icon**: 24px, padding 2px, border-radius 12px
- **Text**: "Filter", 14px, Archivo SemiBold (w600), color #09101D, width 143.50px
- **Spacing**: 10px between icon and text

**Right Section (Sort):**
- **Text**: "Sort", 14px, Archivo SemiBold (w600), color #09101D, right aligned
- **Icon**: 24px, padding 2px, border-radius 12px
- **Spacing**: 10px between text and icon

**Divider:**
- **Height**: 1px
- **Color**: #EAEEF2
- **Vertical Padding**: 5px

**Usage:** Headers для списков с фильтрацией и сортировкой.

---

##### 13. Avatar with Details List Item

Стандартный list item с аватаром и подробностями.

**Container:**
- **Width**: 375px
- **Padding**: Horizontal 16px, Vertical 10px

**Avatar:**
- **Outer**: 48px × 48px
- **Inner**: 40px × 40px (left 4px, top 4px)
- **Border Radius**: 40px (circle)

**Content:**
- **Title**: "Title", 16px, Archivo Bold (w700), color #09101D
- **Subtitle**: "Subtitle", 14px, Archivo Regular (w400), color #414249

**More Icon:**
- **Size**: 24px × 24px
- **Spacing**: 16px from avatar

**Divider:**
- **Height**: 1px
- **Color**: #F4F6F9 (lighter variant!)
- **Vertical Padding**: none (direct border)

**Usage:** Контакты, пользователи, профили.

---

##### 14. Checkbox Agreement List Item

List item с чекбоксом и текстом соглашения.

**Container:**
- **Width**: 375px (full)
- **Padding**: Horizontal 16px, Vertical 10px

**Checkbox:**
- **Size**: 24px × 24px
- **Border**: 2px solid #EAEEF2
- **Border Radius**: 2px
- **Stroke Align**: Center
- **Position**: Left

**Text:**
- **Content**: "By registering, you agree our Terms of Use"
- **Regular Text**: 13px, Archivo Regular (w400), color #23262B
- **Link Text**: "Terms of Use", 13px, Archivo Regular (w400), color #4141E6
- **Spacing**: 5px between checkbox and text

**Usage:** Формы регистрации, соглашения, подтверждения.

---

##### 15. Language Selector List Item

List item для выбора языка с флагом.

**Container:**
- **Width**: 375px
- **Padding**: Horizontal 16px, Vertical 20px

**Flag Icon:**
- **Size**: 40px × 30px
- **Border Radius**: 5px
- **Clip**: antiAlias
- **Example Color**: #46467F (for flag elements)

**Language Text:**
- **Text**: "English", 15px, Archivo SemiBold (w600), color #09101D
- **Spacing**: 10px from flag

**Checkbox (Right):**
- **Size**: 24px × 24px
- **Border**: 2px solid #EAEEF2
- **Border Radius**: 2px
- **Stroke Align**: Center
- **Position**: Right aligned

**Spacing**: 10px between elements

**Usage:** Настройки языка, выбор локали.

---

### 12. Chat / Messaging (Flutter)

Компоненты для чата и мессенджера из Flutter кода.

#### Chat Message Bubbles

**Incoming Message (Left)**
- **Width**: 248px
- **Padding**: 10px
- **Border Radius**: 15px
- **Background**: #F4F6F9 (светло-серый)
- **Text**:
  - Font: Archivo Regular
  - Size: 16px
  - Color: #09101D
  - Line Height: 1.40
- **Layout**:
  - Avatar (left): 32×32px outer, 24×24px inner
  - Spacing: 5px between avatar and bubble
  - Alignment: Start (left)

**Outgoing Message (Right)**
- **Width**: 260px
- **Padding**: Horizontal 16px, Vertical 10px
- **Border Radius**: 15px
- **Background**: #414249 (темно-серый)
- **Text**:
  - Font: Archivo Regular
  - Size: 16px
  - Color: White (#FFFFFF)
  - Line Height: 1.40
- **Layout**:
  - Avatar (right): 32×32px outer, 24×24px inner
  - Spacing: 5px between avatar and bubble
  - Alignment: End (right)

**Metadata Footer:**
- **Time Stamps**:
  - Font: Archivo Regular
  - Size: 11px
  - Color: #747B84 (incoming), White (outgoing)
  - Line Height: 1.40
  - Text Align: Right
  - Spacing: 3px before icon (if present)
- **Layout**: Two time stamps with 5px spacing, aligned start/end

```dart
// Incoming Message
Container(
  width: 248,
  padding: const EdgeInsets.all(10),
  decoration: ShapeDecoration(
    color: const Color(0xFFF4F6F9),
    shape: RoundedRectangleBorder(borderRadius: BorderRadius.circular(15)),
  ),
  child: Column(
    crossAxisAlignment: CrossAxisAlignment.start,
    spacing: 5,
    children: [
      Text(
        'Hi I want to book some desk, is it\npossible?',
        style: TextStyle(
          color: const Color(0xFF09101D),
          fontSize: 16,
          fontFamily: 'Archivo',
          fontWeight: FontWeight.w400,
          height: 1.40,
        ),
      ),
      Row(
        children: [
          Text(
            '3:00PM ',
            style: TextStyle(
              color: const Color(0xFF747B84),
              fontSize: 11,
              fontFamily: 'Archivo',
              fontWeight: FontWeight.w400,
              height: 1.40,
            ),
          ),
        ],
      ),
    ],
  ),
)

// Outgoing Message
Container(
  width: 260,
  padding: const EdgeInsets.symmetric(horizontal: 16, vertical: 10),
  decoration: ShapeDecoration(
    color: const Color(0xFF414249),
    shape: RoundedRectangleBorder(borderRadius: BorderRadius.circular(15)),
  ),
  child: Column(
    crossAxisAlignment: CrossAxisAlignment.end,
    spacing: 5,
    children: [
      Text(
        'Yes of cource, we have a huge amount of desks and offices',
        style: TextStyle(
          color: Colors.white,
          fontSize: 16,
          fontFamily: 'Archivo',
          fontWeight: FontWeight.w400,
          height: 1.40,
        ),
      ),
      Row(
        children: [
          Text(
            '3:00PM ',
            style: TextStyle(
              color: Colors.white,
              fontSize: 11,
              fontFamily: 'Archivo',
              fontWeight: FontWeight.w400,
              height: 1.40,
            ),
          ),
        ],
      ),
    ],
  ),
)
```

#### Chat Avatar (Small)

Маленький вариант аватара для чата.

- **Outer Container**: 32px × 32px
- **Inner Image**: 24px × 24px
  - Position: Left 4px, Top 4px
- **Border Radius**: 40px (circle)
- **Placeholder Background**: #D9DDE2
- **Image Fit**: BoxFit.cover
- **Spacing**: 5px from message bubble

```dart
Container(
  width: 32,
  height: 32,
  child: Stack(
    children: [
      Positioned(
        left: 4,
        top: 4,
        child: Container(
          width: 24,
          height: 24,
          decoration: ShapeDecoration(
            color: const Color(0xFFD9DDE2),
            shape: RoundedRectangleBorder(borderRadius: BorderRadius.circular(40)),
          ),
        ),
      ),
      Positioned(
        left: 4,
        top: 4,
        child: Container(
          width: 24,
          height: 24,
          decoration: ShapeDecoration(
            image: DecorationImage(
              image: NetworkImage("https://placehold.co/24x24"),
              fit: BoxFit.cover,
            ),
            shape: RoundedRectangleBorder(borderRadius: BorderRadius.circular(40)),
          ),
        ),
      ),
    ],
  ),
)
```

#### Date Dividers / Separators

Разделители дат и новых сообщений для чата.

**Specs:**
- **Container Width**: 375px (full width)
- **Padding**: Vertical 5px
- **Badge Padding**: Horizontal 10px, Vertical 2px
- **Border Radius**: 10px
- **Text**:
  - Font: Archivo SemiBold
  - Size: 10px
  - Color: #09101D
  - Line Height: 1.40
  - Text Align: Center

**Варианты:**

1. **"Yesterday"**
   - Background: rgba(255, 192, 67, 0.10) - желтый с 10% opacity

2. **"Mon 30"**
   - Background: rgba(5, 148, 79, 0.10) - темно-зеленый с 10% opacity

3. **"June, 2021"**
   - Background: rgba(11, 36, 251, 0.10) - синий с 10% opacity

4. **"2021"**
   - Background: rgba(255, 105, 55, 0.10) - оранжевый с 10% opacity

5. **"NEW MESSAGES"**
   - No background
   - Text Color: #FF6937 (orange)
   - Text: uppercase

```dart
// Date Divider
Container(
  width: 375,
  padding: const EdgeInsets.symmetric(vertical: 5),
  child: Row(
    mainAxisAlignment: MainAxisAlignment.center,
    children: [
      Container(
        padding: const EdgeInsets.symmetric(horizontal: 10, vertical: 2),
        decoration: ShapeDecoration(
          color: const Color(0x19FFC043), // Yellow with 10% opacity
          shape: RoundedRectangleBorder(borderRadius: BorderRadius.circular(10)),
        ),
        child: Text(
          'Yesterday',
          style: TextStyle(
            color: const Color(0xFF09101D),
            fontSize: 10,
            fontFamily: 'Archivo',
            fontWeight: FontWeight.w600,
            height: 1.40,
          ),
        ),
      ),
    ],
  ),
)

// "NEW MESSAGES" Text
Container(
  width: 375,
  padding: const EdgeInsets.symmetric(vertical: 5),
  child: Text(
    'NEW MESSAGES',
    textAlign: TextAlign.center,
    style: TextStyle(
      color: const Color(0xFFFF6937),
      fontSize: 10,
      fontFamily: 'Archivo',
      fontWeight: FontWeight.w600,
      height: 1.40,
    ),
  ),
)
```

**Usage:** Чат, мессенджер, сообщения между пользователями.

---

### 13. Messages / Notifications

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

### 14. Panels & Cards

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

### 15. Accordion / FAQ

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

### 16. Loading States

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

### 17. Empty States

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

### 18. Special Effects

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

**Текущая версия**: v5.10.0

### Changelog

#### v5.10.0 (2025-11-19)
- **Добавлена новая секция Calendar/Schedule Components:**
  - Комплексная система для календарей и расписаний бронирования
  - 5 специализированных компонентов с IDE AI navigation
- **Flutter Time Grid with Labels:**
  - Временная сетка с labels (10:00-23:00)
  - Time label: padding 8×5px, 11px Regular #09101D
  - Divider line: 442px width, border 0.5px #D9DDE2
  - Row spacing: 10px label-to-line, 15px vertical between rows
- **Flutter Resource/Staff Column Headers:**
  - Large avatar: 56×56px outer, 48×48px inner (without status)
  - Medium avatar: 48×48px with online status badge
  - Name label: 50px width, 11px SemiBold #09101D
  - Spacing: 5px avatar-to-name, 10px between headers
- **Flutter Online Status Badge:**
  - Size: 14×14px circle
  - Background: #11BB8D (green) for online
  - Border: 3px white
  - Position: bottom-left (left 0, top 34 for 48px avatar)
  - Color variants: green (online), red (busy), yellow (away), gray (offline)
- **Flutter Appointment Blocks:**
  - Block size: 130×40px per time slot
  - Single slot: full 15px border-radius
  - Multi-slot: top block (top radius), middle (no radius), bottom (bottom radius)
  - 5 color variants for categorization
  - Content: avatar 32×32px + time 11px + name 10px SemiBold white
  - Spacing: 5px internal
- **Flutter Available Time Slot:**
  - Size: 130×40px
  - Background: #F4F6F9 (light gray)
  - Icon: 24×24px plus icon centered
  - Border radius: 15px
  - Usage: indicates free time for booking
- **Новые цвета:**
  - `#7CC5D6` - светло-голубой (cyan) для standard appointments
  - `#F7B68A` - персиковый (peach) для wellness appointments
- **Appointment color palette:**
  - Purple (#5E38BA): VIP/premium services
  - Cyan (#7CC5D6): Standard appointments
  - Peach (#F7B68A): Wellness/spa services
  - Blue (#4141E6): Regular appointments
  - Red (#E24949): Urgent/priority appointments
- **Typography спецификации:**
  - Time labels: 11px Archivo Regular #09101D
  - Staff names: 11px Archivo SemiBold #09101D
  - Appointment time: 11px Archivo Regular white
  - Appointment client: 10px Archivo SemiBold white
- **IDE AI Navigation markers:** Все 5 компонентов с COMPONENT, CATEGORY, TAGS, RELATED

#### v5.9.0 (2025-11-19)
- **Добавлена секция Flutter Video/Content Card with Social Proof:**
  - Комплексная карточка 230×400px с медиа контентом и социальными элементами
  - Image section: 230×230px с overlay badges
  - Overlay badges для duration ("2:12") и views ("1.342")
  - Avatar group с белой обводкой (4 avatars + counter "1k")
  - Title section: 220px width, 16px Bold #09101D
  - Author info section с avatar 40×40px и текстовой информацией
  - Content spacing: 5px between sections, 6px avatar-to-text, 10px avatar group-to-title
  - Полный Flutter код с комментариями для всех секций
  - IDE AI Navigation markers для быстрого поиска
  - Cross-references к связанным компонентам
- **Добавлена секция Flutter Avatar Groups:**
  - Группы аватаров с белой обводкой для social proof
  - Avatar outer: 32×32px, border 4px white, border-radius 30px
  - Avatar inner: 24×24px image positioned at 4px offset
  - Counter avatar: текст "1k" вместо изображения (10px w600 white)
  - Text position: top 7px (для центрирования)
  - Group spacing: 10px between avatars
  - Typical count: 4-5 avatars (4 images + 1 counter)
  - Usage notes для социального proof: участники, подписчики, команда
  - Variants: с counter/без counter, разные размеры
  - Complete Flutter код для avatar with border и counter avatar
  - IDE AI Navigation markers: CATEGORY: Avatar, Social, User Interface
- **Добавлена секция Flutter Author Info:**
  - Компонент информации об авторе контента
  - Avatar: 40×40px outer, 32×32px inner (positioned at 4px offset)
  - Name: "Nicole Dowson", 13px Archivo SemiBold (w600) #09101D
  - Team/Role: "Fitness App Team", 12px Archivo Regular (w400) #373940
  - Layout: Horizontal row, spacing 6px between avatar and text
  - Text column: cross-axis start (left-aligned)
  - Usage: Для credibility и атрибуции на карточках контента
  - Variants: с verification badge, single line, interactive, with stats
  - Complete Flutter код для avatar + text column
  - IDE AI Navigation markers: CATEGORY: User Interface, Content, Author
- **IDE AI Navigation System:**
  - Добавлены HTML комментарии с метаданными для всех новых компонентов
  - Format: `<!-- COMPONENT: Name | CATEGORY: Categories | TAGS: tags | RELATED: Components -->`
  - Cross-references между связанными компонентами
  - Улучшенная навигация для IDE AI ассистентов
- **Typography спецификации:**
  - Title card: 16px Archivo Bold (w700) #09101D
  - Author name: 13px Archivo SemiBold (w600) #09101D
  - Author team: 12px Archivo Regular (w400) #373940
  - Counter text: 10px Archivo SemiBold (w600) white
- **Color спецификации:**
  - Avatar placeholder: #D9DDE2
  - Primary text: #09101D (dark black)
  - Secondary text: #373940 (gray)
  - Border white: #FFFFFF (4px for avatar groups)
- **Spacing system:**
  - Avatar group: 10px between items
  - Author info: 6px avatar-to-text
  - Card sections: 5px internal spacing
  - Avatar group to title: 10px

#### v5.8.0 (2025-11-19)
- **Добавлена секция Flutter Navigation Header:**
  - Навигационный header для социальных/сервисных приложений
  - Container height: 44px, white background
  - Avatar section: 32×32px outer, 24×24px inner, border-radius 40px, background #D9DDE2
  - Premium Badge "Get $5": height 24px, background #5E38BA, border-radius 11px, text 11px w600 white
  - Points Badge: height 36px, background #FFC043 40% opacity, border-radius 15px, text 16px w800 #23262B
  - Badge spacing: 6px internal spacing между icon и text
  - Complete Flutter код для обоих badges
- **Добавлена секция Flutter Search Input:**
  - Компактное search поле для мобильного приложения
  - Container: 44px height, padding 16px horizontal / 4px vertical
  - Input: 36px height, padding 8×7px, background #F4F6F9, border-radius 15px
  - Icon: 14×14px (меньше стандартных 20px)
  - Placeholder: "Search", #747B84, 16px Archivo Regular
  - Content padding: 5px left / 10px right, spacing 10px
  - Без border для минималистичного дизайна
- **Добавлена секция Flutter Category Cards (Horizontal Scroll):**
  - Горизонтальная галерея карточек категорий
  - Card size: 100×120px, border-radius 12px
  - Spacing: 10px между карточками
  - Container padding: 10px top/bottom, 16px left
  - Selected State: border 2px #4141E6, image 92×112px (с 4px padding), gradient overlay 51.16px from top
  - Normal State: no border, image 100×120px full, gradient overlay 50px from top
  - Gradient: transparent (#00C4C4C4) → semi-dark (#7F1D1D1D - 50% opacity), height 70px
  - Text label: 10px Archivo SemiBold white, padding 10px left/bottom, width 80-90px
  - Categories: Manicure, Pedicure, Makeup, Hair cut, Category or service
  - Complete Flutter код для selected и normal states
- **Новые цвета:**
  - `#5E38BA` - Темно-фиолетовый для premium badges и промо-акций
  - `rgba(255, 192, 67, 0.40)` (#66FFC043) - Желтый 40% opacity для points badge
  - `rgba(29, 29, 29, 0.50)` (#7F1D1D1D) - Черный 50% opacity для gradient overlays на карточках
- **Новые overlay цвета:**
  - `--overlay-black-50`: rgba(29, 29, 29, 0.50) для градиентов на карточках
  - `--overlay-yellow-40`: rgba(255, 192, 67, 0.40) для points badge background
- **Typography спецификации:**
  - Premium badge: 11px Archivo SemiBold (w600) white
  - Points badge: 16px Archivo ExtraBold (w800) #23262B
  - Search placeholder: 16px Archivo Regular (w400) #747B84
  - Category card label: 10px Archivo SemiBold (w600) white
- **Icon спецификации:**
  - Avatar: 32×32px outer, 24×24px inner (circle)
  - Points badge icon: 24×24px, padding 2px, border-radius 100px
  - Search icon: 14×14px (компактный для баланса)

#### v5.7.0 (2025-11-19)
- **Добавлена секция Flutter Dropdown/Select Fields:**
  - Поля выбора для мобильного приложения с 10 различными вариантами компоновки
  - Общие спецификации: Container 375px, Input height 46px (выше чем text input!)
  - Container padding: 16px horizontal / 10px vertical
  - Input padding: 4px top/bottom, 20px left, 15px right
  - Border radius: 15px, Border: 2px solid #F4F6F9 (disabled state)
  - Icon size: 30×30px (квадратные с border-radius 10px, круглые с border-radius 50px)
  - Chevron icons: 24×24px
  - Typography: Label 12px Regular, Value 14px SemiBold, Helper 12px Regular
  - Spacing: 5px, 8px, 10px между элементами
- **10 Вариантов Dropdown/Select:**
  1. Single Line with Square Icon - одна строка с квадратной иконкой (Netflix)
  2. Two-Line with Circle Icon + Chevron - двухстрочный с круглой иконкой (Company/Dropbox)
  3. Two-Line without Icon - двухстрочный без иконки (Your email)
  4. Two-Line without Icon + Helper Text - с helper текстом (Your name)
  5. Two-Line with Square Icon + Chevron - криптовалюта с квадратной иконкой
  6. Two-Line with Circle Icon + Chevron - Bitcoin amount selector
  7. Single Line Long Text + Circle Icon + Ticker + Chevron - Bitcoin address
  8. Circle Icon Only + Chevron on Left - переключатель валюты (BTC)
  9. Circle Icon with Two Chevrons - конвертация валюты
  10. Circle Icon + Chevron + Two-Line Right-Aligned - отображение цены
- **Ключевые отличия от Text Input:**
  - Input height 46px вместо 36px для лучшей читаемости dropdown содержимого
  - Container padding 10px vertical вместо 5px
  - Больше вариантов компоновки с иконками (30×30px вместо 20×20px)
  - Поддержка двухстрочных значений (label + value) с spacing 5px
- **Disabled State спецификации:**
  - Text color: #D9DDE2 для всех текстовых элементов
  - Background: #F4F6F9
  - Border: 2px solid #F4F6F9 (совпадает с фоном)
- **Flutter код примеры:**
  - Complete код для Two-Line with Circle Icon + Chevron
  - Complete код для Circle Icon + Chevron + Two-Line Right-Aligned

#### v5.6.0 (2025-11-19)
- **Добавлена секция Flutter Text Input Fields:**
  - Полный набор из 9 состояний текстовых полей для мобильного приложения
  - Enabled (Default) - начальное состояние с серым фоном #F4F6F9
  - Focus - фокус с border 2px #09101D, видимый курсор
  - Active - Typing - активный ввод с курсором и иконкой очистки
  - Pressed - момент нажатия с темным фоном #EAEEF2
  - Complete - успешное заполнение с checkmark иконкой
  - Incomplete - требует заполнения с warning иконкой
  - Positive (Success) - успешная валидация, зеленая граница #11BB8D, фон rgba(17, 187, 141, 0.05)
  - Negative (Error) - ошибка валидации, красная граница #DA1414, фон rgba(218, 20, 20, 0.05)
  - Disabled - отключенное состояние, светло-серый #D9DDE2
- **Новый цвет:**
  - `#DA1414` - Темно-красный для error borders в input полях
- **Спецификации Input полей:**
  - Container: 375px width, padding 16px horizontal / 5px vertical
  - Input: 36px height, padding 16px left / 20px right, border-radius 15px
  - Icon: 20px × 20px для left/right иконок
  - Cursor: 2px × 16px
  - Typography: Label/Input/Helper - 14px Archivo (w600/w400/w400)
  - Spacing: 8px между label, input и helper text
- **Validation States:**
  - Positive: border 2px #11BB8D, background 5% opacity
  - Negative: border 2px #DA1414, background 5% opacity, error text #E24949
- **Flutter код примеры:**
  - Complete код для Positive (Success) state
  - Complete код для Negative (Error) state

#### v5.5.0 (2025-11-19)
- **Добавлено 15 Advanced List Item Variants:**
  1. Range Slider List Item - с двойным ползунком для диапазона значений
  2. Section Header List Item - заголовки секций с разделителями
  3. User Follow List Item - социальные списки с кнопкой Follow (height 36px)
  4. Crypto/Asset List Item - списки криптовалют с графиками и процентами
  5. Simple Asset List Item - упрощенные списки активов
  6. Expandable/Accordion List Item - раскрывающиеся элементы
  7. File/Document List Item - файлы с метаданными (автор, дата)
  8. Photo Grid List Item - сетка фотографий 3×2 (100px each)
  9. Grid Icon List Item - мини-сетка иконок 2×2 (25px each)
  10. Icon List Item - компактные элементы с одной иконкой
  11. Product/Album List Item - альбомы с крупным изображением (90×90px)
  12. Filter/Sort Header - headers с кнопками фильтра и сортировки
  13. Avatar with Details List Item - стандартные элементы с аватаром
  14. Checkbox Agreement List Item - соглашения с чекбоксами
  15. Language Selector List Item - выбор языка с флагами (40×30px)
- **Новые цвета:**
  - `#23262B` - Очень темный серый для основного текста
  - `#303239` - Темно-серый для метаданных (даты, авторы)
  - `#E24949` - Красный для ошибок и негативных значений
  - `#F8F8FA` - Очень светлый серый для иконок и плейсхолдеров
  - `#B7D5D5` - Бирюзовый для декоративных фонов
  - `#46467F` - Темно-синий для флагов и декоративных элементов
- **Обновлены Flutter Avatar Variants:**
  - Flutter Avatar Small (40×40 outer, 32×32 inner) - для компактных списков
  - Flutter Avatar Medium (48×48 outer, 40×40 inner) - для стандартных list items
  - Flutter Avatar Large (56×56 outer, 48×48 inner) - NEW! для follow lists
- **Range Slider Component:**
  - Track: 4px height, colors #F4F6F9 (inactive) / #4141E6 (active)
  - Thumb: 20×20px, border 4px rgba(11, 36, 251, 0.25)
  - Value Tooltip: dark background #09101D, white text, padding 16×12px
- **Button Specifications:**
  - Follow Button: height 36px, padding 16×10px, background #4141E6, border-radius 15px
- **Badge Specifications:**
  - Crypto Badge: padding 5×2px, background #EAEEF2, border-radius 4px, text 10px
- **Grid Specifications:**
  - Photo Grid: 3×2 layout, 100px items, 10px spacing, border-radius 16px
  - Icon Grid: 2×2 layout, 25px items, 5px spacing, border-radius 5px
- **Text Specifications:**
  - Metadata text: 12px, Archivo SemiBold (w600), color #303239, line-height 1.67
  - Percentage negative: 11px/13px, Archivo Bold/SemiBold, color #E24949
  - Agreement text: 13px, Archivo Regular, color #23262B, link #4141E6
- **Spacing & Layout:**
  - Filter/Sort header: 143.50px filter width, 10px spacing
  - Crypto list: 60×40px chart area, 20px section spacing
  - File list: 64×64px icon container, 2px title spacing, 4px metadata spacing

#### v5.4.0 (2025-11-19)
- **Добавлена секция Chat / Messaging (Flutter):**
  - Chat Message Bubbles (incoming 248px, outgoing 260px)
  - Chat Avatar Small variant (32×32px outer, 24×24px inner, circle)
  - Date Dividers с 5 вариантами (Yesterday, Mon 30, June 2021, 2021, NEW MESSAGES)
- **Новые цвета для чата:**
  - `#747B84` - Приглушенный серый для timestamps и метаданных
  - `#FFC043` - Желтый для date dividers
  - `#05944F` - Темно-зеленый для date dividers
  - `#FF6937` - Оранжевый для date dividers и new messages
- **Спецификации Chat/Messaging:**
  - Incoming message: light gray background (#F4F6F9), left aligned
  - Outgoing message: dark gray background (#414249), right aligned
  - Message text: Archivo Regular 16px
  - Time stamps: Archivo Regular 11px
  - Date divider badges с цветными backgrounds (10% opacity)
  - NEW MESSAGES divider без фона, оранжевый текст
- **Перенумерация секций:** Chat/Messaging стала секцией 12, последующие секции сдвинуты (Messages → 13, Panels → 14, Accordion → 15, Loading → 16, Empty → 17, Special Effects → 18)

#### v5.3.0 (2025-11-19)
- **Добавлены Flutter List Items:**
  - List Item компонент (375px width) с integrated form controls
  - Toggle Switch List Item (51px toggle, title width 276px)
  - Radio Button List Item (title width 309px)
  - Checkbox List Item (title width 309px)
  - Divider спецификации (1px height, color #EAEEF2)
- **Обновлен Toggle Switch:**
  - Исправлена ширина Large Toggle: 51px (было 52px)
  - Добавлен зеленый active state (#11BB8D)
  - Обновлены все состояния (off, on active, on blue, disabled)
- **Новые цвета:**
  - `#11BB8D` - Зеленый для активного toggle и success состояний
  - `#414249` - Темно-серый для subtitle/вторичного текста в списках
- **Text спецификации:**
  - Title: Archivo SemiBold 14px, color #09101D
  - Subtitle: Archivo Regular 13px, color #414249
- **Layout детали:**
  - Padding specs для controls (16px для toggle, 10px для radio/checkbox)
  - Divider left offset (64px для toggle, 36px для radio/checkbox)
  - Vertical padding 10px для content area
- **Перенумерация секций:** List Items теперь секция 11, последующие сдвинуты

#### v5.2.0 (2025-11-19)
- **Добавлены Flutter Form Controls:**
  - Radio Button (24×24px, 3 состояния: unchecked, checked, disabled)
  - Toggle Switch - Large (52×31px, 3 состояния)
  - Toggle Switch - Small (32×20px, 3 состояния)
  - Checkbox (24×24px, 18×18px внутренний box)
- **Новые цвета:**
  - `#EAEEF2` - Светлая граница для неактивных form controls
  - `rgba(11, 36, 251, 0.33)` - Синий с opacity для disabled состояний
- **Спецификации:**
  - Radio Button Group Container (371.50×140px)
  - Детальные размеры и spacing для всех состояний
  - Flutter код примеры для каждого компонента

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
