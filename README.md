<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Happy Birthday</title>
  <style>
    /* Общий стиль */
    body, html {
      margin: 0;
      padding: 0;
      font-family: 'Arial', sans-serif;
      height: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      overflow: hidden;
    }

    /* Фон */
    .background {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: linear-gradient(135deg, #f5d5a4, #fce4ec);
      overflow: hidden;
      z-index: -1;
    }

    /* Основной контент */
    .content {
      text-align: center;
      color: #6a4f4b;
      max-width: 90%;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
      padding: 20px;
      background-color: rgba(255, 255, 255, 0.8);
      border-radius: 15px;
    }

    /* Заголовок */
    h1 {
      font-size: 3em;
      font-weight: bold;
      color: #b87333;
      text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
      margin-bottom: 20px;
    }

    /* Слайд-шоу */
    .slideshow-container {
      position: relative;
      max-width: 100%;
      margin: auto;
    }

    .slide {
      display: none;
    }

    .slide img {
      width: 100%;
      border-radius: 10px;
    }

    .fade {
      animation: fadeEffect 2s infinite;
    }

    @keyframes fadeEffect {
      from { opacity: 0.4; }
      to { opacity: 1; }
    }

    /* Аудиоплеер */
    audio {
      margin-top: 20px;
      outline: none;
    }
  </style>
</head>
<body>
  <!-- Фоновый слой -->
  <div class="background"></div>

  <!-- Основной контент -->
  <div class="content">
    <h1>Happy Birthday!</h1>
    <div class="slideshow-container">
      <div class="slide fade">
        <img src="image1.jpg" alt="Balloons">
      </div>
      <div class="slide fade">
        <img src="image2.jpg" alt="Cake">
      </div>
      <div class="slide fade">
        <img src="image3.jpg" alt="Gifts">
      </div>
    </div>
    <audio controls autoplay loop>
      <source src="background-music.mp3" type="audio/mpeg">
      Your browser does not support the audio element.
    </audio>
  </div>

  <script>
    let slideIndex = 0;
    showSlides();

    function showSlides() {
      let slides = document.getElementsByClassName("slide");
      for (let i = 0; i < slides.length; i++) {
        slides[i].style.display = "none";
      }
      slideIndex++;
      if (slideIndex > slides.length) { slideIndex = 1 }
      slides[slideIndex - 1].style.display = "block";
      setTimeout(showSlides, 3000); // Смена каждые 3 секунды
    }
  </script>
</body>
</html>
