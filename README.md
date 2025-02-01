<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be My Valentine?</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            background-color: #ffccdd;
            margin: 0;
            padding: 0;
        }

        .container {
            margin-top: 100px;
        }

        h1 {
            color: #d63384;
            font-size: 40px;
        }

        .heart {
            font-size: 50px;
            color: red;
        }

        .buttons {
            margin-top: 30px;
        }

        .btn {
            font-size: 20px;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            cursor: pointer;
            border-radius: 10px;
        }

        .yes {
            background-color: #ff4d6d;
            color: white;
        }

        .no {
            background-color: #333;
            color: white;
            position: absolute;
        }

    </style>
</head>
<body>
    <div class="container">
        <h1>Will You Be My Valentine? <span class="heart">❤️</span></h1>
        <div class="buttons">
            <button class="btn yes" onclick="showLove()">Yes</button>
            <button class="btn no" id="noBtn" onmouseover="moveNo()">No</button>
        </div>
        <p id="message" style="display:none; font-size: 25px; color: #d63384; margin-top: 30px;"></p>
    </div>

    <script>
        function showLove() {
            document.getElementById("message").innerHTML = "Yay! I knew you'd say yes! ❤️";
            document.getElementById("message").style.display = "block";
        }

        function moveNo() {
            let button = document.getElementById("noBtn");
            let x = Math.random() * window.innerWidth * 0.7;
            let y = Math.random() * window.innerHeight * 0.7;
            button.style.left = x + "px";
            button.style.top = y + "px";
        }
    </script>
</body>
</html>
