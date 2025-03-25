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
      text-align: center;
      padding: 20px;
      transition: background 0.5s, color 0.5s;
    }

    .main-container {
      background: rgba(0, 0, 0, 0.6);
      border: 5px solid #fff;
      padding: 20px;
      border-radius: 10px;
      display: inline-block;
      max-width: 80%;
      margin: 0 auto;
      box-shadow: 0 0 20px rgba(0, 0, 0, 0.7);
    }

    h1 {
      font-size: 2rem;
      text-shadow: 2px 2px 5px #000;
    }

    p, a {
      font-size: 1rem;
      margin: 5px 0;
    }

    a {
      text-decoration: none;
    }

    button {
      border: none;
      padding: 10px 15px;
      font-size: 1rem;
      border-radius: 5px;
      cursor: pointer;
      margin: 5px;
      transition: background-color 0.3s, color 0.3s;
    }

    #result-container {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 10px;
      margin-top: 20px;
    }

    .result-box {
      border: 2px solid #fff;
      padding: 15px;
      width: 200px;
      text-align: center;
      font-size: 1rem;
      font-weight: bold;
      border-radius: 5px;
    }

    footer {
      margin-top: 50px;
      font-size: 0.9rem;
    }

    /* ธีม */
    .theme-darkwhite {
      background: black;
      color: white;
    }

    .theme-whitedark {
      background: white;
      color: black;
    }

    .theme-firewater {
      background: linear-gradient(to bottom, #1e90ff, #ff4500);
      color: white;
    }

    .theme-cyber {
      background: black;
      color: #00ff00;
    }

    .theme-darkwhite .main-container,
    .theme-cyber .main-container {
      background: rgba(0, 0, 0, 0.8);
    }

    .theme-whitedark .main-container {
      background: rgba(255, 255, 255, 0.9);
      color: black;
    }

    .theme-firewater .main-container {
      background: rgba(0, 0, 0, 0.6);
    }
  </style>
</head>
<body class="theme-firewater"> <!-- ตั้งค่าเริ่มต้นเป็นธีม "น้ำกับไฟ" -->

  <div class="main-container">
    <h1>สุ่มเหตุการณ์ใน PICNIC CARTOON</h1>
    <p>กดปุ่มด้านล่างเพื่อสุ่ม</p>
    <button id="generateBtn">สุ่มเลย!</button>

    <div id="result-container">
      <div id="name1" class="result-box">---</div>
      <div id="action" class="result-box">---</div>
      <div id="name2" class="result-box">---</div>
    </div>

    <hr><br>
    
    <p><strong>เปลี่ยนธีม:</strong></p>
    <button onclick="changeTheme('theme-darkwhite')">ดำขาว</button>
    <button onclick="changeTheme('theme-whitedark')">ขาวดำ</button>
    <button onclick="changeTheme('theme-firewater')">น้ำกับไฟ</button>
    <button onclick="changeTheme('theme-cyber')">ไซเบอร์</button>

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
      <p>V.0.6</p>
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
    "มานิตย์", "ไซฟาเรียส", "เดลันเต้", "ครูวรรบวก", "คุณ", "เพน", "บอลลีวูดแมน",
    "ซินเทียน", "ชีตาห์", "พยัคฆ์สีคราม", "สอง"
  ];
  // รายการเหตุการณ์
  const actions = [
    "จับตูด", "ตกปลา", "ทำอาหาร", "ลูบหัว", "แอบส่องโทรศัพท์", "วาดรูปให้",
    "ขโมยรองเท้าของ", "กินหมาของ", "ขโมยมะขามของสมศักดิ์ไปให้", "เลียขา",
    "ปาหินใส่", "กินข้าวกับ", "นั่งสนทนากับ", "เดินทางไปเที่ยวกับ", "เล่นเกมกับ",
    "วิ่งแข่งกับ", "เรียนหนังสือกับ", "ร้องเพลงคู่กับ", "วาดภาพกับ", "ทำอาหารกับ",
    "เจาะยาง", "ตีดอทกับ", "ตอกไข่", "จับแต่งหญิงให้", "เรียกพวกรุมกระทืบ", "จีบ",
    "ให้ตัง", "เล่นเกมการ์ดแพ้", "จุ๊บเหม่ง", "เล่น russian roulette",
    "กินแหลกกับ", "หยุมหัว", "ตีป้อมกับ", "ลงดันกับ", "ทำเควสกับ", "กินกับ",
    "เปิดแอร์ดับร้อนกับ", "หนีภูเขาไฟระเบิดกับ", "ไปนอนบ้านของ", "ขับจักรยานกับ",
    "พูดหนมน้าใส่", "กัด", "แต่งหน้าให้", "เล่นน้ำสงกรานต์กับ", "ขโมยของ", "กิน",
    "ระเบิดบ้านของ", "เรียกสแตนมาสู้กับ", "คุยเรื่องธุรกิจร้านวินเทจของเอเลียตกับ",
    "เลียหน้า", "ปะแป้ง", "ลอกการบ้าน", "วิ่งหนี", "ให้ช็อคโกแลตกับ", "แปะสติ๊กเกอร์หัวใจให้", "ให้ดอกไม้กับ", "เดทกับ", "เต้นรำกับ", "หอมแก้ม",
  "หอมหัว", "จับมือ", "ควงแขน", "แต่งงานกับ", "เปิดห้องกับ", "อุ้ม", "จูบหลังมือของ", "กัดคอ",
  "กอดคอกับ", "หยิกแก้ม", "ทำช็อคโกแลตให้", "ส่งจดหมายรักให้", "ให้ช่อดอกไม้กับ",
  "คุกเข่าขอแต่งงานกับ", "บอกรัก", "รับรัก", "ส่งจุ๊บให้", "มอบของขวัญให้", "ทำอาหารให้",
  "จูบหน้าผาก", "กระซิบข้างหู", "เขียนการ์ดให้", "ให้ตุ๊กตากับ", "โอบไหล่",
  "ให้กำลังใจ", "เลี้ยงข้าว", "ถ่ายรูปคู่กับ", "เล่นดนตรีให้ฟัง", "ช่วยเลือกของขวัญ",
  "เดินเล่นด้วยกัน", "แตะไหล่", "ยิ้มให้", "ทำเพลงให้", "จับแก้ม", "ชมเชย",
  "ส่งข้อความหวาน ๆ", "โบกมือให้", "ป้อนขนม", "ส่งสายตาหวาน", "ขอให้เป็นแฟน",
  "เช็ดน้ำตาให้", "สวมแหวนให้", "พาไปดูพลุ", "แชร์ร่มด้วยกัน", "แตะหน้าผาก", "ฟังเพลงด้วยกัน"
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
        let randomName1 = randomArrayItem(names);
        let randomName2;
        do {
          randomName2 = randomArrayItem(names);
        } while (randomName1 === randomName2);
        let randomAction = randomArrayItem(actions);

        name1Element.innerText = randomName1;
        actionElement.innerText = randomAction;
        name2Element.innerText = randomName2;
      }, 2000);
    }

    document.getElementById("generateBtn").addEventListener("click", generatePair);

    // เปลี่ยนธีม
    function changeTheme(theme) {
      document.body.className = theme;
    }
  </script>
</body>
</html>