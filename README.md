<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday!</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background: radial-gradient(circle, #ff9a9e, #fad0c4, #fbc2eb);
            overflow: hidden;
            font-family: 'Poppins', sans-serif;
        }

        h1 {
            font-size: 4rem;
            color: #fff;
            text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.3);
            animation: fadeIn 2s ease-in-out;
        }

        .message {
            font-size: 1.5rem;
            color: #fff;
            margin-top: 20px;
            text-align: center;
            animation: fadeIn 3s ease-in-out;
        }

        .paragraphs {
            margin-top: 30px;
            font-size: 1.2rem;
            color: #fff;
            text-align: center;
            line-height: 1.6;
            animation: fadeIn 4s ease-in-out;
        }

        .balloon {
            position: absolute;
            width: 60px;
            height: 80px;
            background: radial-gradient(circle, #ff6f61 40%, #d32f2f);
            border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            animation: float 6s ease-in-out infinite;
        }

        .balloon:nth-child(odd) {
            background: radial-gradient(circle, #ffeb3b 40%, #f57c00);
        }

        .balloon:nth-child(even) {
            background: radial-gradient(circle, #8bc34a 40%, #4caf50);
        }

        .balloon:nth-child(3n) {
            background: radial-gradient(circle, #03a9f4 40%, #0288d1);
        }

        .balloon::after {
            content: '';
            position: absolute;
            width: 2px;
            height: 40px;
            background: #fff;
            bottom: -40px;
            left: 50%;
            transform: translateX(-50%);
        }

        @keyframes float {
            0% {
                transform: translateY(100vh);
                opacity: 0;
            }
            50% {
                opacity: 1;
            }
            100% {
                transform: translateY(-10vh);
                opacity: 0;
            }
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }
    </style>
</head>
<body>
    <h1>🎉 Happy Birthday! 🎂</h1>
    <div class="message">Wishing you a day filled with love, laughter, and joy!</div>
    <div class="paragraphs">
        <p>On this special day, may you be surrounded by the warmth of those who love you. Your presence lights up the lives of so many, and today we celebrate the joy you bring to the world.</p>
        <p>Here’s to a year ahead filled with endless opportunities, vibrant health, and cherished memories. May your heart be as full as the love that surrounds you, and may your dreams take flight just like the balloons soaring above.</p>
        <p>Happy Birthday! May each moment of today bring you closer to your aspirations and fill your heart with unending happiness. Cheers to you and the beautiful journey ahead!</p>
    </div>

    <script>
        // Function to create balloon elements
        function createBalloon() {
            const balloon = document.createElement('div');
            balloon.classList.add('balloon');
            
            // Randomize position and animation duration
            balloon.style.left = ${Math.random() * 100}vw;
            balloon.style.animationDuration = ${Math.random() * 3 + 4}s;
            
            document.body.appendChild(balloon);

            // Remove balloon after animation
            balloon.addEventListener('animationend', () => {
                balloon.remove();
            });
        }

        // Generate balloons continuously
        setInterval(createBalloon, 500);
    </script>
</body>
</html>
