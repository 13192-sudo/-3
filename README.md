<!DOCTYPE html>
<html>
<head>
  <title>แปลงคำ</title>
  <style>
    body { text-align: center; font-family: sans-serif; margin-top: 50px; }
    textarea { width: 300px; height: 100px; }
    button { margin-top: 10px; padding: 10px; border-radius: 8px; }
	body {
  background-color: #6666CC; /* สีฟ้าอ่อน */
}
  </style>
</head>
<body>
  <h1>แปลงคำด่า</h1>
  <textarea id="inputText" placeholder="พิมพ์ข้อความที่นี่"></textarea><br>
  <button onclick="replaceText()">แปลงคำ</button>
  <p>ผลลัพธ์:</p><br>
  <textarea id="outputText" placeholder="ผลลัพธ์ข้อความที่นี่"></textarea>

  <script>
  var textNo1  = ["ไอ้", "อี", "ขี้", "หมา", "เหี้ย","ควาย","บ้านนอก","ควย","หี","เลว","ลาว","เขมร","โง่","บ้า","อีเวร","สันดาร","หำ","ตอแหล","แรด","ปัญญาอ่อน","กู","มึง","จันไร","ไม่เต็มบาท","ไม่ผ่าน","ไอสัส","ตก","เฮงซวย","ห่า","เสือก","อุบาด",""]; //คำหยาบ
  var textNo2  = ["คุณ", "นาง", "อุจจาระ", "สุนัข","สัตร์ครึ่งบกครึ่งน้ำ","กระบือ","ชนบท","อวัยวะเพศชาย","อวัยวะเพศหญิง","นิสัยไม่ดี","ต่างด้าว","ต่างด้าว","ฉลาดคนละทาง","สติไม่ดี","แม่คุณ","ความคิด","อวัยวะเพศชาย","โกหก","คลั่งไคร่เพศชาย"
  ,"สตืปัญญาพัฒนาการช้า","ฉัน","คุณ","ไม่สุภาพ","สติไม่ดี","เต็ม","เพื่อนรัก","ผ่าน","โชคร้าย","เพื่อนรัก","อยากใส่ใจ","ไม่น่ารัก"]; //คำสุภาพ
    function replaceText() {
      let text = document.getElementById("inputText").value;
      let result = text;
	  for (let i = 0; i < textNo1.length; i++) {
		result = result.replace(textNo1[i], textNo2[i]);
	  }
      document.getElementById("outputText").innerText = result;
    }
  </script>
</body>
</html>
