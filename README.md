# Yeu-Minh-Chau
<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <title>Gửi Minh Châu</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Comic Sans MS', cursive;
      background: linear-gradient(to bottom right, #ffe6e6, #ffd1dc);
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      overflow: hidden;
      position: relative;
    }

    .message {
      background: white;
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.2);
      text-align: center;
      max-width: 500px;
    }

    .message h1 {
      color: #e91e63;
      margin-bottom: 10px;
    }

    .message p {
      color: #333;
      font-size: 18px;
    }

    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      transform: rotate(45deg);
      animation: float 6s infinite;
    }

    .heart::before,
    .heart::after {
      content: '';
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      border-radius: 50%;
    }

    .heart::before {
      top: -10px;
      left: 0;
    }

    .heart::after {
      left: -10px;
      top: 0;
    }

    @keyframes float {
      0% {
        bottom: -10px;
        left: calc(50% + (100px * (random() - 0.5)));
        opacity: 0;
      }
      50% {
        opacity: 1;
      }
      100% {
        bottom: 100%;
        left: calc(50% + (100px * (random() - 0.5)));
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <div class="message">
    <h1>Gửi Minh Châu</h1>
    <p>
      Không có từ nào đủ để diễn tả tình cảm của tớ dành cho cậu.<br>
      Mỗi ngày trôi qua, tớ lại càng yêu cậu nhiều hơn.<br>
      Cảm ơn cậu vì nụ cười, ánh mắt và tất cả những điều nhỏ bé<br>
      làm tim tớ rung động. Yêu cậu nhiều lắm!
    </p>
  </div>

  <!-- Trái tim bay -->
  <script>
    function random() {
      return Math.random();
    }

    function createHeart() {
      const heart = document.createElement('div');
      heart.classList.add('heart');
      heart.style.left = `${Math.random() * 100}%`;
      heart.style.animationDuration = `${4 + Math.random() * 3}s`;
      document.body.appendChild(heart);

      setTimeout(() => {
        heart.remove();
      }, 7000);
    }

    setInterval(createHeart, 500);
  </script>
</body>
</html>
