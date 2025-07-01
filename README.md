# -simple-keylogger-based-on-c-

🛡️ Keylogger + UI Inspector (C++ / WinAPI)
📌 Описание (Description)
Данный проект представляет собой учебный инструмент для демонстрации работы с низкоуровневыми функциями Windows API: перехват клавиш и мыши, отслеживание активного окна, логирование буфера обмена, определение типа UI-элемента, а также реализация автозапуска через реестр. Он реализован на языке C++ с использованием WinAPI и библиотеки UIAutomation.

This project is an educational keylogger written in C++ that demonstrates how to work with low-level Windows API: keyboard and mouse hooks, active window tracking, clipboard monitoring, UI control detection, and autostart via the Windows Registry.

⚙️ Возможности / Features
✅ Перехват клавиш в реальном времени
✅ Логирование событий мыши (левый/правый клик)
✅ Считывание названия активного окна и процесса
✅ Захват содержимого буфера обмена по Ctrl+V
✅ Определение типа UI-элемента (текстовое поле, кнопка и т.д.)
✅ Поддержка конфигурации через config.json (white/black list)
✅ Автозапуск через HKCU\Software\Microsoft\Windows\CurrentVersion\Run
✅ Unicode-поддержка (работает с любыми языками)
✅ Сохранение логов в файл keylog.txt в %APPDATA%\SystemLogs

🔧 Используемые технологии / Technologies
C++ (Visual Studio 2022)
WinAPI (SetWindowsHookEx, GetAsyncKeyState, etc.)
UIAutomation Core
nlohmann/json (для чтения конфигурации)
Windows Registry API (RegSetValueEx, RegOpenKeyEx)

Console I/O и File I/O
📁 Структура проекта / Project Structure
├── main.cpp                // Основной файл с логикой
├── config.json             // Конфигурация: белый/черный список
├── keylog.txt              // Лог-файл (создается автоматически)
└── README.md               // Этот файл

🧪 Пример использования (Example Usage)
Соберите проект в Visual Studio 2022.


Убедитесь, что в каталоге рядом с .exe-файлом находится файл config.json, например:
{
  "whitelist": ["notepad.exe", "chrome.exe"],
  "blacklist": ["Telegram.exe", "Discord.exe"]
}

Запустите программу от имени обычного пользователя.
Все события будут логироваться в файл keylog.txt по пути %APPDATA%\SystemLogs.


🚨 ВАЖНО / DISCLAIMER
⚠️ Этот проект предназначен исключительно для учебных целей. Не используйте данный код в продакшене или для мониторинга без согласия пользователя. Нарушение конфиденциальности данных может повлечь за собой юридическую ответственность.
⚠️ This software is provided strictly for educational purposes only. Do not use it on machines you do not own or without explicit consent. Unauthorized use may violate privacy laws.

📌 Требования (Requirements)
Windows 10/11 (x64)
Visual Studio 2022 с установленным Windows SDK
Доступ к реестру пользователя (HKCU)

🧠 Полезные ресурсы
Microsoft Docs: Windows Hooks (https://learn.microsoft.com/en-us/windows/win32/winmsg/about-hooks)
UIAutomation Overview (https://learn.microsoft.com/en-us/windows/win32/winauto/uiauto-uiautomationoverview)
nlohmann/json GitHub (https://github.com/nlohmann/json)

Student Project – Cybersecurity 2nd Year
Kazakhstan, AITU
July 01 2025

