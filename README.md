<!DOCTYPE html>
<html lang="kk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Туған күніңмен!</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            color: #333;
            margin: 0;
            padding: 0;
        }
        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
            background-color: #fff;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .header {
            text-align: center;
            margin: 40px 0;
        }
        .header h1 {
            font-size: 2.5em;
            font-weight: bold;
            margin: 0;
        }
        .subheader {
            font-size: 1.5em;
            text-align: center;
            margin: 20px 0;
            font-style: italic;
        }
        .section {
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin: 40px 0;
        }
        .section img {
            width: 48%;
            border-radius: 8px;
        }
        .text-box {
            width: 48%;
            text-align: left;
        }
        .text-box p {
            font-size: 1.2em;
            line-height: 1.6;
        }
        .surprise {
            text-align: center;
            margin: 40px 0;
        }
        .surprise button {
            background-color: #333;
            color: #fff;
            padding: 10px 20px;
            border: none;
            font-size: 1.2em;
            cursor: pointer;
        }
        .surprise-text {
            display: none;
            font-size: 1.2em;
            margin-top: 20px;
        }
        .slideshow-container {
            position: relative;
            max-width: 100%;
            margin: auto;
        }
        .slides {
            display: none;
            text-align: center;
        }
        .slides img {
            width: 100%;
            max-width: 800px;
            border-radius: 8px;
        }
        .dots {
            text-align: center;
            margin-top: 10px;
        }
        .dots span {
            cursor: pointer;
            height: 15px;
            width: 15px;
            margin: 0 5px;
            background-color: #bbb;
            border-radius: 50%;
            display: inline-block;
        }
        .dots .active {
            background-color: #333;
        }
    </style>
</head>
<body>

<div class="container">
    <div class="header">
        <h1>Туған күніңмен!</h1>
    </div>

    <div class="subheader">
        Для самой любимой мамы!
    </div>

    <div class="section">
        <img src="makeup-brushes.jpg" alt="Сервис">
        <div class="text-box">
            <p>Сізге денсаулық, бақыт және махаббат тілейміз! Әр күніңіз қуанышқа толы болсын, және әр сәт сізге жаңа қуаныш сыйласын!</p>
        </div>
    </div>

    <div class="surprise">
        <button onclick="showSurprise()">Сюрприз!</button>
        <p class="surprise-text" id="surprise-text">Бұл сізге арналған арнайы сыйлық!</p>
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
    </div>
    
    <div class="dots">
        <span class="dot" onclick="currentSlide(1)"></span> 
        <span class="dot" onclick="currentSlide(2)"></span> 
        <span class="dot" onclick="currentSlide(3)"></span> 
    </div>
</div>

<script>
    function showSurprise() {
        document.getElementById('surprise-text').style.display = 'block';
    }

    let slideIndex = 1;
    showSlides(slideIndex);

    function currentSlide(n) {
        showSlides(slideIndex = n);
    }

    function showSlides(n) {
        let i;
        let slides = document.getElementsByClassName("slides");
        let dots = document.getElementsByClassName("dot");
        if (n > slides.length) {slideIndex = 1}
        if (n < 1) {slideIndex = slides.length}
        for (i = 0; i < slides.length; i++) {
            slides[i].style.display = "none";  
        }
        for (i = 0; i < dots.length; i++) {
            dots[i].className = dots[i].className.replace(" active", "");
        }
        slides[slideIndex-1].style.display = "block";  
        dots[slideIndex-1].className += " active";
    }
</script>

</body>
</html>






