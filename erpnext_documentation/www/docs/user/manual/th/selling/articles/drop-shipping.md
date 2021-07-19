<!-- add-breadcrumbs -->
#ดรอปชิป

**Drop shipping** เป็นเทคนิคการจัดการห่วงโซ่อุปทานที่ผู้ค้าปลีกไม่เก็บสินค้าไว้ในสต็อก แต่จะโอนคำสั่งซื้อของลูกค้าและรายละเอียดการจัดส่งไปยังผู้ผลิต ผู้ค้าปลีกรายอื่น หรือผู้ค้าส่ง ซึ่งจะจัดส่งสินค้าไปยังลูกค้าโดยตรง

ใน ERPNext คุณสามารถสร้าง Drop Shipping โดยสร้างใบสั่งซื้อเทียบกับใบสั่งขาย

> การขาย > เอกสาร > ใบสั่งขาย > ใบสั่งซื้อ

#### การตั้งค่าใน Item Master

ตั้งค่า **_Delivered by Supplier (Drop Ship)_** และ **_Default Supplier_** ในรายการหลัก

<img class="screenshot" alt="Setup Item Master" src="{{docs_base_url}}/assets/img/selling/setup-drop-ship-on-item-master.png">

#### การตั้งค่าใบสั่งขาย
หาก Drop Shipping ตั้งค่าไว้ที่รายการหลัก ก็จะตั้งค่า **Supplier จัดส่งถึงลูกค้า** และ **Supplier** ใน รายการใบสั่งขาย โดยอัตโนมัติ

คุณสามารถตั้งค่า Drop Shipping ในรายการใบสั่งขาย ใต้ส่วน **จัดส่ง** ให้ตั้งค่า **ซัพพลายเออร์ส่งถึงลูกค้า** และเลือก **ซัพพลายเออร์** ว่าจะสร้างใบสั่งซื้อใด

<img class="screenshot" alt="Setup Drop Shipping on Sales Order Item" src="{{docs_base_url}}/assets/img/selling/setup-drop-ship-on-sales-order-item.png">

#### สร้างใบสั่งซื้อ
หลังจากส่งใบสั่งขายแล้ว ให้สร้างคำสั่งซื้อขาย

<img class="screenshot" alt="Setup Drop Shipping on Sales Order Item" src="{{docs_base_url}}/assets/img/selling/drop-ship-sales-order.png">

จากใบสั่งขาย รายการทั้งหมดที่มี **ซัพพลายเออร์ส่งถึงลูกค้า** ตรวจสอบแล้วหรือ **ซัพพลายเออร์** (จับคู่กับซัพพลายเออร์ที่เลือกในป๊อปอัปสำหรับซัพพลายเออร์) ที่กล่าวถึง จะถูกแมปไปยังใบสั่งซื้อ

มันจะตั้งค่าลูกค้า ที่อยู่ลูกค้า และผู้ติดต่อโดยอัตโนมัติ

หลังจากส่งใบสั่งซื้อ หากต้องการอัปเดตสถานะการจัดส่ง ให้ใช้ปุ่ม **ทำเครื่องหมายว่าจัดส่งแล้ว** บนใบสั่งซื้อ มันจะอัปเดตเปอร์เซ็นการส่งมอบและปริมาณที่ส่งมอบในใบสั่งขาย

<img class="screenshot" alt="Purchase Order for Drop Shipping" src="{{docs_base_url}}/assets/img/selling/drop-ship-purchase-order.png">

<span style="color:#18B52D">**_Close_**</span>,เป็นคุณลักษณะใหม่ที่นำมาใช้ใน **ใบสั่งซื้อ** และ **ใบสั่งขาย** เพื่อปิดหรือทำเครื่องหมายการปฏิบัติตาม

<img class="screenshot" alt="Close Sales Order" src="{{docs_base_url}}/assets/img/selling/close-sales-order.png">

###รูปแบบการพิมพ์ของ Drop Shipping
คุณสามารถแจ้งซัพพลายเออร์โดยส่งอีเมลหลังจากส่งใบสั่งซื้อโดยแนบรูปแบบการพิมพ์ Drop Shipping

<img class="screenshot" alt="Drop Dhip Print Format" src="{{docs_base_url}}/assets/img/selling/drop-ship-print-format.png">

###วิดีโอช่วยเหลือเกี่ยวกับ Drop Ship

<div class="embed-container">
    <iframe src="https://www.youtube.com/embed/hUc0hu_XLdo?rel=0" frameborder="0" allowfullscreen>
    </iframe>
</div>

{next}    