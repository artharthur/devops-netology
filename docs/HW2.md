# Задание 2 — Теги

## Что сделано
- Создан **лёгковесный** тег `v0.0` на текущем коммите и запушен в оба удалённых репозитория.
- Создан **аннотированный** тег `v0.1` (с сообщением) и запушен в оба удалённых репозитория.

## Использованные команды
```bash
git tag v0.0
git push origin v0.0
git push gitlab v0.0

git tag -a v0.1 -m "v0.1"
git push origin v0.1
git push gitlab v0.1
```

## Проверка локально
```bash
git tag -n          # список тегов с комментариями (виден только у annotated)
git show v0.1       # видно автора тега, дату, сообщение
git cat-file -t v0.0  # тип объекта у v0.0 -> commit (lightweight)
git cat-file -t v0.1  # тип объекта у v0.1 -> tag (annotated)
```

## Ссылки на страницы тегов
- GitHub: https://github.com/artharthur/devops-netology/tags
- GitLab:  https://gitlab.com/ishmakov.arthur/devops-netology-gitlab/-/tags

## О разнице
- Lightweight (v0.0) — просто имя, указывающее на коммит (без автора/даты/сообщения).
- Annotated (v0.1) — отдельный объект tag с автором, датой и сообщением (можно подписывать GPG).
