<!-- add-breadcrumbs -->
# สินค้าคงคลังถาวร

ตามระบบสินค้าคงคลังแบบถาวร การลงบัญชีจะทำสำหรับธุรกรรมสต็อคทุกครั้ง มิฉะนั้นจะทำในช่วงเวลาที่มากขึ้นเช่นรายเดือนหรือรายไตรมาส คลังสินค้าแต่ละแห่งเชื่อมโยงกับหัวหน้าบัญชีที่เกี่ยวข้อง

เมื่อได้รับสินค้าในคลังสินค้าแห่งใดแห่งหนึ่ง ยอดคงเหลือในบัญชีคลังสินค้าจะเพิ่มขึ้น ในทำนองเดียวกัน เมื่อสินค้าถูกจัดส่งจากคลังสินค้า ค่าใช้จ่ายจะถูกจอง และยอดคงเหลือในบัญชีคลังสินค้าจะลดลง

### 1. วิธีเปิดใช้งานสินค้าคงคลังถาวร

1. เปิดใช้งานสินค้าคงคลังถาวร:

    **หน้าแรก > การบัญชี > บริษัท > เปิดใช้งานสินค้าคงคลังถาวร**
    <img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-1.png">
    หากคุณปิดใช้งานสินค้าคงคลังถาวร ผู้ใช้จะต้องจัดการรายการบัญชีด้วยตนเอง
1. ตั้งค่าบัญชีเริ่มต้นต่อไปนี้สำหรับแต่ละบริษัทหากไม่ได้ตั้งค่าไว้ บัญชีเหล่านี้ถูกสร้างขึ้นโดยอัตโนมัติในบัญชี ERPNext ใหม่

    * บัญชีสินค้าคงคลังเริ่มต้น (สินทรัพย์)
    * สต็อกที่ได้รับแต่ไม่เรียกเก็บเงิน (หนี้สิน)
    * บัญชีปรับสต็อก (ค่าใช้จ่าย)
    * ค่าใช้จ่ายรวมอยู่ในการประเมินมูลค่า (ค่าใช้จ่าย)
    * ศูนย์ต้นทุน

1. หากผู้ใช้ต้องการตั้งค่าบัญชีส่วนบุคคลสำหรับแต่ละคลังสินค้า ให้สร้างส่วนหัวของบัญชีสำหรับแต่ละบัญชี ไปที่:

    **บัญชี > ผังบัญชี > บริษัท > การสมัครกองทุน (สินทรัพย์) > สินทรัพย์หมุนเวียน > สินทรัพย์ในสต็อก > *สร้างบัญชีใหม่โดยใช้ชื่อเดียวกับคลังสินค้า***

    ไปที่คลังสินค้าและเชื่อมโยงบัญชีนี้กับคลังสินค้า ซึ่งช่วยในการกรองและดูงบคลังสินค้า

1. สำหรับธุรกรรมสต็อค รายการบัญชีแยกประเภททั่วไปที่ทำกับชุดส่วนหัวบัญชีในคลังสินค้า หากผู้ใช้ไม่ได้ตั้งค่าบัญชีสำหรับคลังสินค้า ระบบจะรับส่วนหัวบัญชีจากคลังสินค้าหลัก หากไม่ได้ตั้งค่าบัญชีสำหรับคลังสินค้าหลัก ระบบจะรับบัญชี (บัญชีสินค้าคงคลังเริ่มต้น) จากข้อมูลหลักของบริษัท

* * *

### 2. ตัวอย่าง

พิจารณาผังบัญชีและการตั้งค่าคลังสินค้าต่อไปนี้สำหรับบริษัทของคุณ:

ผังบัญชี:

* สินทรัพย์ (Dr)
    * สินทรัพย์หมุนเวียน
        * บัญชีลูกหนี้
            * ลูกหนี้
        * สินทรัพย์หุ้น
            * ร้านค้า
            * สินค้าสำเร็จรูป
            * อยู่ระหว่างดำเนินการ
        * สินทรัพย์ภาษี
            *ภาษีมูลค่าเพิ่ม
* หนี้สิน (Cr)
    * หนี้สินหมุนเวียน
        * บัญชีที่สามารถจ่ายได้
            * เจ้าหนี้
        * หนี้สินหุ้น
            * รับสินค้าแล้วแต่ไม่เรียกเก็บเงิน
        * ภาระภาษี
            * ภาษีบริการ
* รายได้ (Cr)
    * รายได้โดยตรง
        * บัญชีขาย
