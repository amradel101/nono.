
<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For NONO ❤️</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            background-color: #ffeef2;
            font-family: 'Arial', sans-serif;
            overflow: hidden;
        }
        .container {
            text-align: center;
            background: white;
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
            width: 380px;
        }
        #sticker {
            width: 100%;
            max-width: 250px;
            height: 200px;
            object-fit: cover;
            border-radius: 15px;
            margin-bottom: 15px;
        }
        h1 { color: #ff4d6d; font-size: 1.6rem; }
        #message { height: 40px; color: #ff758f; font-weight: bold; }
        .buttons {
            display: flex;
            justify-content: center;
            gap: 40px;
            margin-top: 20px;
            height: 60px;
            position: relative;
        }
        button {
            padding: 12px 30px;
            font-size: 1.1rem;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            font-weight: bold;
        }
        #yesBtn { background-color: #ff4d6d; color: white; }
        #noBtn { background-color: #fb6f92; color: white; position: relative; }
    </style>
</head>
<body>

    <div class="container">
        <img id="sticker" src="https://media.giphy.com/media/t8xgPfC5oNIRMrNooe/giphy.gif" alt="Panda">
        <h1 id="question">Will you be my Valentine, NONO? ❤️</h1>
        <div id="message"></div>
        <div class="buttons">
            <button id="yesBtn">Yes</button>
            <button id="noBtn">No</button>
        </div>
    </div>

    <script>
        const noBtn = document.getElementById('noBtn');
        const yesBtn = document.getElementById('yesBtn');
        const message = document.getElementById('message');
        const sticker = document.getElementById('sticker');
        const question = document.getElementById('question');

        // الروابط الأصلية
        const finalGifUrl = "https://media.giphy.com/media/1JmGiBtqTuehfYxuy9/giphy.gif";

        // لما تقف على Yes
        yesBtn.onmouseover = () => { message.innerText = "press here please 🥺✨"; };
        yesBtn.onmouseout = () => { message.innerText = ""; };

        // لما تقف على No
        noBtn.addEventListener('mouseover', () => {
            message.innerText = "don't press here its dangerous! 😂";
            noBtn.style.position = 'fixed';
            const x = Math.random() * (window.innerWidth - noBtn.offsetWidth);
            const y = Math.random() * (window.innerHeight - noBtn.offsetHeight);
            noBtn.style.left = x + 'px';
            noBtn.style.top = y + 'px';
        });

        // حركة الصايع: إضافة علامة استفهام ورقم عشوائي للرابط عشان يجبره يتغير
        yesBtn.onclick = function() {
            question.innerText = "Yay! I Love You! ❤️";
            message.innerText = "i love you NONO! 🥰";
            
            // دي الحركة اللي هتحل كل المشاكل
            sticker.src = finalGifUrl + "?t=" + new Date().getTime();
            
            noBtn.style.display = 'none';
        };
    </script>
</body>
</html>
