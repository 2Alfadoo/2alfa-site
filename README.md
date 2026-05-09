# 2Alfa d.o.o. — Corporate Website

Сайт под верификацию Apple Developer Program. Двуязычный: EN (default) + SL.

## Структура

```
site/
├── index.html         — Home (EN)
├── about.html         — About (EN)
├── terms.html         — Terms & Conditions (EN)
├── privacy.html       — Privacy Policy (EN)
├── styles.css         — общие стили
├── README.md          — этот файл
├── assets/
│   └── favicon.svg
└── sl/
    ├── index.html     — Domov (SL)
    ├── about.html     — O nas (SL)
    ├── terms.html     — Splošni pogoji poslovanja (SL)
    └── privacy.html   — Politika zasebnosti (SL)
```

## Реквизиты, подставленные в сайт

| Поле | Значение |
|---|---|
| Юр. название | 2Alfa, družba z omejeno odgovornostjo |
| Краткое название | 2Alfa d.o.o. |
| Адрес | Podbreg 32, 4280 Kranjska Gora, Slovenija |
| Davčna št. (VAT) | SI37315374 |
| Matična št. | 8144290000 |
| Email | info@2alfa.org |
| Телефон | +386 40 357 188 |
| Директор | Andrej Alferov |

Эти данные стоят на всех 8 страницах (4 EN + 4 SL).

## Языковой переключатель

В шапке справа от навигации — `EN | SL`. Переключение работает попарно: с `index.html` ↔ `sl/index.html`, и т.д. Активный язык подсвечен.

## Фотографии

Сейчас 3 стоковых фото с Unsplash (бесплатные, hotlink стабильный). Для production-сайта компании **лучше свои фото** — реальные апартаменты, рабочее место в салоне. Это сильно повышает доверие Apple к "functional, content-rich website".

Замена: в `index.html` и `sl/index.html` найди три блока `<div class="service-image" style="background-image: url('...');">` и поменяй URL на свои.

## Как разместить

### На 2alfa.org (рекомендую)

У тебя домен уже есть. Залей содержимое папки `site/` на хостинг.

Если хостинга нет — **GitHub Pages**:
1. Создай публичный репозиторий, например `2alfa-site`
2. Загрузи туда содержимое папки `site/` (включая папку `sl/`)
3. Settings → Pages → Source: `main` branch / `(root)`
4. В DNS у регистратора пропиши CNAME на `<username>.github.io`
5. Settings → Pages → Custom domain: `2alfa.org`

Альтернативы для статики: Cloudflare Pages, Netlify, Vercel — бесплатные, поддерживают свой домен, drag-and-drop.

## Когда сайт онлайн

1. Открой `https://2alfa.org` — проверь, грузится с любого устройства
2. Кликни по всем ссылкам в шапке и в футере — все должны открываться без 404
3. Переключи на словенский (`SL`), проверь что все 4 SL-страницы открываются
4. На странице About — проверь, что таблица реквизитов заполнена правильно
5. Только потом — Resubmit в Apple с кейс-номером `102888601075` и enrollment `M7X8KGJNYG`

## Чего касаются требования Apple — где это в сайте

| Apple требует | Где это |
|---|---|
| Names matching enrollment | Везде в шапке/футере: **2Alfa d.o.o.** |
| Addresses | `index.html#contact`, `about.html` (таблица), `privacy.html`, `terms.html` |
| Phone numbers | Те же 4 страницы (EN и SL) |
| Terms and conditions | `terms.html` (10 разделов, EN + SL) |
| About tab | `about.html` + ссылка в главной навигации |
| Functional, content-rich | 4 страницы × 2 языка = 8 страниц контента |
| Domain matches org name | 2alfa.org → 2Alfa d.o.o. ✓ |

## Юридическая оговорка

Я **не юрист**. Terms / Privacy — разумный бойлерплейт под GDPR + словенское право (ZVOP-2) с привязкой к трём направлениям компании. Перед финальной публикацией прогони хотя бы беглым взглядом через бухгалтера или юриста — особенно:

- **eTurizem** — реальный порядок регистрации гостей в полиции
- **Сроки хранения данных** (5 лет — стандартная цифра, может отличаться у тебя)
- **Slovenščina в legal-текстах** — перевод качественный, но юридическая терминология лучше всего проверяется носителем языка / лицом, знакомым с местной практикой

Privacy Policy для самой ZTL Italia на GitHub — отдельный документ, его не трогаем; на сайте на него стоит явная ссылка с уточнением приоритета в части app-specific вопросов.
