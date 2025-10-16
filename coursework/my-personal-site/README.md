# Курсовой проект: MkDocs (Material)

## Установка
```bash
pip install mkdocs mkdocs-material pymdown-extensions
```

## Запуск локально
```bash
mkdocs serve
```

Откройте http://127.0.0.1:8000/ в браузере.

## Сборка статики
```bash
mkdocs build
```

## Кастомизация
- Логотип: `docs/images/logo.svg`
- Фото: `docs/images/portrait.svg` (замените на своё)
- Цвета и опции темы: `mkdocs.yml` → `theme.palette`, `features`
- Навигация: `mkdocs.yml` → `nav`
- Футер/соцсети: `mkdocs.yml` → `extra.copyright`, `extra.social`