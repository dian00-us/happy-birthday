<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>С Днем Рождения, Мама!</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #fff0f5;
            color: #8e44ad;
            text-align: center;
        }
        .container {
            margin: 20px auto;
            max-width: 600px;
            padding: 20px;
            border: 2px solid #f8bbd0;
            border-radius: 15px;
            background-color: #fdf5e6;
            position: relative;
        }
        h1 {
            color: #d81b60;
        }
        .slideshow-container {
            position: relative;
            max-width: 100%;
            margin: auto;
        }
        .slide {
            display: none;
        }
        img {
            width: 100%;
            border-radius: 10px;
        }
        .message {
            margin-top: 20px;
            padding: 15px;
            border: 2px dashed #f06292;
            border-radius: 10px;
            background-color: #fce4ec;
            font-size: 1.2em;
        }
        .heart, .balloon {
            position: absolute;
            width: 50px;
            height: 50px;
            animation: float 5s infinite ease-in-out;
        }
        .heart {
            background: url('heart.png') no-repeat center;
            background-size: cover;
        }
        .balloon {
            background: url('balloon.png') no-repeat center;
            background-size: cover;
        }
        @keyframes float {
            0% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
            100% { transform: translateY(0); }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>С Днем Рождения, Мама!</h1>
        <div class="slideshow-container">
            <div class="slide">
                <img src="photo1.jpg" alt="Фото 1">
            </div>
            <div class="slide">
                <img src="photo2.jpg" alt="Фото 2">
            </div>
            <div class="slide">
                <img src="photo3.jpg" alt="Фото 3">
            </div>
        </div>
        <div class="message">
            Дорогая мама, поздравляю тебя с 50-летием! Ты самая замечательная и любимая мама в мире! Желаю тебе счастья, здоровья и любви!
        </div>
        <div class="heart" style="top: 10px; left: 10px;"></div>
        <div class="balloon" style="bottom: 10px; right: 10px;"></div>
    </div>

    <audio controls autoplay loop>
        <source src="song.mp3" type="audio/mp3">
        Your browser does not support the audio element.
    </audio>

    <script>
        let slideIndex = 0;
        showSlides();

        function showSlides() {
            let slides = document.getElementsByClassName("slide");
            for (let i = 0; i < slides.length; i++) {
                slides[i].style.display = "none";
            }
            slideIndex++;
            if (slideIndex > slides.length) {
                slideIndex = 1;
            }
            slides[slideIndex - 1].style.display = "block";
            setTimeout(showSlides, 3000); // Change image every 3 seconds
        }
    </script>
</body>
</html>


