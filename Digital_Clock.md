# Digital Clock

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Clock</title>
    <style>
        #center
        {
            display: flex;
            height: 100vh;
            align-items: center;
            justify-content: center;
            flex-direction: column;
        }

        h1
        {
            font-size: 40px;
        }

        #clock
        {
            padding: 20px 50px;
            margin-top: 10px;
            font-size: 40px;
            color: White;
            background-color: orange;
            border-radius: 10px;
            border: 5px solid black;
        }
    </style>
</head>
<body style="overflow: hidden;">
    <section id="center">
        <h1>Digital Clock</h1>
        <div id="clock"></div>
    </section>

    <script>
        const clock = document.querySelector("#clock");
        setInterval(function(){
            let date = new Date();
            clock.innerHTML = date.toLocaleTimeString();
        } , 1000);
    </script>
</body>
</html>
```
