# Popizdim: лендинг

Одностраничный сайт приложения [Popizdim](https://github.com/Asmadey/popizdim-app) (диктовка и озвучка для macOS).

Это статический сайт без сборки: `index.html`, папка `assets/`, `vercel.json`, `robots.txt`.

## Локальный просмотр

```bash
python3 -m http.server 8080
```

Откройте <http://localhost:8080>.

## Автодеплой на Vercel

Репозиторий готов к подключению через Git-интеграцию Vercel: после подключения каждый push в `main` выкатывается на боевой адрес, а каждая ветка и pull request получают свой предпросмотр.

1. На [vercel.com](https://vercel.com) выберите **Add New → Project** и импортируйте этот репозиторий (при первом разе разрешите Vercel доступ к GitHub).
2. **Framework Preset**: `Other`. **Build Command** и **Output Directory** оставьте пустыми, **Root Directory** оставьте корнем репозитория.
3. Нажмите **Deploy**. Настройки кэша и заголовков берутся из `vercel.json`.
4. Свой домен: **Project → Settings → Domains**.

После первого деплоя впишите абсолютные адреса в `index.html`, иначе превью в соцсетях не подхватит картинку:

```html
<meta property="og:image" content="https://ВАШ-АДРЕС/assets/banner.jpg" />
<meta property="og:url" content="https://ВАШ-АДРЕС/" />
```

Ссылка на скачивание ведёт на конкретную версию (`releases/download/v1.0.0/Popizdim_1.0.dmg`). При выходе новой версии её нужно обновить в `index.html`.
