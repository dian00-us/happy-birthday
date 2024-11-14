<!DOCTYPE html>
<html lang="kk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Туған күніңмен!</title>
    <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Lora:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Lora', serif;
            background-color: #faf3e0;
            color: #333;
            margin: 0;
            padding: 0;
        }
        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
            background-color: #fff;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
            border-radius: 10px;
            position: relative;
        }
        .header {
            text-align: center;
            margin: 40px 0;
        }
        .header h1 {
            font-size: 3em;
            font-family: 'Great Vibes', cursive;
            color: #e63946;
            margin: 0;
        }
        .subheader {
            font-size: 1.5em;
            text-align: center;
            margin: 20px 0;
            font-style: italic;
            color: #6d6875;
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
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        }
        .text-box {
            width: 48%;
            text-align: left;
            color: #333;
        }
        .text-box p {
            font-size: 1.2em;
            line-height: 1.6;
        }
        .surprise {
            text-align: center;
            margin: 40px 0;
            position: relative;
        }
        .surprise button {
            background-color: #e63946;
            color: white;
            padding: 10px 20px;
            border: none;
            font-size: 1.2em;
            cursor: pointer;
            border-radius: 5px;
            transition: transform 0.2s;
        }
        .surprise button:hover {
            transform: scale(1.1);
        }
        .surprise-text {
            display: none;
            font-size: 1.2em;
            margin-top: 20px;
            color: #457b9d;
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
            background-color: #e63946;
        }

        /* Heart animations */
        @keyframes float {
            0% {
                opacity: 1;
                transform: translateY(0) scale(1);
            }
            100% {
                opacity: 0;
                transform: translateY(-200px) scale(0.5);
            }
        }
        .heart {
            position: absolute;
            bottom: 40px;
            left: 50%;
            font-size: 2em;
            color: #e63946;
            animation: float 2s infinite ease-in-out;
        }

        /* Confetti */
        .confetti {
            position: fixed;
            top: 0;
            left: 50%;
            width: 100px;
            height: 10px;
            animation: fall 3s ease forwards;
        }
        @keyframes fall {
            0% { transform: translateY(-100vh); opacity: 1; }
            100% { transform: translateY(100vh); opacity: 0; }
        }
    </style>
</head>
<body>

<div class="container">
    <div class="header">
        <h1>Туған күніңмен!</h1>
    </div>

    <div class="subheader">
        Махаббатқа, қуанышқа және сәттілікке толы жылдар тілеймін!
    </div>

    <div class="section">
        <img src="makeup-brushes.jpg" alt="Сервис">
        <div class="text-box">
            <p>Сізге денсаулық, бақыт және махаббат тілейміз! Әр күніңіз қуанышқа толы болсын, және әр сәт сізге жаңа қуаныш сыйласын!</p>
            <p>Әр жыл сізді қуанышқа толтырып, махаббатпен және жарықпен орап алсын!</p>
        </div>
    </div>

    <div class="surprise">
        <button onclick="showSurprise()">Сюрприз!</button>
        <p class="surprise-text" id="surprise-text">Бұл сізге арналған арнайы сыйлық! Бақытты күндеріңіз көп болсын!</p>
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

    <div class="heart" id="heart1">&#10084;</div>
    <div class="heart" id="heart2">&#10084;</div>
</div>

<script>
    // Heart animation
    setInterval(() => {
        let heart1 = document.getElementById("heart1");
        let heart2 = document.getElementById("heart2");
        heart1.style.left = `${50 + Math.random() * 10}%`;
        heart2.style.left = `${50 - Math.random() * 10}%`;
    }, 2000);

    // Surprise and Confetti
    function showSurprise() {
        document.getElementById('surprise-text').style.display = 'block';
        launchConfetti();
    }

    function launchConfetti() {
        for (let i = 0; i < 100; i++) {
            let confetti = document.createElement("div");
            confetti.classList.add("confetti");
            confetti.style.left = Math.random() * 100 + "vw";
            confetti.style.backgroundColor = `hsl(${Math.random() * 360}, 100%, 50%)`;
            document.body.appendChild(confetti);
            setTimeout(() => confetti.remove(), 3000);
        }
    }

    // Slideshow
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