* ค่าใช้จ่าย (ดร.)
    * ค่าใช้จ่ายโดยตรง
        * ค่าใช้จ่ายหุ้น
            * ต้นทุนขาย
            * ค่าใช้จ่ายรวมอยู่ในการประเมินมูลค่า
            * การปรับสต็อก
    * ค่าใช้จ่ายทางอ้อม
        * ค่าจัดส่ง
        * ภาษีศุลกากร

#### 2.1 คลังสินค้า - การกำหนดค่าบัญชี

  * ร้านค้า
  * อยู่ระหว่างดำเนินการ
  * สินค้าสำเร็จรูป

#### 2.2 ใบเสร็จการซื้อ

สมมติว่าคุณซื้อ _10 nos_ ของรายการ "RM0001" ที่ _$200_ และ _5 nos_ ของรายการ "Base Plate" ที่ **$100** จากซัพพลายเออร์ "Arcu Vel Quam Fabricators" ต่อไปนี้เป็นรายละเอียดของใบเสร็จรับเงินการซื้อ:

**ซัพพลายเออร์:** Arcu Vel Quam Fabricators

**รายการ:**

<table class="table table-bordered">
    <thead>
        <tr>
            <th>Item</th>
            <th>Warehouse</th>
            <th>Qty</th>
            <th>Rate</th>
            <th>Amount</th>
            <th>Valuation Amount</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>RM0001</td>
            <td>Stores</td>
            <td>10</td>
            <td>200</td>
            <td>2000</td>
            <td>2250</td>
        </tr>
    </tbody>
</table>
<p><strong>Taxes:</strong>
</p>
<table class="table table-bordered">
    <thead>
        <tr>
            <th>Account</th>
            <th>Amount</th>
            <th>Category</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Shipping Charges</td>
            <td>100</td>
            <td>Total and Valuation</td>
        </tr>
        <tr>
            <td>VAT (10%)</td>
            <td>200</td>
            <td>Total</td>
        </tr>
        <tr>
            <td>Customs Duty</td>
            <td>150</td>
            <td>Valuation</td>
        </tr>
    </tbody>
</table>

**สต็อกแยกประเภท**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-receipt-sl-1.png">

**บัญชีแยกประเภท**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-receipt-gl-2.png">

เมื่อยอดสต็อกเพิ่มขึ้นผ่านใบเสร็จรับเงิน บัญชี "ร้านค้า" จะถูกหักและบัญชีชั่วคราว "ใบเสร็จรับเงินแต่ไม่เรียกเก็บเงิน" จะถูกเครดิต เพื่อรักษาระบบบัญชีสองรายการ ในเวลาเดียวกัน ค่าใช้จ่ายติดลบจะถูกจองในส่วนหัวของบัญชีที่มีประเภทเป็น "การประเมินค่า" หรือ "ยอดรวมและการประเมินมูลค่า" ในตารางภาษีและค่าธรรมเนียมสำหรับจำนวนเงินที่เพิ่มเพื่อวัตถุประสงค์ในการประเมินค่า เพื่อหลีกเลี่ยงการจองค่าใช้จ่ายซ้ำซ้อน

#### 2.3 ใบแจ้งหนี้การซื้อ

ในการรับบิลจากซัพพลายเออร์ สำหรับใบเสร็จการซื้อข้างต้น คุณจะต้องทำใบกำกับสินค้าสำหรับสิ่งเดียวกัน รายการบัญชีแยกประเภททั่วไปมีดังนี้:

**บัญชีแยกประเภททั่วไป**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-pinv-gl-3.png">

บัญชี "ได้รับสินค้าแต่ไม่ถูกเรียกเก็บเงิน" จะถูกหักและทำให้เป็นโมฆะ
ของใบเสร็จการซื้อ

#### 2.4 ใบส่งของ

สมมติว่า คุณมีคำสั่งซื้อจาก "Utah Automation Services" ให้ส่งสินค้าจำนวน 5 รายการ "RM0001"
ที่ 300 ดอลลาร์ ต่อไปนี้เป็นรายละเอียดของใบส่งสินค้า:

**ลูกค้า:** Utah Automation Services

**รายการ:**
<table class="table table-bordered">
    <thead>
        <tr>
            <th>Item</th>
            <th>Warehouse</th>
            <th>Qty</th>
            <th>Rate</th>
            <th>Amount</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>RM0001</td>
            <td>Stores</td>
            <td>5</td>
            <td>300</td>
            <td>1500</td>
        </tr>
    </tbody>
