---
title: LinkedIn Settings
add_breadcrumbs: 1
show_sidebar: 0

metatags:
 description: LinkedIn Settings for Social Media Post
 keywords: Social Media Post Scheduling, CRM, frappe, erpnext new features, erp, open source erp, free erp, security
---

# การตั้งค่า LinkedIn

การตั้งค่าที่เกี่ยวข้องกับ LinkedIn เช่น OAuth สามารถกำหนดค่าได้ที่นี่ ERPNext ต้องการสิทธิ์เข้าถึง API ซึ่งโพสต์นั้นถูกแชร์และบรรลุโดยใช้ OAuth 2.0 Authentication Protocol

## 1. วิธีตั้งค่าแอพ LinkedIn Developer

คุณต้องมีแอพ LinkedIn Developer สำหรับบริษัทของคุณ ERPNext โต้ตอบกับแอพนี้เพื่อแชร์โพสต์

### 1.1 สร้างแอปนักพัฒนา LinkedIn

สร้างแอพตามลิงค์ `https://www.linkedin.com/developers` กรอกรายละเอียดทั้งหมดและตรวจสอบ และแอพนั้นมีผลิตภัณฑ์ดังต่อไปนี้

1. แบ่งปันบน LinkedIn
2. ลงชื่อเข้าใช้ด้วย LinkedIn
3. แพลตฟอร์มนักพัฒนาการตลาด
![LinkedIn Developer App Product](/docs/assets/img/crm/linkedin-dev-products.png)

### 1.2 กำหนดค่า URL เปลี่ยนเส้นทาง:

1. ไปที่แอพ LinkedIn Developers จากนั้นไปที่แท็บ **รับรองความถูกต้อง**
2. ในส่วน **การตั้งค่า OAuth 2.0** เพิ่ม **URL เปลี่ยนเส้นทาง**:
`https://{ไซต์ของคุณ}/api/method/erpnext.crm.doctype.linkedin_settings.linkedin_settings.callback`
3. คลิก **อัปเดต** เพื่อทำการเปลี่ยนแปลง 
![LinkedIn Redirect URL](/docs/assets/img/crm/linkedin-redirect-urls.png)

## 2 วิธีการตั้งค่า LinkedIn

ในการเข้าถึงการตั้งค่า LinkedIn ไปที่:
> หน้าแรก > CRM > การตั้งค่า > การตั้งค่า LinkedIn

![LinkedIn Settings](/docs/assets/img/crm/linkedin-settings.png)

### รหัสบริษัท
คุณได้รับรหัสบริษัทจาก URL บริษัท LinkedIn ของคุณ
![LinkedIn Company ID](/docs/assets/img/crm/linkedin-company-id.png)

### รหัสผู้บริโภคและความลับของผู้บริโภค
คุณได้รับ **รหัสผู้บริโภค** และ **ความลับผู้บริโภค** จากบัญชีนักพัฒนา LinkedIn ของคุณ ไปที่:
> `https://www.linkedin.com/developers/` > แอปของฉัน > `{แอปของคุณ}` > การตรวจสอบสิทธิ์

![LinkedIn Client](/docs/assets/img/crm/linkedin-client.png)

เมื่อคุณบันทึกเอกสารโดยกรอก **รหัสบริษัท**, **รหัสผู้บริโภค** และ **ความลับของผู้บริโภค** เอกสารนั้นจะเปลี่ยนเส้นทางไปยังหน้าลงชื่อเข้าใช้ของ LinkedIn โดยให้ข้อมูลประจำตัว LinkedIn ที่ถูกต้องและคลิกอนุญาต สมาชิกจะอนุมัติ คำขอของแอปพลิเคชันในการเข้าถึงข้อมูลสมาชิกและโต้ตอบกับ LinkedIn ในนามของพวกเขา
![Authorize LinkedIn](/docs/assets/img/crm/authorize-linkedin.jpg)

{next}