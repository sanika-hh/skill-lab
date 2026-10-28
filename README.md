<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Login Page</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }

    body {
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: linear-gradient(135deg, #667eea, #764ba2);
    }

    .login-box {
      width: 350px;
      padding: 35px;
      background: white;
      border-radius: 15px;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
    }

    h2 {
      text-align: center;
      margin-bottom: 25px;
      color: #333;
    }

    .input-group {
      margin-bottom: 18px;
    }

    label {
      display: block;
      margin-bottom: 8px;
      color: #444;
    }

    input {
      width: 100%;
      padding: 12px;
      border: 1px solid #ccc;
      border-radius: 7px;
      outline: none;
    }

    input:focus {
      border-color: #667eea;
    }

    .show-password {
      margin-top: 10px;
      font-size: 13px;
    }

    .show-password input {
      width: auto;
    }

    button {
      width: 100%;
      padding: 12px;
      border: none;
      border-radius: 7px;
      background: #667eea;
      color: white;
      font-size: 16px;
      cursor: pointer;
    }

    button:hover {
      background: #5265d5;
    }

    #message {
      text-align: center;
      margin-top: 15px;
      font-size: 14px;
    }

    .signup {
      text-align: center;
      margin-top: 20px;
      font-size: 14px;
    }

    .signup a {
      color: #667eea;
      text-decoration: none;
    }
  </style>
</head>

<body>
  <div class="login-box">
    <h2>Login</h2>

    <form id="loginForm">
      <div class="input-group">
        <label for="email">Email Address</label>
        <input
          type="email"
          id="email"
          placeholder="Enter your email"
          required
        >
      </div>

      <div class="input-group">
        <label for="password">Password</label>
        <input
          type="password"
          id="password"
          placeholder="Enter your password"
          required
          minlength="6"
        >

        <div class="show-password">
          <input type="checkbox" id="showPassword">
          <label for="showPassword" style="display:inline">
            Show password
          </label>
        </div>
      </div>

      <button type="submit">Login</button>
      <p id="message" role="status"></p>
    </form>

    <p class="signup">
      Don't have an account? <a href="signup.html">Sign up</a>
    </p>
  </div>

  <script>
    const password = document.getElementById("password");
    const showPassword = document.getElementById("showPassword");
    const form = document.getElementById("loginForm");
    const message = document.getElementById("message");

    showPassword.addEventListener("change", function () {
      password.type = this.checked ? "text" : "password";
    });

    form.addEventListener("submit", function (event) {
      event.preventDefault();

      message.style.color = "#d97706";
      message.textContent =
        "Form validated. Connect a backend to authenticate your account.";
    });
  </script>
</body>
</html># skill-lab
