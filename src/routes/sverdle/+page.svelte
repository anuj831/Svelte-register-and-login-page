<svelte:head>
	<title>Login Page</title>
	<meta name="description" content="About this app" />
</svelte:head>
<div class="text-column">
	   
    <div class=“container”>
    <h1>Please Login Here</h1>
  
    <div class="container">
		<h2>Login</h2>
		<hr style="color:black;">
		<form action="#">
		  <div class="input-group">
			
			<input type="text" id="loginUsername" name="username" placeholder="User Name">
		  </div>
		  <div class="input-group">
			
			<input type="password" id="loginPassword" name="password" placeholder="Password">
		  </div>
      <p style="color:black;">Forgot password?</p>
		  <div class="input-group">
         <input type="submit" value="Login" on:click="{login}">
       
		  </div>
		</form>
		<p class="message">Not a Member! <span style="color:#1e8dc0;"> SignUp <span/></p> 
	  </div>
  
	</div>
</div>
<style>
	 .container {
      width: 300px;
      margin: 0 auto;
      margin-top: 100px;
      padding: 20px;
      background-color: #fff;
      border-radius: 5px;
      box-shadow: 0px 2px 10px rgba(0, 0, 0, 0.3);

    }

    h2 {
      text-align: center;
	  color:black;
	  font-weight: bold;
	  font-size:22px;
    }

    .input-group {
      margin-bottom: 20px;
	 
	  
    }

    

    .input-group input[type="text"],
    .input-group input[type="password"] {
      width: 100%;
      padding: 7px;
      font-size: 16px;
      border-radius: 3px;
	  border-bottom:1px solid;
      
    }

    .input-group input[type="submit"] {
      width: 100%;
      padding: 7px;
      font-size: 16px;
      border-radius: 10px;
      border: none;
      background-color: #1e8dc0;
      color: #150101;
      cursor: pointer;
    }

  

    .message {
      color: rgb(11, 11, 12);
      text-align: center;
      margin-bottom: 20px;
    }
</style>
<script>
 
  function register() {
    var username = document.getElementById("regUsername").value;
    var password = document.getElementById("regPassword").value;
    
   
    if (localStorage.getItem(username)) {
      alert("Username already exists. Please choose a different username.");
      return;
    }
    
    
    localStorage.setItem(username, password);
    alert("Registration successful. Please log in.");
  }
  
  
  function login() {
    var username = document.getElementById("loginUsername").value;
    var password = document.getElementById("loginPassword").value;
    
    
    if (localStorage.getItem(username)) {
     
      if (localStorage.getItem(username) === password) {
        alert("Login successful. Welcome, " + username + "!");
        window.location.href = "/";
      } else {
        alert("Incorrect password. Please try again.");
      }
    } else {
      alert("Username not found. Please register first.");
    }
  }
</script>