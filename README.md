# ABLIOFIT для Android

WebView-обёртка вокруг вашей страницы (`app/src/main/assets/index.html`).
Данные хранятся локально (localStorage), интернет не нужен.

## Способ 1. Android Studio
1. File → Open → выберите папку проекта, дождитесь синхронизации Gradle.
2. Подключите телефон (отладка по USB) и нажмите Run ▶
   или Build → Build APK(s) → `app/build/outputs/apk/debug/app-debug.apk`

## Способ 2. Без Android Studio (GitHub)
1. Создайте репозиторий на github.com и загрузите в него все файлы проекта
   (вместе с папкой `.github`).
2. Вкладка Actions → «Build APK» → Run workflow.
3. Когда сборка завершится, скачайте артефакт `ABLIOFIT-apk` — внутри `.apk`.

## Установка на телефон
Скопируйте APK на телефон, откройте и разрешите установку из этого источника.

## Обновление страницы
Замените `app/src/main/assets/index.html` и пересоберите. Чтобы установить
поверх старой версии, увеличьте `versionCode` в `app/build.gradle.kts`.

## Google Play
Нужен собственный keystore вместо debug-подписи (см. `signingConfig`
в `app/build.gradle.kts`) и сборка AAB: `gradle :app:bundleRelease`.
