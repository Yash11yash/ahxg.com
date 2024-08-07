<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AHXG</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            color: #e0e0e0; /* Light text color */
            background-color: #121212; /* Dark background color */
        }

        header {
            background-color: #1f1f1f; /* Darker header background */
            color: #e0e0e0; /* Light text color */
            padding: 10px 0;
            text-align: center;
        }

        header h1 {
            margin: 0;
        }

        nav ul {
            list-style-type: none;
            padding: 0;
            margin: 0;
        }

        nav ul li {
            display: inline;
            margin: 0 10px;
        }

        nav ul li a {
            color: #e0e0e0; /* Light text color for links */
            text-decoration: none;
        }

        nav ul li a:hover {
            color: #b3b3b3; /* Slightly lighter color on hover */
        }

        main {
            padding: 20px;
        }

        section {
            margin-top: 20px;
            background-color: #1f1f1f; /* Dark background for sections */
            border-radius: 8px;
            padding: 20px;
        }

        .tweet-section,
        .image-upload-section {
            background-color: #2c2c2c; /* Slightly darker background for sections */
            border-radius: 8px;
            padding: 15px;
        }

        textarea {
            width: 100%;
            height: 100px;
            margin-bottom: 10px;
            background-color: #333; /* Dark background for textarea */
            color: #e0e0e0; /* Light text color */
            border: 1px solid #444;
            border-radius: 4px;
            padding: 10px;
        }

        button {
            background-color: #444; /* Dark button background */
            color: #e0e0e0; /* Light text color */
            border: none;
            padding: 10px 20px;
            cursor: pointer;
            border-radius: 4px;
            margin-top: 10px;
        }

        button:hover {
            background-color: #555; /* Slightly lighter button background on hover */
        }

        #uploadedImage {
            max-width: 100%;
            margin-top: 10px;
            border: 1px solid #444; /* Border for the uploaded image */
            border-radius: 4px;
        }

        footer {
            background-color: #1f1f1f; /* Dark footer background */
            color: #e0e0e0; /* Light text color */
            padding: 10px;
            text-align: center;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to AHXG</h1>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <section id="home">
            <h2>Home</h2>
            <p>Welcome to the AHXG website. We are glad to have you here.</p>
            <div class="tweet-section">
                <h3>Post a Tweet</h3>
                <textarea id="tweetInput" placeholder="What's happening?"></textarea>
                <button onclick="postTweet()">Tweet</button>
                <div id="tweetOutput"></div>
            </div>
        </section>
        <section id="about">
            <h2>About</h2>
            <p>Learn more about AHXG and what we do.</p>
        </section>
        <section id="contact">
            <h2>Contact</h2>
            <p>Get in touch with us via email or phone.</p>
            <div class="image-upload-section">
                <h3>Upload an Image</h3>
                <input type="file" id="imageUpload" accept="image/*">
                <img id="uploadedImage" src="" alt="" style="display:none;">
            </div>
        </section>
    </main>
    <footer>
        <p>&copy; 2024 AHXG. All rights reserved.</p>
    </footer>
    <script>
        function postTweet() {
            const tweetInput = document.getElementById('tweetInput');
            const tweetOutput = document.getElementById('tweetOutput');
            const tweetText = tweetInput.value;
            if (tweetText) {
                tweetOutput.innerHTML = `<p>${tweetText}</p>`;
                tweetInput.value = '';
            }
        }

        document.getElementById('imageUpload').addEventListener('change', function() {
            const file = this.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = function(e) {
                    const img = document.getElementById('uploadedImage');
                    img.src = e.target.result;
                    img.style.display = 'block';
                }
                reader.readAsDataURL(file);
            }
        });
    </script>
</body>
</html>
