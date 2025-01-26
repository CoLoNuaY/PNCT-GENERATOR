<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>สุ่มเหตุการณ์ - PICNIC CARTOON</title>
  <meta name="description" content="เว็บสุ่มเหตุการณ์ใน PICNIC CARTOON ที่สนุกและน่าตื่นเต้น">
  <meta name="keywords" content="สุ่มเหตุการณ์, PICNIC CARTOON, เว็บสุ่ม">
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(to bottom, #1e90ff, #ff4500); /* ธีมน้ำกับไฟ */
      color: #fff;
      text-align: center;
      padding: 20px;
    }

    .main-container {
      background: rgba(0, 0, 0, 0.6); /* พื้นหลังโปร่งแสง */
      border: 5px solid #fff; /* กรอบสีขาว */
      padding: 20px;
      border-radius: 10px;
      display: inline-block;
      max-width: 80%;
      margin: 0 auto;
      box-shadow: 0 0 20px rgba(0, 0, 0, 0.7);
    }

    h1 {
      font-size: 2rem;
      color: #fff;
      text-shadow: 2px 2px 5px #000;
      margin-bottom: 10px;
    }

    p, a {
      font-size: 1rem;
      color: #ccc;
      margin: 5px 0;
    }

    a {
      text-decoration: none;
      color: #ffdd00;
    }

    a:hover {
      text-decoration: underline;
    }

    button {
      background-color: #fff;
      color: #000;
      border: none;
      padding: 10px 20px;
      font-size: 1rem;
      border-radius: 5px;
      cursor: pointer;
      margin-top: 20px;
      transition: background-color 0.3s, color 0.3s;
    }

    button:hover {
      background-color: #333;
      color: #fff;
    }

    #result-container {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 10px;
      margin-top: 20px;
    }

    .result-box {
      background: rgba(0, 0, 0, 0.8);
      color: #00ffff;
      border: 2px solid #fff;
      padding: 20px;
      width: 200px;
      text-align: center;
      font-size: 1rem;
      font-weight: bold;
      border-radius: 5px;
    }

    footer {
      margin-top: 50px;
      font-size: 0.9rem;
      color: #fff;
    }
  </style>
</head>
<body>
  <div class="main-container">
    <h1>สุ่มเหตุการณ์ใน PICNIC CARTOON</h1>
    <p>กดปุ่มด้านล่างเพื่อสุ่ม</p>
    <button id="generateBtn">สุ่มเลย!</button>
    <div id="result-container">
      <div id="name1" class="result-box">---</div>
      <div id="action" class="result-box">---</div>
      <div id="name2" class="result-box">---</div>
    </div>
    <hr>
    <br>
    <p>
      <strong>YOUTUBE PICNIC CARTOON:</strong><br>
      <a href="https://youtube.com/@picniccartoon?si=2KwwhL5_45kM1Btc" target="_blank">พี่ปิคนิค</a>
    </p>
    <p>
      <strong>ผู้สร้างและผู้เขียนโค๊ด:</strong><br>
      <a href="https://x.com/BAICLOVE?t=yPv2jYpxb9yVzkUiyAe36A&s=09" target="_blank">โคลเวอร์</a>
    </p>
    <footer>
      <p>V.0.3</p>
    </footer>
  </div>

  <script>
    // รายการตัวละคร
    const names = [
      "สมศักดิ์", "ภูวฤทธิ์", "เจษฎา", "อรุณกร", "เรืองศักดิ์", "จิรเมธ", "กฤตรัตน์",
      "คาปูชิโน่", "มัคคิอาโต้", "ลาเต้", "มอคค่า", "มานาซิโอ้", "ราซารัส", "การิคการี่",
      "อลันตั้น", "ท่านผู้ถ่ายทอด", "ท่านหมายเลข 1", "ชูการ์", "ชานนท์", "ภีมพิพัฒน์",
      "จันทรา", "ราตรี", "มนตรา", "คุโรบะ", "อุงกะอุงกะ", "แบงค์", "ไหมทอง", "ศรเพชร",
      "มาริสา", "ชาดเพชร", "เอลเลียต", "นรเนศ", "ณเรศ", "ดนุเดช", "ชวิน", "รัชชานนท์",
      "วาคิม", "นครินทร์", "ครูวรรลพ", "ดำ", "แดง", "ชมพู", "น้ำเงิน", "เหลือง", 
      "มานิตย์", "ไซฟาเรียส", "เดลันเต้", "ครูวรรบวก", "คุณ"
    ];

    // รายการเหตุการณ์
    const actions = [
      "จับตูด", "ตกปลา", "ทำอาหาร", "ลูบหัว", "แอบส่องโทรศัพท์", "วาดรูปให้",
      "ขโมยรองเท้าของ", "กินหมาของ", "ขโมยมะขามของสมศักดิ์ไปให้", "เลียขา",
      "ปาหินใส่", "กินข้าวกับ", "นั่งสนทนากับ", "เดินทางไปเที่ยวกับ", "เล่นเกมกับ",
      "วิ่งแข่งกับ", "เรียนหนังสือกับ", "ร้องเพลงคู่กับ", "วาดภาพกับ", "ทำอาหารกับ"
    ];

    function randomArrayItem(array) {
      return array[Math.floor(Math.random() * array.length)];
    }

    function generatePair() {
      const name1Element = document.getElementById("name1");
      const actionElement = document.getElementById("action");
      const name2Element = document.getElementById("name2");

      let interval = setInterval(() => {
        name1Element.innerText = randomArrayItem(names);
        actionElement.innerText = randomArrayItem(actions);
        name2Element.innerText = randomArrayItem(names);
      }, 100);

      setTimeout(() => {
        clearInterval(interval);
        const randomName1 = randomArrayItem(names);
        let randomName2;
        do {
          randomName2 = randomArrayItem(names);
        } while (randomName1 === randomName2);
        const randomAction = randomArrayItem(actions);

        name1Element.innerText = randomName1;
        actionElement.innerText = randomAction;
        name2Element.innerText = randomName2;
      }, 2000);
    }

    document.getElementById("generateBtn").addEventListener("click", generatePair);
  </script>
</body>
</html>