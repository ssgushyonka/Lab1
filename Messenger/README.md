# Messenger - Android приложение

Простое Android-приложение "Мессенджер" с использованием архитектуры на основе Activity и Fragment, а также встроенной навигации.

## Функциональные требования

✅ **Главная активность**: Одна главная активность как точка входа  
✅ **Bottom Navigation**: Навигация с помощью Bottom Navigation  
✅ **Три экрана**:
- 📰 Экран новостной ленты (заглушка с текстом)
- 👤 Экран профиля пользователя с основными данными
- ⚙️ Экран настроек с переключателем темы

✅ **Android Navigation**: Навигация через NavController и Navigation Graph  
✅ **Отслеживание жизненного цикла**: Логирование при создании и завершении компонентов

## Технический стек

- **Язык**: Kotlin
- **Архитектура**: Activity + Fragment
- **Навигация**: Android Navigation Component
- **UI**: Material Design Components
- **Хранение данных**: SharedPreferences (для настроек темы)

## Структура проекта

```
app/src/main/
├── java/com/example/messenger/
│   ├── MainActivity.kt                    # Главная активность
│   └── fragments/
│       ├── NewsFragment.kt               # Фрагмент новостей
│       ├── ProfileFragment.kt            # Фрагмент профиля
│       └── SettingsFragment.kt           # Фрагмент настроек
├── res/
│   ├── layout/
│   │   ├── activity_main.xml             # Layout главной активности
│   │   ├── fragment_news.xml             # Layout новостей
│   │   ├── fragment_profile.xml          # Layout профиля
│   │   └── fragment_settings.xml         # Layout настроек
│   ├── navigation/
│   │   └── nav_graph.xml                 # Navigation Graph
│   ├── menu/
│   │   └── bottom_navigation_menu.xml    # Меню Bottom Navigation
│   └── drawable/
│       ├── ic_news.xml                   # Иконка новостей
│       ├── ic_profile.xml                # Иконка профиля
│       └── ic_settings.xml               # Иконка настроек
```

## Основные возможности

### 🏠 Главная активность (MainActivity)
- Настройка Bottom Navigation
- Отслеживание жизненного цикла с логированием
- Применение сохраненной темы при запуске

### 📰 Экран новостей (NewsFragment)
- Заглушка с описанием будущего функционала
- Отслеживание жизненного цикла

### 👤 Экран профиля (ProfileFragment)
- Отображение основных данных пользователя
- Аватар, имя, статус, дополнительная информация
- Отслеживание жизненного цикла

### ⚙️ Экран настроек (SettingsFragment)
- Переключатель темной темы
- Сохранение настроек в SharedPreferences
- Список других настроек (заглушка)
- Отслеживание жизненного цикла

## Особенности реализации

### Отслеживание жизненного цикла
Все компоненты (Activity и Fragment) логируют ключевые события жизненного цикла:
- `onCreate()` / `onCreateView()`
- `onStart()` / `onResume()`
- `onPause()` / `onStop()`
- `onDestroy()` / `onDestroyView()`

### Навигация
- Использование Android Navigation Component
- Navigation Graph с тремя destination
- Автоматическая привязка Bottom Navigation к NavController

### Темы
- Поддержка светлой и темной темы
- Сохранение выбора пользователя
- Применение темы при запуске приложения

## Запуск проекта

1. Откройте проект в Android Studio
2. Синхронизируйте Gradle файлы
3. Запустите приложение на эмуляторе или устройстве

## Логирование

Для просмотра логов жизненного цикла используйте фильтр по тегам:
- `MainActivity`
- `NewsFragment`
- `ProfileFragment`
- `SettingsFragment`

## Расширение функционала

Проект структурирован для легкого расширения:
- Добавление новых экранов через Navigation Graph
- Расширение функционала каждого Fragment
- Добавление новых настроек
- Интеграция с реальными данными

## Требования

- Android API 21+ (Android 5.0)
- Kotlin 2.0.21+
- Android Gradle Plugin 8.9.1+
