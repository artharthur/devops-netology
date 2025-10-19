# devops-netologyfirst line

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
fix: add new line
