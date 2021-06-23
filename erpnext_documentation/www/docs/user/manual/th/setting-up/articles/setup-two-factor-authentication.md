<!-- add-breadcrumbs -->
#ตั้งค่าการตรวจสอบสิทธิ์สองปัจจัย (Two Factor Authentication/2FA)

##เปิดใช้งานการตรวจสอบสิทธิ์แบบสองปัจจัย (2FA)

เปิดใช้งานการพิสูจน์ตัวตนแบบสองปัจจัยโดยรันคำสั่ง

`bench --site [sitename] set-config enable_two_factor_auth true` 

ระบุสิ่งต่อไปนี้ในการตั้งค่าระบบ

* วิธีการตรวจสอบ OTP (แอป OTP = TOTP โดยใช้ Soft หรือ Hard Token ในขณะที่ Email/SMS = HOTP โดยใช้ Email หรือ SMS
* เวลาหมดอายุของ QR Code บนเซิร์ฟเวอร์หากระบุ OTP App ไว้
* ชื่อผู้ออก OTP

<img alt="Enable Two Factor Auth" class="screenshot" src="{{docs_base_url}}/assets/img/articles/twofactor/twofactor-1.png">


เมื่อเปิดใช้งาน 2FA จากการตั้งค่า จะเปิดใช้งานสำหรับบทบาท "ทั้งหมด" ด้วย ด้วยวิธีนี้ ผู้ใช้ทั้งหมดรวมถึงผู้ดูแลระบบจะต้องดำเนินการตรวจสอบสิทธิ์ระดับที่ 2 ด้วยโทเค็น การยกเลิกการเลือกช่องทำเครื่องหมาย "การตรวจสอบสิทธิ์สองปัจจัย" ในบทบาท "ทั้งหมด" และเปิดใช้งานในบทบาทอื่น ความจำเป็นในการเข้าสู่ระบบด้วยโทเค็นสามารถจำกัดเฉพาะบทบาทเฉพาะได้ 2FA ใช้ไม่ได้กับการเข้าสู่ระบบโดยผู้ใช้เว็บและการเข้าสู่ระบบ API

<img alt="Role Enable Two Factor Auth" class="screenshot" src="{{docs_base_url}}/assets/img/articles/twofactor/twofactor-2.png">

หากใช้การตรวจสอบสิทธิ์ SMS โปรดตรวจสอบให้แน่ใจว่าการตั้งค่า SMS ของคุณอัปเดตแล้ว

<img alt="SMS Settings" class="screenshot" src="{{docs_base_url}}/assets/img/articles/twofactor/twofactor-3.png">

หากใช้อีเมล ตรวจสอบให้แน่ใจว่าการตั้งค่าบัญชีอีเมลขาออกของคุณได้รับการอัปเดตแล้ว

<img alt="Email Settings" class="screenshot" src="{{docs_base_url}}/assets/img/articles/twofactor/twofactor-4.png">

เมื่อผู้ใช้ใหม่พยายามเข้าสู่ระบบเป็นครั้งแรกในระบบที่เปิดใช้งานการตรวจสอบสิทธิ์แบบสองปัจจัยและมีตัวเลือกการตรวจสอบสิทธิ์เป็นแอป OTP อีเมลจะถูกส่งที่มีลิงก์ไปยังรหัส QR

<img alt="Email Notify Two Factor" class="screenshot" src="{{docs_base_url}}/assets/img/articles/twofactor/twofactor-5.png">
<img alt="QR Code Page" class="screenshot" src="{{docs_base_url}}/assets/img/articles/twofactor/twofactor-6.png">

การสแกนรหัส QR ด้วยแอปตรวจสอบสิทธิ์ เช่น Google Authenticator จะลงทะเบียนการเข้าถึงของผู้ใช้ และเริ่มสร้างโทเค็นที่สามารถใช้เข้าสู่ระบบได้โดยอัตโนมัติ

<img alt="Two Factor Scan App" class="screenshot" src="{{docs_base_url}}/assets/img/articles/twofactor/twofactor_app.jpeg">

หากใช้อีเมล/SMS เป็นวิธีการตรวจสอบสิทธิ์ คุณจะได้รับการแจ้งเตือนด้วย

<img alt="Email and SMS" class="screenshot" src="{{docs_base_url}}/assets/img/articles/twofactor/twofactor-8.png">
