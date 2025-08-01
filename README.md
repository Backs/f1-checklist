# 🏎️💨 Техосмотр проекта: Чеклист для борьбы с техническим долгом

> **Формула успеха:** Надежность × Скорость разработки  
> Проверьте свой проект перед выходом на трассу нового сезона!

## 🔧 1. Пилотская подготовка: Онбординг и окружение
- [ ] **🚦 Старт с одного клика:** Проект запускается по F5 (или 1 скриптом) без ручных шагов
- [ ] **📖 Четкий брифинг:** В `README.md` есть актуальные шаги: установка, запуск, тесты, деплой
- [ ] **🔐 Секреты в сейфе:** Нет паролей/ключей в репозитории. Используется Vault и другие централизованные инструменты упралвения настройками
- [ ] **🆕 Страница новичка:** В Wiki есть раздел с графиками, алертами, процессами команды
- [ ] **🚧 Тестовые стенды:** Есть достаточное количество независимых тестовых окружения + инструкция по созданию

## 🛠️ 2. Техника: Надежность и производительность
- [ ] **🟢 Зеленый флаг:** 
  - Все тесты **зеленые** в CI и запускаются при каждом пуше
  - Нет зависимости от порядка выполнения или внешних сервисов
- [ ] **📊 Телеметрия:**
  - Есть дашборды с **бизнес-метриками** (RPS, время ответа, ошибки)
  - В Sentry/логах нет "мусорных" ошибок (уровень `ERROR` = критические сбои)
- [ ] **⚙️ Двигатель (.NET):**
  - Версия фреймворка **в поддержке** (не ниже .NET 8)
  - Нет утечек памяти (проверено через профилирование)
- [ ] **📝 Эффективность:**
  - Логирование настроено разумно (нет дампа огромных json)
  - Нет N+1 запросов, избыточных выборок из БД и других сервисов

## ⛽ 3. Топливная система: Базы данных
- [ ] **🧰 Миграции как код:** Схема БД версионируется (EF Core Migrations, Liquibase)
- [ ] **👌 Оптимальные типы:** Нет `nvarchar(MAX)` для хранения всего
- [ ] **📊 Индексы под контролем:** Нет дублирующих/неиспользуемых индексов
- [ ] **⏱️ Мониторинг запросов:** Следим за медленными (>1000ms) запросами

## ✈️ 4. Аэродинамика: Чистота кода
- [ ] **🚲 Велосипеды в парке:** Нет кастомных реализаций стандартных решений (без веских причин)
- [ ] **📦 Зависимости:** Все пакеты обновлены до актуальных версий
- [ ] **📜 Документация нестандартных решений:** Если "велосипед" необходим, объяснено ЗАЧЕМ

## 🏁 5. Гонка без сбоев: Культура надежности
- [ ] **🔴 Нет игнора красных флагов:** Сломанные тесты чинятся за день (никто не говорит "Да забей, они всегда красные")
- [ ] **🔒 Эксперименты безопасны:** Новички могут пробовать идеи без страха сломать общее окружение
- [ ] **📉 Техдолг под контролем:** Устаревшие зависимости/велосипеды задокументированы и приоритизированы
- [ ] **📡 Дежурство без стресса:** Разработчики не боятся дежурства благодаря полезным метрикам

**Важно**: Не пытайтесь чинить всё сразу! Выберите 2-3 пункта, которые больнее всего тормозят вашу "гонку".
