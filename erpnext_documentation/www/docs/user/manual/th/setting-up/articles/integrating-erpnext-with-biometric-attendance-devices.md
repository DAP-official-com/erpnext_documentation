---
title: Integrating ERPNext With Biometric Attendance Devices
add_breadcrumbs: 1
show_sidebar: 0

metatags:
 description: ERPNext has the provision to mark attendance from Check-in and Check-out logs from biometric. There are several possible methods to integrate your biometric device based on the vendor and the available features of your device.
 keywords: frappe, erpnext, erpnext attendance, biometric device integration, human resource, auto attendance
---

<!-- add-breadcrumbs -->
# การบูรณาการ ERPNext กับอุปกรณ์ไบโอเมตริกซ์ (Biometric Attendance Devices)

บันทึกการเข้างานจากอุปกรณ์ไบโอเมตริกซ์เป็นประเภทของบันทึกการเช็คอินและเช็คเอาท์ของพนักงาน

ERPNext มีข้อกำหนดในการจัดเก็บบันทึกเหล่านี้ในเอกสารที่เรียกว่า การเข้างานของพนักงาน (Employee Checkin)

จากนั้นสามารถทำเครื่องหมายการเข้างานตามบันทึกการเช็คอินของพนักงานและ [การตั้งค่าการเข้างานอัตโนมัติ](/docs/user/manual/th/human-resources/shift-management#25-auto-attendance-settings) ของพนักงานโดยใช้การเข้าร่วมอัตโนมัติ [การเข้างานอัตโนมัติ](/docs/user/manual/th/human-resources/auto-attendance)

ดังนั้น การรวมอุปกรณ์ไบโอเมตริกซ์ของคุณ -- หรือระบบควบคุมการเข้าออกใดๆ ที่รวบรวมเข้า/ออก-- สามารถทำได้โดยขั้นตอนต่อไปนี้:

  1. [การตั้งค่า Auto Attendance เพื่อทำเครื่องหมายการเข้าร่วมจาก Employee Checkin](#1-setting-up-auto-attendance-to-mark-attendance-from-the-employee-checkin)
  1. [การใส่บันทึก Biometric Punch ลงใน ERPNext's Employee Checkin](#2-populating-the-biometric-punch-logs-into-erpnexts-employee-checkin)

## 1. การตั้งค่าการเข้างานอัตโนมัติเพื่อทำเครื่องหมายการเข้างานจากพนักงาน

ก่อนที่คุณจะนำเข้าบันทึกการเช็คอินและเช็คเอาต์ของพนักงานเข้าสู่ระบบ ERPNext ของคุณ คุณจะต้องตั้งค่าพนักงานและกะของพนักงานก่อนจึงจะสามารถสร้างการเข้างานโดยใช้คุณสมบัติการเข้าร่วมอัตโนมัติใน ERPNext

ดูลิงก์ต่อไปนี้เพื่อตั้งค่าการเข้างานอัตโนมัติ: ตั้งค่าการเข้างานอัตโนมัติ [ตั้งค่าการเข้างานอัตโนมัติ](/docs/user/manual/th/human-resources/auto-attendance#steps-to-setup-auto-attendance)

เมื่อคุณได้ตั้งค่าพนักงานและกำหนดกะให้กับพนักงานแล้ว คุณก็พร้อมที่จะดำเนินการในขั้นตอนต่อไป

## 2. การใส่บันทึก Biometric Punch ลงใน ERPNext's Employee Checkin
ขึ้นอยู่กับระบบไบโอเมตริกซ์และคุณสมบัติของระบบ คุณสามารถนำเข้าบันทึกเข้าสู่ ERPNext ได้หลายวิธี:

1. ใช้เครื่องมือนำเข้าข้อมูลของ ERPNext:
    - วิธีแก้ปัญหาที่ง่ายที่สุด (ในแง่ของความซับซ้อนในการใช้งาน) คือการสร้าง Excel/CSV ของการเช็คอิน/เช็คเอาต์ และใช้เครื่องมือนำเข้าข้อมูลในตัวใน ERPNext เพื่อนำเข้าเอกสารการเช็คอินของพนักงานเป็นระยะ
    - โปรดดู [เอกสารประกอบเกี่ยวกับเครื่องมือนำเข้าข้อมูลของ ERPNext](/docs/user/manual/th/setting-up/data/data-import) สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการทำเช่นนี้

1. การใช้ API:
    - คุณสามารถทำให้กระบวนการนำเข้า Biometric Punch Logs เป็นไปโดยอัตโนมัติโดยผสานเข้ากับ API ที่มีอยู่ใน ERPNext
    - API นี้สามารถเข้าถึงได้ที่: `/api/method/erpnext.hr.doctype.employee_checkin.employee_checkin.add_log_based_on_employee_field`
    - วิธีนี้ต้องใช้ความรู้ด้านเทคนิค และคุณควรติดต่อผู้ติดตั้ง ERPNext หรือผู้จำหน่ายระบบไบโอเมตริกซ์ของคุณ

1. ตั้งค่า Python สคริปต์บนคอมพิวเตอร์ของคุณเพื่อรวม ZKTeco หรืออุปกรณ์ที่คล้ายกัน:
    - วิธีนี้ใช้ได้กับ ZKTeco หรืออุปกรณ์ที่คล้ายกันที่ใช้ ZKProtocol เพื่อสื่อสารผ่าน TCP/IP
    - สคริปต์นี้มีอยู่ที่: [github:frappe/push-biometric-erpnext](https://github.com/frappe/push-biometric-erpnext).
    - โปรดปฏิบัติตามคำแนะนำในหน้าสคริปต์เพื่อตั้งค่าบนคอมพิวเตอร์ของคุณ
    - สคริปต์นี้ดึงบันทึกไบโอเมตริกซ์จากอุปกรณ์ที่รองรับ และใช้ API ที่กล่าวถึงในขั้นตอนข้างต้นเพื่อส่งข้อมูลไปยัง ERPNext
