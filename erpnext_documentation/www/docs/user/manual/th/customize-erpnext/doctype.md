<!-- add-breadcrumbs -->
# DocType (เอกสาร)

**DocType เป็นส่วนประกอบหลักของแอปพลิเคชันใดๆ ที่ใช้ Frappe Framework**

อธิบายรูปแบบและมุมมองของข้อมูลของคุณ ประกอบด้วยเขตข้อมูลใดบ้างที่จัดเก็บไว้สำหรับข้อมูลของคุณ และมีลักษณะการทำงานระหว่างกันอย่างไร ประกอบด้วยข้อมูลเกี่ยวกับวิธีการตั้งชื่อข้อมูลของคุณ แบบฟอร์มต่างๆ เช่น ใบสั่งขาย ใบแจ้งหนี้การขาย ใบสั่งงาน จะถูกเพิ่มเป็น DocTypes ในแบ็กเอนด์

DocType ช่วยให้คุณสามารถแทรกแบบฟอร์มที่กำหนดเองใน ERPNext ได้ตามความต้องการของคุณ

อ่าน [เอกสาร DocType](https://frappe.io/docs/user/th/understanding-doctypes) เพื่อความเข้าใจที่มากขึ้น

ในการสร้าง DocType ใหม่ ไปที่:

> ตั้งค่า > ปรับแต่ง > Doctype > ใหม่

## 1. วิธีสร้าง DocType ใหม่:

1. **ชื่อ**: ป้อนชื่อของ DocType ใหม่
1. **โมดูล**: ป้อนโมดูลที่คุณต้องการเพิ่ม DocType ใหม่เข้าไป
1. บันทึก

<img alt="DocType" class="screenshot" src="{{docs_base_url}}/assets/img/customize/doctype-student-transfer.png">

### 1.1. รายละเอียดเพิ่มเติม

1. **ฟิลด์**

 คุณสามารถเลือกเพิ่มฟิลด์ได้มากเท่าที่คุณต้องการ นอกจากนี้ยังสามารถเพิ่มป้ายกำกับ ประเภทฟิลด์ ฟิลด์บังคับ และตัวเลือกอื่นๆ ที่เกี่ยวข้องได้ที่นี่ เรียนรู้เพิ่มเติมเกี่ยวกับประเภทฟิลด์ [ที่นี่](/docs/user/manual/th/customize-erpnext/articles/field-types.html)

 <img alt="DocType" class="screenshot" src="{{docs_base_url}}/assets/img/customize/doctype-student-transfer-certificate.png">


1. **การตั้งชื่อ**

 ที่นี่คุณสามารถเลือกได้ว่าต้องการตั้งชื่อแบบฟอร์มแต่ละแบบฟอร์มภายใน DocType นี้โดยอัตโนมัติหรือไม่ ตามที่ระบุในคำอธิบาย คุณสามารถเลือกรูปแบบการตั้งชื่อแบบฟอร์มได้ ฟิลด์เดียวกันสามารถเป็นฟิลด์ภายใน DocType, Naming Series, Prompt, A Defined Naming Series หรือชื่อตามรูปแบบ สำหรับการตั้งชื่อ คุณสามารถเพิ่มคำอธิบายและตัวพิมพ์ชื่อ (เป็นตัวพิมพ์ชื่อเรื่องหรือตัวพิมพ์ใหญ่) เพื่อความสะดวกของคุณ

 <img alt="DocType" class="screenshot" src="{{docs_base_url}}/assets/img/customize/doctype-student-transfer-certificate-1.png">

1. **การตั้งค่าแบบฟอร์ม**

 การตั้งค่าเพิ่มเติมสำหรับแบบฟอร์ม ฟิลด์รูปภาพ สิ่งที่แนบมา ไทม์ไลน์ ฯลฯ สามารถกำหนดค่าได้ที่นี่ หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับแบบฟอร์ม โปรดไปที่ [กำหนดแบบฟอร์ม](/docs/user/manual/th/customize-erpnext/customize-form)

 <img alt="DocType" class="screenshot" src="{{docs_base_url}}/assets/img/customize/doctype-student-transfer-certificate-2.png">

1. **การตั้งค่ามุมมอง**

 ที่นี่ คุณสามารถกำหนดการตั้งค่ามุมมองสำหรับ DocType เช่น ช่องค้นหา ช่องจัดเรียงเริ่มต้น ลำดับการจัดเรียงเริ่มต้น เป็นต้น

1. **กฎการอนุญาต**

 คุณสามารถกำหนดกฎการอนุญาตสำหรับ DocType ได้ที่นี่ และกำหนดค่าว่าผู้ใช้รายใดจะสามารถใช้หรือเปลี่ยนแปลง DocType นี้ได้ เรียนรู้เพิ่มเติมเกี่ยวกับ [ผู้ใช้และการอนุญาต](/docs/user/manual/th/setting-up/users-and-permissions) ที่นี่

 <img alt="DocType" class="screenshot" src="{{docs_base_url}}/assets/img/customize/doctype-student-transfer-certifictae-3.png">

1. **มุมมองเว็บ**

 คุณสามารถเลือกได้ว่าต้องการมุมมองเว็บของ DocType นี้หรือไม่ การมีมุมมองเว็บสำหรับ DocType จะทำให้ผู้ใช้เว็บไซต์ของคุณสามารถเข้าถึงแบบฟอร์มได้ โปรดอย่าลังเลที่จะเรียนรู้เพิ่มเติมเกี่ยวกับ [ผู้ใช้เว็บไซต์](/docs/user/manual/th/setting-up/articles/difference-between-system-user-and-website-user)

### 1.2. คุณสมบัติเพิ่มเติม

1. **สามารถส่งได้**: คุณสามารถเลือกได้ว่าต้องการให้ DocType นี้ 'บันทึก' เท่านั้น หรือ 'ส่ง' ด้วย โดยการทำเครื่องหมายและยกเลิกการทำเครื่องหมายที่ช่องนี้
1. **เป็นตารางย่อย**: คุณสามารถกำหนดได้ว่าต้องการให้ DocType ใหม่เป็นตารางย่อยภายใน DocType อื่นหรือไม่ ชำระเงิน [Child Table](/docs/user/manual/th/customize-erpnext/articles/customizing-data-visibility-in-child-table) สำหรับข้อมูลเพิ่มเติม
1. **โสด**: หากเลือก Doctype นี้จะกลายเป็นรูปแบบเดียว เช่น Sales Order ซึ่งผู้ใช้จะ
ไม่สามารถผลิตซ้ำได้ เช่น การตั้งค่าการขายในโมดูลการขายเป็นประเภทเอกสารเดียว
1. **เป็นต้นไม้**: DocTypes สองสามรายการใน ERPNext มีโครงสร้างเป็น Tree ซึ่งมี DocType หลักและ DocType ย่อยบางส่วน เช่น Doctype Company มีโครงสร้างเป็น Tree มีบริษัทแม่และบริษัทลูก ซึ่งเราเรียกว่าบริษัทในเครือ หากคุณต้องการให้ DocTypes ของคุณมีโครงสร้างที่คล้ายคลึงกัน คุณสามารถเปิดใช้งานตัวเลือกนี้ได้

    <img alt="DocType" class="screenshot" src="{{docs_base_url}}/assets/img/customize/customize-is tree.png">

1. **รายการด่วน**: คุณสามารถเลือกได้ว่าต้องการสร้างรายการด่วนสำหรับ DocType นี้หรือไม่ ซึ่งจะช่วยให้คุณสามารถป้อนรายละเอียดที่จำเป็นเพียงไม่กี่รายการและบันทึก DocType เพื่อให้มีการป้อนข้อมูลอย่างรวดเร็ว ตัวอย่างเช่น ตรวจสอบรายการด่วนใน [รายการบันทึก](/docs/user/manual/th/accounts/journal-entry#11-quick-entry)
1. **ติดตามการเปลี่ยนแปลง**: คุณสามารถเลือกตัวเลือกนี้หากคุณต้องการเก็บบันทึกการเปลี่ยนแปลงที่ทำกับแต่ละแบบฟอร์ม ลองดู [Document Versioning](/docs/user/manual/th/using-erpnext/document-versioning) เพื่อความเข้าใจในเรื่องนี้มากขึ้น
1. **ติดตามแล้ว**: คุณสามารถเลือกตัวเลือกนี้หากคุณต้องการเก็บบันทึกของผู้ใช้ทั้งหมดที่ได้เห็นแบบฟอร์มนี้
1. **ติดตามการดู**: คุณสามารถเลือกตัวเลือกนี้หากคุณต้องการเก็บบันทึกทุกครั้งที่ผู้ใช้แต่ละคนดูแบบฟอร์มนี้

  <img alt="Customize Form" class="screenshot" src="{{docs_base_url}}/assets/img/customize/customize-track-views.png">

1. **กำหนดเอง?**: ฟิลด์นี้จะถูกตรวจสอบโดยค่าเริ่มต้นเมื่อเพิ่ม Doctype แบบกำหนดเอง ในทำนองเดียวกัน หากคุณกำลังปรับแต่ง DocType ที่มีอยู่แล้วในระบบ ฟิลด์นี้ตามค่าเริ่มต้นจะไม่ถูกเลือก

## 2. วิดีโอ

<div class="embed-container">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/WSzkpPm3iIU?start=585" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

{next}
