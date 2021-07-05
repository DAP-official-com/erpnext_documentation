<!-- add-breadcrumbs -->
# การประเมินค่าอัตราแลกเปลี่ยน

ใน ERPNext คุณสามารถทำรายการบัญชีได้หลายสกุลเงิน ตัวอย่างเช่น หากคุณมีบัญชีธนาคารในสกุลเงินต่างประเทศ คุณสามารถทำธุรกรรมในสกุลเงินนั้นได้และระบบจะแสดงยอดเงินในธนาคารในสกุลเงินนั้น

วัตถุประสงค์ของหลักการประเมินค่าอัตราแลกเปลี่ยนใหม่คือการปรับยอดดุลในบัญชีแยกประเภททั่วไปตามการเปลี่ยนแปลงในอัตราแลกเปลี่ยนสกุลเงิน สิ่งนี้มีประโยชน์เมื่อคุณปิดสมุดบัญชีและต้องการอัปเดตบัญชีแยกประเภทของบริษัทของคุณโดยนำเงินมาจากบัญชีสกุลเงินอื่น

ในการเข้าถึงรายการการประเมินค่าอัตราแลกเปลี่ยนใหม่ ไปที่:
> หน้าหลัก > บัญชี > หลายสกุลเงิน > การประเมินค่าอัตราแลกเปลี่ยน

## 1. วิธีตั้งค่าสกุลเงินในบัญชี

1. ในการเริ่มต้นการบัญชีแบบหลายสกุลเงิน คุณต้องกำหนดสกุลเงินทางบัญชีในเรกคอร์ดบัญชี
1. คุณสามารถกำหนดสกุลเงินจากผังบัญชีขณะสร้างบัญชี

 <img class="screenshot" alt="Set Currency from Chart of Accounts" src="{{docs_base_url}}/assets/img/accounts/multi-currency/chart-of-accounts.png">
 
1. คุณยังสามารถกำหนด/แก้ไขสกุลเงินสำหรับบัญชีที่มีอยู่ได้ด้วยการเปิดเรกคอร์ดบัญชีเฉพาะ
1. คลิกที่บัญชีและคลิกที่แก้ไข

 <img class="screenshot" alt="Modify Account Currency"  src="{{docs_base_url}}/assets/img/accounts/multi-currency/account-set-currency.png">

## 2. วิธีเปิดใช้งานการประเมินค่าอัตราแลกเปลี่ยน

คุณลักษณะการประเมินค่าอัตราแลกเปลี่ยนใหม่มีไว้สำหรับจัดการกับสถานการณ์เมื่อคุณมีบัญชีที่มีสกุลเงินต่างกันในผังบัญชีของบริษัท

1. ไปที่: **การตั้งค่า> บริษัท > *เลือก บริษัท***.
1. ตั้งค่าฟิลด์ 'บัญชีกำไร/ขาดทุนจากการแลกเปลี่ยนที่ยังไม่รับรู้' ในประเภทเอกสารของบริษัทบัญชีนี้ใช้เพื่อปรับสมดุลส่วนต่างของเครดิตทั้งหมดและเดบิตทั้งหมด
 <img class="screenshot" alt="Field Set for Company"   src="{{docs_base_url}}/assets/img/accounts/field_set_company.png">

1. ไปที่ **บัญชี > ตั้งค่า > การประเมินค่าอัตราแลกเปลี่ยน > คลิกใหม่**.
1. เลือกบริษัท
1. คลิกปุ่ม 'รับรายการ' มันจะดึงข้อมูลบัญชีที่มีสกุลเงินแตกต่างจาก 'สกุลเงินเริ่มต้น' ที่ตั้งไว้ในบริษัท
1. การดำเนินการนี้จะดึงอัตราแลกเปลี่ยนใหม่โดยอัตโนมัติหากไม่ได้ตั้งค่าใน Currency Exchange DocType สำหรับสกุลเงินอื่น มันจะดึง 'อัตราแลกเปลี่ยน' ที่ตั้งไว้ใน [อัตราแลกเปลี่ยน](/docs/user/manual/en/accounts/currency-exchange)
 <img class="screenshot" alt="Exchange Rate Revaluation"   src="{{docs_base_url}}/assets/img/accounts/exchange-rate-revaluation.png">

1. ในการส่งปุ่ม **สร้างรายการบันทึกประจำวัน** จะปรากฏขึ้น
<img class="screenshot" alt="Exchange Rate Revaluation Submitting"    src="{{docs_base_url}}/assets/img/accounts/exchange-rate-revaluation-submit.png">

1. กดที่ปุ่มนี้จะสร้างรายการบันทึกประจำวันสำหรับการประเมินค่าอัตราแลกเปลี่ยนใหม่
<img class="screenshot" alt="Journal Entry"   src="{{docs_base_url}}/assets/img/accounts/journal-entry-exchange.png">

1. ในการส่งรายการบันทึกประจำวัน บัญชีแยกประเภททั่วไปจะได้รับผลดังนี้:
<img class="screenshot" alt="Journal Entry"   src="{{docs_base_url}}/assets/img/accounts/journal-entry-exchange-submit.png">

### 3. หัวข้อที่เกี่ยวข้อง
1. [รายการบันทึกประจำวันระหว่างบริษัทภายใน](/docs/user/manual/en/accounts/inter-company-journal-entry)
1. [ใบแจ้งหนี้ระหว่างบริษัท](/docs/user/manual/en/accounts/inter-company-invoices)
