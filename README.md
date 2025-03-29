<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GitHub Pages Login</title>
    <style>
        body { font-family: Arial, sans-serif; background-color: #f4f4f4; padding: 20px; }
        .login-container { width: 300px; margin: auto; padding: 20px; background-color: white; border-radius: 5px; box-shadow: 0px 4px 8px rgba(0,0,0,0.2); }
        input { width: 100%; padding: 10px; margin-bottom: 10px; border: 1px solid #ccc; border-radius: 5px; }
        button { width: 100%; padding: 10px; background-color: #003366; color: white; border: none; border-radius: 5px; cursor: pointer; }
    </style>
</head>
<body>

    <div class="login-container">
        <h2>Login</h2>
        <input type="text" id="username" placeholder="Username" />
        <input type="password" id="password" placeholder="Password" />
        <button onclick="login()">Login</button>
    </div>

    <script>
        async function login() {
            var username = document.getElementById('username').value;
            var password = document.getElementById('password').value;

            // Simulate calling an external API for authentication (e.g., Firebase, custom API)
            // In this example, we're just mocking the login.
            if (username === 'JohnDoe' && password === 'password123') {
                // Simulate successful login: set secure cookies
                setSecureCookies(username);
                alert('Login successful!');
            } else {
                alert('Invalid login credentials');
            }
        }

        function setSecureCookies(username) {
            // Set a secure cookie with HttpOnly and SameSite attributes (client-side only)
            document.cookie = `username=${username}; Secure; HttpOnly; SameSite=Strict; path=/;`;

            // Example: Set session token cookie (in real-world, use JWT or OAuth tokens)
            var sessionToken = 'abcdef123456';
            document.cookie = `sessionToken=${sessionToken}; Secure; HttpOnly; SameSite=Strict; path=/;`;
        }
    </script>

</body>
</html>
