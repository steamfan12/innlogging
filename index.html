<?php
// Database connection details
$host = 'localhost'; // Database host
$dbname = 'google_scam'; // Database name
$db_user = 'root'; // Database username
$db_pass = 'Passord'; // Database password

// Create a connection
$conn = new mysqli($host, $db_user, $db_pass, $dbname);

// Check connection
if ($conn->connect_error) {
    die("Connection failed: " . $conn->connect_error);
}

$login_message = "";

// Check if account was created successfully
if (isset($_GET['account_created']) && $_GET['account_created'] == 1) {
    $login_message = "Account created successfully! Please log in.";
}

// Check if form is submitted
if ($_SERVER['REQUEST_METHOD'] === 'POST') {
    $brukernavn = $_POST['brukernavn'] ?? '';
    $passord = $_POST['passord'] ?? '';

    // Validate username and password length
    if (strlen($brukernavn) < 3 || strlen($passord) < 6) {
        $login_message = "Username must be at least 3 characters and password at least 6 characters.";
    } else {
        // Prevent SQL injection
        $brukernavn = $conn->real_escape_string($brukernavn);

        // Query to fetch the hashed password for the given username
        $sql = "SELECT passord FROM user WHERE brukernavn = '$brukernavn'";
        $result = $conn->query($sql);

        if ($result->num_rows > 0) {
            $row = $result->fetch_assoc();
            $hashed_passord = $row['passord'];

            // Verify the password
            if (password_verify($passord, $hashed_passord)) {
                // Login successful
                session_start();
                $_SESSION['brukernavn'] = $brukernavn; // Store username in session
                header("Location: welcome.php"); // Redirect to welcome page
                exit();
            } else {
                // Invalid password
                $login_message = "Invalid username or password.";
            }
        } else {
            // Username not found
            $login_message = "Invalid username or password.";
        }
    }
}

// Close the connection
$conn->close();
?>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sign in - Google Accounts</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Roboto', sans-serif;
        }

        body {
            display: flex;
            flex-direction: column;
            min-height: 100vh;
            background: #f0f4f9;
        }

        nav {
            padding: 24px;
            display: flex;
            justify-content: flex-end;
        }

        .nav-links a {
            color: #444;
            text-decoration: none;
            font-size: 13px;
            margin-left: 24px;
        }

        main {
            position: relative;
            flex: 1;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding-top: 48px;
            min-width: 600px;
            margin: 0 auto;
        }

        .container {
            position: relative; /* Make the container the reference point for absolute positioning */
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            width: 1000px;
            border-radius: 25px;
            padding: 60px 50px;
            background: #ffffff;
        }

        .left-content {
            flex: 1;
            margin-right: 40px;
            display: flex;
            flex-direction: column;
            align-items: flex-start;
        }

        .logo {
            margin-bottom: 16px;
            height: 40px;
            position: relative;
            top: -10px;
            left: -10px;
        }

        .right-content {
            flex: 2;
            display: flex;
            flex-direction: column;
            align-items: flex-start;
            margin-top: auto;
        }

        h1 {
            font-size: 32px;
            font-weight: 400;
            margin-bottom: 8px;
        }

        .subtitle {
            font-size: 16px;
            font-weight: 400;
            margin-bottom: 32px;
            color: #202124;
        }

        .form-group {
            width: 100%;
            margin-bottom: 16px;
        }

        input {
            width: 100%; /* Ensure the input stretches to fill the container */
            max-width: 600px; /* Set a maximum width for larger screens */
            min-width: 500px; /* Set a minimum width to ensure the input is long enough */
            height: 54px;
            border: 1px solid #dadce0;
            border-radius: 4px;
            padding: 13px 15px;
            font-size: 16px;
            color: #202124;
        }

        input:focus {
            border: 2px solid #1a73e8;
            outline: none;
        }

        .forgot-email {
            margin-bottom: 16px;
            color: #1a73e8;
            text-decoration: none;
            font-weight: 500;
            font-size: 14px;
        }

        .forgot-email:hover {
            background: #f6fafe;
        }

        .info-text {
            color: #5f6368;
            font-size: 14px;
            margin: 32px 0;
            max-width: 90%;
            line-height: 1.5;
        }

        .learn-more {
            color: #1a73e8;
            text-decoration: none;
            font-weight: 500;
        }

        .learn-more:hover {
            text-decoration: underline;
        }

        .button-group {
            display: flex;
            justify-content: flex-end; /* Align items to the right */
            align-items: center;
            position: absolute; /* Position the button group relative to the container */
            bottom: 20px; /* Distance from the bottom of the white box */
            right: 120px; /* Adjust this value to move the buttons slightly more to the left */
            gap: 16px; /* Add spacing between the link and button */
        }

        .create-account {
            color: #1a73e8;
            text-decoration: none;
            font-weight: 500;
            font-size: 14px;
        }

        button {
            background: #1a73e8;
            color: white;
            border: none;
            padding: 9px 24px;
            border-radius: 4px;
            font-size: 14px;
            font-weight: 500;
            cursor: pointer;
        }

        button:hover {
            background: #1557b0;
            box-shadow: 0 1px 2px rgba(0, 0, 0, 0.3);
        }

        footer {
            background: #f0f4f9;
            padding: 24px;
            display: flex;
            justify-content: space-between;
            color: #757575;
            font-size: 12px;
        }

        .footer-left select {
            border: none;
            background: #f0f4f9;
            color: #757575;
            font-size: 12px;
            padding: 4px;
            outline: none;
        }

        .footer-right a {
            color: #757575;
            text-decoration: none;
            margin-left: 24px;
        }

        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <main>
        <div class="container">
            <div class="left-content">
                <img src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ffreelogopng.com%2Fimages%2Fall_img%2F1657952440google-logo-png-transparent.png&f=1&nofb=1&ipt=b7259c6000b6b3a495e309cab647f337fea78c881fe2c53d600689dd94f06846&ipo=images" 
                     alt="Google" class="logo">
                <h1>Sign in</h1>
                <p class="subtitle">Use your Google Account</p>
            </div>
            <div class="right-content">
                <?php if (!empty($login_message)): ?>
                    <p style="color: red;"><?php echo $login_message; ?></p>
                <?php endif; ?>
                <form id="login-form" action="" method="POST">
                    <div class="form-group">
                        <input type="text" id="brukernavn" name="brukernavn" placeholder="Email or phone" required>
                    </div>
                    <div class="form-group hidden" id="password-group">
                        <input type="password" id="passord" name="passord" placeholder="Password" required>
                    </div>
                    <div class="button-group">
                        <a href="create_account.php" class="create-account">Create account</a>
                        <button type="button" id="next-button" style="border-radius: 20px;">Next</button>
                    </div>
                </form>
                <a href="#" class="forgot-email">Forgot email?</a>
                <p class="info-text">Not your computer? Use Guest mode to sign in privately. <a href="#" class="learn-more">Learn more about using Guest mode</a></p>
            </div>
        </div>
    </main>

    <footer>
        <div class="footer-left">
            <select>
                <option>English (United States)</option>
            </select>
        </div>
        
        <div class="footer-right">
            <a href="#">Help</a>
            <a href="#">Privacy</a>
            <a href="#">Terms</a>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const nextButton = document.getElementById('next-button');
            const loginButton = document.getElementById('login-button');
            const passwordGroup = document.getElementById('password-group');

            nextButton.addEventListener('click', () => {
                // Show the password field and login button
                passwordGroup.classList.remove('hidden');
                loginButton.classList.remove('hidden');
                nextButton.classList.add('hidden');
            });
        });
    </script>
</body>
</html>
