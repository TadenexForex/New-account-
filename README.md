# New-account-<!-- Start of login page code -->
<html>
  <head>
    <title>Tadenex Forex capital - Login</title>
  </head>
  <body>
    <h1>Login</h1>
    <form action="login.php" method="post">
      <label for="username">Username:</label>
      <input type="text" id="username" name="username"><br><br>
      <label for="password">Password:</label>
      <input type="password" id="password" name="password"><br><br>
      <input type="submit" value="Login">
    </form>
  </body>
</html>
<!-- End of login page code -->
<form action="login.php" method="post">
  <label for="username">Username:</label>
  <input type="text" id="username" name="username"><br><br>
  <label for="password">Password:</label>
  <input type="password" id="password" name="password"><br><br>
  <input type="submit" value="Login">
</form>
<script>
function validateForm() {
  var username = document.forms["loginForm"]["username"].value;
  var password = document.forms["loginForm"]["password"].value;
  if (username == "" || password == "") {
    alert("Please fill in all fields");
    return false;
  }
}
</script>
<form action="login.php" method="post" name="loginForm" onsubmit="return validateForm()">
  <label for="username">Username:</label>
  <input type="text" id="username" name="username"><br><br>
  <label for="password">Password:</label>
  <input type="password" id="password" name="password"><br><br>
  <input type="submit" value="Login">
</form>
<?php
session_start();

$username = $_POST['username'];
$password = $_POST['password'];

// Replace the following with your actual authentication logic
if ($username == "example" && $password == "password123") {
  $_SESSION['loggedIn'] = true;
  header('Location: welcome.php');
} else {
  header('Location: login.php?error=1');
}
?>
