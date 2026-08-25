# 🏗️ План Разделения на Подпроекты

## 📋 **Анализ Текущей Структуры**

### 🎯 **Основные Функциональные Блоки:**
1. **🧠 Core Engine** - обработка контента (parsers, converters, scrapers, generators, validators)
2. **🌐 Web Components** - веб-интерфейс и API (ui, api, templates)
3. **🛠️ CLI Tools** - утилиты командной строки (automation, cli)
4. **📚 Documentation** - документация и примеры (user, developer, examples)
5. **⚙️ Configuration** - конфигурация и стили (pipelines, styles, metadata)
6. **🚀 Deployment** - деплоймент и инфраструктура (docker, scripts)
7. **📦 Content Pipeline** - обработка контента (scraped, parsed, uml, tei)
8. **🧪 Testing & Validation** - тесты и валидация

## 🎯 **Предлагаемая Структура Подпроектов:**

### 1️⃣ **integral-philosophy-core** 🧠
**Основной движок обработки контента**
- Content parsing (Markdown, LaTeX, HTML, etc.)
- Format conversion (10+ formats)
- Content validation and quality checks
- AST manipulation and analysis

### 2️⃣ **integral-philosophy-web** 🌐
**Веб-интерфейс и API**
- Flask/FastAPI web interface
- REST API endpoints
- Web templates and static assets
- Real-time processing dashboard

### 3️⃣ **integral-philosophy-cli** 🛠️
**Инструменты командной строки**
- Main CLI interface
- Scraping tools
- Conversion utilities
- Batch processing scripts

### 4️⃣ **integral-philosophy-content** 📚
**Контент и примеры**
- Sample academic articles
- Test datasets
- Example configurations
- Template collections

### 5️⃣ **integral-philosophy-config** ⚙️
**Конфигурация и стили**
- Pipeline configurations
- TEI templates and XSLT
- Academic style templates
- Processing rules

### 6️⃣ **integral-philosophy-deploy** 🚀
**Деплоймент и инфраструктура**
- Docker configurations
- Kubernetes manifests
- CI/CD pipelines
- Monitoring and logging

### 7️⃣ **integral-philosophy-docs** 📖
**Документация**
- User guides
- Developer documentation
- API references
- Architecture docs

### 8️⃣ **integral-philosophy-tests** 🧪
**Тестирование и валидация**
- Unit tests
- Integration tests
- End-to-end tests
- Performance tests

## 🔗 **Интеграция Подпроектов:**

### **Main Project** (integral-philosophy)
```
integral-philosophy/
├── 📦 README.md           # Основная документация
├── 🐳 docker-compose.yml  # Полная система
├── 🛠️ setup.sh           # Автоустановка
├── 📜 requirements.txt     # Основные зависимости
├── 🌐 main.py           # Unified CLI
└── 📂 .gitmodules       # Git submodules
```

### **Git Submodules Structure:**
```bash
git submodule add https://github.com/neoallunity/integral-philosophy-core.git core/
git submodule add https://github.com/neoallunity/integral-philosophy-web.git web/
git submodule add https://github.com/neoallunity/integral-philosophy-cli.git cli/
git submodule add https://github.com/neoallunity/integral-philosophy-content.git content/
git submodule add https://github.com/neoallunity/integral-philosophy-config.git config/
git submodule add https://github.com/neoallunity/integral-philosophy-deploy.git deploy/
git submodule add https://github.com/neoallunity/integral-philosophy-docs.git docs/
git submodule add https://github.com/neoallunity/integral-philosophy-tests.git tests/
```

## 🎯 **Преимущества Подпроектной Структуры:**

### **🏗️ Модульность**
- Независимая разработка каждого компонента
- Изоляция зависимостей
- Версионирование отдельных модулей

### **👥 Командная Работа**
- Разные команды могут работать над разными подпроектами
- Специализация разработчиков
- Независимый релиз цикл

### **📦 Переиспользование**
- Core engine можно использовать отдельно
- Web interface для других проектов
- CLI tools как независимые утилиты

### **🔧 Поддержка**
- Изолированные проблемы
- Фокусированная документация
- Специфичные тесты

### **📈 Масштабирование**
- Легкое добавление новых подпроектов
- Независимое развитие компонентов
- Гибкая архитектура

## 🚀 **План Реализации:**

### **Фаза 1: Создание Подпроектов**
1. Организовать core engine как отдельный проект
2. Выделить web components
3. Создать CLI tools проект

### **Фаза 2: Настройка Интеграции**
1. Настроить git submodules
2. Обновить основной проект
3. Создать unified setup

### **Фаза 3: Документация и Тесты**
1. Создать документацию подпроектов
2. Настроить CI/CD для каждого подпроекта
3. Интеграционное тестирование

### **Фаза 4: Деплоймент**
1. Настроить Docker Compose
2. Создать Helm charts
3. Настроить мониторинг