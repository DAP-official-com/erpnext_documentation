<!-- add-breadcrumbs -->

# คัดลอกการวางหลายระเบียนจาก Excel

**หากคุณมีลำดับของระเบียนที่บันทึกไว้ในแผ่นงาน Excel ซึ่งจำเป็นต้องจับคู่กับตารางย่อยใน ERPNext ก็สามารถทำได้เช่นเดียวกันโดยใช้คุณลักษณะนี้**

สมมติว่า คุณมีรายการของรายการที่บันทึกไว้ในแผ่นงาน Excel และคุณจำเป็นต้องคัดลอกรายการดังกล่าวไปยังตารางย่อย 'รายการ' ในใบสั่งขาย

## ขั้นตอนในการคัดลอกวางบันทึกจาก excel

* เตรียมข้อมูลต้นฉบับใน Excel หรือโปรแกรมแก้ไขข้อความโดยคั่นแต่ละคอลัมน์ด้วยแท็บ

 ![Copy Pasting](/docs/assets/img/using-erpnext/using-copy-paste-1.png)

* ลากเพื่อเลือกระเบียน แล้วคลิกปุ่มเมนูคัดลอกหรือโดย Ctrl + C (Cmd + C) สำหรับ

กรณีที่ 1 คอลัมน์แรกของแผ่นงาน Excel ควรเป็นส่วนหัวของคอลัมน์และเนื้อหาในนั้น

กรณีที่ 2 เมื่อไม่มีส่วนหัวของคอลัมน์ที่กำหนดไว้ ข้อมูลจะถูกแมปกับคอลัมน์ที่มองเห็นได้

 ![Copy Pasting](/docs/assets/img/using-erpnext/using-copy-paste-4.png)

* วางเคอร์เซอร์ไปที่ช่องป้อนข้อมูลเป้าหมายของตารางย่อย และวาง คุณลักษณะการคัดลอกและวางนี้แตกต่างจากการนำเข้าผ่านคุณลักษณะไฟล์อัปโหลด ซึ่งจะทริกเกอร์เหตุการณ์การเปลี่ยนแปลงฟิลด์โดยอัตโนมัติ

 ![Copy Pasting](/docs/assets/img/using-erpnext/using-copy-paste-3.gif)

สำหรับการพิจารณาประสิทธิภาพ คุณควรวางระเบียนน้อยกว่าหรือเท่ากับ 100 ต่อครั้งเท่านั้น

{next}