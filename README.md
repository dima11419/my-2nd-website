<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Interactive Website</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f5f5f5;
        }
        
        .header {
            text-align: center;
            padding: 40px 0;
            background-color: #ffffff;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
            margin-bottom: 20px;
        }

        .content {
            background-color: #ffffff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }

        .theme-toggle {
            background-color: #007bff;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 4px;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .theme-toggle:hover {
            background-color: #0056b3;
        }

        .dark-theme {
            background-color: #333;
            color: #fff;
        }

        .dark-theme .header,
        .dark-theme .content {
            background-color: #444;
            color: #fff;
        }

        .counter {
            text-align: center;
            margin: 20px 0;
        }

        .counter button {
            background-color: #28a745;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 4px;
            cursor: pointer;
            margin: 0 10px;
        }

        .counter button:hover {
            background-color: #218838;
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>Goodbye to My Interactive Website</h1>
        <button class="theme-toggle" onclick="toggleTheme()">Toggle Dark Mode</button>
    </div>

    <div class="content">
        <h2>About</h2>
        <p>This is a simple interactive website that demonstrates basic HTML, CSS, and JavaScript functionality. Try out the different features below!</p>

        <div class="counter">
            <h3>Counter: <span id="count">0</span></h3>
            <button onclick="updateCounter(1)">Increment</button>
            <button onclick="updateCounter(-1)">Decrement</button>
        </div>

        <h2>Current Time</h2>
        <p id="current-time"></p>
    </div>

    <script>
        // Theme toggling
        function toggleTheme() {
            document.body.classList.toggle('dark-theme');
        }

        // Counter functionality
        let count = 0;
        function updateCounter(value) {
            count += value;
            document.getElementById('count').textContent = count;
        }

        // Update time
        function updateTime() {
            const now = new Date();
            document.getElementById('current-time').textContent = now.toLocaleString();
        }

        // Update time every second
        setInterval(updateTime, 1000);
        updateTime(); // Initial call
    </script>
</body>
</html>
