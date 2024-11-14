<html lang="kk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Туған күніңізбен!</title>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@600&family=Great+Vibes&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Dancing Script', cursive;
            background: linear-gradient(135deg, #f5e1d8, #f1c6a1);
            color: #5e4a3a;
            margin: 0;
            padding: 0;
            overflow-x: hidden;
        }
        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
            background-color: #fff8f2;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
            border-radius: 10px;
            position: relative;
            transition: background-color 0.3s ease;
        }
        .header {
            text-align: center;
            margin: 40px 0;
        }
        .header h1 {
            font-size: 3.5em;
            font-family: 'Great Vibes', cursive;
            color: #a85d3a;
            margin: 0;
        }
        .subheader {
            font-size: 1.8em;
            text-align: center;
            margin: 20px 0;
            font-style: italic;
            color: #7a5038;
            font-family: 'Great Vibes', cursive;
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
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s ease;
        }
        .section img:hover {
            transform: scale(1.05);
        }
        .text-box {
            width: 48%;
            text-align: left;
        }
        .envelope {
            background-color: #fff8f2;
            border: 2px solid #a85d3a;
            padding: 20px;
            border-radius: 10px;
            position: relative;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            transition: border-color 0.3s ease, background-color 0.3s ease;
        }
        .envelope:hover {
            background-color: #f1d4c4;
            border-color: #8c4734;
        }
        .envelope:before {
            content: "";
            position: absolute;
            top: -15px;
            left: 50%;
            transform: translateX(-50%);
            border-left: 20px solid transparent;
            border-right: 20px solid transparent;
            border-bottom: 20px solid #a85d3a;
        }
        .envelope p {
            color: #5e4a3a;
            font-size: 1.3em;
            line-height: 1.6;
            font-family: 'Great Vibes', cursive;
        }
        .surprise {
            text-align: center;
            margin: 40px 0;
        }
        .surprise button {
            background-color: #a85d3a;
            color: white;
            padding: 12px 25px;
            border: none;
            font-size: 1.2em;
            cursor: pointer;
            border-radius: 8px;
            transition: transform 0.2s, background-color 0.3s;
            font-family: 'Dancing Script', cursive;
        }
        .surprise button:hover {
            transform: scale(1.1);
            background-color: #8c4734;
        }
        .surprise-text {
            display: none;
            font-size: 1.4em;
            margin-top: 20px;
            color: #7a5038;
            font-family: 'Great Vibes', cursive;
        }
        .slideshow-container {
            position: relative;
            max-width: 100%;
            margin: auto;
        }
        .slides {
            display: none;
            text-align: center;
            transition: opacity 1s ease;
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
            background-color: #a85d3a;
        }

        /* Confetti animation (firework effect) */
        .confetti {
            position: fixed;
            width: 5px;
            height: 5px;
            background: #f9a1bc;
            opacity: 0;
            top: 50%;
            left: 50%;
            animation: firework 1.5s ease-out forwards;
        }
        @keyframes firework {
            0% { opacity: 1; transform: translate(-50%, -50%) scale(1); }
            100% { opacity: 0; transform: translate(-50%, -50%) scale(4); }
        }

        /* Number "50" animation */
        .fifty {
            position: relative;
            top: 20px;
            left: 50%;
            font-size: 5em;
            font-weight: bold;
            color: #a85d3a;
            opacity: 0;
            transform: translateX(-50%) scale(1);
            animation: scaleUp 3s ease-in-out infinite;
            font-family: 'Great Vibes', cursive;
        }
        @keyframes scaleUp {
            0%, 100% { opacity: 0; transform: translateX(-50%) scale(1); }
            50% { opacity: 1; transform: translateX(-50%) scale(1.5); }
        }

        /* Music button */
        .music-container {
            position: absolute;
            top: 10px;
            right: 10px;
        }
        .music-container button {
            background-color: #a85d3a;
            color: white;
            padding: 12px 20px;
            border: none;
            font-size: 1.2em;
            cursor: pointer;
            border-radius: 8px;
        }
        .music-container button:hover {
            background-color: #8c4734;
        }
    </style>
</head>
<body>

