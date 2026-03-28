# Project 3   "Analog Clock"

## HTML
```HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Analog-Clock</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="clock-container">
        <div style="--clr:#ff4d58; --h:70px; --w:10px" id="hour" class="hand"><i></i></div>
        <div style="--clr:#00a6ff; --h:100px; --w:7px" id="minute" class="hand"><i></i></div>
        <div style="--clr:#ffffff; --h:140px; --w:4px" id="second" class="hand"><i></i></div>

        <span style="--v:1"><b>1</b></span>
        <span style="--v:2"><b>2</b></span>
        <span style="--v:3"><b>3</b></span>
        <span style="--v:4"><b>4</b></span>
        <span style="--v:5"><b>5</b></span>
        <span style="--v:6"><b>6</b></span>
        <span style="--v:7"><b>7</b></span>
        <span style="--v:8"><b>8</b></span>
        <span style="--v:9"><b>9</b></span>
        <span style="--v:10"><b>10</b></span>
        <span style="--v:12"><b>12</b></span>
        <span style="--v:11"><b>11</b></span>
    </div>

    <script src="script.js"></script>
</body>
</html>
```


## CSS
```CSS
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, Helvetica, sans-serif;
}
body {
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    background: #212121;
    color: #fff;
}
.clock-container {
    position: relative;
    height: 400px;
    width: 400px;
    background: #000;
    border: 10px solid #02ddff;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
}
.clock-container span {
    position: absolute;
    transform: rotate(calc(30deg * var(--v)));
    inset: 13px;
    text-align: center;
}
.clock-container span b {
    display: inline-block;
    font-size: 30px;
    transform: rotate(calc(-30deg * var(--v)));
}
.clock-container::before {
    position: absolute;
    content: '';
    height: 20px;
    width: 20px;
    background: #fff;
    border-radius: 50%;
    z-index: 10;
}
.clock-container .hand {
    display: flex;
    align-items: flex-end;
    justify-content: center;
}
.clock-container .hand i {
    position: absolute;
    height: var(--h);
    width: var(--w);
    background: var(--clr);
    border-radius: 20%;
}
```


## JavaScript
```JavaScript
console.log("Vikash")
let hour = document.querySelector('#hour');
let minute = document.querySelector('#minute');
let second = document.querySelector('#second');

function showTime() {
    let time = new Date();
    console.log(time)
    let h = time.getHours();
    let m = time.getMinutes();
    let s = time.getSeconds();
    
    hour.style.transform = `rotate(${(h*30) + (m/2)}deg)`;
    minute.style.transform = `rotate(${m * 6}deg)`;
    second.style.transform = `rotate(${s*6}deg)`;
    setInterval(showTime, 1000);
}
showTime();
```