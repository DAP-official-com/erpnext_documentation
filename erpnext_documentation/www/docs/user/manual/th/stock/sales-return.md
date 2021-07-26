<!-- add-breadcrumbs -->
#สินค้าที่ขายถูกส่งคืน

**สินค้าที่ขายถูกส่งคืนเรียกว่า Sales Return**

ธุรกิจมักจะคืนสินค้าที่ขายไปแล้ว ลูกค้าสามารถส่งคืนได้เนื่องจากปัญหาด้านคุณภาพ การไม่จัดส่งในวันที่ตกลงกันไว้ หรือเหตุผลอื่นใด

## 1. ข้อกำหนดเบื้องต้น
ก่อนสร้างและใช้ Sales Return ขอแนะนำให้สร้างสิ่งต่อไปนี้ก่อน:

* [รายการ](/docs/user/manual/th/stock/item)
* [ใบแจ้งหนี้การขาย](/docs/user/manual/th/accounts/sales-invoice)

    หรือ

    [หมายเหตุการจัดส่ง](/docs/user/manual/th/stock/delivery-note)

## 2. วิธีสร้างผลตอบแทนจากการขาย

1. ขั้นแรกให้เปิดใบนำส่งสินค้า / ใบกำกับสินค้าเดิมที่ลูกค้าส่งคืน

    <img class="screenshot" alt="Original Delivery Note" src="{{docs_base_url}}/assets/img/stock/sales-return-original-delivery-note.png">

1. จากนั้นคลิกที่ 'สร้าง > การคืนสินค้าจากการขาย' จะเปิดบันทึกการจัดส่งใหม่โดยทำเครื่องหมายที่ 'คือผลตอบแทน' รายการ อัตรา และภาษีจะเป็นตัวเลขติดลบ

    <img class="screenshot" alt="Return Against Delivery Note" src="{{docs_base_url}}/assets/img/stock/sales-return-against-delivery-note.png">

1. คุณยังสามารถสร้างรายการส่งคืนกับใบแจ้งหนี้การขายเดิม เพื่อส่งคืนสินค้าพร้อมกับใบลดหนี้ ให้ทำเครื่องหมายที่ตัวเลือก "อัปเดตสต็อก" ในการส่งคืนใบกำกับสินค้า

    <img class="screenshot" alt="Return Against Sales Invoice" src="{{docs_base_url}}/assets/img/stock/sales-return-against-sales-invoice.png">

1. เมื่อยื่น หมายเหตุการจัดส่งสินค้าคืน / ใบแจ้งหนี้การขาย ระบบจะเพิ่มยอดสต๊อกในโกดังดังกล่าว เพื่อรักษามูลค่าหุ้นที่ถูกต้อง ยอดสต็อกจะเพิ่มขึ้นตามอัตราการซื้อเดิมของสินค้าที่ส่งคืน

    <img class="screenshot" alt="Return Stock Ledger" src="{{docs_base_url}}/assets/img/stock/sales-return-stock-ledger.png">

1. ในกรณีของการส่งคืนใบกำกับสินค้า บัญชีลูกค้าจะได้รับเครดิตและบัญชีรายได้และภาษีที่เกี่ยวข้องจะถูกหักตามที่แสดงในบัญชีแยกประเภท

    <img class="screenshot" alt="Return Stock Ledger" src="{{docs_base_url}}/assets/img/stock/sales-return-general-ledger.png">

หากเปิดใช้งาน สินค้าคงคลังถาวร ระบบจะโพสต์รายการบัญชีกับบัญชีคลังสินค้าเพื่อซิงค์ยอดคงเหลือในบัญชีคลังสินค้ากับยอดคงเหลือในสต็อกตามบัญชีแยกประเภท

## 3. ผลกระทบต่อการคืนสต็อคผ่านใบส่งสินค้า
ในการสร้างผลตอบแทนจากการขายเทียบกับใบส่งสินค้า:

* **จำนวนที่ส่งคืน** ในบันทึกการจัดส่งเดิมพร้อมกับใบสั่งขายที่เชื่อมโยงกับข้อมูลนั้น ได้รับการอัปเดต

* สถานะของใบนำส่งสินค้าเดิมจะเปลี่ยนเป็น **ส่งคืนแล้ว** หากส่งคืน 100%:
  ![Return Issued](/docs/assets/img/stock/sales-return-issue.png)

## 4. หัวข้อที่เกี่ยวข้อง
1. [การคืนสินค้า](/docs/user/manual/th/stock/purchase-return)
1. [สินค้าคงคลังถาวร](/docs/user/manual/th/stock/perpetual-inventory)
