# Diplomen.com

Готов статичен сайт. Няма build, сървър или инсталация — качваш файловете и работи.

**Хостинг:** Cloudflare Pages (проект `diplomen`), свързан с това репо — всеки push в `main` се деплойва автоматично на https://diplomen.com.

## Файлове

| Файл | Какво е |
|---|---|
| `index.html` | Целият сайт (снимки, лого, шрифтове и анимации са вътре) |
| `terms.html` | Общи условия |
| `privacy.html` | Политика за поверителност |
| `og-image.png` | Картинка при споделяне на линка |
| `favicon-32.png`, `favicon-512.png`, `apple-touch-icon.png` | Иконки |
| `robots.txt`, `sitemap.xml` | За Google |
| `CNAME` | Домейн за GitHub Pages (`diplomen.com`) |
| `.nojekyll` | Казва на GitHub Pages да не обработва файловете |

## 1. Качване в GitHub

1. github.com → **New repository** → име `diplomen-site` → **Public** → Create.
2. **Add file → Upload files** → провлачи всички файлове от тази папка (включително `.nojekyll` и `CNAME`) → **Commit changes**.

## 2. Хост — избери един вариант

**A) GitHub Pages (безплатно)**
1. Repository → **Settings → Pages**.
2. Source: **Deploy from a branch** → Branch: `main` / `(root)` → Save.
3. След 1–2 минути сайтът е на `https://<user>.github.io/diplomen-site/`.

**B) Netlify или Vercel (безплатно)**
1. netlify.com или vercel.com → **Add new project → Import from GitHub** → избери `diplomen-site`.
2. Build command: празно. Publish directory: `/` → Deploy.

## 3. Домейн diplomen.com

**GitHub Pages:** Settings → Pages → Custom domain: `diplomen.com` → Save → отметни **Enforce HTTPS**.
При регистратора на домейна добави DNS записи:

| Тип | Име | Стойност |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | `<user>.github.io` |

**Netlify / Vercel:** Domains → Add `diplomen.com` → следвай DNS инструкциите им. Изтрий файла `CNAME`, ако не ползваш GitHub Pages.

DNS промените влизат в сила от няколко минути до 24 часа.

## Преди публикуване — попълни

- В `terms.html` и `privacy.html`: фирма, ЕИК, адрес, имейл (полетата в жълто). Добре е юрист да ги прегледа.
- Ако домейнът не е `diplomen.com`: смени го в `CNAME`, `robots.txt`, `sitemap.xml` и в мета таговете на `index.html` (редактира се в дизайн проекта и се експортира отново).

## След публикуване

- Провери как изглежда линкът при споделяне: https://developers.facebook.com/tools/debug/
- Добави сайта в Google Search Console и подай `sitemap.xml`.

## Контакти в сайта

Instagram и Messenger: `diplomen_` · Viber и WhatsApp: +359 887 239 978
