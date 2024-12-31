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
            <p class="subtitle">Дорогая тётя Ира!🎉🎂
Сегодня твой день, и мы хотим пожелать:
🌸 Радости, как весенний рассвет,
✨ Удачи, как звёзд на небе,
❤️ Любви, как в сказке!

Ты для нас самая добрая, милая и прекрасная! 💐
Пусть твоя улыбка 🌟 сияет ярче солнца,
А каждый новый день дарит счастье и тепло! ☀️

С Днём Рождения, любимая тётя! 🎁💖</p>
        </header>
        
        <main>
            <div class="slideshow">
                <img src="https://github.com/dian00-us/happy-birthday/blob/main/942b65b8-b19b-4b89-a812-61ca150a4f22.jpeg?raw=true" alt="Фото 1" class="slide active">
               
                <img src="https://github.com/dian00-us/happy-birthday/blob/main/82cbd7e6-d8cd-4b42-b1b0-b528fc3b52fc.jpeg?raw=true" alt="Фото 3" class="slide">
                <img src="https://github.com/dian00-us/happy-birthday/blob/main/6dd3d1a8-739c-481d-ae96-622b1df79a95.jpeg?raw=true" alt="Фото 4" class="slide">
                <img src="https://github.com/dian00-us/happy-birthday/blob/main/677c87cf-7bd9-4d08-b052-88dd159b7d5a.jpeg?raw=true" alt="Фото 5" class="slide">
                <img src="https://github.com/dian00-us/happy-birthday/blob/main/52709f16-9fe4-474f-9879-47130280f47b.jpeg?raw=true" alt="Фото 6" class="slide"> 
                <img src="https://github.com/dian00-us/happy-birthday/blob/main/44530081-a756-41de-859d-38e95d51c04f.jpeg?raw=true" alt="Фото 7" class="slide">
                <img src="https://github.com/dian00-us/happy-birthday/blob/main/40fffc53-7e82-47fb-ac0b-f387f766c6d9.jpeg?raw=true" alt="Фото 8" class="slide">
                <img src="https://github.com/dian00-us/happy-birthday/blob/main/1ae07659-6bb4-4246-8f07-d9e473c72b8c.jpeg?raw=true" alt="Фото 9" class="slide">
                <img src="https://github.com/dian00-us/happy-birthday/blob/main/16af279d-f3bc-4e29-9b83-7fdeb4f965a4.jpeg?raw=true" alt="Фото 10" class="slide">
                <img src="https://github.com/dian00-us/happy-birthday/blob/main/0931624b-3b7f-478e-aa8e-9ac997d264b0.jpeg?raw=true" alt="Фото 11" class="slide">
            </div>
            
            <button class="surprise-button">Нажми для сюрприза!</button>
            
            <div class="surprise hidden">
                <p>Ты самая лучшая тётя! Желаем счастья, здоровья и исполнения всех мечт❤️!</p>
        
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
