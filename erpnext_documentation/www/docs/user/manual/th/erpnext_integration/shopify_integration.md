<!-- add-breadcrumbs -->
# การใช้ Shopify

Shopify Connector ดึงคำสั่งซื้อจาก Shopify และสร้างใบสั่งขายเทียบกับคำสั่งซื้อเหล่านั้นใน ERPNext

ขณะสร้างใบสั่งขายหากลูกค้าหรือสินค้าหายไปใน ERPNext ระบบจะสร้างลูกค้า/สินค้าใหม่โดยดึงรายละเอียดที่เกี่ยวข้องจาก Shopify

### วิธีการตั้งค่าตัวเชื่อมต่อ

#### สร้างแอปส่วนตัวใน Shopify

1. คลิกที่แอพในแถบเมนู
<img class="screenshot" alt="Menu Section" src="{{docs_base_url}}/assets/img/erpnext_integrations/app_menu.png">

2. คลิก **จัดการแอปส่วนตัว** เพื่อสร้างแอปส่วนตัว
<img class="screenshot" alt="Manage Private Apps" src="{{docs_base_url}}/assets/img/erpnext_integrations/manage_private_apps.png">

3. กรอกรายละเอียดและสร้างแอพ แต่ละแอพมีคีย์ API รหัสผ่านและความลับที่ใช้ร่วมกัน
<img class="screenshot" alt="App Details" src="{{docs_base_url}}/assets/img/erpnext_integrations/app_details.png">


#### การตั้งค่า Shopify บน ERPNext:-
เมื่อคุณสร้างแอปส่วนตัวบน Shopify แล้ว ให้ตั้งค่าข้อมูลรับรองแอปและรายละเอียดอื่นๆ ในการตั้งค่า Shopify ใน ERPNext

> หากต้องการเข้าถึงการตั้งค่า Shopify ให้ไปที่:
การผสานการทำงาน > การตั้งค่า Shopify

หมายเหตุ: Shopify ไม่รองรับการเชื่อมต่อ HTTP ที่ไม่ปลอดภัย ไซต์ ERPNext ของคุณต้องสามารถยอมรับคำขอ HTTPS ได้ เข้าถึงไซต์ ERPNext ของคุณโดยใช้ `https://` url ก่อนดำเนินการต่อ

1. เลือกประเภทแอปเป็นคีย์ API แบบส่วนตัวและกรอก รหัสผ่าน และข้อมูลลับที่แชร์จากแอปส่วนตัวของ Shopify
<img class="screenshot" alt="Setup Private App Credentials" src="{{docs_base_url}}/assets/img/erpnext_integrations/app_details.png">

2. ตั้งค่าลูกค้า บริษัท และการกำหนดค่าสินค้าคงคลัง
<img class="screenshot" alt="ERP Configurations" src="{{docs_base_url}}/assets/img/erpnext_integrations/erp_configurations.png">

3. ตั้งค่าการกำหนดค่าการซิงค์
    ระบบจะดึงคำสั่งซื้อจาก Shopify และสร้างใบสั่งขายใน ERPNext คุณสามารถกำหนดค่าระบบ ERPNext เพื่อบันทึกการชำระเงินและการปฏิบัติตามคำสั่งซื้อ
<img class="screenshot" alt="Sync Configure" src="{{docs_base_url}}/assets/img/erpnext_integrations/sync_config.png">

4. ตั้งค่า Tax Mapper
    เตรียมภาษีและค่าจัดส่งสำหรับภาษีและค่าจัดส่งแต่ละรายการที่คุณสมัครใน Shopify
<img class="screenshot" alt="Taxes and Shipping Charges" src="{{docs_base_url}}/assets/img/erpnext_integrations/tax_config.png">


หลังจากตั้งค่าการกำหนดค่าทั้งหมดแล้ว ให้เปิดใช้งานการซิงค์ Shopify และบันทึกการตั้งค่า การดำเนินการนี้จะลงทะเบียน API กับ Shopify และระบบจะเริ่มการซิงค์คำสั่งซื้อระหว่าง Shopify และ ERPNext


### กำลังซิงค์คำสั่งซื้อเก่าจาก Shopify

เมื่อคุณกำหนดค่า Shopify เสร็จแล้วและเปิดใช้งาน การซิงค์ Shopify คุณจะได้รับข้อกำหนดในการซิงค์คำสั่งซื้อเก่าของคุณจาก Shopify ไปยัง ERPNext คำสั่งซื้อสูงสุด 250 รายการจะถูกซิงค์ทุกชั่วโมงผ่านงานพื้นหลัง จนกว่าคำสั่งซื้อทั้งหมดภายในช่วงดังกล่าวจะได้รับการซิงค์

สามารถซิงค์ใบแจ้งหนี้ตามเกณฑ์สองข้อต่อไปนี้

#### 1. ซิงค์คำสั่งซื้อเก่าตามวันที่

1. เปิดใช้งาน "ซิงค์คำสั่งซื้อ Shopify เก่าที่หายไป"
1. เลือก "วันที่" ในช่อง "ซิงค์ตาม" และป้อนวันที่จากและถึงวันที่ซึ่งต้องซิงค์คำสั่งซื้อ

<img class="screenshot" alt="Sync Order By Date" src="{{docs_base_url}}/assets/img/erpnext_integrations/shopify-order-sync-date.png">


#### 2. ซิงค์คำสั่งซื้อเก่าตาม Shopify Order ID

1. เปิดใช้งาน "ซิงค์คำสั่งซื้อ Shopify เก่าที่หายไป"
1. เลือก "Shopify Order ID" ในช่อง "Sync Based On" และป้อนรหัสจากและไปยังคำสั่งซื้อระหว่างนั้นต้องซิงค์คำสั่งซื้อ วิธีที่ง่ายที่สุดในการรับรหัสคำสั่งซื้อของ Shopify มาจาก URL ของคำสั่งซื้อดังที่แสดงในภาพด้านล่าง

<img class="screenshot" alt="Shopify Order ID" src="{{docs_base_url}}/assets/img/erpnext_integrations/shopify-order-id.png">

<img class="screenshot" alt="Sync Order ID" src="{{docs_base_url}}/assets/img/erpnext_integrations/shopify-order-sync-id.png">

### หมายเหตุ:
ตัวเชื่อมต่อจะไม่จัดการการยกเลิกคำสั่งซื้อ หากคุณยกเลิกคำสั่งซื้อใดๆ ใน Shopify คุณจะต้องยกเลิกคำสั่งซื้อที่เกี่ยวข้องและเอกสารอื่นๆ ใน ERPNext ด้วยตนเอง

#### เวอร์ชัน 11:
เราได้ปรับปรุงการผสานรวมของ Shopify เพื่อให้เป็นไปในทิศทางเดียว - ตัวเชื่อมต่อ Shopify จะดึงคำสั่งซื้อจาก Shopify และสร้างใบสั่งขายเทียบกับพวกเขาใน ERPNext ไม่ใช่ในทางกลับกัน
