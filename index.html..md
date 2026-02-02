#   
<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <meta name="viewport" content="width=device-width, initial-scale=1.0">  
    <title>A Special Valentine's Invitation ❤️</title>  
    <link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Quicksand:wght@400;700&display=swap" rel="stylesheet">  
    <style>  
        :root {  
            --primary-pink: #FF69B4; /* Hot Pink */  
            --secondary-pink: #FFB6C1; /* Light Pink */  
            --accent-red: #FF4500;    /* Orange Red */  
            --button-yes: #4CAF50;    /* Green for Yes */  
            --button-no: #F44336;     /* Red for No */  
            --text-color: #333;  
            --background-gradient: linear-gradient(135deg, #fcecf0 0%, #f7dadd 100%);  
        }  
  
        body {  
            margin: 0;  
            padding: 0;  
            display: flex;  
            justify-content: center;  
            align-items: center;  
            min-height: 100vh;  
            background: var(--background-gradient);  
            font-family: 'Quicksand', sans-serif;  
            color: var(--text-color);  
            overflow: hidden; /* Prevent scroll when noBtn moves */  
            position: relative;  
        }  
  
        .background-elements {  
            position: absolute;  
            width: 100%;  
            height: 100%;  
            overflow: hidden;  
            z-index: 1;  
        }  
  
        .flag-element {  
            position: absolute;  
            opacity: 0.1;  
            font-size: 8em;  
            animation: float 20s infinite ease-in-out;  
        }  
  
        .flag-colombia-left {  
            top: 10%; left: 5%;  
            transform: rotate(-15deg);  
        }  
        .flag-colombia-right {  
            bottom: 20%; right: 10%;  
            transform: rotate(20deg);  
            animation-delay: 5s;  
        }  
        .flag-france-top {  
            top: 5%; right: 20%;  
            transform: rotate(5deg);  
            animation-delay: 10s;  
        }  
        .flag-france-bottom {  
            bottom: 5%; left: 20%;  
            transform: rotate(-10deg);  
            animation-delay: 15s;  
        }  
  
        @keyframes float {  
            0% { transform: translateY(0px); }  
            50% { transform: translateY(-30px); }  
            100% { transform: translateY(0px); }  
        }  
  
        #card {  
            background: rgba(255, 255, 255, 0.95);  
            padding: 40px;  
            border-radius: 30px;  
            box-shadow: 0 15px 35px rgba(0,0,0,0.15);  
            text-align: center;  
            max-width: 450px;  
            width: 90%;  
            z-index: 10;  
            position: relative; /* For z-index to work */  
            backdrop-filter: blur(5px); /* Frosted glass effect */  
        }  
  
        h1, h2 {  
            font-family: 'Pacifico', cursive;  
            color: var(--primary-pink);  
            font-size: 2.5rem;  
            margin: 10px 0 25px;  
            line-height: 1.2;  
        }  
  
        .gif-container {  
            margin-bottom: 20px;  
        }  
  
        .gif-container img {  
            width: 150px;  
            height: 150px;  
            border-radius: 50%;  
            object-fit: cover;  
            border: 4px solid var(--secondary-pink);  
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);  
            animation: pulse 1.5s infinite alternate;  
        }  
  
        @keyframes pulse {  
            0% { transform: scale(1); box-shadow: 0 5px 15px rgba(0,0,0,0.1); }  
            100% { transform: scale(1.05); box-shadow: 0 8px 20px rgba(0,0,0,0.2); }  
        }  
  
        .btn-container {  
            display: flex;  
            justify-content: center;  
            align-items: center;  
            gap: 20px;  
            margin-top: 30px;  
            min-height: 80px; /* Ensure space for growing buttons */  
            position: relative; /* For noBtn absolute positioning */  
        }  
  
        button {  
            padding: 15px 35px;  
            border: none;  
            border-radius: 50px;  
            font-size: 1.2rem;  
            font-weight: 700;  
            cursor: pointer;  
            transition: all 0.2s ease-in-out, transform 0.1s;  
            box-shadow: 0 8px 15px rgba(0,0,0,0.1);  
            white-space: nowrap; /* Prevent text wrap */  
        }  
  
        #yesBtn, #yesBtn2 {  
            background-color: var(--primary-pink);  
            color: white;  
        }  
  
        #noBtn, #noBtn2 {  
            background-color: var(--secondary-pink);  
            color: white;  
            position: absolute; /* Essential for evasion */  
        }  
  
        /* Hover effects */  
        button:hover {  
            transform: translateY(-3px);  
            box-shadow: 0 12px 20px rgba(0,0,0,0.15);  
        }  
  
        #yesBtn:hover, #yesBtn2:hover {  
            background-color: #FF5A9C;  
        }  
  
        #noBtn:hover, #noBtn2:hover {  
            background-color: #EEA0AD;  
        }  
  
        /* Gift Box */  
        .gift-box-container {  
            margin-top: 30px;  
            cursor: pointer;  
            transition: transform 0.3s ease;  
        }  
  
        .gift-box-container:hover {  
            transform: scale(1.05);  
        }  
  
        .gift-box {  
            width: 120px;  
            height: 100px;  
            background-color: var(--primary-pink);  
            border-radius: 10px;  
            position: relative;  
            margin: 0 auto;  
            box-shadow: 0 8px 15px rgba(0,0,0,0.2);  
        }  
  
        .gift-box::before { /* Ribbon */  
            content: '';  
            position: absolute;  
            width: 30px;  
            height: 120px;  
            background-color: var(--accent-red);  
            top: -10px;  
            left: 50%;  
            transform: translateX(-50%);  
            border-radius: 5px;  
        }  
        .gift-box::after { /* Bow */  
            content: '';  
            position: absolute;  
            width: 60px;  
            height: 20px;  
            background-color: var(--accent-red);  
            top: -15px;  
            left: 50%;  
            transform: translateX(-50%);  
            border-radius: 10px;  
            box-shadow: 0 2px 5px rgba(0,0,0,0.3);  
        }  
  
        .gift-text {  
            font-family: 'Pacifico', cursive;  
            font-size: 1.8rem;  
            color: var(--primary-pink);  
            margin-top: 20px;  
            opacity: 0;  
            transform: translateY(20px);  
            transition: opacity 0.5s ease, transform 0.5s ease;  
        }  
        .gift-text.revealed {  
            opacity: 1;  
            transform: translateY(0);  
        }  
  
        /* Confetti for celebration */  
        .confetti-canvas {  
            position: fixed;  
            top: 0;  
            left: 0;  
            width: 100%;  
            height: 100%;  
            pointer-events: none;  
            z-index: 9999;  
        }  
  
        /* Responsive adjustments */  
        @media (max-width: 600px) {  
            #card {  
                padding: 25px;  
                border-radius: 20px;  
                max-width: 95%;  
            }  
            h1, h2 {  
                font-size: 2rem;  
            }  
            .gif-container img {  
                width: 120px;  
                height: 120px;  
            }  
            button {  
                padding: 12px 25px;  
                font-size: 1rem;  
            }  
            .gift-box {  
                width: 100px;  
                height: 80px;  
            }  
            .gift-box::before { width: 25px; height: 100px; }  
            .gift-box::after { width: 50px; height: 18px; }  
            .gift-text { font-size: 1.5rem; }  
            .flag-element { font-size: 6em; }  
        }  
    </style>  
