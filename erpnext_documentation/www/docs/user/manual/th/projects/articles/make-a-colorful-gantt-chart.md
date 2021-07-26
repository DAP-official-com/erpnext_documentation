<!--add breadcrumbs-->

#สร้างแผนภูมิแกนต์ที่มีสีสัน

ERPNext ให้ผู้ใช้เพิ่มสีให้กับเอกสารบางอย่างเพื่อให้เห็นภาพและการนำเสนอที่ดีขึ้น ตัวอย่างที่ดีคือ [ปฏิทินกิจกรรม](/docs/user/manual/th/using-erpnext/calendar) โดยคุณสามารถเพิ่มสีสำหรับแต่ละกิจกรรมได้

เราจะดำเนินการดังกล่าวโดยกำหนด [งาน](/docs/user/manual/th/projects/tasks) เองภายใต้โมดูล Projects

## ขั้นตอนในการเพิ่มสีสันให้กับแผนภูมิแกนต์

1. ไปที่ [แบบฟอร์มกำหนดเอง](/docs/user/manual/th/customize-erpnext/customize-form) ในระบบและเลือก *Task* ใน _Enter Form Type_ ตัวเลือก หรือคุณสามารถเข้าถึงหน้าจอนี้ได้โดยไปที่ **เมนู > ปรับแต่ง** จากรายการงานหรือแบบฟอร์ม

 <img class="screenshot" alt="customize-form" src="/docs/assets/img/articles/project-gantt-customize-form-1.gif">

1. เพิ่มฟิลด์ใหม่ใน doctype ของ fieldtype color
1. ตรวจสอบตัวเลือก *ในมุมมองรายการ*

 <img class="screenshot" alt="customize-form" src="/docs/assets/img/articles/project-gantt-in-list.png">

1. บันทึกแบบฟอร์ม กลับไปที่รายการงาน และโหลดซ้ำ
1. เมื่อเปิดงานที่มีอยู่หรือใหม่ คุณควรเห็นช่องสี เลือกสีสำหรับงาน

 <img class="screenshot" alt="customize-form" src="/docs/assets/img/articles/project-gantt-pick-color.png">

1. กลับไปที่รายการงานและสลับไปที่มุมมองแกนต์

  <img class="screenshot" alt="customize-form" src="/docs/assets/img/articles/project-gantt-colors.png">
