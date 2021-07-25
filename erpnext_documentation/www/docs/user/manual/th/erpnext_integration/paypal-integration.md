<!-- add-breadcrumbs -->
#การตั้งค่า PayPal

เกตเวย์การชำระเงินเป็นบริการของผู้ให้บริการแอปพลิเคชันอีคอมเมิร์ซที่อนุญาตการชำระเงินด้วยบัตรเครดิตสำหรับธุรกิจอิเล็กทรอนิกส์ ผู้ค้าปลีกออนไลน์ อิฐและคลิก หรืออิฐและปูนแบบดั้งเดิม

เกตเวย์การชำระเงินอำนวยความสะดวกในการถ่ายโอนข้อมูลระหว่างพอร์ทัลการชำระเงิน (เช่น เว็บไซต์ โทรศัพท์มือถือหรือบริการตอบกลับด้วยเสียงแบบโต้ตอบ) และ Front End Processor หรือธนาคารที่ซื้อ

ในการตั้งค่า PayPal ,
`สำรวจ > บูรณาการ > การตั้งค่า PayPal`

#### ตั้งค่า PayPal

ในการเปิดใช้งานบริการชำระเงิน PayPal คุณต้องกำหนดค่าพารามิเตอร์ เช่น ชื่อผู้ใช้ API รหัสผ่าน API และลายเซ็น

<img class="screenshot" alt="PayPal Settings" src="{{docs_base_url}}/assets/img/setup/integrations/paypal_settings.png">

คุณยังสามารถตั้งค่าสภาพแวดล้อมการชำระเงินทดสอบได้ด้วยการตั้งค่า `ใช้แซนด์บ็อกซ์`

ในการเปิดใช้งานบริการ ระบบจะสร้างบันทึก Payment Gateway และส่วนหัวของบัญชีในผังบัญชีที่มีประเภทบัญชีเป็นธนาคาร

<img class="screenshot" alt="PayPal COA" src="{{docs_base_url}}/assets/img/setup/integrations/paypal_coa.png">

นอกจากนี้ยังจะสร้างรายการบัญชี ช่องทางการชำระเงิน บัญชีเกตเวย์การชำระเงินเป็นฮับการกำหนดค่าจากสิ่งนี้ คุณสามารถตั้งค่าส่วนหัวของบัญชีจาก COA ที่มีอยู่ เทมเพลตเนื้อหาอีเมลคำขอชำระเงินเริ่มต้น

<img class="screenshot" alt="Payment Gateway Account" src="{{docs_base_url}}/assets/img/setup/integrations/payment_gateway_account_paypal.png">


หลังจากเปิดใช้บริการและกำหนดค่าบัญชี ช่องทางการชำระเงิน แล้ว ระบบของคุณจะสามารถรับการชำระเงินออนไลน์ได้

####สกุลเงินที่รองรับการทำธุรกรรม
AUD, BRL, CAD, CZK, DKK, EUR, HKD, HUF, ILS, JPY, MYR, MXN, TWD, NZD, NOK, PHP, PLN, GBP, RUB, SGD, SEK, CHF, THB, TRY, USD

##Get PayPal credentials

#### ลายเซ็น Paypal Sanbox API
 - เข้าสู่ระบบบัญชีนักพัฒนา paypal <a href="https://developer.paypal.com/">บัญชีนักพัฒนา PayPal</a>
 - จากแท็บ **บัญชี** สร้างบัญชีธุรกิจใหม่
<img class="screenshot" alt="Payment Request" src="{{docs_base_url}}/assets/img/setup/integrations/setup-sanbox-1.png">

- จากโปรไฟล์บัญชีนี้ คุณจะได้รับข้อมูลประจำตัวแซนด์บ็อกซ์ api ของคุณ
<img class="screenshot" alt="Payment Request" src="{{docs_base_url}}/assets/img/setup/integrations/sanbox-credentials.png">


---

#### ลายเซ็น API บัญชี PayPal
 - เข้าสู่ระบบบัญชี PayPal และไปที่โปรไฟล์
<img class="screenshot" alt="Payment Request" src="{{docs_base_url}}/assets/img/setup/integrations/api-step-1.png">

 - จาก **เครื่องมือการขายของฉัน** ไปที่ **การเข้าถึง api**
<img class="screenshot" alt="Payment Request" src="{{docs_base_url}}/assets/img/setup/integrations/api-step-2.png">

 - ในหน้าการเข้าถึง API เลือกตัวเลือกที่ 2 เพื่อสร้างข้อมูลรับรอง API
<img class="screenshot" alt="Payment Request" src="{{docs_base_url}}/assets/img/setup/integrations/api-step-3.png">