![Header](https://your-image-url.com/banner.png)

# 👋 Hey there, I'm **Safwan**!  

🎓 I'm a 19-year-old B.Tech CSE student specializing in **Full Stack Web Development**!  
💻 Passionate about creating interactive, engaging platforms and exploring the world of **3D web experiences**.  

---

## 🌟 About Me  
- 🔹 I’m currently diving deep into building web applications with **modern frameworks** like **React**, **Next.js**, and **Node.js**.  
- 🔹 Exploring advanced technologies like **Three.js** for 3D experiences and **D3.js** for data visualization.  
- 🔹 Open to collaborating on **innovative projects** and **open-source contributions**.  
- ⚡ Fun Fact: I can debug for hours without realizing it's 4 AM! 🕓  

---

## 🛠️ My Tech Toolbox  
Here’s a breakdown of the tech I use and my proficiency:  

![HTML](https://img.shields.io/badge/-HTML5-E34F26?logo=html5&logoColor=white&style=flat)
![CSS](https://img.shields.io/badge/-CSS3-1572B6?logo=css3&logoColor=white&style=flat)
![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?logo=javascript&logoColor=black&style=flat)
![React](https://img.shields.io/badge/-React-61DAFB?logo=react&logoColor=black&style=flat)
![Next.js](https://img.shields.io/badge/-Next.js-000000?logo=next.js&logoColor=white&style=flat)
![Node.js](https://img.shields.io/badge/-Node.js-339933?logo=node.js&logoColor=white&style=flat)
![MongoDB](https://img.shields.io/badge/-MongoDB-47A248?logo=mongodb&logoColor=white&style=flat)
![Express.js](https://img.shields.io/badge/-Express.js-000000?logo=express&logoColor=white&style=flat)
![Python](https://img.shields.io/badge/-Python-3776AB?logo=python&logoColor=white&style=flat)

### Tech Stack Proficiency Graph  
```mermaid
pie
title My Tech Stack Proficiency
"HTML": 90
"CSS": 85
"JavaScript": 85
"React": 75
"Next.js": 70
"Node.js": 70
"MongoDB": 65
"Express.js": 60
"Python": 80
```

---

## 📈 GitHub Stats  
![GitHub Stats](https://github-readme-stats.vercel.app/api?username=safwan125&show_icons=true&theme=radical)  
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=safwan125&layout=compact&theme=radical)  
![GitHub Streak](https://streak-stats.demolab.com?user=safwan125&theme=radical)  

---

## 🐍 Play Snake Game on This Page!  
<div align="center">
  <canvas id="snakeCanvas" width="500" height="500" style="border:1px solid black;"></canvas>
  <script>
    const canvas = document.getElementById('snakeCanvas');
    const ctx = canvas.getContext('2d');

    const box = 20;
    let snake = [{ x: 9 * box, y: 10 * box }];
    let direction = "RIGHT";
    let food = {
      x: Math.floor(Math.random() * 25) * box,
      y: Math.floor(Math.random() * 25) * box,
    };

    document.addEventListener('keydown', changeDirection);

    function changeDirection(event) {
      if (event.keyCode === 37 && direction !== "RIGHT") direction = "LEFT";
      else if (event.keyCode === 38 && direction !== "DOWN") direction = "UP";
      else if (event.keyCode === 39 && direction !== "LEFT") direction = "RIGHT";
      else if (event.keyCode === 40 && direction !== "UP") direction = "DOWN";
    }

    function collision(head, array) {
      return array.some(segment => head.x === segment.x && head.y === segment.y);
    }

    function drawGame() {
      ctx.fillStyle = "white";
      ctx.fillRect(0, 0, canvas.width, canvas.height);

      for (let i = 0; i < snake.length; i++) {
        ctx.fillStyle = i === 0 ? "green" : "lightgreen";
        ctx.fillRect(snake[i].x, snake[i].y, box, box);
      }

      ctx.fillStyle = "red";
      ctx.fillRect(food.x, food.y, box, box);

      let headX = snake[0].x;
      let headY = snake[0].y;

      if (direction === "LEFT") headX -= box;
      if (direction === "UP") headY -= box;
      if (direction === "RIGHT") headX += box;
      if (direction === "DOWN") headY += box;

      if (headX === food.x && headY === food.y) {
        food = {
          x: Math.floor(Math.random() * 25) * box,
          y: Math.floor(Math.random() * 25) * box,
        };
      } else {
        snake.pop();
      }

      const newHead = { x: headX, y: headY };

      if (
        headX < 0 ||
        headX >= canvas.width ||
        headY < 0 ||
        headY >= canvas.height ||
        collision(newHead, snake)
      ) {
        clearInterval(game);
        alert("Game Over");
      }

      snake.unshift(newHead);
    }

    const game = setInterval(drawGame, 100);
  </script>
</div>

---

## 🌈 Fun Facts  
- 🎮 Gaming is my go-to for unwinding.  
- 📖 I enjoy reading about cutting-edge tech and innovations.  
- ✈️ Love traveling and exploring new cultures.  

---

## 🤝 Let’s Connect!  
I’d love to collaborate or hear about your exciting ideas.  
- 📩 [Email Me](mailto:safwan.sm125@gmail.com)  
- 💼 [Connect on LinkedIn](https://linkedin.com/in/safwan125)  

---

🌟 From [Safwan](https://github.com/safwan125)
