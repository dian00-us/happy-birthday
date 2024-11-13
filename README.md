
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Поздравление с 50-летием!</title>
    <style>
        /* Основные стили для страницы */
        body {
            font-family: 'Verdana', sans-serif;
            margin: 0;
            padding: 0;
            background: #f3f1e8; /* Теплый уютный фон */
            color: #5a4e44; /* Нежный темно-бежевый текст */
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        /* Контейнер для всего содержимого */
        .content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 90%;
            max-width: 1200px;
            padding: 40px;
            box-sizing: border-box;
            border-radius: 20px;
            background: #fff8e1; /* Легкий кремовый оттенок */
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
        }

        /* Заголовок на левой стороне */
        header {
            text-align: left;
            width: 45%;
            font-size: 2.8em;
            color: #b29b6e; /* Золотисто-бежевый */
            font-weight: 600;
            line-height: 1.2;
            animation: fadeInLeft 2s ease-in-out forwards;
        }

        header p {
            font-size: 1.6em;
            color: #b29b6e;
            margin-top: 20px;
            font-weight: 400;
            animation: fadeInLeft 3s ease-in-out forwards;
        }

        /* Конверт с поздравлением */
        .envelope {
            width: 50%;
            max-width: 600px;
            padding: 40px;
            background: #f8d7b1; /* Светлый персиковый оттенок */
            border-radius: 15px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.15);
            text-align: left;
            opacity: 0;
            animation: fadeInRight 2s ease-out forwards;
        }

        .envelope h2 {
            font-size: 2.5em;
            color: #5a4e44; /* Темно-бежевый */
            margin: 0;
            margin-bottom: 20px;
        }

        .envelope p {
            font-size: 1.5em;
            color: #5a4e44;
            line-height: 1.6;
            margin-top: 20px;
        }

        /* Анимация для текста */
        @keyframes fadeInLeft {
            0% { opacity: 0; transform: translateX(-30px); }
            100% { opacity: 1; transform: translateX(0); }
        }

        @keyframes fadeInRight {
            0% { opacity: 0; transform: translateX(30px); }
            100% { opacity: 1; transform: translateX(0); }
        }

        /* Всплывающее окно сюрприза */
        .popup {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0, 0, 0, 0.6);
            display: none;
            justify-content: center;
            align-items: center;
            z-index: 1000;
            animation: popupIn 1s ease-out forwards;
        }

        .popup-content {
            background: #ffffff;
            padding: 30px;
            border-radius: 15px;
            text-align: center;
            max-width: 500px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
        }

        .popup-content h3 {
            font-size: 2.2em;
            color: #f28c8c; /* Розовый акцент */
        }

        .popup-content p {
            font-size: 1.3em;
            color: #7c5c3a;
            margin-top: 10px;
        }

        .close-btn {
            background: #f0b890;
            color: white;
            border: none;
            padding: 12px 24px;
            font-size: 1.2em;
            cursor: pointer;
            border-radius: 8px;
            margin-top: 20px;
        }

        .close-btn:hover {
            background: #d18b5a;
        }

        @keyframes popupIn {
            0% { opacity: 0; transform: scale(0.7); }
            100% { opacity: 1; transform: scale(1); }
        }

        /* Мобильная версия */
        @media (max-width: 768px) {
            header {
                font-size: 2.2em;
                width: 100%;
                text-align: center;
            }

            .content {
                flex-direction: column;
                justify-content: center;
                padding: 20px;
            }

            .envelope {
                margin-top: 40px;
                width: 100%;
                padding: 20px;
            }

            .envelope h2 {
                font-size: 2em;
            }

            .envelope p {
                font-size: 1.2em;
            }
        }

    </style>
</head>
<body>

<!-- Фон с градиентом -->
<div class="background"></div>

<div class="content">
    <!-- Текст на левой стороне -->
    <header>
        <h1>С Днем Рождения, мама!</h1>
        <p>Тебе исполняется 50 лет!</p>
    </header>

    <!-- Конверт с поздравлением на правой стороне -->
    <div class="envelope">
        <h2>Дорогая мама!</h2>
        <p>Поздравляю тебя с этим чудесным и важным событием! 50 лет — это не просто цифра, это целая жизнь, наполненная радостью, трудностями, победами и бесконечной любовью. Ты — моя опора, вдохновение и пример для подражания. Пусть впереди будут только самые яркие и счастливые моменты! Желаю тебе здоровья, счастья и нескончаемой гармонии в душе. Мы тебя очень любим и гордимся тобой!</p>
    </div>
</div>

<!-- Вставка фона музыки -->
<audio autoplay loop>
    <source src="your-music-file.mp3" type="audio/mp3">
    Ваш браузер не поддерживает элемент audio.
</audio>

<!-- Всплывающее окно сюрприза -->
<div class="popup" id="popup">
    <div class="popup-content">
        <h3>Сюрприз для тебя!</h3>
        <p>Мама, ты — самая лучшая в мире! Спасибо за все, что ты делаешь для нас.</p>
        <button class="close-btn" onclick="closePopup();">Закрыть</button>
    </div>
</div>

<script>
    // Открытие и закрытие всплывающего окна
    function showPopup() {
        document.getElementById("popup").style.display = "flex";
    }

    function closePopup() {
        document.getElementById("popup").style.display = "none";
    }

    // Показать всплывающее окно с небольшим задержкой
    setTimeout(showPopup, 3000); // Показывать через 3 секунды
</script>

</body>
</html>








