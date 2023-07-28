<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mysterious Night Sky</title>
    <style>
        body {
            background-color: #000;
            color: #fff;
            font-family: 'Arial', sans-serif;
            text-align: center;
            margin: 0;
            padding: 0;
        }

        #stars {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
        }

        .star {
            position: absolute;
            background-color: #fff;
            border-radius: 50%;
            opacity: 0.8;
        }

        @keyframes twinkle {
            0% { opacity: 0; transform: scale(1); }
            50% { opacity: 0.8; transform: scale(1.2); }
            100% { opacity: 0; transform: scale(1); }
        }

        h1, p {
            margin: 30px 0;
        }
    </style>
</head>
<body>
    <div id="stars">
        <!-- Generating random stars -->
        <script>
            const numberOfStars = 100;
            const starsContainer = document.getElementById('stars');
            for (let i = 0; i < numberOfStars; i++) {
                const star = document.createElement('div');
                star.className = 'star';
                star.style.top = Math.random() * 100 + '%';
                star.style.left = Math.random() * 100 + '%';
                star.style.width = Math.random() * 3 + 'px';
                star.style.height = star.style.width;
                star.style.animation = `twinkle ${Math.random() * 3 + 1}s infinite`;
                starsContainer.appendChild(star);
            }
        </script>
    </div>
    <h1>Welcome to the Mysterious Night Sky</h1>
    <p>Look up and marvel at the twinkling stars!</p>
</body>
</html>
