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

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bootstrap vs Plain HTML & CSS Example</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        code {
            background-color: #f5f5f5;
            padding: 2px 4px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-family: "Courier New", monospace;
            font-size: 14px;
        }
        pre {
            background-color: #f5f5f5;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-family: "Courier New", monospace;
            font-size: 14px;
            overflow-x: auto;
        }
        .example {
            margin-bottom: 40px;
        }
    </style>
</head>
<body>

<h1>Bootstrap vs Plain HTML & CSS</h1>
<p>This page compares two ways to build the same webpage: one using <strong>Bootstrap 5</strong> and the other using <strong>plain HTML & CSS</strong>.</p>

<!-- Bootstrap Example -->
<div class="example">
    <h2>Example 1: Using Bootstrap 5</h2>
    <p>The following page uses Bootstrap’s prebuilt classes to create a responsive navbar and hero section.</p>
    <pre><code>
&lt;!DOCTYPE html&gt;
&lt;html lang="en"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;Bootstrap Example&lt;/title&gt;
    &lt;link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet"&gt;
&lt;/head&gt;
&lt;body&gt;

&lt;nav class="navbar navbar-expand-lg navbar-dark bg-dark"&gt;
    &lt;div class="container"&gt;
        &lt;a class="navbar-brand" href="#"&gt;MyBrand&lt;/a&gt;
        &lt;button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"&gt;
            &lt;span class="navbar-toggler-icon"&gt;&lt;/span&gt;
        &lt;/button&gt;
        &lt;div class="collapse navbar-collapse" id="navbarNav"&gt;
            &lt;ul class="navbar-nav ms-auto"&gt;
                &lt;li class="nav-item"&gt;&lt;a class="nav-link" href="#"&gt;Home&lt;/a&gt;&lt;/li&gt;
                &lt;li class="nav-item"&gt;&lt;a class="nav-link" href="#"&gt;About&lt;/a&gt;&lt;/li&gt;
            &lt;/ul&gt;
        &lt;/div&gt;
    &lt;/div&gt;
&lt;/nav&gt;

&lt;div class="container-fluid text-center text-white d-flex align-items-center justify-content-center" style="height: 400px; background: #444;"&gt;
    &lt;h1&gt;Welcome to My Site&lt;/h1&gt;
&lt;/div&gt;

&lt;script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"&gt;&lt;/script&gt;

&lt;/body&gt;
&lt;/html&gt;
    </code></pre>
</div>

<!-- Plain HTML & CSS Example -->
<div class="example">
    <h2>Example 2: Using Plain HTML & CSS</h2>
    <p>This version of the same page is built from scratch using only HTML and CSS. The styling, positioning, and responsiveness need to be manually handled.</p>
    <pre><code>
&lt;!DOCTYPE html&gt;
&lt;html lang="en"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;Plain HTML & CSS Example&lt;/title&gt;
    &lt;style&gt;
        body {
            margin: 0;
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
            padding: 10px;
        }
        .nav-links {
            display: flex;
            gap: 15px;
        }
        .hero {
            height: 400px;
            background-color: #444;
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;

&lt;nav class="navbar"&gt;
    &lt;a href="#" class="navbar-brand"&gt;MyBrand&lt;/a&gt;
    &lt;div class="nav-links"&gt;
        &lt;a href="#"&gt;Home&lt;/a&gt;
        &lt;a href="#"&gt;About&lt;/a&gt;
    &lt;/div&gt;
&lt;/nav&gt;

&lt;div class="hero"&gt;
    &lt;h1&gt;Welcome to My Site&lt;/h1&gt;
&lt;/div&gt;

&lt;/body&gt;
&lt;/html&gt;
    </code></pre>
</div>
</body>
</html>

## Key Differences:

<ul>
    <li> Bootstrap provides pre-designed components and responsive features out of the box </li>
    <li> Plain HTML & CSS requires more manual work for the layout, position, and styling </li>
    <li> Plain HTML & CSS requires custom media queries and more CSS rules for responsiveness </li>
    <li> With Bootstrap, you get prebuilt mobile-friendly navbar without additional work</li>
</ul>

Fried Chicken Test



