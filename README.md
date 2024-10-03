<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Neon HTML Course & AI Coding</title>
    <style>
        /* Reset styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        /* Body neon background */
        body {
            font-family: 'Arial', sans-serif;
            background-color: #000;
            background: radial-gradient(circle, rgba(0, 0, 0, 1) 0%, rgba(0, 0, 0, 1) 50%, rgba(0, 255, 255, 0.1) 100%);
            color: #fff;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: flex-start;
            height: 100vh;
            padding-top: 60px;
        }

        /* Responsive container for course and AI content */
        .container, .ai-coding-section {
            text-align: center;
            display: none;
            width: 90%;
            max-width: 600px;
            margin-top: 20px;
        }

        /* Menu Bar */
        .menu-bar {
            position: fixed;
            top: 0;
            width: 100%;
            background-color: rgba(0, 255, 255, 0.2);
            padding: 10px;
            display: flex;
            justify-content: space-around;
            align-items: center;
            box-shadow: 0 0 10px #00ffff;
            z-index: 100;
        }

        .menu-bar a {
            color: #00ffff;
            text-decoration: none;
            font-size: 1.2rem;
            font-weight: bold;
            text-shadow: 0 0 10px #00ffff;
        }

        /* Start Button with Neon effect */
        .start-btn {
            font-size: 2.5rem;
            padding: 15px 30px;
            border: 3px solid #00ff00;
            border-radius: 15px;
            background-color: transparent;
            color: #00ff00;
            text-shadow: 0 0 10px #00ff00, 0 0 20px #00ff00, 0 0 30px #00ff00;
            cursor: pointer;
            transition: 0.3s;
        }

        .start-btn:hover {
            background-color: #00ff00;
            color: #000;
            text-shadow: none;
        }

        /* Course Content */
        .course-content {
            margin-top: 20px;
            padding: 20px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            font-size: 1.2rem;
            text-align: left;
            line-height: 1.6;
            box-shadow: 0 0 20px #00ffff, 0 0 40px #00ffff;
        }

        /* Copy Button */
        .copy-btn {
            margin-top: 15px;
            padding: 10px 20px;
            border: none;
            background-color: #ff0000;
            color: #fff;
            border-radius: 10px;
            cursor: pointer;
        }

        .copy-btn:hover {
            background-color: #ff3333;
        }

        /* AI Coding Section */
        .ai-coding-section {
            padding: 20px;
            background: rgba(255, 0, 255, 0.1);
            border-radius: 15px;
            box-shadow: 0 0 20px #ff00ff, 0 0 40px #ff00ff;
        }

        .ai-coding-section h3 {
            font-size: 2rem;
            text-shadow: 0 0 10px #ff00ff, 0 0 20px #ff00ff;
            margin-bottom: 20px;
        }

        .ai-coding-section p {
            font-size: 1.1rem;
            line-height: 1.6;
        }

        /* Neon Pulse Effect */
        body::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle, rgba(0,255,255,0.2) 20%, transparent 80%);
            animation: neonPulse 5s infinite alternate;
            z-index: -1;
        }

        @keyframes neonPulse {
            from {
                opacity: 0.4;
            }
            to {
                opacity: 0.9;
            }
        }

        /* Hidden Text Area for Copy */
        #code-text {
            position: absolute;
            left: -9999px;
        }

        /* Media Queries for Mobile Responsiveness */
        @media (max-width: 600px) {
            body {
                padding-top: 70px;
            }

            .menu-bar a {
                font-size: 1rem;
            }

            .start-btn {
                font-size: 1.5rem;
                padding: 10px 20px;
            }

            .course-content, .ai-coding-section {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>

    <!-- Menu Bar -->
    <div class="menu-bar">
        <a href="#start-course">Start Course</a>
        <a href="#ai-coding">Go to AI Coding</a>
    </div>

    <!-- Start Button -->
    <button class="start-btn" id="start-btn">Start Course</button>

    <!-- Course Content Section -->
    <div class="container" id="course-container">
        <h2>Advanced HTML Tags Course</h2>
        <div class="course-content">
            <pre><code>
&lt;!-- Example of Advanced HTML Tags --&gt;
&lt;section&gt;
    &lt;article&gt;
        &lt;h1&gt;HTML5 Advanced Features&lt;/h1&gt;
        &lt;p&gt;Learn about semantic tags in HTML5 like &lt;header&gt;, &lt;footer&gt;, &lt;nav&gt;, and &lt;article&gt;.&lt;/p&gt;
        &lt;footer&gt;This is the footer of the article.&lt;/footer&gt;
    &lt;/article&gt;

    &lt;aside&gt;
        &lt;p&gt;This is an aside element, often used for sidebars.&lt;/p&gt;
    &lt;/aside&gt;
&lt;/section&gt;
            </code></pre>
        </div>
        <!-- Copy Button -->
        <button class="copy-btn" id="copy-btn">Copy Code</button>
    </div>

    <!-- AI Coding Section -->
    <div class="container ai-coding-section" id="ai-coding">
        <h3>Coding AI Simulation</h3>
        <p>
            <strong>AI:</strong> "Can you provide me a piece of HTML code that works for creating a simple form with a text input and a submit button?"
        </p>
        <pre><code>
&lt;form&gt;
    &lt;label for="name"&gt;Enter your name:&lt;/label&gt;
    &lt;input type="text" id="name" name="name" placeholder="Your name"&gt;
    &lt;button type="submit"&gt;Submit&lt;/button&gt;
&lt;/form&gt;
        </code></pre>
    </div>

    <!-- Hidden Text Area for Copy -->
    <textarea id="code-text">
<!-- Example of Advanced HTML Tags -->
<section>
    <article>
        <h1>HTML5 Advanced Features</h1>
        <p>Learn about semantic tags in HTML5 like <header>, <footer>, <nav>, and <article>.</p>
        <footer>This is the footer of the article.</footer>
    </article>

    <aside>
        <p>This is an aside element, often used for sidebars.</p>
    </aside>
</section>
    </textarea>

    <script>
        // Show course content when 'Start' is clicked
        document.getElementById('start-btn').addEventListener('click', function() {
            document.getElementById('course-container').style.display = 'block';
        });

        // Copy the code when 'Copy Code' is clicked
        document.getElementById('copy-btn').addEventListener('click', function() {
            const codeText = document.getElementById('code-text');
            codeText.select();
            document.execCommand('copy');
            alert('Code copied to clipboard!');
        });
    </script>

</body>
</html>
