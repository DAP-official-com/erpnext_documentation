<!-- add-breadcrumbs -->
#ที่อยู่

คุณสามารถบันทึกที่อยู่ที่เกี่ยวข้องกับลูกค้าเป้าหมาย ลูกค้า ผู้จัดหา ผู้ถือหุ้น หุ้นส่วนการขาย หรือคลังสินค้า

คุณยังสามารถเพิ่มที่อยู่เป็นเรกคอร์ดแบบสแตนด์อโลนโดยไม่ต้องเชื่อมโยงกับเอนทิตีใดๆ ที่ระบุไว้ข้างต้น

ในการเข้าถึงรายการที่อยู่ ให้ไปที่:
> หน้าแรก > CRM > ที่อยู่

## 1. วิธีสร้างที่อยู่

1. ไปที่รายการที่อยู่และคลิกที่ใหม่
1. เลือกประเภทที่อยู่
1. กรอกรายละเอียดใน ที่อยู่บรรทัดที่ 1 ที่อยู่บรรทัดที่ 2 เมือง/เมือง ประเทศ
1. ป้อนที่อยู่อีเมล โทรศัพท์ และแฟกซ์
1. ป้อน DocType และ ชื่อ เพื่อเชื่อมโยงที่อยู่นี้กับลูกค้า ซัพพลายเออร์ ฯลฯ
4. บันทึก
    <img class="screenshot" alt="Contact" src="{{docs_base_url}}/assets/img/crm/address.png">

คุณสามารถเพิ่มที่อยู่จากบันทึกลูกค้าหรือซัพพลายเออร์ได้โดยคลิกที่ปุ่ม "ที่อยู่ใหม่" ดังที่แสดงด้านล่าง

<img class="screenshot" alt="Contact" src="{{docs_base_url}}/assets/img/crm/address-from-supp.png">

ในการนำเข้าที่อยู่หลายรายการจากสเปรดชีต ให้ใช้ [เครื่องมือนำเข้าข้อมูล](/docs/user/manual/th/setting-up/data/data-import).

---
## 2. คุณสมบัติ

### 2.1 เชื่อมโยงที่อยู่ไปยังหลายหน่วยงาน

ที่อยู่อาจเชื่อมโยงกับลูกค้าหลายรายหรือซัพพลายเออร์หลายราย

ที่อยู่สามารถเชื่อมโยงกับลูกค้าและซัพพลายเออร์ได้ในเวลาเดียวกัน

<img class="screenshot" alt="Contact" src="{{docs_base_url}}/assets/img/crm/link_address_to_multipl_entities.png">

### 2.2 ชื่อที่อยู่

หากที่อยู่ไม่ได้เชื่อมโยงกับหน่วยงานใดๆ คุณต้องเพิ่มชื่อด้วยตนเอง

หากที่อยู่เชื่อมโยงกับหน่วยงาน เช่น ลูกค้าหรือซัพพลายเออร์ ชื่อจะถูกสร้างขึ้นโดยอัตโนมัติในรูปแบบ 'ชื่อหน่วยงาน-ประเภทที่อยู่'

<img class="screenshot" alt="Contact" src="{{docs_base_url}}/assets/img/crm/address_title_generation.png">

### 2.3 ที่อยู่สำหรับการเรียกเก็บเงินที่ต้องการและที่อยู่สำหรับจัดส่ง

หากคุณเลือก 'ที่อยู่สำหรับจัดส่งที่ต้องการ' ที่อยู่จะถูกเพิ่มโดยอัตโนมัติในที่อยู่สำหรับจัดส่งในธุรกรรมใบสั่งขาย ใบกำกับสินค้า และใบส่งสินค้า

ในทำนองเดียวกัน หากคุณทำเครื่องหมายที่ 'ที่อยู่สำหรับการเรียกเก็บเงินที่ต้องการ' ที่อยู่จะถูกเพิ่มโดยอัตโนมัติในที่อยู่สำหรับการเรียกเก็บเงินในใบสั่งขาย ใบกำกับสินค้า และธุรกรรมใบส่งของ

<!--### 2.4 GST Localization for India
If the customer/supplier has registered for GST, enter Party GSTIN and GST State.Make sure GSTIN entered is in valid format.

In sales transactions along with address, GSTIN is also fetched.

<img class="screenshot" alt="Contact" src="{{docs_base_url}}/assets/img/crm/gstin_in_so.png">

You can also add addresses of your own company's facilities. Check 'Is Your Company Address', select Company in Link DocType, and Company Name in Link Name for such addresses and you can select them in GST Sales Invoice to print your own address.

<img class="screenshot" alt="Contact" src="{{docs_base_url}}/assets/img/crm/own_company_address.png">


>GSTIN is to be added in Address and not in Customer/Supplier, as one Customer/Supplier may have multiple GSTIN (one for each state where he conducts his business).-->


### 3. หัวข้อที่เกี่ยวข้อง
1. [ลูกค้า](/docs/user/manual/th/CRM/customer)
1. [ซัพพลายเออร์](/docs/user/manual/th/buying)
1. [พันธมิตรการขาย](/docs/user/manual/th/selling)

{next}
