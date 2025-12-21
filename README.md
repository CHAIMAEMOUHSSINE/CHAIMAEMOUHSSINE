<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Special GitHub Profile</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Poppins:wght@300;400;600&display=swap');
        
        :root {
            --pink: #ffb8e0;
            --lavender: #d8b4ff;
            --mint: #b4ffd8;
            --peach: #ffd8b4;
            --white: #fff9fd;
            --shadow: rgba(255, 184, 224, 0.3);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #fff9fd 0%, #ffe6f7 100%);
            color: #6d5c7a;
            min-height: 100vh;
            padding: 20px;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            position: relative;
        }
        
        .floating-hearts {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }
        
        .heart {
            position: absolute;
            background-color: var(--pink);
            display: inline-block;
            height: 20px;
            width: 20px;
            transform: rotate(-45deg);
            opacity: 0.7;
            animation: float 15s infinite linear;
        }
        
        .heart:before,
        .heart:after {
            content: "";
            background-color: var(--pink);
            border-radius: 50%;
            height: 20px;
            width: 20px;
            position: absolute;
        }
        
        .heart:before {
            top: -10px;
            left: 0;
        }
        
        .heart:after {
            left: 10px;
            top: 0;
        }
        
        @keyframes float {
            0% { transform: translateY(100vh) rotate(-45deg); opacity: 0; }
            10% { opacity: 0.7; }
            90% { opacity: 0.7; }
            100% { transform: translateY(-100px) rotate(-45deg); opacity: 0; }
        }
        
        header {
            text-align: center;
            padding: 40px 20px;
            position: relative;
        }
        
        h1 {
            font-family: 'Dancing Script', cursive;
            font-size: 4rem;
            color: #ff6bb5;
            text-shadow: 3px 3px 0 var(--lavender);
            margin-bottom: 20px;
            animation: bounce 2s infinite alternate;
        }
        
        @keyframes bounce {
            0% { transform: translateY(0); }
            100% { transform: translateY(-10px); }
        }
        
        .intro-text {
            font-size: 1.2rem;
            max-width: 600px;
            margin: 0 auto 30px;
            line-height: 1.6;
            background-color: rgba(255, 255, 255, 0.8);
            padding: 20px;
            border-radius: 20px;
            box-shadow: 0 10px 30px var(--shadow);
        }
        
        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            margin: 40px 0;
            padding: 30px;
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 25px;
            box-shadow: 0 10px 30px var(--shadow);
        }
        
        .tech-icon {
            width: 70px;
            height: 70px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--pink), var(--lavender));
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .tech-icon:hover {
            transform: translateY(-10px) scale(1.1);
            box-shadow: 0 15px 30px rgba(255, 107, 181, 0.4);
        }
        
        .tech-icon img {
            width: 40px;
            height: 40px;
            filter: brightness(0) invert(1);
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin: 30px 0;
            flex-wrap: wrap;
        }
        
        .social-btn {
            padding: 12px 25px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 10px;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .social-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        .linkedin { background: linear-gradient(135deg, #0077b5, #00a0dc); color: white; }
        .twitter { background: linear-gradient(135deg, #1da1f2, #1a91da); color: white; }
        .discord { background: linear-gradient(135deg, #7289da, #5a6fc2); color: white; }
        .twitch { background: linear-gradient(135deg, #9146ff, #772ce8); color: white; }
        .dev { background: linear-gradient(135deg, #0a0a0a, #333); color: white; }
        
        .stats-section {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin: 40px 0;
            flex-wrap: wrap;
        }
        
        .stat-card {
            background: white;
            border-radius: 20px;
            padding: 25px;
            width: 250px;
            box-shadow: 0 10px 30px var(--shadow);
            text-align: center;
            transition: all 0.3s ease;
            border: 3px solid transparent;
            background-clip: padding-box;
            position: relative;
            overflow: hidden;
        }
        
        .stat-card:hover {
            transform: translateY(-10px);
            border-image: linear-gradient(135deg, var(--pink), var(--lavender)) 1;
        }
        
        .stat-card h3 {
            color: #ff6bb5;
            margin-bottom: 15px;
            font-size: 1.5rem;
        }
        
        .stat-number {
            font-size: 2.5rem;
            font-weight: 700;
            color: #a86bc9;
            margin-bottom: 10px;
        }
        
        .games-section {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 30px;
            margin: 50px 0;
        }
        
        .game-card {
            width: 300px;
            height: 200px;
            border-radius: 20px;
            overflow: hidden;
            position: relative;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
            cursor: pointer;
            transition: all 0.4s ease;
        }
        
        .game-card:hover {
            transform: translateY(-15px) scale(1.05);
            box-shadow: 0 25px 50px rgba(255, 107, 181, 0.3);
        }
        
        .game-image {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        
        .game-card:hover .game-image {
            transform: scale(1.1);
        }
        
        .game-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(to top, rgba(216, 180, 255, 0.9), transparent);
            padding: 20px;
            color: white;
            transform: translateY(100%);
            transition: transform 0.3s ease;
        }
        
        .game-card:hover .game-overlay {
            transform: translateY(0);
        }
        
        footer {
            text-align: center;
            padding: 30px;
            margin-top: 50px;
            color: #a86bc9;
            font-size: 0.9rem;
            border-top: 2px dashed var(--lavender);
        }
        
        .special-button {
            display: block;
            margin: 30px auto;
            padding: 15px 40px;
            background: linear-gradient(135deg, var(--pink), var(--lavender));
            color: white;
            border: none;
            border-radius: 50px;
            font-size: 1.2rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 10px 20px rgba(255, 107, 181, 0.3);
        }
        
        .special-button:hover {
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 15px 30px rgba(255, 107, 181, 0.5);
            background: linear-gradient(135deg, var(--lavender), var(--pink));
        }
        
        .sparkle {
            position: absolute;
            width: 10px;
            height: 10px;
            background-color: white;
            border-radius: 50%;
            box-shadow: 0 0 10px white;
            animation: sparkle 1.5s infinite alternate;
        }
        
        @keyframes sparkle {
            0% { opacity: 0.3; transform: scale(0.5); }
            100% { opacity: 1; transform: scale(1); }
        }
        
        @media (max-width: 768px) {
            h1 { font-size: 2.5rem; }
            .tech-stack { gap: 15px; }
            .tech-icon { width: 60px; height: 60px; }
            .tech-icon img { width: 30px; height: 30px; }
            .stats-section { flex-direction: column; align-items: center; }
            .game-card { width: 100%; max-width: 300px; }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body>
    <div class="floating-hearts" id="hearts-container"></div>
    
    <div class="container">
        <header>
            <h1>Hey there! 👋 What's Up?</h1>
            <div class="intro-text">
                <p>Welcome to my magical corner of the internet! ✨ I'm a developer who loves creating beautiful, functional things with code. When I'm not coding, you can find me exploring new technologies, playing games, or enjoying a cup of tea. ☕</p>
            </div>
        </header>
        
        <section class="tech-stack">
            <div class="tech-icon">
                <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" alt="TypeScript">
            </div>
            <div class="tech-icon">
                <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nextjs/nextjs-original.svg" alt="NextJS">
            </div>
            <div class="tech-icon">
                <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-plain.svg" alt="Tailwind CSS">
            </div>
            <div class="tech-icon">
                <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/storybook/storybook-original.svg" alt="Storybook">
            </div>
            <div class="tech-icon">
                <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/graphql/graphql-plain.svg" alt="GraphQL">
            </div>
            <div class="tech-icon">
                <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/go/go-original.svg" alt="Go">
            </div>
            <div class="tech-icon">
                <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/rust/rust-plain.svg" alt="Rust">
            </div>
            <div class="tech-icon">
                <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nestjs/nestjs-plain.svg" alt="NestJS">
            </div>
            <div class="tech-icon">
                <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" alt="Python">
            </div>
            <div class="tech-icon">
                <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/amazonwebservices/amazonwebservices-original.svg" alt="AWS">
            </div>
        </section>
        
        <div class="social-links">
            <a href="#" class="social-btn linkedin">
                <i class="fab fa-linkedin"></i> LinkedIn
            </a>
            <a href="#" class="social-btn twitter">
                <i class="fab fa-twitter"></i> Twitter
            </a>
            <a href="#" class="social-btn discord">
                <i class="fab fa-discord"></i> Discord
            </a>
            <a href="#" class="social-btn twitch">
                <i class="fab fa-twitch"></i> Twitch
            </a>
            <a href="#" class="social-btn dev">
                <i class="fab fa-dev"></i> Dev.to
            </a>
        </div>
        
        <button class="special-button" id="magic-button">
            <i class="fas fa-magic"></i> Sprinkle Some Magic!
        </button>
        
        <div class="stats-section">
            <div class="stat-card">
                <h3>Coding Streak</h3>
                <div class="stat-number">127 days</div>
                <p>Consistent coding every single day! 🚀</p>
            </div>
            
            <div class="stat-card">
                <h3>Projects Built</h3>
                <div class="stat-number">42</div>
                <p>From small experiments to full apps 🎨</p>
            </div>
            
            <div class="stat-card">
                <h3>Cups of Tea</h3>
                <div class="stat-number">∞</div>
                <p>Fuel for all the coding sessions ☕</p>
            </div>
        </div>
        
        <section class="games-section">
            <div class="game-card">
                <img src="https://images.unsplash.com/photo-1550745165-9bc0b252726f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Gaming Setup" class="game-image">
                <div class="game-overlay">
                    <h3>Gaming Time! 🎮</h3>
                    <p>Check out my gaming setup and favorite games</p>
                </div>
            </div>
            
            <div class="game-card">
                <img src="https://images.unsplash.com/photo-1518709268805-4e9042af2176?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1468&q=80" alt="Creative Coding" class="game-image">
                <div class="game-overlay">
                    <h3>Creative Coding 🎨</h3>
                    <p>Exploring the intersection of art and technology</p>
                </div>
            </div>
            
            <div class="game-card">
                <img src="https://images.unsplash.com/photo-1542751371-adc38448a05e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Game Development" class="game-image">
                <div class="game-overlay">
                    <h3>Game Dev 🕹️</h3>
                    <p>My journey in creating interactive experiences</p>
                </div>
            </div>
        </section>
        
        <footer>
            <p>Made with <i class="fas fa-heart" style="color: #ff6bb5;"></i> and lots of sparkles ✨</p>
            <p>© 2023 My Magical GitHub Profile | Keep shining! 🌟</p>
        </footer>
    </div>

    <script>
        // Create floating hearts
        const heartsContainer = document.getElementById('hearts-container');
        for (let i = 0; i < 25; i++) {
            const heart = document.createElement('div');
            heart.classList.add('heart');
            heart.style.left = `${Math.random() * 100}%`;
            heart.style.animationDelay = `${Math.random() * 15}s`;
            heart.style.animationDuration = `${15 + Math.random() * 10}s`;
            heart.style.width = `${10 + Math.random() * 15}px`;
            heart.style.height = heart.style.width;
            heartsContainer.appendChild(heart);
        }
        
        // Create sparkles
        for (let i = 0; i < 15; i++) {
            const sparkle = document.createElement('div');
            sparkle.classList.add('sparkle');
            sparkle.style.left = `${Math.random() * 100}%`;
            sparkle.style.top = `${Math.random() * 100}%`;
            sparkle.style.animationDelay = `${Math.random() * 2}s`;
            document.body.appendChild(sparkle);
        }
        
        // Magic button interaction
        const magicButton = document.getElementById('magic-button');
        magicButton.addEventListener('click', function() {
            // Create burst of hearts
            for (let i = 0; i < 30; i++) {
                const burstHeart = document.createElement('div');
                burstHeart.classList.add('heart');
                burstHeart.style.left = `${50 + (Math.random() * 20 - 10)}%`;
                burstHeart.style.top = `${80}%`;
                burstHeart.style.animation = `float ${3 + Math.random() * 2}s linear forwards`;
                burstHeart.style.width = `${15 + Math.random() * 20}px`;
                burstHeart.style.height = burstHeart.style.width;
                burstHeart.style.backgroundColor = getRandomColor();
                document.body.appendChild(burstHeart);
                
                // Remove after animation
                setTimeout(() => {
                    burstHeart.remove();
                }, 5000);
            }
            
            // Change button text temporarily
            const originalText = magicButton.innerHTML;
            magicButton.innerHTML = '<i class="fas fa-sparkles"></i> Magical!';
            magicButton.style.background = 'linear-gradient(135deg, #ffd8b4, #b4ffd8)';
            
            setTimeout(() => {
                magicButton.innerHTML = originalText;
                magicButton.style.background = 'linear-gradient(135deg, #ffb8e0, #d8b4ff)';
            }, 2000);
        });
        
        // Add hover effect to tech icons
        const techIcons = document.querySelectorAll('.tech-icon');
        techIcons.forEach(icon => {
            icon.addEventListener('mouseenter', function() {
                this.style.background = `linear-gradient(135deg, ${getRandomColor()}, ${getRandomColor()})`;
            });
            
            icon.addEventListener('mouseleave', function() {
                this.style.background = 'linear-gradient(135deg, var(--pink), var(--lavender))';
            });
        });
        
        // Game card click effect
        const gameCards = document.querySelectorAll('.game-card');
        gameCards.forEach(card => {
            card.addEventListener('click', function() {
                this.style.transform = 'scale(0.95)';
                setTimeout(() => {
                    this.style.transform = '';
                }, 200);
                
                // Show a message
                const messages = [
                    "Yay! Let's play! 🎮",
                    "Game on! 🕹️",
                    "This is gonna be fun! ✨",
                    "Ready player one! 👾"
                ];
                alert(messages[Math.floor(Math.random() * messages.length)]);
            });
        });
        
        // Helper function for random pastel colors
        function getRandomColor() {
            const colors = ['#ffb8e0', '#d8b4ff', '#b4ffd8', '#ffd8b4', '#b4e0ff', '#ffb4b4'];
            return colors[Math.floor(Math.random() * colors.length)];
        }
        
        // Animated numbers in stat cards
        const statNumbers = document.querySelectorAll('.stat-number');
        statNumbers.forEach(stat => {
            if (stat.textContent === '127' || stat.textContent === '42') {
                const target = parseInt(stat.textContent);
                let current = 0;
                const increment = target / 50;
                const timer = setInterval(() => {
                    current += increment;
                    if (current >= target) {
                        current = target;
                        clearInterval(timer);
                    }
                    stat.textContent = Math.floor(current) + (stat.textContent.includes('days') ? ' days' : '');
                }, 30);
            }
        });
    </script>
</body>
</html>
