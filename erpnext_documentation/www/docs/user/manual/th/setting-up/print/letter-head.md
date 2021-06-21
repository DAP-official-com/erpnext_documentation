<!-- add-breadcrumbs -->
#หัวจดหมาย

**หัวจดหมายประกอบด้วยชื่อองค์กร โลโก้ ที่อยู่ ฯลฯ ซึ่งปรากฏอยู่ที่ส่วนบนสุดในเอกสาร*

ทุกบริษัทมีหัวจดหมายเริ่มต้น โดยทั่วไปค่าหัวจดหมายเหล่านี้จะถูกตั้งค่าเป็นส่วนหัวและส่วนท้ายในเอกสาร ใน ERPNext คุณสามารถบันทึกรายละเอียดเหล่านี้ได้ใน Letter Head master

รายละเอียดเหล่านี้จะปรากฏในรูปแบบการพิมพ์ของธุรกรรม เช่น ใบสั่งขาย ใบกำกับการขาย สลิปเงินเดือน ใบสั่งซื้อ ฯลฯ ใน ERPNext หัวจดหมายใช้สำหรับตั้งค่าส่วนบนของเอกสารเท่านั้น เนื้อหาอื่น ๆ จะถูกจัดรูปแบบไว้ล่วงหน้าและ สามารถกำหนดค่าผ่านทาง [รูปแบบการพิมพ์](/docs/user/manual/en/setting-up/print/print-format) และ [การพิมพ์หัวกระดาษ](/docs/user/manual/en/setting-up/print/print-headings).

ในการเข้าถึงหัวจดหมาย ไปที่:
> หน้าหลัก > การตั้งค่า > หัวจดหมาย

## 1. วิธีสร้างหัวจดหมาย
1. ไปที่รายการหัวจดหมาย คลิก**ใหม่**
1. ป้อนชื่อหัวจดหมาย คุณสามารถสร้างหัวจดหมายแยกต่างหากสำหรับที่ตั้งสำนักงานต่างๆ
1. เลือกว่าจะอิงตามรูปภาพหรือ HTML
1. คุณสามารถป้อนรายละเอียดในหัวจดหมายโดยใช้:

  * ภาพโลโก้: คลิกที่ปุ่มแนบเพื่อแนบภาพ เมื่อแทรกรูปภาพแล้ว HTML ของรูปภาพจะถูกสร้างขึ้นโดยอัตโนมัติ
  * ข้อมูลอื่นๆ (เช่น ที่อยู่ หมายเลขประจำตัวผู้เสียภาษี ฯลฯ) ที่คุณต้องการใส่ไว้ในหัวจดหมาย

    <img class="screenshot" alt="Print Heading" src="{{docs_base_url}}/assets/img/setup/print/letter-head.png">
  
  > หากคุณต้องการกำหนดให้หัวจดหมายเริ่มต้น ให้คลิกที่ "หัวจดหมายเริ่มต้น"

1. หลังจากป้อนค่าในส่วนหัวกระดาษและท้ายกระดาษแล้ว ให้บันทึกหัวจดหมาย

คุณสามารถตั้งค่าหัวจดหมายตาม HTML เพื่อทำการเปลี่ยนแปลงได้:

![Letter Head based on](/docs/assets/img/setup/print/letter-head-based-on.gif)

นี่คือลักษณะของหัวจดหมายในการพิมพ์ของเอกสาร

<img class="screenshot" alt="Print Heading" src="{{docs_base_url}}/assets/img/setup/print/letter-head-1.png">

> โปรดทราบว่าส่วนท้ายจะปรากฏเฉพาะเมื่อเห็นการพิมพ์ของเอกสารใน PDF ส่วนท้ายจะไม่ปรากฏในตัวอย่างก่อนพิมพ์ที่ใช้ HTML

## 2. วิดีโอ
<div class="embed-container">
  <iframe src="https://www.youtube.com/embed/cKZHcx1znMc?end=58&rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen>
  </iframe>
</div>

### 3. หัวข้อที่เกี่ยวข้อง
1. [เทมเพลตที่อยู่](/docs/user/manual/en/setting-up/print/address-template)
1. [ข้อกำหนดและเงื่อนไข](/docs/user/manual/en/setting-up/print/terms-and-conditions)
1. [เทมเพลตเช็ค](/docs/user/manual/en/setting-up/print/cheque-print-template)
1. [พิมพ์หัวเรื่อง](/docs/user/manual/en/setting-up/print/print-headings)
