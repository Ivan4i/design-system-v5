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

### Background Colors

```css
/* Фоновые цвета из Flutter кода */
--color-bg-primary: #FFFFFF;
--color-bg-secondary: #F4F6F9;       /* Светло-серый фон */
--color-bg-tertiary: #D9DDE2;        /* Серый фон */
--color-bg-overlay: #EFD1D5DB;       /* Overlay для клавиатуры */
--color-bg-elevated: #FDFDFD;        /* Приподнятый белый фон */
```

### Text Colors

```css
/* Цвета текста из Flutter кода */
--color-text-primary: #09101D;       /* Основной черный текст */
--color-text-secondary: #23262B;     /* Вторичный темный текст */
--color-text-tertiary: #2A2B2F;      /* Третичный темный текст */
--color-text-gray: #373940;          /* Серый текст (из Content Card) */
--color-text-muted: rgba(0, 0, 0, 0.55);  /* Приглушенный текст */
```

### Accent Colors

```css
/* Акцентные цвета из Flutter кода */
--color-primary: #4141E6;            /* Основной синий (кнопки) */
--color-accent-blue: #4141E6;
--color-accent-purple: #7B61FF;      /* Фиолетовый акцент (borders) */
--color-accent-green: #11BB8D;       /* Зеленый акцент (border) */
--color-accent-green-light: #0C11BB8D;  /* Зеленый с прозрачностью */
--color-accent-pink: #FC466B;        /* Розовый градиент */
```

### Brand Colors

```css
/* Brand цвета из Flutter кода (Start Screens) */
--color-brand-orange: #FF6937;       /* Основной оранжевый (primary actions) */
--color-brand-red: #E24949;          /* Красный (secondary actions) */
--color-social-facebook: #4C69AB;    /* Facebook синий */
--color-social-apple: #23262B;       /* Apple темно-серый */
```

### Gradient Colors

```css
/* Цвета градиентов из Flutter кода */
--gradient-purple: #833AB4;          /* Фиолетовый (Instagram gradient) */
--gradient-red: #FD1D1D;             /* Красный (Instagram gradient) */
--gradient-orange: #FCB045;          /* Оранжевый (Instagram gradient) */

/* Instagram-style gradient */
--gradient-instagram: linear-gradient(135deg, #833AB4 0%, #FD1D1D 50%, #FCB045 100%);

/* Pricing/Subscription gradient (из Buttons Light) */
--gradient-pricing-start: #FF512F;    /* Оранжево-красный (начало) */
--gradient-pricing-end: #DD2476;      /* Розовый (конец) */
--gradient-pricing: linear-gradient(90deg, #FF512F 0%, #DD2476 100%);

/* Outline button colors (из Buttons Light) */
--outline-border-orange: #FE5032;     /* Оранжевый для outline кнопок */
```

### Payment System Colors

```css
/* Цвета платежных систем */
--mastercard-red: #DA1414;
--mastercard-orange: #F79E1C;
```

### Border Colors

```css
/* Цвета границ */
--color-border-primary: #D9DDE2;
--color-border-focus: #4141E6;
--color-border-success: #11BB8D;
--color-border-pink: #FC466B;
--color-border-purple: #7B61FF;
```

### Divider Colors

```css
/* Цвета разделителей из Flutter кода */
--color-divider-light: #EAEEF2;      /* Светлый divider (1px) */
--color-divider-thick: #F4F6F9;      /* Толстый divider (10px) */
```

### Chart Colors

```css
/* Цвета для графиков из Flutter кода */
--chart-grid-light: #A4ABB3;         /* Светло-серый для линий сетки */
--chart-grid-dark: #747B84;          /* Темно-серый для осей */
--chart-label-text: #09101D;         /* Черный для подписей */
```

### Progress & Stepper Colors

```css
/* Цвета для прогресс-баров и степперов из Flutter кода */
--color-progress-blue: #0B24FB;             /* Синий для активного прогресса */
--color-progress-inactive: rgba(9, 16, 29, 0.10);  /* Неактивный сегмент - #1909101D */
--color-progress-partial: rgba(11, 36, 251, 0.30); /* Частичный прогресс - #4C0B24FB */
--color-stepper-active: #4141E6;            /* Активный шаг (синий) */
--color-stepper-inactive: #EAEEF2;          /* Неактивный шаг (светло-серый) */
--color-stepper-current: #4141E6;           /* Текущий шаг (синий с кольцом) */
```

### Input Field Colors

```css
/* Цвета для текстовых полей из Flutter кода */
--input-bg-normal: #F4F6F9;                 /* Обычный фон input */
--input-bg-pressed: #EAEEF2;                /* Фон при нажатии */
--input-bg-disabled: #EAEEF2;               /* Фон disabled состояния */
--input-bg-success: rgba(17, 187, 141, 0.05);  /* Фон успешного ввода - #0C11BB8D */
--input-bg-error: rgba(218, 20, 20, 0.05);     /* Фон ошибки - #0CDA1414 */
--input-placeholder: #747B84;               /* Цвет placeholder */
--input-border-focus: #09101D;              /* Черная граница при фокусе */
--input-border-success: #11BB8D;            /* Зеленая граница (success) */
--input-border-error: #DA1414;              /* Красная граница (error) */
--input-text-error: #E24949;                /* Красный текст ошибки */
--input-text-disabled: #D9DDE2;             /* Серый текст disabled */
```

### Shadow Colors

```css
/* Тени из Flutter кода */
--shadow-keyboard-dark: #898A8D;
--shadow-keyboard-light: rgba(4, 4, 15, 0.36);
--shadow-button-dark: rgba(0, 0, 0, 0.35);
--shadow-tooltip: rgba(0, 0, 0, 0.10);      /* Тень для светлых tooltips - #19000000 */
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
--font-size-8: 0.5rem;        /* 8px - лейблы графиков */
--font-size-10: 0.625rem;     /* 10px - метки графиков (Q1, Q2...) */
--font-size-11: 0.6875rem;    /* 11px */
--font-size-12: 0.75rem;      /* 12px */
--font-size-13: 0.8125rem;    /* 13px - из Flutter кода */
--font-size-14: 0.875rem;     /* 14px - из Flutter кода */
--font-size-15: 0.9375rem;    /* 15px */
--font-size-16: 1rem;         /* 16px - из Flutter кода */
--font-size-18: 1.125rem;     /* 18px - из Flutter кода */
--font-size-23: 1.4375rem;    /* 23px - клавиатура iOS */
--font-size-24: 1.5rem;       /* 24px */
--font-size-26: 1.625rem;     /* 26px */
--font-size-27: 1.6875rem;    /* 27px - иконки клавиатуры */
--font-size-32: 2rem;         /* 32px */
--font-size-72: 4.5rem;       /* 72px - крупные заголовки */
```

### Font Weights

```css
--font-weight-regular: 400;
--font-weight-medium: 500;
--font-weight-semibold: 600;
--font-weight-bold: 700;
--font-weight-extrabold: 800;  /* Из Flutter кода для крупных заголовков */
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
--line-height-70: 0.70;       /* 70% - для крупных заголовков */
--line-height-140: 1.40;      /* 140% - основной из Flutter кода */
```

### Letter Spacing

```css
/* Из Flutter кода клавиатуры */
--letter-spacing-tight: -0.32px;   /* Для клавиатуры */
--letter-spacing-normal: 0;        /* По умолчанию */
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

### Text Styles (Из Flutter кода)

#### Card Title
- **Bold**: Font: 18px (1.125rem), Weight: 700, Line Height: 140%, Color: #09101D
- **Использование**: Заголовки карточек

#### Card Description
- **Regular**: Font: 14px (0.875rem), Weight: 400, Line Height: 140%, Color: #23262B
- **Использование**: Описание в карточках

#### Button Text
- **Semibold**: Font: 14px (0.875rem), Weight: 600, Line Height: 140%, Color: #FFFFFF (на primary кнопках)
- **Height**: 44px

#### Link Text
- **Regular**: Font: 14px (0.875rem), Weight: 400, Line Height: 140%, Color: #4141E6
- **Использование**: Ссылки "More info"

#### Small Text
- **Regular**: Font: 13px (0.8125rem), Weight: 400, Line Height: 140%, Color: #23262B
- **Использование**: Мелкий текст подсказок

#### Keyboard Keys
- **Regular**: Font: 23px (1.4375rem), Weight: 400, Color: #000000
- **Использование**: Буквы на клавиатуре iOS

#### Keyboard Actions
- **Regular**: Font: 16px (1rem), Weight: 400, Letter Spacing: -0.32px, Color: #000000
- **Использование**: Текст на функциональных кнопках клавиатуры

#### Badge Text
- **Semibold**: Font: 10px (0.625rem), Weight: 600, Line Height: 140%, Color: #FFFFFF
- **Использование**: Текст в badge (например, "Live")

#### Chart Labels
- **Quarter Labels (Q1-Q4)**: Font: 10px (0.625rem), Weight: 600, Color: #09101D, Line Height: 140%
- **Использование**: Метки кварталов на графиках

#### Chart Legend Labels
- **Bold**: Font: 8px (0.5rem), Weight: 700, Color: #09101D, Line Height: 140%
- **Использование**: Подписи в легенде графика

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
/* Из Flutter кода */
--radius-none: 0;
--radius-sm: 0.3125rem;   /* 5px - клавиатура */
--radius-base: 0.75rem;   /* 12px - badge Live */
--radius-md: 0.9375rem;   /* 15px - кнопки, inputs */
--radius-lg: 1.25rem;     /* 20px - карточки */
--radius-xl: 1.875rem;    /* 30px - аватары */
--radius-2xl: 2rem;       /* 32px */
--radius-3xl: 2.5rem;     /* 40px - контейнеры */
--radius-full: 100px;     /* Полностью круглый - кнопки, иконки, аватары */
```

