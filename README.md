<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Поздравление с 50-летием!</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            color: #fff;
            background: #e6d1b3; /* Уютный фон с теплым оттенком */
            overflow: hidden;
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        /* Плавный фон с градиентом */
        .background {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(to bottom, #f5e2d8, #e6d1b3); /* Теплый градиент */
            z-index: -1;
        }

        /* Контейнер для текста и конверта */
        .content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 80%;
            max-width: 1200px;
            padding: 40px;
            box-sizing: border-box;
        }

        header {
            text-align: left;
            font-size: 3.5em;
            color: #b79d7e; /* Золотисто-бежевый */
            letter-spacing: 2px;
            font-weight: bold;
            animation: fadeInLeft 2s ease-in-out forwards;
            width: 40%;
        }

        header p {
            font-size: 1.5em;
            color: #b79d7e;
            margin-top: 10px;
            animation: fadeInLeft 3s ease-in-out forwards;
        }

        .envelope {
            width: 50%;
            max-width: 600px;
            padding: 40px;
            background: #d5b98a; /* Легкий золотисто-бежевый */
            border-radius: 25px;
            position: relative;
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.3);
            opacity: 0;
            animation: slideInRight 2s ease-out forwards;
            text-align: left;
        }

        .envelope:before {
            content: "";
            position: absolute;
            top: -20px;
            left: 50%;
            transform: translateX(-50%);
            width: 0;
            height: 0;
            border-left: 60px solid transparent;
            border-right: 60px solid transparent;
            border-bottom: 30px solid #d5b98a;
        }

        .envelope h2 {
            font-size: 2.8em;
            color: #fff;
            margin: 0;
            text-align: left;
        }

        .envelope p {
            font-size: 1.5em;
            color: #fff;
            margin-top: 20px;
            line-height: 1.6;
            text-align: left;
        }

        /* Анимация для появления текста */
        @keyframes fadeInLeft {
            0% { opacity: 0; transform: translateX(-30px); }
            100% { opacity: 1; transform: translateX(0); }
        }

        /* Анимация появления конверта */
        @keyframes slideInRight {
            0% { opacity: 0; transform: translateX(30px); }
            100% { opacity: 1; transform: translateX(0); }
        }

        /* Анимация для цифры 50 */
        .number {
            position: absolute;
            font-size: 150px;
            color: #b79d7e;
            font-weight: bold;
            animation: numberAnim 3s ease-in-out infinite;
            opacity: 0.6;
        }

        .number-50 {
            animation-delay: 0s;
        }

        .number-50.left {
            top: 10%;
            left: 5%;
        }

        .number-50.right {
            top: 40%;
            left: 80%;
        }

        @keyframes numberAnim {
            0% {
                opacity: 0;
                transform: scale(0.5);
            }
            50% {
                opacity: 1;
                transform: scale(1.3);
            }
            100% {
                opacity: 0;
                transform: scale(0.5);
            }
        }

        /* Анимация для сердечек */
        .heart {
            position: absolute;
            font-size: 50px;
            color: #f28c8c;
            animation: float 10s infinite ease-in-out;
            opacity: 0.8;
        }

        @keyframes float {
            0% {
                transform: translateY(0) rotate(0deg);
            }
            50% {
                transform: translateY(-200px) rotate(180deg);
            }
            100% {
                transform: translateY(0) rotate(360deg);
            }
        }

        /* Всплывающее окно сюрприза */
        .popup {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0, 0, 0, 0.7);
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
            font-size: 2.5em;
            color: #f0b890;
        }

        .popup-content p {
            font-size: 1.5em;
            color: #7c5c3a;
        }

        .close-btn {
            background: #f0b890;
            color: white;
            border: none;
            padding: 10px 20px;
            font-size: 1.2em;
            cursor: pointer;
            border-radius: 8px;
            margin-top: 20px;
        }

        .close-btn:hover {
            background: #d18b5a;
        }

        /* Всплывающее окно - анимация */
        @keyframes popupIn {
            0% { opacity: 0; transform: scale(0.7); }
            100% { opacity: 1; transform: scale(1); }
        }

        /* Мобильная версия */
        @media (max-width: 600px) {
            header h1 {
                font-size: 2.5em;
            }

            .button {
                font-size: 1.2em;
                padding: 12px 20px;
            }

            .envelope {
                padding: 20px;
            }

            .envelope h2 {
                font-size: 2.5em;
            }

            .envelope p {
                font-size: 1.2em;
            }

            header {
                margin: 0 5%;
            }

            .content {
                margin: 0 5%;
                flex-direction: column;
                align-items: center;
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

<!-- Анимация для цифры 50 -->
<div class="number number-50 left">50</div>
<div class="number number-50 right">50</div>

<!-- Анимация для сердечек -->
<div class="heart" style="top: 10%; left: 20%;">❤️</div>
<div class="heart" style="top: 30%; left: 40%;">❤️</div>
<div class="heart" style="top: 50%; left: 60%;">❤️</div>
<div class="heart" style="top: 70%; left: 80%;">❤️</div>
<div class="heart" style="top: 80%; left: 15%;">❤️</div>

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
</script>

</body>
</html>








