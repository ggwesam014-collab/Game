<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>لعبة 2D بسيطة - جمع العملات</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        }
        
        .game-container {
            text-align: center;
            padding: 20px;
            background: rgba(255, 255, 255, 0.95);
            border-radius: 10px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
        }
        
        h2 {
            color: #333;
            margin-bottom: 15px;
        }
        
        canvas {
            border: 2px solid #333;
            border-radius: 5px;
            background: #fff;
            cursor: none;
        }
        
        .score-board {
            margin-top: 15px;
            font-size: 24px;
            color: #333;
        }
        
        .controls {
            margin-top: 15px;
            color: #666;
            font-size: 14px;
        }
        
        button {
            padding: 10px 20px;
            margin-top: 10px;
            background: #667eea;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            cursor: pointer;
            transition: background 0.3s;
        }
        
        button:hover {
            background: #5a67d8;
        }
    </style>
</head>
<body>
    <div class="game-container">
        <h2>🎮 لعبة جمع العملات 🎮</h2>
        
        <canvas id="gameCanvas" width="400" height="400"></canvas>
        
        <div class="score-board">
            النقاط: <span id="score">0</span>
        </div>
        
        <div class="controls">
            حرك الفأرة لتحريك الشخصية 🟡 ← جمع العملات الحمراء 🔴
        </div>
        
        <button onclick="resetGame()">لعبة جديدة</button>
    </div>

    <script>
        const canvas = document.getElementById('gameCanvas');
        const ctx = canvas.getContext('2d');
        const scoreElement = document.getElementById('score');

        // اللاعب
        let player = {
            x: 200,
            y: 200,
            radius: 15,
            color: '#FFD700' // ذهبي
        };

        // العملات
        let coins = [];
        let score = 0;

        // إنشاء عملة جديدة
        function createCoin() {
            return {
                x: Math.random() * (canvas.width - 30) + 15,
                y: Math.random() * (canvas.height - 30) + 15,
                radius: 10,
                color: '#FF4444', // أحمر
                collected: false
            };
        }

        // إنشاء 5 عملات في البداية
        for (let i = 0; i < 5; i++) {
            coins.push(createCoin());
        }

        // رسم اللاعب
        function drawPlayer() {
            ctx.beginPath();
            ctx.arc(player.x, player.y, player.radius, 0, Math.PI * 2);
            ctx.fillStyle = player.color;
            ctx.fill();
            ctx.shadowColor = 'rgba(0, 0, 0, 0.3)';
            ctx.shadowBlur = 10;
            ctx.shadowOffsetY = 3;
            ctx.closePath();
            
            // رسم عيون صغيرة
            ctx.shadowBlur = 0;
            ctx.beginPath();
            ctx.arc(player.x - 5, player.y - 5, 3, 0, Math.PI * 2);
            ctx.fillStyle = '#000';
            ctx.fill();
            
            ctx.beginPath();
            ctx.arc(player.x + 5, player.y - 5, 3, 0, Math.PI * 2);
            ctx.fill();
        }

        // رسم العملات
        function drawCoins() {
            coins.forEach(coin => {
                if (!coin.collected) {
                    ctx.beginPath();
                    ctx.arc(coin.x, coin.y, coin.radius, 0, Math.PI * 2);
                    ctx.fillStyle = coin.color;
                    ctx.fill();
                    
                    // رسم بريق على العملة
                    ctx.shadowBlur = 0;
                    ctx.beginPath();
                    ctx.arc(coin.x - 3, coin.y - 3, 2, 0, Math.PI * 2);
                    ctx.fillStyle = '#FFAAAA';
                    ctx.fill();
                }
            });
        }

        // التحقق من جمع العملات
        function checkCollisions() {
            coins.forEach(coin => {
                if (!coin.collected) {
                    // حساب المسافة بين اللاعب والعملة
                    const dx = player.x - coin.x;
                    const dy = player.y - coin.y;
                    const distance = Math.sqrt(dx * dx + dy * dy);
                    
                    // إذا لامس اللاعب العملة
                    if (distance < player.radius + coin.radius) {
                        coin.collected = true;
                        score++;
                        scoreElement.textContent = score;
                        
                        // إضافة عملة جديدة
                        coins.push(createCoin());
                    }
                }
            });
        }

        // تحديث اللعبة
        function update() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // إعادة تعيين الظلال
            ctx.shadowBlur = 0;
            ctx.shadowColor = 'transparent';
            
            // رسم اللاعب والعملات
            drawPlayer();
            drawCoins();
            
            // التحقق من التصادم
            checkCollisions();
            
            // تحديث الحركة
            requestAnimationFrame(update);
        }

        // تتبع حركة الفأرة
        canvas.addEventListener('mousemove', (event) => {
            const rect = canvas.getBoundingClientRect();
            const scaleX = canvas.width / rect.width;
            const scaleY = canvas.height / rect.height;
            
            // تحديث موقع اللاعب مع منعه من الخروج من الشاشة
            let mouseX = (event.clientX - rect.left) * scaleX;
            let mouseY = (event.clientY - rect.top) * scaleY;
            
            // التأكد من بقاء اللاعب داخل اللوحة
            player.x = Math.min(Math.max(mouseX, player.radius), canvas.width - player.radius);
            player.y = Math.min(Math.max(mouseY, player.radius), canvas.height - player.radius);
        });

        // إعادة تعيين اللعبة
        function resetGame() {
            score = 0;
            scoreElement.textContent = score;
            coins = [];
            for (let i = 0; i < 5; i++) {
                coins.push(createCoin());
            }
            player.x = 200;
            player.y = 200;
        }

        // بدء اللعبة
        update();

        // دالة إعادة التعيين متاحة في النطاق العالمي
        window.resetGame = resetGame;
    </script>
</body>
</html>
