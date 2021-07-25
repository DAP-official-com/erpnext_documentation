<!-- add-breadcrumbs -->
#การใช้ RazorPay

เกตเวย์การชำระเงินเป็นบริการของผู้ให้บริการแอปพลิเคชันอีคอมเมิร์ซที่อนุญาตการชำระเงินด้วยบัตรเครดิตสำหรับธุรกิจอิเล็กทรอนิกส์ ผู้ค้าปลีกออนไลน์ อิฐและคลิก หรืออิฐและปูนแบบดั้งเดิม

เกตเวย์การชำระเงินอำนวยความสะดวกในการถ่ายโอนข้อมูลระหว่างพอร์ทัลการชำระเงิน (เช่น เว็บไซต์ โทรศัพท์มือถือหรือบริการตอบกลับด้วยเสียงแบบโต้ตอบ) และ Front End Processor หรือธนาคารที่ซื้อ

ในการตั้งค่า RazorPay

`สำรวจ> บูรณาการ> การตั้งค่า RazorPay`

<img class="screenshot" alt="Razorpay Settings" src="{{docs_base_url}}/assets/img/setup/integrations/razorpay-api.gif">

#### ตั้งค่า RazorPay

ในการเปิดใช้งานบริการชำระเงิน RazorPay คุณต้องกำหนดค่าพารามิเตอร์ เช่น คีย์ API, API Secret

<img class="screenshot" alt="Razorpay Settings" src="{{docs_base_url}}/assets/img/setup/integrations/razorpay_settings.png">

ในการเปิดใช้งานบริการ ระบบจะสร้างบันทึก ช่องทางการชำระเงิน และส่วนหัวของบัญชีในผังบัญชีที่มีประเภทบัญชีเป็นธนาคาร

<img class="screenshot" alt="Razorpay COA" src="{{docs_base_url}}/assets/img/setup/integrations/razorpay_coa.png">

นอกจากนี้ยังจะสร้างรายการบัญชี ช่องทางการชำระเงิน บัญชีเกตเวย์การชำระเงินเป็นฮับการกำหนดค่าจากสิ่งนี้ คุณสามารถตั้งค่าส่วนหัวของบัญชีจาก COA ที่มีอยู่ เทมเพลตเนื้อหาอีเมลคำขอชำระเงินเริ่มต้น

<img class="screenshot" alt="Payment Gateway Account" src="{{docs_base_url}}/assets/img/setup/integrations/payment_gateway_account_razorpay.png">

หลังจากเปิดใช้บริการและกำหนดค่าบัญชี ช่องทางการชำระเงิน แล้ว ระบบของคุณจะสามารถรับการชำระเงินออนไลน์ได้

####สกุลเงินที่รองรับการทำธุรกรรม

RazorPay จะใช้ได้กับบริษัทที่มี `INR (รูปีอินเดีย)` เป็นสกุลเงินเท่านั้น