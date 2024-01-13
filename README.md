<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="../node_modules/bootstrap/dist/css/bootstrap.css">
    <style>
        #slider{
            width: 10px;
            height: 35px;
            background-color: black;
            position: absolute;
            top: 130px;
        }
    </style>
    <script>
        function CalculatorClick(){
            var slider = document.getElementById("slider");
            var bmi = parseInt(document.getElementById("txtBMI").value);
            slider.style.left = bmi + 'px';
            var p = document.querySelector("p");
            if(bmi>10 && bmi<320){
                p.innerHTML = "Under Weight - Take Protiens";
            }else if (bmi>320 && bmi<600) {
                p.innerHTML = "Normal Weight - Great !";
            }
        }
    </script>
</head>
<body class="container-fluid">
    <h1>Your BMI</h1>
    <input type="text" size="4" id="txtBMI"> <button onclick="CalculatorClick()">Calculator</button>
    <h1>BMI Status</h1>
    <div class="progress">
        <div class="progress-bar bg-warning me-1" style="width: 30%;">
    </div>
    <div class="progress-bar bg-success me-1" style="width: 30%;">
    </div>
    <div class="progress-bar bg-dark me-1" style="width: 30%;">
    </div>
    <div class="progress-bar bg-danger" style="width: 30%;">
    </div>
    <div id="slider"></div>
</div>
<p></p>
</body>
</html>
