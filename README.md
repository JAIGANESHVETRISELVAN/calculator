```
<html >
<head>

    <title>My Calculator</title>
    <style>
        #calc {
            text-align: center;
            margin: auto;
            width: 10000px;
        }
        .button {
            margin-left: 550px;
            margin-right: 550px;
            padding: 30px;
            background-color:rgb(205, 170, 150);
            color: rgb(225, 163, 163);
            border:10px solid rgb(7, 252, 121); 
        }

        .button input[type="button"] {
            background-color:rgb(37, 227, 34);
            height: 40px;
            width: 40px;
            margin: 0 2px;
            border: 3px solid rgb(187, 135, 222);
        }
    </style>
</head>

<body style="background-color: rgb(0, 0, 0);">
    <h1 align="center" style="color: rgb(88, 168, 120);">CALCULATOR</h1>
        <h3 align="center" style="color: rgb(48, 155, 77);">JAIGANESH V</h3>
        <div class="button">
            <center>
            
            <input type="text" id="t1" style="width:270px; height:30px;"><br><br>
            <input type="button" onkeydown="op(event)" onclick="f('7')" value="7">
            <input type="button" onkeydown="op(event)" onclick="f('8')" value="8">
            <input type="button" onkeydown="op(event)" onclick="f('9')" value="9">
            <input type="button" onkeydown="op(event)" onclick="f('+')" value="+">
            <input type="button" onkeydown="op(event)" value="C"  onclick="clr()"><br><br>
            <input type="button" onkeydown="op(event)" onclick="f('4')" value="4">
            <input type="button" onkeydown="op(event)" onclick="f('5')" value="5">
            <input type="button" onkeydown="op(event)" onclick="f('6')" value="6">
            <input type="button" onkeydown="op(event)" onclick="f('*')" value="x">
            <input type="button" onkeydown="op(event)" onclick="f('^0.5')" value="+/-"><br><br>
            <input type="button" onkeydown="op(event)" onclick="f('1')" value="1">
            <input type="button" onkeydown="op(event)" onclick="f('2')" value="2">
            <input type="button" onkeydown="op(event)" onclick="f('3')" value="3">
            <input type="button" onkeydown="op(event)" onclick="f('-')" value="-">
            <input type="button" onkeydown="op(event)" onclick="f('/')" value="%"><br><br>    
            <input type="button" onkeydown="op(event)" onclick="f('0')" value="0">
            <input type="button" onkeydown="op(event)" onclick="f('.')"
                value=".">
            <input type="button" onkeydown="op(event)" onclick="f('+')" value="+">
            <input type="button" onclick="solve()" value="=" style="color: rgb(212, 192, 255); width:110px;font-weight:bolder;">
        </center>
        </div>
</body>
<script src="https://cdnjs.cloudflare.com/ajax/libs/mathjs/9.4.4/math.js"></script>

<script>
    function f(val) {
        document.getElementById('t1').value += val;
    }

    function clr() {
        document.getElementById('t1').value = "";
    }

    function op(event) {
        if (event.key == '7' || event.key == '8' || event.key == '9' || event.key == '+' || event.key == '+/-' || event.key == '4' ||
            event.key == '5' || event.key == '6' || event.key == '#' || event.key == '+/-' || event.key == '1' ||
            event.key == '2' || event.key == '3' || event.key == '-' || event.key == '/' || event.key == '0' || event.key == '.') {
            document.getElementById('t1').value += event.key;
        }
    }

    var cal = document.getElementById('calc');
    cal.onkeyup = function (event) {
        if (event.keyCode == 13) {
            console.log("Enter");
            solve();
        }
    }

    function solve() {
        let x = document.getElementById('t1').value;
        let y = math.evaluate(x);
        document.getElementById('t1').value = y;
    }
</script>

</html>
```
![Screenshot 2024-07-08 234455](https://github.com/JAIGANESHVETRISELVAN/calculator/assets/133752156/107badbe-d2e5-4e94-93f9-7a38fe681337)
