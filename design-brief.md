# Stilliano Designer Landing — Design Brief

Аналог design.md из styles.refero.design. Канон визуального языка для дизайнерского лендинга Стиллиано. Используется как промт для генерации (Magic MCP, redesign-skill, ui-ux-pro-max) и как контрольный документ при ручной правке.

Референсы-основа: AEROSTEP (премиальные лестницы), FORMA CASA (премиум-кухни), ЭСТ (загородные дома). Все три - российский премиум-минимализм 2025.

---

## 1. Концепция и тон

**Что:** Партнёрская программа Стиллиано для дизайнеров интерьера. Не каталог кухонь, не B2C-промо.
**Кому:** Дизайнер интерьера, который ведёт частных клиентов. Хочет зарабатывать на отделке и мебели не через скрытые откаты, а через прозрачный процент.
**Доминанта Hero:** Цифры/заработок/уверенность. Не «креатив»/«неуведение клиента»/«эмоция».
**Тон:** Фактический, спокойный, тёплый. Без воодушевления, без агрессии, без инфоцыганщины.
**Стиль копи:** Описательно-фактический (X — современное Y, за счёт Z). Без рифм, без обращений «Вы рисуете - мы воплощаем». Ключевые смыслы выделяются **жирным**, не курсивом.

---

## 2. Семья дизайна

**Стилевая семья:** Warm Russian Premium Minimal 2025.
**Соседи в семье:** AEROSTEP, FORMA CASA, ЭСТ, premium-сегмент архитектурных бюро Москвы.
**НЕ-семья:** Apple bento, glassmorphism, neumorphism, editorial luxury (Cereal/Kinfolk), brutalism, dark mode SaaS, Tilda-default.

### Тренды 2025, которые забираем

1. Тёплая ivory-палитра (не белая, не grey)
2. Брутально-крупный гротеск Hero H1 (80-120px) на спокойном фоне
3. CAPS pre-title 11-13px с большим letter-spacing над H1
4. Pill-shaped CTA с круглой иконкой-стрелкой
5. Floating-карточки поверх Hero-фото с микро-доказательством («+150 проектов», «5 млн ₽»)
6. Соц-доказательство с маленькими аватарами в Hero
7. Большие радиусы 20-24px на карточках
8. Иконки тонкими линиями в кружках, монохром
9. Тёмный финальный CTA-блок поверх blurred-фото
10. Stat-row 3-4 цифры под Hero и в блоке доверия
11. Cinematic фото в тёплом свете (натуральный продукт, не AI)

### Антитренды (что НЕ делаем)

- Центрированный текст в крупных блоках (только мелкие подписи)
- Gradient-фоны, gradient-mesh
- Glassmorphism, neumorphism
- Hero с центрированным текстом без фото
- Карусели проектов мелкими превью
- Эмодзи в копи и заголовках
- Длинное тире (—), только дефис (-)
- Серый/синий «корпоративный» сток-цвет
- AI-сгенерированные лица команды
- Trustpilot/G2 badges (это SaaS-маркер)
- Курсив для эмоционального акцента — заменяется жирным

---

## 3. Палитра

CSS-переменные:

```css
:root {
  /* Базовый фон */
  --bg: #F5F0E6;        /* ivory — основной фон */
  --bg-2: #EFE8D8;      /* cream — фон карточек */
  --bg-warm: #ECE4D2;   /* linen — вторичный блок */
  --bg-dark: #2A211B;   /* deep coffee — footer-CTA, не чистый чёрный */

  /* Текст */
  --ink: #2A211B;       /* deep coffee — основной текст */
  --ink-2: #5A4D42;     /* warm grey — secondary */
  --ink-3: #9A8D80;     /* muted — pre-title, captions */

  /* Акценты */
  --accent-deep: #5C3A1A;  /* deep brown — CTA primary */
  --accent: #8A6A44;       /* deep gold — иконки стрелок, акценты */
  --accent-2: #A8835A;     /* warm gold — hover, мелкие detail */

  /* Линии */
  --line: rgba(31, 24, 18, 0.08);
  --line-strong: rgba(31, 24, 18, 0.16);
}
```

**Логика:** ivory-фон + deep brown CTA + warm gold акценты. Чистого чёрного нет нигде. Каждый «тёмный» элемент имеет коричневый подтон.