<div class="container">
    <!-- Favicon audio for background music -->
    <audio id="background-music" autoplay loop>
        <source src="https://github.com/dian00-us/birthday/raw/main/birthday_song.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
    </audio>

    <!-- Music control button -->
    <div class="music-container">
        <button onclick="toggleMusic()">music</button>
    </div>

    <div class="header">
        <h1>Туған күніңізбен!</h1>
    </div>

    <div class="subheader">
        Құрметті анашым, сізді 50 жылдық мерей тойыңызбен құттықтаймын!!!
    </div>

    <div class="section">
        <img src="https://gas-kvas.com/grafic/uploads/posts/2024-01/gas-kvas-com-p-tsvetochki-krasivie-na-prozrachnom-fone-33.png" alt="Сервис">
        <div class="text-box envelope">
            <p>Сізге денсаулық, бақыт және махаббат тілейміз! Әр күніңіз қуанышқа толы болсын, және әр сәт сізге жаңа қуаныш сыйласын❤️</p>
            <p>Анашым, 50 жыл бойы сіздің мейіріміңіз бен сүйіспеншілігіңіз менің өмірімді жарықтандырып келеді. Сіздің күлкіңіз мен үшін ең қымбат нәрсе, сол үшін еш мұңаймай, тек күлімсіреп жүруіңізді қалаймын. Алдағы өмір жолыңда денсаулығыңыз мықты болып, қуаныш пен бақыт әрдайым серігіңіз болсын, арман-мақсаттарыңыз орындалып, өмірдің ең әдемі сәттерін өзіңізге тарту етсін!!💖💖💖</p>
        </div>
    </div>

    <div class="fifty">50</div>

    <div class="surprise">
        <button onclick="showSurprise()">Бұл сізгееее</button>
        <p class="surprise-text" id="surprise-text">Мен сізді жақсы көремін, туған күніңіз құтты болсын❤️</p>
    </div>

    <div class="slideshow-container">
        <div class="slides">
            <img src="https://github.com/dian00-us/happy-birthday/blob/main/ph1.jpg?raw=true" alt="Фото 1">
        </div>
        <div class="slides">
            <img src="https://github.com/dian00-us/happy-birthday/blob/main/ph2.jpg?raw=true" alt="Фото 2">
        </div>
        <div class="slides">
            <img src="https://github.com/dian00-us/happy-birthday/blob/main/ph3.jpg?raw=true" alt="Фото 3">
        </div> 
        <div class="slides">
            <img src="https://github.com/dian00-us/happy-birthday/blob/main/ph4.jpg?raw=true" alt="Фото 4">
        </div> 
        <div class="slides">
            <img src="https://github.com/dian00-us/happy-birthday/blob/main/ph5.jpg?raw=true" alt="Фото 5">
        </div>
        <div class="slides">
            <img src="https://github.com/dian00-us/happy-birthday/blob/main/ph6.jpg?raw=true" alt="Фото 6">
        </div>
        <div class="slides">
            <img src="https://github.com/dian00-us/happy-birthday/blob/main/ph7.jpg?raw=true" alt="Фото 7">
        </div>
        <div class="slides">
            <img src="https://github.com/dian00-us/happy-birthday/blob/main/ph8.jpg?raw=true" alt="Фото 8">
        </div>
        <div class="slides">
            <img src="https://github.com/dian00-us/happy-birthday/blob/main/ph9.jpg?raw=true" alt="Фото 9">
        </div>
        <div class="slides">
            <img src="https://github.com/dian00-us/happy-birthday/blob/main/ph10.jpg?raw=true" alt="Фото 10">
        </div>
        <div class="slides">
            <img src="https://github.com/dian00-us/happy-birthday/blob/main/ph11.jpg?raw=true" alt="Фото 11">
        </div>
        <div class="slides">
            <img src="https://github.com/dian00-us/happy-birthday/blob/main/ph12.jpg?raw=true" alt="Фото 12">
        </div>
    </div>
    
    <div class="dots">
        <span class="dot" onclick="currentSlide(1)"></span> 
        <span class="dot" onclick="currentSlide(2)"></span> 
        <span class="dot" onclick="currentSlide(3)"></span> 
    </div>
</div>

<script>
    // Show surprise with confetti
    function showSurprise() {
        document.getElementById('surprise-text').style.display = 'block';
        launchConfetti();
    }

    function launchConfetti() {
        for (let i = 0; i < 50; i++) {
            let confetti = document.createElement("div");
            confetti.classList.add("confetti");
            confetti.style.left = (Math.random() * 100) + "vw";
            confetti.style.top = (Math.random() * 100) + "vh";
            confetti.style.backgroundColor = `hsl(${Math.random() * 360}, 100%, 70%)`;
            document.body.appendChild(confetti);
            setTimeout(() => confetti.remove(), 1500);
        }
    }

    // Automatic Slideshow
    let slideIndex = 0;
    function showSlides() {
        let i;
        let slides = document.getElementsByClassName("slides");
        for (i = 0; i < slides.length; i++) {
            slides[i].style.display = "none";  
        }
        slideIndex++;
        if (slideIndex > slides.length) {slideIndex = 1}    
        slides[slideIndex - 1].style.display = "block";  
        setTimeout(showSlides, 1500); // Faster transition
    }
    showSlides();

    // Toggle music
    function toggleMusic() {
        var audio = document.getElementById("background-music");
        if (audio.paused) {
            audio.play();
        } else {
            audio.pause();
        }
    }
</script>

</body>
</html>
