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
--color-text-muted: rgba(0, 0, 0, 0.55);  /* Приглушенный текст */
```

### Accent Colors

```css
/* Акцентные цвета из Flutter кода */
--color-primary: #4141E6;            /* Основной синий (кнопки) */
--color-accent-blue: #4141E6;
--color-accent-green: #11BB8D;       /* Зеленый акцент (border) */
--color-accent-green-light: #0C11BB8D;  /* Зеленый с прозрачностью */
--color-accent-pink: #FC466B;        /* Розовый градиент */
```

### Gradient Colors

```css
/* Цвета градиентов из Flutter кода */
--gradient-purple: #833AB4;          /* Фиолетовый (Instagram gradient) */
--gradient-red: #FD1D1D;             /* Красный (Instagram gradient) */
--gradient-orange: #FCB045;          /* Оранжевый (Instagram gradient) */

/* Instagram-style gradient */
--gradient-instagram: linear-gradient(135deg, #833AB4 0%, #FD1D1D 50%, #FCB045 100%);
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
```

### Shadow Colors

```css
/* Тени из Flutter кода */
--shadow-keyboard-dark: #898A8D;
--shadow-keyboard-light: rgba(4, 4, 15, 0.36);
--shadow-button-dark: rgba(0, 0, 0, 0.35);
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
--font-size-10: 0.625rem;     /* 10px - из Flutter кода */
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

#### Primary Button

- **Size**:
  - Height: 44px (standard mobile)
  - Padding: 16px horizontal, 10px vertical
  - Width: 100% (full-width) или 327px
  - Gap между элементами: 8px
- **Border Radius**: 15px
- **Typography**:
  - Font Size: 14px
  - Font Weight: 600 (semibold)
  - Line Height: 140%
- **Colors**:
  - Background: #4141E6
  - Text: #FFFFFF
  - Shadow: None (flat design)
- **Alignment**: Center (text и иконки)

**States:**
- **Default**: Background: #4141E6, Text: white
- **Hover**: Легкое затемнение (opacity: 0.9)
- **Active**: Затемнение (opacity: 0.8)
- **Disabled**: Background: #D9DDE2, Text: rgba(0,0,0,0.4), Cursor: not-allowed

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

#### Close Button (в карточках)
- **Size**: 24px × 24px
- **Padding**: 6px (иконка 12px)
- **Border Radius**: 100px (circular)
- **Background**: #F4F6F9
- **Position**: Absolute, top-right

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

### 19. Badges (из Flutter кода)

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

---

### 20. Screen Container (из Flutter кода)

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

**Текущая версия**: v5.1.0

### Changelog

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
