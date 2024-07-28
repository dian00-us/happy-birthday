<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday</title>
    <style>
        body {
            font-family: 'Georgia', serif;
            background: linear-gradient(120deg, #f6d365 0%, #fda085 100%);
            color: #333;
            text-align: center;
            padding: 20px;
            margin: 0;
        }
        .container {
            background: #ffffff;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
            max-width: 700px;
            margin: 20px auto;
        }
        h1 {
            color: #FF6347;
            font-size: 36px;
            margin-bottom: 20px;
        }
        p {
            font-size: 18px;
            line-height: 1.6;
            margin: 10px 0;
        }
        .heart {
            color: #FF6347;
            font-size: 48px;
            margin: 20px 0;
        }
        .slideshow-container {
            position: relative;
            max-width: 100%;
            margin: 20px auto;
        }
        .slides {
            display: none;
        }
        .active {
            display: block;
        }
        .fade {
            animation: fadeEffect 1.5s;
        }
        @keyframes fadeEffect {
            from {opacity: 0.4} 
            to {opacity: 1}
        }
        @media (min-width: 768px) {
            h1 {
                font-size: 48px;
            }
            p {
                font-size: 20px;
            }
        }
        .audio-control {
            margin: 20px 0;
        }
        .audio-control button {
            background-color: #FF6347;
            color: white;
            border: none;
            padding: 15px 30px;
            font-size: 18px;
            border-radius: 10px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        .audio-control button:hover {
            background-color: #ff4500;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Даниял, туған күніңмен!!!</h1>
        <div class="heart">❤</div>
        <p>Қымбатты Даниял,</p>
        <p> Төртінші туған күнің құтты болсын! Сенің әрбір күнің жарық, қуанышқа толы және қызыққа бай болсын. Сен біздің өміріміздің ең жарқын жұлдызысың, және біз сенің өсіп, дамып жатқаныңды көргенімізге қуаныштымыз.

            Төрт жасқа толу - бұл үлкен кезең! Әр күні жаңа нәрселерді үйреніп, қызықты достар тауып, керемет сәттерді бастан кешір. Біздің саған деген махаббатымыз шексіз, және біз сенің әрбір қадамыңды қолдаймыз.

            Денсаулығың мықты, күлкің ешқашан үзілмесін. Сенің армандарың орындалсын, ал болашағың жарқын болсын. Біздің сүйікті кішкентайымыз, біз сені мақтан тұтамыз және сені өте жақсы көреміз!

        </p>
        <p>Ізгі ниетпен, </p>
        <p>Жақын адамдарын</p>
        
        <div class="slideshow-container">
            <div class="slides fade">
                <img src="C:\Users\THINKPAD\Desktop\birthday\images\image1.jpg" style="width:100%; border-radius: 10px;">
            </div>
            <div class="slides fade">
                <img src="C:\Users\THINKPAD\Desktop\birthday\images\image2.jpg" style="width:100%; border-radius: 10px;">
            </div>
            <div class="slides fade">
                <img src="C:\Users\THINKPAD\Desktop\birthday\images\image3.jpg" style="width:100%; border-radius: 10px;">
            </div>
            <div class="slides fade">
                <img src="C:\Users\THINKPAD\Desktop\birthday\images\image4.jpg" style="width:100%; border-radius: 10px;">
            </div>
            <div class="slides fade">
                <img src="C:\Users\THINKPAD\Desktop\birthday\images\image5.jpg" style="width:100%; border-radius: 10px;">
            </div>
            <div class="slides fade">
                <img src="C:\Users\THINKPAD\Desktop\birthday\images\image6.jpg" style="width:100%; border-radius: 10px;">
            </div>
            <div class="slides fade">
                <img src="C:\Users\THINKPAD\Desktop\birthday\images\image7.jpg" style="width:100%; border-radius: 10px;">
            </div>
            <div class="slides fade">
                <img src="C:\Users\THINKPAD\Desktop\birthday\images\image8.jpg" style="width:100%; border-radius: 10px;">
            </div>
            <div class="slides fade">
                <img src="C:\Users\THINKPAD\Desktop\birthday\images\image9.jpg" style="width:100%; border-radius: 10px;">
            </div>
            <div class="slides fade">
                <img src="C:\Users\THINKPAD\Desktop\birthday\images\image10.jpg" style="width:100%; border-radius: 10px;">
            </div>
            <div class="slides fade">
                <img src="C:\Users\THINKPAD\Desktop\birthday\images\image11.jpg" style="width:100%; border-radius: 10px;">
            </div>
            <div class="slides fade">
                <img src="C:\Users\THINKPAD\Desktop\birthday\images\image12.jpg" style="width:100%; border-radius: 10px;">
            </div>
        </div>
    </div>

    <div class="audio-control">
        <button onclick="playAudio()">Включить музыку</button>
        <audio id="birthdayAudio">
            <source src="C:\Users\THINKPAD\Desktop\birthday\music\birthday_song.mp3" type="audio/mp3">
            Ваш браузер не поддерживает воспроизведение аудио.
        </audio>
    </div>

    <script>
        let slideIndex = 0;
        showSlides();

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

        function playAudio() {
            document.getElementById("birthdayAudio").play();
        }
    </script>
</body>
</html>
