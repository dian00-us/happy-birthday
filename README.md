<html lang="kk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Құттықтау</title>
    <style>
        body {
            background-color: #fbe7c6;
            font-family: 'Georgia', serif;
            color: #6c4f47;
            text-align: center;
            margin: 0;
            padding: 0;
        }

        .container {
            background-color: #fdf2e9;
            padding: 50px;
            border-radius: 15px;
            margin-top: 50px;
            width: 80%;
            max-width: 600px;
            box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
        }

        h1 {
            font-size: 2.5em;
            color: #ff6f61;
            font-family: 'Arial', sans-serif;
        }

        h2 {
            font-size: 1.5em;
            color: #b5645b;
            margin-top: 10px;
        }

        .content {
            font-size: 1.2em;
            line-height: 1.6;
            color: #6a4e4c;
        }

        .flower {
            width: 100px;
            height: 100px;
            background-image: url('https://example.com/flower.png');
            background-size: cover;
            display: inline-block;
            margin: 20px;
        }

        .footer {
            margin-top: 40px;
            font-size: 1.2em;
            color: #d45b5b;
        }

        .footer a {
            color: #d45b5b;
            text-decoration: none;
        }

        /* Слайдшоу */
        .slideshow-container {
            position: relative;
            max-width: 100%;
            margin-top: 30px;
        }

        .mySlides {
            display: none;
        }

        .img-slide {
            width: 100%;
            border-radius: 10px;
        }

        /* Стиль для окошек с сюрпризом */
        .surprise-box {
            display: inline-block;
            width: 150px;
            height: 150px;
            background-color: #ffdfdf;
            border: 2px solid #ff6f61;
            border-radius: 10px;
            margin: 15px;
            text-align: center;
            line-height: 150px;
            font-size: 1.5em;
            color: #ff6f61;
            cursor: pointer;
            position: relative;
        }

        .surprise-content {
            display: none;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 1.2em;
            color: #6a4e4c;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Құрметті анашым!</h1>
        <h2>50 жасқа толған мерейтойыңмен шын жүректен құттықтаймын!</h2>
        <div class="content">
            <p>Жақсы өмірдің үлгісін көрсетіп, бізді тәрбиеңмен өсіріп, сүйіспеншілігіңмен қоршап жүргенің үшін рахмет! 
            Сенің мейірімділігің, даналығың біз үшін әрдайым ең бағалы қазына. </p>
            <p>50 жас – өмірдің әсем және жарқын кезеңі, ал сен сол кезеңде де бізді сүйіп, қолдап, өзіңнің керемет жарқын бейнеңді 
            көрсетіп жүрсің. Біз сені өте жақсы көреміз!</p>
        </div>
        
        <!-- Слайдшоу -->
        <div class="slideshow-container">
            <div class="mySlides fade">
                <img src="https://via.placeholder.com/600x400?text=Сурет+1" class="img-slide">
            </div>
            <div class="mySlides fade">
                <img src="https://via.placeholder.com/600x400?text=Сурет+2" class="img-slide">
            </div>
            <div class="mySlides fade">
                <img src="https://via.placeholder.com/600x400?text=Сурет+3" class="img-slide">
            </div>
        </div>

        <!-- Окошки с сюрпризом -->
        <div class="surprise-box" onclick="showSurprise('surprise1')">
            <span>Бас</span>
            <div id="surprise1" class="surprise-content">
                <p>Бұл анамның ең жақсы күлімсіреуі!</p>
            </div>
        </div>
        <div class="surprise-box" onclick="showSurprise('surprise2')">
            <span>Бас</span>
            <div id="surprise2" class="surprise-content">
                <p>Сенің сүйіспеншілігің біз үшін үлкен сый!</p>
            </div>
        </div>
        <div class="surprise-box" onclick="showSurprise('surprise3')">
            <span>Бас</span>
            <div id="surprise3" class="surprise-content">
                <p>Біздің жүрегімізде мәңгілікке орын бар!</p>
            </div>
        </div>

        <div class="footer">
            <p>Сүйіспеншілікпен, сенің балаларың.</p>
        </div>
    </div>

    <script>
        // Слайдшоу
        let slideIndex = 0;
        showSlides();

        function showSlides() {
            let slides = document.getElementsByClassName("mySlides");
            for (let i = 0; i < slides.length; i++) {
                slides[i].style.display = "none";
            }
            slideIndex++;
            if (slideIndex > slides.length) {slideIndex = 1}
            slides[slideIndex-1].style.display = "block";
            setTimeout(showSlides, 3000); // Изменить картинку каждые 3 секунды
        }

        // Функция для отображения сюрприза
        function showSurprise(id) {
            let surpriseContent = document.getElementById(id);
            surpriseContent.style.display = surpriseContent.style.display === "block" ? "none" : "block";
        }
    </script>
</body>
</html>
