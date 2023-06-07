<!DOCTYPE html>
<html>
<head>
	<title>Smart Library - Login</title>	
	<style>
		body {
			background-image: url('https://images.wallpaperscraft.com/image/single/books_library_shelves_138556_3840x2160.jpg');
			background-repeat: no-repeat;
			background-size: cover;
      background-color: #EAF4EB;
			font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
		}
		fieldset {
			margin: 0 auto;
			width: 300px;
			background-color: #fff;
			padding: 100px;
			border-radius: 10px;
			box-shadow: 0 0 10px rgba(0,0,0,0.3);
		}
		
		h1 {
			text-align: center;
			margin-bottom: 20px;
			color: #2E7166;
		}
		
		label {
			display: block;
			margin-bottom: 10px;
			color: #333;
			font-size: 16px;
			font-weight: bold;
		}	
		input[type="text"], input[type="password"] {
			width: 100%;
			padding: 10px;
			border:#333;
			border-radius: 5px;
			margin-bottom: 20px;
			box-sizing: border-box;
			font-size: 16px;
		}b 
		button[type="submit"] {
			background-color: #2E7166;
			color: #fff;
			border: none;
			border-radius: 5px;
			padding: 10px 20px;
			font-size: 16px;
			cursor: pointer;
		}
		
		.signup {
			text-align: center;
			margin-top: 20px;
		}
		
		.signup a {
			color: #2E7166
			text-decoration: none;
			font-weight: bold;
		}
		
    .form-container {
			background-color: #FFFFFF;
			max-width: 500px;
			margin: 50px auto;
			padding: 20px;
			border-radius: 10px;
			box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
		}

    .form-container input[type=text], .form-container input[type=password]{
			width: 100%;
			padding: 12px 20px;
			margin: 8px 0;
			display: inline-block;
			border: 1px solid #ccc;
			border-radius: 4px;
			box-sizing: border-box;
		}
    .form-container button {
			background-color: #2E7166;
			color: #FFFFFF;
			padding: 12px 20px;
			border: none;
			border-radius: 4px;
			cursor: pointer;
			width: 100%;
			margin-top: 10px;
			font-size: 18px;
		}
    
		.navbar {
			background-color: #2E7166;
			overflow: hidden;
			display: flex;
			justify-content: space-between;
			align-items: center;
			padding: 10px;
		}
		
		.navbar a {
			color: #FFFFFF;
			text-decoration: none;
			margin: 0 10px;
			font-size: 18px;
		}
		
		.logo {
			font-weight: bold;
			font-size: 24px;
		}

		.tooltip {
  position: absolute;
  z-index: 1;
  display: none;
  padding: 10px;
  border-radius: 5px;
  background-color: #fff;
  box-shadow: 0px 0px 5px rgba(0, 0, 0, 0.2);
  top: 60px;
  right: 0;
}

.help-link:hover + .tooltip {
  display: block;
}
button:hover {
  background-color:#333;
}
	</style>
</head>
<body>	
	<div class="navbar">
		<span class="logo" style="color:#ccc">Smart Library</span>
		<a href="#" class="help-link">Help</a>
		<span class="tooltip">Chairman<br>Suyog Baral<br>Contact:<br>suyogbaral9@gmail.com</span>
	  </div>
  <div class="form-container">
	<form name="loginForm" onsubmit="return validateForm()">
		<h1>Login</h1>
		<label for="username">Username:</label>
		<input type="text" id="username" name="username" required>
		<label for="password">Password:</label>
		<input type="password" id="password" name="password" required>
		<button type="submit" onclick="return validateForm()">SignIn</button>
		<div class="signup">
			<p>Don't have an account? <a href="signuppage.html">Sign Up</a></p>
		</div>
	</form>	
	<script>
		function validateForm() {
    var username = document.forms["loginForm"]["username"].value;
    var password = document.forms["loginForm"]["password"].value;
    if (username === "" || password === "") {
        alert("Please fill in all the required fields.");
        return false;
    } else if (username === "user1234" && password === "pass1234") {
        window.location.replace("reserve.html");
        return false;
    } else {
        alert("Invalid username or password.");
        return false;
    }
}
	</script>
</body>
</html>
