<!DOCTYPE html>
<html lang="my">
<head>
    <meta charset="UTF-8">
    <title>For You</title>
    <style>
        body {
            background-color: #fce4ec;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            font-family: sans-serif;
            margin: 0;
            overflow: hidden;
        }
        .box {
            background: white;
            padding: 35px;
            border-radius: 20px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            text-align: center;
            position: relative;
            width: 320px;
        }
        h3 {
            color: #d81b60;
            margin-bottom: 25px;
            font-size: 18px;
        }
        .buttons {
            display: flex;
            justify-content: space-around;
            align-items: center;
            gap: 20px;
            margin-top: 20px;
        }
        button {
            padding: 10px 25px;
            border: none;
            border-radius: 20px;
            font-size: 16px;
            cursor: pointer;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
            font-weight: bold;
        }
        #yesBtn {
            background: #ff4081;
            color: white;
        }
        #yesBtn:hover {
            background: #e91e63;
        }
        #noBtn {
            background: #e0e0e0;
            color: #333;
            position: absolute;
            transition: 0.1s;
        }
    </style>
</head>
<body>
    <div class="box">
        <h3>ငါတို့ တစ်ကစနေ ပြန်စဥ်းစားမလား</h3>
        <div class="buttons">
            <button id="yesBtn" onclick="alert('Yay! ❤️ သဘောတူပြီနော်')">Yes</button>
            <button id="noBtn" onmouseover="moveNo()" onclick="moveNo()">No</button>
        </div>
    </div>

    <script>
        function moveNo() {
            const noBtn = document.getElementById('noBtn');
            const maxX = window.innerWidth - noBtn.offsetWidth - 50;
            const maxY = window.innerHeight - noBtn.offsetHeight - 50;
            
            const randomX = Math.floor(Math.random() * maxX);
            const randomY = Math.floor(Math.random() * maxY);
            
            noBtn.style.position = 'fixed';
            noBtn.style.left = randomX + 'px';
            noBtn.style.top = randomY + 'px';
        }
    </script>
</body>
</html>
