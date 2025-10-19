# Задание 3 — Ветки

## Что сделано
- Ветка `main` привязана к GitHub: `[origin/main]`.
- Найдён коммит **Prepare to delete and move**: `3a9b4a7`.
- Создана ветка `fix` от этого коммита и запушена в GitHub.
- В `fix` изменён `README.md` (добавлена строка) и изменения запушены.

## Команды
```bash
git switch main
git log --oneline --grep='Prepare to delete and move'
git checkout 3a9b4a7
git switch -c fix
git push -u origin fix
```

## Ссылки

- Граф коммитов (GitHub): https://github.com/artharthur/devops-netology/network
- Ветки: main, fix
