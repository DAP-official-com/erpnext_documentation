<!-- add-breadcrumbs -->
# การอนุญาตบทบาทสำหรับเพจและรายงาน

**สามารถควบคุมการเข้าถึงเพจและรายงานต่างๆ ได้ในการอนุญาตบทบาทสำหรับเพจและรายงาน**

ประเภทเอกสาร ได้แก่ ใบสั่งขาย ลูกค้า ซัพพลายเออร์ ฯลฯ เป็น**ประเภทเอกสาร**ซึ่งหมายความว่าสามารถมี**เอกสารประเภทนั้น**ได้หลายฉบับในเอกสารประเทภเดียวกัน เช่น [ตั้งค่าในการขาย](/docs/user/manual/en/selling/selling-settings) คุณไม่สามารถสร้างการตั้งค่าการขายได้หลายรายการ แต่คุณสามารถสร้างใบสั่งขายได้หลายรายการ

ใน ERPNext ผู้ใช้สามารถสร้างส่วนติดต่อผู้ใช้กำหนดเองโดยใช้หน้าและรายงานที่กำหนดเองโดยใช้ [ตัวสร้างรายงาน](/docs/user/videos/learn/report-builder.html) หรือ [รายงานแบบสอบถาม](https://frappe.io/docs/user/en/guides/reports-and-printing/how-to-make-query-report). ERPNext มี [ระบบการอนุญาตตามบทบาท](/docs/user/manual/en/setting-up/users-and-permissions/role-based-permissions)ซึ่งคุณสามารถกำหนดบทบาทให้กับผู้ใช้ได้ สามารถกำหนดบทบาทเดียวกันให้กับเพจและรายงานเพื่อเข้าถึงได้

หากผู้ใช้เปิดใช้งานโหมดนักพัฒนาซอฟต์แวร์ พวกเขาจะสามารถเพิ่มบทบาทได้โดยตรงในเพจและเรกคอร์ดรายงาน ในกรณีดังกล่าว สิทธิ์จะปรากฏในไฟล์ JSON สำหรับหน้า/รายงานด้วย พิจารณาว่าคุณต้องการจำกัดบทบาทที่สามารถเข้าถึงบางหน้าและรายงานใน ERPNext ซึ่งสามารถทำได้ผ่านการอนุญาตบทบาทสำหรับหน้าและรายงาน

ในการเข้าถึงการอนุญาตตามบทบาทสำหรับเพจและรายงาน ให้ไปที่:

> หน้าหลัก > ผู้ใช้และการอนุญาต > การอนุญาตบทบาทสำหรับเพจและรายงาน


## 1. วิธีใช้การอนุญาตตามบทบาทสำหรับเครื่องมือหน้าและรายงาน

หากปิดใช้งานโหมดนักพัฒนาซอฟต์แวร์ ผู้ใช้สามารถกำหนดบทบาทให้กับเพจและรายงานได้โดยใช้หน้า "การอนุญาตตามบทบาทสำหรับเครื่องมือหน้าและรายงาน"

<img alt="Tools to assign custom roles to the page" class="screenshot" src="{{docs_base_url}}/assets/img/users-and-permissions/role-permission-for-page-and-report.png">

### 1.1 รีเซ็ตเป็นค่าเริ่มต้น

การใช้ปุ่ม "รีเซ็ตเป็นค่าเริ่มต้น" ผู้ใช้สามารถลบสิทธิ์ที่กำหนดเองที่ใช้กับหน้าหรือรายงาน จากนั้นการอนุญาตเริ่มต้นจะมีผลกับหน้าหรือรายงานนั้น

<img alt="Reset the default roles" class="screenshot" src="{{docs_base_url}}/assets/img/users-and-permissions/reset-roles-permission-for-page-report.png">

## การตั้งค่าการอนุญาตตามบทบาทจากเพจ/รายงานในฐานะนักพัฒนา
### การอนุญาตตามบทบาทสำหรับเพจ
1. ไปที่: หน้าแรก > ผู้พัฒนา > เพจ
1. เพิ่มแถวและเลือกบทบาทอื่นที่สามารถเข้าถึงเพจได้

    <img alt="Assign roles to the page" class="screenshot" src="{{docs_base_url}}/assets/img/users-and-permissions/roles-for-page.png">

### การอนุญาตตามบทบาทสำหรับรายงาน
1. ไปที่: หน้าแรก > ผู้พัฒนา > รายงาน
1. เพิ่มแถวที่มีบทบาทที่สามารถเข้าถึงรายงานได้

    <img alt="Assign roles to the report" class="screenshot" src="{{docs_base_url}}/assets/img/users-and-permissions/roles-for-report.png">

### 3. หัวข้อที่เกี่ยวข้อง
1. [บทบาทและโปรไฟล์บทบาท](/docs/user/manual/en/setting-up/users-and-permissions/role-and-role-profile)
1. [สิทธิ์ตามบทบาท](/docs/user/manual/en/setting-up/users-and-permissions/role-based-permissions)
1. [สิทธิ์ของผู้ใช้](/docs/user/manual/en/setting-up/users-and-permissions/user-permissions)
