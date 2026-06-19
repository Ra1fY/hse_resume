# Резюме Игнатьева Алексея Львович

**ФИО:** Игнатьев Алексей Львович

**Группа:** БКНАД251

---

## Описание

Резюме написано на LaTeX. Сборка автоматизирована с помощью Docker и GitHub Actions.

---

## Структура репозитория
├── .github/  
│ └── workflows/  
│ └── main.yml # CI: проверка сборки  
├── CV/  
│ ├── cv.tex # Резюме  
│ └── hse_logo.jpg # Логотип  
├── Dockerfile # Сборка через Docker  
├── choose_system.py # Выбор системы  
├── choose_reviewer.py # Выбор проверяющего  
└── README.md

---

## Локальная сборка

```bash
docker build -t resume_builder .
docker run --rm -v $(pwd):/output resume_builder sh -c "cd /app/CV && pdflatex -interaction=nonstopmode cv.tex && cp cv.pdf /output/"
```

---

## Контакты
Email: alignatev@edu.hse.ru
Telegram: @yomayomamazvonit228
