<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Valentine Invitation</title>
<style>
    body {
        text-align: center;
        font-family: Arial, sans-serif;
        background-color: #ffe6f0;
        padding: 50px;
    }
    h1 {
        color: #d63384;
    }
    img {
        width: 250px;
        margin: 20px 0;
    }
    button {
        padding: 10px 20px;
        font-size: 18px;
        margin: 10px;
        cursor: pointer;
        border: none;
        border-radius: 8px;
    }
    #yesBtn {
        background-color: #28a745;
        color: white;
    }
    #noBtn {
        background-color: #dc3545;
        color: white;
        position: relative;
    }
</style>
</head>
<body>

<div id="main">
    <h1>Camille, will you be my Valentine?</h1>
    <img src="https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExbnBjYnUwMGFnb2x4dWt6OW9xODM0dGc5bncwd3FlbDlrMnNhYXE1eiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/9rgVLYnPzzUpLsaaxN/giphy.gif" alt="Begging GIF">
    <br>
    <button id="yesBtn" onclick="sayYes()">Yes</button>
    <button id="noBtn" onclick="sayNo()">No</button>
</div>

<script>
let noClickCount = 0;

function sayNo() {
    noClickCount++;

    if (noClickCount === 1) {
        document.querySelector("h1").innerText = "Are you sure?";
    }

    let yesBtn = document.getElementById("yesBtn");
    yesBtn.style.fontSize = (18 + noClickCount * 10) + "px";
    yesBtn.style.padding = (10 + noClickCount * 5) + "px " + (20 + noClickCount * 10) + "px";

    if (noClickCount > 5) {
        document.getElementById("noBtn").style.display = "none";
    }
}

function sayYes() {
    document.getElementById("main").innerHTML = `
        <h1>Yay!!</h1>
        <img src="https://media.giphy.com/media/26tOZ42Mg6pbTUPHW/giphy.gif" alt="Fireworks GIF">
    `;
}
</script>

</body>
</html>
