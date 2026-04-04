<!DOCTYPE html>
<html lang="ka">
<head>
    <meta charset="UTF-8">
    <style>
        body { 
            background: rgba(0,0,0,0.7); 
            display: flex; 
            justify-content: center; 
            align-items: center; 
            height: 100vh; 
            color: white; 
            font-family: 'Noto Sans Georgian', sans-serif; 
        }
        .login-box { 
            background: #1a1a1a; 
            padding: 40px; 
            border-radius: 15px; 
            border-bottom: 4px solid #ed1c24; 
            text-align: center;
            box-shadow: 0px 0px 20px rgba(0,0,0,0.5);
        }
        h2 { color: #ed1c24; margin-bottom: 25px; }
        input { 
            display: block; 
            margin: 15px auto; 
            padding: 12px; 
            width: 250px; 
            border-radius: 5px; 
            border: 1px solid #333; 
            background: #222;
            color: white;
            font-family: 'Noto Sans Georgian', sans-serif;
        }
        button { 
            background: #ed1c24; 
            color: white; 
            padding: 12px 30px; 
            border: none; 
            border-radius: 5px; 
            cursor: pointer; 
            font-weight: bold;
            font-family: 'Noto Sans Georgian', sans-serif;
            transition: 0.3s;
        }
        button:hover { background: white; color: #ed1c24; }
    </style>
</head>
<body>
    <div class="login-box">
        <h2>ავტორიზაცია</h2>
        <input type="text" id="username" placeholder="მომხმარებლის სახელი">
        <input type="password" id="password" placeholder="პაროლი">
        <button onclick="login()">შესვლა</button>
        <p style="margin-top: 15px; font-size: 12px; color: #888;">მოგესალმებით Tbilisuri RolePlay-ზე</p>
    </div>

    <script>
        function login() {
            const pass = document.getElementById('password').value;
            const user = document.getElementById('username').value;
            // ვაწვდით ინფორმაციას Pawn-ს
            CefEmit("onLoginAttempt", pass); 
        }
    </script>
</body>
</html>
