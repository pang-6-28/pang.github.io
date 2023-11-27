# pang.github.io
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Interactive Voting</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin: 50px;
    }
    h2 {
      color: #333;
    }
    .options {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin-top: 20px;
    }
    .option {
      padding: 10px 20px;
      cursor: pointer;
      background-color: #3498db;
      color: #fff;
      border: none;
      border-radius: 5px;
      font-size: 16px;
    }
    .result {
      margin-top: 20px;
      font-size: 18px;
    }
  </style>
</head>
<body>

  <h2>投票選項</h2>

  <div class="options">
    <button class="option" onclick="vote(0)">選項 A</button>
    <button class="option" onclick="vote(1)">選項 B</button>
    <button class="option" onclick="vote(2)">選項 C</button>
  </div>

  <div class="result">
    <p>投票結果：</p>
    <p id="resultA">選項 A: 0 票</p>
    <p id="resultB">選項 B: 0 票</p>
    <p id="resultC">選項 C: 0 票</p>
  </div>

  <script>
    // 初始化投票數據
    let votes = [0, 0, 0];

    // 投票函數
    function vote(option) {
      votes[option]++;
      updateResults();
    }

    // 更新投票結果
    function updateResults() {
      document.getElementById('resultA').innerText = `選項 A: ${votes[0]} 票`;
      document.getElementById('resultB').innerText = `選項 B: ${votes[1]} 票`;
      document.getElementById('resultC').innerText = `選項 C: ${votes[2]} 票`;
    }
  </script>

</body>
</html>
