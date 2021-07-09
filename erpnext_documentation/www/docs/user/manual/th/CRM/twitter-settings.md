---
title: Twitter Settings
add_breadcrumbs: 1
show_sidebar: 0

metatags:
 description: Twitter Settings for Social Media Post
 keywords: Social Media Post Scheduling, CRM, frappe, erpnext new features, erp, open source erp, free erp, security
---

# การตั้งค่า Twitter

คุณสามารถกำหนดค่าการตั้งค่าที่เกี่ยวข้องกับ Twitter เช่น OAuth ได้ที่นี่ ERPNext ต้องการสิทธิ์เข้าถึง API ซึ่งโพสต์นั้นถูกแชร์และบรรลุโดยใช้ OAuth 2.0 Authentication Protocol

## 1. วิธีตั้งค่า Twitter App

คุณต้องมีแอพ Twitter สำหรับบริษัทของคุณ ERPNext โต้ตอบกับแอพนี้เพื่อแชร์ทวีต

### 1.1 สร้างแอพ Twitter Developer

สร้างแอปโดยลิงก์ `https://developer.twitter.com/' และตรวจสอบว่าแอปนั้นมีสิทธิ์การเข้าถึง **อ่านและเขียน**
![Twitter App Permission](/docs/assets/img/crm/twitter-app-permission.png)

### 1.2. กำหนดค่า Callback URL
1. เลือกแอพของคุณและไปที่ **รายละเอียดแอพ**
2. จากนั้นไปที่ **แก้ไข** และคลิก **แก้ไขรายละเอียด**
3. เพิ่ม URL เว็บไซต์ของคุณใน **URL โทรกลับ** เช่น:
`https://{ไซต์ของคุณ}/api/method/erpnext.crm.doctype.twitter_settings.twitter_settings.callback`
4. คลิก **บันทึก** เพื่อทำการเปลี่ยนแปลง

![Twitter App Callback URL](/docs/assets/img/crm/twitter-callback-url.png)


## 2. วิธีการตั้งค่า Twitter 

ในการเข้าถึงการตั้งค่า Twitter ไปที่:
> หน้าแรก > CRM > การตั้งค่า > การตั้งค่า Twitter

![Twitter Settings](/docs/assets/img/crm/twitter-settings.png)

### 2.1 คีย์ API และรหัสลับของ API

คุณได้รับ **API Key** และ **API Key Secret** จากบัญชีนักพัฒนา Twitter ของคุณ ไปที่:
> `https://developer.twitter.com/` > My Apps > `{Your App}` > Keys and tokens

![Twitter Keys Tokens](/docs/assets/img/crm/twitter-key-token.png)

เมื่อคุณบันทึกเอกสารโดยกรอก **รหัส API** และ **รหัสลับของ API** เอกสารจะเปลี่ยนเส้นทางไปยังหน้าลงชื่อเข้าใช้ของ Twitter โดยระบุข้อมูลประจำตัว Twitter ที่ถูกต้องและคลิก **อนุญาตแอป** สมาชิกจะอนุมัติคำขอแอปพลิเคชันของคุณ เพื่อเข้าถึงข้อมูลสมาชิกและโต้ตอบกับ Twitter
![Twitter Authorize App](/docs/assets/img/crm/twitter-authorize-app.png)

{next}