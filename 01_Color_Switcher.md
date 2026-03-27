
# Project 1   "Color-Switcher"

## HTML
```HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Color Switcher</title>
    <link rel="stylesheet" href="style.css ">
</head>
<body>
    <div class="color-changer-container">
        <h1>Color Switcher</h1>
        <div class="buttons-container">
            <div class="button" id="gray"></div>
            <div class="button" id="blue"></div>
            <div class="button" id="yellow"></div>
            <div class="button" id="white"></div>
            <div class="button" id="red"></div>
        </div>
        <h2>
            Try clicking on one of the colors above
            <span>to change the background color of this page!</span>
        </h2>
    </div>

    <script src="script.js"></script>
</body>
</html>
```


## CSS
```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, Helvetica, sans-serif;
}
body {
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
}
h1 {
    font-size: 50px;
    margin-top: -100px;
}
.buttons-container {
    display: flex;
    justify-content: center;
    margin: 50px 0;
}
span {
    display: block;
}
.button {
    height: 150px;
    width: 150px;
    border: 2px solid black;
    margin-right: 15px;
}
#gray {
    background: gray;
}
#blue {
    background: blue;
}
#yellow {
    background: yellow;
}
#white {
    background: white;
}
#red {
    background: red;
}
```


## JavaScript
```JavaScript
console.log("Vikash");
const body = document.querySelector('body');
let buttons = document.querySelectorAll('.button');

buttons.forEach((button) => {
    console.log(button);
    button.addEventListener('click', (e) => {
        console.log(e);
        console.log(e.target);
        console.log(e.target.id);
        console.log(e.target.className);

        body.style.background = e.target.id;
    })
})
```