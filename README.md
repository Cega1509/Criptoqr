# CryptoQR — Android App

Приложение для шифрования текста с AES-256-GCM и генерации QR-кодов.

---

## 🛠 Как собрать APK

### Способ 1: Android Studio (рекомендуется)

1. Скачай [Android Studio](https://developer.android.com/studio) и установи
2. Открой Android Studio → **Open** → выбери папку `CryptoQR`
3. Дождись синхронизации Gradle (первый раз ~5 минут)
4. Меню: **Build → Build Bundle(s) / APK(s) → Build APK(s)**
5. APK появится в `app/build/outputs/apk/debug/app-debug.apk`

### Способ 2: Командная строка (если установлен JDK 17+)

```bash
cd CryptoQR
chmod +x gradlew       # (на Mac/Linux)
./gradlew assembleDebug
# На Windows: gradlew.bat assembleDebug
```

APK будет в: `app/build/outputs/apk/debug/app-debug.apk`

---

## 📱 Установка APK на телефон

1. Включи **«Установка из неизвестных источников»**:
   Настройки → Безопасность → Установка неизвестных приложений
2. Перенеси APK на телефон (USB / Telegram себе / облако)
3. Открой файл и нажми **Установить**

---

## 🔒 Технологии

- **AES-256-GCM** — шифрование военного уровня
- **PBKDF2** (310 000 итераций) — защита от перебора паролей
- **QR-код** — зашифрованные данные в виде QR
- Всё работает **офлайн**, данные никуда не передаются
- WebView + чистый HTML/JS/CSS — без внешних зависимостей

---

## 📋 Требования

- Android 7.0+ (API 24+)
- JDK 17 для сборки
- Android Studio Hedgehog или новее
