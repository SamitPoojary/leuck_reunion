<html lang="{{ site.lang | default: "en-US" }}">
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title>Sign Up For Your Account</title>
    <style>
        h1 {
          text-align: center;
          font-size: 40px;
          font-weight: 700;
          color: #0AAAF5;
          font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
        }
        input.login {
          font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
          margin-top: 5%;
          position: inline;
          width: 50%;
          margin-left: 25%;
          margin-right: 30%;
          padding: 2%;
          font-size: 25px;
          background-color: #0AAAF5;
          color: #0AAAF5;
          border: none;
          border-radius: 5px;
          border-bottom: 4px solid #0AAAF5;
          transition-duration: 0.3s;
        }
        input.login:focus {
          background-color: #4d4c4b;
          outline: none;
        }
        button {
          outline: none;
          -webkit-tap-highlight-color: transparent;
          font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
          font-size: 20px;
          margin-top: 4%; 
          margin-bottom: 4%;
          position: inline;
          width: 40%;
          margin-left: 30%;
          margin-right: 30%;
          padding: 2%;
          border-radius: 8px;
          background-color: #302f2f;
          color: #0AAAF5;
          border: none;
          transition-duration: 0.3s;
        }
        
        div.noacc {
          margin-top: 4%;
          margin-left: 25%;
          margin-right: 25%;
          position: inline;
          width: 50%;
        }
        #alracc {
          font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
          color: #0AAAF5;
          font-size: 25px;
          text-align: center;
          margin-bottom: 0%;          
        }
    </style>

  </head>
  <body>
    <h1 class="header">
      Sign Up For Your Account!
    </h1>
    <input type="username" class="login" id="user" placeholder="Username">
    <input type="name" class="login" id="name" placeholder="Full Name">
    <input type="password" class="login" id="pswd" placeholder="Password">
    <div>
    <br>
      <button id="enter" type="button" onclick="window.location.href='{{ site.baseurl }}/movie_review/search';">Create Account</button>
      <div class="noacc">
       <p id="alracc">Back to Login Page</p>
      </div>
      <button id="login" type="button" onclick="window.location.href='{{ site.baseurl }}/movie_review/login/login';">Log In</button>
    </div>
  </body>
  <script>
      // Get the input field
      var input = document.getElementById("pswd");
      // Execute a function when the user presses a key on the keyboard
      input.addEventListener("keypress", function(event) {
        // If the user presses the "Enter" key on the keyboard
        if (event.key === "Enter") {
          event.preventDefault();
          // Trigger the button element with a click
          document.getElementById("enter").click();
        }
      });
    </script>
</html>