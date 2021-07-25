<!-- add-breadcrumbs -->
# การตั้งค่า Braintree

ในการตั้งค่า Braintree ให้ไปที่ `สำรวจ > บูรณาการ > การตั้งค่า Braintree`

## ตั้งค่า Braintree

ในการเปิดใช้งาน Braintree ในบัญชี ERPNext ของคุณ คุณต้องกำหนดค่าพารามิเตอร์ต่อไปนี้:

- ID ผู้ค้า
- กุญแจสาธารณะ
- กุญแจส่วนตัว

คุณสามารถตั้งค่าเกตเวย์การชำระเงินของ Braintree ได้หลายช่องทางหากต้องการ ทางเลือกของบัญชีเกตเวย์การชำระเงินจะเป็นตัวกำหนดว่าบัญชี Braintree ใดที่ใช้สำหรับการชำระเงิน

![Braintree Settings](/docs/assets/img/setup/integrations/braintree_account.png)

ในการเปิดใช้งานบริการ ระบบจะสร้างบันทึก ช่องทางการชำระเงิน และส่วนหัวของบัญชีในผังบัญชีที่มีประเภทบัญชีเป็นธนาคาร

![Braintree COA](/docs/assets/img/setup/integrations/braintree_coa.png)


นอกจากนี้ยังจะสร้างบัญชีช่องทางการชำระเงิน คุณสามารถเปลี่ยนบัญชีธนาคารเริ่มต้นได้หากต้องการ และสร้างเทมเพลตสำหรับคำขอชำระเงิน

![Payment Gateway Account](/docs/assets/img/setup/integrations/payment_gateway_account_braintree.png)

หลังจากกำหนดค่าบัญชีช่องทางการชำระเงิน แล้ว ระบบของคุณสามารถยอมรับการชำระเงินออนไลน์ผ่าน Braintree ได้

## รองรับสกุลเงินการทำธุรกรรม

```
"AED","AMD","AOA","ARS","AUD","AWG","AZN","BAM","BBD","BDT","BGN","BIF","BMD","BND","BOB",
"BRL","BSD","BWP","BYN","BZD","CAD","CHF","CLP","CNY","COP","CRC","CVE","CZK","DJF","DKK",
"DOP","DZD","EGP","ETB","EUR","FJD","FKP","GBP","GEL","GHS","GIP","GMD","GNF","GTQ","GYD",
"HKD","HNL","HRK","HTG","HUF","IDR","ILS","INR","ISK","JMD","JPY","KES","KGS","KHR","KMF",
"KRW","KYD","KZT","LAK","LBP","LKR","LRD","LSL","LTL","MAD","MDL","MKD","MNT","MOP","MUR",
"MVR","MWK","MXN","MYR","MZN","NAD","NGN","NIO","NOK","NPR","NZD","PAB","PEN","PGK","PHP",
"PKR","PLN","PYG","QAR","RON","RSD","RUB","RWF","SAR","SBD","SCR","SEK","SGD","SHP","SLL",
"SOS","SRD","STD","SVC","SYP","SZL","THB","TJS","TOP","TRY","TTD","TWD","TZS","UAH","UGX",
"USD","UYU","UZS","VEF","VND","VUV","WST","XAF","XCD","XOF","XPF","YER","ZAR","ZMK","ZWD"
```