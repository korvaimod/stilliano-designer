# IMPLEMENTATION STATUS

Обновлено 2026-06-19 после полного прогона playbook'а сайта за 1-3 дня. Файл: `claude-full-v1.html` (1465 строк, все 11 секций сверстаны).

## Свод

| # | Секция | Статус | Скрин |
|---|---|---|---|
| 01 | Header + Hero | ✅ implemented + verified (1485×1059) | `_playwright/shots/final-hero.png` |
| 02 | Комплексная реализация | ✅ implemented + verified | `_playwright/shots/sec-02-complex.png` |
| 03 | Калькулятор дохода (с JS) | ✅ implemented + verified | `_playwright/shots/sec-03-calc.png` |
| 04 | Гарантии и обязательства | ✅ implemented + verified | `_playwright/shots/sec-04-guarantees.png` |
| 05 | Как проходит работа | ✅ implemented + verified | `_playwright/shots/sec-05-workflow.png` |
| 06 | Производственная база | ✅ implemented + verified | `_playwright/shots/sec-06-production.png` |
| 07 | Материалы и комплектующие | ✅ implemented + verified | `_playwright/shots/sec-07-materials.png` |
| 08 | Партнёры и проекты | ✅ implemented + verified | `_playwright/shots/sec-08-partners.png` |
| 09 | Шоурум | ✅ implemented + verified | `_playwright/shots/sec-09-showroom.png` |
| 10 | Команда проекта | ✅ implemented + verified | `_playwright/shots/sec-10-team.png` |
| 11 | Финальный оффер + футер | ✅ implemented + verified | `_playwright/shots/sec-11-final.png` |

## Фиксы 2026-06-19 (по playbook'у)

- Hero overflow починен: H1 размер уменьшен до `clamp(40px, 3.4vw, 56px)`, колонки `1.05fr / 1fr`, gap`s сужены, min-height пересчитан. 1485×1059 помещает Hero + stats полностью.
- Trust-badge из Hero убран (правило `max 4 элемента в Hero`)
- Em-dash + en-dash sweep: 9 мест → 0 (sed по всему HTML)
- `window.addEventListener('scroll', ...)` заменён на IntersectionObserver-sentinel (taste-skill §5.D)
- Hero PNG 855KB → WebP 50KB (sharp). `<picture>` с srcset 800/1600 + `<link rel="preload">` + `fetchpriority="high"`
- Manrope сужен до 400/600/700 weights (вместо 6 вариантов)

## Lighthouse (desktop, 2026-06-19 после оптимизации)

- Performance: **68** (was 63 до WebP)
- Accessibility: 89
- Best Practices: 96
- SEO: 100
- LCP: **3.4s** (was 6.9s)
- CLS: 0.001
- TBT: 0ms
- FCP: 2.3s

JSON отчёты: `_playwright/shots/lighthouse.json` (до), `_playwright/shots/lighthouse2.json` (после).

## Что осталось (до production-ready)

- [ ] Self-host Manrope (`.woff2` локально) - выведет Perf в 90+
- [ ] Mobile-адаптив пройти отдельно (правило VIEWPORTS.md: desktop утвердить, потом mobile)
- [ ] Accessibility доводка: color-contrast, label associations (89 → 95+)
- [ ] Реальные фото проектов вместо frame-плейсхолдеров (08, 07, 09, 02)
- [ ] Реальные фото команды (08, 10)
- [ ] Видеотур производства (06)
- [ ] Фото шоурума (09)
- [ ] Карта Yandex Maps вместо placeholder (11)
- [ ] **Деплой** (Cloudflare Pages / Vercel / Yandex Cloud) - ждёт явной команды
- [ ] **PostHog + Yandex Metrica + Resend** - ждёт явной команды
- [ ] Метрика → AmoCRM → Директ (мостик качества лида)

## Связано

- `mastery/conversion/site-1-3-days-playbook.md` - playbook процесса (сборки лендингов 1-3 дня)
- `_playwright/shot.js` - скрипт screenshot-цикла
- `design-brief.md` - канон визуального языка
- `CONTENT_FINAL.md` - канон копи
