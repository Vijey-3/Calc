# Ex.08 Design of a Standard Calculator
## Date:26/04/2024

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
    <link rel="stylesheet" href="theme.css">
</head>
<body>
    <div class="container">
        <h3 class="text">VIJEY K S(212223040239)</h3>

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

    <script src="code.js"></script>
</body>
</html>
code.js
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
theme.css
.container {
    text-align: center;
    margin-top: 23px;
}

.calculator {
    border: none;
    background-color: #ff0000;
    padding: 30px;
    border-radius: 20px;
    display: inline-block;
}

h1 {
    font-size: 40px;
    font-family: Arial, Helvetica, sans-serif;
}

h3 {
    font-size: 20px;
    font-weight: bold;
    color: black;
    text-align: center;
    margin: auto;
    margin-top: 20px;
}

input {
    text-align: right;
    border-radius: 0px;
    border: 2px solid rgb(13, 13, 13);
    padding: 20px;
    background: rgb(255, 255, 255);
    font-size: 40px;
    height: 60px;
    width: 290px;
    color: rgb(11, 11, 11);
}

table {
    margin: auto;
}

button {
    border-radius: 30px;
    border: 5;
    outline: 0;
    box-shadow: -8px -8px 15px rgba(180, 180, 180, 0.1),  5px 5px 15px rgba(0, 0, 0, 0.2);
    font-size: 20px;
    background: transparent;
    color:"green";
    width: 60px;
    height: 60px;
    margin: 6px;
    cursor: pointer;
}

.color {
    color: "blue";
}

```
## OUTPUT:
![alt text](<Screenshot (51).png>)
![alt text](<Screenshot (52).png>)
## RESULT:
The program for designing a standard calculator using HTML and CSS is executed successfully.