### Shadows

#### Shadows из Flutter кода

```css
/* Тени клавиатуры iOS */
--shadow-keyboard-key: 0 1px 0 0 rgba(0, 0, 0, 0.35);
--shadow-keyboard-dark: 0 1px 0 0 #898A8D;
--shadow-keyboard-light: 0 1px 0 0 rgba(4, 4, 15, 0.36);

/* Card Shadows */
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

#### Tooltip Shadows

```css
/* Тень для светлых tooltips из Flutter кода */
--shadow-tooltip: 0 6px 15px 0 rgba(0, 0, 0, 0.10);
```

### Borders

#### Border Width

```css
/* Из Flutter кода */
--border-width-0: 0;
--border-width-1: 1px;    /* По умолчанию */
--border-width-2: 2px;    /* Аватары, акценты, focus states */
--border-width-4: 4px;    /* Группы аватаров */
```

#### Border Offset

```css
--border-offset-0: 0;
--border-offset-1: 1px;
--border-offset-2: 2px;
```

### Opacity Scale

```css
/* Из Flutter кода */
--opacity-0: 0;
--opacity-10: 0.1;
--opacity-20: 0.2;
--opacity-25: 0.25;       /* Фоновый overlay - из кода */
--opacity-30: 0.3;
--opacity-40: 0.4;
--opacity-50: 0.5;
--opacity-55: 0.55;       /* Приглушенный текст - из кода */
--opacity-60: 0.6;
--opacity-70: 0.7;
--opacity-80: 0.8;
--opacity-90: 0.9;
--opacity-100: 1;
```

---

## Компоненты

### 1. Cards

#### Basic Card (из Flutter кода)

- **Width**: 375px (max width для mobile), 327px (внутренний content)
- **Padding**:
  - Top: 8px
  - Left/Right: 16px
  - Bottom: 16px
- **Border Radius**: 20px
- **Background**: #FFFFFF
- **Shadow**: None (clean design)
- **Gap между секциями**: 20px

**Content Structure:**
- **Icon/Image Section**:
  - Spacing: 8px между элементами
  - Icon container: 60px × 60px, padding: 2px, border-radius: 100px
- **Text Section**:
  - Title: 18px, weight: 700, color: #09101D, line-height: 140%
  - Description: 14px, weight: 400, color: #23262B, line-height: 140%
  - Width: 327px, text-align: center

**Варианты:**

#### Card with Icon
- **Icon Container**: 60px × 60px, circular (border-radius: 100px)
- **Close Button**: 24px × 24px, top-right position, background: #F4F6F9, border-radius: 100px

#### Card with Image
- **Image Size**: 79.01px × 79.01px
- **Border Radius**: 15px
- **Background**: #F4F6F9 (fallback)

#### Card with Avatar
- **Avatar Container**: 56px × 56px (large), 48px × 48px (medium), 40px × 40px (small), 32px × 32px (extra small)
- **Border**: 2px solid color (для акцентов, например #FC466B)
- **Border Radius**: Circular (30px для 56px avatar)
- **Live Badge**:
  - Size: 28px × 14px
  - Padding: 4px horizontal, 2px vertical
  - Border: 1px solid white
  - Gradient: linear-gradient(90deg, #833AB4, #FD1D1D, #FCB045)
  - Border Radius: 12px
  - Text: 10px, weight: 600, color: white

#### Card with Payment Method
- **Input Height**: 46px
- **Padding**: 16px left, 20px right
- **Border**: 2px solid #11BB8D
- **Border Radius**: 15px
- **Background**: rgba(17, 187, 141, 0.05)
- **Mastercard Icon**: 20px × 20px
  - Red circle: #DA1414
  - Orange circle: #F79E1C

#### Пример использования

```css
.card {
  width: 100%;
  max-width: 375px;
  padding: 8px 16px 16px;
  border-radius: 20px;
  background: #FFFFFF;
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.card__content {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
}

.card__title {
  font-size: 18px;
  font-weight: 700;
  color: #09101D;
  line-height: 1.4;
  text-align: center;
  max-width: 327px;
}

.card__description {
  font-size: 14px;
  font-weight: 400;
  color: #23262B;
  line-height: 1.4;
  text-align: center;
  max-width: 327px;
}
```

---

### 2. Buttons (из Flutter кода)

#### Button Sizes

**Standard Button:**
- Height: 44px
- Padding: 16px horizontal, 10px vertical
- Font Size: 14px, Weight: 600

**Large Button (Onboarding/CTA):**
- Height: 52px
- Padding: 16px horizontal, 10px vertical
- Font Size: 15px, Weight: 600

**Social Button:**
- Height: 44px
- Padding: 16px horizontal, 10px vertical
- Border Radius: 4px (меньше!)
- Icon: 20px

#### Primary Button

- **Size**: 44px height (standard), 52px (large CTA)
- **Padding**: 16px horizontal, 10px vertical
- **Border Radius**: 15px
- **Typography**:
  - Font Size: 14px (standard), 15px (large)
  - Font Weight: 600 (semibold)
  - Line Height: 140%
- **Colors**:
  - Background: #4141E6
  - Text: #FFFFFF
  - Shadow: None (flat design)
- **Width**: 100% (full-width)
- **Alignment**: Center (text и иконки)

**States:**
- **Default**: Background: #4141E6, Text: white
- **Hover**: Легкое затемнение (opacity: 0.9)
- **Active**: Затемнение (opacity: 0.8)
- **Disabled**: Background: #D9DDE2, Text: rgba(0,0,0,0.4), Cursor: not-allowed

#### Brand Orange Button (Primary CTA)

- **Size**: 52px height (large)
- **Padding**: 16px horizontal, 10px vertical
- **Border Radius**: 15px
- **Background**: #FF6937 (brand orange)
- **Text**: white, 15px, weight 600
- **Usage**: "Sign up", главные CTA

#### Brand Red Button (Secondary CTA)

- **Size**: 52px height (large)
- **Padding**: 16px horizontal, 10px vertical
- **Border Radius**: 15px
- **Background**: #E24949 (brand red)
- **Text**: white, 15px, weight 600
- **Icon**: 24px (left side), spacing 8px
- **Usage**: "Sign in via mobile number"

#### Gradient Button (Pricing/Premium)

- **Size**: 44px height (standard)
- **Padding**: 16px horizontal, 10px vertical
- **Border Radius**: 30px (большой!)
- **Background**: linear-gradient(90deg, #FF512F 0%, #DD2476 100%)
- **Text**: 14px, weight 600, white
- **Spacing**: 8px между текстом и badge
- **Usage**: Pricing buttons, premium CTA, subscription actions

**С Price Badge:**
- Badge height: 20px
- Badge padding: 10px horizontal, 5px vertical
- Badge radius: 12px
- Badge background: white
- Badge text: 11px, weight 600, color #FF512F

**Example:**
- Primary: "\$ 86.99/Year" + "Save 23%" badge
- Secondary: "\$ 9.49/Month" without badge

#### Outline Button (Colored Border)

- **Size**: 44px height (standard)
- **Padding**: 16px horizontal, 10px vertical
- **Border Radius**: 30px (большой!)
- **Border**: 1px solid #FE5032
- **Background**: white
- **Text**: 14px, weight 600, color #E24949
- **Usage**: Secondary pricing option, alternative CTA

#### Secondary Button / Text Button

- **Size**: Same as Primary
- **Padding**: 16px horizontal, 5px vertical
- **Border Radius**: 15px
- **Colors**:
  - Background: transparent
  - Text: #09101D (default) или #4141E6 (link style)
  - Shadow: None
- **Typography**: 14px, weight: 400 или 600, line-height: 140%

**Варианты:**

#### Link Button
- **Text Color**: #4141E6
- **Background**: transparent
- **Font Weight**: 400
- **Underline**: None (optional on hover)
- **Использование**: "More info", "Dismiss"

#### Two-Button Layout
- **Container**: Row с gap: 10px
- **Buttons**: Flex-grow: 1 (равная ширина)
- **Left Button**: Text style (Dismiss)
- **Right Button**: Primary style (Action - "Appk", etc.)

#### iOS Keyboard Button
- **Key Size**: 31.5px × 42px
- **Padding**: Centered text
- **Border Radius**: 5px
- **Background**: #FFFFFF
- **Shadow**: 0 1px 0 0 rgba(0,0,0,0.35)
- **Text**: 23px, weight: 400, color: #000000

#### Functional Keys (Space, Return, etc.)
- **Space Bar**: Width: 182.49px, Height: 42px
- **Return Key**: Width: 87.73px, Height: 42px, Background: #ADB3BC
- **123 Key**: Smaller width
- **Border Radius**: 5px
- **Shadow**: 0 1px 0 0 (varies by type)

#### Social Auth Buttons

**Layout:**
- **Container**: Row with equal spacing (gap: 10px)
- **Buttons**: Expanded (равная ширина, flex: 1)
- **Width**: 3 buttons per row
- **Padding**: 16px horizontal, 10px vertical (container)

**Button Specifications:**
- **Height**: 44px
- **Border Radius**: 4px (меньше чем у обычных!)
- **Padding**: 16px horizontal, 10px vertical
- **Icon**: 20px (centered)

**Варианты:**

**Google Button:**
- Background: #F4F6F9 (светло-серый)
- Icon: Google logo (20px)

**Facebook Button:**
- Background: #4C69AB (Facebook blue)
- Icon: Facebook logo (20px, white)

**Apple Button:**
- Background: #23262B (темно-серый/черный)
- Icon: Apple logo (20px, white)

#### Close Button (в карточках)
- **Size**: 24px × 24px
- **Padding**: 6px (иконка 12px)
- **Border Radius**: 100px (circular)
- **Background**: #F4F6F9
- **Position**: Absolute, top-right

---

### 3. Inputs (из Flutter кода)

#### Text Input Field

**Container:**
- **Width**: 375px (mobile full width)
- **Padding**: 16px horizontal, 5px vertical
- **Spacing**: 8px между элементами (label, input, helper)

**Input Field:**
- **Height**: 36px
- **Padding**: left: 16px, right: 20px
- **Border Radius**: 15px
- **Font**: 14px, weight: 400, line-height: 140%

**Label:**
- **Font Size**: 14px
- **Font Weight**: 600 (semibold)
- **Color**: #09101D
- **Line Height**: 140%

**Helper Text:**
- **Font Size**: 14px
- **Font Weight**: 400
- **Color**: #747B84
- **Line Height**: 140%

**Placeholder:**
- **Text**: "Enter here..."
- **Font Size**: 14px
- **Font Weight**: 400
- **Color**: #747B84
- **Line Height**: 140%

**Clear/Action Icon:**
- **Size**: 20px × 20px
- **Position**: Right side of input

#### Input States

**1. Enabled (Default):**
```css
.input--enabled {
  background: #F4F6F9;
  border: none;
  color: #09101D;
}
.input--enabled::placeholder {
  color: #747B84;
}
```

**2. Focus:**
```css
.input--focus {
  background: #F4F6F9;
  border: 2px solid #09101D;
  outline: none;
}
```

**3. Pressed:**
```css
.input--pressed {
  background: #EAEEF2;
  border: none;
}
```

**4. Active - Typing:**
```css
.input--active {
  background: #F4F6F9;
  border: 2px solid #09101D;
}
/* With clear icon visible */
```

**5. Complete (Filled):**
```css
.input--complete {
  background: #F4F6F9;
  border: none;
  color: #09101D;
}
/* Clear icon (X) visible on right */
```

**6. Incomplete:**
```css
.input--incomplete {
  background: #F4F6F9;
  border: none;
}
/* Clear icon visible */
```

**7. Positive (Success):**
```css
.input--success {
  background: rgba(17, 187, 141, 0.05);
  border: 2px solid #11BB8D;
  color: #09101D;
}
/* Check icon visible on right */
```

**8. Negative (Error):**
```css
.input--error {
  background: rgba(218, 20, 20, 0.05);
  border: 2px solid #DA1414;
  color: #09101D;
}
.input--error + .helper-text {
  color: #E24949;
}
/* Error icon visible on right */
```

**9. Disabled:**
```css
.input--disabled {
  background: #EAEEF2;
  border: none;
  color: #D9DDE2;
  cursor: not-allowed;
  pointer-events: none;
}
.input--disabled::placeholder {
  color: #D9DDE2;
}
.label--disabled {
  color: #D9DDE2;
}
.helper-text--disabled {
  color: #D9DDE2;
}
```

#### Input Usage Example

```css
/* Base Input */
.input-field {
  width: 100%;
  max-width: 375px;
  padding: 16px;
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.input-field__label {
  font-size: 14px;
  font-weight: 600;
  color: #09101D;
  line-height: 1.4;
}

.input-field__input {
  width: 100%;
  height: 36px;
  padding: 0 20px 0 16px;
  border-radius: 15px;
  background: #F4F6F9;
  border: none;
  font-size: 14px;
  font-weight: 400;
  color: #09101D;
  line-height: 1.4;
  transition: all 0.2s ease;
}

.input-field__input::placeholder {
  color: #747B84;
}

.input-field__input:focus {
  border: 2px solid #09101D;
  outline: none;
}

.input-field__input:disabled {
  background: #EAEEF2;
  color: #D9DDE2;
  cursor: not-allowed;
}

.input-field__helper {
  font-size: 14px;
  font-weight: 400;
  color: #747B84;
  line-height: 1.4;
}

.input-field__input.error {
  background: rgba(218, 20, 20, 0.05);
  border: 2px solid #DA1414;
}

.input-field__helper.error {
  color: #E24949;
}

.input-field__input.success {
  background: rgba(17, 187, 141, 0.05);
  border: 2px solid #11BB8D;
}
```

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

### 5. Dividers (из Flutter кода)

#### Thin Divider (1px)

- **Height**: 1px
- **Width**: 100% (full width)
- **Color**: #EAEEF2
- **Padding**: 5px vertical (контейнер)
- **Margin**: 0
- **Usage**: Разделение секций контента

**Варианты с отступами:**
```
No indent: 0px left padding
Level 1:   16px left padding
Level 2:   36px left padding
Level 3:   52px left padding
Level 4:   74px left padding
Level 5:   84px left padding
```

#### Thick Divider (10px)

- **Height**: 10px
- **Width**: 100% (full width)
- **Color**: #F4F6F9
- **Padding**: 0
- **Margin**: 0
- **Usage**: Сильное визуальное разделение секций

#### Divider Container

**Example Container:**
- **Width**: 475px (или responsive)
- **Padding**: 50px all sides
- **Border**: 1px solid #7B61FF
- **Border Radius**: 15px
- **Background**: transparent
- **Spacing between dividers**: 42px

#### Text Style для заголовка секции Divider

- **Font Size**: 72px
- **Font Weight**: 800 (extrabold)
- **Line Height**: 0.70 (70%)
- **Color**: #09101D
- **Font Family**: Archivo

#### Использование

```css
/* Thin divider */
.divider-thin {
  width: 100%;
  height: 1px;
  background: #EAEEF2;
  padding: 5px 0;
}

/* Thick divider */
.divider-thick {
  width: 100%;
  height: 10px;
  background: #F4F6F9;
}

/* С отступом (Level 1) */
.divider-indent-1 {
  padding-left: 16px;
  padding-right: 16px;
}

/* С отступом (Level 2) */
.divider-indent-2 {
  padding-left: 36px;
  padding-right: 16px;
}
```

---

### 6. Forms

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

### 8. Charts (из Flutter кода)

#### Quarterly Bar Chart (4 Quarters)

**Container:**
- **Width**: 375px (mobile full width)
- **Height**: 185px (chart area)
- **Padding**: 16px horizontal, 10px vertical
- **Background**: Transparent

**Bar Specifications:**
- **Width**: Равномерно распределенные (Expanded widgets)
- **Height**: 166px (когда повернут вертикально)
- **Transform**: Повернут на -90° (rotateZ(-1.57))
- **Border**: 1px solid #A4ABB3
- **Border Alignment**: strokeAlignCenter
- **Background**: Transparent (только border)
- **Spacing между барами**: 10px

**Quarter Labels (Q1, Q2, Q3, Q4):**
- **Font Size**: 10px
- **Font Weight**: 600 (semibold)
- **Color**: #09101D
- **Text Align**: Center
- **Line Height**: 140%
- **Padding**: 5px horizontal
- **Border Radius**: 10px
- **Spacing от бара**: 5px

**Chart Layout:**
- **Row Layout**: 4 равномерных колонки
- **Column per Quarter**:
  - Bar (166px height, rotated)
  - Spacing (5px)
  - Label (Q1-Q4)

#### Chart Legend

**Container:**
- **Width**: 504.38px (или расчетная для mobile)
- **Height**: 160px (auto по контенту)
- **Padding**: 10px top, 16px right, 10px bottom
- **Spacing между строками**: 15px

**Legend Items:**
- **Label Font Size**: 8px
- **Label Font Weight**: 700 (bold)
- **Label Color**: #09101D
- **Label Padding**: Wrapped in container с border-radius 10px
- **Label Spacing**: 1px internal

**Legend Lines:**
- **Border**: 1px solid #747B84
- **Alignment**: strokeAlignCenter
- **Width**: Expanded (растягивается)
- **Spacing от label**: 10px

**Legend Row Structure:**
```
[Label] ─────────────────────
```

#### Grid Lines (Horizontal)

- **Border Width**: 1px
- **Color**: #747B84 (темно-серый)
- **Style**: Solid
- **Stroke Align**: Center
- **Spacing**: 15px между линиями

#### Vertical Grid Lines

- **Border Width**: 1px
- **Color**: #A4ABB3 (светло-серый)
- **Style**: Solid
- **Использование**: Для баров и вертикальных разделителей

#### Chart Typography

**Labels (Quarters):**
- Font: 10px, Weight: 600, Color: #09101D

**Legend Labels:**
- Font: 8px, Weight: 700, Color: #09101D

**Axis Labels:**
- Font: 8px, Weight: 700, Color: #09101D

#### Chart Colors Palette

```css
/* Основные цвета графиков */
--chart-grid-light: #A4ABB3;    /* Вертикальные линии, бары */
--chart-grid-dark: #747B84;     /* Горизонтальные линии, оси */
--chart-text: #09101D;          /* Все подписи */
```

---

### 9. Avatars (из Flutter кода)

#### Sizes

- **Extra Small**: 32px × 32px (в группах)
- **Small**: 40px × 40px (в группах)
- **Medium**: 48px × 48px (в группах)
- **Large**: 56px × 56px (основной)
- **Extra Large**: 60px × 60px (иконки)

#### Styles

- **Border Radius**: Circular (40px для 48px avatar, 30px для 56px avatar, 100px для иконок)
- **Border Width**:
  - Solo avatar: 2px solid (accent color, например #FC466B)
  - Group avatars: 4px solid white
- **Placeholder**: Background: #D9DDE2
- **Image Fit**: Cover

#### Avatar с Live Badge (из Flutter кода)

- **Avatar Size**: 56px × 56px
- **Border**: 2px solid #FC466B (Instagram gradient border)
- **Inner Avatar**: 48px × 48px (4px отступ от внешней границы)
- **Live Badge**:
  - Position: Bottom of avatar container
  - Size: 28px × 14px
  - Padding: 4px horizontal, 2px vertical
  - Border: 1px solid white
  - Border Radius: 12px
  - Background: linear-gradient(90deg, #833AB4, #FD1D1D, #FCB045)
  - Text: "Live", 10px, weight: 600, color: white

#### Avatar Groups (из Flutter кода)

- **Layout**: Horizontal row с gap: 10px
- **Overlap**: None (используется gap вместо overlap)
- **Individual Avatar**:
  - Container: 40px × 40px
  - Border: 4px solid white
  - Border Radius: 30px (circular)
  - Inner Image: 32px × 32px
  - Background: #D9DDE2 (placeholder)
- **Group Spacing**: 6px между border и следующим аватаром
- **Max Visible**: Обычно 4-5 аватаров, затем "+N" badge

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

### 17. iOS Keyboard (из Flutter кода)

#### Keyboard Container
- **Width**: 375px (full width)
- **Height**: 290px (клавиатура + home indicator)
- **Background**: rgba(209, 213, 219, 0.94) - #EFD1D5DB
- **Clip**: antiAlias

#### Keyboard Layout
- **Keys Area**: 214px height
- **Bottom Bar**: 76px height (включает home indicator)

#### Key Specifications

**Letter Keys:**
- **Size**: 31.5px × 42px
- **Border Radius**: 5px
- **Background**: #FFFFFF
- **Shadow**: 0 1px 0 0 rgba(0, 0, 0, 0.35)
- **Font**: 23px, weight: 400, color: #000000
- **Text Align**: Center

**Space Bar:**
- **Size**: 182.49px × 42px
- **Border Radius**: 5px
- **Background**: #FDFDFD
- **Shadow**: 0 1px 0 0 rgba(4, 4, 15, 0.36)
- **Text**: "space", 16px, weight: 400, letter-spacing: -0.32px

**Return Key:**
- **Size**: 87.73px × 42px
- **Border Radius**: 5px
- **Background**: #ADB3BC
- **Shadow**: 0 1px 0 0 #898A8D
- **Text**: "return", 16px, weight: 400, letter-spacing: -0.32px, color: #000000

**123 Key:**
- **Text**: "123", 16px, weight: 400, letter-spacing: -0.32px
- **Background**: Same as Return key

**Symbol Keys:**
- **Font**: 27px (для символов типа 􀊱, 􀆪)
- **Color**: rgba(0, 0, 0, 0.55)
- **Usage**: Keyboard switchers, emoji button

#### Keyboard Row Spacing
- **Top Row** (QWERTYUIOP): 9px from top
- **Middle Row** (ASDFGHJKL): 63px from top
- **Bottom Row** (ZXCVBNM): 117px from top
- **Function Row** (Space, Return, etc.): 165px from top

---

### 18. Home Indicator (из Flutter кода)

#### Specifications
- **Width**: 134px
- **Height**: 5px
- **Border Radius**: 100px (pill shape)
- **Background**: #09101D (черный)
- **Border**: 1px solid (может быть #FFFFFF или #09101D в зависимости от варианта)
- **Position**: Bottom center, 21px from bottom
- **Container Height**: 34px

#### Alternative Variant
- **Border Color**: Может быть white для контраста с темным фоном

---

### 19. Progress Bars & Steppers (из Flutter кода)

#### Linear Progress Bar

**Container:**
- **Width**: 375px (full width на mobile)
- **Padding**: 16px horizontal
- **Background**: Transparent

**Progress Bar Specifications:**
- **Height**: 3px
- **Border Radius**: 10px (pill shape)
- **Spacing между сегментами**: 5px
- **Colors**:
  - Active (completed): #0B24FB
  - In-progress / Partial: rgba(11, 36, 251, 0.30) - #4C0B24FB
  - Inactive (not started): rgba(9, 16, 29, 0.10) - #1909101D

**Варианты по количеству шагов:**
- **2 Steps**: Два сегмента 50/50
- **3 Steps**: Три сегмента 33/33/33
- **4 Steps**: Четыре сегмента 25/25/25/25
- **5 Steps**: Пять сегментов 20/20/20/20/20
- **6 Steps**: Шесть сегментов по ~16.67%

**Layout:**
```
[Segment 1] 5px [Segment 2] 5px [Segment 3] 5px [Segment 4]
```

#### Stepper (Horizontal)

**Container:**
- **Width**: 375px (mobile full width)
- **Padding**: 32px left/right
- **Background**: Transparent
- **Spacing между шагами**: Auto-distribute (Expanded widgets)

**Step Indicator:**
- **Outer Circle**: 18px × 18px
- **Inner Dot**: 14px × 14px (fill для completed)
- **Border**: 2px (для current step)
- **Colors**:
  - **Completed**: #4141E6 solid fill
  - **Current**: #4141E6 outer ring (2px) + white center + #4141E6 inner dot (4px)
  - **Inactive**: #EAEEF2 fill
- **Spacing**: 3px между элементами

**Connector Line:**
- **Height**: 4px
- **Width**: Expanded (заполняет пространство между шагами)
- **Border Radius**: 10px (pill)
- **Colors**:
  - Completed: #4141E6
  - Incomplete: #EAEEF2

**Step Label:**
- **Text**: "Step name"
- **Font Size**: 10px
- **Font Weight**: 600 (semibold)
- **Color**: #09101D
- **Text Align**: Center
- **Margin Top**: 8px (от индикатора)

**Stepper Layout:**
```
(●)━━━━━(●)━━━━━(○)━━━━━(○)
Step 1  Step 2  Step 3  Step 4
```

#### Circular Progress

**Specifications:**
- **Size**: 64px × 64px
- **Stroke Width**: 5px
- **Border Radius**: Full circle (100px)
- **Colors**:
  - Active (progress): #4141E6
  - Track (background): #F4F6F9
- **Center Content**: Optional text, percentage, or icon

**With Labels:**
- **Title**:
  - Font: 15px
  - Weight: 600
  - Color: #09101D
  - Margin Top: 8px
- **Subtitle**:
  - Font: 14px
  - Weight: 400
  - Color: #414249
  - Margin Top: 4px

#### Progress Typography

**Labels:**
- Font: 10px, Weight: 600, Color: #09101D

**Title (для circular):**
- Font: 15px, Weight: 600, Color: #09101D

**Subtitle:**
- Font: 14px, Weight: 400, Color: #414249

#### Использование

```css
/* Linear Progress Bar */
.progress-bar {
  width: 100%;
  max-width: 343px; /* 375px - 32px padding */
  height: 3px;
  display: flex;
  gap: 5px;
}

.progress-bar__segment {
  flex: 1;
  height: 3px;
  border-radius: 10px;
}

.progress-bar__segment--active {
  background: #0B24FB;
}

.progress-bar__segment--partial {
  background: rgba(11, 36, 251, 0.30);
}

.progress-bar__segment--inactive {
  background: rgba(9, 16, 29, 0.10);
}

/* Stepper */
.stepper {
  display: flex;
  align-items: center;
  padding: 0 32px;
  gap: auto;
}

.stepper__step {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 3px;
}

.stepper__indicator {
  width: 18px;
  height: 18px;
  border-radius: 100px;
}

.stepper__indicator--completed {
  background: #4141E6;
}

.stepper__indicator--current {
  border: 2px solid #4141E6;
  background: white;
  position: relative;
}

.stepper__indicator--current::after {
  content: '';
  width: 14px;
  height: 14px;
  background: #4141E6;
  border-radius: 100px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.stepper__indicator--inactive {
  background: #EAEEF2;
}

.stepper__connector {
  flex: 1;
  height: 4px;
  border-radius: 10px;
}

.stepper__connector--completed {
  background: #4141E6;
}

.stepper__connector--incomplete {
  background: #EAEEF2;
}

.stepper__label {
  font-size: 10px;
  font-weight: 600;
  color: #09101D;
  margin-top: 8px;
}

/* Circular Progress */
.circular-progress {
  width: 64px;
  height: 64px;
  position: relative;
}

.circular-progress__track {
  stroke: #F4F6F9;
  stroke-width: 5px;
}

.circular-progress__fill {
  stroke: #4141E6;
  stroke-width: 5px;
  stroke-linecap: round;
}
```

---

### 20. Badges (из Flutter кода)

#### Live Badge (Instagram-style)
- **Size**: 28px × 14px
- **Padding**: 4px horizontal, 2px vertical
- **Border Radius**: 12px
- **Border**: 1px solid white
- **Background**: linear-gradient(90deg, #833AB4 0%, #FD1D1D 50%, #FCB045 100%)
- **Typography**:
  - Text: "Live"
  - Font Size: 10px
  - Font Weight: 600
  - Color: white
  - Line Height: 140%
- **Position**: Usually bottom of avatar or top-right of content

#### Level Badge (из Buttons Light)

**Specifications:**
- **Height**: 24px
- **Padding**: left 5px, right 10px
- **Border Radius**: 10px
- **Background**: white
- **Icon**: 24px × 24px (6px padding inside)
- **Typography**:
  - Text: "Beginner level", "Intermediate", "Advanced"
  - Font Size: 11px
  - Font Weight: 600
  - Color: #23262B
  - Line Height: 140%
- **Spacing**: 8px между icon и text
- **Position**: Bottom right на preview изображении

**Usage:**
- Content cards (courses, tutorials, articles)
- Skill level indicators
- Difficulty badges

**CSS Example:**

```css
.level-badge {
  height: 24px;
  padding-left: 5px;
  padding-right: 10px;
  border-radius: 10px;
  background: white;
  display: inline-flex;
  align-items: center;
  gap: 0;
}

.level-badge__icon {
  width: 24px;
  height: 24px;
  padding: 6px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.level-badge__text {
  font-size: 11px;
  font-weight: 600;
  color: #23262B;
  line-height: 1.4;
  white-space: nowrap;
}
```

#### Price Badge (из Buttons Light)

**Specifications:**
- **Height**: 20px
- **Padding**: 10px horizontal, 5px vertical
- **Border Radius**: 12px
- **Background**: white
- **Typography**:
  - Text: "Save 23%", "50% OFF", "-20%"
  - Font Size: 11px
  - Font Weight: 600
  - Color: #FF512F (gradient start color)
  - Line Height: 140%
- **Position**: Inside gradient button, right side

**Usage:**
- Pricing buttons
- Discount indicators
- Promotional badges

**CSS Example:**

```css
.price-badge {
  height: 20px;
  padding: 5px 10px;
  border-radius: 12px;
  background: white;
  display: inline-flex;
  align-items: center;
  justify-content: center;
}

.price-badge__text {
  font-size: 11px;
  font-weight: 600;
  color: #FF512F;
  line-height: 1.4;
  white-space: nowrap;
}

/* Inside gradient button */
.gradient-button .price-badge {
  margin-left: 8px;
}
```

---

### 21. Screen Container (из Flutter кода)

#### Mobile Screen Container
- **Width**: 375px (iPhone-like width)
- **Height**: 812px (iPhone X-like height)
- **Background**: rgba(217, 221, 226, 0.25) с opacity 0.25 - #D9DDE2
- **Border Radius**: 40px (при клипе на экран)
- **Clip Behavior**: antiAlias

#### Status Bar Area
- **Height**: 44px
- **Position**: Top of screen
- **Content**: Time, signal indicators (обычно оставляется пустым в дизайне)

#### Safe Area
- **Top**: 44px (status bar)
- **Bottom**: 34px (home indicator area)
- **Sides**: 8px padding (для карточек)

---

### 22. Progress Dots Indicator (из Flutter кода)

#### Specifications

**Container:**
- **Padding**: 20px vertical
- **Alignment**: Center
- **Spacing**: 6px между точками

**Dot:**
- **Size**: 20px width × 4px height (pill shape)
- **Border Radius**: 5px
- **Colors**:
  - Active: #09101D (черный)
  - Inactive: rgba(9, 16, 29, 0.10) - #1909101D

**Layout:**
```
● ○ ○ ○ ○  (5 dots)
```

**Usage:**
- Onboarding screens
- Multi-step forms
- Image carousels/sliders

#### CSS Example

```css
.progress-dots {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 6px;
  padding: 20px 0;
}

.progress-dots__dot {
  width: 20px;
  height: 4px;
  border-radius: 5px;
  transition: background-color 0.3s ease;
}

.progress-dots__dot--active {
  background: #09101D;
}

.progress-dots__dot--inactive {
  background: rgba(9, 16, 29, 0.10);
}
```

---

### 23. Onboarding / Start Screens (из Flutter кода)

#### Screen Container

**Specifications:**
- **Width**: 375px (mobile full width)
- **Background**: white
- **Border Radius**: 30px
- **Clip**: antiAlias

**Варианты высот:**
- Full onboarding: 369px
- Compact (social only): 265px

#### Layout Structure

**1. Gradient Overlay (Optional)**
```css
background: linear-gradient(180deg, rgba(255,255,255,0) 0%, #FFFFFF 100%);
padding-top: 50px;
```

**2. Content Section**
- **Padding**: 20px top, 16px left/right, 10px bottom

**Title:**
- Font Size: 32px
- Font Weight: 700 (bold)
- Line Height: 140%
- Color: #09101D
- Text Align: Center
- Max Width: 343px

**Description:**
- Font Size: 14px
- Font Weight: 400
- Line Height: 140%
- Color: #09101D
- Text Align: Center
- Max Width: 343px

**Spacing:** 10px between title and description

**3. Progress Dots**
- Padding: 20px vertical
- See Progress Dots Indicator above

**4. Actions Section**

**Primary CTA (Large):**
- Button: 52px height, brand orange (#FF6937) or red (#E24949)
- Full width (with 16px side padding)
- Spacing: 10px between buttons

**Secondary Link:**
- Height: 44px
- Text with link style
- Regular: #09101D, 12px, weight 500
- Link: #FF6937 (brand orange), 12px, weight 500

**Social Auth Row:**
- 3 equal buttons (Google, Facebook, Apple)
- Gap: 10px
- Padding: 16px horizontal, 10px vertical

**Text Link:**
- Text: "Sign up later"
- Font: 14px, weight 600, #09101D
- No background
- Padding: 16px horizontal

**5. Home Indicator**
- Width: 134px
- Height: 5px
- Border Radius: 100px (pill)
- Background: #09101D
- Position: Bottom center, 21px from bottom

#### Usage Example

```css
/* Onboarding Screen Container */
.onboarding-screen {
  width: 375px;
  background: white;
  border-radius: 30px;
  overflow: hidden;
  position: relative;
}

/* Gradient Overlay */
.onboarding-screen__overlay {
  background: linear-gradient(180deg, rgba(255,255,255,0) 0%, #FFFFFF 100%);
  padding-top: 50px;
}

/* Content */
.onboarding-screen__content {
  padding: 20px 16px 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
}

.onboarding-screen__title {
  font-size: 32px;
  font-weight: 700;
  line-height: 1.4;
  color: #09101D;
  text-align: center;
  max-width: 343px;
}

.onboarding-screen__description {
  font-size: 14px;
  font-weight: 400;
  line-height: 1.4;
  color: #09101D;
  text-align: center;
  max-width: 343px;
}

/* Actions */
.onboarding-screen__actions {
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 10px;
  padding: 10px 0;
}

/* Social Auth Row */
.social-auth-row {
  display: flex;
  gap: 10px;
  padding: 10px 16px;
}

.social-auth-row__button {
  flex: 1;
  height: 44px;
  border-radius: 4px;
  display: flex;
  align-items: center;
  justify-content: center;
}
```

#### Flexible Blocks

**Гибкие элементы для адаптации:**

1. **Количество действий:** Легко добавить/убрать кнопки в секции actions
2. **Social buttons:** Можно добавить больше провайдеров (GitHub, Twitter и т.д.)
3. **Progress dots:** Количество точек адаптируется под количество шагов
4. **Gradient overlay:** Опциональный, можно отключить
5. **Spacing:** Все отступы вынесены в переменные, легко настраиваются

---

### 24. Tooltips (из Flutter кода)

#### Tooltip Specifications

**Container:**
- **Padding**: 16px horizontal, 12px vertical
- **Border Radius**: 8px
- **Max Width**: Auto (адаптируется к контенту)

**Typography:**
- **Font Size**: 13px
- **Font Weight**: 400 (regular)
- **Line Height**: 140% (1.40)
- **Font Family**: Archivo

**Arrow/Pointer:**
- **Size**: 4px height (треугольник)
- **Spacing от tooltip**: 10px
- **Position**: Top, Bottom, Left, Right, Center (8 направлений)

#### Tooltip Variants

**1. Dark Tooltip (Темная)**

```css
.tooltip--dark {
  background: #09101D;
  color: white;
  padding: 12px 16px;
  border-radius: 8px;
  font-size: 13px;
  font-weight: 400;
  line-height: 1.4;
  box-shadow: none;
}
```

**Спецификации:**
- Background: #09101D (черный)
- Text Color: white
- Padding: 12px vertical, 16px horizontal
- Border Radius: 8px
- Shadow: None

**2. Light Tooltip (Светлая)**

```css
.tooltip--light {
  background: white;
  color: #09101D;
  padding: 12px 16px;
  border-radius: 8px;
  font-size: 13px;
  font-weight: 400;
  line-height: 1.4;
  box-shadow: 0 6px 15px 0 rgba(0, 0, 0, 0.10);
}
```

**Спецификации:**
- Background: white
- Text Color: #09101D (черный)
- Padding: 12px vertical, 16px horizontal
- Border Radius: 8px
- Shadow: 0 6px 15px 0 rgba(0, 0, 0, 0.10)

#### Tooltip Positioning

**Arrow Positions (8 направлений):**

1. **Top Left** - стрелка слева сверху
2. **Top Center** - стрелка по центру сверху
3. **Top Right** - стрелка справа сверху
4. **Right Top** - стрелка справа сверху (боковая)
5. **Right Center** - стрелка справа по центру
6. **Right Bottom** - стрелка справа снизу (боковая)
7. **Bottom Left** - стрелка слева снизу
8. **Bottom Center** - стрелка по центру снизу
9. **Bottom Right** - стрелка справа снизу
10. **Left Top** - стрелка слева сверху (боковая)
11. **Left Center** - стрелка слева по центру
12. **Left Bottom** - стрелка слева снизу (боковая)

**Spacing:**
- От элемента до tooltip: 10px
- Arrow height: 4px
- Arrow padding: 16px от края (для left/right aligned)

#### Tooltip Usage Example

```css
/* Base Tooltip */
.tooltip {
  position: absolute;
  padding: 12px 16px;
  border-radius: 8px;
  font-size: 13px;
  font-weight: 400;
  line-height: 1.4;
  font-family: 'Archivo', sans-serif;
  white-space: nowrap;
  z-index: 1000;
}

/* Dark variant */
.tooltip--dark {
  background: #09101D;
  color: white;
}

/* Light variant */
.tooltip--light {
  background: white;
  color: #09101D;
  box-shadow: 0 6px 15px 0 rgba(0, 0, 0, 0.10);
}

/* Arrow base */
.tooltip::before {
  content: '';
  position: absolute;
  width: 0;
  height: 0;
  border-style: solid;
}

/* Top arrow (pointing down) */
.tooltip--arrow-top::before {
  bottom: -4px;
  border-width: 4px 4px 0 4px;
}

.tooltip--dark.tooltip--arrow-top::before {
  border-color: #09101D transparent transparent transparent;
}

.tooltip--light.tooltip--arrow-top::before {
  border-color: white transparent transparent transparent;
}

/* Bottom arrow (pointing up) */
.tooltip--arrow-bottom::before {
  top: -4px;
  border-width: 0 4px 4px 4px;
}

.tooltip--dark.tooltip--arrow-bottom::before {
  border-color: transparent transparent #09101D transparent;
}

.tooltip--light.tooltip--arrow-bottom::before {
  border-color: transparent transparent white transparent;
}

/* Left arrow (pointing right) */
.tooltip--arrow-left::before {
  right: -4px;
  border-width: 4px 0 4px 4px;
}

.tooltip--dark.tooltip--arrow-left::before {
  border-color: transparent transparent transparent #09101D;
}

.tooltip--light.tooltip--arrow-left::before {
  border-color: transparent transparent transparent white;
}

/* Right arrow (pointing left) */
.tooltip--arrow-right::before {
  left: -4px;
  border-width: 4px 4px 4px 0;
}

.tooltip--dark.tooltip--arrow-right::before {
  border-color: transparent #09101D transparent transparent;
}

.tooltip--light.tooltip--arrow-right::before {
  border-color: transparent white transparent transparent;
}

/* Arrow alignment */
.tooltip--arrow-left-align::before {
  left: 16px;
}

.tooltip--arrow-center-align::before {
  left: 50%;
  transform: translateX(-50%);
}

.tooltip--arrow-right-align::before {
  right: 16px;
}

.tooltip--arrow-top-align::before {
  top: 18px;
}

.tooltip--arrow-middle-align::before {
  top: 50%;
  transform: translateY(-50%);
}

.tooltip--arrow-bottom-align::before {
  bottom: 18px;
}
```

#### Tooltip Behavior

**Show/Hide:**
- Trigger: Hover (desktop), Tap (mobile)
- Delay: 200ms перед показом
- Duration: Visible пока hover активен
- Animation: Fade in/out (150ms)

**Accessibility:**
- Role: tooltip
- Aria-describedby: связь с элементом
- Keyboard: Показывается при фокусе
- Screen readers: Читается автоматически

**Best Practices:**
- Текст: Краткий и информативный (1-2 строки)
- Размещение: Не перекрывает важный контент
- Контраст: Достаточный для читабельности
- Responsive: Адаптируется к границам экрана

---

### 25. Content Cards (из Buttons Light)

#### Course/Content Card with Pricing

**Card Container:**
- **Width**: 375px (mobile full width)
- **Height**: 430px (flexible, auto-adjust)
- **Border Radius**: 30px
- **Background**: white
- **Clip**: antiAlias
- **Shadow**: Optional (0 2px 8px rgba(0,0,0,0.08))

**Layout Structure:**

**1. Image Section**
- **Container**: 375px × 231px (padding 16px top/left/right)
- **Image**:
  - Width: 343px
  - Height: 211px
  - Border Radius: 15px
  - Background: #F4F6F9
  - Fit: cover

**Overlays на изображении:**

**Level Badge (bottom-right):**
- Position: Bottom-right с padding 10px
- See Level Badge specs above

**Favorite Button (top-right):**
- Size: 30px × 30px
- Padding: 8px (icon 14px)
- Border Radius: 100px (circle)
- Background: white
- Position: Top-right с padding 10px

**2. Content Section**
- **Padding**: 10px vertical, 16px horizontal
- **Spacing**: 5px между элементами

**Title:**
- Font Size: 16px
- Font Weight: 700 (bold)
- Line Height: 140%
- Color: #09101D
- Max Width: 343px

**Subtitle/Location:**
- Font Size: 15px
- Font Weight: 400
- Line Height: 140%
- Color: #D9DDE2
- Max Width: 343px

**Author Section:**
- **Avatar**: 32px × 32px (в контейнере 40px с offset 4px)
- **Border Radius**: 10px
- **Spacing**: 6px между avatar и text
- **Name**:
  - Font: 13px, weight 400
  - Color: #4141E6 (link style)
- **Role**:
  - Font: 12px, weight 400
  - Color: #373940

**3. Gradient Overlay**
- **Position**: Starts at 254px from top
- **Padding Top**: 30px
- **Gradient**: linear-gradient(180deg, rgba(255,255,255,0) 0%, #FFFFFF 100%)
- **Purpose**: Smooth transition для pricing секции

**4. Pricing/Actions Section**
- **Padding**: 5px vertical per button container
- **Container padding**: 16px horizontal
- **Spacing**: 10px между кнопками

**Primary Pricing (Gradient Button):**
- See Gradient Button specs
- Text: "\$ 86.99/Year" + "Save 23%" badge
- Full width with horizontal padding

**Secondary Pricing (Outline Button):**
- See Outline Button specs
- Text: "\$ 9.49/Month"
- Full width with horizontal padding

**5. Home Indicator**
- Width: 134px
- Height: 5px
- Border Radius: 100px
- Background: #09101D
- Position: Bottom center, 21px from bottom

#### Flexible Elements

**Adaptations:**
1. **Image**: Можно заменить на video preview или carousel
2. **Badges**: Добавить/убрать level badge, favorite
3. **Content**: Title и subtitle опциональны, можно варьировать длину
4. **Author**: Опциональная секция, можно показать несколько авторов
5. **Pricing**: 1-2 опции, можно добавить больше вариантов подписки
6. **Actions**: Легко добавить дополнительные кнопки (Free trial, Learn more)

#### CSS Example

```css
/* Content Card Container */
.content-card {
  width: 375px;
  min-height: 430px;
  border-radius: 30px;
  background: white;
  overflow: hidden;
  position: relative;
}

/* Image Section */
.content-card__image-container {
  width: 100%;
  padding: 20px 16px 0;
}

.content-card__image {
  width: 343px;
  height: 211px;
  border-radius: 15px;
  background: #F4F6F9;
  object-fit: cover;
  position: relative;
}

/* Overlays */
.content-card__favorite {
  position: absolute;
  top: 10px;
  right: 10px;
  width: 30px;
  height: 30px;
  padding: 8px;
  border-radius: 100px;
  background: white;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
}

.content-card__level-badge {
  position: absolute;
  bottom: 10px;
  right: 10px;
}

/* Content */
.content-card__content {
  padding: 10px 16px;
  display: flex;
  flex-direction: column;
  gap: 5px;
}

.content-card__title {
  font-size: 16px;
  font-weight: 700;
  line-height: 1.4;
  color: #09101D;
}

.content-card__subtitle {
  font-size: 15px;
  font-weight: 400;
  line-height: 1.4;
  color: #D9DDE2;
}

/* Author */
.content-card__author {
  display: flex;
  align-items: center;
  gap: 6px;
}

.content-card__avatar {
  width: 32px;
  height: 32px;
  border-radius: 10px;
  object-fit: cover;
}

.content-card__author-name {
  font-size: 13px;
  font-weight: 400;
  color: #4141E6;
}

.content-card__author-role {
  font-size: 12px;
  font-weight: 400;
  color: #373940;
}

/* Gradient Overlay */
.content-card__overlay {
  position: absolute;
  left: 0;
  top: 254px;
  width: 100%;
  padding-top: 30px;
  background: linear-gradient(180deg, rgba(255,255,255,0) 0%, #FFFFFF 100%);
}

/* Pricing Actions */
.content-card__actions {
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 10px;
  padding: 0 16px;
}

/* Home Indicator */
.content-card__home-indicator {
  width: 134px;
  height: 5px;
  border-radius: 100px;
  background: #09101D;
  margin: 0 auto;
  margin-top: 34px;
  margin-bottom: 21px;
}
```

#### Usage Examples

**Course Card:**
```html
<div class="content-card">
  <div class="content-card__image-container">
    <img src="course.jpg" class="content-card__image" />
    <button class="content-card__favorite">❤</button>
    <div class="content-card__level-badge level-badge">
      <span class="level-badge__text">Beginner level</span>
    </div>
  </div>

  <div class="content-card__content">
    <h3 class="content-card__title">Healthy food course & practice</h3>
    <p class="content-card__subtitle">New York, 214 W 29th St</p>

    <div class="content-card__author">
      <img src="avatar.jpg" class="content-card__avatar" />
      <div>
        <div class="content-card__author-name">Nicole Dowson</div>
        <div class="content-card__author-role">Kitchen Crew</div>
      </div>
    </div>
  </div>

  <div class="content-card__overlay">
    <div class="content-card__actions">
      <button class="gradient-button">
        $ 86.99/Year
        <span class="price-badge">Save 23%</span>
      </button>
      <button class="outline-button">$ 9.49/Month</button>
    </div>

    <div class="content-card__home-indicator"></div>
  </div>
</div>
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

## Градиенты (из Flutter кода)

### Instagram-style Gradient

**Использование**: Live badge, accent borders, premium features

```css
background: linear-gradient(90deg, #833AB4 0%, #FD1D1D 50%, #FCB045 100%);
```

**Цвета:**
- Start: #833AB4 (фиолетовый)
- Middle: #FD1D1D (красный)
- End: #FCB045 (оранжевый)

**Применение:**
- Live badge на аватарах
- Premium borders
- Accent highlights
- Feature indicators

### Gradient Direction

**Horizontal (90deg):**
- Begin: Alignment(0.00, 0.50)
- End: Alignment(1.00, 0.50)
- Используется для badge и горизонтальных элементов

**Vertical (180deg):**
- Не используется в текущем дизайне

**Diagonal (135deg):**
- Альтернативный вариант для больших площадей

### Flutter Implementation

```dart
decoration: BoxDecoration(
  gradient: LinearGradient(
    begin: Alignment(0.00, 0.50),
    end: Alignment(1.00, 0.50),
    colors: [
      Color(0xFF833AB4),
      Color(0xFFFD1D1D),
      Color(0xFFFCB045),
    ],
  ),
  borderRadius: BorderRadius.circular(12),
  border: Border.all(color: Colors.white, width: 1),
),
```

### CSS Implementation

```css
.gradient-instagram {
  background: linear-gradient(90deg, #833AB4 0%, #FD1D1D 50%, #FCB045 100%);
}

.gradient-border {
  border: 2px solid;
  border-image: linear-gradient(90deg, #833AB4, #FD1D1D, #FCB045) 1;
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

**Текущая версия**: v5.8.0

### Changelog

#### v5.8.0 (2025-11-19)
- **Content Cards**: Добавлена секция с карточками контента и pricing
  - Course/Content Card: 375px × 430px, 30px border-radius
  - Image section: 343px × 211px, level badge, favorite button overlays
  - Content: Title (16px bold), Subtitle (15px), Author (avatar + name/role)
  - Gradient overlay: Плавный переход от контента к pricing секции
  - Pricing actions: Gradient и Outline кнопки
  - Home indicator: 134px × 5px pill (bottom center)
  - Flexible elements: Легко адаптировать image, badges, content, pricing
- **Gradient Buttons**: Новый вариант кнопок для pricing/premium
  - Height: 44px, Border-radius: 30px (большой!)
  - Gradient: linear-gradient(90deg, #FF512F 0%, #DD2476 100%)
  - Price Badge: 20px height, 12px radius, white background
  - Text: 14px weight 600, с опциональным badge
  - Usage: Subscription, premium CTA, pricing options
- **Outline Buttons**: Цветной outline вариант
  - Border: 1px solid #FE5032
  - Border-radius: 30px
  - Text: 14px weight 600, color #E24949
  - Usage: Secondary pricing, alternative CTA
- **Level Badge**: Новый компонент для difficulty/skill indicators
  - Height: 24px, padding 5px/10px, radius 10px
  - Icon: 24px с 6px padding
  - Text: 11px weight 600, color #23262B
  - Usage: Course cards, skill levels, difficulty badges
- **Price Badge**: Компонент для discount индикаторов
  - Height: 20px, padding 5px/10px, radius 12px
  - Text: 11px weight 600, color #FF512F
  - Position: Inside gradient buttons
  - Usage: "Save 23%", "50% OFF", promotional badges
- **Цвета**: Добавлены градиенты для pricing кнопок
  - Gradient start: #FF512F (оранжево-красный)
  - Gradient end: #DD2476 (розовый)
  - Outline border: #FE5032 (оранжевый)
  - Text gray: #373940 (для author role)
- **Компоненты**: CSS примеры для всех новых элементов
  - Content card layout с flexible sections
  - Gradient и Outline кнопки
  - Level и Price badges

#### v5.7.0 (2025-11-19)
- **Onboarding/Start Screens**: Добавлена секция с готовыми блоками
  - Screen container: 375px width, 30px border-radius, white background
  - Gradient overlay: от прозрачного к белому (опциональный)
  - Content section: Title (32px, bold), Description (14px)
  - Actions: Primary CTA, Social auth, Text links
  - Home indicator: 134px × 5px pill
  - Flexible blocks: Легко адаптируемые секции (добавить/убрать кнопки, провайдеры)
- **Progress Dots Indicator**: Новый компонент
  - Dot: 20px width × 4px height, 5px border-radius
  - Active: #09101D, Inactive: rgba(9, 16, 29, 0.10)
  - Spacing: 6px, padding: 20px vertical
  - Usage: Onboarding, multi-step forms, carousels
- **Brand Colors**: Добавлены новые цвета
  - Brand orange: #FF6937 (primary CTA)
  - Brand red: #E24949 (secondary CTA)
  - Social Facebook: #4C69AB
  - Social Apple: #23262B
- **Buttons**: Обновлена секция с новыми вариантами
  - Large button: 52px height (вместо 44px) для onboarding/CTA
  - Brand Orange Button: #FF6937, 52px, "Sign up"
  - Brand Red Button: #E24949, 52px, with icon
  - Social Auth Buttons: Google, Facebook, Apple (44px, 4px radius, equal width)
  - Button sizes: Standard (44px), Large (52px), Social (44px)
- **Компоненты**: Добавлены CSS примеры для всех новых элементов
  - Onboarding screen layout
  - Progress dots animation
  - Social auth row
  - Flexible blocks примеры

#### v5.6.0 (2025-11-19)
- **Tooltips (Всплывающие подсказки)**: Добавлен компонент Tooltips
  - 2 варианта: Dark (черная) и Light (светлая с тенью)
  - Container: 8px border-radius, 16px/12px padding
  - Typography: 13px, weight 400, line-height 140%
  - Arrow/Pointer: 4px height, 10px spacing, 12 направлений позиционирования
  - Dark tooltip: #09101D background, white text, no shadow
  - Light tooltip: white background, #09101D text, shadow 0 6px 15px rgba(0,0,0,0.10)
- **Shadows**: Добавлена тень для tooltips
  - Tooltip shadow: 0 6px 15px 0 rgba(0, 0, 0, 0.10)
- **Компоненты**: Добавлены CSS примеры для tooltips
  - Arrow positioning (top, bottom, left, right)
  - Arrow alignment (left, center, right, top, middle, bottom)
  - Accessibility и behavior спецификации

#### v5.5.0 (2025-11-19)
- **Input Fields (Текстовые поля)**: Полностью переработана секция Inputs
  - 9 состояний: Enabled, Focus, Pressed, Active-Typing, Complete, Incomplete, Positive, Negative, Disabled
  - Container: 375px width, 16px horizontal padding, 8px spacing
  - Input: 36px height, 15px border-radius, 16px/20px padding
  - Label: 14px (weight 600), Helper: 14px (weight 400)
  - Placeholder: 14px (weight 400), color #747B84
  - Action icons: 20px × 20px (clear, check, error)
- **Цвета**: Добавлены цвета для input полей
  - Input backgrounds: #F4F6F9 (normal), #EAEEF2 (pressed/disabled)
  - Success: rgba(17, 187, 141, 0.05) background, #11BB8D border
  - Error: rgba(218, 20, 20, 0.05) background, #DA1414 border
  - Placeholder: #747B84
  - Border focus: #09101D
  - Error text: #E24949
  - Disabled text: #D9DDE2
- **Компоненты**: Добавлены CSS примеры для всех состояний inputs
  - Base input styles
  - State modifiers (enabled, focus, error, success, disabled)
  - Helper text variations

#### v5.4.0 (2025-11-19)
- **Progress Bars & Steppers**: Добавлена полная спецификация прогресс-баров и степперов
  - Linear Progress Bar: 3px height, 10px border-radius, 5px gaps между сегментами
  - Stepper (Horizontal): 18px outer circle, 14px inner dot, 4px connector lines
  - Circular Progress: 64px × 64px, 5px stroke width
  - Варианты: 2-6 шагов для linear progress
  - Typography: 10px labels (weight 600), 15px titles, 14px subtitles
- **Цвета**: Добавлены цвета для прогресс-баров и степперов
  - Progress blue: #0B24FB (активный прогресс)
  - Progress inactive: rgba(9, 16, 29, 0.10)
  - Progress partial: rgba(11, 36, 251, 0.30)
  - Stepper active: #4141E6
  - Stepper inactive: #EAEEF2
- **Компоненты**: Добавлен раздел "Progress Bars & Steppers" с CSS примерами
  - Linear progress с сегментами
  - Horizontal stepper с индикаторами и коннекторами
  - Circular progress с метками

#### v5.3.0 (2025-11-19)
- **Dividers (Разделители)**: Добавлена полная спецификация разделителей
  - Thin Divider: 1px height, #EAEEF2 color
  - Thick Divider: 10px height, #F4F6F9 color
  - Indent levels: 0px, 16px, 36px, 52px, 74px, 84px
  - Container: 475px width, 50px padding, 1px border #7B61FF
- **Цвета**: Добавлены новые цвета
  - Accent purple: #7B61FF (фиолетовый для границ)
  - Divider light: #EAEEF2
  - Divider thick: #F4F6F9
  - Border purple: #7B61FF
- **Типографика**: Расширены размеры шрифтов
  - Font size 72px для крупных заголовков
  - Font weight 800 (extrabold)
  - Line height 0.70 (70%)
  - Использование: заголовки секций "Divider"

#### v5.2.0 (2025-11-19)
- **Charts (Графики)**: Добавлена полная спецификация графиков
  - Quarterly Bar Chart: 375px width, 185px height, вертикальные бары
  - Chart Legend: 8px labels (bold), горизонтальные линии
  - Grid Lines: #A4ABB3 (light), #747B84 (dark)
  - Chart Typography: 8px (legends), 10px (quarters)
  - Chart Colors: #A4ABB3, #747B84, #09101D
- **Цвета**: Добавлены цвета для графиков
  - Chart grid light: #A4ABB3
  - Chart grid dark: #747B84
  - Chart text: #09101D
- **Типографика**: Добавлен размер 8px для лейблов графиков
  - Font size 8px для легенды
  - Font size 10px для меток кварталов
  - Text styles для графиков

#### v5.1.0 (2025-11-19)
- **Цветовая палитра**: Добавлены реальные цвета из Flutter кода
  - Background colors: #F4F6F9, #D9DDE2, #EFD1D5DB, #FDFDFD
  - Text colors: #09101D, #23262B, #2A2B2F
  - Accent colors: #4141E6, #11BB8D, #FC466B
  - Gradient colors: Instagram-style (#833AB4, #FD1D1D, #FCB045)
  - Payment system colors: Mastercard (#DA1414, #F79E1C)
- **Типографика**: Расширены размеры шрифтов
  - Добавлены: 23px (клавиатура), 27px (иконки)
  - Letter spacing: -0.32px для клавиатуры
  - Новые text styles из Flutter кода
- **Spacing & Layout**: Обновлены border radius и shadows
  - Border radius: 5px, 12px, 15px, 20px, 30px, 40px, 100px
  - iOS keyboard shadows
  - Opacity: 0.25, 0.55
- **Компоненты**: Полностью обновлены на основе Flutter кода
  - Cards: Mobile-first (375px), padding 8/16px, border-radius 20px
  - Buttons: Primary (#4141E6), height 44px, border-radius 15px
  - Avatars: Sizes 32-60px, Instagram-style borders
  - iOS Keyboard: Полная спецификация клавиатуры
  - Home Indicator: 134×5px pill
  - Live Badge: Instagram gradient badge
  - Screen Container: 375×812px (iPhone X)
- **Градиенты**: Instagram-style gradient с примерами кода
  - Flutter и CSS implementations
  - Horizontal gradient (90deg)

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
