<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Мир Котиков с аудио 🐾</title>
    <style>
        :root {
            --pink-light: #fff0f5;
            --pink-main: #ffb6c1;
            --pink-dark: #ff69b4;
            --text-color: #4a4a4a;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--pink-light);
            color: var(--text-color);
            margin: 0;
            padding: 0;
        }

        header {
            background: linear-gradient(135deg, var(--pink-main), #ffe4e1);
            padding: 40px 20px;
            text-align: center;
            box-shadow: 0 4px 10px rgba(0,0,0,0.05);
        }

        h1 {
            margin: 0;
            font-size: 3em;
            color: white;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
        }

        .subtitle {
            font-size: 1.2em;
            color: #6a6a6a;
            margin-top: 10px;
        }

        .container {
            max-width: 1000px;
            margin: 30px auto;
            padding: 0 20px;
        }

        .compliment-box {
            background: white;
            padding: 25px;
            border-radius: 20px;
            text-align: center;
            box-shadow: 0 8px 20px rgba(255, 182, 193, 0.3);
            margin-bottom: 40px;
        }

        #compliment-text {
            font-size: 1.4em;
            font-weight: bold;
            color: var(--pink-dark);
            margin-bottom: 15px;
            min-height: 40px;
            transition: opacity 0.2s ease;
        }

        button {
            background-color: var(--pink-dark);
            color: white;
            border: none;
            padding: 12px 28px;
            font-size: 1.1em;
            border-radius: 30px;
            cursor: pointer;
            box-shadow: 0 4px 15px rgba(255, 105, 180, 0.4);
            transition: all 0.3s ease;
        }

        button:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(255, 105, 180, 0.6);
        }

        .gallery-title {
            text-align: center;
            font-size: 2em;
            color: var(--pink-dark);
            margin-bottom: 5px;
        }

        .gallery-subtitle {
            text-align: center;
            color: #888;
            margin-bottom: 25px;
            font-size: 1em;
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
        }

        .cat-card {
            background: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            cursor: pointer;
        }

        .cat-card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 12px 25px rgba(255, 182, 193, 0.5);
        }

        .cat-card img {
            width: 100%;
            height: 250px;
            object-fit: cover;
        }

        .cat-info {
            padding: 20px;
            text-align: center;
        }

        .cat-info h3 {
            margin: 0 0 10px 0;
            color: #333;
        }

        .cat-info p {
            margin: 0;
            color: #777;
            font-style: italic;
        }

        footer {
            text-align: center;
            padding: 30px;
            color: #aaa;
            font-size: 0.9em;
        }
    </style>
</head>
<body>

    <header>
        <h1>Мур-Клуб 🐾</h1>
        <div class="subtitle">Самое уютное место в интернете</div>
    </header>

    <div class="container">
        
        <div class="compliment-box">
            <div id="compliment-text">Нажми на кнопку, чтобы получить кошачье предсказание! ✨</div>
            <button onclick="generateCompliment()">Узнать предсказание 🐱</button>
        </div>

        <h2 class="gallery-title">Наши пушистые друзья</h2>
        <div class="gallery-subtitle">Нажми на любого котика, чтобы он мяукнул! 🔊</div>
        
        <div class="gallery">
            
            <!-- Клик на карточку вызывает функцию playMeow() -->
            <div class="cat-card" onclick="playMeow()">
                <img src="https://unsplash.com" alt="Милый котик">
                <div class="cat-info">
                    <h3>Зефирка</h3>
                    <p>Профессионально спит 18 часов в сутки.</p>
                </div>
            </div>

            <div class="cat-card" onclick="playMeow()">
                <img src="https://unsplash.com" alt="Рыжий кот">
                <div class="cat-info">
                    <h3>Персик</h3>
                    <p>Генератор громкого мурчания и уюта.</p>
                </div>
            </div>

            <div class="cat-card" onclick="playMeow()">
                <img src="https://unsplash.com" alt="Кот в очках">
                <div class="cat-info">
                    <h3>Мурзик</h3>
                    <p>Эксперт по выпрашиванию вкусняшек.</p>
                </div>
            </div>

        </div>
    </div>

    <footer>
        <p>© 2026 Создано с любовью и лапками 🐾</p>
    </footer>

    <script>
        const compliments = [
            "Сегодня идеальный день, чтобы полежать кусь-кусь! 🐾",
            "Ты заслуживаешь самую большую порцию вкусняшек! 🍖",
            "Твое мурчание сделало бы этот мир лучше. Мяу! ❤️",
            "Кто-то думает о тебе прямо сейчас (и это котик). 🐱",
            "Ты топчешь этот мир своими лапками очень грациозно! ✨",
            "Все твои дела пройдут гладко, как шелковая шёрстка! 🌟"
        ];

        // Массив со ссылками на открытые аудиофайлы кошачьего мяуканья
        const meowSounds = [
            "https://mixkit.co",
            "https://google.com",
            "https://google.com"
        ];

        function generateCompliment() {
            const textElement = document.getElementById('compliment-text');
            const randomIndex = Math.floor(Math.random() * compliments.length);
            
            textElement.style.opacity = 0;
            
            setTimeout(() => {
                textElement.innerText = compliments[randomIndex];
                textElement.style.opacity = 1;
            }, 200);
        }

        // Функция воспроизведения случайного мяуканья
        function playMeow() {
            const randomIndex = Math.floor(Math.random() * meowSounds.length);
            const audio = new Audio(meowSounds[randomIndex]);
            audio.volume = 0.6; // Комфортная громкость
            audio.play().catch(error => {
                console.log("Браузер заблокировал автовоспроизведение. Нужно сначала кликнуть по странице.");
            });
        }
    </script>

</body>
</html>
