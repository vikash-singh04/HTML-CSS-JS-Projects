# Project 1   "Color-Switcher"

## HTML
```HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>Digital-Clock</title>
</head>
<body>
    <div class="clock-container">
        <h1></h1>
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
    color:#fff;
}
body {
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    background: #212121
}
.clock-container {
    font-size: 50px;
}
```


## JavaScript
```javascript
console.log("Vikash")
const h1 = document.querySelector('h1');
console.log(h1.innerHTML);
function showTime() {
    let time = new Date();
    console.log(time);
    let hour = time.getHours();
    let minute = time.getMinutes();
    let second = time.getSeconds();
    let a = "AM";
    if(hour > 12) {
        hour = hour - 12;
        a = "PM";
    }
    hour = (hour < 10) ? "0"+hour : hour;
    minute = (minute < 10) ? "0"+minute : minute;
    second = (second < 10) ? "0"+second : second;
    h1.innerHTML = `${hour} : ${minute} : ${second} ${a}`;
    setInterval(showTime, 1000);
}
showTime();
```