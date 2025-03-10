<!--add breadcrumbs-->

# การนำเข้าข้อมูล

**เครื่องมือนำเข้าข้อมูลช่วยให้คุณสามารถนำเข้าบันทึกจากไฟล์ CSV/Excel**

เครื่องมือนำเข้าข้อมูลเป็นวิธีที่ง่ายในการอัปโหลด (หรือแก้ไข) ข้อมูลจำนวนมาก (โดยเฉพาะข้อมูลหลัก) เข้าสู่ระบบ

ในการเริ่มต้นนำเข้าข้อมูล ไปที่:

> หน้าหลัก > การนำเข้าข้อมูลและการตั้งค่า > นำเข้าข้อมูล

หรือไปที่เอกสารที่คุณต้องการนำเข้าแล้วคลิกเมนู > นำเข้า:

<img alt="Start Import" class="screenshot" src="/docs/assets/img/setup/data-import/task-menu-import.png">

ก่อนใช้การนำเข้าข้อมูล**ตรวจสอบให้แน่ใจ**ว่าคุณมีข้อมูลทั้งหมดพร้อม


## 1. การเพิ่มบันทึกใหม่

สมมติว่าคุณต้องการนำเข้ารายชื่อลูกค้าจากระบบเก่าของคุณไปยัง ERPNext ขั้นตอนแรกคือการดาวน์โหลดเทมเพลตซึ่งเราสามารถป้อนข้อมูลของเราได้

### 1.1 ดาวน์โหลดเทมเพลต

1. ไปที่รายชื่อลูกค้า คลิกที่เมนู > นำเข้า คลิกที่**ใหม่**
1. เลือกประเภทการนำเข้าเป็นแทรกระเบียนใหม่
1. คลิกที่**บันทึก**
1. คลิกที่ดาวน์โหลดแม่แบบ
1. ขณะที่เพิ่มระเบียนใหม่ เทมเพลตควรว่างเปล่า หากคุณมีลูกค้าไม่กี่รายในระบบของคุณ คุณสามารถเลือกประเภทการส่งออกเป็น "5 ระเบียน" เพื่อดูรูปแบบที่คุณต้องป้อนข้อมูลในเทมเพลต
1. เลือกประเภทไฟล์ของเทมเพลตการส่งออก
1. เลือกฟิลด์ที่คุณต้องการกรอกเป็นรายละเอียดลูกค้า
1. คลิกที่**ส่งออก**

![Download Template](/docs/assets/img/setup/data-import/download-template.gif)

### 1.2 การเพิ่มข้อมูลในเทมเพลต

เทมเพลตที่ดาวน์โหลดของคุณจะมีลักษณะดังนี้:

![Blank Template](/docs/assets/img/setup/data-import/blank-template-file.png)

เปิดเทมเพลตที่ดาวน์โหลดในแอปพลิเคชันสเปรดชีต (เช่น Excel, Numbers หรือ Libre Office) แล้วป้อนข้อมูลด้านล่างส่วนหัวของคอลัมน์ที่แสดงดังนี้:

![Customer Template with Data](/docs/assets/img/setup/data-import/customer-template-with-data.png)

บันทึกเทมเพลตของคุณเป็นไฟล์ Excel หรือ Comma Separated Values ​​(CSV)

> คุณสามารถปล่อยให้คอลัมน์ ID ว่างเปล่าในขณะที่แทรกระเบียนใหม่

เมื่อคุณสร้างเทมเพลตนี้ แต่ละแถวจะสร้างเรกคอร์ดลูกค้าในระบบ


### 1.3 การนำเข้าเทมเพลต

1. หลังจากอัปเดตไฟล์เทมเพลตของคุณแล้ว ให้กลับไปที่ฟอร์มการนำเข้าข้อมูลและแนบไฟล์โดยคลิกที่ปุ่ม**แนบ**
1. เลือกไฟล์ทมเพลตและคลิกที่**อัปโหลด**
1. หลังจากอัปโหลดจะประสบความสำเร็จคลิกที่**เริ่มต้นนำเข้า**

![Upload Template File](/docs/assets/img/setup/data-import/upload-template-file.png)

หากมีข้อผิดพลาดในเทมเพลตของคุณ ข้อผิดพลาดนั้นจะแสดงในส่วนคำเตือน คำเตือนจะถูกจัดหมวดหมู่ตามแถวหรือคอลัมน์พร้อมหมายเลข เพื่อให้คุณสามารถติดตามและแก้ไขปัญหาได้อย่างง่ายดายในเทมเพลต คุณต้องแก้ไขคำเตือนทั้งหมดก่อนจึงจะสามารถนำเข้าข้อมูลได้

