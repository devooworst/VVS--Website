<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PGCC Website</title>
    <link rel="icon" type="image/png" href="pgcc_favicon.png">
    <style>
        body { font-family: 'Arial', sans-serif; background-color: white; color: #003366; text-align: center; margin: 0; }
        header { background-color: #003366; color: white; padding: 10px; position: fixed; width: 100%; top: 0; left: 0; display: flex; align-items: center; justify-content: space-between; z-index: 1000; }
        header img { height: 50px; margin-left: 15px; }
        nav ul { list-style-type: none; padding: 0; margin: 0; display: flex; }
        nav ul li { margin: 0 15px; }
        nav ul li a { color: white; text-decoration: none; font-weight: bold; padding: 10px; }
        nav ul li a:hover { background-color: rgba(255, 255, 255, 0.2); border-radius: 5px; }
        .container { padding-top: 80px; }
        .section { display: none; padding: 40px; animation: fadeIn 1s; }
        .section.active { display: block; }
        .image-section { width: 80%; max-width: 600px; margin: 20px auto; }
        .image-section img { width: 100%; border-radius: 10px; box-shadow: 0px 4px 8px rgba(0,0,0,0.2); }
        .audio-controls { margin-top: 20px; }
        .audio-controls input { width: 100px; }
        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
        .login-form { position: fixed; bottom: 10px; right: 10px; background-color: #003366; color: white; padding: 20px; border-radius: 10px; box-shadow: 0px 4px 8px rgba(0,0,0,0.2); }
        .login-form input { margin: 5px 0; padding: 10px; width: 200px; }
        .login-form button { padding: 10px 15px; background-color: #0066cc; border: none; color: white; cursor: pointer; }
        .login-form button:hover { background-color: #0055b3; }
    </style>
</head>
<body>
    <header>
        <img src="https://drive.google.com/uc?id=1gdAsvhgVSVM4nZq195LSu7x7gliX_edh" alt="PGCC Logo"> 
        <nav>
            <ul>
                <li><a href="#" onclick="showSection('intro')">Home</a></li>
                <li><a href="#" onclick="showSection('vss')">What is VSS?</a></li>
                <li><a href="#" onclick="showSection('impact')">Examples of Impact</a></li>
                <li><a href="#" onclick="showSection('help')">Help</a></li>
            </ul>
        </nav>
    </header>
    <div class="container">
        <section id="intro" class="section active">
            <h1>Welcome to PGCC</h1>
            <p>Our mission is to create a positive impact through strategic solutions.</p>
            <div class="image-section">
                <img src="https://drive.google.com/uc?id=1wh0pjG8jK5_7ZwXM6rH0_q6yqXIQ1XFS" alt="Welcome Image" loading="lazy">
            </div>
        </section>

        <section id="vss" class="section">
            <h1>What is VSS?</h1>
            <p>VSS (Value-Driven Strategic Solutions) is an innovative approach to solving complex challenges.</p>
            <div class="image-section">
                <img src="https://drive.google.com/uc?id=1TT78XHAY6pMupmkWUTV3D4WoVK7s31K9" alt="VSS Concept" loading="lazy">
            </div>
        </section>

        <section id="impact" class="section">
            <h1>Examples of Impact</h1>
            <p>Here are some ways VSS has changed organizations:</p>
            <div class="audio-controls">
                <button onclick="toggleAudio()">▶️ Play / ⏸️ Pause Narration</button>
                <input type="range" id="audioProgress" value="0" step="1" min="0">
                <audio id="impactAudio" ontimeupdate="updateProgress()">
                    <source src="https://drive.google.com/uc?id=1f4l_zgqQGc2-q1ZoHZX4tLnPsg1VpWO0" type="audio/m4a">
                    Your browser does not support the audio element.
                </audio>
            </div>
        </section>

        <section id="help" class="section">
            <h1>Help & Contact</h1>
            <p>Contact us at: <strong>support@pgcc.com</strong></p>
        </section>
    </div>

    <!-- Login Form -->
    <div class="login-form">
        <h2>Login</h2>
        <form onsubmit="setSecureCookie(event)">
            <input type="text" id="username" name="username" placeholder="Username" required>
            <input type="password" id="password" name="password" placeholder="Password" required>
            <button type="submit">Login</button>
        </form>
    </div>

    <script>
        document.cookie = "userPreferences=darkMode; Secure; HttpOnly; SameSite=Strict";
        
        function setSecureCookie(event) {
            event.preventDefault();
            var username = document.getElementById("username").value;
            var password = document.getElementById("password").value;
            
