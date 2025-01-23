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
      background-color: #f9f9f9;
      color: #333;
      text-align: center;
      padding: 20px;
    }

    h1 {
      font-size: 2rem;
      color: #555;
    }

    button {
      background-color: #000;
      color: #fff;
      border: none;
      padding: 10px 20px;
      font-size: 1rem;
      border-radius: 5px;
      cursor: pointer;
      margin-top: 20px;
      transition: background-color 0.3s;
    }

    button:hover {
      background-color: #333;
    }

    #result {
      margin-top: 20px;
      font-size: 1.5rem;
      color: #000;
      font-weight: bold;
      opacity: 1;
      transition: opacity 0.5s ease-in-out;
    }

    .hidden {
      opacity: 0;
    }
  </style>
</head>
<body>
  <h1>สุ่มเหตุการณ์ใน PICNIC CARTOON</h1>
  <p>กดปุ่มด้านล่างเพื่อสุ่ม</p>
  <button id="generateBtn">สุ่มเลย!</button>
  <div id="result"></div>

  <script>
    // รายการชื่อ
    const names = [
      "สมศักดิ์", "ภูวฤทธิ์", "เจษฎา", "อรุณกร", "เรืองศักดิ์", "จิรเมธ", "กฤตรัตน์",
      "คาปูชิโน่", "มัคคิอาโต้", "ลาเต้", "มอคค่า", "มานาซิโอ้ย", "ราซารัส", "การิคการี่",
      "อลันตั้น", "ท่านผู้ถ่ายทอด", "ท่านหมายเลข 1", "ชูการ์", "ชานนท์", "ภีมพิพัฒน์",
      "จันทรา", "ราตรี", "มนตรา", "คุโรบะ", "อุงกะอุงกะ", "แบงค์", "ไหมทอง", "ศรเพชร",
      "มาริสา", "ชาดเพชร", "เอลเลียต", "นรเนศ", "ณเรศ", "ดนุเดช", "ชวิน", "รัชชานนท์",
      "วาคิม", "นครินทร์", "ครูวรรลพ", "ดำ", "แดง", "ชมพู", "น้ำเงิน", "เหลือง", "พีพี", "ไวโอเลต"
    ];

    // รายการการกระทำ
    const actions = [
      "กินข้าวกับ", "นั่งสนทนากับ", "เดินทางไปเที่ยวกับ", "เล่นเกมกับ", "วิ่งแข่งกับ",
      "เรียนหนังสือกับ", "ร้องเพลงคู่กับ", "วาดภาพกับ", "ทำอาหารกับ", "สำรวจป่ากับ"
    ];

    function generatePair() {
      const resultElement = document.getElementById("result");

      // แสดงข้อความระหว่างรอสุ่ม
      resultElement.innerText = "กำลังสุ่ม...";
      resultElement.classList.remove("hidden");

      // รอ 500ms เพื่อสร้างเอฟเฟกต์การสุ่ม
      setTimeout(() => {
        // สุ่มชื่อและการกระทำ
        const randomName1 = names[Math.floor(Math.random() * names.length)];
        let randomName2;
        do {
          randomName2 = names[Math.floor(Math.random() * names.length)];
        } while (randomName1 === randomName2);
        const randomAction = actions[Math.floor(Math.random() * actions.length)];

        // แสดงผลลัพธ์
        resultElement.innerText = `${randomName1} ${randomAction} ${randomName2}`;
      }, 500);
    }

    // เพิ่ม Event Listener ให้ปุ่ม
    document.getElementById("generateBtn").addEventListener("click", generatePair);
  </script>
</body>
</html>
