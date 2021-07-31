# rgaColorCodeGnaretor

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<style>
    body{
        height: 100vh;
        display: grid;
        place-items: center;
        margin: 0; padding: 0;
        box-sizing: border-box;

    }
    .main{
        display: grid;
        place-items: center;
        width: 300px;
        height: 500px;
        background: #333;
        border-radius: 20px;
        color: #fff;
        box-shadow: 5px 5px 10px #333;
        padding: 5px;
        font-family: sans-serif;
    }

    .main #box{
        width: 200px;
        height: 30px;
        border-radius: 20px;
        text-align: center;
        font-size: 1rem;
        outline: none;
    }
    input[type="range"]{
        -webkit-appearance: none;
        height: 15px;
        width: 80%;
        border-radius: 20px;
        outline: none;
    }

    input[type="range"]::-webkit-slider-thumb{
        -webkit-appearance: none;
        height: 25px;
        width: 25px;
        background-color: #fff;
        cursor: pointer;
        border-radius: 50%;
        outline: none;
    }
    .main #red{
        background: linear-gradient(90deg, #000, red);
    }
    .main #green{
        background: linear-gradient(90deg, #000, green);
    }
    .main #blue{
        background: linear-gradient(90deg, #000, blue);
    }
     
     
     
</style>
<body>
    <div class="main">
        Result: <input type="text" id="box" value="rgb(255, 255, 255)">
        Red: <input type="range" min="0" max="255" value="255"    id="red">
        Green: <input type="range" min="0" max="255" value="255"  id="green">
        Blue: <input type="range" min="0" max="255" value="255"   id="blue">
        
    </div>

    <script type="text/javascript">
        function myColor(){
            var red = document.getElementById('red').value;
            var green = document.getElementById('green').value;
            var blue = document.getElementById('blue').value;
            var color = 'rgb('+ red +','+ green +','+ blue +')';
            document.body.style.backgroundColor = color;
            document.getElementById('box').value = color;
        }

        document.getElementById('red').addEventListener('input',myColor);
        document.getElementById('green').addEventListener('input',myColor);
        document.getElementById('blue').addEventListener('input',myColor);
    </script>
    
</body>
</html>
