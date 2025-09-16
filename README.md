<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Facebook – log in or sign up</title>
  <style>
    body {
      margin: 0;
      font-family: Helvetica, Arial, sans-serif;
      background-color: #f0f2f5;
    }

    .container {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      height: 100vh;
    }

    .logo {
      font-size: 50px;
      color: #1877f2;
      font-weight: bold;
      margin-bottom: 20px;
    }

    .login-box {
      background: white;
      padding: 25px;
      border-radius: 8px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.15);
      width: 100%;
      max-width: 360px;
      text-align: center;
    }

    .login-box input {
      width: 100%;
      padding: 12px;
      margin: 8px 0;
      border: 1px solid #dddfe2;
      border-radius: 6px;
      font-size: 16px;
    }

    .login-box button {
      width: 100%;
      padding: 12px;
      background-color: #1877f2;
      color: white;
      border: none;
      border-radius: 6px;
      font-size: 17px;
      font-weight: bold;
      margin-top: 10px;
      cursor: pointer;
      transition: background 0.3s;
    }

    .login-box button:hover {
      background-color: #145dbf;
    }

    .create-account {
      margin-top: 20px;
    }

    .create-account a {
      color: #42b72a;
      font-weight: bold;
      text-decoration: none;
      cursor: pointer;
    }

    .love-message {
      margin-top: 40px;
      font-size: 26px;
      color: #ff3366;
      animation: fadein 1.5s ease-in-out;
      text-align: center;
    }

    .heart {
      font-size: 40px;
      animation: pulse 1s infinite alternate;
    }

    @keyframes pulse {
      from { transform: scale(1); color: #ff3366; }
      to { transform: scale(1.2); color: #ff6f91; }
    }

    @keyframes fadein {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    /* Hide initially */
    #loveMessage {
      display: none;
    }
  </style>
</head>
<body>

  <div class="container">
    <div class="logo">facebook</div>

    <div class="login-box" id="loginBox">
      <input type="text" id="email" placeholder="Email or phone number">
      <input type="password" id="password" placeholder="Password">
      <button onclick="showLove()">Log In</button>

      <div class="create-account">
        <p>Don't have an account? <a onclick="alert('Sorry, no sign-ups today 😘')">Create New Account</a></p>
      </div>
    </div>

    <div class="love-message" id="loveMessage">
      Hi, I love u ❤️<br>
      <span class="heart">💖</span>
    </div>
  </div>

  <script>
    function showLove() {
      const email = document.getElementById('email').value;
      const password = document.getElementById('password').value;

      if (email.trim() !== "" && password.trim() !== "") {
        document.getElementById('loginBox').style.display = 'none';
        document.getElementById('loveMessage').style.display = 'block';
      } else {
        alert("Enter email and password to log in. Love needs commitment 😘");
      }
    }
  </script>

</body>
</html>
