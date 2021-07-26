<!-- add-breadcrumbs -->
#คืนสินค้าที่ซื้อมา

**สินค้าที่ซื้อที่ถูกส่งคืนเรียกว่าการซื้อคืนสินค้า**

ด้วยคุณสมบัติการคืนสินค้า คุณสามารถส่งคืนสินค้าไปที่
ผู้ผลิต. ซึ่งอาจเกิดจากหลายสาเหตุ เช่น ความชำรุดบกพร่องของสินค้า
คุณภาพไม่ตรงกัน ผู้ซื้อไม่ต้องการสต็อก ฯลฯ

## 1. ข้อกำหนดเบื้องต้น
ก่อนสร้างและใช้การคืนสินค้า ขอแนะนำให้สร้างสิ่งต่อไปนี้ก่อน:

* [รายการ](/docs/user/manual/th/stock/item)
* [ใบแจ้งหนี้การขาย](/docs/user/manual/th/accounts/purchase-invoice)

    หรือ

    [ใบเสร็จรับเงิน](/docs/user/manual/th/stock/purchase-receipt)


## 2. วิธีสร้างการคืนสินค้า
1. ขั้นแรกให้เปิดใบเสร็จรับเงินต้นฉบับ โดยที่ซัพพลายเออร์รายใดส่งสินค้า

    <img class="screenshot" alt="Original Purchase Receipt" src="{{docs_base_url}}/assets/img/stock/purchase-return-original-purchase-receipt.png">

1. คลิกที่ 'สร้าง > คืนสินค้า' จะเปิดใบเสร็จการซื้อใหม่โดยทำเครื่องหมายที่ 'คืนสินค้า' รายการ อัตรา และภาษีจะเป็นตัวเลขติดลบ

    <img class="screenshot" alt="Return Against Purchase Receipt" src="{{docs_base_url}}/assets/img/stock/purchase-return-against-purchase-receipt.png">

1. ในการยื่นแบบ การคืนสินค้าที่ซื้อมา ระบบจะลดปริมาณสินค้าจากคลังสินค้าดังกล่าว เพื่อรักษามูลค่าหุ้นที่ถูกต้อง ยอดสต็อกจะเพิ่มขึ้นตามอัตราการซื้อเดิมของสินค้าที่ส่งคืน

    <img class="screenshot" alt="Return Stock Ledger" src="{{docs_base_url}}/assets/img/stock/purchase-return-stock-ledger.png">

1. ในบัญชีแยกประเภทบัญชี บัญชีสต็อกในมือจะถูกเครดิตและบัญชีที่ได้รับแต่ไม่ถูกเรียกเก็บเงินจะถูกหัก

    <img class="screenshot" alt="Return Stock Ledger" src="{{docs_base_url}}/assets/img/stock/purchase-return-general-ledger.png">

หากเปิดใช้งาน สินค้าคงคลังถาวร ระบบจะโพสต์รายการบัญชีกับบัญชีคลังสินค้าเพื่อซิงค์ยอดคงเหลือในบัญชีคลังสินค้ากับยอดคงเหลือของสต็อคตามบัญชีแยกประเภท

## 3. ผลกระทบต่อการคืนสต็อคผ่านใบเสร็จรับเงิน
ในการสร้างการคืนสินค้ากับใบเสร็จการซื้อ:

* **จำนวนที่ส่งคืน** ในใบเสร็จรับเงินต้นฉบับพร้อมกับใบสั่งซื้อใดๆ ที่เชื่อมโยงกับใบสั่งซื้อนั้นได้รับการอัปเดต

* สถานะของใบเสร็จการซื้อเดิมจะเปลี่ยนเป็น **ส่งคืนแล้ว** หากส่งคืน 100%:
  ![Return Issued](/docs/assets/img/stock/purchase-return-issue.png)

### 4. หัวข้อที่เกี่ยวข้อง
1. [การคืนสินค้า](/docs/user/manual/th/stock/sales-return)
1. [สินค้าคงคลังถาวร](/docs/user/manual/th/stock/perpetual-inventory)
