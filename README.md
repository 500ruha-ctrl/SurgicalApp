<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Surgical App</title>
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="app">
        <!-- Шапка -->
        <header>
            <div class="avatar">
                <img src="https://via.placeholder.com/50/2ecc71/ffffff?text=🏥" alt="Logo">
            </div>
            <div class="header-text">
                <h1>Surgical App</h1>
                <span class="status">● Онлайн</span>
            </div>
        </header>

        <!-- Основной контент -->
        <main id="content">
            <!-- Главная страница -->
            <div id="page-home" class="page active">
                <div class="greeting">
                    <h2>Добро пожаловать!</h2>
                    <p>Выберите действие ниже</p>
                </div>
                
                <div class="menu-grid">
                    <button class="menu-btn" data-page="appointment">
                        <span class="icon">📋</span>
                        Запись на приём
                    </button>
                    <button class="menu-btn" data-page="results">
                        <span class="icon">📊</span>
                        Результаты анализов
                    </button>
                    <button class="menu-btn" data-page="chat">
                        <span class="icon">💬</span>
                        Чат с врачом
                    </button>
                    <button class="menu-btn" data-page="records">
                        <span class="icon">📅</span>
                        Мои записи
                    </button>
                </div>
            </div>

            <!-- Страница записи -->
            <div id="page-appointment" class="page">
                <button class="back-btn">← Назад</button>
                <h2>📋 Запись на приём</h2>
                <form id="appointment-form">
                    <input type="text" placeholder="Ваше имя" required>
                    <input type="date" required>
                    <input type="time" required>
                    <select required>
                        <option value="">Выберите врача</option>
                        <option>Хирург Иванов А.А.</option>
                        <option>Травматолог Петров Б.Б.</option>
                        <option>Онколог Сидоров В.В.</option>
                    </select>
                    <textarea placeholder="Комментарий"></textarea>
                    <button type="submit" class="submit-btn">✅ Отправить</button>
                </form>
                <div id="form-output" class="output"></div>
            </div>

            <!-- Страница результатов -->
            <div id="page-results" class="page">
                <button class="back-btn">← Назад</button>
                <h2>📊 Результаты анализов</h2>
                <div class="result-item">
                    <span>Общий анализ крови</span>
                    <span class="status-badge success">✓ Готово</span>
                </div>
                <div class="result-item">
                    <span>Биохимия</span>
                    <span class="status-badge warning">⏳ В обработке</span>
                </div>
                <div class="result-item">
                    <span>МРТ</span>
                    <span class="status-badge success">✓ Готово</span>
                </div>
                <div class="result-item">
                    <span>УЗИ</span>
                    <span class="status-badge danger">⚠️ Требуется пересдача</span>
                </div>
            </div>

            <!-- Страница чата -->
            <div id="page-chat" class="page">
                <button class="back-btn">← Назад</button>
                <h2>💬 Чат с врачом</h2>
                <div class="chat-messages">
                    <div class="message received">Здравствуйте! Чем могу помочь?</div>
                    <div class="message sent">Здравствуйте! Беспокоит боль в колене.</div>
                    <div class="message received">Понял. Когда началась боль?</div>
                </div>
                <div class="chat-input">
                    <input type="text" placeholder="Напишите сообщение...">
                    <button>📤</button>
                </div>
            </div>

            <!-- Страница записей -->
            <div id="page-records" class="page">
                <button class="back-btn">← Назад</button>
                <h2>📅 Мои записи</h2>
                <div class="record-card">
                    <div class="record-date">15 июня 2026</div>
                    <div class="record-doctor">Хирург Иванов А.А.</div>
                    <div class="record-time">⏰ 14:30</div>
                    <span class="status-badge success">✓ Подтверждено</span>
                </div>
                <div class="record-card">
                    <div class="record-date">22 июня 2026</div>
                    <div class="record-doctor">Травматолог Петров Б.Б.</div>
                    <div class="record-time">⏰ 10:00</div>
                    <span class="status-badge warning">⏳ Ожидает</span>
                </div>
            </div>
        </main>
    </div>

    <script src="script.js"></script>
</body>
</html>
