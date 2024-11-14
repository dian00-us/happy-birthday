
<html lang="kk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>С Днем Рождения</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f9f9f9;
            color: #333;
            margin: 0;
            padding: 0;
        }
        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
            text-align: center;
        }
        h1 {
            font-size: 3em;
            margin-bottom: 20px;
        }
        .message {
            font-size: 1.2em;
            margin-bottom: 30px;
        }
        .surprise-box {
            margin-bottom: 30px;
        }
        .surprise-box button {
            background-color: #333;
            color: white;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
            font-size: 1em;
        }
        .slideshow-container {
            position: relative;
            max-width: 100%;
            margin: auto;
        }
        .slides {
            display: none;
        }
        .slides img {
            width: 100%;
            border-radius: 8px;
        }
        .prev, .next {
            cursor: pointer;
            position: absolute;
            top: 50%;
            width: auto;
            padding: 16px;
            color: white;
            font-weight: bold;
            font-size: 18px;
            transition: 0.6s ease;
            border-radius: 0 3px 3px 0;
            user-select: none;
        }
        .next {
            right: 0;
            border-radius: 3px 0 0 3px;
        }
        .prev:hover, .next:hover {
            background-color: rgba(0,0,0,0.8);
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Туған күніңмен!</h1>
    <div class="message">
        Сізге денсаулық, бақыт және махаббат тілейміз! Әр күніңіз қуанышқа толы болсын!
    </div>

    <div class="surprise-box">
        <button onclick="showSurprise()">Сюрприз!</button>
        <p id="surprise-text" style="display:none; font-size:1.2em; margin-top:20px;">Бұл сізге арналған арнайы сыйлық!</p>
    </div>

    <div class="slideshow-container">
        <div class="slides">
            <img src="photo1.jpg" alt="Фото 1">
        </div>
        <div class="slides">
            <img src="photo2.jpg" alt="Фото 2">
        </div>
        <div class="slides">
            <img src="photo3.jpg" alt="Фото 3">
        </div>

        <a class="prev" onclick="changeSlide(-1)">&#10094;</a>
        <a class="next" onclick="changeSlide(1)">&#10095;</a>
    </div>
</div>

<script>
    let slideIndex = 0;

    function showSurprise() {
        document.getElementById('surprise-text').style.display = 'block';
    }

    function showSlides() {
        let slides = document.getElementsByClassName("slides");
        for (let i = 0; i < slides.length; i++) {
            slides[i].style.display = "none";
        }
        slideIndex++;
        if (slideIndex > slides.length) {slideIndex = 1}
        slides[slideIndex-1].style.display = "block";
        setTimeout(showSlides, 3000); // Change image every 3 seconds
    }

    function changeSlide(n) {
        slideIndex += n;
        let slides = document.getElementsByClassName("slides");
        if (slideIndex > slides.length) {slideIndex = 1}
        if (slideIndex < 1) {slideIndex = slides.length}
        for (let i = 0; i < slides.length; i++) {
            slides[i].style.display = "none";
        }
        slides[slideIndex-1].style.display = "block";
    }

    showSlides();
</script>

</body>
</html>







