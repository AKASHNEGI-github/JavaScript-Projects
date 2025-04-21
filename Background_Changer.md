# Background Changer

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Background Changer</title>
    <style>
        #center
        {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .box
        {
            margin: 10px;
            width: 100px;
            height: 100px;
            border-radius: 10px;
            border: 3px solid black;
        }

        #red
        {
            background-color: red;
            
            
        }

        #yellow
        {
            background-color: yellow;
        }

        #green
        {
            background-color: green;
        }

        #blue
        {
            background-color: blue;
        }
    </style>
</head>
<body style="overflow: hidden;">
    <section id="center">
        <div class="box" id="red"></div>
        <div class="box" id="yellow"></div>
        <div class="box" id="green"></div>
        <div class="box" id="blue"></div>
    </section>

    <script>
        const body = document.querySelector("body");
        const box = document.querySelectorAll(".box");
        box.forEach(function(block){
            block.addEventListener("click" , function(event){
                console.log(event.target);
                if(event.target.id === "red"){
                    body.style.backgroundColor = event.target.id;
                }
                else if(event.target.id === "yellow"){
                    body.style.backgroundColor = event.target.id;
                }
                if(event.target.id === "green"){
                    body.style.backgroundColor = event.target.id;
                }
                if(event.target.id === "blue"){
                    body.style.backgroundColor = event.target.id;
                }
            });
        });
    </script>
</body>
</html>
```
