---
layout: essay
type: essay
title: "My Introduction to UI Frameworks"
date: 2025-02-26
published: true
---

Since the beginning of my interest in Computer Science, I've always had an interest in how websites are made. I found UI frameworks to be one of my most exciting topics as I loved how you can code and create a website using as much as your mind can think. In my first steps into learning about UI frameworks originally I was excited as this has always been an interest to me, but as I went forward I learned how hard Bootstrap 5 is. Ultimately this experience made me more motivated to learn UI frameworks as although the learning curve may be higher I do see the benefits of putting your time and effort into learning and mastering this skill.  

## Why Use a UI Framework?

Personally, I found it easier to use a UI framework while coding specific things compared to writing plain HTML and CSS. UI frameworks give you pre-coded components that can help developers create user interfaces for apps and websites. UI frameworks also make it easier for developers due to its presets. Below, I’ve included a side-by-side comparison of a page built with and without Bootstrap:

---

## Side-by-Side Comparison: Bootstrap vs Plain HTML & CSS

---
layout: essay
type: essay
title: "My Introduction to UI Frameworks"
date: 2025-02-26
published: true
---

Since the beginning of my interest in Computer Science, I've always had an interest in how websites are made. I found UI frameworks to be one of my most exciting topics as I loved how you can code and create a website using as much as your mind can think. In my first steps into learning about UI frameworks, I was excited as this has always been an interest to me, but as I went forward, I learned how hard Bootstrap 5 is. Ultimately, this experience made me more motivated to learn UI frameworks as although the learning curve may be higher, I do see the benefits of putting your time and effort into learning and mastering this skill.  

## Why Use a UI Framework?

Personally, I found it easier to use a UI framework while coding specific things compared to writing plain HTML and CSS. UI frameworks give you pre-coded components that can help developers create user interfaces for apps and websites. UI frameworks also make it easier for developers due to its presets. Below, I’ve included a vertical comparison of a page built with and without Bootstrap:

---

## Example 1: Using Bootstrap 5

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bootstrap Example</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container">
        <a class="navbar-brand" href="#">MyBrand</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav ms-auto">
                <li class="nav-item"><a class="nav-link" href="#">Home</a></li>
                <li class="nav-item"><a class="nav-link" href="#">About</a></li>
            </ul>
        </div>
    </div>
</nav>

<div class="container-fluid text-center text-white d-flex align-items-center justify-content-center" style="height: 400px; background: #444;">
    <h1>Welcome to My Site</h1>
</div>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>

</body>
</html>

