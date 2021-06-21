<!--add breadcrumbs-->

# การลบข้อมูลส่วนบุคคล

ในฐานะที่เป็นส่วนหนึ่งของการปฏิบัติตาม GDPR ERPNext มีการลบข้อมูลส่วนบุคคล

เครื่องมือลบข้อมูลส่วนบุคคลช่วยให้ผู้ใช้สามารถระบุข้อมูลส่วนบุคคลที่สามารถระบุตัวตนได้ทั้งหมดที่ผู้ใช้สร้างขึ้นขณะใช้ ERPNext กล่าวคือ ข้อมูลส่วนบุคคลที่สามารถระบุตัวตนได้จะถูกสุ่ม ซึ่งรวมถึงข้อมูลส่วนบุคคลที่สามารถระบุตัวตนได้จากบัญชีผู้ใช้ของคุณ เช่น ชื่อผู้ใช้ ชื่อเต็ม วันเกิด หมายเลขโทรศัพท์ หมายเลขโทรศัพท์มือถือ สถานที่ ความสนใจ ประวัติ ลายเซ็นอีเมล อีเมล ผู้ติดต่อ ที่อยู่ การสื่อสาร ฯลฯ นอกจากนี้ยังรวมข้อมูลจากลูกค้าเป้าหมาย และโอกาส รายละเอียดที่คุณบันทึกไว้ เช่น หมายเลขโทรศัพท์ หมายเลขโทรศัพท์มือถือ แฟกซ์ เว็บไซต์ และชื่อ

อย่างไรก็ตาม ข้อมูลนี้ไม่รวมข้อมูลที่กฎหมายกำหนดให้ต้องดูแลโดยธุรกิจ

## 1. วิธีการขอลบข้อมูลผู้ใช้

1. ในการเริ่มต้นลบข้อมูลส่วนบุคคลที่สามารถระบุตัวตนได้ คุณต้องไปที่ [host-name]/request-to-delete-data เช่น example.erpnext.com/request-to-delete-data)

    <img class="screenshot" alt="Request Data Webform" src="{{docs_base_url}}/assets/img/setup/personal-data-deletion-request/request-to-delete-data-webform.png">

2. ป้อนอีเมลที่เชื่อมโยงกับบัญชี ERPNext ของคุณ หลังจากส่งคำขอของคุณแล้ว คุณจะได้รับคำตอบที่สำเร็จ

    <img class="screenshot" alt="Deletion Request Success" src="{{docs_base_url}}/assets/img/setup/personal-data-deletion-request/deletion-request-success.png">

3. การดำเนินการนี้จะส่งอีเมลพร้อมลิงก์ยืนยันเพื่อลบข้อมูลไปยังที่อยู่อีเมลที่เชื่อมโยงกับผู้ใช้

    <img class="screenshot" alt="Verification Email" src="{{docs_base_url}}/assets/img/setup/personal-data-deletion-request/verification-email.png">

4. เมื่อผู้ใช้คลิกที่ลิงค์ยืนยัน ข้อความยืนยันจะปรากฏขึ้น
    <img class="screenshot" alt="Confirmed Verification" src="{{docs_base_url}}/assets/img/setup/personal-data-deletion-request/confirmed-verification.png">

## 2. วิธีลบข้อมูลส่วนตัวของผู้ใช้

คำขอลบข้อมูลจะถูกบันทึกไว้ในประเภทเอกสาร "คำขอลบข้อมูลส่วนบุคคล"

<img class="screenshot" alt="Personal Data Download Request Doctype" src="{{docs_base_url}}/assets/img/setup/personal-data-deletion-request/personal-data-deletion-request-doctype.png">

เอกสารประเภทนี้จะรักษาสถานะสามสถานะเพื่อให้กระบวนการลบข้อมูลผู้ใช้เสร็จสมบูรณ์

### 2.1 อยู่ระหว่างการตรวจสอบ

สถานะนี้บ่งชี้ว่าผู้ใช้ได้ร้องขอให้ลบข้อมูลผ่านทางเว็บฟอร์ม อย่างไรก็ตาม การตรวจสอบคำขอนี้ยังคงรอดำเนินการอยู่ ค้นหาคำขอลบข้อมูลส่วนบุคคลจากแถบค้นหา

<img class="screenshot" alt="Pending Verification" src="{{docs_base_url}}/assets/img/setup/personal-data-deletion-request/pending-verification.png">

### 2.2 รอการอนุมัติ

แสดงว่าผู้ใช้ได้ตรวจสอบคำขอผ่านทางอีเมลแล้ว เปิดใช้งานตัวเลือก "ลบข้อมูล" สำหรับผู้จัดการระบบ

<img class="screenshot" alt="Pending Approval" src="{{docs_base_url}}/assets/img/setup/personal-data-deletion-request/pending-approval.png">

### 2.3 ลบ
นี่แสดงว่าตัวจัดการระบบได้คลิกที่ปุ่ม "ลบข้อมูล" ซึ่งหมายความว่าข้อมูลส่วนบุคคลที่ระบุตัวบุคคลนั้นได้ของผู้ใช้นั้นไม่ระบุชื่อ

<img class="screenshot" alt="Deleted User" src="{{docs_base_url}}/assets/img/setup/personal-data-deletion-request/deleted-user.png">

### 3. หัวข้อที่เกี่ยวข้อง
1. [ดาวน์โหลดข้อมูลส่วนบุคคล](/docs/user/manual/en/setting-up/personal-data-download)

