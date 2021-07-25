<!-- add-breadcrumbs -->

# การใช้ร่วมกับ Exotel

การรวมนี้ทำให้คุณสามารถรวม Exotel เข้ากับบัญชี ERPNext ของคุณได้ ลูกค้าเป้าหมายและหมายเลขโทรศัพท์ที่บันทึกผ่าน Exotel สามารถบันทึกลงใน ERPNext ของคุณได้โดยตรง

## 1. คุณสมบัติ

- ติดตามสายเรียกเข้าในบัญชี ERPNext ของคุณ
- แสดงป๊อปอัปข้อมูลลูกค้าเป้าหมาย/ลูกค้าที่มีอยู่แก่พนักงานเมื่อได้รับสายเรียกเข้า

## 2. วิธีการตั้งค่า

### 2.1 ตั้งค่าบัญชี Exotel ของคุณ

- เข้าสู่ระบบบัญชี Exotel ของคุณและไปที่ App Bazar
- สร้างแอพใหม่สำหรับโฟลว์ใหม่
- ตั้งค่าโฟลว์ตามที่คุณต้องการ
- ใน API การเชื่อมต่อของคุณภายใต้ "สร้างป๊อปอัป..." และวาง URL ต่อไปนี้:
`https://<ไซต์ของคุณ>/api/method/erpnext.erpnext_integrations.exotel_integration.handle_incoming_call`

![Connect Applet](/docs/assets/img/erpnext_integrations/exotel_integration/connect_applet.png)
![Call Popup Section](/docs/assets/img/erpnext_integrations/exotel_integration/create_popup_section.png)

> **หมายเหตุ:** แทนที่ `<your-site>` ใน URL ด้วยชื่อไซต์ของคุณ ตัวอย่างเช่น หากชื่อไซต์คือ **frappe.erpnext.com** ดังนั้น URL จะเป็น:
`https://frappe.erpnext.com/api/method/erpnext.erpnext_integrations.exotel_integration.handle_incoming_call`

- หลังจากนั้นเพิ่มแอปเพล็ต Passthru ภายใต้ "หลังจากการสนทนาการโทรสิ้นสุด" และวาง URL ต่อไปนี้:
`https://<ไซต์ของคุณ>/api/method/erpnext.erpnext_integrations.exotel_integration.handle_end_call`

![After Conversation Ends Section](/docs/assets/img/erpnext_integrations/exotel_integration/after_conversation_ends_section.png)

![After call ends section](/docs/assets/img/erpnext_integrations/exotel_integration/passthru_end_call.png)

> **หมายเหตุ:** อย่าลืมทำเครื่องหมายที่ "Make Passthru Async"

- คล้ายกัน เพิ่มแอปเพล็ต Passthru ในส่วน "ถ้าไม่มีใครตอบ..." และวาง URL ต่อไปนี้:
`https://<ไซต์ของคุณ>/api/method/erpnext.erpnext_integrations.exotel_integration.handle_missed_call`

![No Response Section](/docs/assets/img/erpnext_integrations/exotel_integration/no_response.png)

![After call ends section](/docs/assets/img/erpnext_integrations/exotel_integration/passthru_missed_call.png)

> **หมายเหตุ:** อย่าลืมทำเครื่องหมายที่ "Make Passthru Async"

- บันทึกการไหล
- ตอนนี้กำหนดแอพที่สร้างขึ้นใหม่นี้ให้กับ ExoPhone ของคุณซึ่งคุณได้รับสายธุรกิจของคุณ

### 2.2 การตั้งค่าใน ERPNext

- จาก Awesome Bar ให้ไปที่ 'การตั้งค่า Exotel'
- ตั้งค่า "Exotel SID" และ "Exotel Token" ของคุณ คุณสามารถค้นหาคีย์ Exotel API และโทเค็นได้ใน [แดชบอร์ด Exotel](https://my.exotel.com/apisettings/site#api-credentials)
- ไปที่สื่อการสื่อสาร
- เพิ่ม ExoPhone ของคุณและกำหนดเวลาหมายเลขนั้น ตามกำหนดการนี้ พนักงานจะได้รับป๊อปอัป
