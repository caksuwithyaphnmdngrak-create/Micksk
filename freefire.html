<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Mini Free Fire Simulator</title>
  <style>
    body { margin: 0; background: #111; color: white; font-family: Arial; text-align: center; }
    canvas { background: #222; display: block; margin: 20px auto; border: 3px solid #fff; }
  </style>
</head>
<body>
  <h1>🎮 Mini Free Fire (Demo)</h1>
  <p>ใช้ปุ่ม ⬅️ ➡️ เพื่อเคลื่อนที่ | Spacebar ยิง</p>
  <canvas id="gameCanvas" width="600" height="400"></canvas>
  <p>คะแนน: <span id="score">0</span></p>

  <script>
    const canvas = document.getElementById("gameCanvas");
    const ctx = canvas.getContext("2d");
    let player = { x: 280, y: 350, w: 40, h: 40, color: "lime" };
    let bullets = [];
    let enemies = [];
    let score = 0;

    // สร้างศัตรูใหม่
    function spawnEnemy() {
      let x = Math.random() * (canvas.width - 30);
      enemies.push({ x: x, y: 0, w: 30, h: 30, color: "red" });
    }

    // คีย์บอร์ดควบคุม
    let keys = {};
    document.addEventListener("keydown", e => keys[e.code] = true);
    document.addEventListener("keyup", e => keys[e.code] = false);

    function update() {
      // เคลื่อนที่
      if (keys["ArrowLeft"] && player.x > 0) player.x -= 5;
      if (keys["ArrowRight"] && player.x < canvas.width - player.w) player.x += 5;

      // ยิง
      if (keys["Space"]) {
        bullets.push({ x: player.x + player.w/2 - 5, y: player.y, w: 5, h: 10, color: "yellow" });
        keys["Space"] = false; // ยิงทีละนัด
      }

      // อัปเดตลูกกระสุน
      bullets.forEach(b => b.y -= 7);
      bullets = bullets.filter(b => b.y > 0);

      // อัปเดตศัตรู
      enemies.forEach(en => en.y += 2);

      // ตรวจจับการชน
      enemies.forEach((en, i) => {
        bullets.forEach((b, j) => {
          if (b.x < en.x + en.w && b.x + b.w > en.x && b.y < en.y + en.h && b.h + b.y > en.y) {
            enemies.splice(i, 1);
            bullets.splice(j, 1);
            score++;
            document.getElementById("score").innerText = score;
          }
        });
      });

      // ลบศัตรูที่หลุดขอบ
      enemies = enemies.filter(en => en.y < canvas.height);
    }

    function draw() {
      ctx.clearRect(0, 0, canvas.width, canvas.height);
      // player
      ctx.fillStyle = player.color;
      ctx.fillRect(player.x, player.y, player.w, player.h);

      // bullets
      bullets.forEach(b => {
        ctx.fillStyle = b.color;
        ctx.fillRect(b.x, b.y, b.w, b.h);
      });

      // enemies
      enemies.forEach(en => {
        ctx.fillStyle = en.color;
        ctx.fillRect(en.x, en.y, en.w, en.h);
      });
    }

    function gameLoop() {
      update();
      draw();
      requestAnimationFrame(gameLoop);
    }

    setInterval(spawnEnemy, 1000); // ศัตรูโผล่ทุก 1 วิ
    gameLoop();
  </script>
</body>
</html>