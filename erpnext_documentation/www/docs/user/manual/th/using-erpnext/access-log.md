---
title: Access log
add_breadcrumbs: 1
show_sidebar: 0

metatags:
 description: Access Log is a security feature that logs all data exports in the form of printing of Forms and reports, private file downloading and exporting reports in excel/csv formats.
 keywords: frappe, access log, erpnext v12, erpnext release notes, erpnext new features, erp, open source erp, free erp, security
---

# บันทึกการเข้าถึง

> Introduced in Version 13

**บันทึกการเข้าถึงเป็นคุณลักษณะด้านความปลอดภัยที่บันทึกการส่งออกข้อมูลทั้งหมดโดยผู้ใช้ทุกคนในระบบ**

เป็นเครื่องมือสำหรับผู้จัดการระบบเพื่อติดตามว่าผู้ใช้เข้าถึงหรือส่งออกไฟล์ใดในระบบ สิ่งนี้มีประโยชน์ในการติดตามข้อมูลที่ละเอียดอ่อนของบริษัทของคุณ เช่น ธุรกรรมหรือการเงิน

บันทึกการเข้าถึงถูกสร้างขึ้นในเหตุการณ์ต่อไปนี้:

 - การพิมพ์แบบฟอร์มและรายงานทั้งหมด
 - ดาวน์โหลดไฟล์ส่วนตัว
 - การส่งออกผ่านรูปแบบ XLSX/CSV

ใน ERPNext Access Log พร้อมใช้งานสำหรับ System Managers ซึ่งสามารถเข้าถึงได้โดยใช้ Global Search หรือผ่าน:

> หน้าหลัก > ผู้ใช้และการอนุญาต > บันทึก > บันทึกการเข้าถึง

![Access Log](/docs/assets/img/using-erpnext/using-access-log-3.png)

ในกรณีที่มีการสร้างบันทึกการเข้าใช้ในกรณีที่ส่งออก **รายงานปุ่มแสดงรายงาน** จะถูกสร้างขึ้นในบันทึกที่เกี่ยวข้อง เมื่อคลิกปุ่มนี้ คุณสามารถดูรายงานที่ส่งออกพร้อมกับตัวกรองที่ตั้งไว้

![Access Log](/docs/assets/img/using-erpnext/using-access-log-1.png)

ในทำนองเดียวกันปุ่ม **แสดงเอกสาร** จะถูกสร้างขึ้นในกรณีของเหตุการณ์ที่เกี่ยวข้องกับเอกสารโดยตรง เช่น การพิมพ์เอกสารและการดาวน์โหลดไฟล์ส่วนตัว

![Access Log](/docs/assets/img/using-erpnext/using-access-log-2.png)

เหตุการณ์เช่น [การพิมพ์ทั่วไป](/docs/user/manual/en/setting-up/print/raw-printing) บันทึกข้อมูลพร้อมกับเทมเพลตที่เลือกสำหรับเอกสาร

![Access Log](/docs/assets/img/using-erpnext/using-acces-log-4.png)