</head>  
<body>  
  
    <div class="background-elements">  
        <span class="flag-element flag-colombia-left">🇨🇴</span>  
        <span class="flag-element flag-colombia-right">🇨🇴</span>  
        <span class="flag-element flag-france-top">🇫🇷</span>  
        <span class="flag-element flag-france-bottom">🇫🇷</span>  
        <span class="flag-element" style="top: 30%; left: 30%; font-size: 7em; animation-delay: 2s;">❤️</span>  
        <span class="flag-element" style="bottom: 15%; right: 30%; font-size: 6em; animation-delay: 7s;">✨</span>  
    </div>  
  
    <div id="card">  
        <div class="gif-container">  
            <img id="status-gif" src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExOHpwaGZ4Z3R4Z3R4Z3R4Z3R4Z3R4Z3R4Z3R4Z3R4Z3R4Z3R4Z3R4Z3R4Z3R4Z3R4Z3R4Z3R4Z3&ep=v1_gifs_search&rid=giphy.gif&ct=g" alt="Cute gif">  
        </div>  
        <h1 id="question">Will you be my Valentine? ❤️</h1>  
        <div class="btn-container">  
            <button id="yesBtn">YES</button>  
            <button id="noBtn">NO</button>  
        </div>  
  
        <div id="secondQuestionContainer" style="display: none;">  
            <h2 style="margin-top: 40px;">Want to know where we're eating? 🍽️</h2>  
            <div class="btn-container">  
                <button id="yesBtn2">YES</button>  
                <button id="noBtn2">NO</button>  
            </div>  
        </div>  
  
        <div id="giftContainer" style="display: none;">  
            <div class="gift-box-container" onclick="revealRestaurant()">  
                <div class="gift-box"></div>  
                <p class="gift-text" id="restaurantName">Caffe Fernet</p>  
            </div>  
        </div>  
    </div>  
  
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.9.2/dist/confetti.browser.min.js"></script>  
  
    <script>  
        const noBtn = document.getElementById('noBtn');  
        const yesBtn = document.getElementById('yesBtn');  
        const noBtn2 = document.getElementById('noBtn2');  
        const yesBtn2 = document.getElementById('yesBtn2');  
        const question = document.getElementById('question');  
        const statusGif = document.getElementById('status-gif');  
        const secondQuestionContainer = document.getElementById('secondQuestionContainer');  
        const giftContainer = document.getElementById('giftContainer');  
        const restaurantName = document.getElementById('restaurantName');  
  
        let yesScale = 1; // For first Yes button  
        let yesScale2 = 1; // For second Yes button  
        let noClicks = 0; // For first  
