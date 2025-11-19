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
--color-primary-action: #2E5AAC;   /* Primary action цвет для onboarding/auth screens (buttons, progress, focus) */
--color-accent-blue: #1D4ED8;      /* blue-700 */
--color-accent-purple: #7B61FF;    /* Фиолетовый из Flutter кода */
--color-accent-yellow: #FFC043;    /* Желтый/золотой для charts из Flutter */
--color-accent-green-light: #D4FC79; /* Светло-зеленый для градиентов Cash Card */
--color-accent-green: #96E6A1;     /* Зеленый для градиентов Cash Card */
--color-accent-green-tab: #98E7A0; /* Зеленый для активных табов Cash Card */
--color-accent-green-border: #9AE89F; /* Зеленая рамка аватара Cash Card */
--color-accent-green-button: #D2FC7B; /* Светло-зеленая кнопка Activate */
--color-success: #11BB8D;          /* Зеленый для success badges из Flutter */
--color-error: #DA1414;            /* Красный для destructive actions из Flutter (delete, remove) */
--color-notification: #E24949;     /* Красный для notification badges из Flutter (active notifications, alerts) */
```

### Background Colors

```css
/* Фоны для компонентов */
--color-bg-light: #F4F6F9;         /* Светлый фон из Flutter (основной для cards) */
--color-bg-light-input: #FAFAFB;   /* Очень светлый фон для input полей (onboarding/auth screens) */
--color-bg-light-pressed: #EAEEF2; /* Pressed state для светлых компонентов (textarea, inputs) */
--color-bg-dark: #18202F;          /* Темный scaffold background из Flutter */
--color-bg-dark-secondary: #23262B; /* Темный вторичный фон (для picker items, secondary dark elements) */
--color-bg-overlay: rgba(0, 0, 0, 0.10);  /* Overlay для изображений */
--color-bg-card-light: #D9DDE2;    /* Светлая карточка (avatar placeholder) */
--color-bg-card-dark: #09101D;     /* Темная карточка (dark buttons, dark elements) */
--color-bg-success-light: rgba(17, 187, 141, 0.05); /* Success state background (5% opacity) */
--color-bg-error-light: rgba(218, 20, 20, 0.05);   /* Error state background (5% opacity) */
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
--space-50: 3.125rem; /* 50px - из Flutter spacing: 50 (для Picker spacing) */
--space-70: 4.375rem; /* 70px - из Flutter spacing: 70 (для Row spacing) */
```

### Gradient Colors

```css
/* Градиенты из Flutter кода */
--gradient-live-badge: linear-gradient(90deg, #833AB4 0%, #FD1D1D 50%, #FCB045 100%);
--gradient-image-overlay: linear-gradient(180deg, rgba(196, 196, 196, 0) 0%, rgba(29, 29, 29, 0.50) 100%);
--gradient-cash-card: linear-gradient(90deg, #D4FC79 0%, #96E6A1 100%); /* Зеленый градиент для Cash Card */
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

#### Textarea (Multi-line Input - Flutter Mobile)

**Container**:
- Width: 375px (mobile screen width)
- Padding: 16px horizontal
- Column spacing: 10px (между label и field)

**Field**:
- Height: 135px
- Padding: 20px horizontal, 15px vertical
- Border Radius: 15px
- Background: #F4F6F9 (color-bg-light)
- Border: none (default), 2px solid (focus/active/positive/negative states)

**Typography**:
- **Label**:
  - Font: Archivo 14px, weight 600
  - Color: #09101D (color-text-primary)
  - Line Height: 1.40
- **Placeholder**:
  - Font: Archivo 14px, weight 400
  - Color: #747B84 (color-text-secondary)
  - Line Height: 1.40
- **Content Text**:
  - Font: Archivo 14-15px, weight 400
  - Color: #09101D (color-text-primary)
  - Line Height: 1.40
- **Character Counter**:
  - Font: Archivo 10px, weight 600
  - Position: Right (bottom-right corner)
  - Format: "current/max" (e.g., "256/1200")
  - Color: normal (#747B84), error (#E24949 when over limit)
- **Helper Message**:
  - Font: Archivo 14px, weight 400
  - Color: #747B84 (color-text-secondary)
  - Margin Top: 5px
- **Error Message**:
  - Font: Archivo 14px, weight 400
  - Color: #E24949 (color-notification)
  - Margin Top: 5px

**Icons**:
- Close Icon: 24px × 24px (positioned top-right inside field)
- Check Icon: 24px × 24px (for positive/success state)
- Size: 24px container, internal icon sizing varies

**States**:

1. **Enabled** (Default):
   - Background: #F4F6F9 (color-bg-light)
   - Border: none
   - Placeholder: #747B84
   - Counter: "0/1200" (#747B84)

2. **Focus**:
   - Background: #F4F6F9 (color-bg-light)
   - Border: 2px solid #09101D (color-text-primary)
   - Placeholder: visible or hidden (when typing)

3. **Pressed** (Tap/Click):
   - Background: #EAEEF2 (color-bg-light-pressed)
   - Border: none
   - Temporary state during press

4. **Complete** (With Content):
   - Background: #F4F6F9 (color-bg-light)
   - Border: none
   - Content text: visible
   - Counter: "256/1200" (#747B84)
   - Close icon: visible (24px, top-right)

5. **Active-Typing** (Actively Typing):
   - Background: #F4F6F9 (color-bg-light)
   - Border: 2px solid #09101D (color-text-primary)
   - Content text: visible
   - Counter: "256/1200" (#747B84)
   - Close icon: visible (24px, top-right)

6. **Incomplete** (Required but Empty):
   - Background: #F4F6F9 (color-bg-light)
   - Border: none
   - Placeholder: visible
   - Counter: "0/1200" (#747B84)
   - Close icon: visible (24px, top-right)

7. **Positive** (Success/Valid):
   - Background: rgba(17, 187, 141, 0.05) (color-bg-success-light)
   - Border: 2px solid #11BB8D (color-success)
   - Content text: visible
   - Check icon: visible (24px, positioned appropriately)
   - Helper message: optional success message

8. **Negative** (Error/Invalid):
   - Background: rgba(218, 20, 20, 0.05) (color-bg-error-light)
   - Border: 2px solid #DA1414 (color-error)
   - Content text: visible
   - Counter: "1322/1200" in #E24949 (shows over-limit)
   - Error message: visible below field
   - Helper text: replaced by error message

9. **Disabled**:
   - Background: #F4F6F9 (color-bg-light)
   - All text colors: #D9DDE2 (color-text-disabled)
   - Counter: #D9DDE2
   - Helper: #D9DDE2
   - Cursor: not-allowed
   - Opacity: reduced

**Character Counter Functionality**:
- Always visible in bottom-right corner
- Updates in real-time as user types
- Shows "current/max" format
- Color changes to #E24949 when limit exceeded
- Example: "0/1200", "256/1200", "1322/1200"

**Validation Patterns**:
- **Success**: Green border (#11BB8D) + light green background
- **Error**: Red border (#DA1414) + light red background + error message
- **Over Limit**: Counter turns red (#E24949)

**Usage**: Multi-line text input for comments, descriptions, messages, notes, etc.

#### Select

- **Height**: 40px (medium)
- **Padding**: 10px 36px 10px 12px
- **Icon**: Chevron down, Right: 12px, Size: 16px

---

### 4. Pickers (Flutter Mobile)

#### Day Picker

**Container**:
- Padding: 50px all
- Border: 1px solid #7B61FF (color-accent-purple)
- Border Radius: 15px
- Clip Behavior: antiAlias

**Row Layout**:
- Spacing: 50px (space-50)

**Day Item**:
- Width: 50px
- Padding: 14px horizontal, 8px vertical
- Border Radius: 15px
- Column spacing: 2px

**States**:
- **Dark Selected**:
  - Background: #23262B (color-bg-dark-secondary)
  - Text: white
- **Light**:
  - Background: #F4F6F9 (color-bg-light)
  - Text: #09101D (color-text-primary)
- **Disabled**:
  - Background: #F4F6F9 (color-bg-light)
  - Text: #D9DDE2 (color-text-disabled)

**Typography**:
- Label ("Day"):
  - Font: Archivo 12px, weight 400
  - Line Height: 1.40
  - Text Align: center
- Number ("00"):
  - Font: Archivo 14px, weight 600
  - Line Height: 1.40
  - Text Align: center

#### Time Picker

**Container**:
- Padding: 50px all
- Border: 1px solid #7B61FF (color-accent-purple)
- Border Radius: 15px
- Clip Behavior: antiAlias

**Row Layout**:
- Spacing: 50px (space-50)

**Time Slot**:
- Height: 40px (для selected/active)
- Padding: 10px all
- Border Radius: 15px

**States**:
- **Primary Selected**:
  - Background: #09101D (color-bg-card-dark)
  - Text: white
- **Dark**:
  - Background: #23262B (color-bg-dark-secondary)
  - Text: white
- **Disabled/Crossed**:
  - Background: transparent
  - Text: #D9DDE2 (color-text-disabled)
  - Text Decoration: line-through
- **Light**:
  - Background: #F4F6F9 (color-bg-light)
  - Text: #09101D (color-text-primary)

**Typography**:
- Time Text ("10:00"):
  - Font: Archivo 12px, weight 400
  - Line Height: 1.40

---

### 5. File Type & Dropdown Components (Flutter Mobile)

#### File Type Icons Grid

**Container**:
- Height: 318px
- Padding: 50px all
- Background: white (#FFFFFF)
- Border: 1px solid #7B61FF (color-accent-purple)
- Border Radius: 15px
- Clip Behavior: antiAlias

**Layout**:
- Type: Row
- Spacing: 10px (между элементами)
- Main Axis: start
- Cross Axis: center

**File Type Item**:
- Width: 34px
- Height: 40px
- Container: Stack (для иконки и контента)

**Usage**: Grid для отображения различных типов файлов (PDF, DOC, XLS, etc.)

#### Dropdown/Context Menu

**Container**:
- Height: 318px (или auto)
- Padding: 50px all
- Background: white (#FFFFFF)
- Border: 1px solid #7B61FF (color-accent-purple)
- Border Radius: 15px
- Clip Behavior: antiAlias

**Layout**:
- Type: Column
- Main Axis: center
- Cross Axis: center

**Menu Item**:
- Width: 333px
- Padding: 16px horizontal, 8px vertical
- Background: #F4F6F9 (color-bg-light)
- Row spacing: 16px (между иконкой и текстом)

**Menu Item Variants**:
- **First Item (Top)**:
  - Border Radius: 15px (только top-left и top-right)
  - Text Color: #09101D (color-text-primary)
- **Middle Item**:
  - Border Radius: none (прямоугольный)
  - Text Color: #09101D (color-text-primary)
- **Last Item (Bottom)**:
  - Border Radius: 15px (только bottom-left и bottom-right)
  - Text Color: может быть обычный (#09101D) или destructive (#DA1414)
- **Destructive Item**:
  - Background: #F4F6F9 (color-bg-light)
  - Text Color: #DA1414 (color-error) - для опасных действий (Delete, Remove)

**Icon**:
- Size: 24px × 24px
- Clip Behavior: antiAlias

**Typography**:
- Font: Archivo 14px, weight 600
- Line Height: 1.40
- Text Width: 192px
- Colors:
  - Normal: #09101D (color-text-primary)
  - Destructive: #DA1414 (color-error)

**Usage**: Dropdown меню, контекстные меню, action sheets с возможностью destructive действий

---

### 6. Segmented Control (Flutter Mobile)

#### Segmented Control (2-3 Segments)

**Container**:
- Width: 375px (mobile screen width)
- Height: 41px
- Padding: 16px-17px horizontal, 5px vertical
- Clip Behavior: antiAlias

**Background Track**:
- Background: #F4F6F9 (color-bg-light)
- Border Radius: 8px
- Padding: 2px all (inner padding для сегментов)

**Segment (Selected)**:
- Background: white (#FFFFFF)
- Border Radius: 8px
- Shadow: rgba(0, 0, 0, 0.10) blur 4px, offset (0, 1), spread 0
- Text: Archivo 13px, weight 600, color #09101D
- Padding: 5px vertical
- Text Align: center

**Segment (Unselected)**:
- Background: transparent
- Border Radius: 8px
- Text: Archivo 13px, weight 600, color #09101D
- Padding: 5px vertical
- Text Align: center

**Layouts**:
- **2 Segments**: Row with 2 expanded items, spacing 10px
- **3 Segments**: Row with 3 expanded items, spacing 2px

**Usage**: Toggle между двумя или тремя опциями (например, выбор валюты, периода, режима)

---

### 7. Tabs (Flutter Mobile)

#### Tab Bar

**Container**:
- Width: 375px (mobile screen width)
- Background: white (#FFFFFF)
- Clip Behavior: antiAlias

**Tab Item**:
- Height: 52px
- Padding: 10px horizontal
- Row spacing: 8px (между элементами)

**Tab Variants**:
- **2 Tabs**: Row with 2 expanded items
- **3 Tabs**: Row with 3 expanded items
- **4+ Tabs**: Row with start alignment (scrollable)

**Tab Elements**:
- **Icon** (optional):
  - Size: 20px × 20px
  - Padding: 2px
  - Border Radius: 100px
  - Container: Stack для иконки
- **Text**:
  - Font: Archivo 14px, weight 600
  - Color: #09101D (color-text-primary)
  - Line Height: 1.40
- **Badge** (optional):
  - Height: 20px
  - Padding: 4px horizontal, 2px vertical
  - Border Radius: 20px
  - Text: white, 10px, weight 600, line-height 1.40
  - Content: число (например, "11")

**Badge Variants**:
- **Active/Notification**:
  - Background: #E24949 (color-notification)
  - Text: white
- **Inactive/Count**:
  - Background: #414249 (color-text-tertiary)
  - Text: white

**Tab States**:
- **Active**:
  - Bottom border: 2px solid #23262B (color-bg-dark-secondary)
- **Inactive**:
  - Bottom border: 2px solid #F4F6F9 (color-bg-light)

**Usage**: Навигация между разделами, с опциональными иконками и счетчиками уведомлений

---

### 8. Badges & Tags (Flutter Mobile)

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

### 9. Forms

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

### 10. Tables

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

### 11. Navigation

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

### 12. Charts

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

#### Spiral/Radial Timeline Chart (Flutter Mobile)

**Размеры**:
- Container: 375px × 170px или 375px × 240px
- Chart Area: 186px × 186px (circular area)
- Clip Behavior: antiAlias

**Data Points**:
- Size: 5px × 5px
- Shape: OvalBorder (круг)
- Colors:
  - Primary: #4141E6 (color-primary)
  - Secondary: #FFC043 (color-accent-yellow)
- Border:
  - Width: 1px
  - Stroke Align: strokeAlignOutside
  - Primary Border: rgba(11, 36, 251, 0.20) - #0B24FB с opacity 20%
  - Secondary Border: rgba(255, 192, 67, 0.20) - #FFC043 с opacity 20%

**Labels** (Year markers):
- Font: Archivo 10px, weight 400
- Color: #09101D (color-text-primary)
- Line Height: 1.40
- Text Align: center
- Positioning: Absolute (Positioned по кругу)
- Examples: "2014", "2015", "2016", "2017", "2018", "2019", "2020", "2021"

**Layout**:
- Points и labels распределены по окружности
- Абсолютное позиционирование для всех элементов
- Chart area центрируется в контейнере

**Использование**: Timeline visualization, yearly data, spiral progress charts

---

### 13. Avatars (Flutter Mobile)

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

### 14. List Items

#### List Item

- **Height**: 48px (medium)
- **Padding**: 12px 16px
- **Border Bottom**: 1px solid color-border-primary
- **States**:
  - Hover: Background: color-bg-secondary
  - Active: Background: color-primary-light
  - Selected: Background: color-primary-light, Border-left: 3px solid color-primary

---

### 15. Messages / Notifications

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

#### Snackbar (Flutter Mobile)

**Container**:
- Width: 375px (mobile screen width)
- Padding: 16px all (outer container)
- Clip Behavior: antiAlias

**Snackbar Base**:
- Background: #09101D (color-bg-card-dark)
- Border Radius: 15px
- Padding: 16px all
- Clip Behavior: antiAlias (optional, based on variant)

**Typography**:
- **Message Text**:
  - Font: Archivo 14px, weight 600
  - Color: white (#FFFFFF)
  - Line Height: 1.40
  - Width: varies by variant (159px-311px)
- **Action Button Text**:
  - Font: Archivo 13px, weight 600
  - Color: white (#FFFFFF)
  - Line Height: 1.40

**Elements**:

1. **Avatar** (optional):
   - Container: 56px × 56px
   - Inner Avatar: 48px × 48px
   - Position: left 4px, top 4px (within container)
   - Border Radius: 40px
   - Background: white (placeholder)
   - Image: NetworkImage with BoxFit.cover
   - Padding: 16px (around avatar container)

2. **Icon** (optional):
   - Size: 24px × 24px
   - Padding: 16px (around icon)
   - Clip Behavior: antiAlias

3. **Close Button** (optional):
   - Icon Size: 20px × 20px
   - Container Height: 44px or 36px
   - Padding: 16px horizontal, 10px vertical
   - Border Radius: 15px
   - Position: right side

4. **Action Button** (optional):
   - Height: 36px or 44px
   - Padding: 16px horizontal, 10px vertical
   - Border Radius: 15px
   - Text: "Action" (customizable)
   - Position: right side
   - Spacing: 70px (internal row spacing)

**Variants**:

1. **Basic Snackbar** (Text Only):
   - Padding: 16px all
   - Message width: 311px
   - No icons, no actions
   - **Usage**: Simple notifications

2. **Snackbar with Icon**:
   - Icon: 24px (left side, padding 16px)
   - Message width: 235px-271px
   - Optional close button (20px icon)
   - Row layout: Icon + Text + (optional Close)
   - **Usage**: Info, success, warning, error notifications

3. **Snackbar with Avatar**:
   - Avatar: 56px container (left side, padding 16px)
   - Message width: 203px-239px
   - Optional close button or action button
   - Row layout: Avatar + Text + (optional Action/Close)
   - **Usage**: User-related notifications, social updates

4. **Snackbar with Action**:
   - No icon/avatar
   - Message width: 223px-267px
   - Action button: height 36px or 44px (right side)
   - Row layout: Text + Action Button
   - **Usage**: Notifications requiring user action

5. **Snackbar with Icon and Action**:
   - Icon: 24px (left side)
   - Message width: varies
   - Action button: height 44px (right side)
   - Row layout: Icon + Text + Action Button
   - **Usage**: Notifications with context icon and action

6. **Snackbar with Avatar and Action**:
   - Avatar: 56px container (left side)
   - Message width: 159px-223px
   - Action button: height 36px or 44px (right side)
   - Row layout: Avatar + Text + Action Button
   - **Usage**: Social notifications with user context and action

**Layout Patterns**:
- **Row Layout**: Main axis start, cross axis center
- **Expanded Text**: Text container uses Expanded to fill available space
- **Spacing**: 8px between major elements
- **Padding**:
  - Avatar/Icon section: padding 16px
  - Text section: padding 16px vertical, 0-8px horizontal (right)
  - Action/Close: padding 16px horizontal, 10px vertical

**Height Variations**:
- Text only: ~56px (with 2-line message)
- With icon/avatar: ~88px (with 2-line message)
- With action button: varies (36px-44px button height)

**Usage Guidelines**:
- Use basic snackbar for simple status messages
- Add icon for semantic meaning (success, error, info, warning)
- Add avatar for user-related notifications
- Add action button when user response is needed
- Add close button for persistent snackbars
- Position at bottom of screen for mobile
- Auto-dismiss after 3-5 seconds (optional)
- Stack multiple snackbars vertically with 10px spacing

---

### 16. Panels & Cards

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

### 17. Accordion / FAQ

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

### 18. Loading States

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

### 19. Empty States

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

## Mobile Card Components (Flutter)

<!-- AI-FRIENDLY: Mobile Card Components -->
**See Also**: [E-commerce Product Cards](#e-commerce-components-flutter-mobile) for shopping/marketplace card components

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

## Financial Components (Flutter Mobile)

### Cash Card Component

**Container**:
- Width: 375px (full mobile width)
- Padding: 16px horizontal, 10px vertical
- Background: white

**Header Section**:
- **Height**: 44px
- **Padding**: 16px horizontal
- **Layout**: Row with spaceBetween
- **Elements**:
  - **Title**: "Cash Card"
    - Font: Archivo 24px, weight 700
    - Color: #09101D (color-text-primary)
    - Line Height: 1.40
  - **Avatar with Actions**:
    - Avatar Container: 40px × 40px
    - Border: 2px solid #9AE89F (color-accent-green-border)
    - Border Radius: 30px
    - Inner Avatar: 32px × 32px (4px offset)
    - Background: #D9DDE2 (placeholder)
    - Image: NetworkImage, fit cover
    - Border Radius: 40px
    - Settings Icon: 24px × 24px, background #F4F6F9, border-radius 10px
    - Spacing: 6px between avatar and icon

**Card Section** (padding: top 50px, bottom 10px):
- **Container**: Full width, padding 16px horizontal, 10px vertical
- **Card Container**:
  - Padding: 10px all
  - Background: linear-gradient(90deg, #D4FC79 0%, #96E6A1 100%)
  - Border: 1px solid rgba(0, 0, 0, 0.05)
  - Border Radius: 15px
  - Clip Behavior: antiAlias

**Card Inner Layout**:
- **Top Section** (padding: 10px):
  - **Logo Container**: 60px × 60px
    - Border Radius: 15px
    - Image: NetworkImage, fit contain
    - Position: left
  - **Menu Icon**: 20px × 20px
    - Position: right
    - Padding: 10px (container)

- **Card Data Section** (padding: 10px, bottom section):
  - **Card Number**:
    - Text: "1234 5678 9000 0000"
    - Font: OCR-A 22px, weight 400
    - Color: #09101D
    - Line Height: 1.40
    - Letter Spacing: 2.59px
    - Shadow: 0px 1px 1px rgba(0, 0, 0, 0.40)
    - Width: 303px

  - **Card Details Row** (spacing: 20px, layout: spaceBetween):
    - **Name**: "JANE APPK"
      - Font: OCR-A 11px, weight 400
      - Color: #09101D
      - Letter Spacing: 2px
      - Shadow: 0px 1px 1px rgba(0, 0, 0, 0.40)
    - **Expiry Date**: "04 / 23"
      - Font: OCR-A 11px, weight 400
      - Color: #09101D
      - Letter Spacing: 1px
      - Shadow: 0px 1px 1px rgba(0, 0, 0, 0.40)
    - **Card Logo**: 40px × 24px (Visa/Mastercard logo)
      - Position: right

**Notification Item** (padding: 10px horizontal):
- **Container**: Full width
- **Background**: white
- **Clip Behavior**: antiAlias
- **Layout**: Row

**Notification Content** (padding: left 16px, vertical 12px):
- **Width**: 160px
- **Title**: "Cash Card Shipped"
  - Font: Archivo 14px, weight 600
  - Color: #09101D (color-text-primary)
  - Line Height: 1.40
- **Time**: "19 hours ago"
  - Font: Archivo 11px, weight 600
  - Color: #23262B (color-bg-dark-secondary)
  - Line Height: 1.40

**Activate Button** (padding: 16px horizontal, right aligned):
- **Height**: 36px
- **Padding**: 16px horizontal, 10px vertical
- **Background**: #D2FC7B (color-accent-green-button)
- **Border Radius**: 15px
- **Text**: "Activate"
  - Font: Archivo 11px, weight 600
  - Color: #09101D
  - Line Height: 1.40

**Tabs Section** (padding: 16px horizontal):
- **Container**: Full width
- **Spacing**: 20px between tabs
- **Clip Behavior**: antiAlias

**Tab Item**:
- **Height**: 52px
- **Padding**: 10px horizontal (text container)
- **Clip Behavior**: antiAlias
- **Spacing**: 8px (internal)

**Tab States**:
- **Active Tab** ("Cashback"):
  - Text: "Cashback"
    - Font: Archivo 13px, weight 600
    - Color: #98E7A0 (color-accent-green-tab)
    - Line Height: 1.40
  - Underline: 2px solid #98E7A0
  - Position: bottom

- **Inactive Tabs** ("Boosts slots", "Special offers"):
  - Text Font: Archivo 11px, weight 600
  - Color: #09101D (color-text-primary)
  - Line Height: 1.40
  - Underline: 2px transparent

**Cashback Section** (padding: 16px horizontal, 20px vertical):
- **Container**: Full width
- **Spacing**: 10px between items
- **Clip Behavior**: antiAlias

**Cashback Item**:
- **Container**: Column layout
- **Padding**: 10px all
- **Background**: rgba(212, 252, 122, 0.50) (#D4FC7A with 50% opacity)
- **Border Radius**: 15px
- **Clip Behavior**: antiAlias
- **Spacing**: 5px (between icon and percentage)

**Cashback Elements**:
- **Icon Container**: 44px × 44px
  - Padding: 15px (for icon)
  - Background: Store logo image
  - Border Radius: 15px
  - Image Fit: contain
- **Percentage Text**: "5%"
  - Font: Archivo 13px, weight 600
  - Color: #09101D
  - Line Height: 1.40
  - Centered

**Empty Cashback Slot**:
- Same container specs
- Icon: 44px × 44px with 1px solid #09101D border
- Border Radius: 15px
- Plus icon: 16.80px × 16.80px (centered, -1.40px offset positioning)

**Layout Notes**:
- Card gradient can be customized per card type
- OCR-A font used for authentic card number display
- Card supports both network images and placeholder states
- Notification can be dismissed or have different actions
- Tabs are horizontally scrollable if more than 3
- Cashback slots flexible (add/remove based on active offers)

---

## Onboarding & Authentication Screens (Flutter Mobile)

### Common Elements

#### Status Bar
- **Height**: 44px
- **Background**: #09101D (color-bg-card-dark)
- **Content**: System time, signal indicators (21px × 54px container)
- **Usage**: Fixed at top of screen

#### Pull Indicator
- **Size**: 40px × 3px
- **Background**: #D9DDE2 (color-bg-card-light)
- **Border Radius**: 100px (fully rounded)
- **Position**: Centered horizontally, 8px from top edge
- **Usage**: Bottom sheet pull handle

#### Progress Indicator (Step Bar)
- **Container**: 375px width, padding 10px vertical
- **Segment Height**: 3px
- **Number of Segments**: 5 (customizable)
- **Spacing**: 0 (segments touch)
- **Active Segment**: #2E5AAC (color-primary-action)
- **Inactive Segment**: rgba(9, 16, 29, 0.10) (10% opacity black)
- **Border Radius**:
  - First segment: left corners 10px
  - Last segment: right corners 10px
  - Middle segments: 3px (rectangular)
- **Usage**: Multi-step form progress tracking

#### Back Button
- **Container**: 44px height, padding 16px horizontal, 10px vertical
- **Icon**: 24px × 24px (2px padding inner)
- **Border Radius**: 12px
- **Position**: Top left of screen
- **Usage**: Navigate to previous screen/step

### Screen 1: Phone Number Input

**Layout**:
- **Container**: 375px × 499px
- **Background**: white
- **Border Radius**: 30px (top corners)
- **Status Bar**: 44px black bar at top
- **Pull Indicator**: 40px × 3px, centered

**Progress**: 1 of 5 segments active

**Header**:
- **Padding**: 16px horizontal, 10px vertical
- **Spacing**: 5px between title and subtitle
- **Title**: "Add your mobile number"
  - Font: Archivo 26px, weight 700
  - Color: #09101D (color-text-primary)
  - Line Height: 1.40
- **Subtitle**: "We'll need to confirm it by sending a text"
  - Font: Archivo 18px, weight 400
  - Color: #414249 (color-text-tertiary)
  - Line Height: 1.40
  - Width: 343px

**Phone Input Section** (padding: 16px horizontal, 5px vertical, top 20px):
- **Label**: "Mobile number"
  - Font: Archivo 14px, weight 600
  - Color: #09101D
  - Line Height: 1.40
- **Input Row** (spacing: 8px):
  - **Country Selector**:
    - Height: 46px
    - Padding: left 16px, right 10px
    - Background: #FAFAFB (color-bg-light-input)
    - Border Radius: 15px
    - Flag: 22px × 16px, border-radius 2px
    - Dropdown icon: 20px × 20px
    - Spacing: 20px between flag and icon
  - **Phone Input**:
    - Height: 46px
    - Padding: left 16px, right 20px
    - Border: 2px solid #2E5AAC (color-primary-action) when focused
    - Border Radius: 15px
    - Text: "+1 628 123 4567"
      - Font: Archivo 14px, weight 600
      - Color: #09101D
      - Line Height: 1.40
    - Cursor: 2px × 16px

**Disclaimer Text** (padding: 16px horizontal, 10px vertical):
- **Font**: Archivo 12px, weight 400
- **Color**: #747B84 (color-text-secondary)
- **Line Height**: 1.40
- **Width**: 343px
- **Content**: "By continuing, you confirm that you're the owner..."

**Next Button** (padding: 16px horizontal, 10px vertical):
- **Height**: 44px
- **Padding**: 16px horizontal, 10px vertical
- **Background**: #2E5AAC (color-primary-action)
- **Border Radius**: 15px
- **Text**: "Next"
  - Font: Archivo 14px, weight 600
  - Color: white
  - Line Height: 1.40
- **Layout**: Row with spaceBetween, spacing 70px

### Screen 2: Registration Form

**Layout**:
- **Container**: 375px × 515px
- **Background**: white
- **Border Radius**: 30px (top corners)
- **Status Bar**: 44px at top (no background color)

**Header**:
- **Padding**: left 16px, right 16px, bottom 10px
- **Title**: "Get started"
  - Font: Archivo 32px, weight 700
  - Color: #09101D (color-text-primary)
  - Line Height: 1.40
  - Width: 343px
  - Height: 44px

**Form Inputs** (4 fields, 16px horizontal padding, 5px vertical):
1. **Full Name**:
   - Height: 46px
   - Padding: left 16px, right 20px
   - Border: 1px solid #D9DDE2 (color-text-disabled)
   - Border Radius: 15px
   - Placeholder: "Full Name"
     - Font: Archivo 15px, weight 400
     - Color: rgba(9, 16, 29, 0.40) (40% opacity)
     - Line Height: 1.40

2. **Email Address**:
   - Same specs as Full Name
   - Placeholder: "Email Address"

3. **Confirm Email**:
   - Same specs as Full Name
   - Placeholder: "Confirm Email"

4. **Password**:
   - Same specs as Full Name
   - Placeholder: "Password"

**Password Strength Indicator** (padding: 16px horizontal, 10px vertical):
- **Container**: 3 segments
- **Segment Height**: 3px
- **Spacing**: 10px between segments
- **Border Radius**: 3px
- **Colors**:
  - Weak (1 segment): #D9DDE2
  - Medium (2 segments): #D9DDE2
  - Strong (3 segments): #D9DDE2
- **Layout**: Row with expanded segments

**Terms Text** (padding: 16px horizontal, 10px vertical):
- **Font**: Archivo 15px, weight 400/600
- **Color**: #747B84 (regular), #11BB8D (links - color-success)
- **Line Height**: 1.40
- **Width**: 343px
- **Content**: "By signing up for Appka, you agree to the Appka's **Term of Service** and **Privacy Policy**"

**Create Account Button** (padding: 16px horizontal, 10px vertical):
- **Height**: 44px
- **Padding**: 16px horizontal, 10px vertical (inner: 10px horizontal for text)
- **Background**: #11BB8D (color-success)
- **Border Radius**: 15px
- **Text**: "Create account"
  - Font: Archivo 14px, weight 600
  - Color: white
  - Line Height: 1.40
- **Layout**: Row with spaceBetween, spacing 70px

### Screen 3: Phone Verification (OTP)

**Layout**:
- **Container**: 375px × 444px
- **Background**: white
- **Border Radius**: 30px (top corners)
- **Status Bar**: 44px black bar at top
- **Pull Indicator**: 40px × 3px, centered

**Progress**: 4 of 5 segments active (#2E5AAC)

**Header**:
- **Padding**: 16px horizontal, 10px vertical
- **Spacing**: 5px between title and subtitle
- **Title**: "Check your phone"
  - Font: Archivo 26px, weight 700
  - Color: #09101D (color-text-primary)
  - Line Height: 1.40
- **Subtitle**: "To confirm your account, enter the 4-digit code sent to **+1 628 123 4567**"
  - Font: Archivo 18px, weight 400/700 (number in bold)
  - Color: #414249 (color-text-tertiary)
  - Line Height: 1.40
  - Width: 343px

**Code Input Section** (padding: 16px horizontal, 5px vertical, top 20px, bottom 10px):
- **Label**: "Code"
  - Font: Archivo 14px, weight 600
  - Color: #09101D
  - Line Height: 1.40
- **Code Fields** (4 fields, spacing: 20px):
  - **Width**: Expanded (equal width)
  - **Height**: 46px
  - **Background**: #FAFAFB (color-bg-light-input)
  - **Border Radius**: 12px
  - **States**:
    - Empty: background #FAFAFB
    - Filled: text "4", font Archivo 14px weight 400, color #09101D, centered
    - Active/Focus: border 2px solid #2E5AAC (color-primary-action)
  - **Clip Behavior**: antiAlias

**Helper Text** (padding: 16px horizontal, 20px vertical):
- **Font**: Archivo 14px, weight 400/600
- **Color**: #23262B (regular), #2E5AAC (link - color-primary-action)
- **Line Height**: 1.40
- **Width**: 343px
- **Content**: "Didn't get the code? **See other options**"

**Usage Notes**:
- All screens use 375px width (standard mobile)
- Padding typically 16px horizontal for content
- Border radius: 15px for buttons/inputs, 12px for small fields
- Spacing between elements: 5px-20px depending on hierarchy
- Forms can be extended with additional fields as needed
- Progress indicator segments adjustable (3-7 steps typical)
- Input states: default, focus (2px border), filled, disabled (not shown)

---

<!-- AI-FRIENDLY: E-commerce Components Section -->
<!-- KEYWORDS: product card, shopping, marketplace, e-commerce, retail, catalog -->
<!-- COMPONENT_TYPE: Product Listings, Shopping Cards -->
<!-- USE_CASES: Product catalogs, marketplace listings, shopping grids, retail apps -->

## E-commerce Components (Flutter Mobile)

**Component Type**: Product Card (Vertical Layout)
**Use Cases**: Shopping, Marketplace, Product Listings, Retail Catalogs
**Related Components**: [Image Cards](#mobile-card-components-flutter), [Badges](#badges-flutter-mobile), [Buttons](#buttons-flutter-mobile)
**Platform**: Flutter Mobile (375px width standard)

---

### Product Card - Vertical Layout

<!-- AI-FRIENDLY: Product Card Component -->
**Description**: Vertical product card for e-commerce applications with image, badge, favorite button, rating, price, brand, and size information.

#### Container (Product List Wrapper)

**Outer Container**:
- **Width**: 375px (mobile screen width)
- **Padding**: 30px vertical
- **Background**: #FFFFFF (white)
- **Border Radius**: 30px
- **Clip Behavior**: antiAlias

**Cards Row** (Horizontal Scrollable):
- **Padding**: 16px horizontal, 10px vertical
- **Spacing**: 5px between cards
- **Layout**: Row with horizontal scroll
- **Clip Behavior**: antiAlias

#### Individual Product Card

**Card Container**:
- **Width**: 170px
- **Height**: 360px
- **Border Radius**: 15px
- **Layout**: Column (Image + Content)

**Card Structure**:
```
Product Card (170×360px)
├─ Image Section (~253px height, Expanded)
│  ├─ Product Image (170×253px, fit: cover, border-radius: 5px)
│  ├─ Favorite Button (top-left overlay, 30×30px)
│  └─ Status Badge (bottom-left overlay, "🔥 New")
└─ Content Section (~107px height)
   ├─ Rating (👌 4.8 (130))
   ├─ Price & Brand ($96.50, Nike 👟)
   └─ Sizes (36 ・ 37・ 38・ 39)
```

---

#### Image Section

**Image Container** (Expanded):
- **Width**: 170px (full card width)
- **Height**: ~253px (flexible, uses Expanded)
- **Border Radius**: 5px
- **Image Fit**: BoxFit.cover
- **Clip Behavior**: antiAlias
- **Image Source**: NetworkImage (placeholder or product image URL)

**Overlay Layout**:
- **Arrangement**: Column with `spaceBetween`
- **Elements**: Favorite Button (top) + Status Badge (bottom)

---

#### Favorite Button (Top-Left Overlay)

**Position**: Top-left corner of image
- **Padding from edges**: 10px all

**Button Container**:
- **Size**: 30px × 30px
- **Background**: #FFFFFF (white)
- **Border Radius**: 100px (circle)
- **Padding**: 8px (inner padding)

**Icon**:
- **Size**: ~16.8px × 16.8px (14px with 1.4px positioning offset)
- **Icon Type**: Heart (favorite/wishlist icon)
- **Color**: Not specified (typically #09101D or #DA1414 for filled)

**Interaction**:
- **States**: Default (outline heart), Active (filled heart)
- **Action**: Toggle favorite/wishlist

---

#### Status Badge (Bottom-Left Overlay)

**Position**: Bottom-left corner of image
- **Padding from edges**: 5px all

**Badge Container**:
- **Height**: auto (content-based)
- **Padding**: 5px horizontal, 3px vertical
- **Background**: #09101D (color-bg-card-dark)
- **Border Radius**: 5px

**Badge Content**: "🔥 New"
- **Emoji**: "🔥"
  - Font: Archivo 9px, weight 400
  - Color: #FFFFFF (white)
  - Line Height: 1.40
- **Text**: "New"
  - Font: Archivo 9px, weight 600
  - Color: #FFFFFF (white)
  - Line Height: 1.40

**Badge Variants** (Customizable):
- "🔥 New" - New arrivals
- "🏷️ Sale" - Sale items
- "⭐ Trending" - Trending products
- "🎯 Limited" - Limited edition
- Custom text + emoji combinations

---

#### Content Section (Card Bottom)

**Container**:
- **Padding**: top 10px, left 5px, right 10px, bottom 10px
- **Clip Behavior**: antiAlias
- **Spacing**: 5px between elements (column spacing)

**Elements** (Top to Bottom):
1. Rating Row
2. Product Info (Price + Brand)
3. Sizes

---

##### 1. Rating Row

**Layout**: Row with minimal spacing

**Rating Content**: "👌 4.8 (130)"

- **Emoji**: "👌"
  - Font Size: 13px
  - Color: #E24949 (color-notification) - used for visual accent

- **Rating Number**: "4.8"
  - Font: Archivo 13px, weight 600
  - Color: #09101D (color-text-primary)
  - Line Height: 1.40

- **Space**: " " (single space)
  - Font: Archivo 13px, weight 400
  - Color: #747B84 (color-text-secondary)

- **Review Count**: "(130)"
  - Font: Archivo 13px, weight 400
  - Color: #747B84 (color-text-secondary)
  - Line Height: 1.40

**Format**: `[emoji] [rating] ([count])`
**Examples**:
- "👌 4.8 (130)"
- "👌 4.5 (89)"
- "👌 5.0 (12)"

---

##### 2. Product Info (Price + Brand)

**Container**:
- **Width**: 155px max (full available width with padding)
- **Spacing**: 4px between price/brand and sizes

**Inner Spacing**: 2px between price and brand

**Price**:
- **Text**: "$96.50" / "$159.20" / "$350"
- **Font**: Archivo 14px, weight 600
- **Color**: #09101D (color-text-primary)
- **Line Height**: 1.40
- **Width**: 155px max

**Brand with Emoji**:
- **Brand Name**: "Nike"
  - Font: Archivo 14px, weight 600
  - Color: #09101D (color-text-primary)
  - Line Height: 1.40

- **Emoji**: "👟" (category emoji)
  - Font: Archivo 14px, weight 400
  - Color: #414249 (color-text-tertiary)
  - Line Height: 1.40

**Format**: `[brand_name] [emoji]`
**Examples**:
- "Nike 👟" - Footwear
- "Apple 📱" - Electronics
- "Adidas 👕" - Apparel
- "Samsung 💻" - Tech

---

##### 3. Sizes (Available Variants)

**Text**: "36 ・ 37・ 38・ 39"
- **Font**: Archivo 13px, weight 400
- **Color**: #747B84 (color-text-secondary)
- **Line Height**: 1.40
- **Width**: 155px max
- **Separator**: " ・ " (bullet separator)

**Format**: `[size1] ・ [size2]・ [size3]・ [size4]`

**Examples**:
- Footwear: "36 ・ 37・ 38・ 39"
- Apparel: "S ・ M・ L・ XL"
- Single size: "One Size"
- Out of stock: "Sold Out" (можно использовать цвет #DA1414)

---

### Layout Specifications

**Product Grid**:
- **Columns**: 2 cards per row (visible area)
- **Card Width**: 170px
- **Spacing**: 5px between cards
- **Scroll**: Horizontal scroll for additional cards
- **Padding**: 16px horizontal from screen edges

**Responsive Calculations**:
```
Screen Width: 375px
Container Padding: 16px × 2 = 32px
Available Width: 375px - 32px = 343px
Card Width: 170px
Spacing: 5px
Cards Visible: 2 cards (170px + 5px + 170px = 345px ≈ 343px with scroll)
```

---

### Usage Guidelines

**When to Use**:
- Product catalog screens
- Marketplace listings
- Search results
- Category browsing
- Recommended products sections

**Flexible Elements**:
- **Badge**: Can be customized with different text/emoji or hidden
- **Favorite Button**: Can be removed for non-authenticated users
- **Sizes**: Can be replaced with color swatches, variants, or other metadata
- **Rating**: Can be hidden if product is new (no reviews yet)
- **Price**: Can show original + discounted price for sales

**Accessibility**:
- Favorite button should have minimum touch target 44×44px (padding around 30px circle)
- Rating should include screen reader text: "Rated 4.8 out of 5 stars, 130 reviews"
- Product images should have alt text describing the product

**Performance**:
- Use image loading placeholders (skeleton or blur hash)
- Lazy load images for off-screen cards
- Cache images for better scroll performance
- Consider image optimization (WebP, AVIF)

---

### Color Reference

All colors used are from existing design system palette:

```css
/* Text */
--color-text-primary: #09101D;     /* Price, brand, rating */
--color-text-secondary: #747B84;   /* Sizes, review count */
--color-text-tertiary: #414249;    /* Emoji accents */

/* Backgrounds */
--color-bg-card-dark: #09101D;     /* Badge background */

/* Accents */
--color-notification: #E24949;     /* Rating emoji accent */

/* Structural */
--color-white: #FFFFFF;            /* Container, favorite button */
```

---

### Component Variations

**Horizontal Product Card** (Alternative Layout):
- Width: 343px (full content width)
- Height: 120px
- Layout: Row (Image left 120×120px + Content right)
- Use case: List view, cart items

**Product Card with Action Button** (Enhanced):
- Add "Add to Cart" button at bottom (44px height)
- Total height: 404px (360px + 44px)
- Button: #11BB8D background, Archivo 14px weight 600

**Compact Product Card** (Smaller):
- Width: 140px (from existing Mobile Cards)
- Height: 210px (from existing Mobile Cards)
- Use case: Compact grids, related products

---

<!-- END AI-FRIENDLY: E-commerce Components -->

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
  - Accent yellow: #FFC043 (для charts)
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
- Chart Components:
  - Spiral/Radial Timeline Chart (186×186px chart area)
  - Data points: 5×5px with borders
  - Colors: #4141E6 и #FFC043
  - Labels: Archivo 10px, center aligned
- Picker Components (Flutter Mobile):
  - Day Picker: 50px padding, 15px radius, border #7B61FF
  - Time Picker: states (Primary Selected, Dark, Disabled, Light)
  - Typography: Archivo 12px/14px
  - Spacing: 50px между элементами
- File Type & Dropdown Components (Flutter Mobile):
  - File Type Icons Grid: 34×40px items, spacing 10px, white background
  - Dropdown/Context Menu: 333px width items, 16px/8px padding
  - Destructive actions: #DA1414 (color-error)
  - Menu item variants: top rounded, middle flat, bottom rounded
- Segmented Control (Flutter Mobile):
  - Container: 375×41px, padding 16-17px/5px
  - Background track: #F4F6F9, border-radius 8px, padding 2px
  - Selected segment: white background, shadow, Archivo 13px weight 600
  - Layouts: 2 segments (spacing 10px), 3 segments (spacing 2px)
- Tabs Component (Flutter Mobile):
  - Tab bar: 375px width, white background, height 52px
  - Tab padding: 10px horizontal, spacing 8px
  - Optional elements: icon (20px), badge (20px height)
  - Badge variants: Active (#E24949 notification), Inactive (#414249)
  - Tab states: Active (2px border #23262B), Inactive (2px border #F4F6F9)
  - Typography: Archivo 14px weight 600, badge text 10px weight 600
- Mobile Layout Patterns (375px width)
- Spacing values: 5px, 10px, 15px, 20px, 50px, 70px
- Border radius values: 8px, 10px, 11px, 12px, 15px, 16px
- Typography: Archivo (10px-16px, weights 400-900, line-height 1.20-1.40)
- Colors:
  - Added #23262B (bg-dark-secondary) для picker items
  - Added #DA1414 (error) для destructive actions
  - Added #E24949 (notification) для активных уведомлений и badges
  - Added #EAEEF2 (bg-light-pressed) для pressed state светлых компонентов
  - Added rgba(17, 187, 141, 0.05) (bg-success-light) для success state background
  - Added rgba(218, 20, 20, 0.05) (bg-error-light) для error state background
- Textarea Component (Multi-line Input - Flutter Mobile):
  - Container: 375px width, padding 16px horizontal
  - Field: 135px height, padding 20px/15px, border-radius 15px
  - Typography: Label (Archivo 14px weight 600), Placeholder (14px weight 400 #747B84), Content (14-15px weight 400), Counter (10px weight 600)
  - Character counter: bottom-right position, "current/max" format (e.g., "256/1200"), changes to #E24949 when over limit
  - Icons: Close icon (24px), Check icon (24px for success state)
  - 9 States documented:
    1. Enabled: Background #F4F6F9, placeholder, counter "0/1200"
    2. Focus: Border 2px #09101D
    3. Pressed: Background #EAEEF2 (temporary state)
    4. Complete: With content, counter "256/1200", close icon
    5. Active-Typing: Border 2px #09101D, content, counter, close icon
    6. Incomplete: Placeholder, counter "0/1200", close icon
    7. Positive: Border 2px #11BB8D, background rgba(17,187,141,0.05), check icon
    8. Negative: Border 2px #DA1414, background rgba(218,20,20,0.05), counter "1322/1200" in error color, error message
    9. Disabled: All colors #D9DDE2
  - Validation patterns: Success (green border + light green bg), Error (red border + light red bg + error message)
  - Helper and error messages: Archivo 14px weight 400, positioned below field
- Snackbar Component (Flutter Mobile):
  - Container: 375px width, padding 16px all
  - Background: #09101D (color-bg-card-dark), border-radius 15px, padding 16px
  - Typography: Message (Archivo 14px weight 600, white), Action (Archivo 13px weight 600, white)
  - Elements: Avatar (56px container, 48px image), Icon (24px), Close button (20px icon), Action button (36px-44px height)
  - 6 Variants documented:
    1. Basic (text only): 311px message width
    2. With Icon: 24px icon, 235-271px message width, optional close button
    3. With Avatar: 56px avatar container, 203-239px message width
    4. With Action: 223-267px message width, 36-44px action button
    5. With Icon and Action: combines icon + text + action
    6. With Avatar and Action: 159-223px message width, avatar + action
  - Layout: Row layout with expanded text, 8px spacing between elements
  - Height: ~56px (text only), ~88px (with icon/avatar)
  - Usage guidelines: Bottom positioning, auto-dismiss 3-5s, stack vertically with 10px spacing
- Onboarding & Authentication Screens (Flutter Mobile):
  - New colors: #2E5AAC (primary-action), #FAFAFB (bg-light-input)
  - Common Elements:
    - Status Bar: 44px height, #09101D background
    - Pull Indicator: 40px × 3px, #D9DDE2, border-radius 100px
    - Progress Indicator: 5 segments, 3px height, #2E5AAC active, rgba(9,16,29,0.10) inactive
    - Back Button: 44px height, 24px icon, 12px border-radius
  - Screen 1 - Phone Number Input (375×499px):
    - Header: Title (Archivo 26px weight 700), Subtitle (18px weight 400 #414249)
    - Country Selector: 46px height, #FAFAFB background, 22×16px flag, 20px dropdown icon
    - Phone Input: 46px height, border 2px #2E5AAC (focus), Archivo 14px weight 600
    - Disclaimer: Archivo 12px weight 400, color #747B84
    - Next Button: 44px height, #2E5AAC background, Archivo 14px weight 600 white
  - Screen 2 - Registration Form (375×515px):
    - Header: "Get started" - Archivo 32px weight 700
    - Form Inputs: 4 fields (Full Name, Email, Confirm Email, Password)
    - Input specs: 46px height, border 1px #D9DDE2, placeholder Archivo 15px rgba(9,16,29,0.40)
    - Password Strength: 3 segments, 3px height, 10px spacing
    - Terms: Archivo 15px, #747B84 text, #11BB8D links
    - Create Button: 44px height, #11BB8D background
  - Screen 3 - Phone Verification OTP (375×444px):
    - Progress: 4 of 5 segments active
    - Header: Title (Archivo 26px weight 700), Subtitle with bold phone number
    - Code Fields: 4 fields, 46px height, #FAFAFB background, border 2px #2E5AAC (focus)
    - Helper text: "Didn't get the code?" with link #2E5AAC
  - Usage Notes: Flexible forms (add/remove fields), adjustable progress (3-7 steps), 375px width standard
- Financial Components (Cash Card - Flutter Mobile):
  - New colors: #D4FC79 (accent-green-light), #96E6A1 (accent-green), #98E7A0 (accent-green-tab), #9AE89F (accent-green-border), #D2FC7B (accent-green-button)
  - New gradient: linear-gradient(90deg, #D4FC79 0%, #96E6A1 100%) for Cash Card background
  - Cash Card Component:
    - Header: Title "Cash Card" (Archivo 24px weight 700), Avatar 40px with 2px green border (#9AE89F), Settings icon 24px
    - Card Section: Gradient background, 10px padding, 15px border-radius, 1px border rgba(0,0,0,0.05)
    - Logo: 60px × 60px, border-radius 15px, fit contain
    - Card Number: OCR-A 22px, letter-spacing 2.59px, shadow 0px 1px 1px rgba(0,0,0,0.40)
    - Card Details: Name (OCR-A 11px, letter-spacing 2px), Expiry (OCR-A 11px, letter-spacing 1px), Card logo 40×24px
  - Notification Item:
    - Container: full width, white background
    - Title: Archivo 14px weight 600 #09101D
    - Time: Archivo 11px weight 600 #23262B
    - Activate Button: 36px height, #D2FC7B background, Archivo 11px weight 600
  - Tabs Section:
    - Active Tab: Archivo 13px weight 600, color #98E7A0, 2px underline
    - Inactive Tabs: Archivo 11px weight 600, color #09101D
    - Height: 52px, spacing 20px
  - Cashback Section:
    - Item: 44×44px icon container, rgba(212,252,122,0.50) background, 15px border-radius
    - Percentage: Archivo 13px weight 600, centered
    - Empty Slot: 44×44px with 1px border #09101D, plus icon centered
  - Usage: Flexible cashback slots (add/remove), customizable card gradients, OCR-A font for authenticity
- E-commerce Components (Product Cards - Flutter Mobile):
  - NEW SECTION with AI-friendly markers for IDE navigation
  - Product Card - Vertical Layout (170×360px):
    - Container: 375px width, 30px vertical padding, white background, 30px border-radius
    - Cards Row: Horizontal scroll, 5px spacing, 16px horizontal padding
    - Card Structure: Image Section (~253px) + Content Section (~107px)
  - Image Section:
    - Image: 170×253px, fit cover, border-radius 5px
    - Favorite Button: 30×30px circle, white background, top-left overlay (10px padding)
    - Icon: ~16.8px heart icon
    - Status Badge: Bottom-left overlay (5px padding), "🔥 New"
      - Background: #09101D, border-radius 5px, padding 5px/3px
      - Typography: Archivo 9px (emoji weight 400, text weight 600), white color
    - Badge Variants: New, Sale, Trending, Limited (customizable)
  - Content Section (padding 10px/5px/10px/10px, spacing 5px):
    - Rating: "👌 4.8 (130)"
      - Emoji: 13px #E24949 (notification color)
      - Rating: Archivo 13px weight 600 #09101D
      - Count: Archivo 13px weight 400 #747B84
    - Price & Brand (spacing 2px):
      - Price: Archivo 14px weight 600 #09101D ("$96.50", "$159.20", "$350")
      - Brand: Archivo 14px weight 600 #09101D + emoji 14px weight 400 #414249 ("Nike 👟")
    - Sizes: "36 ・ 37・ 38・ 39"
      - Font: Archivo 13px weight 400 #747B84
      - Separator: " ・ " (bullet)
  - Layout Specifications:
    - Grid: 2 cards per row visible (170px + 5px + 170px ≈ 343px)
    - Scroll: Horizontal scroll for additional cards
    - Responsive: 375px width standard, 16px horizontal padding
  - Component Variations:
    - Horizontal Card: 343px×120px (list view)
    - With Action Button: 404px height (add "Add to Cart")
    - Compact Card: 140×210px (from existing Mobile Cards)
  - Usage Guidelines:
    - Use Cases: Product catalogs, marketplace listings, search results, category browsing
    - Flexible Elements: Badge (customizable/removable), Favorite button (auth-dependent), Sizes (replaceable with variants), Rating (hideable for new products), Price (supports discounts)
    - Accessibility: 44×44px touch targets, screen reader support, alt text for images
    - Performance: Image placeholders, lazy loading, caching, optimization (WebP/AVIF)
  - Cross-references: Links to [Mobile Card Components], [Badges], [Buttons]
  - AI-friendly markers: Keywords (product card, shopping, marketplace, e-commerce, retail, catalog), Component Type (Product Listings, Shopping Cards), Use Cases
- Layout patterns и Best practices

---

## Поддержка и контакты

- **Документация**: `/docs`
- **Компоненты**: `/components`
- **Примеры**: `/examples`
- **Вопросы**: Создайте issue в репозитории

---

**© 2025 Design System v5. Все права защищены.**
