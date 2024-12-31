
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>С Днём Рождения!</title>
    <style>
        body {
            margin: 0;
            font-family: 'Arial', sans-serif;
            background-color: #fef7f2;
            color: #5f4b3b;
        }

        .container {
            text-align: center;
            padding: 20px;
        }

        header {
            margin-bottom: 20px;
        }

        header h1 {
            font-size: 2.5em;
            color: #c79a7e;
        }

        .subtitle {
            font-size: 1.2em;
            color: #805f4c;
        }

        .slideshow {
            margin: 20px auto;
            width: 80%;
            max-width: 600px;
            position: relative;
            overflow: hidden;
            border-radius: 10px;
        }

        .slide {
            width: 100%;
            display: none;
            border-radius: 10px;
        }

        .slide.active {
            display: block;
        }

        .surprise-button {
            background-color: #f7d9c4;
            border: none;
            padding: 15px 30px;
            font-size: 1.2em;
            color: #5f4b3b;
            cursor: pointer;
            border-radius: 5px;
            margin: 20px 0;
            transition: 0.3s ease;
        }

        .surprise-button:hover {
            background-color: #d7b59e;
        }

        .surprise {
            margin: 20px 0;
            font-size: 1.5em;
        }

        .hidden {
            display: none;
        }

        .heart {
            width: 100px;
            margin-top: 20px;
        }

        footer {
            margin-top: 20px;
            padding: 10px;
            background-color: #e9d3bf;
            color: #5f4b3b;
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>С Днём Рождения, тётя!</h1>
            <p class="subtitle">Мы тебя очень любим! Пусть этот день будет самым счастливым для тебя!</p>
        </header>
        
        <main>
            <div class="slideshow">
                <img src="photo1.jpg" alt="Фото 1" class="slide active">
                <img src="photo2.jpg" alt="Фото 2" class="slide">
                <img src="photo3.jpg" alt="Фото 3" class="slide">
            </div>
            
            <button class="surprise-button">Нажми для сюрприза!</button>
            
            <div class="surprise hidden">
                <p>Ты самая лучшая тётя! Желаем счастья, здоровья и исполнения всех мечт!</p>
                <img src="heart.png" alt="Сердечко" class="heart">
            </div>
        </main>
        
        <footer>
            <p>© 2024 С любовью, от твоей племянницы</p>
        </footer>
    </div>
    <audio id="background-music" autoplay loop>
        <source src="https://github.com/dian00-us/birthday/raw/main/birthday_song.mp3" type="audio/mpeg">
    </audio>
    <script>
        // Слайд-шоу
        let currentSlide = 0;
        const slides = document.querySelectorAll('.slide');

        function showSlide(index) {
            slides.forEach((slide, i) => {
                slide.classList.remove('active');
                if (i === index) {
                    slide.classList.add('active');
                }
            });
        }

        setInterval(() => {
            currentSlide = (currentSlide + 1) % slides.length;
            showSlide(currentSlide);
        }, 3000);

        // Кнопка-сюрприз
        const surpriseButton = document.querySelector('.surprise-button');
        const surprise = document.querySelector('.surprise');

        surpriseButton.addEventListener('click', () => {
            surprise.classList.toggle('hidden');
            surpriseButton.textContent = surprise.classList.contains('hidden') 
                ? 'Нажми для сюрприза!' 
                : 'Сюрприз открыт!';
        });
    </script>
</body>
</html>
