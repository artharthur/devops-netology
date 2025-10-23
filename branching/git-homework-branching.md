# Домашнее задание «Ветвления в Git» — отчёт

Дата: 2025-10-23

## Ссылка на граф веток (GitHub)
https://github.com/artharthur/devops-netology/network

## Скрипты (ветка main)
- `branching/merge.sh` — вывод по одному аргументу на строку (while + shift)
- `branching/rebase.sh` — вывод в стиле: `Next parameter: <arg>` + разделитель `=====`

## Кратко, что сделано
- Созданы `merge.sh` и `rebase.sh` на базе `"$*"`, коммит: **prepare for merge and rebase**.
- Ветка **git-merge**: переход на `"$@"`, затем `while ... shift`; смержено в `main` (разрешён конфликт в `merge.sh`).
- Ветка **git-rebase**: два коммита на `rebase.sh`; выполнен `git rebase -i main` с `fixup`, решены конфликты; объединённый результат в `main`.

## Как проверить
1. Откройте ссылку на граф (выше) — видны ветки `git-merge` и `git-rebase`, их вливания в `main`.
2. В ветке `main` файлы:
   - `branching/merge.sh`
   - `branching/rebase.sh`
