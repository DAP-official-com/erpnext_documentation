<!-- add-breadcrumbs -->
#การตั้งค่า Stripe

ในการตั้งค่า Stripe
`สำรวจ> บูรณาการ> การตั้งค่า Stripe'

#### ตั้งค่า Stripe

ในการเปิดใช้งานบริการชำระเงิน Stripe คุณต้องกำหนดค่าพารามิเตอร์ เช่น Publishable Key, Secret Key
<img class="screenshot" alt="Razorpay Settings" src="{{docs_base_url}}/assets/img/setup/integrations/stripe_setting.png">

ในการเปิดใช้บริการ ระบบจะสร้างบันทึก ช่องทางการชำระเงิน และส่วนหัวของบัญชีตามผังบัญชีที่มีประเภทบัญชีเป็นธนาคาร

<img class="screenshot" alt="Stripe COA" src="{{docs_base_url}}/assets/img/setup/integrations/stripe_coa.png">

นอกจากนี้ยังจะสร้างรายการบัญชี ช่องทางการชำระเงิน บัญชีเกตเวย์การชำระเงินเป็นฮับการกำหนดค่าจากสิ่งนี้ คุณสามารถตั้งค่าส่วนหัวของบัญชีจาก COA ที่มีอยู่ เทมเพลตเนื้อหาอีเมลคำขอชำระเงินเริ่มต้น

<img class="screenshot" alt="Payment Gateway Account" src="{{docs_base_url}}/assets/img/setup/integrations/payment_gateway_account_stripe.png">

หลังจากตั้งค่าบัญชี ช่องทางการชำระเงิน แล้ว ระบบของคุณสามารถยอมรับการชำระเงินออนไลน์ได้

### ตั้งค่าแผนการสมัครสมาชิก

หากคุณต้องการเรียกเก็บเงินเป็นจำนวนเป็นงวดแทนการเรียกเก็บเงินแบบครั้งเดียว คุณสามารถใช้ระบบสมัครสมาชิกของ Stripe ได้

เมื่อคุณสร้างแผนการเรียกเก็บเงินใน Stripe แล้ว ให้เพิ่ม "แผนการชำระเงิน" ใหม่อย่างน้อยหนึ่งรายการใน Frappe

<img class="screenshot" alt="Payment Plan" src="{{docs_base_url}}/assets/img/setup/integrations/payment_plan.png">


หลังจากนั้น เมื่อคุณสร้างคำขอชำระเงิน ให้คลิกช่องทำเครื่องหมาย "เป็นการสมัครสมาชิก" และเพิ่มระบบจะดึงแผนการสมัครสมาชิกที่เกี่ยวข้องจากภายในการสมัครรับข้อมูลที่เกี่ยวข้อง

<img class="screenshot" alt="Payment Request" src="{{docs_base_url}}/assets/img/setup/integrations/subscription_payment_request.png">


ERPNext จะสร้างการสมัครสมาชิกใหม่โดยอัตโนมัติสำหรับลูกค้ารายนี้ใน Stripe


####สกุลเงินที่รองรับการทำธุรกรรม
	"AED", "ALL", "ANG", "ARS", "AUD", "AWG", "BBD", "BDT", "BIF", "BMD", "BND",
	"BOB", "BRL", "BSD", "BWP", "BZD", "CAD", "CHF", "CLP", "CNY", "COP", "CRC", "CVE", "CZK", "DJF",
	"DKK", "DOP", "DZD", "EGP", "ETB", "EUR", "FJD", "FKP", "GBP", "GIP", "GMD", "GNF", "GTQ", "GYD",
	"HKD", "HNL", "HRK", "HTG", "HUF", "IDR", "ILS", "INR", "ISK", "JMD", "JPY", "KES", "KHR", "KMF",
	"KRW", "KYD", "KZT", "LAK", "LBP", "LKR", "LRD", "MAD", "MDL", "MNT", "MOP", "MRO", "MUR", "MVR",
	"MWK", "MXN", "MYR", "NAD", "NGN", "NIO", "NOK", "NPR", "NZD", "PAB", "PEN", "PGK", "PHP", "PKR",
	"PLN", "PYG", "QAR", "RUB", "SAR", "SBD", "SCR", "SEK", "SGD", "SHP", "SLL", "SOS", "STD", "SVC",
	"SZL", "THB", "TOP", "TTD", "TWD", "TZS", "UAH", "UGX", "USD", "UYU", "UZS", "VND", "VUV", "WST",
	"XAF", "XOF", "XPF", "YER", "ZAR"