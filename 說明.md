# 簡單計算機
簡單計算機是個開源軟體，你可以任意的修改它，並且分享它

這個軟體主要是有了興趣而設計，包括動畫元素以及排版都是合併成.html檔
![github上的檔案截圖](https://raw.githubusercontent.com/txt5889/123ez/f09b1d08736e61472947dc78edf26d3a1a2fc963/%E6%88%AA%E5%9C%96%202023-11-07%20%E4%B8%8B%E5%8D%888.05.22.png)
接著！我還試著用Chrome做出了這個網站的qr code

![qr code 圖](https://raw.githubusercontent.com/txt5889/math/main/qrcode_txt5889.github.io%20(1).png)

現在你可以試著改造出你自己的計算機

我直接把程式碼全部整理在下面
```
<!DOCTYPE html>
<html>
<head>
    <title>簡單計算機</title>
    <style>
        body {
            background-color: #f0f0f0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        .calculator {
            width: 300px;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            background-color: #fff;
        }

        input[type="text"], input[type="button"] {
            width: 50px;
            height: 50px;
            margin: 5px;
            font-size: 20px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        input[type="text"] {
            width: 100%;
            text-align: right;
        }

        input[type="button"] {
            background-color: #a0c8f0; /* 淺藍色 */
            color: #fff;
            border: none;
            border-radius: 5px;
            transition: background-color 0.2s, transform 0.1s;
        }

        input[type="button"]:hover {
            background-color: #70a0d8; /* 深藍色 */
            transform: scale(1.05);
        }
    </style>
</head>
<body>
    <div class="calculator">
        <input type="text" id="display" readonly>
        <br>
        <input type="button" value="7" onclick="appendToDisplay('7')">
        <input type="button" value="8" onclick="appendToDisplay('8')">
        <input type="button" value="9" onclick="appendToDisplay('9')">
        <input type="button" value="+" onclick="appendToDisplay('+')">
        <br>
        <input type="button" value="4" onclick="appendToDisplay('4')">
        <input type="button" value="5" onclick="appendToDisplay('5')">
        <input type="button" value="6" onclick="appendToDisplay('6')">
        <input type="button" value="-" onclick="appendToDisplay('-')">
        <br>
        <input type="button" value="1" onclick="appendToDisplay('1')">
        <input type="button" value="2" onclick="appendToDisplay('2')">
        <input type="button" value="3" onclick="appendToDisplay('3')">
        <input type="button" value="*" onclick="appendToDisplay('*')">
        <br>
        <input type="button" value="C" onclick="clearDisplay()">
        <input type="button" value="0" onclick="appendToDisplay('0')">
        <input type="button" value="=" onclick="calculate()">
        <input type="button" value="/" onclick="appendToDisplay('/')">
    </div>

    <script>
        function appendToDisplay(value) {
            document.getElementById('display').value += value;
        }

        function clearDisplay() {
            document.getElementById('display').value = '';
        }

        function calculate() {
            try {
                document.getElementById('display').value = eval(document.getElementById('display').value);
            } catch (error) {
                document.getElementById('display').value = 'Error';
            }
        }
    </script>
</body>
</html>
```

或者是要下載來修改也可以，諾要下載請點擊 **計算機.html** 下載
