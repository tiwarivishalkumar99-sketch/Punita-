<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>A Special Message For You ✨</title>
    <style>
        body {
            background: linear-gradient(135deg, #fbc2eb, #a6c1ee);
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            font-family: 'Arial', sans-serif;
            overflow: hidden;
            position: relative;
        }
        .card {
            text-align: center;
            background: rgba(255, 255, 255, 0.9);
            padding: 40px 30px;
            border-radius: 25px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.15);
            z-index: 10;
            max-width: 85%;
            border: 2px solid #fff;
            animation: popUp 1s ease-in-out;
        }
        h1 {
            color: #4a00e0;
            font-size: 2.8rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
        }
        .message {
            color: #ff2a74;
            font-size: 1.8rem;
            font-weight: bold;
            margin-top: 15px;
            line-height: 1.4;
            animation: glow 1.5s ease-in-out infinite alternate;
        }
        /* Stars & Flowers Animation */
        .element {
            position: absolute;
            bottom: -50px;
            font-size: 24px;
            animation: floatUp 6s linear infinite;
            opacity: 0.8;
        }
        @keyframes popUp {
            0% { transform: scale(0.5); opacity: 0; }
            100% { transform: scale(1); opacity: 1; }
        }
        @keyframes glow {
            from { text-shadow: 0 0 10px #fff, 0 0 20px #ff2a74; }
            to { text-shadow: 0 0 20px #fff, 0 0 30px #ff758c; }
        }
        @keyframes floatUp {
            0% { transform: translateY(0) rotate(0deg); opacity: 1; }
            100% { transform: translateY(-110vh) rotate(360deg); opacity: 0; }
        }
    </style>
</head>
<body>

    <div class="card">
        <h1>Hey Punita... ✨</h1>
        <div class="message">Kl apki wasp h! 🌸🏡</div>
    </div>

    <script>
        // Mix of flowers and stars
        const items = ['🌸', '✨', '⭐', '💮', '🌼'];
        
        function createFloatingElements() {
            const element = document.createElement('div');
            element.classList.add('element');
            element.innerHTML = items[Math.floor(Math.random() * items.length)];
            element.style.left = Math.random() * 100 + 'vw';
            element.style.animationDuration = Math.random() * 3 + 4 + 's';
            element.style.fontSize = Math.random() * 15 + 20 + 'px';
            document.body.appendChild(element);
            
            setTimeout(() => { element.remove(); }, 7000);
        }
        setInterval(createFloatingElements, 400);
    </script>
</body>
</html>
