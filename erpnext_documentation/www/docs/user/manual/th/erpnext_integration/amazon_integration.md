<!-- add-breadcrumbs -->
# การรวม Amazon MWS
 ตัวเชื่อมต่อ Amazon ดึงผลิตภัณฑ์และใบสั่งขายจากตลาดของ Amazon
 การซิงค์ผลิตภัณฑ์และใบสั่งขายเป็นแบบต่อเนื่อง คุณต้องซิงค์ผลิตภัณฑ์ก่อนที่คุณจะซิงค์ใบสั่งขาย

## วิธีการตั้งค่าตัวเชื่อมต่อ Amazon MWS

### การตั้งค่าข้อมูลรับรองใน ERPNext
คุณสามารถขอข้อมูลประจำตัวนักพัฒนาจาก Amazon MWS เมื่อคุณเป็นผู้ขายที่ลงทะเบียนบนเว็บไซต์ของพวกเขา สำหรับรายละเอียดเพิ่มเติมเกี่ยวกับเรื่องเดียวกัน ให้คลิก [ที่นี่](https://docs.developer.amazonservices.com/en_ES/dev_guide/DG_Registering.html)

#### 1. ตั้งค่า MWS Credentials
ป้อน ID ผู้ขาย, รหัสคีย์การเข้าถึง AWS, โทเค็นการตรวจสอบสิทธิ์ MWS, คีย์ลับ, รหัส Market Place, ภูมิภาค และโดเมน
<img class="screenshot" alt="Setup Credentials" src="{{docs_base_url}}/assets/img/erpnext_integrations/amazon_mws_settings_1.png">

#### 2. ตั้งค่ารายละเอียดคำสั่งซื้อ
ตั้งค่าบริษัท คลังสินค้า กลุ่มสินค้า รายการราคา กลุ่มลูกค้า อาณาเขต ประเภทลูกค้า และกลุ่มบัญชี
   กลุ่มบัญชีใช้เพื่อเก็บค่าคอมมิชชั่น ภาษี ฯลฯ ที่ Amazon เรียกเก็บ
<img class="screenshot" alt="ERPNext Configurations" src="{{docs_base_url}}/assets/img/erpnext_integrations/amazon_mws_settings_2.png">
 
#### 3. ตั้งค่าการกำหนดค่าการซิงค์
เมื่อใช้ After Date คุณสามารถซิงค์ผลิตภัณฑ์และคำสั่งซื้อที่สร้างขึ้นหลังจากวันที่ที่ระบุ ในกรณีที่คุณกำลังนำเข้าข้อมูลในอดีตจำนวนมาก ขอแนะนำให้เริ่มตามลำดับเวลาย้อนกลับของ After Date และนำเข้าข้อมูลเป็นส่วนเล็กๆ
<img class="screenshot" alt="Sync Configurations" src="{{docs_base_url}}/assets/img/erpnext_integrations/amazon_mws_settings_3.png">
หลังจากตั้งค่าคอนฟิกทั้งหมดแล้ว ให้คลิกที่ เปิดใช้งาน Amazon และบันทึกการตั้งค่า ตอนนี้คุณพร้อมที่จะใช้
บูรณาการ
 
#### 4. ซิงค์ผลิตภัณฑ์
คลิกที่ปุ่มนี้เพื่อซิงค์ผลิตภัณฑ์ เมื่อสำเร็จแล้ว คุณควรเห็นผลิตภัณฑ์ Amazon ของคุณเป็นรายการใน ERPNext

<img class="screenshot" alt="Sync Configurations" src="{{docs_base_url}}/assets/img/erpnext_integrations/amazon_mws_settings_4.png">
<img class="screenshot" alt="Sync Configurations" src="{{docs_base_url}}/assets/img/erpnext_integrations/amazon_mws_settings_5.png">
 
#### 5. ซิงค์คำสั่งซื้อ
คลิกที่ปุ่มนี้เพื่อซิงค์ใบสั่งขาย เมื่อสำเร็จแล้ว คุณควรเห็นคำสั่งซื้อของ Amazon
   เป็นคำสั่งขายใน ERPNext คุณยังสามารถตั้งค่าตัวจัดกำหนดการเพื่อซิงค์คำสั่งซื้อโดยอัตโนมัติ

>ในกรณีที่บัญชีนักพัฒนาของคุณไม่สามารถเข้าถึงข้อมูลส่วนบุคคลที่สามารถระบุตัวตนได้ ชื่อลูกค้าจะถูกเก็บไว้เป็นการรวมกันของ ผู้ซื้อ + &lt;Order ID&gt;

  <img class="screenshot" alt="Sync Configurations" src="{{docs_base_url}}/assets/img/erpnext_integrations/amazon_mws_settings_6.png">

### หมายเหตุ

ตัวเชื่อมต่อจะไม่จัดการการยกเลิกคำสั่งซื้อ หากคุณยกเลิกคำสั่งซื้อใดๆ ใน Amazon คุณต้องยกเลิกคำสั่งซื้อและเอกสารอื่นๆ ใน ERPNext ด้วยตนเอง
