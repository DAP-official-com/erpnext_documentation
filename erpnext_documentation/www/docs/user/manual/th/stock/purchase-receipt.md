<!-- add-breadcrumbs -->
# ใบเสร็จการซื้อ

**ใบเสร็จการซื้อเกิดขึ้นเมื่อคุณยอมรับสินค้าจากซัพพลายเออร์ของคุณโดยปกติเทียบกับใบสั่งซื้อ**

คุณยังสามารถรับใบเสร็จรับเงินได้โดยตรงโดยไม่ต้องมีใบสั่งซื้อ ในการดำเนินการนี้ ให้ตั้งค่าใบสั่งซื้อ
ต้องเป็น "ไม่" ในการตั้งค่าการซื้อ

หากต้องการเข้าถึงรายการใบเสร็จรับเงิน ให้ไปที่:
> หน้าหลัก > สต๊อก > ธุรกรรมสต๊อก > ใบเสร็จการซื้อ

![Purchase Receipt flow](/docs/assets/img/stock/purchase-receipt-flow.png)

## 1. ข้อกำหนดเบื้องต้น
ก่อนสร้างและใช้ใบเสร็จรับเงิน ขอแนะนำให้สร้างสิ่งต่อไปนี้ก่อน:

* [ใบสั่งซื้อ](/docs/user/manual/th/buying/purchase-order)

> หมายเหตุ: ตั้งแต่เวอร์ชัน 13 เป็นต้นไป เราได้แนะนำบัญชีแยกประเภทที่ไม่เปลี่ยนรูปแบบ ซึ่งจะเปลี่ยนกฎสำหรับการยกเลิกรายการสต็อกและการผ่านรายการธุรกรรมสต็อคย้อนหลังใน ERPNext [เรียนรู้เพิ่มเติมที่นี่](/docs/user/manual/th/accounts/articles/immutable-ledger-in-erpnext)


## 2. วิธีสร้างใบเสร็จการซื้อ
ใบเสร็จการซื้อมักจะสร้างจาก [ใบสั่งซื้อ](/docs/user/manual/th/buying/purchase-order) ในใบสั่งซื้อ คลิกที่ สร้าง > ใบเสร็จการซื้อ

หากต้องการสร้างใบเสร็จรับเงิน _manually_ (ไม่แนะนำ) ให้ทำตามขั้นตอนเหล่านี้:

1. ไปที่รายการใบเสร็จการซื้อ คลิกที่ ใหม่
1. ชื่อซัพพลายเออร์และรายการสามารถดึงมาจากใบสั่งซื้อโดยคลิกที่ 'รับรายการจาก > ใบสั่งซื้อ'
1. คุณสามารถตั้งค่าคลังสินค้าที่ยอมรับสำหรับสินค้าทั้งหมดในใบเสร็จการซื้อนี้ ข้อมูลนี้จะถูกดึงออกมาหากตั้งค่าไว้ในใบสั่งซื้อ
1. ในกรณีที่รายการใดมีข้อบกพร่อง ให้ตั้งค่าคลังสินค้าที่ถูกปฏิเสธซึ่งรายการเหล่านั้นจะถูกเก็บไว้
1. เลือกรายการและป้อนจำนวนในตารางรายการ
1. อัตราจะถูกดึงออกมาและจำนวนเงินจะถูกคำนวณโดยอัตโนมัติ
1. คุณสามารถขยายแถวรายการเพื่อเปลี่ยนคลังสินค้าที่ยอมรับสำหรับรายการได้
1. บันทึกและส่ง

    <img class="screenshot" alt="Purchase Receipt" src="{{docs_base_url}}/assets/img/stock/purchase-receipt.png">

