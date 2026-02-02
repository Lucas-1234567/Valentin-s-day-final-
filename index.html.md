#   
<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <meta name="viewport" content="width=device-width, initial-scale=1.0">  
    <title>A Special Question for You ❤️</title>  
    <style>  
        body {  
            margin: 0;  
            padding: 0;  
            display: flex;  
            justify-content: center;  
            align-items: center;  
            height: 100vh;  
            background: linear-gradient(135deg, #fcecf0 0%, #f7dadd 100%);  
            font-family: 'Arial Rounded MT Bold', 'Helvetica', sans-serif;  
            overflow: hidden;  
            color: #d63384;  
        }  
  
        #card {  
            background: white;  
            padding: 40px;  
            border-radius: 30px;  
            box-shadow: 0 15px 35px rgba(0,0,0,0.1);  
            text-align: center;  
            max-width: 400px;  
            z-index: 10;  
        }  
  
        h1 { font-size: 2rem; margin: 20px 0; }  
  
        .btn-container {  
            display: flex;  
            justify-content: center;  
            align-items: center;  
            gap: 20px;  
            margin-top: 20px;  
            height: 150px; /* Espace pour la croissance du bouton */  
        }  
  
        button {  
            padding: 15px 30px;  
            border: none;  
            border-radius: 15px;  
            font-size: 1.1rem;  
            font-weight: bold;  
            cursor: pointer;  
            transition: all 0.2s ease;  
        }  
  
        #yesBtn {  
            background-color: #ff4d6d;  
            color: white;  
        }  
  
        #noBtn {  
            background-color: #adb5bd;  
            color: white;  
            position: absolute; /* Important pour l'esquive */  
        }  
  
        img { width: 180px; border-radius: 15px; }  
    </style>  
</head>  
<body>  
  
    <div id="card">  
        <img id="status-gif" src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExOHpwaGZ4Z3R4Z3R4Z3R4Z3R4Z3R4Z3R4Z3R4Z3R4Z3R4Z3R4Z3R4Z3R4Z3R4Z3R4Z3R4Z3R4Z3&ep=v1_gifs_search&rid=giphy.gif&ct=g" alt="Cute gif">  
        <h1 id="question">Will you be my Valentine? ❤️</h1>  
        <div class="btn-container">  
            <button id="yesBtn">YES</button>  
            <button id="noBtn">NO</button>  
        </div>  
    </div>  
  
    <script>  
        const noBtn = document.getElementById('noBtn');  
        const yesBtn = document.getElementById('yesBtn');  
        const question = document.getElementById('question');  
        const gif = document.getElementById('status-gif');  
          
        let yesScale = 1;  
        let noClicks = 0;  
  
        function moveButton() {  
            // Calcule une position aléatoire sécurisée  
            const x = Math.random() * (window.innerWidth - noBtn.offsetWidth - 20);  
            const y = Math.random() * (window.innerHeight - noBtn.offsetHeight - 20);  
              
            noBtn.style.left = `${x}px`;  
            noBtn.style.top = `${y}px`;  
              
            // Fait grossir le bouton OUI  
            yesScale += 0.5;  
            yesBtn.style.transform = `scale(${yesScale})`;  
              
            // Bonus : change le texte si elle persiste  
            noClicks++;  
            if(noClicks > 5) question.innerText = "Please? 🥺";  
            if(noClicks > 10) question.innerText = "You're clicking the wrong one! 😤";  
        }  
  
        // Esquive au survol (PC) et au toucher (Mobile)  
        noBtn.addEventListener('mouseover', moveButton);  
        noBtn.addEventListener('touchstart', (e) => {  
            e.preventDefault();  
            moveButton();  
        });  
  
        // Succès  
        yesBtn.addEventListener('click', () => {  
            document.getElementById('card').innerHTML = `  
                <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExbmZ0bmZ0bmZ0bmZ0bmZ0bmZ0bmZ0bmZ0bmZ0bmZ0bmZ0bmZ0&ep=v1_gifs_search&rid=giphy.gif&ct=g">  
                <h1>I knew it! Love you! 🥰 ❤️</h1>  
            `;  
        });  
    </script>  
</body>  
</html>  
