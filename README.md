# Design System v5

Полноценная дизайн-система для создания современных, консистентных и масштабируемых интерфейсов.

## 📚 Документация

- **[Полная документация дизайн-системы](./DESIGN_SYSTEM.md)** - главный документ со всеми компонентами, цветами, типографикой и паттернами

## 🚀 Быстрый старт

### 1. Подключение стилей

```html
<!-- Подключите CSS переменные -->
<link rel="stylesheet" href="styles/variables.css">

<!-- Подключите компоненты -->
<link rel="stylesheet" href="styles/components.css">
```

### 2. Использование компонентов

```html
<!-- Пример кнопки -->
<button class="btn btn--md btn--primary">Click me</button>

<!-- Пример карточки -->
<div class="card">
  <h3>Card Title</h3>
  <p>Card content goes here</p>
</div>

<!-- Пример input -->
<div class="form-group">
  <label class="form-label">Email</label>
  <input type="email" class="input input--md" placeholder="example@email.com">
</div>
```

## 📁 Структура проекта

```
design-system-v5/
├── DESIGN_SYSTEM.md      # Полная документация дизайн-системы
├── README.md             # Этот файл
├── styles/
│   ├── variables.css     # CSS переменные (цвета, spacing, typography)
│   └── components.css    # Готовые компоненты
├── components/           # Будущие React/Vue компоненты
├── examples/
│   └── demo.html         # Демо-страница со всеми компонентами
└── docs/                 # Дополнительная документация
```

## 🎨 Основные возможности

### Цветовая система

- **Primary & Secondary** цвета для брендинга
- **Semantic** цвета (success, error, warning, info)
- **Neutral** палитра с 10 оттенками серого
- **Chart** цвета для визуализации данных
- **Градиенты** для специальных эффектов

### Компоненты

- **Buttons** - 4 варианта, 3 размера
- **Cards** - базовые, elevated, outlined, interactive
- **Inputs** - text, textarea, select
- **Forms** - layouts, labels, validation
- **Badges & Tags** - для статусов и тегов
- **Alerts** - success, error, warning, info
- **Avatars** - 6 размеров
- **Loaders** - spinners и skeleton loaders
- **Navigation** - main nav, sidebar
- **Tables** - с поддержкой сортировки и фильтрации

### Типографика

- **10 размеров** шрифтов (от 12px до 60px)
- **8 начертаний** (от thin до black)
- **5 line-heights** для разных контекстов
- **Готовые стили** для headings и body text

### Layout & Spacing

- **13-позиционная** spacing scale (от 0 до 96px)
- **8 вариантов** border-radius
- **Shadows** для cards, buttons, hovers
- **Grid & Flexbox** утилиты

## 🎯 Примеры использования

### Создание карточки продукта

```html
<div class="card card--interactive">
  <div class="flex items-center gap-4 mb-4">
    <div class="avatar avatar--lg">
      <img src="product.jpg" alt="Product">
    </div>
    <div>
      <h3 class="text-lg font-semibold">Product Name</h3>
      <p class="text-sm text-secondary">Category</p>
    </div>
  </div>

  <p class="text-base mb-4">Product description goes here...</p>

  <div class="flex items-center justify-between">
    <span class="badge badge--success">In Stock</span>
    <button class="btn btn--md btn--primary">Buy Now</button>
  </div>
</div>
```

### Форма с валидацией

```html
<form>
  <div class="form-group">
    <label class="form-label">Username</label>
    <input type="text" class="input input--md" placeholder="Enter username">
    <div class="form-helper">Choose a unique username</div>
  </div>

  <div class="form-group">
    <label class="form-label">Password</label>
    <input type="password" class="input input--md input--error">
    <div class="form-error">Password must be at least 8 characters</div>
  </div>

  <button type="submit" class="btn btn--md btn--primary">Submit</button>
</form>
```

### Alert сообщения

```html
<div class="alert alert--success">
  <strong>Success!</strong> Your changes have been saved.
</div>

<div class="alert alert--error">
  <strong>Error!</strong> Something went wrong.
</div>
```

## 🎨 Демо

Откройте `examples/demo.html` в браузере, чтобы увидеть все компоненты в действии.

## 📖 Использование CSS переменных

Все значения доступны как CSS переменные:

```css
.custom-element {
  /* Цвета */
  color: var(--color-primary);
  background: var(--color-bg-secondary);

  /* Spacing */
  padding: var(--space-4);
  margin-bottom: var(--space-6);

  /* Typography */
  font-size: var(--font-size-lg);
  font-weight: var(--font-weight-semibold);

  /* Border & Radius */
  border: var(--border-width-1) solid var(--color-border-primary);
  border-radius: var(--radius-md);

  /* Shadow */
  box-shadow: var(--shadow-base);

  /* Transitions */
  transition: var(--transition-base);
}
```

## 🌙 Dark Mode

Дизайн-система включает автоматическую поддержку темной темы:

```css
/* Автоматическое определение темы системы */
@media (prefers-color-scheme: dark) {
  /* Темная тема применится автоматически */
}

/* Или используйте класс */
<body class="dark">
  <!-- Темная тема -->
</body>
```

## 🔧 Кастомизация

### Переопределение переменных

```css
:root {
  /* Измените primary цвет */
  --color-primary: #FF6B6B;
  --color-primary-hover: #EE5A5A;

  /* Измените шрифт */
  --font-primary: 'Your Font', sans-serif;

  /* Измените spacing */
  --space-4: 1.25rem; /* Вместо 1rem */
}
```

## 📝 Принципы использования

### Для дизайнеров

1. Используйте цвета только из палитры
2. Следуйте spacing scale для отступов
3. Применяйте готовые компоненты
4. Документируйте новые паттерны

### Для разработчиков

1. Всегда используйте CSS переменные
2. Переиспользуйте классы компонентов
3. Следуйте BEM методологии для новых стилей
4. Тестируйте accessibility (WCAG 2.1)

### Для продуктовой команды

1. Ссылайтесь на компоненты в требованиях
2. Используйте консистентную терминологию
3. Предлагайте улучшения через GitHub Issues

## 🚧 Roadmap

- [ ] React компоненты
- [ ] Vue компоненты
- [ ] Figma файлы
- [ ] Storybook интеграция
- [ ] npm пакет
- [ ] TypeScript definitions
- [ ] Accessibility audit
- [ ] Animations library

## 📄 Лицензия

© 2025 Design System v5. Все права защищены.

## 🤝 Контрибьютинг

Contributions, issues и feature requests приветствуются!

## 📬 Контакты

- Документация: `./DESIGN_SYSTEM.md`
- Issues: GitHub Issues
- Демо: `examples/demo.html`

---

**Версия**: v5.0.0
**Последнее обновление**: 2025-11-19