คุณยังสามารถเพิ่ม 'Supplier Delivery Note' ลงในใบเสร็จรับเงินได้หากซัพพลายเออร์ของคุณเพิ่มหมายเหตุ
การใช้ช่องกาเครื่องหมาย 'แก้ไขวันที่และเวลาที่โพสต์' คุณสามารถแก้ไขเวลาและวันที่โพสต์ของใบเสร็จการซื้อได้ โดยค่าเริ่มต้น วันที่และเวลาจะถูกตั้งค่าเมื่อคุณคลิกที่ปุ่มใหม่

เป็นการคืนสินค้า: ทำเครื่องหมายที่ช่องนี้หากคุณกำลังส่งคืนสินค้าที่ไม่ได้รับการยอมรับในคลังสินค้าของคุณ

### 2.1 สถานะ

นี่คือสถานะที่ใบเสร็จการซื้อสามารถอยู่ใน:

* **ฉบับร่าง**: บันทึกแบบร่างแล้วแต่ยังไม่ได้ส่งไปยังระบบ
* **To Bill**: ยังคงถูกเรียกเก็บเงินโดยใช้ [ใบแจ้งหนี้การซื้อ](/docs/user/manual/th/accounts/purchase-invoice)
* **เสร็จสมบูรณ์**: ส่งและรับรายการทั้งหมดแล้ว
* **ส่งคืนสินค้าแล้ว**: ส่งคืนสินค้าทั้งหมดแล้ว
* **ยกเลิกแล้ว**: ยกเลิกใบเสร็จการซื้อ
* **ปิด**: วัตถุประสงค์ของการปิดคือการจัดการการปิดระยะสั้น ตัวอย่างเช่น คุณสั่งซื้อ 20 จำนวน แต่ปิดที่ 15 จำนวน ส่วนที่เหลืออีก 5 จะไม่ได้รับหรือเรียกเก็บเงิน

## 3. คุณสมบัติ
### 3.1 รายการสกุลเงินและราคา
สกุลเงินของใบเสร็จการซื้อจะแสดงในส่วนนี้ โดยจะดึงมาจากใบสั่งซื้อ ราคาสินค้าจะถูกดึงมาจากรายการราคาที่ตั้งไว้ การทำเครื่องหมายที่ละเว้นกฎการกำหนดราคาจะละเว้นกฎการกำหนดราคาที่ตั้งไว้ในบัญชี > กฎการกำหนดราคา

เนื่องจากสินค้าที่เข้ามาจะส่งผลต่อมูลค่าของสินค้าคงคลังของคุณ จำเป็นต้องแปลงเป็นสกุลเงินหลักหากคุณสั่งซื้อในสกุลเงินอื่น คุณจะต้องอัปเดตอัตราการแปลงสกุลเงิน หากมี

อ่านเกี่ยวกับ [รายการราคา](/docs/user/manual/th/stock/price-lists)
และ [ธุรกรรมหลายสกุลเงิน](/docs/user/manual/th/accounts/articles/managing-transactions-in-multiple-currency)
เพื่อทราบข้อมูลเพิ่มเติม

### 3.2 รายละเอียดคลังสินค้า
ชุดคลังสินค้าต่อไปนี้จะนำไปใช้กับรายการทั้งหมดในตารางรายการของใบเสร็จการซื้อ คุณสามารถเปลี่ยนโกดังสำหรับแต่ละรายการผ่านตารางได้

* **คลังสินค้าที่ยอมรับ**: นี่คือคลังสินค้าที่คุณจะยอมรับและจัดเก็บรายการที่เข้ามา โดยปกตินี่คือคลังสินค้า'ร้านค้า'
* **คลังสินค้าที่ถูกปฏิเสธ:** นี่คือคลังสินค้าที่คุณจะเก็บสินค้าที่ถูกปฏิเสธซึ่งมีข้อบกพร่องหรือไม่เป็นไปตามเครื่องหมายคุณภาพ

#### Subcontracting

* **Raw Materials Consumed**: In case you're subcontracting, select 'Yes' to consume the Raw Materials from the vendor. Read [Subcontracting](/docs/user/manual/th/manufacturing/subcontracting) to know more.

