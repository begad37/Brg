<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>لعبة التخمين الخطيرة</title>
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
    </style>
</head>
<body>

    <h1>🎮 لعبة التخمين</h1>
    <p>اختر رقمًا بين 1 و 10، وإذا لم تخمن الرقم الصحيح، سيتم إغلاق المتصفح! 😈</p>
    
    <input type="number" id="guess" placeholder="اكتب رقمك هنا">
    <button onclick="checkGuess()">تحقق</button>

    <p id="message"></p>

    <script>
        let randomNumber = Math.floor(Math.random() * 10) + 1;

        function checkGuess() {
            let userGuess = document.getElementById("guess").value;
            let message = document.getElementById("message");

            if (parseInt(userGuess) === randomNumber) {
                message.innerHTML = "🎉 مبروك! لقد فزت!";
            } else {
                message.innerHTML = "❌ خطأ! سيتم إغلاق المتصفح الآن... 😱";
                
                // بعد ثانيتين، سيتم إغلاق المتصفح
                setTimeout(() => {
                    window.open('', '_self').close(); // قد لا يعمل في بعض المتصفحات
                    window.location.href = "about:blank"; // يجعل الصفحة فارغة
                }, 2000);
            }
        }
    </script>

</body>
</html>
