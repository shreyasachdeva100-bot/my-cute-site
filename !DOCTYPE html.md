#   
<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <title>Come Over</title>  
    <style>  
        body {  
            margin: 0;  
            height: 100vh;  
            overflow: hidden;  
            display: flex;  
            align-items: center;  
            justify-content: center;  
            font-family: Arial, sans-serif;  
  
            /* Pink gradient background */  
            background: linear-gradient(135deg, #ff9a9e, #fad0c4, #fbc2eb);  
        }  
  
        h1 {  
            font-size: 42px;  
            color: #ffffff;  
            text-shadow: 0 2px 8px rgba(0,0,0,0.2);  
            z-index: 2;  
        }  
  
        .emoji {  
            position: absolute;  
            font-size: 30px;  
            animation: floatUp linear infinite;  
            opacity: 0.9;  
        }  
  
        @keyframes floatUp {  
            from {  
                transform: translateY(100vh);  
                opacity: 1;  
            }  
            to {  
                transform: translateY(-10vh);  
                opacity: 0;  
            }  
        }  
    </style>  
</head>  
<body>  
  
    <h1>Come over please</h1>  
  
    <script>  
        const emojis = ["❤️", "☺️", "🌸", "🫦", "😍"];  
  
        function createEmoji() {  
            const emoji = document.createElement("div");  
            emoji.className = "emoji";  
            emoji.innerText = emojis[Math.floor(Math.random() * emojis.length)];  
  
            emoji.style.left = Math.random() * 100 + "vw";  
            emoji.style.animationDuration = (3 + Math.random() * 4) + "s";  
            emoji.style.fontSize = (24 + Math.random() * 20) + "px";  
  
            document.body.appendChild(emoji);  
  
            setTimeout(() => emoji.remove(), 7000);  
        }  
  
        setInterval(createEmoji, 300);  
    </script>  
  
</body>  
</html>  
  
