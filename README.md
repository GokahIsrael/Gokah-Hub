<!Doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title> Gokah Hub</title>

    <style>
        body {
            font-family: Arial, sans-serif;
            background: #f2f2f2;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        .signup-container {
            background: #fff;
            padding: 25px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
            width: 350px;
        }

        .signup-container h2 {
            text-align: center;
            margin-bottom: 20px;
        }

        .signup-container input {
            width: 100%;
            padding: 10px;
            margin: 8px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
            font-size: 15px;
        }

        .signup-container button {
            width: 100%;
            padding: 10px;
            background: #007bff;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
            margin-top: 10px;
        }

        .signup-container button:hover {
            background: #0056b3;
        }

        .message {
            text-align: center;
            margin-top: 15px;
            font-size: 14px;
            color: green;
            display: none;
        }

        .home-btn {
            background: #28a745;
            margin-top: 10px;
            display: none; /* hide until form is completed */
        }

        .home-btn:hover {
            background: #1e7d34;
        }
    </style>
</head>

<body>

    <div class="signup-container">
        <h2>Sign Up</h2>

        <input type="text" id="name" placeholder="Full Name">
        <input type="email" id="email" placeholder="Email Address">
        <input type="password" id="password" placeholder="Password">

        <button onclick="submitForm()">Create Account</button>

        <p class="message" id="successMsg">Account created successfully!</p>

        <button class="home-btn" id="homeBtn" onclick="goHome()">Go to Home Page</button>
    </div>

    <script>
        function submitForm() {
            let name = document.getElementById("name").value.trim();
            let email = document.getElementById("email").value.trim();
            let password = document.getElementById("password").value.trim();
            let message = document.getElementById("successMsg");
            let homeBtn = document.getElementById("homeBtn");

            if (name === "" || email === "" || password === "") {
                alert("Please fill in all fields!");
                return;
            }

            message.style.display = "block";
            homeBtn.style.display = "block";

            // Reset fields
            document.getElementById("name").value = "";
            document.getElementById("email").value = "";
            document.getElementById("password").value = "";
        }

        function goHome() {
            // Change "home.html" to your actual homepage URL
            window.location.href = "home.html";
        }
    </script>

</body>
</html>
