<!-- add-breadcrumbs -->
# การรวม Google Contacts

ERPNext ให้การผสานรวมกับ Google Contacts เพื่อให้ผู้ใช้ทั้งหมดซิงโครไนซ์ Google Contacts กับ ERPNext

## วิธีตั้งค่าการใช้ Google Contacts
เพื่อให้สามารถซิงโครไนซ์กับ Google Contacts ได้ คุณต้องอนุญาต ERPNext เพื่อรับข้อมูล Contacts จาก Google การรวม Google Contacts ถูกตั้งค่าด้วยขั้นตอนต่อไปนี้:

- สร้างข้อมูลรับรอง OAuth 2.0 ผ่าน [การตั้งค่า Google](/docs/user/manual/th/erpnext_integration/google_settings)
- ในรายการ Google Contacts ให้คลิกใหม่ ป้อนอีเมลบัญชี Google ที่คุณต้องการซิงค์แล้วบันทึก ตอนนี้คลิกที่ **อนุญาตการเข้าถึงผู้ติดต่อ** เพื่ออนุญาต ERPNext เพื่อรับข้อมูลผู้ติดต่อจาก Google

## วิธีใช้ Google Contacts

### การสร้างผู้ติดต่อใน ERPNext
- เมื่อการรวม Google Contacts สำเร็จ ผู้ติดต่อทั้งหมดที่สร้างใน ERPNext จะถูกซิงค์หากเลือก 'Push to Google Contacts'

การสร้างผู้ติดต่อใน ERPNext:
<img class="screenshot" src="/docs/assets/img/erpnext_integrations/google_contacts_create_contact.gif">

จะแสดงใน Google Contacts:
<img class="screenshot" src="/docs/assets/img/erpnext_integrations/google_contacts_create_contact_!.gif">
### ซิงค์ผู้ติดต่อจาก Google Contacts
- เมื่อการรวม Google Contacts สำเร็จ ผู้ติดต่อทั้งหมดใน Google Contacts จะถูกซิงค์หากเลือก "ดึงจาก Google Contacts"
  <img class="screenshot" src="/docs/assets/img/erpnext_integrations/google_contacts_contact_sync.gif">
