<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pedro Henrique - Banner</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            width: 100%;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a0000 25%, #2d0000 50%, #1a0000 75%, #000000 100%);
            background-size: 400% 400%;
            animation: gradientShift 8s ease infinite;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            overflow: hidden;
        }

        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .container {
            width: 100%;
            max-width: 1200px;
            height: 600px;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
            border-radius: 20px;
        }

        .stars {
            position: absolute;
            width: 100%;
            height: 100%;
            overflow: hidden;
        }

        .star {
            position: absolute;
            border-radius: 50%;
            animation: twinkle 3s infinite;
        }

        .star.type1 {
            width: 2px;
            height: 2px;
            background: #ff0000;
        }

        .star.type2 {
            width: 3px;
            height: 3px;
            background: #cc0000;
            opacity: 0.7;
        }

        .star.type3 {
            width: 1px;
            height: 1px;
            background: #ffffff;
            opacity: 0.6;
        }

        @keyframes twinkle {
            0%, 100% { opacity: 0.3; }
            50% { opacity: 1; }
        }

        .content {
            text-align: center;
            z-index: 10;
            animation: slideUp 1s ease-out;
        }

        @keyframes slideUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .title {
            font-size: 4.5rem;
            font-weight: 900;
            margin-bottom: 20px;
            background: linear-gradient(45deg, #ff0000, #ff3333, #ff0000);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            background-size: 200% 200%;
            animation: gradientText 3s ease infinite;
            letter-spacing: 3px;
            text-shadow: 0 0 30px rgba(255, 0, 0, 0.5);
        }

        @keyframes gradientText {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .subtitle {
            font-size: 1.8rem;
            color: #ff0000;
            margin-bottom: 30px;
            font-weight: 300;
            letter-spacing: 2px;
            animation: fadeInDelay 1.5s ease-out;
            text-shadow: 0 0 20px rgba(255, 0, 0, 0.5);
        }

        @keyframes fadeInDelay {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .icons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
            animation: fadeInDelay2 2s ease-out;
        }

        @keyframes fadeInDelay2 {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .icon {
            width: 50px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: rgba(255, 0, 0, 0.1);
            border: 2px solid #ff0000;
            border-radius: 12px;
            font-size: 1.8rem;
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
            cursor: pointer;
            box-shadow: 0 0 15px rgba(255, 0, 0, 0.3);
        }

        .icon:hover {
            background: rgba(255, 0, 0, 0.3);
            border-color: #ff3333;
            transform: translateY(-5px) rotate(5deg);
            box-shadow: 0 10px 30px rgba(255, 0, 0, 0.6), 0 0 20px rgba(255, 0, 0, 0.5);
        }

        .floating-shapes {
            position: absolute;
            width: 100%;
            height: 100%;
            z-index: 1;
        }

        .shape {
            position: absolute;
            opacity: 0.08;
            border-radius: 50%;
        }

        .shape-1 {
            width: 300px;
            height: 300px;
            background: #ff0000;
            top: -100px;
            left: -100px;
            animation: float 20s infinite ease-in-out;
            filter: blur(50px);
        }

        .shape-2 {
            width: 250px;
            height: 250px;
            background: #ff0000;
            top: 50%;
            right: -100px;
            animation: float 25s infinite ease-in-out reverse;
            filter: blur(50px);
        }

        .shape-3 {
            width: 200px;
            height: 200px;
            background: #cc0000;
            bottom: -50px;
            left: 20%;
            animation: float 30s infinite ease-in-out;
            filter: blur(50px);
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(30px); }
        }

        .line {
            position: absolute;
            height: 3px;
            background: linear-gradient(90deg, transparent, #ff0000, #cc0000, transparent);
            width: 300px;
            z-index: 2;
        }

        .line-1 {
            top: 100px;
            left: -300px;
            animation: slideLine 3s ease-in-out infinite;
        }

        .line-2 {
            bottom: 100px;
            right: -300px;
            animation: slideLine 3s ease-in-out infinite 1.5s;
        }

        @keyframes slideLine {
            0% { transform: translateX(0); opacity: 0; }
            50% { opacity: 1; }
            100% { transform: translateX(600px); opacity: 0; }
        }

        .badge {
            display: inline-block;
            padding: 10px 20px;
            background: rgba(255, 0, 0, 0.15);
            border: 2px solid #ff0000;
            border-radius: 50px;
            color: #ff0000;
            font-size: 0.9rem;
            margin-top: 15px;
            backdrop-filter: blur(10px);
            font-weight: 600;
            box-shadow: 0 0 20px rgba(255, 0, 0, 0.3);
            transition: all 0.3s ease;
        }

        .badge:hover {
            background: rgba(255, 0, 0, 0.3);
            border-color: #ff3333;
            box-shadow: 0 0 30px rgba(255, 0, 0, 0.6);
        }

        .accent-line {
            width: 100px;
            height: 4px;
            background: linear-gradient(90deg, #ff0000, #cc0000);
            margin: 15px auto;
            border-radius: 2px;
        }
    </style>
</head>
<body>
    <div class="stars" id="starfield"></div>
    
    <div class="container">
        <div class="floating-shapes">
            <div class="shape shape-1"></div>
            <div class="shape shape-2"></div>
            <div class="shape shape-3"></div>
            <div class="line line-1"></div>
            <div class="line line-2"></div>
        </div>

        <div class="content">
            <h1 class="title">🚀 PEDRO HENRIQUE 🎮</h1>
            <div class="accent-line"></div>
            <p class="subtitle">Full Stack Developer | Game Enthusiast</p>
            
            <div class="icons">
                <div class="icon">💻</div>
                <div class="icon">🎮</div>
                <div class="icon">⚡</div>
                <div class="icon">🔧</div>
                <div class="icon">🌟</div>
            </div>

            <div style="margin-top: 30px;">
                <span class="badge">✨ Transforming Ideas Into Code</span>
            </div>
        </div>
    </div>

    <script>
        // Criar estrelas animadas com cores vermelho e preto
        const starfield = document.getElementById('starfield');
        const types = ['type1', 'type2', 'type3'];
        
        for (let i = 0; i < 70; i++) {
            const star = document.createElement('div');
            star.className = 'star ' + types[Math.floor(Math.random() * types.length)];
            star.style.left = Math.random() * 100 + '%';
            star.style.top = Math.random() * 100 + '%';
            star.style.animationDelay = Math.random() * 3 + 's';
            starfield.appendChild(star);
        }
    </script>
</body>
</html>
