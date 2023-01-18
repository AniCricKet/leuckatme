<style>
  .main-container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin-top: -90px;
  }

  .login-container {
    background-color: #201c1c;
    padding: 20px;
    margin-top: -90px;
    border-radius: 10px;
    box-shadow: 0px 0px 10px 0px #ccc;
    width: 400px;
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
    background-color: #f6f6ef;
    color: #444;
  }

  button {
    width: 100%;
    background-color: #ace34b;
    color: #fff;
    padding: 14px 20px;
    margin: 8px 0;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }

  button:hover {
    background-color: #4caf50;
  }

  .signup-link a {
    color: #ace34b;
    text-align: center;
    display: block;
    text-decoration: underline;
  }
</style>


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
            <a href="signup">Don't have an account? Sign Up here!</a>
          </div>
        </div>
    </div>
  </div>
</body>

<form>
  <input type="text" id="input-field">
  <button type="submit" id="submit-button">Submit</button>
</form>

<script>
  const submitButton = document.getElementById("submit-button");
  submitButton.addEventListener("click", function(event) {
    event.preventDefault(); // prevent the form from submitting

    const inputField = document.getElementById("input-field");
    const data = { input: inputField.value };

    fetch("/submit", {
      method: "POST",
      body: JSON.stringify(data),
      headers: { "Content-Type": "application/json" }
    })
    .then(response => {
      console.log("Success:", response);
    })
    .catch(error => {
      console.error("Error:", error);
    });
  });
</script>
