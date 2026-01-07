# Website
Stranger Things Tribute Website
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Stranger Things</title>

<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&display=swap" rel="stylesheet">

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Bebas Neue', cursive;
    height: 100vh;
    background: black;
    overflow: hidden;
}

/* COMMON FULLSCREEN */
.page {
    height: 100vh;
    width: 100%;
    display: none;
    justify-content: center;
    align-items: center;
    text-align: center;
}

/* HOME PAGE */
#home {
    display: flex;
    background:
        linear-gradient(to bottom, rgba(0,0,0,0.4), rgba(0,0,0,0.9)),
        url("poster.png");
    background-size: cover;
    background-position: center;
}

.title {
    font-size: 6rem;
    color: red;
    letter-spacing: 5px;
    text-shadow: 0 0 20px red;
}

.subtitle {
    margin-top: 20px;
    font-size: 1.5rem;
    color: white;
    letter-spacing: 3px;
}

.btn {
    margin-top: 40px;
    padding: 15px 40px;
    font-size: 1.2rem;
    background: transparent;
    border: 2px solid red;
    color: red;
    cursor: pointer;
    letter-spacing: 2px;
    transition: 0.3s;
}

.btn:hover {
    background: red;
    color: black;
    box-shadow: 0 0 20px red;
}

/* GOODBYE PAGE */
#goodbye {
    background: radial-gradient(circle, #12001a, #000);
    color: white;
    display: flex;
    flex-direction: column;
    animation: fadeIn 2s ease-in;
}

.goodbye-text {
    font-size: 5rem;
    color: red;
    margin-bottom: 30px;
    text-shadow: 0 0 30px red;
}

.quote {
    font-size: 1.5rem;
    max-width: 700px;
    line-height: 1.8;
    color: #ddd;
    letter-spacing: 2px;
}

/* Fade animation */
@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}
</style>
</head>

<body>

<!-- HOME PAGE -->
<div id="home" class="page">
    <div>
        <div class="title">STRANGER<br>THINGS</div>
        <div class="subtitle">WELCOME TO THE UPSIDE DOWN</div>
        <button class="btn" onclick="enterStrangerThings()">
            ENTER STRANGER THINGS
        </button>
    </div>
</div>

<!-- GOODBYE PAGE -->
<div id="goodbye" class="page">
    <div class="goodbye-text">GOODBYE</div>
    <div class="quote">
        “Friends don’t lie.<br><br>
        But sometimes… they disappear into the Upside Down.”
    </div>
</div>

<script>
function enterStrangerThings() {
    document.getElementById("home").style.display = "none";
    document.getElementById("goodbye").style.display = "flex";
}
</script>

</body>
</html>
