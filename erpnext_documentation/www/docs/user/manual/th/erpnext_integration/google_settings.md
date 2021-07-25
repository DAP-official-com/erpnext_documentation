<!-- add-breadcrumbs -->
# การตั้งค่า Google

ในการเปิดใช้งาน Google Integrations ERPNext จำเป็นต้องเข้าถึง API ซึ่งข้อมูลจะถูกซิงค์ซึ่งทำได้โดยใช้ OAuth 2.0 Authentication Protocol

## วิธีตั้งค่า Google Settings

### สำหรับ Google ปฏิทิน, Google Contacts, Google Drive

เพื่อให้สามารถซิงโครไนซ์กับ Google ปฏิทิน, Google Contacts หรือ Google Drive คุณต้องอนุญาต ERPNext เพื่อรับข้อมูลจาก Google ต่อไปนี้เป็นตัวอย่างการตั้งค่า Google Contacts Integration

1. สร้างโครงการใหม่บน Google Cloud Platform และสร้างข้อมูลรับรอง OAuth 2.0 ใหม่
<img class="screenshot" src="/docs/assets/img/erpnext_integrations/google_contacts_project_creation.gif">
- เปิดใช้งานการเข้าถึง API ในไลบรารี API สำหรับการรวมที่คุณต้องการรวมเข้าด้วยกัน
  - Google ปฏิทิน: **API ของปฏิทิน**
  - Google Contacts: ** People API **
  - Google ไดรฟ์: ** API ของไดรฟ์**

 <img class="screenshot" src="/docs/assets/img/erpnext_integrations/api.gif">
- ใน **API & Services > Credentials** ให้สร้าง Credential ใหม่และเลือก **Create OAuth client ID**
- เลือกประเภทแอปพลิเคชัน **เว็บแอปพลิเคชัน**
- เพิ่ม `https://{yoursite}` ไปยังต้นทาง JavaScript ที่ได้รับอนุญาต
- เพิ่ม `https://{yoursite}?cmd=frappe.integrations.doctype.{integration_name}{integration_name}.google_callback` เป็น URI การเปลี่ยนเส้นทางที่ได้รับอนุญาต
  - คุณต้องแทนที่ "integration_name" ด้วยหนึ่งในรายการต่อไปนี้:
     - Google ปฏิทิน: **google\_calendar**
     - Google Contacts: **google\_contacts**
     - Google ไดรฟ์: **google\_drive**
  - เช่น: สำหรับ Google Contacts URL จะเป็น `https://{yoursite}?cmd=frappe.integrations.doctype.google_contacts.google_contacts.google_callback`

 <img class="screenshot" src="/docs/assets/img/erpnext_integrations/google_contacts_oauth.gif">
- เพิ่ม Client ID และ Client Secret ในการตั้งค่า Google ใน **หน้าแรก > การรวมระบบ > บริการของ Google > การตั้งค่า Google**

### สำหรับ Google Maps

เพื่อให้สามารถซิงโครไนซ์กับ Google Maps ได้ คุณต้องสร้างคีย์ API เนื่องจาก Google Maps ไม่จำเป็นต้องเข้าถึงข้อมูลจาก Google

1. สร้างโครงการใหม่บน Google Cloud Platform และสร้างคีย์ API ใหม่
- เปิดใช้งานการเข้าถึง API ในไลบรารี API สำหรับเส้นทาง API จากนั้นเพิ่มคีย์ API ในการตั้งค่า Google ใน **หน้าแรก > การรวมระบบ > บริการของ Google > การตั้งค่า Google**
<img class="screenshot" src="/docs/assets/img/erpnext_integrations/api_key.gif">
