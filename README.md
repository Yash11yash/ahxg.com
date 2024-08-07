<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple YouTube Layout</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
        }
        .header {
            background-color: #f8f8f8;
            padding: 10px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            border-bottom: 1px solid #e0e0e0;
        }
        .header .logo {
            font-size: 24px;
            font-weight: bold;
        }
        .header .search-bar {
            flex: 1;
            margin: 0 20px;
        }
        .header .search-bar input {
            width: 100%;
            padding: 8px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        .header .profile {
            font-size: 18px;
        }
        .sidebar {
            width: 240px;
            background-color: #f9f9f9;
            padding: 10px;
            position: fixed;
            top: 50px;
            bottom: 0;
            border-right: 1px solid #e0e0e0;
        }
        .sidebar .menu-item {
            margin: 10px 0;
            font-size: 18px;
        }
        .main-content {
            margin-left: 260px;
            padding: 20px;
        }
        .video {
            margin-bottom: 20px;
        }
        .video img {
            width: 100%;
            height: auto;
        }
        .video .title {
            font-size: 18px;
            margin-top: 5px;
        }
    </style>
</head>
<body>
    <div class="header">
        <div class="logo">YouTube</div>
        <div class="search-bar">
            <input type="text" placeholder="Search...">
        </div>
        <div class="profile">Profile</div>
    </div>
    <div class="sidebar">
        <div class="menu-item">Home</div>
        <div class="menu-item">Trending</div>
        <div class="menu-item">Subscriptions</div>
        <div class="menu-item">Library</div>
    </div>
    <div class="main-content">
        <div class="video">
            <img src="https://via.placeholder.com/800x450" alt="Video Thumbnail">
            <div class="title">Video Title 1</div>
        </div>
        <div class="video">
            <img src="https://via.placeholder.com/800x450" alt="Video Thumbnail">
            <div class="title">Video Title 2</div>
        </div>
        <!-- Add more video items here -->
    </div>
</body>
</html>
