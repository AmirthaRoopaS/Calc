# Ex.08 Design of a Standard Calculator
## Date:

## AIM:
To design a web application for a standard calculator with minimum five operations.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for creating attractive colors.

### Step 4:
Write JavaScript program for implementing five different operations.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
calc.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Calculator</title>
    <link rel="stylesheet" href="style.css">
</head>
<body bgcolor="black">
    <div class="container">
        <h1>CALCULATOR</h1>
        <h2 class="text">AMIRTHA ROOPA.S (212221220005)</h2><br>
        <h2 class="text">STANDARD CALCULATOR</h2>

        <div class="calculator">
            <input type="text" name="screen" id="screen">
            <table>
                <tr>
                    <td><button class="color">(</button></td>
                    <td><button class="color">)</button></td>
                    <td><button class="color">C</button></td>
                    <td><button class="color">%</button></td>
                </tr>
                <tr>
                    <td><button>7</button></td>
                    <td><button>8</button></td>
                    <td><button>9</button></td>
                    <td><button class="color">*</button></td>
                </tr>
                <tr>
                    <td><button>4</button></td>
                    <td><button>5</button></td>
                    <td><button>6</button></td>
                    <td><button class="color">-</button></td>
                </tr>
                <tr>
                    <td><button>1</button></td>
                    <td><button>2</button></td>
                    <td><button>3</button></td>
                    <td><button class="color">+</button></td>
                </tr>
                <tr>
                    <td><button>0</button></td>
                    <td><button class="color">.</button></td>
                    <td><button class="color">/</button></td>
                    <td><button class="color">=</button></td>
                </tr>
            </table>
        </div>
    </div>

    <script src="index.js"></script>
</body>
</html>
```
```
style.css

.container {
    text-align: center;
    margin-top: 25px;
}

.calculator {
    border: none;
    background-color: #85508a;
    padding: 30px;
    display: inline-block;
}

h1 {
    font-size: 45px;
    font-family: 'Garmond',Verdana, Geneva, Tahoma, sans-serif;
}

h2 {
    font-size: 25px;
    font-weight: bold;
    color: rgb(98, 189, 169);
    text-align: center;
    margin: border;
    margin-top: 20px;
}

input {
    border: 2px solid rgb(11, 33, 37);
    padding: 20px;
    background: rgb(172, 205, 236);
    font-size: 40px;
    height: 50px;
    width: 290px;
    color: rgb(11, 11, 11);
}

table {
    margin: auto;
}

button {
    border: 15;
    font-size: 35px;
    background: rgb(216, 227, 118);
    color: rgb(225, 9, 103);
    width: 80px;
    height: 80px;
    margin: 8px;
    cursor: pointer;
}

.color {
    color: rgb(1, 10, 36);
}
```
```
index.js

let screen = document.getElementById('screen');
buttons = document.querySelectorAll('button');
let screenValue = '';
for (item of buttons) {
    item.addEventListener('click', (e) => {
        buttonText = e.target.innerText;
        console.log('Button text is ', buttonText);
        if (buttonText == 'X') {
            buttonText = '*';
            screenValue += buttonText;
            screen.value = screenValue;
        }
        else if (buttonText == 'C') {
            screenValue = "";
            screen.value = screenValue;
        }
        else if (buttonText == '=') {
            screen.value = eval(screenValue);
        }
        else {
            screenValue += buttonText;
            screen.value = screenValue;
        }
    })
}
```
## OUTPUT:
![image](https://github.com/AmirthaRoopaS/Calc/assets/143496311/0c86e59d-5e3f-422d-8e44-592dd638bf37)
![image](https://github.com/AmirthaRoopaS/Calc/assets/143496311/dbd811c6-b1b4-4c29-bcad-9dcc05ff4fb3)
## RESULT:
The program for designing a standard calculator using HTML and CSS is executed successfully.