### 3.3 Items table

* **Barcode**: You can track Items using [barcodes](/docs/user/manual/th/stock/articles/track-items-using-barcode).

* **Scan Barcode**: You can add Items in the Items table by scanning their barcodes if you have a barcode scanner. Read documentation for [tracking items using barcode](/docs/user/manual/th/stock/articles/track-items-using-barcode) to know more.

* The Item Code, name, description, Image, and Manufacturer will be fetched from the Item master.

* **Received and Accepted**: Set the received, accepted and rejected quantity. The UoM is fetched from the Item master. You will need to update the “UOM Conversion Factor” if your Purchase Order for an Item is in a different Unit of Measure (UOM) than what you stock (Stock UOM).

    ![Purchase Receipt Items table](/docs/assets/img/stock/purchase-receipt-item.png)

* **Rate**: The Rate is fetched if set in the [Price List](/docs/user/manual/th/stock/price-lists) and the total Amount is calculated.

* **Item Tax Template**: You can set an Item Tax Template to apply a specific Tax amount to this particular Item. To know more, visit [this page](/docs/user/manual/th/accounts/item-tax-template).

* The Item Weight details per unit and Weight UOM are fetched if set in the Item master.

* **Warehouse and Reference**: You can set the accepted and rejected Warehouses and also add a Quality Inspection, see next section.

* **Serial No, Batch No, and BOM**: If your Item is serialized or batched, you will have to enter Serial Number
and Batch in the Items table. You are allowed to enter multiple Serial Numbers
in one row (each on a separate line) and you must enter the same number of
Serial Numbers as the quantity.

    There are separate fields for entering Serial Numbers of both accepted and rejected Items here. A Batch Number can also be set if you're storing a batch of plastic medicines for example.

    Ticking on 'Allow Zero Valuation Rate' will allow submitting the Purchase Receipt even if the Valuation Rate of the Item is 0. This can be a sample item or due to a mutual understanding with your Supplier.

* You can link a BOM here if the Item is being [subcontracted](/docs/user/manual/th/manufacturing/subcontracting). Linking the BOM here will affect the Stock ledger, i.e. the raw material stock will be deducted from the Supplier Warehouse.

    **Note**: The Item has to be serialized or batched for these features to work. If the Item is serialized a popup will appear where you can enter the Serial Numbers.

* Accounting Dimensions help to tag each transaction with different Dimensions without the need for creating new Cost Centers. You need to create Accounting Dimensions first, to know more, visit [this page](/docs/user/manual/th/accounts/accounting-dimensions).

* Page Break will create a page break just before this item when printing.

### 3.4 Tracking Quality Inspection
If for certain Items, it is mandatory to record Quality Inspections (if you have set it in your Item master), you will need to update the “Quality Inspection" field. The system will only allow you to “Submit” the
Purchase Receipt if you update the “Quality Inspection”.

