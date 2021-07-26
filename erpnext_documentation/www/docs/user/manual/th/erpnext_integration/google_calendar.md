<!-- add-breadcrumbs -->
# การใช้ ปฏิทิน Google 

ERPNext ให้การผสานรวมกับ ปฏิทิน Google  เพื่อให้ผู้ใช้ทุกคนสามารถซิงโครไนซ์กิจกรรมในปฏิทินของ Google กับ ERPNext


## วิธีตั้งค่าการใช้ ปฏิทิน Google 

เพื่อให้สามารถซิงโครไนซ์กับ Google ปฏิทินได้ คุณต้องให้สิทธิ์ ERPNext เพื่อรับข้อมูลกิจกรรมในปฏิทินจาก Google การรวม Google ปฏิทินได้รับการตั้งค่าตามขั้นตอนต่อไปนี้:

- สร้างข้อมูลรับรอง OAuth 2.0 ผ่าน [การตั้งค่า Google](/docs/user/manual/th/erpnext_integration/google_settings)
- ในรายการ Google ปฏิทิน ให้คลิกใหม่ ป้อนชื่อปฏิทินและผู้ใช้ที่คุณต้องการซิงค์แล้วบันทึก
- ขึ้นอยู่กับว่าคุณต้องการซิงค์ข้อมูลใด คุณสามารถเลือกติดตามได้
  - ดึงจาก Google ปฏิทิน - ซิงค์กิจกรรมทั้งหมดจาก Google ปฏิทินไปยัง ERPNext
  - พุชไปที่ Google ปฏิทิน - ซิงค์กิจกรรมทั้งหมดจาก ERPNext ไปยัง Google ปฏิทิน
- ตอนนี้คลิกที่ **อนุญาตการเข้าถึงปฏิทิน** เพื่ออนุญาต ERPNext เพื่อรับข้อมูลกิจกรรมในปฏิทินจาก Google
- เมื่อได้รับอนุญาตแล้ว คุณสามารถซิงค์ Google Calendar Event ด้วยตนเองหรือให้ ERPNext ซิงค์ Google Contacts ทุกวัน

## วิธีใช้ ปฏิทิน Google 

### การสร้างกิจกรรมใน ERPNext
- เมื่อการผสานรวม Google ปฏิทินสำเร็จ กิจกรรมทั้งหมดที่สร้างใน ERPNext จะถูกซิงค์หากเลือก "พุชไปที่ Google ปฏิทิน"
- การสร้างกิจกรรมใน ERPNext
  <img class="screenshot" src="/docs/assets/img/erpnext_integrations/erpnext-gc.gif">
- การลบกิจกรรมใน ERPNext
  <img class="screenshot" src="/docs/assets/img/erpnext_integrations/gc-erpnext.gif">

### กำลังซิงค์กิจกรรมจาก ปฏิทิน Google
- เมื่อการผสานรวม ปฏิทิน Google สำเร็จ กิจกรรมทั้งหมดใน ปฏิทิน Google จะถูกซิงค์หากเลือก "ดึงจาก ปฏิทิน Google"
- ซิงค์กิจกรรมจาก ปฏิทิน Google กับ ERPNext
  <img class="screenshot" src="/docs/assets/img/erpnext_integrations/gc-sync.gif">
