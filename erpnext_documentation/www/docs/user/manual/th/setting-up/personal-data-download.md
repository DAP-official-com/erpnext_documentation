<!--add breadcrumbs-->

# ดาวน์โหลดข้อมูลส่วนบุคคล

ในฐานะที่เป็นส่วนหนึ่งของการปฏิบัติตาม GDPR ERPNext มีการดาวน์โหลดข้อมูลส่วนบุคคล

เครื่องมือดาวน์โหลดข้อมูลส่วนบุคคลทำให้ผู้ใช้สามารถดาวน์โหลดข้อมูลส่วนบุคคลทั้งหมดที่สร้างขึ้นขณะใช้ ERPNext ได้โดยอัตโนมัติ ซึ่งรวมถึงข้อมูลส่วนบุคคลที่สามารถระบุตัวตนได้จากบัญชีผู้ใช้ของคุณ เช่น ชื่อผู้ใช้ ชื่อเต็ม วันเกิด หมายเลขโทรศัพท์ หมายเลขโทรศัพท์มือถือ สถานที่ ความสนใจ ประวัติ ลายเซ็นอีเมล อีเมล ผู้ติดต่อ ที่อยู่ การสื่อสาร ฯลฯ นอกจากนี้ยังรวมข้อมูลจากลูกค้าเป้าหมาย และโอกาส รายละเอียดที่คุณบันทึกไว้ เช่น หมายเลขโทรศัพท์ หมายเลขโทรศัพท์มือถือ แฟกซ์ เว็บไซต์ และชื่อ

## 1. วิธีขอดาวน์โหลดข้อมูลผู้ใช้

1. ในการเริ่มต้นดาวน์โหลดข้อมูล ผู้ใช้ต้อง **เข้าสู่ระบบ** และไปที่ [host-name]/request-data (e.g. erpnext.com/request-data)

    <img class="screenshot" alt="Request Data" src="{{docs_base_url}}/assets/img/setup/personal-data-download-request/request-data-webform.png">

2. หลังจากส่งคำขอของคุณแล้ว คุณจะได้รับคำตอบที่สำเร็จ
    <img class="screenshot" alt="Request Data" src="{{docs_base_url}}/assets/img/setup/personal-data-download-request/download-request-succes.png">

3. การดำเนินการนี้จะส่งอีเมลพร้อมลิงก์ดาวน์โหลดข้อมูลไปยังที่อยู่อีเมลที่เชื่อมโยงกับผู้ใช้
    <img class="screenshot" alt="Download Data Email" src="{{docs_base_url}}/assets/img/setup/personal-data-download-request/download-data-email.png">

ไฟล์ที่สามารถดาวน์โหลดได้จะอยู่ในรูปแบบ JSON

## 2. คำขอดาวน์โหลดข้อมูลเอกสารส่วนบุคคล

คำขอจะถูกบันทึกไว้ในเอกสาร (DocType) "คำขอดาวน์โหลดข้อมูลส่วนบุคคล" ลิงก์ไฟล์ที่ส่งไปยังผู้ใช้ทางอีเมลจะแนบมากับเอกสารด้วย ค้นหาคำขอดาวน์โหลดข้อมูลส่วนบุคคลจากแถบค้นหา

<img class="screenshot" alt="Personal Data Download Request Doctype" src="{{docs_base_url}}/assets/img/setup/personal-data-download-request/personal-data-download-request-doctype.png">

### 3. หัวข้อที่เกี่ยวข้อง
1. [การลบข้อมูลส่วนบุคคล](/docs/user/manual/en/setting-up/personal-data-deletion)