After enabling Inspection Criteria in the [Item form](/docs/user/manual/th/stock/item#216-inspection-criteria) for Purchase and attaching a Quality Inspection Template there, Quality Inspections can be recorded in Purchase Receipts.

To know more, visit the [Quality Inspection](/docs/user/manual/th/stock/quality-inspection) page.

![Quality Inspection](/docs/assets/img/stock/quality-inspection.png)


### 3.5 Raw Materials Consumed
* The **Consumed Items** table contains the Raw Materials consumed by the Supplier in order to receive the Finished Item.
* The **Get Current Stock** button will fetch the current stock of the Consumed Items from the Supplier Warehouse.
    <img class="screenshot" alt="Purchase Receipt" src="{{docs_base_url}}/assets/img/stock/purchase-receipt-consumed-items.png">

### 3.6 Taxes and Valuation
The Taxes and Charges will be fetched from the [Purchase Order](/docs/user/manual/th/buying/purchase-order).

Visit the [Purchase Taxes and Charges Template](/docs/user/manual/th/buying/purchase-taxes-and-charges-template) page to know more about taxes.

The total taxes and charges will be displayed below the table.

To add taxes automatically via a Tax Category, visit [this page](/docs/user/manual/th/accounts/tax-category).

Make sure to mark all your taxes in the Taxes and Charges table correctly for an accurate valuation.

#### Shipping Rule
A Shipping Rule helps set the cost of shipping an Item. The cost will usually increase with the distance of shipping. To know more, visit the [Shipping Rule](/docs/user/manual/th/selling/shipping-rule) page.


### 3.7 Additional Discount
Any additional discounts to the whole order can be set in this section.
Read [Applying Discount](/docs/user/manual/th/selling/articles/applying-discount) for more details.

### 3.8 More Information
The Status of the Purchase Receipt is shown here and at the top. The various statuses are: Draft, To Bill, Completed, Canceled, and Closed. This section also shows % Amount Billed, i.e. the percentage of amount for which [Sales Invoices](/docs/user/manual/th/accounts/sales-invoice) are created.

### 3.9 Printing Settings

#### Letterhead
You can print your Purchase Receipt on your company's letterhead. Know more [here](/docs/user/manual/th/setting-up/print/letter-head).

'Group same items' will group the same items added multiple times in the items table. This can be seen when your print.

#### Print Headings
Purchase Receipt headings can also be changed when printing the document. You can do this by selecting a **Print Heading**. To create new Print Headings go to: Home > Settings > Printing > Print Heading. Know more [here](/docs/user/manual/th/setting-up/print/print-headings).

### 3.10 After Submitting

A Stock Ledger Entry is created for each Item adding the Item in the Warehouse
by the “Accepted Quantity” If you have rejections, a Stock Ledger Entry is
made for each Rejection. The “Pending Quantity” is updated in the Purchase
Order.

After submitting the Purchase Receipt, the following can be created:

* [Purchase Return](/docs/user/manual/th/stock/purchase-return)
* [Stock Entry](/docs/user/manual/th/stock/stock-entry)
* [Purchase Invoice](/docs/user/manual/th/accounts/purchase-invoice)
* [Retaining Sample Stock](/docs/user/manual/th/stock/retain-sample-stock)

![Purchase Receipt submit](/docs/assets/img/stock/purchase-receipt-submit.png)

### 3.11 Returning a Purchase Order
Once you've received a Purchase Order using a Purchase Receipt, you can create a return entry in case the Item needs to be returned to the [Supplier](/docs/user/manual/th/buying/supplier). To know more, visit the [Purchase Return](/docs/user/manual/th/stock/purchase-return) page.

### 3.12 Skipping Purchase Receipt

If you don't want to create a Purchase Receipt after a Purchase Order and directly want to create a Purchase Invoice, enable the feature for it in [Buying Settings](/docs/user/manual/th/buying/buying-settings#23-purchase-receipt-required).

* * *

#### Changing the value of Items post Purchase Receipt:

Sometimes, certain expenses that add to the total of your purchased Items are known
only after a while. Common example is, if you are importing the Items, you
will come to know of Customs Duty, etc only when your “Clearing Agent” sends
you a bill. If you want to attribute this cost to your purchased Items, you
will have to use the [Landed Cost Voucher](/docs/user/manual/th/stock/landed-cost-voucher). Why “Landed Cost”? Because it represents the charges that you paid when it landed in your possession.

## 4. Related Topics
1. [Delivery Note](/docs/user/manual/th/stock/delivery-note)
1. [Purchase Order](/docs/user/manual/th/buying/purchase-order)
1. [Purchase Invoice](/docs/user/manual/th/accounts/purchase-invoice)
1. [Supplier](/docs/user/manual/th/buying/supplier)
1. [Landed Cost Voucher](/docs/user/manual/th/stock/landed-cost-voucher)
