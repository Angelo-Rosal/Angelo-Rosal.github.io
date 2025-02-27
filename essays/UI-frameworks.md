---
layout: essay
type: essay
title: "My Introduction to UI Frameworks"
date: 2025-02-26
published: true
---

Since the beginning of my interest in Computer Science, I've always had an interest in how websites are made. I found UI frameworks to be one of my most exciting topics as I loved how you can code and create a website using as much as your mind can think. In my first steps into learning about UI frameworks originally I was excited as this has always been an interest to me, but as I went forward I learned how hard Bootstrap 5 is. Ultimately this experience made me more motivated to learn UI frameworks as although the learning curve may be higher I do see the benefits of putting your time and effort into learning and mastering this skill.  

## Why Use a UI Framework?

Personally, I found it easier to use a UI Framework well coding specific things compared to writing plain HTML and CSS. UI frame works give you pre-coded components that can help developers create user interfaces for apps and websites. UI frame works also makes it easier for developers due to its presets. An example of a side-by-side comparison of a page built with and without Bootstrap is:

## Bootstrap Example:
<code>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bootstrap Page</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <style>
        .hero {
            height: 400px;
            background: url('https://placekitten.com/1200/400') center/cover no-repeat;
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
        }
    </style>
</head>
<body>

<!-- Navbar -->
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container">
        <a class="navbar-brand" href="#">My Site</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
            aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav ms-auto">
                <li class="nav-item"><a class="nav-link" href="#">Home</a></li>
                <li class="nav-item"><a class="nav-link" href="#">About</a></li>
                <li class="nav-item"><a class="nav-link" href="#">Contact</a></li>
            </ul>
        </div>
    </div>
</nav>

<!-- Hero Section -->
<div class="hero">
    <h1>Welcome to My Site</h1>
</div>

<!-- Content Section -->
<div class="container my-5">
    <h2>About Us</h2>
    <p>We are a passionate team building awesome things using Bootstrap!</p>
</div>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
</code>

## HTML & CSS Example:
<code>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Plain CSS Page</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: Arial, sans-serif;
        }
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background-color: #333;
            padding: 15px 20px;
        }
        .navbar a {
            color: white;
            text-decoration: none;
            padding: 8px 12px;
        }
        .navbar .nav-links {
            display: flex;
            gap: 15px;
        }
        .navbar a:hover {
            background-color: #555;
        }
        .hero {
            height: 400px;
            background: url('https://placekitten.com/1200/400') center/cover no-repeat;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
        }
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 50px auto;
        }
    </style>
</head>
<body>

<!-- Navbar -->
<nav class="navbar">
    <a href="#">My Site</a>
    <div class="nav-links">
        <a href="#">Home</a>
        <a href="#">About</a>
        <a href="#">Contact</a>
    </div>
</nav>

<!-- Hero Section -->
<div class="hero">
    <h1>Welcome to My Site</h1>
</div>

<!-- Content Section -->
<div class="container">
    <h2>About Us</h2>
    <p>We are a passionate team building awesome things using plain HTML & CSS!</p>
</div>

</body>
</html>
</code>

Yes
