<!-- add-breadcrumbs -->
#เปิดสต๊อก

**สต็อคเปิดคือจำนวนและมูลค่าของวัสดุที่บริษัทมีเพื่อขายหรือใช้เมื่อต้นรอบระยะเวลาบัญชี**

สต็อคปิดของรอบระยะเวลาบัญชีก่อนหน้าจะกลายเป็นสต็อคเปิดของรอบระยะเวลาบัญชีปัจจุบัน

## 1. ข้อกำหนดเบื้องต้น

* สร้าง [คลังสินค้า](/docs/user/manual/th/stock/warehouse)
* เชื่อมโยงคลังสินค้ากับบัญชีแยกประเภทที่เหมาะสม

## 2. การเปิดสต็อคสำหรับรายการที่ไม่ต่อเนื่อง

หากต้องการโพสต์การเปิดสต็อก โปรดไปที่หน้า [การกระทบยอดสต็อก](/docs/user/manual/th/stock/stock-reconciliation)


## 3. การเปิดสต็อคสำหรับรายการที่เรียงลำดับและต่อเนื่องกัน

สร้างระเบียน [Batch](/docs/user/manual/th/stock/batch) และ [Serial No](/docs/user/manual/th/stock/serial-no) ไว้ล่วงหน้า ในการโพสต์สต็อคเปิดสำหรับรายการต่อเนื่องและแบบแบทช์:

1. ไปที่ **สต็อค > ธุรกรรมสต็อค > รายการสต็อค > ใหม่**
1. เลือก 'Material Receipt' ใน 'Stock Entry Type'
1. เลือกคลังสินค้าใน 'คลังเป้าหมายเริ่มต้น'
1. ในตารางรายการ เลือกรหัสรายการ จำนวน และอัตราพื้นฐาน
1. สำหรับรายการแบทช์ ให้เลือก Batch No.
1. สำหรับรายการซีเรียลไลซ์ ให้เลือก Serial No.
1. บันทึกและส่ง

## 4. วีดีโอ
<div>
    <div class="embed-container">
        <iframe src="https://www.youtube.com/embed/nlHX0ZZ84Lw?end=120" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen>
        </iframe>
    </div>
</div>

### 5. หัวข้อที่เกี่ยวข้อง
1. [การบัญชีสินค้าคงคลัง](/docs/user/manual/th/stock/accounting-of-inventory-stock)
1. [รายการสต็อค](/docs/user/manual/th/stock/stock-entry)
1. [การกระทบยอดสต็อก](/docs/user/manual/th/stock/stock-reconciliation)