![Import Warnings](/docs/assets/img/setup/data-import/import-warnings.png)

หลังจากที่คุณแก้ไขคำเตือนแล้ว ให้คลิกที่ **เริ่มต้นนำเข้า** อีกครั้งเพื่อนำเข้าข้อมูล เมื่อนำเข้าข้อมูลสำเร็จ คุณจะเห็นบันทึกของแต่ละระเบียนที่สร้างขึ้นในส่วนบันทึกการนำเข้า

![Import Success](/docs/assets/img/setup/data-import/import-success.png)

## 2. อัปเดตบันทึกที่มีอยู่ 

สมมติว่าคุณต้องการอัปเดตข้อมูลลูกค้าจำนวนมากในระบบของคุณ ขั้นตอนแรกคือการดาวน์โหลดเทมเพลตพร้อมข้อมูล

### 2.1 ดาวน์โหลดเทมเพลต

1. ไปที่รายชื่อลูกค้า คลิกที่เมนู > นำเข้า คลิกที่**ใหม่**
1. เลือกประเภทการนำเข้าเป็นอัปเดตระเบียนที่มีอยู่
1. คลิกที่**บันทึก**
1. คลิกที่ดาวน์โหลด**เทมเพลต**
1. ขณะอัปเดตเรกคอร์ดที่มีอยู่ คุณต้องส่งายการออกจากระบบด้วยฟิลด์ ID และฟิลด์ที่คุณต้องการอัปเดต คุณสามารถเลือกรายการทั้งหมด (All Records) หรือรายการที่ถูกคัดกรอง (Filtered Records) ขึ้นอยู่กับกรณีของคุณ
1. เลือกฟิลด์ที่คุณต้องการอัปเดตสำหรับเรกคอร์ดลูกค้า
1. คลิกที่**ส่งออก**

### 2.2 การอัปเดตข้อมูลในเทมเพลต

เทมเพลตที่ดาวน์โหลดของคุณจะมีลักษณะดังนี้:

![Customer Template for Update](/docs/assets/img/setup/data-import/customer-template-for-update.png)

เปลี่ยนค่าในเทมเพลตของคุณและบันทึกไฟล์เป็น Excel หรือ CSV

> ขณะส่งออกบันทึกเพื่ออัปเดต ตรวจสอบให้แน่ใจว่าคอลัมน์ ID ถูกส่งออกและไม่ถูกแตะต้อง ค่าในคอลัมน์ ID ใช้เพื่อระบุเร็กคอร์ดในระบบ คุณสามารถอัปเดตค่าในคอลัมน์อื่นแต่ไม่สามารถอัปเดตในคอลัมน์ ID

### 2.3 การนำเข้าเทมเพลท 

