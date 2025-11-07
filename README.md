# sarthak-index.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Percentage Calculator</title>
  <style>
    /* Background and layout */
    body {
      background: linear-gradient(to right, #ff9900, #0072ff);
      font-family: 'Poppins', sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      color: #0a0000;
    }

    /* Calculator container */
    .calculator {
      background: rgba(186, 18, 18, 0.15);
      padding: 30px;
      border-radius: 15px;
      text-align: center;
      box-shadow: 0 8px 20px rgba(15, 15, 15, 0.2);
      width: 320px;
    }

    h1 {
      margin-bottom: 20px;
    }

    input {
      width: 90%;
      padding: 10px;
      margin: 10px 0;
      border: none;
      border-radius: 8px;
      font-size: 16px;
      text-align: center;
    }

    button {
      width: 100%;
      padding: 10px;
      margin-top: 15px;
      background-color: #00ffcc;
      border: none;
      border-radius: 8px;
      font-size: 16px;
      color: #7910f1;
      cursor: pointer;
      transition: 0.3s;
    }

    button:hover {
      background-color: #00ccaa;
    }

    .result {
      margin-top: 20px;
      font-size: 18px;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <div class="calculator">
    <h1>Percentage Calculator</h1>

    <input type="number" id="value" placeholder="Enter Marks Obtained">
    <input type="number" id="total" placeholder="Enter total Marks">
    <button onclick="calculatePercentage()">Calculate</button>

    <div class="result" id="result"></div>
  </div>

  <script>
    function calculatePercentage() {
      const value = parseFloat(document.getElementById("value").value);
      const total = parseFloat(document.getElementById("total").value);
      const resultDiv = document.getElementById("result");

      if (isNaN(value) || isNaN(total) || total === 0) {
        resultDiv.textContent = "Please enter valid numbers!";
        return;
      }

      const percentage = (value / total) * 100;
      resultDiv.textContent = Result: ${percentage.toFixed(2)}%;
    }
  </script>
</body>
</html>
