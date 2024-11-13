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
            color: #333;
            background: #f9f4f2; /* Нюдовый фон */
            overflow: hidden;
            position: relative;
        }

        /* Плавный фон с градиентом */
        .background {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(to bottom, #f1e3d5, #f4e0c1); /* Нежный градиент */
            z-index: -1;
        }

        header {
            text-align: center;
            background: #f8d9bb; /* Светло-нюдовый оттенок */
            padding: 30px;
            border-radius: 0 0 30px 30px;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
            margin: 0 10%;
        }

        header h1 {
            font-size: 3.5em;
            color: #b98d62;
            margin: 0;
            animation: fadeIn 2s ease-in-out;
        }

        header p {
            font-size: 1.5em;
            color: #7c5c3a;
            margin-top: 10px;
            opacity: 0;
            animation: fadeIn 3s ease-in-out;
        }

        .content {
            padding: 30px;
            text-align: center;
            margin: 0 10%;
        }

        .slideshow-container {
            max-width: 800px;
            position: relative;
            margin: auto;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .slides {
            display: none;
        }

        .slide img {
            width: 100%;
            border-radius: 10px;
        }

        .button {
            background-color: #f0b890;
            color: white;
            border: none;
            padding: 15px 30px;
            font-size: 1.4em;
            cursor: pointer;
            border-radius: 12px;
            margin-top: 30px;
            transition: all 0.3s ease;
        }

        .button:hover {
            background-color: #d18b5a;
            transform: scale(1.05);
        }

        /* Оформление поздравления в виде конверта */
        .envelope {
            width: 80%;
            max-width: 800px;
            margin: 40px auto;
            padding: 40px;
            background: #f7e8d1;
            border-radius: 25px;
            position: relative;
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.1);
            opacity: 0;
            animation: slideIn 2s ease-out forwards;
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
            border-bottom: 30px solid #f7e8d1;
        }

        .envelope h2 {
            font-size: 3.2em;
            color: #f0b890;
            margin: 0;
        }

        .envelope p {
            font-size: 1.4em;
            color: #7c5c3a;
            margin-top: 20px;
            line-height: 1.5;
        }

        /* Анимация сердечек */
        .heart {
            position: absolute;
            font-size: 40px;
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

        /* Анимация появления заголовка */
        @keyframes fadeIn {
            0% { opacity: 0; transform: translateY(-50px); }
            100% { opacity: 1; transform: translateY(0); }
        }

        /* Анимация появления конверта */
        @keyframes slideIn {
            0% { opacity: 0; transform: translateY(50px); }
            100% { opacity: 1; transform: translateY(0); }
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
            }
        }

    </style>
</head>
<body>

<!-- Фон с градиентом -->
<div class="background"></div>

<header>
    <h1>С Днем Рождения, мама!</h1>
    <p>Тебе исполняется 50 лет!</p>
</header>

<div class="content">
    <!-- Слайд-шоу -->
    <div class="slideshow-container">
        <div class="slides fade">
            <div class="slide">
                <img src="photo1.jpg" alt="Фото 1">
            </div>
        </div>
        <div class="slides fade">
            <div class="slide">
                <img src="photo2.jpg" alt="Фото 2">
            </div>
        </div>
        <div class="slides fade">
            <div class="slide">
                <img src="photo3.jpg" alt="Фото 3">
            </div>
        </div>
    </div>

    <button class="button" onclick="showPopup();">Открыть сюрприз</button>

    <!-- Окно с поздравлением в виде конверта -->
    <div class="envelope">
        <h2>Дорогая мама!</h2>
        <p>Поздравляю тебя с этим чудесным и важным событием! 50 лет — это не просто цифра, это целая жизнь, наполненная радостью, трудностями, победами и бесконечной любовью. Ты — моя опора, вдохновение и пример для подражания. Пусть впереди будут только самые яркие и счастливые моменты! Желаю тебе здоровья, счастья и нескончаемой гармонии в душе. Мы тебя очень любим и гордимся тобой!</p>
    </div>

    <div class="heart" style="top: 10%; left: 20%;">❤️</div>
    <div class="heart" style="top: 30%; left: 40%;">❤️</div>
    <div class="heart" style="top: 50%; left: 60%;">❤️</div>
    <div class="heart" style="top: 70%; left: 80%;">❤️</div>
    <div class="heart" style="top: 80%; left: 15%;">❤️</div>
</div>

<!-- Всплывающее окно сюрприза -->
<div class="popup" id="popup">
    <div class="popup-content">
        <h3>Сюрприз для тебя!</h3>
        <p>Мама, ты — самая лучшая в мире! Спасибо за все, что ты делаешь для нас.</p>
        <button class="close-btn" onclick="closePopup();">Закрыть</button>
    </div>
</div>

<script>
    // Слайд-шоу
    let slideIndex = 0;

    function showSlides() {
        let slides = document.getElementsByClassName("slides");
        for (let i = 0; i < slides.length; i++) {
            slides[i].style.display = "none";
        }
        slideIndex++;
        if (slideIndex > slides.length) { slideIndex = 1 }
        slides[slideIndex - 1].style.display = "block";
        setTimeout(showSlides, 3000); // Изменение слайда каждые 3 секунды
    }

    showSlides(); // Инициализация слайд-шоу

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