ทำตามขั้นตอนในหัวข้อ[การนำเข้าเทมเพลต](#23-importing-the-template)ด้านบน

## 3. การนำเข้าบันทึกย่อย

ข้อมูลใน ERPNext ถูกจัดเก็บไว้ในตาราง เช่น สเปรดชีตที่มีคอลัมน์และแถวของข้อมูล แต่ละแบบฟอร์มชอบใบสั่งขายมีหลายฟิลด์เช่นลูกค้า บริษัท ฯลฯ นอกจากนี้ยังมีตารางเช่นตารางรายการ ตารางภาษี ฯลฯ ในการนำเข้าข้อมูล ชุดของฟิลด์ในใบสั่งขายจะถือเป็นตารางหลักและแถว ภายในตารางย่อย (ตารางรายการ) จะถือว่าเป็นตารางย่อยสำหรับการนำเข้าข้อมูล

แต่ละแบบฟอร์มใน ERPNext สามารถมีตารางย่อยหลายตารางที่เชื่อมโยงอยู่ ตารางย่อยเชื่อมโยงกับตารางหลักและนำไปใช้โดยมีค่าหลายค่าสำหรับคุณสมบัติใดๆ ตัวอย่างเช่น รายการสามารถมีหลายราคาได้ ใบกำกับการขายมีหลายรายการ ภาษี และอื่นๆ

เมื่อคุณส่งออกเอกสารที่มีตารางย่อย เช่น แถวย่อยแต่ละแถวจะปรากฏในแถวที่แยกจากกัน แต่จะเชื่อมโยงกับแถวหลักเพียงแถวเดียว ค่าที่ตามมาในคอลัมน์หลักจะยังคงว่างเปล่า คุณต้องตรวจสอบให้แน่ใจว่าคำสั่งซื้อนี้ไม่เสียหายเมื่อคุณนำเข้าผ่านการนำเข้าข้อมูล

![Child Table Export](/docs/assets/img/setup/data-import/child-table-export.png)

## 4. ตัวเลือกการนำเข้าข้อมูล

### 4.1 นำเข้าจาก Google sheet

คุณยังนำเข้าข้อมูลจาก Google sheet ได้อีกด้วย นำเข้าเทมเพลตของคุณใน Google sheet และป้อนข้อมูล ตรวจสอบให้แน่ใจว่า Google sheet เป็นแบบสาธารณะ คุณทดสอบได้โดยเปิด URL ของ Google sheet ในหน้าต่างเบราว์เซอร์ที่ไม่ระบุตัวตน (incognito browser window.)

![Google Sheets](/docs/assets/img/setup/data-import/google-sheets.png)

![Import via Google Sheets](/docs/assets/img/setup/data-import/import-via-google-sheets.png)

### 4.2 ส่งหลังจากนำเข้า

ประเภทเอกสารใน ERPNext ส่วนใหญ่มีสองประเภท - เอกสารหลักและธุรกรรม ต้นแบบคือระเบียนเช่นลูกค้าและงานซึ่งไม่สามารถบันทึกได้เท่านั้น ธุรกรรมต่างๆ เช่น ใบสั่งขาย ใบแจ้งหนี้การซื้อ เป็นเอกสารที่ส่งได้และสามารถส่งได้

เมื่อคุณเลือกประเภทเอกสารที่ส่งได้สำหรับการนำเข้า คุณสามารถทำเครื่องหมายที่**ส่งหลังจากนำเข้า**เพื่อส่งเอกสารหลังจากที่นำเข้าแล้ว

### 4.3 อย่าส่งอีเมล

สมมติว่าคุณได้สร้าง [การแจ้งเตือน](/docs/user/manual/en/setting-up/notifications) ในระบบของคุณและเมื่อใดก็ตามที่สร้างลูกค้าเป้าหมาย อีเมลจะถูกส่งไป ตอนนี้ หากคุณกำลังนำเข้าลูกค้าเป้าหมายจำนวนมาก อีเมลจำนวนมากจะถูกส่งไป ซึ่งอาจไม่ต้องการ คุณสามารถปิดใช้งานตัวเลือกนี้เพื่อหลีกเลี่ยงการส่งอีเมล

## 5. หมายเหตุเพิ่มเติม

### 5.1 จำกัดการอัพโหลด

ไม่มีการจำกัดจำนวนระเบียนที่สามารถนำเข้าได้ แต่คุณต้องลองอัปโหลดครั้งละไม่กี่พันรายการเท่านั้น การนำเข้าระเบียนจำนวนมาก (สมมติว่า 50,000) อาจทำให้ระบบช้าลงอย่างมากสำหรับผู้ใช้ที่ใช้ระบบ

### 5.2 ไฟล์ CSV

ไฟล์ CSV (Comma Separated Value) เป็นไฟล์ข้อมูลที่คุณสามารถอัปโหลดไปยัง ERPNext เพื่ออัปเดตข้อมูลต่างๆ ไฟล์สเปรดชีตจากแอปพลิเคชันสเปรดชีตยอดนิยม เช่น MS Excel หรือ Open Office Spreadsheet สามารถบันทึกเป็นไฟล์ CSV ได้

หากคุณใช้ Microsoft Excel และใช้อักขระที่ไม่ใช่ภาษาอังกฤษ อย่าลืมบันทึกไฟล์ที่เข้ารหัสเป็น UTF-8

สำหรับ Excel เวอร์ชันเก่า ไม่มีวิธีบันทึกเป็น UTF-8 ที่ชัดเจน ดังนั้นให้บันทึกไฟล์ของคุณเป็น CSV จากนั้นเปิดใน Notepad จากนั้นบันทึกเป็น “UTF-8” (หรืออัปเกรด Excel ของคุณ!)


## 6. วีดีโอ

<div class="embed-container">
    <iframe src="https://www.youtube.com/embed/Ta2Xx3QoK3E" frameborder="0" allowfullscreen></iframe>
</div>

## 7. หัวข้อที่เกี่ยวข้อง

1. [ผังผู้นำเข้าบัญชี](/docs/user/manual/en/setting-up/chart-of-accounts-importer)
1. [การส่งออกข้อมูล](/docs/user/manual/en/setting-up/data/data-export)
