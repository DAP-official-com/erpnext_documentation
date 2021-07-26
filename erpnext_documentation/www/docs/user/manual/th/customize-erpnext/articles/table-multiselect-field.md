# ตาราง MultiSelect ฟิลด์

ฟิลด์ Table MultiSelect นั้นคล้ายกับฟิลด์ลิงก์มาก ความแตกต่างที่สำคัญคือฟิลด์ Table MultiSelect ให้คุณเลือกค่าได้หลายค่า

ให้เราพิจารณาตัวอย่างเพื่อทำความเข้าใจในสิ่งเดียวกัน สมมติว่าคุณต้องการกำหนด ToDo ให้กับผู้ใช้หลายรายดังที่แสดงด้านล่าง:

<img alt="Table MultiSelect Field" class="screenshot" src="{{docs_base_url}}/assets/img/articles/table-multiselect-field.png">

You can add a Table MultiSelect Field by using the following steps:

## ขั้นตอนที่ 1: สร้าง DocType ย่อย

สร้าง DocType ใหม่ เปิดใช้งานช่องทำเครื่องหมาย 'Is Child Table' และ 'Editable Grid' และเพิ่มฟิลด์ที่มีประเภท 'Link' ดังที่แสดงด้านล่าง

ตั้งค่าฟิลด์ลิงก์เป็นฟิลด์บังคับ ตรวจสอบให้แน่ใจว่าฟิลด์ภายในตารางย่อยมีการทำเครื่องหมาย "ในมุมมองรายการ"

<img alt="DocType for Table MultiSelect" class="screenshot" src="{{docs_base_url}}/assets/img/articles/doctype-for-table-multi-select.png">

## ขั้นตอนที่ 2: เพิ่มฟิลด์ด้วยประเภท 'Table MultiSelect'

สร้างฟิลด์ด้วยประเภท 'ตาราง MultiSelect' และเพิ่ม DocType ที่สร้างขึ้นในขั้นตอนแรกใน 'ตัวเลือก'

<img alt="Field with type Table MultiSelect" class="screenshot" src="{{docs_base_url}}/assets/img/articles/multi-select-field.png">

คุณสามารถลบค่าที่เลือกได้โดยคลิกที่เครื่องหมายกากบาทถัดจากค่าที่เลือก หรือโดยการวางเคอร์เซอร์ไว้ข้างๆ ค่านั้นแล้วกด Backspace

ฟิลด์นี้อนุญาตให้เลือกค่าได้เพียงครั้งเดียวเท่านั้น

> หมายเหตุ: ไม่สามารถเพิ่มฟิลด์ MultiSelect ของตารางใน DocTypes ย่อย

{next}
