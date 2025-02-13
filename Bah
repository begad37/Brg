<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>لعبة التخمين المرعبة</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            text-align: center;
            background: linear-gradient(to right, #141e30, #243b55);
            color: white;
            transition: all 1s ease;
        }
        h1 {
            font-size: 2.5rem;
            margin-top: 50px;
        }
        input, button {
            font-size: 1.2rem;
            padding: 10px;
            margin: 10px;
            border-radius: 5px;
            border: none;
        }
        input {
            width: 200px;
            text-align: center;
        }
        button {
            background-color: #ff4757;
            color: white;
            cursor: pointer;
            transition: 0.3s;
        }
        button:hover {
            background-color: #ff6b81;
        }
        #message {
            font-size: 1.5rem;
            margin-top: 20px;
        }
        .hidden {
            display: none;
        }
        .gallery img {
            width: 150px;
            height: 150px;
            margin: 10px;
            border-radius: 10px;
        }
    </style>
</head>
<body>

    <h1>🎮 لعبة التخمين</h1>
    <p>اختر رقمًا بين 1 و 10، وإذا لم تخمن الرقم الصحيح، سيتم مسح جميع صورك! 😈</p>
    
    <input type="number" id="guess" placeholder="اكتب رقمك هنا">
    <button onclick="checkGuess()">تحقق</button>

    <p id="message"></p>

    <div class="gallery">
        <img src="https://via.placeholder.com/150" alt="صورة 1">
        <img src="https://via.placeholder.com/150" alt="صورة 2">
        <img src="https://via.placeholder.com/150" alt="صورة 3">
        <img src="https://via.placeholder.com/150" alt="صورة 4">
    </div>

    <script>
        let randomNumber = Math.floor(Math.random() * 10) + 1;

        function checkGuess() {
            let userGuess = document.getElementById("guess").value;
            let message = document.getElementById("message");
            let images = document.querySelectorAll(".gallery img");

            if (parseInt(userGuess) === randomNumber) {
                message.innerHTML = "🎉 مبروك! لقد فزت!";
            } else {
                message.innerHTML = "❌ خطأ! يتم الآن حذف جميع صورك... 😱";

                // بعد ثانيتين، تختفي الصور وتظهر رسالة مرعبة
                setTimeout(() => {
                    images.forEach(img => img.style.display = "none");
                    document.body.style.background = "black";
                    document.body.innerHTML = "<h1 style='color:red; margin-top:20%; font-size:3rem;'>❌ تم حذف جميع صورك</h1>";
                }, 2000);
            }
        }
    </script>

</body>
</html>
