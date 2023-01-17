<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" type="text/css" href="style.css">
    <title>Burger Bytes Sign Up</title>
  </head>
  <body>
    <header>
      <div class="container">
        <table>
          <tr>
              <td><a href="/">Home&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</a></td>
              <td><a href="/hours">Hours&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</a></td>
              <td><a href="/menu">Menu&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</a></td>
              <td><a href="/gallery">Gallery&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</a></td>
              <td><a href="/login">Login&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</a></td>
              <td><a href="/employment">Employment&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</a></td>
          </tr>
      </table>
      </div>
    </header>
    <div class="main-container">
      <div class="signup-container">
        <form>
          <h2>Sign Up</h2>
          <input type="text" placeholder="Username" required>
          <input type="email" placeholder="Email" required>
          <input type="password" placeholder="Password" required>
          <input type="password" placeholder="Confirm Password" required>
          <button type="submit">Submit</button>
        </form>
      </div>
    </div>
  </body>
</html>

<style>
  body {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #f2f2f2;
}

.signup-container {
  background-color: #fff;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0px 0px 10px 0px #ccc;
  width: 300px;
  text-align: center;
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
}

button {
  width: 100%;
  background-color: #4CAF50;
  color: white;
  padding: 14px 20px;
  margin: 8px 0;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: #45a049;
}

h2 {
  margin-bottom: 20px;
}

header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background-color: #fff;
  padding: 10px;
  border-radius: 10px;
  box-shadow: 0px 0px 10px 0px #ccc;
  text-align: center;
}

header .container {
  margin: auto;
  display: flex;
  justify-content: center;
}


header a {
  color: #000;
  text-decoration: none;
  margin-right: 10px;
  font-size: 16px;
  padding: 15 px;
}

header a:hover {
  color: #4CAF50;
}

header table {
  margin: 0;
}
</style>