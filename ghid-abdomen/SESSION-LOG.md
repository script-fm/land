# Session Log: Ghid Abdomen Landing Page

**Дата:** 2 февраля 2026
**Цель:** Подготовить лендинг для публикации в GetCourse

---

## Что было сделано

### 1. Создан репозиторий для хостинга изображений

**Репозиторий:** https://github.com/script-fm/land

**Загруженные изображения:**
```
ghid-abdomen/images/
├── ghid-cover.png      — обложка гида
├── case-1.jpg          — фото трансформации 1
├── case-2.jpg          — фото трансформации 2
├── case-3.jpg          — фото трансформации 3
├── video-mockup.png    — mockup видео бонуса
├── gift-box.png        — иконка подарка
└── gift-training.png   — изображение тренировки
```

**Базовый URL для изображений:**
```
https://raw.githubusercontent.com/script-fm/land/main/ghid-abdomen/images/
```

---

### 2. Обновлён index.html

Все относительные пути к изображениям (`images/...`) заменены на абсолютные URL с GitHub.

**Файл:** `index.html`

---

### 3. Создан getcourse-block.html

Отдельный HTML-файл для вставки в конструктор GetCourse.

**Файл:** `getcourse-block.html`

**Особенности:**
- Все CSS-классы изолированы через префикс `.ga-*` (ghid-abdomen)
- Стили не влияют на системные блоки GetCourse
- CSS-переменные: `--ga-bg`, `--ga-accent`, etc.
- Весь контент обёрнут в `.ga-wrapper`

---

### 4. Интегрированы виджеты GetCourse

**Виджеты форм:**
- **Gratuit (бесплатный):** widget ID `1556272`
- **VIP:** widget ID `1556273`

**Реализация:**
- Виджеты GetCourse — это inline-формы, не popup
- Создана своя модальная система (`.ga-modal-overlay`, `.ga-modal`)
- При клике на кнопку открывается модальное окно с формой внутри

**Кнопки:**
- `Alege gratuit` → открывает модалку с формой бесплатного пакета
- `Alege VIP` → открывает модалку с формой VIP пакета

**Функции:**
- `gaOpenModal('free')` / `gaOpenModal('vip')` — открыть модалку
- `gaCloseModal('free')` / `gaCloseModal('vip')` — закрыть модалку
- Закрытие по клику на overlay или Escape

---

## Структура файлов

```
ghid-abdomen/
├── index.html              — основной лендинг (standalone)
├── getcourse-block.html    — версия для GetCourse (изолированные стили + модалки)
├── SESSION-LOG.md          — этот файл
└── images/                 — локальные изображения (backup)
    ├── ghid-cover.png
    ├── case-1.jpg
    ├── case-2.jpg
    ├── case-3.jpg
    ├── video-mockup.png
    ├── gift-box.png
    └── gift-training.png
```

---

## Как использовать getcourse-block.html

### Вариант 1: Один HTML-блок (рекомендуется)
1. Скопировать весь код из `getcourse-block.html`
2. В GetCourse создать страницу → добавить блок "HTML-код"
3. Вставить код
4. Сохранить и опубликовать

### Вариант 2: Отдельные блоки
Если нужно добавить другие блоки между секциями:
1. Скопировать `<style>...</style>` в первый HTML-блок
2. Копировать нужные секции (`.ga-hero`, `.ga-author`, etc.) в отдельные блоки
3. Модалки и скрипты — в последний блок

---

## GitHub репозиторий

**URL:** https://github.com/script-fm/land

**Файлы в репозитории:**
- `ghid-abdomen/index.html`
- `ghid-abdomen/getcourse-block.html`
- `ghid-abdomen/images/*`

**Прямые ссылки:**
- Landing: https://raw.githubusercontent.com/script-fm/land/main/ghid-abdomen/index.html
- GetCourse block: https://raw.githubusercontent.com/script-fm/land/main/ghid-abdomen/getcourse-block.html

---

## Важные заметки

1. **Токен GitHub** использовался для push — рекомендуется деактивировать после сессии
2. **Изображения** хостятся на GitHub Raw — бесплатно, но есть лимиты трафика
3. **Виджеты GetCourse** загружаются с `fitnessmama.school` — требуется активная подписка

---

## Контакты

При вопросах обращаться к команде разработки.
