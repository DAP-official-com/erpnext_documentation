<!-- add-breadcrumbs -->
# ดาวน์โหลดข้อมูลสำรอง

ใน ERPNext คุณสามารถดาวน์โหลดการสำรองฐานข้อมูลด้วยตนเอง 

หากต้องการรับการสำรองฐานข้อมูลล่าสุด ให้ไปที่

> หน้าแรก > การตั้งค่า > ดาวน์โหลดข้อมูลสำรอง

ข้อมูลสำรองที่มีให้ดาวน์โหลดจะอัปเดตทุก ๆ แปดชั่วโมง คลิกที่ลิงค์เพื่อดาวน์โหลดข้อมูลสำรองในเวลาที่กำหนด

<img class="screenshot" alt="Download Backup" src="{{docs_base_url}}/assets/img/articles/download-backup-1.png">

โดยค่าเริ่มต้น ข้อมูลสำรองล่าสุดสามรายการจะพร้อมให้ดาวน์โหลด หากต้องการเปลี่ยนแปลง ให้คลิกที่ "ตั้งค่าจำนวนการสำรองข้อมูล" การดำเนินการนี้จะนำคุณไปยังการตั้งค่าระบบ ซึ่งคุณสามารถตั้งค่าจำนวนข้อมูลสำรองที่สามารถดาวน์โหลดได้ในแต่ละครั้ง

<img class="screenshot" alt="Download Backup" src="{{docs_base_url}}/assets/img/articles/download-backup-2.png">

## ดาวน์โหลดไฟล์สำรอง

การคลิกที่ดาวน์โหลดไฟล์สำรองจะส่งอีเมลพร้อมลิงก์ไปยังไฟล์สำรองสำหรับไฟล์ส่วนตัวและสาธารณะ ต้องกำหนดค่า[อีเมล](/docs/user/manual/en/setting-up/email) เพื่อให้ใช้งานได้

<img class="screenshot" alt="Download Backup" src="{{docs_base_url}}/assets/img/articles/download-backup-files.png">

## การสำรองข้อมูลอัตโนมัติไปยัง Cloud Storage

คุณยังสามารถทำให้การสำรองข้อมูลของคุณเป็นแบบอัตโนมัติเพื่ออัปโหลดโดยตรงบนแพลตฟอร์มที่เก็บข้อมูลบนคลาวด์ ปัจจุบัน ERPNext รองรับ:

1. Amazon S3
1. [Dropbox](/docs/user/manual/en/erpnext_integration/dropbox-backup)
1. [Google Drive](/docs/user/manual/en/erpnext_integration/google_drive)



