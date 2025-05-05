# StopWatch
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>StopWatch</title>
    <style>
        .center
        {
            display: flex;
            height: 100vh;
            align-items: center;
            justify-content: center;
            flex-direction: column;
        }

        button
        {
            height: 50px;
            width: 50px;
            border-radius: 5px;
            margin: 15px;
        }
    </style>
</head>
<body>
    <div class="center">
        <h1>StopWatch</h1>
        <button id="value"></button>
        <div>
            <button id="start">Start</button>
            <button id="reset">Reset</button>
            <button id="stop">Stop</button>
        </div>
    </div>

    <script>
        let val = 0;
        let intervalId;
        document.getElementById("value").innerText = val;
        // Start
        document.getElementById("start").addEventListener("click" , function(){
            intervalId = setInterval(function(){
                document.getElementById("value").innerText = ++val;
            } , 1000); 
        });
        // Reset
        document.getElementById("reset").addEventListener("click" , function(){
            val = 0;
            document.getElementById("value").innerText = val;
            clearInterval(intervalId); // Stop timer after reset
        });
        // Stop
        document.getElementById("stop").addEventListener("click" , function(){
            clearInterval(intervalId);
        });
    </script>
</body>
</html>
```
