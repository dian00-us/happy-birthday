<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>С Днем Рождения!</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: linear-gradient(to right, #ffecd2, #fcb69f);
    }
    h1 {
      text-align: center;
      color: #ff6f61;
      margin: 20px;
    }
    .slideshow-container {
      max-width: 100%;
      position: relative;
      margin: auto;
    }
    .slide {
      display: none;
    }
    img {
      width: 100%;
      height: auto;
    }
    @keyframes fade {
      from {opacity: 0.4}
      to {opacity: 1}
    }
  </style>
</head>
<body>
  <h1>С Днем Рождения!</h1>

  <!-- Слайд-шоу -->
  <div class="slideshow-container">
    <div class="slide fade">
      <img src="image1.jpg" alt="Слайд 1">
    </div>
    <div class="slide fade">
      <img src="image2.jpg" alt="Слайд 2">
    </div>
    <div class="slide fade">
      <img src="image3.jpg" alt="Слайд 3">
    </div>
  </div>

  <!-- Фоновая музыка -->
  <audio autoplay loop>
    <source src="your-audio-file.mp3" type="audio/mpeg">
    Ваш браузер не поддерживает аудио.
  </audio>

  <script>
    // Слайд-шоу
    let slideIndex = 0;
    showSlides();

    function showSlides() {
      let slides = document.getElementsByClassName("slide");
      for (let i = 0; i < slides.length; i++) {
        slides[i].style.display = "none";
      }
      slideIndex++;
      if (slideIndex > slides.length) {slideIndex = 1}
      slides[slideIndex - 1].style.display = "block";
      setTimeout(showSlides, 3000); // Смена каждые 3 секунды
    }
  </script>
</body>
</html>
