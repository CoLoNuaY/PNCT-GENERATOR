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
      background-color: #000; /* สีพื้นหลังดำ */
      color: #fff; /* สีตัวอักษรขาว */
      text-align: center;
      padding: 20px;
    }

    h1 {
      font-size: 2rem;
      color: #f0f0f0;
      margin-bottom: 10px;
    }

    p, a {
      font-size: 1rem;
      color: #ccc;
      margin: 5px 0;
    }

    a {
      text-decoration: none;
      color: #1e90ff;
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
      flex-direction: column; /* เปลี่ยนเป็นแนวตั้ง */
      align-items: center;
      gap: 10px;
      margin-top: 20px;
    }

    .result-box {
      background-color: #000;
      color: #fff;
      border: 2px solid #fff; /* ขอบสีขาว */
      padding: 20px;
      width: 200px;
      text-align: center;
      font-size: 1rem;
      font-weight: bold;
    }

    footer {
      margin-top: 50px;
      font-size: 0.9rem;
      color: #ccc;
    }
  </style>
</head>
<body>
  <h1>สุ่มเหตุการณ์ใน PICNIC CARTOON</h1>
  <p>กดปุ่มด้านล่างเพื่อสุ่ม</p>
  <button id="generateBtn">สุ่มเลย!</button>
  <div id="result-container">
    <div id="name1" class="result-box">---</div>
    <div id="action" class="result-box">---</div>
    <div id="name2" class="result-box">---</div>
  </div><hr>
<br>
  <p>
    <strong>YOUTUBE PICNIC CARTOON:</strong><br>
    <a href="https://youtube.com/@picniccartoon?si=2KwwhL5_45kM1Btc" target="_blank">https://youtube.com/@picniccartoon?si=2KwwhL5_45kM1Btc</a>
  </p>

  <p>
    <strong>ผู้สร้างและผู้เขียนโค๊ด:</strong><br>
    <a href="https://x.com/BAICLOVE?t=yPv2jYpxb9yVzkUiyAe36A&s=09" target="_blank">โคลเวอร์</a>
  </p>

  <footer>
    <p>V.0.2</p>
  </footer>

  <script>
    // รายการชื่อ
    const names = [
      "สมศักดิ์", "ภูวฤทธิ์", "เจษฎา", "อรุณกร", "เรืองศักดิ์", "จิรเมธ", "กฤตรัตน์",
      "คาปูชิโน่", "มัคคิอาโต้", "ลาเต้", "มอคค่า", "มานาซิโอ้", "ราซารัส", "การิคการี่",
      "อลันตั้น", "ท่านผู้ถ่ายทอด", "ท่านหมายเลข 1", "ชูการ์", "ชานนท์", "ภีมพิพัฒน์",
      "จันทรา", "ราตรี", "มนตรา", "คุโรบะ", "อุงกะอุงกะ", "แบงค์", "ไหมทอง", "ศรเพชร",
      "มาริสา", "ชาดเพชร", "เอลเลียต", "นรเนศ", "ณเรศ", "ดนุเดช", "ชวิน", "รัชชานนท์",
      "วาคิม", "นครินทร์", "ครูวรรลพ", "ดำ", "แดง", "ชมพู", "น้ำเงิน", "เหลือง", "พีพี", "ไวโอเลต", "ลีโอน่า", "พิกุลทอง"
    ];

    // รายการการกระทำ
    const actions = [
      "กินข้าวกับ", "นั่งสนทนากับ", "เดินทางไปเที่ยวกับ", "เล่นเกมกับ", "วิ่งแข่งกับ",
      "เรียนหนังสือกับ", "ร้องเพลงคู่กับ", "วาดภาพกับ", "ทำอาหารกับ", "สำรวจป่ากับ", "ตบตูด", "เตะตูด", "ให้ดอกไม้", "กัด", "ต่อยกับ", "เผา", "นอนกับ", "ดูหนังกับ", "เล่นเกมกระดานกับ", "เล่นเกมการ์ดกับ", "จูบกับ", "ตบหัว", "ทำแผลให้", "ยืนมอง", "ส่งจดหมายรักให้", "ซื้อของของ"
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
      }, 100); // ชื่อสุ่มเร็ว

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
      }, 2000); // หยุดหลัง 2 วินาที
    }

    document.getElementById("generateBtn").addEventListener("click", generatePair);
  </script>
</body>
</html>