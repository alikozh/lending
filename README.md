# RECAPQ — сайт репетитора (alimath.site)

Статический сайт (HTML/CSS). Быстрый, SEO-оптимизированный, 3 языка (RU / KZ / EN).

## Структура
```
site/
├── index.html          Русская версия (главная)
├── kz/index.html       Казахская
├── en/index.html       Английская
├── assets/
│   ├── styles.css      Общий дизайн
│   ├── favicon.svg, favicon-32.png, apple-touch-icon.png
│   ├── icon-192.png, icon-512.png
│   ├── og-image.svg, og-image.png   Превью для репостов (1200×630)
│   └── photo.jpg       ← ПОЛОЖИТЕ СЮДА своё фото
├── site.webmanifest, robots.txt, sitemap.xml
```

## Посмотреть локально
Быстро:
```
open index.html
```
С сервером (чтобы работали пути `/assets/` и переключатель языков):
```
cd site && python3 -m http.server 8080
# затем открыть http://localhost:8080
```

## Что доделать перед публикацией
1. **Фото.** Положить своё фото как `assets/photo.jpg`, затем в трёх файлах
   (`index.html`, `kz/index.html`, `en/index.html`) заменить блок с плейсхолдером
   «Ваше фото» на строку (она уже написана рядом в комментарии):
   `<img src="/assets/photo.jpg" alt="Репетитор RECAPQ по математике и физике" width="330" height="400">`
2. **Отзывы.** В секции «Отзывы» сейчас примеры (помечены `TODO`). Замените на реальные —
   с настоящими именами и текстом. Фейковые отзывы вредят и доверию, и SEO.
3. **Контакты.** Проверьте Telegram `@recapq`, телефон `+7 707 570 79 93`, WhatsApp.

## Публикация (любой вариант — бесплатно)
- **Netlify / Vercel / Cloudflare Pages:** перетащить папку `site/` или подключить репозиторий.
  Указать корнем папку `site`. Привязать домен `alimath.site`.
- **GitHub Pages:** запушить содержимое `site/` в ветку, включить Pages.

Домен `alimath.site` уже прописан во всех SEO-тегах, sitemap и структурированных данных.

## После деплоя (SEO-запуск)
1. Google Search Console → добавить `alimath.site`, отправить `sitemap.xml`.
2. Проверить структурированные данные: search.google.com/test/rich-results
3. Проверить превью ссылки в Telegram/WhatsApp (og-image).
4. PageSpeed Insights для контроля скорости.
