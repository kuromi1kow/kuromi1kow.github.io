# Assylkhan Geniyat — academic website

Personal academic website built on the [Academic Pages](https://github.com/academicpages/academicpages.github.io) Jekyll template and hosted on GitHub Pages.

## Где что лежит

| Что | Файл |
|---|---|
| Имя, био в сайдбаре, email, LinkedIn, адрес сайта | `_config.yml` |
| Главная страница (About, News, Selected publications) | `_pages/about.md` |
| Публикации (по файлу на статью) | `_publications/*.md` |
| Research & Projects (по файлу на проект) | `_portfolio/*.md` |
| CV-страница | `_pages/cv.md` |
| PDF резюме | `files/Assylkhan_Geniyat_CV.pdf` |
| Меню сверху | `_data/navigation.yml` |
| Фото | `images/profile.jpg` (квадратное; путь задан в `_config.yml` → `avatar`) |

## Как опубликовать на GitHub Pages

1. Создай на GitHub **пустой публичный** репозиторий с именем `<твой-username>.github.io`.
2. В `_config.yml` замени `url` и `repository` (помечены `TODO`) на свой username.
3. Запушь эту папку в ветку `master`:
   ```bash
   git add -A
   git commit -m "My academic website"
   git remote add origin https://github.com/<твой-username>/<твой-username>.github.io.git
   git push -u origin master
   ```
4. На GitHub: **Settings → Pages → Source: GitHub Actions**. Через пару минут сайт будет на `https://<твой-username>.github.io`.

## Локальный просмотр

```bash
PATH="/opt/homebrew/opt/ruby/bin:$PATH" bundle install
PATH="/opt/homebrew/opt/ruby/bin:$PATH" bundle exec jekyll serve
```

Сайт откроется на http://localhost:4000. После правок в `_config.yml` сервер нужно перезапустить.