**Композиция как FORMA CASA**, но чёрный (#000) заменён на coffee (#2A211B) и CTA-таблетка коричневая (#5C3A1A) с золотой стрелкой (#A8835A).

---

## 4. Типографика

Шрифт: **Manrope variable 300-800**.

```
Pre-title    12px / 600 / letter-spacing 0.32em / uppercase / color: --ink-3
Hero H1      96-104px desktop, 56px mobile / 700 / line-height 1.02 / letter-spacing -0.02em
H2 секций    56-64px / 700 / line-height 1.08
H3 карточек  22-24px / 600 / line-height 1.25
Body large   19px / 400 / line-height 1.55
Body         17px / 400 / line-height 1.6
Small/caption 14px / 500 / line-height 1.4
Stat number  72-96px / 700 / Manrope tabular-nums
```

**Акценты:**
- В заголовках выделяем **жирным** (weight 800 vs основной 700) ключевое слово/выгоду
- Курсив НЕ используем
- Цветовой акцент на одном слове — color: --accent-deep

Пример: «Партнёрская программа Стиллиано — для дизайнеров, которые **зарабатывают на отделке**, а не теряют клиента».

---

## 5. Сетка и пропорции

```
max-width контейнера: 1280px
side padding: 56px (desktop) / 32px (tablet) / 24px (mobile)
vertical padding между секциями: 120-160px (desktop) / 80px (mobile)
inner gap внутри блока: 24-32px
column gap в grid: 24px
```

**Никакого full-width контента, кроме Hero и footer-CTA.** Всё остальное — в контейнере 1280px с боковыми отступами.

---

## 6. Карточный язык

```css
.card {
  background: #FFFFFF; /* или --bg-2 для второго слоя */
  border: 1px solid var(--line);
  border-radius: 24px; /* крупные карточки */
  padding: 32px;
  box-shadow: none; /* на тёплом фоне shadow выглядит грязно */
}

.chip {
  background: var(--bg-2);
  border: 1px solid var(--line);
  border-radius: 14px;
  padding: 12px 16px;
}
```

Большие радиусы — обязательный признак семьи (AEROSTEP/FORMA/ЭСТ все на 20-24px).

---

## 7. Кнопки и CTA

```css
/* Primary — pill с круглой стрелкой */
.cta-primary {
  display: inline-flex;
  align-items: center;
  gap: 12px;
  padding: 16px 22px 16px 28px;
  background: var(--accent-deep); /* #5C3A1A */
  color: var(--bg);
  border-radius: 999px;
  font: 600 15px Manrope;
  letter-spacing: 0.005em;
  transition: transform 250ms ease, background 250ms ease;
}
.cta-primary:hover {
  transform: translateY(-1px);
  background: #6E4520;
}
.cta-primary__arrow {
  width: 32px; height: 32px;
  background: var(--accent-2); /* warm gold #A8835A */
  border-radius: 999px;
  display: inline-flex; align-items: center; justify-content: center;
}

/* Secondary — текст + play-иконка слева */
.cta-secondary {
  display: inline-flex;
  align-items: center;
  gap: 12px;
  padding: 12px 0;
  font: 500 15px Manrope;
  color: var(--ink-2);
}
.cta-secondary__icon {
  width: 38px; height: 38px;
  border-radius: 999px;
  border: 1px solid var(--line-strong);
  display: inline-flex; align-items: center; justify-content: center;
}
```

CTA всегда парой: primary (brown pill с золотой стрелкой) + secondary (play-icon + текст).

---

## 8. Иконки

- Стиль: **outline 1.5px stroke**, не filled
- Размер базовый: 20-22px
- Помещаются в кружок 40-44px с бордером 1px --line
- Цвет stroke: --ink-2 (warm grey)
- Никаких цветных fill, никаких градиентов

Источник: Lucide или Phosphor outline. Не использовать Material Icons filled, не использовать эмодзи.

---

## 9. Hero — универсальный паттерн

Поддерживаем 3 раскладки на выбор. **Текст обязан читаться** в любой:

### Вариант A — Full-bleed фото (AEROSTEP)
- Frame-плейсхолдер на всю ширину окна, высота 720-820px
- На фото — тёмный градиент-оверлей слева (linear-gradient(90deg, rgba(42,33,27,0.78) 0%, rgba(42,33,27,0) 60%))
- Текст слева в контейнере, цвет --bg
- Floating-карточка справа поверх фото (white card, radius 24px)

### Вариант B — Асимметрия (FORMA CASA)
- Левая колонка 50% — текст на --bg
- Правая колонка 50% — frame-плейсхолдер с radius 24px
- Внизу под фото справа — chip с количеством проектов и аватарами

### Вариант C — Split 50/50
- Левая колонка — заголовок + цифра-доминанта
- Правая колонка — фото на всю высоту Hero, без скругления

Любой вариант содержит:
- CAPS pre-title над H1 (12px, --ink-3)
- H1 с выделенным жирным ключевым словом
- Sub-headline 1-2 строки, max-width 540px
- Pair CTA (primary + secondary)
- Stat-row внизу Hero (3-4 чипа со ключевыми параметрами программы)

---

## 10. Floating-карточки в Hero

Размещаются поверх фото или на стыке Hero и следующего блока.

```
[ icon ]  Выплачено дизайнерам в 2024
          5 млн ₽
          [ +N маленькие аватары ]
```

Структура:
- Width: 280-340px
- Background: #FFFFFF
- Radius: 24px
- Padding: 20px 24px
- Border: 1px solid --line
- Контент: иконка-кружок + 2 строки + аватары/число
- box-shadow: 0 12px 32px rgba(31,24,18,0.06) — единственное место где shadow допустим

---

## 11. Stat-row под Hero

4 чипа в одну строку:

```
[icon] Прозрачная   [icon] Выплата       [icon] Закрепление    [icon] Без скрытых
       комиссия            до 14 дней           клиента               откатов
       10-15%              после монтажа        в CRM                  и подарков
```

Каждый чип:
- Иконка-кружок 36px слева
- 2 строки текста справа (label 14px / value 16px weight 600)
- Без бордера, разделители — вертикальная линия --line высотой 36px между чипами

---

## 12. Footer-CTA

Полноширинный блок 200px высоты:
- Background: --bg-dark (#2A211B) либо blurred-photo с overlay rgba(42,33,27,0.85)
- H2 слева 40-48px, color: --bg
- Sub слева 17px, color: rgba(245,240,230,0.7)
- CTA-primary справа
- Padding: 80px 56px

---

## 13. Motion

- Все transitions: 250ms ease (стандарт), 200ms для микро-hover
- Hover на CTA: translateY(-1px) + смена фона
- Hover на карточке проекта: translateY(-2px), shadow появляется
- Fade-in блоков при скролле: opacity 0→1, translateY(20px → 0), 600ms ease, intersection observer
- НЕ slide-in огромные, НЕ parallax на фото (выглядит дёшево)
- Все cubic-bezier — `cubic-bezier(0.22, 1, 0.36, 1)` (custom ease-out, более премиум чем стандартный ease)

---

## 14. Фрейм-плейсхолдеры (пока нет фото)

Реальные фото Виталий подгрузит позже. Пока — фреймы:

```html
<div class="frame frame--hero">
  <!-- placeholder: cinematic фото кухни Стиллиано, тёплый свет -->
  <span class="frame__label">FRAME · HERO · cinematic kitchen, warm light</span>
</div>
```

```css
.frame {
  background: linear-gradient(135deg, var(--bg-warm) 0%, var(--bg-2) 100%);
  border: 1px dashed var(--line-strong);
  border-radius: 24px;
  display: flex; align-items: center; justify-content: center;
  color: var(--ink-3);
  font: 500 13px Manrope;
  letter-spacing: 0.16em;
  text-transform: uppercase;
  min-height: 320px;
}
.frame--hero { min-height: 720px; border-radius: 0; }
.frame--card { min-height: 280px; border-radius: 24px; }
.frame--small { min-height: 180px; border-radius: 14px; }
```

Подписи плейсхолдеров:
- `FRAME · HERO · cinematic kitchen, dark warm`
- `FRAME · PROJECT · realized kitchen Moscow`
- `FRAME · FACTORY · CNC machine`
- `FRAME · TEAM · workshop master, warm portrait`
- `FRAME · SHOWROOM · interior shot`
- `FRAME · MATERIAL · close-up texture`

---

## 15. Промт для генератора (готов к копи-пасте)

Скармливай это в Magic MCP, redesign-skill или ui-ux-pro-max:

```
Premium Russian B2C designer-partnership landing page in the "Warm Russian Premium Minimal 2025" family.
Design family neighbors: aerostep.ru (premium staircases), formacasa.ru (premium kitchens), est-stroy.ru (premium country homes).
Audience: interior designers leading private clients (premium kitchen partnership program).

Style: warm minimal, editorial, factual, calm. Not luxury-editorial (Cereal/Kinfolk), not bento, not glassmorphism, not brutalism, not dark mode.

Palette (strict):
- Background: #F5F0E6 ivory primary, #EFE8D8 cream secondary, #ECE4D2 linen accent
- Text: #2A211B deep coffee (never pure black), #5A4D42 warm grey, #9A8D80 muted
- Accents: #5C3A1A deep brown for primary CTA, #8A6A44 deep gold for icons, #A8835A warm gold for hover
- No grey, no blue, no pure black, no white. Everything has warm undertone.

Typography:
- Font: Manrope variable 300-800
- Hero H1: 96-104px desktop, weight 700, line-height 1.02, letter-spacing -0.02em
- One key word in H1 bolded (weight 800), not italicized. Italics not used anywhere.
- Pre-title 12px CAPS letter-spacing 0.32em over each section title
- Body 17px line-height 1.6

Layout:
- Container 1280px max-width, 56px side padding
- 120-160px vertical padding between sections
- Card border-radius 24px, chip 14px
- No drop shadows except on floating cards in Hero

CTA:
- Pill-shaped, padding 16px 22px 16px 28px
- Background: #5C3A1A deep brown (not black)
- Circular gold (#A8835A) arrow icon 32px on the right
- Hover: translateY(-1px)

Hero composition: choose one of three patterns (text must remain readable):
A) Full-bleed photo with left-side dark gradient overlay, text on photo
B) Asymmetric: text left 50%, photo right 50% with radius 24px
C) Split 50/50

Hero must include:
- CAPS pre-title over H1
- H1 with one bolded key word — factual descriptive headline, not emotional
- Sub-headline 1-2 lines max 540px
- Primary CTA (brown pill) + Secondary CTA (text + circular play icon)
- Floating white card over photo with micro-proof ("Paid to designers in 2024: 5 mln ₽" with mini avatars)
- Stat row below Hero (4 chips with key program parameters separated by thin vertical lines)

Icons: 1.5px stroke outline only (Lucide / Phosphor outline style), in 40px outlined circles, no fills, no colors.

Footer CTA: full-width 200px tall block, deep coffee background OR blurred photo with overlay, H2 left + CTA right.

Avoid: centered text in major blocks, gradients on backgrounds, glassmorphism, emojis in copy, AI-generated team faces, em-dash, carousels with tiny thumbnails, Apple bento grid, Trustpilot badges.

Motion: 250ms ease transitions, custom cubic-bezier(0.22, 1, 0.36, 1) for hovers, subtle fade-in on scroll, no parallax.

Sections to render (in order, from existing structure-v1.md):
1. Hero
2. Калькулятор комиссии 10-15%
3. Выплаты (история выплат, 5 млн ₽ за 2024)
4. Этапы работы дизайнера в программе
5. Фабрика и производство
6. Материалы
7. Гарантии (фокус на закреплении клиента в CRM)
8. Команда
9. Шоу-рум
10. С кем работаем (логотипы дизайн-студий)
11. Финальный CTA

Use frame placeholders for all images — real photos will be added later.
```

---

## 16. Какие скиллы вызывать на следующем шаге

В порядке применения:

1. **redesign-skill** на `designer-prototype-v4.html` с этим брифом на входе → перевёрстка v4 под канон.
   - Команда: `/redesign-skill` → передать путь к v4 + содержимое раздела 15 этого файла.
   - Применяет: цветовые токены, типографику, сетку, карточный язык, motion.

2. **ui-ux-pro-max** для дополнительных идей по конкретным блокам (если v4 не покрывает все 11):
   - Команда: `python ~/.claude/skills/ui-ux-pro-max/scripts/search.py --design-system "premium kitchen partnership program warm minimal russian"`
   - Применяет: дополняет недостающие паттерны под нашу семью.

3. **Magic MCP** под конкретные сложные блоки (Hero с floating-карточкой, stat-row, footer-CTA):
   - Использовать ТОЛЬКО с плейсхолдерами по [[feedback_magic_mcp_no_real_data]]
   - Промт строить на разделе 15 + конкретный блок.

4. **taste-skill** для финального анти-slop аудита перед показом руководству.
   - Прогоняет на: AI-default паттерны, generic иконки, glassmorphism residue, неконсистентность палитры.

5. **emil-design-eng** (опционально) для тонкой моторики hover/motion — если после redesign motion остаётся скучным.

---

## 17. Источники и связь

- Структура: [[structure-v1]] — 11 блоков
- Доминанта Hero: [[feedback_designer_landing_dominant_offer]] — цифры/заработок/уверенность
- Заголовки: [[feedback_descriptive_factual_headlines]] — описательно-фактический стиль
- Курсив не используем: уточнение Виталия 2026-06-15
- Магия с плейсхолдерами: [[feedback_magic_mcp_no_real_data]]
- Анти-AI-slop в копи: humanizer skill + ai-clone/voice/stop-words.md
- Палитра-канон в памяти: [[stilliano-designer-landing-state]]

Версия: 1.0 (2026-06-15). Канон визуального языка. Изменения — через явное согласование с Виталием.
