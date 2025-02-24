<!DOCTYPE html><html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hello World Animation</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background: #fff;
            color: #333;
            font-family: 'Arial', sans-serif;
            overflow: hidden;
            margin: 0;
        }.container {
        font-size: 4em;
        font-weight: bold;
        position: relative;
        display: inline-block;
        overflow: hidden;
        border-radius: 20px;
        padding: 20px 40px;
        color: #fff;
        animation: changeColor 10s infinite alternate, pulse 1.5s infinite alternate;
    }

    @keyframes pulse {
        0% { transform: scale(1); }
        100% { transform: scale(1.1); }
    }

    @keyframes changeColor {
        0% { background: #ff416c; }
        20% { background: #ff4b2b; }
        40% { background: #ff8c00; }
        60% { background: #4caf50; }
        80% { background: #2196f3; }
        100% { background: #9c27b0; }
    }

    .hello {
        display: inline-block;
        animation: changeText 10s infinite alternate;
    }

    @keyframes changeText {
        0% { content: "Hello"; }
        20% { content: "Hola"; }
        40% { content: "नमस्ते"; }
        60% { content: "سلام"; }
        80% { content: "Bonjour"; }
        100% { content: "Ciao"; }
    }

    .hello::before {
        content: "Hello";
        animation: changeText 10s infinite alternate;
    }

    .world {
        display: inline-block;
        margin-left: 10px;
    }
</style>

</head>
<body>
    <div class="container">
        <span class="hello"></span>
        <span class="world">World!</span>
    </div>
</body>
</html>