# devops-netology first line

## Ignore rules
- Системные файлы macOS: `.DS_Store`
- Файлы IDE/редакторов: `.idea/`, `*.swp`
- Terraform:
  - директории `.terraform/`
  - состояния `*.tfstate*`
  - lock-файл `.terraform.lock.hcl`
  - crash-логи `crash*.log`
  - override-файлы `override.tf*`
  - файлы с переменными `*.tfvars*` (секреты)

## .gitignore в каталоге `terraform`: что означают шаблоны

Язык правил gitignore):
- `*` — любой набор символов (кроме `/`)
- `?` — один любой символ
- `**` — любое число каталогов (в т.ч. 0)
- завершающий `/` — правило для каталогов
- `!` — инверсия (не используется ниже)
- `#` — комментарий

Используемые шаблоны:
- `**/.terraform/*` — любой каталог с именем `.terraform` на любом уровне и всё его содержимое.
- `*.tfstate` — все файлы, чьи имена **заканчиваются** на `.tfstate`.
- `*.tfstate.*` — имена с подстрокой `.tfstate.` и любым суффиксом (например `.tfstate.backup`).
- `crash.log` — строго файл с именем `crash.log`.
- `crash.*.log` — `crash.` + любой набор символов + `.log` (например `crash.2025-01-01.log`).
- `override.tf` / `override.tf.json` — строго эти имена.
- `*_override.tf` / `*_override.tf.json` — имена, **заканчивающиеся** на `_override.tf` или `_override.tf.json`.
- `*.tfvars` / `*.tfvars.json` — имена, **заканчивающиеся** на `.tfvars` или `.tfvars.json`.
- `.terraform.lock.hcl` — строго этот файл.
- `.terraformrc` / `terraform.rc` — строго эти имена.