</table>
<p><strong>Taxes:</strong>
</p>
<table class="table table-bordered">
    <thead>
        <tr>
            <th>Account</th>
            <th>Amount</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Service Tax</td>
            <td>150</td>
        </tr>
        <tr>
            <td>VAT</td>
            <td>100</td>
        </tr>
    </tbody>
</table>

**สต็อกแยกประเภท**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-dn-sl-4.png">

**บัญชีแยกประเภท**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-dn-gl-5.png">

เนื่องจากสินค้าถูกส่งจากคลังสินค้า "ร้านค้า" บัญชี "ร้านค้า" จะได้รับเครดิตและ
จำนวนเงินที่เท่ากันจะถูกหักเข้าบัญชีค่าใช้จ่าย "ต้นทุนขาย"
จำนวนเดบิต/เครดิต เท่ากับมูลค่าการประเมินทั้งหมด (ต้นทุนการซื้อ) ของ
รายการขาย และมูลค่าการประเมินจะคำนวณจากความต้องการของคุณ
วิธีการประเมินมูลค่า (FIFO / Moving Average) หรือต้นทุนตามจริงของรายการต่อเนื่อง



    In this example, we have considered the valuation method as FIFO.
    Valuation Rate  = Purchase Rate + Charges Included in Valuation
                    = 200 + (250 / 10)
                    = 225
    Total Valuation Amount  = 220 * 5
                            = 1125



* * *

### 2.5 ใบแจ้งหนี้การขายพร้อมอัพเดทสต็อค

สมมติว่าคุณไม่ได้ทำ ใบจัดส่งสินค้า ขัดกับคำสั่งด้านบน แต่
คุณได้จัดทำใบกำกับสินค้าโดยตรงด้วยตัวเลือก "อัพเดทสต็อค" รายละเอียด
ของใบกำกับสินค้าจะเหมือนกับใบส่งสินค้าข้างต้น

**สต็อกแยกประเภท**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-inv-sl-6.png">

**บัญชีแยกประเภท**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-inv-gl-7.png">

นอกเหนือจากรายการบัญชีปกติสำหรับใบแจ้งหนี้ "ร้านค้า" และ "ต้นทุนของ
บัญชีสินค้าที่ขาย" จะได้รับผลกระทบตามมูลค่าการประเมินด้วยเช่นกัน

#### 2.6 รายการสต็อค (ใบเสร็จรับเงินวัสดุ)

**รายการ:**

<table class="table table-bordered">
    <thead>
        <tr>
            <th>Item</th>
            <th>Target Warehouse</th>
            <th>Qty</th>
            <th>Rate</th>
            <th>Amount</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>RM0001</td>
            <td>Stores</td>
            <td>50</td>
            <td>220</td>
            <td>11000</td>
        </tr>
    </tbody>
</table>

**สต็อกแยกประเภท**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-st-receipt-sl.png">

**บัญชีแยกประเภท**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-st-receipt-gl.png">

#### 2.7 รายการสต็อค (Material Issue)

**รายการ:**

<table class="table table-bordered">
    <thead>
        <tr>
            <th>Item</th>
            <th>Source Warehouse</th>
            <th>Qty</th>
            <th>Rate</th>
            <th>Amount</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>RM0001</td>
            <td>Stores</td>
            <td>10</td>
            <td>220</td>
            <td>2200</td>
        </tr>
    </tbody>
</table>

**สต็อคแยกประเภท**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-st-issue-sl.png">

**บัญชีแยกประเภท**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-st-issue-gl.png">

#### 2.8 รายการสต็อค (การโอนวัสดุ)

**รายการ:**

<table class="table table-bordered">
    <thead>
        <tr>
            <th>Item</th>
            <th>Source Warehouse</th>
            <th>Target Warehouse</th>
            <th>Qty</th>
            <th>Rate</th>
            <th>Amount</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>RM0001</td>
            <td>Stores</td>
            <td>Work In Progress</td>
            <td>10</td>
            <td>220</td>
            <td>2200</td>
        </tr>
    </tbody>
</table>

**สต็อคแยกประเภท**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-st-transfer-sl.png">

**บัญชีแยกประเภท**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-st-transfer-gl.png">

#### 3. หัวข้อที่เกี่ยวข้อง
1. [การบัญชีสินค้าคงคลัง](/docs/user/manual/th/stock/accounting-of-inventory-stock)
1. [ย้ายไปยังคลังสินค้าถาวร](/docs/user/manual/th/stock/articles/migrate-to-perpetual-inventory)