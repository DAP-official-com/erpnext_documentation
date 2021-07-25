<!-- add-breadcrumbs -->
# ERPNext Shipping

**แอป ERPNext Shipping ช่วยให้คุณเปรียบเทียบอัตราค่าจัดส่งที่นำเสนอโดยผู้ให้บริการหลายราย สร้างป้ายกำกับ และติดตามสถานะการจัดส่งของคุณ**

สามารถทำงานร่วมกับผู้ให้บริการดังต่อไปนี้:

1. [Packlink](https://www.packlink.com/en-GB/)
1. [LetMeShip](https://www.letmeship.com/th/)
1. [SendCloud](https://www.sendcloud.com/home-new/)

## 1. การตั้งค่า

เพื่อให้แอปทำงานได้อย่างราบรื่น คุณจะต้องสร้างคีย์ API จาก **อย่างน้อยหนึ่ง** ของแพลตฟอร์มที่ระบุไว้ข้างต้น นี่คือคำแนะนำในการตั้งค่า:

### 1.1 Packlink API

1. ลงทะเบียนบน [Packlink PRO](https://auth.packlink.com/en-GB/pro/register?platform=PRO&platform_country=UN)
1. ปฏิบัติตาม [ขั้นตอนเหล่านี้](https://support-pro.packlink.com/hc/en-gb/articles/213431749-How-to-generate-an-API-key-on-PRO) เพื่อสร้าง * *คีย์ API**
1. ค้นหา **Packlink** ใน Awesome bar
1. เพิ่ม **คีย์ API** ไปยัง Packlink DocType ทำเครื่องหมายในช่อง "เปิดใช้งาน"
1. บันทึก

<img class="screenshot" alt="Packlink API" src="{{docs_base_url}}/assets/img/erpnext_integrations/packlink_api.png">

### 1.1 Sendcloud API

1. ลงทะเบียนบน [Sendcloud](https://panel.sendcloud.sc/accounts/signup/)
1. ปฏิบัติตาม [ขั้นตอนเหล่านี้](https://support.sendcloud.com/hc/en-us/articles/360024967612-Service-points-for-API-Integrations#step-1-) เพื่อสร้าง **คีย์สาธารณะ ** และ **รหัสลับ**
1. ค้นหา **SendCloud** ใน Awesome bar
1. เพิ่ม **กุญแจสาธารณะ** ในฟิลด์ 'รหัส API' และ **รหัสลับ** ในฟิลด์ 'รหัสลับ API' ของ SendCloud DocType
1. ตรวจสอบช่อง **เปิดใช้งาน**
1. บันทึก

<img class="screenshot" alt="Sendcloud API" src="{{docs_base_url}}/assets/img/erpnext_integrations/sendcloud_api.png">

### 1.1 LetMeShip API

1. ลงทะเบียนบน [LetMeShip](https://www.letmeship.com/th/)
1. ปฏิบัติตาม [ขั้นตอนเหล่านี้](https://www.letmeship.com/th/connect-the-shipping-interface/) เพื่อสร้าง **API ID** และ **รหัสผ่าน API**
1. ค้นหา **LetMeShip** ใน Awesome bar
1. เพิ่ม **API ID** และ **รหัสผ่าน API** ใน LetMeShip DocType ทำเครื่องหมายในช่อง **เปิดใช้งาน**
1. บันทึก

<img class="screenshot" alt="LetMeShip API" src="{{docs_base_url}}/assets/img/erpnext_integrations/letmeship_api.png">

## 2. คุณสมบัติ

### 2.1 การเปรียบเทียบอัตราค่าจัดส่ง

เมื่อ [ส่งสินค้า](/docs/user/manual/th/stock/shipment) แล้ว หากติดตั้งแอปแล้ว ปุ่ม **ดึงข้อมูลอัตราค่าจัดส่ง** จะปรากฏขึ้น เมื่อคลิก คุณจะได้รับรายการบริการพร้อมกับผู้ให้บริการและอัตราค่าบริการ

<img class="screenshot" alt="Fetch Rates" src="{{docs_base_url}}/assets/img/erpnext_integrations/fetch_rates.png">

คุณยังสามารถเพิ่มบริการที่ใช้บ่อยใน **บริการที่ต้องการ** โดยใช้ **ประเภทบริการพัสดุ**:

1. สมมติว่าบริการเด่นเป็นบริการที่เราใช้งานบ่อย ให้เราเพิ่มลงใน **บริการที่ต้องการ**

 <img class="screenshot" alt="Highlight Service" src="{{docs_base_url}}/assets/img/erpnext_integrations/service_highlight.png">

1. ไปที่ **ประเภทบริการพัสดุ** > **ใหม่** สร้าง **บริการพัสดุภัณฑ์** ใหม่ ในกรณีของเราคือ 'ทีเอ็นที'
1. เพิ่ม **ประเภทบริการพัสดุ** ในกรณีของเรา มันจะเป็น 'เศรษฐกิจ'
1. เพิ่ม 'Economy' ลงในตาราง **Parcel Service Type Alias** ด้วย
1. เพิ่มคำอธิบาย (ไม่บังคับ)
1. เปิดใช้งานช่อง **แสดงในรายการบริการที่ต้องการ** บันทึก.

ตอนนี้เมื่อคุณคลิกที่ปุ่ม **ดึงข้อมูลอัตราค่าจัดส่ง** คุณจะเห็นบริการที่ไฮไลต์ไว้ก่อนหน้านี้เสมอภายใต้ **บริการที่ต้องการ**

<img class="screenshot" alt="Preferred Service" src="{{docs_base_url}}/assets/img/erpnext_integrations/preferred_service.png">

### 2.2 การสร้างการจัดส่ง

หลังจากเปรียบเทียบราคาแล้ว คุณสามารถดำเนินการกับบริการใดก็ได้โดยคลิก **เลือก** กับแถวบริการที่เหมาะสม เมื่อคลิก การจัดส่งจะถูกสร้างขึ้นโดยอัตโนมัติบนแพลตฟอร์มของผู้ให้บริการของคุณ

คุณจะสังเกตเห็นว่าส่วน **ข้อมูลการจัดส่ง** ได้รับการอัปเดตโดยอัตโนมัติตามการจัดส่งที่สร้างขึ้น

<img class="screenshot" alt="Shipment Creation" src="{{docs_base_url}}/assets/img/erpnext_integrations/create_shipment.gif">

คุณยังสามารถค้นหาธุรกรรมของคุณบนแพลตฟอร์มของผู้ให้บริการโดยใช้ช่อง **รหัสการจัดส่ง**

<img class="screenshot" alt="Packlink Shipment" src="{{docs_base_url}}/assets/img/erpnext_integrations/packlink_shipment.png">

### 2.3 การพิมพ์ฉลาก

หากต้องการใช้ปุ่ม **พิมพ์ฉลากการจัดส่ง** จะต้องสร้าง **รหัสการจัดส่ง** ในบันทึกปัจจุบัน

<img class="screenshot" alt="Print Label Button" src="{{docs_base_url}}/assets/img/erpnext_integrations/print_label_button.png">

จากนั้นคุณสามารถคลิกและสร้างป้ายกำกับการจัดส่งได้

<img class="screenshot" alt="Dummy Shipping Label" src="{{docs_base_url}}/assets/img/erpnext_integrations/dummy_shipping_label.png">


คุณยังสามารถติดตามสถานะการจัดส่งของคุณได้โดยคลิกที่ **ดู** > **ติดตามสถานะ**

> **หมายเหตุ** : แพลตฟอร์มที่ผสานรวมในปัจจุบันอาจไม่ให้บริการในภูมิภาคของคุณ โปรดไปที่ลิงก์ที่แนบมากับพวกเขาเพื่อทราบข้อมูลเพิ่มเติม