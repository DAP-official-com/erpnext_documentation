#การบริโภควัสดุ

ฟังก์ชันการใช้วัสดุช่วยให้คุณมี 'รายการสต็อค' การบริโภคหลายรายการเทียบกับใบสั่งงาน หากต้องการเปิดใช้งาน ให้ไปที่การผลิต > การตั้งค่าการผลิต

<img class="screenshot" alt="Item Alternative" src="{{docs_base_url}}/assets/img/manufacturing/allow-material-consumption.png">

เมื่อเปิดใช้งานแล้ว ปุ่ม 'การใช้วัสดุ' จะพร้อมใช้งานในใบสั่งงานเมื่อเริ่มต้น

<img class="screenshot" alt="Item Alternative" src="{{docs_base_url}}/assets/img/manufacturing/material-consumption-button.png">

เมื่อคลิกปุ่ม จะทำสิ่งต่อไปนี้:

1. จะสร้างรายการสต็อคโดยมีวัตถุประสงค์ 'การใช้วัสดุเพื่อการผลิต'

<img class="screenshot" alt="Item Alternative" src="{{docs_base_url}}/assets/img/manufacturing/material-consumption-for-manufacture.png">

2. หาก "Backflush Raw Materials Based On" ในการตั้งค่าการผลิตถูกตั้งค่าเป็น "BOM" หากจะเสนอให้ใช้ปริมาณที่จำเป็นทั้งหมดสำหรับการผลิต
3. หาก "Backflush Raw Materials Based On" ในการตั้งค่าการผลิตถูกตั้งค่าเป็น 'วัสดุที่ถ่ายโอนเพื่อการผลิต' หากจะเสนอให้ใช้ปริมาณที่โอนทั้งหมดสำหรับการผลิต
4. เมื่อส่งแล้ว จะอัปเดตคอลัมน์ 'จำนวนที่ใช้ไป' ในใบสั่งงาน

<img class="screenshot" alt="Item Alternative" src="{{docs_base_url}}/assets/img/manufacturing/consumed-qty.png">

5. ในการใช้วัสดุที่ประสบความสำเร็จ จะแนะนำปริมาณที่ยังไม่ได้ใช้
6. เมื่อคลิกปุ่ม "เสร็จสิ้น" ใน ใบสั่งงาน จะพิจารณาถึงปริมาณที่ใช้ไป

### การตรวจสอบความถูกต้อง

* หากไม่ได้ตั้งค่า "อนุญาตการใช้วัสดุหลายรายการ" ในการตั้งค่าการผลิต แต่ "การใช้วัสดุสำหรับการผลิต" จะถูกใช้ในรายการสต็อค

<img class="screenshot" alt="Item Alternative" src="{{docs_base_url}}/assets/img/manufacturing/material-consumption-stock-entry.gif">

* ไม่สามารถยกเลิก "การใช้วัสดุสำหรับการผลิต" สำหรับคำสั่งงานที่เสร็จสมบูรณ์

<img class="screenshot" alt="Item Alternative" src="{{docs_base_url}}/assets/img/manufacturing/cancel-material-consumption-stock-entry.gif">
