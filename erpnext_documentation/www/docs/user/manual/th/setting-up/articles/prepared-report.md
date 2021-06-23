---
title: การใช้รายงานที่เตรียมไว้
add_breadcrumbs: 1
show_sidebar: 0

metatags:
 description: ERPNext allows report generation in the background so users can continue with their usual tasks while the report is being generated for them.
 keywords: frappe, erpnext, erpnext reports, mis, prepared report, background reports
---

<!-- add-breadcrumbs -->
# Using Prepared Report

หลายครั้งเมื่อมีการสร้างรายงานที่เกี่ยวข้องกับปริมาณข้อมูลขนาดใหญ่กล่าวว่ามีรายงาน GL ตลอดทั้งปีคุณอาจจะจบลงได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: **การร้องขอหมดเวลา (Request Timeout)** สิ่งนี้เกิดขึ้นเนื่องจากมีข้อมูลจำนวนมากที่ต้องประมวลผลและนำเสนอในหน้ารายงาน แต่มีทรัพยากรเซิร์ฟเวอร์ไม่เพียงพอจึงส่งผลให้หมดเวลา

สำหรับการประมวลผลรายงานดังกล่าวได้ดียิ่งขึ้น ERPNext ขอเสนอรายงานที่เตรียมไว้ (ตั้งแต่เวอร์ชัน 11) เมื่อตั้งค่ารายงานเป็นรายงานที่เตรียมไว้ รายงานจะถูกสร้างขึ้นผ่าน [านเบื้องหลัง](https://frappe.io/docs/user/en/guides/app-development/running-background-jobs) และเมื่อพร้อมแล้ว ผู้ใช้จะสามารถดูได้

## ขั้นตอนในการตั้งค่ารายงานที่เตรียมไว้

1. ไปที่ [บทบาทการอนุญาตให้หน้าและรายงาน](/docs/user/manual/en/setting-up/users-and-permissions/role-permission-for-page-and-report).
1. ในฟิลด์ 'ตั้งบทบาท' เลือก **รายงาน**
1. ในฟิลด์ 'รายงาน' ให้เลือกรายงานที่คุณต้องการเปิด/ปิดใช้งานรายงานที่เตรียมไว้
1. ใช้ช่องทำเครื่องหมาย **ปิดใช้งานรายงานที่เตรียมไว้** เพื่อเปิด/ปิดใช้งานรายงานที่เตรียมไว้ หากเลือกตัวเลือกนี้ ตัวเลือกรายงานที่เตรียมไว้จะถูกปิดใช้งานสำหรับรายงานที่เลือก
1. คลิกที่**อัปเดท**

<img alt="Setup Prepared Report" class="screenshot" src="{{docs_base_url}}/assets/img/articles/set-prep-report.gif">

## วิธีใช้รายงานที่เตรียมไว้

1. เปิดรายงานดังกล่าว (พูดบัญชีแยกประเภททั่วไป) และใช้ตัวกรองทั้งหมดที่จำเป็น
1. หากเปิดใช้งานตัวเลือกรายงานที่เตรียมไว้สำหรับรายงานนั้น คุณจะเห็นปุ่ม **สร้างรายงาน** 
    <img alt="Generate Prepared Report" class="screenshot" src="{{docs_base_url}}/assets/img/articles/prepared-report-generate.png">
1. จะเห็นการแจ้งเตือนที่ด้านล่างขวาของหน้าจอว่า "เริ่มรายงานแล้ว คุณสามารถติดตามสถานะได้ที่นี่ "
    <img alt="Prepared Report Initiated" class="screenshot" src="{{docs_base_url}}/assets/img/articles/prepared-report-bg.png">
1. คุณสามารถรอบนหน้าจอดังกล่าวหรือคลิกที่นี่ในข้อความด้านบนเพื่อเปิดหน้าสำหรับรายงาน การดำเนินการนี้จะเปิดหน้าใหม่สำหรับรายงาน:
    <img alt="Prepared Report Queued" class="screenshot" src="{{docs_base_url}}/assets/img/articles/prepared-report-queued.png">
    หน้ารายงานมีสถานะเป็น **"อยู่ในคิว"** เมื่อรายงานพร้อมแล้ว คุณจะเห็นปุ่มแสดงรายงานซึ่งคุณสามารถคลิกเพื่อดูรายงานได้
     <img alt="Prepared Report Initiated" class="screenshot" src="{{docs_base_url}}/assets/img/articles/prepared-report-page.png">
1. เนื่องจากรายงานที่เตรียมไว้นั้นเป็นประเภทเอกสารเช่นกัน ในการดูรายการรายงานที่เตรียมไว้ คุณสามารถใช้ [ัดการบทบาทและหน้าที่](/docs/user/manual/en/setting-up/users-and-permissions/role-based-permissions) เพื่อให้สิทธิ์เข้าถึงได้