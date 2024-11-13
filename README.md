<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Поздравление с 50-летием!</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background: #f0e6f6;
            margin: 0;
            padding: 0;
            color: #333;
            overflow: hidden; /* Убираем полосу прокрутки */
            position: relative;
        }

        /* Плавный фон с градиентом */
        .background {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(to bottom, #ff9a9e, #fad0c4);
            z-index: -1;
        }

        header {
            text-align: center;
            background: #ffcc99;
            padding: 20px;
            border-radius: 0 0 30px 30px;
        }
        
        header h1 {
            font-size: 2.5em;
            color: #a15d48;
            margin: 0;
        }

        header p {
            font-size: 1.2em;
            color: #7a4f35;
            margin-top: 10px;
        }

        .content {
            padding: 20px;
            text-align: center;
        }

        .slideshow-container {
            max-width: 600px;
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
            background-color: #f49e7e;
            color: white;
            border: none;
            padding: 10px 20px;
            font-size: 1.2em;
            cursor: pointer;
            border-radius: 5px;
            margin-top: 20px;
            transition: background-color 0.3s;
        }

        .button:hover {
            background-color: #d78f6c;
        }

        .message-box {
            background: #f5d0a9;
            padding: 20px;
            border-radius: 10px;
            margin-top: 20px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .message-box h2 {
            font-size: 2.5em;
            color: #7a4f35;
            margin: 0;
        }

        .message-box p {
            font-size: 1.2em;
            color: #5c3b2f;
            margin-top: 10px;
        }

        /* Анимация сердечек */
        .heart {
            position: absolute;
            font-size: 40px;
            color: #ff4b5c;
            animation: float 10s infinite;
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

        /* Стиль для кнопки на мобильных устройствах */
        @media (max-width: 600px) {
            header h1 {
                font-size: 2em;
            }

            .message-box h2 {
                font-size: 2em;
            }

            .button {
                font-size: 1em;
                padding: 8px 15px;
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

    <button class="button" onclick="window.scrollTo(0, document.body.scrollHeight);">Посмотреть поздравление</button>

    <!-- Окно с поздравлением -->
    <div class="message-box">
        <h2>Дорогая мама!</h2>
        <p>Поздравляю тебя с 50-летием! Ты — невероятная, добрая, заботливая и любящая. Ты — наша поддержка и вдохновение. Пусть этот день будет наполнен счастьем, радостью и самыми светлыми моментами. Мы тебя очень любим!</p>
    </div>
</div>

<!-- Анимация сердечек -->
<div class="heart" style="top: 10%; left: 20%;">❤️</div>
<div class="heart" style="top: 30%; left: 40%;">❤️</div>
<div class="heart" style="top: 50%; left: 60%;">❤️</div>
<div class="heart" style="top: 70%; left: 80%;">❤️</div>
<div class="heart" style="top: 80%; left: 15%;">❤️</div>

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
</script>

</body>
</html>




