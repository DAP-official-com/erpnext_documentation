<!-- add-breadcrumbs -->
# การตั้งค่า SMS

**คุณสามารถสมัครใช้บริการ SMS เพื่อส่ง SMS ไปยังหมายเลขโทรศัพท์มือถือ**

หากต้องการรวม SMS ใน ERPNext ให้ติดต่อผู้ให้บริการเกตเวย์ SMS ที่ให้บริการ HTTP API พวกเขาจะสร้างบัญชีให้คุณและจะให้ชื่อผู้ใช้และรหัสผ่านที่ไม่ซ้ำกัน

ในการเข้าถึงการตั้งค่า SMS ไปที่:

> หน้าหลัก > การตั้งค่า > การตั้งค่า SMS

ในการกำหนดค่าการตั้งค่า SMS ใน ERPNext ให้ค้นหา HTTP API (เอกสารที่อธิบายวิธีการเข้าถึงอินเทอร์เฟซ SMS จากแอปพลิเคชันบุคคลที่สาม) ในเอกสารนี้ คุณจะได้รับ URL ที่ใช้ในการส่ง SMS โดยใช้คำขอ HTTP คุณสามารถใช้ URL นี้เพื่อกำหนดการตั้งค่า SMS ใน ERPNext

ตัวอย่าง URL เกตเวย์ SMS:
    
    http://instant.smses.com/web2sms.php?username=<USERNAME>&password;=<PASSWORD>&to;=<MOBILENUMBER>&sender;=<SENDERID>&message;=<MESSAGE>
    

<img class="screenshot" alt="SMS Setting 2" src="{{docs_base_url}}/assets/img/setup/sms-settings2.jpg">

> หมายเหตุ: สำหรับ URL เกตเวย์ของ SMS ให้รวมเฉพาะสตริงที่นำหน้า "?"

ตัวอย่าง:
    
    http://instant.smses.com/web2sms.php?username=abcd&password;=abcd&to;=9900XXXXXX&sender;
    =DEMO&message;=THIS+IS+A+TEST+SMS

URL ด้านบนจะส่ง SMS จากบัญชี abcd ไปยังหมายเลขโทรศัพท์มือถือ 9900XXXXXX โดยมี ID ผู้ส่งเป็น DEMO พร้อมข้อความว่า "THIS IS A TEST SMS"

โปรดทราบว่าพารามิเตอร์บางตัวใน URL เป็นแบบคงที่ คุณจะได้รับค่าคงที่จากผู้ให้บริการ SMS ของคุณ เช่น ชื่อผู้ใช้ รหัสผ่าน ฯลฯ ควรป้อนค่าคงที่เหล่านี้ในตาราง Static Parameters

<img class="screenshot" alt="SMS Setting" src="{{docs_base_url}}/assets/img/setup/sms-settings1.png">

### หัวข้อที่เกี่ยวข้อง 
1. [บัญชีอีเมล์](/docs/user/manual/th/setting-up/email/email-account)
1. [การแจ้งเตือน](/docs/user/manual/th/setting-up/notifications)
