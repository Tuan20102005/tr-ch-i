<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <title>Bạn có đặc biệt không?</title>
  <style>
    body {
      background-color: #fff0f6;
      font-family: 'Segoe UI', sans-serif;
      text-align: center;
      padding-top: 100px;
    }

    h1 {
      color: #d63384;
    }

    #btn {
      font-size: 24px;
      padding: 20px 40px;
      background-color: #ff69b4;
      color: white;
      border: none;
      border-radius: 20px;
      cursor: pointer;
      box-shadow: 0 5px 15px rgba(0,0,0,0.2);
    }

    #btn:hover {
      background-color: #ff85c1;
    }

    #message {
      margin-top: 40px;
      font-size: 20px;
      color: #333;
      line-height: 1.6;
    }
  </style>
</head>
<body>

  <h1>💖 Trò chơi dành riêng cho bạn 💖</h1>
  <button id="btn">Bấm vào để biết mình có đặc biệt không!</button>
  <div id="message"></div>

  <script>
    const messages = [
      "Hệ thống đang kiểm tra độ đáng yêu...",
      "Phát hiện mức độ dễ thương: 100% 🌸",
      "Đang xác nhận sự thông minh... 101% rồi nè 🤓",
      "Ồ, hình như bạn là người đặc biệt nhất hôm nay đó! 💖",
      "Tặng bạn sticker: 🌟 Cô gái vàng trong làng cute 🌟",
      "Chúc bạn ngủ ngon nha 💤 Mơ đẹp và luôn rạng rỡ như vậy nhé 🧸🌙"
    ];

    let index = 0;
    const btn = document.getElementById('btn');
    const msg = document.getElementById('message');

    btn.addEventListener('click', () => {
      if (index < messages.length) {
        msg.innerHTML += `<p>${messages[index]}</p>`;
        index++;
      } else {
        btn.disabled = true;
        btn.innerText = "💤 Đã xong rồi nè ~";
      }
    });
  </script>

</body>
</html>
