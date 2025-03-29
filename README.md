<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PGCC Website</title>
    <link rel="icon" type="image/png" href="pgcc_favicon.png"> <!-- Tab Icon -->
    <style>
        body { font-family: 'Arial', sans-serif; background-color: white; color: #003366; text-align: center; }
        header { background-color: #003366; color: white; padding: 10px; position: fixed; width: 100%; top: 0; left: 0; display: flex; align-items: center; justify-content: center; }
        header img { height: 50px; margin-right: 15px; }
        nav ul { list-style-type: none; padding: 0; }
        nav ul li { display: inline; margin: 0 15px; }
        nav ul li a { color: white; text-decoration: none; font-weight: bold; }
        .container { padding-top: 80px; }
        .section { display: none; padding: 40px; animation: fadeIn 1s; }
        .section.active { display: block; }
        .image-section { width: 80%; max-width: 600px; margin: 20px auto; }
        .image-section img { width: 100%; border-radius: 10px; box-shadow: 0px 4px 8px rgba(0,0,0,0.2); }
        .audio-controls { margin-top: 20px; }
        .security-section { padding: 20px; background-color: #f8d7da; color: #721c24; border-radius: 5px; margin: 20px auto; max-width: 80%; }
        .security-section h2 { font-size: 1.5em; }
        .security-section p { font-size: 1.1em; }
        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
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
                <li><a href="#" onclick="showSection('security')">Security</a></li>
            </ul>
        </nav>
    </header>
    <div class="container">
        <section id="intro" class="section active">
            <h1>Welcome to PGCC</h1>
            <p>Our mission is to create a positive impact through strategic solutions.</p>
            <div class="image-section">
                <img src="https://drive.google.com/uc?id=1wh0pjG8jK5_7ZwXM6rH0_q6yqXIQ1XFS" alt="Welcome Image">
            </div>
        </section>

        <section id="security" class="section">
            <h1>Security Measures</h1>
            <div class="security-section">
                <h2>Data Protection and Security</h2>
                <p>We are committed to ensuring the security and privacy of all users.</p>
            </div>
        </section>
    </div>

    <script>
        function setSecureCookie(name, value) {
            document.cookie = `${name}=${value}; Secure; HttpOnly; SameSite=Strict; Path=/;`;
        }

        setSecureCookie('userSession', 'fakeSecureToken12345');
        setSecureCookie('preferences', 'darkMode=true');

        function showSection(sectionId) {
            var sections = document.querySelectorAll('.section');
            sections.forEach(section => section.classList.remove('active'));
            document.getElementById(sectionId).classList.add('active');
        }
    </script>
</body>
</html>
