# Calculator-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stylish Calculator</title>
    <style>
        body {
            background: #121212;
            display: flex;
            flex-direction: column;
            align-items: center;
            height: 100vh;
            margin: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        .social-top {
            margin-top: 20px;
            display: flex;
            justify-content: center;
            gap: 20px;
        }

        .social-top a {
            text-decoration: none;
            color: #ffffff;
            font-size: 24px;
            transition: 0.3s;
        }

        .social-top a:hover {
            color: #00ffc8;
        }

        .social-top i {
            font-size: 28px;
        }

        .calculator {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            padding: 20px;
            border-radius: 20px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.5);
            width: 320px;
            margin-top: 30px;
        }

        .display {
            background: #1f1f1f;
            color: #00ffc8;
            padding: 20px;
            font-size: 28px;
            border-radius: 12px;
            text-align: right;
            margin-bottom: 20px;
        }

        .buttons {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 12px;
        }

        button {
            padding: 20px;
            font-size: 18px;
            border: none;
            border-radius: 12px;
            background: #2b2b2b;
            color: #ffffff;
            transition: 0.2s;
        }

        button:hover {
            background: #00ffc8;
            color: #121212;
            cursor: pointer;
        }
    </style>
    <!-- Font Awesome for icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
</head>
<body>

    <!-- Social Media Links Top -->
    <div class="social-top">
        <a href="https://www.instagram.com/___nobi_shizu____________13_18/profilecard/?igsh=MWMwcnBiY2QwOG11Zg==" target="_blank" title="Instagram">
            <i class="fab fa-instagram"></i>
        </a>
        <a href="https://wa.me/919103594759" target="_blank" title="WhatsApp">
            <i class="fab fa-whatsapp"></i>
        </a>
        <a href="https://www.snapchat.com/add/meir-muzamil?share_id=WWzpo__-oeA&locale=en-US" target="_blank" title="Snapchat">
            <i class="fab fa-snapchat"></i>
        </a>
    </div>

    <!-- Calculator -->
    <div class="calculator">
        <div class="display" id="display">0</div>
        <div class="buttons">
            <button onclick="clearDisplay()">C</button>
            <button onclick="appendValue('(')">(</button>
            <button onclick="appendValue(')')">)</button>
            <button onclick="appendValue('/')">÷</button>

            <button onclick="appendValue('7')">7</button>
            <button onclick="appendValue('8')">8</button>
            <button onclick="appendValue('9')">9</button>
            <button onclick="appendValue('*')">×</button>

            <button onclick="appendValue('4')">4</button>
            <button onclick="appendValue('5')">5</button>
            <button onclick="appendValue('6')">6</button>
            <button onclick="appendValue('-')">−</button>

            <button onclick="appendValue('1')">1</button>
            <button onclick="appendValue('2')">2</button>
            <button onclick="appendValue('3')">3</button>
            <button onclick="appendValue('+')">+</button>

            <button onclick="appendValue('0')">0</button>
            <button onclick="appendValue('.')">.</button>
            <button onclick="calculate()">=</button>
            <button onclick="appendValue('Math.sqrt(')">√</button>
        </div>
    </div>

    <script>
        let display = document.getElementById('display');

        function appendValue(value) {
            if (display.innerText === "0" || display.innerText === "Error") {
                display.innerText = value;
            } else {
                display.innerText += value;
            }
        }

        function clearDisplay() {
            display.innerText = "0";
        }

        function calculate() {
            try {
                display.innerText = eval(display.innerText);
            } catch {
                display.innerText = "Error";
            }
        }
    </script>
</body>
</html>
