<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tempora - Saving Teachers' Time</title>
    <style>
        /* Smooth scrolling for anchor links */
        html {
            scroll-behavior: smooth;
        }
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(135deg, #e0f7fa, #f3e5f5, #e0f2f1);
            color: #333;
        }
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 50px;
            background: rgba(255, 255, 255, 0.8);
            backdrop-filter: blur(10px);
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        header h1 {
            margin: 0;
            color: #5c6bc0;
        }
        nav ul {
            list-style: none;
            margin: 0;
            padding: 0;
            display: flex;
            gap: 20px;
        }
        nav a {
            text-decoration: none;
            color: #333;
            font-weight: bold;
            transition: color 0.2s;
        }
        nav a:hover {
            color: #5c6bc0;
        }
        .hero {
            text-align: center;
            padding: 80px 20px 60px;
        }
        .title-box {
            display: inline-block;
            border: 2px solid #333;
            padding: 10px 30px;
            border-radius: 10px;
            font-size: 3em;
            font-weight: bold;
            background-color: #fff;
        }
        .tagline {
            font-size: 1.5em;
            margin-top: 20px;
            color: #444;
        }
        
        /* AI Search Bar Styles */
        .ai-search-container {
            margin-top: 40px;
            display: flex;
            justify-content: center;
            padding: 0 20px;
        }
        .ai-search-box {
            display: flex;
            width: 100%;
            max-width: 700px;
            background: #fff;
            border-radius: 50px;
            padding: 8px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            border: 1px solid #e0e0e0;
        }
        .ai-search-input {
            flex-grow: 1;
            border: none;
            padding: 15px 25px;
            border-radius: 50px;
            font-size: 1.1em;
            outline: none;
            color: #333;
        }
        .ai-search-input::placeholder {
            color: #999;
        }
        .ai-generate-btn {
            background: linear-gradient(135deg, #5c6bc0, #3f51b5);
            color: #fff;
            border: none;
            padding: 15px 35px;
            border-radius: 40px;
            font-size: 1.05em;
            font-weight: bold;
            cursor: pointer;
            transition: transform 0.2s, box-shadow 0.2s;
        }
        .ai-generate-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(92, 107, 192, 0.4);
        }

        /* Carousel Styles */
        .carousel-container {
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 50px 0;
            background-color: rgba(255, 255, 255, 0.4);
        }
        .carousel {
            display: flex;
            overflow-x: auto;
            scroll-behavior: smooth;
            width: 80%;
            gap: 20px;
            padding: 20px;
        }
        .carousel::-webkit-scrollbar {
            height: 8px;
        }
        .carousel::-webkit-scrollbar-track {
            background: rgba(0,0,0,0.05);
            border-radius: 10px;
        }
        .carousel::-webkit-scrollbar-thumb {
            background: #5c6bc0;
            border-radius: 10px;
        }
        .textbook-card {
            flex: 0 0 calc(20% - 20px);
            background: #fff;
            border-radius: 15px;
            text-align: center;
            padding: 20px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            transition: transform 0.2s;
            cursor: pointer;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: flex-end; 
        }
        .textbook-card:hover {
            transform: scale(1.05);
        }
        .book-icon {
            width: 80px;
            height: 100px;
            background-color: #e0f2f1;
            margin: 0 auto 15px;
            display: flex;
            justify-content: center;
            align-items: center;
            border-radius: 5px;
            font-weight: bold;
            color: #00796b;
            font-size: 2em;
        }
        /* Style for the actual image cover */
        .custom-book-img {
            width: 80px;
            height: 115px; /* Set fixed height to match the icons */
            object-fit: cover; /* Ensures the image fills the space nicely */
            border-radius: 4px;
            margin: 0 auto 15px;
            box-shadow: 0 3px 6px rgba(0,0,0,0.15);
        }

        /* About Section */
        .about-section {
            padding: 80px 20px;
            text-align: center;
            background-color: #fff;
            margin: 60px auto;
            width: 70%;
            border-radius: 15px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.05);
            line-height: 1.8;
            color: #444;
        }
        .about-section h2 {
            color: #5c6bc0;
            font-size: 2.5em;
            margin-bottom: 20px;
        }
        .about-section p {
            font-size: 1.2em;
            max-width: 800px;
            margin: 0 auto;
        }
    </style>
</head>
<body>

<header>
    <h1>Tempora</h1>
    <nav>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">Resources</a></li>
            <li><a href="#about">About</a></li>
        </ul>
    </nav>
</header>

<section class="hero">
    <div class="title-box">Tempora</div>
    <p class="tagline">...saving teachers' time</p>
    
    <div class="ai-search-container">
        <div class="ai-search-box">
            <input type="text" class="ai-search-input" placeholder="E.g., Generate a 10-question history quiz based on Textbook 3 Unit 1...">
            <button class="ai-generate-btn">Generate ✨</button>
        </div>
    </div>
</section>

<section class="carousel-container">
    <div class="carousel">
        <div class="textbook-card">
            <img src="https://i.postimg.cc/2LQm0WZS/9780194504515v2.jpg" alt="Maturita Solutions" class="custom-book-img">
            <p>Maturita Solutions</p>
        </div>
        <div class="textbook-card">
            <div class="book-icon">📖</div>
            <p>Textbook 2</p>
        </div>
        <div class="textbook-card">
            <div class="book-icon">📖</div>
            <p>Textbook 3</p>
        </div>
        <div class="textbook-card">
            <div class="book-icon">📖</div>
            <p>Textbook 4</p>
        </div>
        <div class="textbook-card">
            <div class="book-icon">📖</div>
            <p>Textbook 5</p>
        </div>
        <div class="textbook-card">
            <div class="book-icon">📖</div>
            <p>Textbook 6</p>
        </div>
        <div class="textbook-card">
            <div class="book-icon">📖</div>
            <p>Textbook 7</p>
        </div>
        <div class="textbook-card">
            <div class="book-icon">📖</div>
            <p>Textbook 8</p>
        </div>
        <div class="textbook-card">
            <div class="book-icon">📖</div>
            <p>Textbook 9</p>
        </div>
        <div class="textbook-card">
            <div class="book-icon">📖</div>
            <p>Textbook 10</p>
        </div>
    </div>
</section>

<section id="about" class="about-section">
    <h2>Empowering Educators with AI</h2>
    <p>We know that teachers are often overconsumed with the endless hours required for class preparation. Between grading, planning, and administrative tasks, finding the right supplemental resources can be exhausting.</p>
    <br>
    <p><strong>Tempora</strong> is designed to change that. By leveraging an advanced AI model, our application instantly provides high-quality, perfectly tailored additional teaching materials for your specific textbooks. Reclaim your evenings and weekends.</p>
</section>

<br><br><br>

</body>
</html>
