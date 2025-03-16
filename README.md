
<!DOCTYPE html>

<html lang="en">

  <head>

  <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
  
  <title>Happy Birthday!</title>
  <style>
    
      body {
            font-family: cursive;
            margin: 0;
            padding: 0;
            text-align: center;
            background: black;
            overflow: hidden;
            position: relative;
     }
      
      .container {
            position: relative;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
        }

        .card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 8px 16px rgba(255, 0, 0, 0.5);
            max-width: 500px;
            animation: fadeIn 2s ease-in-out;
            position: relative;
            z-index: 2;
            color: white;
            border: 2px solid #ff4081;
        }

        h1 {
            color: #ff4081;
            font-size: 2.5em;
            text-shadow: 0 0 10px #ff4081, 0 0 20px #ff4081;
        }

        #message {
            font-size: 18px;
            color: white;
            text-align: left;
            white-space: pre-line;
            border-right: 2px solid #ff4081;
            display: inline-block;
            overflow: hidden;
            width: 0;
            animation: typing 4s steps(80, end) forwards, blink 0.7s infinite;
        }

        @keyframes typing {
            from { width: 0; }
            to { width: 100%; }
        }

        @keyframes blink {
            50% { border-color: transparent; }
        }

        .hearts {
            position: absolute;
            width: 100%;
            height: 100%;
            overflow: hidden;
            z-index: 1;
        }

        .heart {
            font-size: 30px;
            position: absolute;
            bottom: -100px;
            animation: float 6s infinite ease-in-out;
            opacity: 0.8;
        }

        .heart:nth-child(1) { left: 10%; animation-duration: 6s; }
        .heart:nth-child(2) { left: 20%; animation-duration: 7s; }
        .heart:nth-child(3) { left: 30%; animation-duration: 5s; }
        .heart:nth-child(4) { left: 40%; animation-duration: 6.5s; }
        .heart:nth-child(5) { left: 50%; animation-duration: 7.5s; }
        .heart:nth-child(6) { left: 60%; animation-duration: 6.2s; }
        .heart:nth-child(7) { left: 70%; animation-duration: 6.8s; }
        .heart:nth-child(8) { left: 80%; animation-duration: 7.2s; }
        .heart:nth-child(9) { left: 90%; animation-duration: 5.5s; }

        @keyframes float {
            0% { transform: translateY(0); opacity: 1; }
            50% { transform: translateY(-50vh); opacity: 0.8; }
            100% { transform: translateY(-100vh); opacity: 0; }
        }
    </style>
</head>
<body>

    <div class="container">
        <div class="hearts">
            <div class="heart">💕</div>
            <div class="heart">❤️</div>
            <div class="heart">💕</div>
            <div class="heart">❤️</div>
            <div class="heart">💕</div>
            <div class="heart">❤️</div>
            <div class="heart">💕</div>
            <div class="heart">❤️</div>
            <div class="heart">💕</div>
        </div>

        <div class="card">
            <h1>🎉 Happy Birthday, ANNIE! 🎈</h1>
            <p id="message"></p>
        </div>
    </div>

    <script>
        const messageText = `Dear Annie, 💕❤️Today is your special day, and I just want to remind you how **amazing** you are! 🥳Thank you for being such a **wonderful friend**—always bringing happiness, laughter, and good vibes. May this year be filled with love, success, and endless joy! 💖Enjoy your day to the fullest! 🎂🎁✨With lots of love,The Optimist`;

        let index = 0;
        function typeEffect() {
            document.getElementById("message").textContent = messageText.slice(0, index);
            index++;
            if (index <= messageText.length) {
                setTimeout(typeEffect, 50);
            }
        }

        setTimeout(typeEffect, 1000);
    </script>

</body>
</html> 
