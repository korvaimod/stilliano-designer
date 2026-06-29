# VIEWPORTS FOR VISUAL COMPARISON

## Desktop source-of-truth

Для первого этапа сравнивать header + hero с PNG при viewport:

`1485 x 1059`

Именно такой размер у файла:

`design-source-of-truth/01-hero-approved.png`

## Desktop implementation viewport

При локальной проверке в браузере выставлять:

- width: `1485px`
- height: `1059px`
- device scale factor: `1`

## Mobile viewport

Для мобильной проверки использовать:

- width: `390px`
- height: `844px`

## Tablet viewport

Дополнительно:

- width: `768px`
- height: `1024px`

## Правило

Сначала довести desktop 1485x1059.  
Только после утверждения desktop делать mobile/tablet адаптив.

Не сравнивать макет на случайной ширине браузера.
