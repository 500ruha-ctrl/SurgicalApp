<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
  <title>Surgical App</title>
  <script src="https://telegram.org/js/telegram-web-app.js"></script>
  <style>
    :root {
      --text-color: #ffffff;
      --btn-bg: rgba(99, 168, 91, 0.85); /* Полупрозрачный зеленый */
      --btn-active-bg: rgba(79, 138, 72, 0.95);
    }

    body {
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
      margin: 0;
      padding: 16px;
      display: flex;
      flex-direction: column;
      gap: 10px;
      -webkit-tap-highlight-color: transparent;
      box-sizing: border-box;

      /* Использование вашего фото bg.jpg с легким затемнением */
      background: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)), 
                  url('./bg.jpg') center/cover no-repeat fixed;
      min-height: 100vh;
    }

    .menu-button {
      background-color: var(--btn-bg);
      color: #ffffff;
      border: 1px solid rgba(255, 255, 255, 0.2);
      border-radius: 12px;
      padding: 14px 18px;
      font-size: 16px;
      font-weight: 500;
      display: flex;
      justify-content: space-between;
      align-items: center;
      cursor: pointer;
      backdrop-filter: blur(6px);
      -webkit-backdrop-filter: blur(6px);
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.25);
      transition: background-color 0.15s ease, transform 0.1s ease;
      width: 100%;
      box-sizing: border-box;
      text-align: left;
    }

    .menu-button:active {
      background-color: var(--btn-active-bg);
      transform: scale(0.98);
    }

    .icon {
      font-size: 18px;
      opacity: 0.9;
    }
  </style>
</head>
<body>

  <!-- Разделы со скриншота 1 -->
  <button class="menu-button" onclick="openSection('ФакХир в таблицах и схемах')">
    <span>ФакХир в таблицах и схемах</span>
    <span class="icon">↗</span>
  </button>

  <button class="menu-button" onclick="openSection('Хирургия желчных путей')">
    <span>Хирургия желчных путей</span>
    <span class="icon">↗</span>
  </button>

  <button class="menu-button" onclick="openSection('Миниинвазивная хирургия')">
    <span>Миниинвазивная хирургия</span>
    <span class="icon">↗</span>
  </button>

  <button class="menu-button" onclick="openSection('Моша Шайн «Здравый смысл»')">
    <span>Моша Шайн «Здравый смысл»</span>
    <span class="icon">↗</span>
  </button>

  <button class="menu-button" onclick="openSection('Тактика врача - хирурга')">
    <span>Тактика врача - хирурга</span>
    <span class="icon">↗</span>
  </button>

  <button class="menu-button" onclick="openSection('Эндокриная хирургия')">
    <span>Эндокриная хирургия</span>
    <span class="icon">↗</span>
  </button>

  <button class="menu-button" onclick="openSection('Пластическая хирургия')">
    <span>Пластическая хирургия</span>
    <span class="icon">↗</span>
  </button>

  <button class="menu-button" onclick="openSection('Гнойная хирургия')">
    <span>Гнойная хирургия</span>
    <span class="icon">↗</span>
  </button>

  <button class="menu-button" onclick="openSection('Торакальная хирургия')">
    <span>Торакальная хирургия</span>
    <span class="icon">↗</span>
  </button>

  <button class="menu-button" onclick="openSection('Оперативная гинекология')">
    <span>Оперативная гинекология</span>
    <span class="icon">↗</span>
  </button>

  <button class="menu-button" onclick="openSection('Детская хирургия')">
    <span>Детская хирургия</span>
    <span class="icon">↗</span>
  </button>

  <!-- Разделы со скриншота 2 -->
  <button class="menu-button" onclick="openSection('Герниология')">
    <span>Герниология</span>
    <span class="icon">↗</span>
  </button>

  <button class="menu-button" onclick="openSection('ГЭ Неттера')">
    <span>ГЭ Неттера</span>
    <span class="icon">↗</span>
  </button>

  <button class="menu-button" onclick="openSection('Э.Итала «Атлас абдоминальной хирургии»')">
    <span>Э.Итала «Атлас абдоминальной хиру...»</span>
    <span class="icon">↗</span>
  </button>

  <button class="menu-button" onclick="openSection('Атласы лапароскопической хирургии')">
    <span>Атласы лапароскопической хирургии</span>
    <span class="icon">↗</span>
  </button>

  <button class="menu-button" onclick="openSection('Безопасная ЛХЭ')">
    <span>Безопасная ЛХЭ</span>
    <span class="icon">↗</span>
  </button>

  <button class="menu-button" onclick="openSection('Оперативка Литтмана')">
    <span>Оперативка Литтмана</span>
    <span class="icon">↗</span>
  </button>

  <button class="menu-button" onclick="openSection('Неотложная хирургия')">
    <span>Неотложная хирургия</span>
    <span class="icon">↗</span>
  </button>

  <button class="menu-button" onclick="openSection('Топографическая анатомия')">
    <span>Топографическая анатомия</span>
    <span class="icon">↗</span>
  </button>

  <button class="menu-button" onclick="openSection('Энциклопедия хир.рака желудка')">
    <span>Энциклопедия хир.рака желудка</span>
    <span class="icon">↗</span>
  </button>

  <button class="menu-button" onclick="openSection('УЗИ, КТ-диагностика')">
    <span>УЗИ, КТ-диагностика</span>
    <span class="icon">↗</span>
  </button>

  <button class="menu-button" onclick="openSection('Ссылки на операции, лекции')">
    <span>Ссылки на операции, лекции</span>
    <span class="icon">↗</span>
  </button>

  <button class="menu-button" onclick="openSection('Колопроктология')">
    <span>Колопроктология</span>
    <span class="icon">↗</span>
  </button>

  <script>
    const tg = window.Telegram.WebApp;
    tg.ready();
    tg.expand();

    function openSection(title) {
      if (tg.HapticFeedback) {
        tg.HapticFeedback.impactOccurred('light');
      }
      console.log('Открыт раздел:', title);
    }
  </script>
</body>
</html>
