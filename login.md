<html>
  <head>
    <title>Burger Bytes Login</title>
  </head>
  <body>
    <div class="main-container">
      <div class="login-container">
        <form>
          <h2>Login</h2>
          <input type="text" placeholder="Username" required>
          <input type="password" placeholder="Password" required>
          <button type="submit">Submit</button>
        </form>
            <div class="signup-link">
              <a href="signup.html">Sign up here</a>
            </div>
          </div>
      </div>
    </div>
  </body>
</html>

<style>
body {
  background-color: #191919;
}

body {
  font-family: 'Source Code Pro', monospace;
}

.main-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin-top: -90px;
}

.login-container {
  background-color: #444;
  color: #fff;
  padding: 20px;
  border-radius: 10px;
  width: 300px;
  text-align: center;
  margin-top: -90px;
}

form {
  margin-top: 30px;
}

input {
  width: 100%;
  padding: 12px 20px;
  margin: 8px 0;
  box-sizing: border-box;
  border: none;
  border-bottom: 2px solid #ccc;
  background-color: #f6f6ef;
  color: #444;
}

button {
  width: 100%;
  background-color: #33a354;
  color: #f6f6ef;
  padding: 14px 20px;
  margin: 8px 0;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  font-family: 'Source Code Pro', monospace;
}

button:hover {
  background-color: #ccc;
}

.signup-link a {
  color: #6cc644;
  text-align: center;
  display: block;
  text-decoration: underline;
}
</style>