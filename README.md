<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Vox spam</title>

<style>
    body {
        margin: 0;
        font-family: "Georgia", serif;
        background-color: #f4f4f4;
        overflow-x: hidden;
    }

    header {
        background: #2c2c2c;
        color: white;
        text-align: center;
        padding: 30px 10px;
        animation: fadeDown 1s ease;
    }

    nav {
        background: #444;
        text-align: center;
        padding: 12px;
        animation: fadeDown 1.2s ease;
    }

    nav a {
        color: white;
        margin: 0 15px;
        text-decoration: none;
        font-weight: bold;
        position: relative;
    }

    nav a::after {
        content: "";
        position: absolute;
        width: 0;
        height: 2px;
        background: white;
        left: 0;
        bottom: -4px;
        transition: 0.3s;
    }

    nav a:hover::after {
        width: 100%;
    }

    .container {
        padding: 40px;
        text-align: center;
    }

    .content {
        background: white;
        padding: 30px;
        border: 1px solid #ccc;
        display: inline-block;
        max-width: 700px;
        animation: fadeUp 1.5s ease;
        box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    }

    button {
        margin-top: 20px;
        padding: 10px 20px;
        border: none;
        background: #333;
        color: white;
        cursor: pointer;
        transition: 0.3s;
    }

    button:hover {
        background: #555;
        transform: scale(1.05);
    }

    footer {
        margin-top: 40px;
        background: #2c2c2c;
        color: white;
        text-align: center;
        padding: 15px;
        animation: fadeUp 2s ease;
    }

    /* Animations */
    @keyframes fadeDown {
        from {
            opacity: 0;
            transform: translateY(-40px);
        }
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }

    @keyframes fadeUp {
        from {
            opacity: 0;
            transform: translateY(40px);
        }
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }

    .hidden {
        opacity: 0;
        transform: translateY(30px);
        transition: 0.6s;
    }

    .show {
        opacity: 1;
        transform: translateY(0);
    }

</style>
</head>

<body>

<header>
    <h1>VOX SPAM</h1>
    <p>Dream with Lucifer</p>
</header>

<nav>
    <a href="">Home</a>
    <a href="">About</a>
    <a href="">Services</a>
    <a href="077 8675197">Contact</a>
</nav>

<div class="container">
    <div class="content hidden" id="box">
        <h1 font-size ="10px">Warning...</h2>
        <p>
            Those who access this website should be careful
        </p>

       <button onclick="reveal()"> Click Me </button>
    </div>
</div>

<footer>
    <p>&copy; Vox spam web page</p>
</footer>

<script>
    // Reveal on load
    window.onload = () => {
        document.getElementById("box").classList.add("show");
    };

    // Button animation trigger
    function reveal() {
        const box = document.getElementById("box");
        box.style.transform = "scale(1.05)";
        setTimeout(() => {
            box.style.transform = "scale(1)";
        }, 200);
    }
</script>

</body>
</html>
