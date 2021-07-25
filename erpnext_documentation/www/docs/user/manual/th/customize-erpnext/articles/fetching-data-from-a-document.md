<!-- add-breadcrumbs -->
#ดึงข้อมูลจากเอกสาร

**คำถาม:** เราติดตามช่องหมายเลขใบสั่งซื้อและวันที่สั่งซื้อของลูกค้าในใบสั่งขาย เพื่อให้ค่าเหล่านี้ถูกดึงเข้าสู่ Sales Invoice ด้วย เราได้แทรก Custom Field ใน Sales Invoice อย่างไรก็ตาม เมื่อเราสร้างใบกำกับสินค้าจากใบสั่งขาย รายละเอียดใบสั่งซื้อของลูกค้าจะไม่ถูกดึงข้อมูล

**คำตอบ:** เมื่อดึงข้อมูลจากธุรกรรมหนึ่งไปยังอีกธุรกรรมหนึ่ง การแมปข้อมูลจะเสร็จสิ้นตามชื่อฟิลด์ หากธุรกรรมสองรายการมีช่องที่มีชื่อเหมือนกันทุกประการ ค่าของธุรกรรมนั้นจะถูกจับคู่

ตัวอย่างเช่น ถ้าคุณต้องการให้ดึง PO No. และวันที่ PO ของลูกค้าจากใบสั่งขายไปยัง Sales Invoice คุณควรตรวจสอบให้แน่ใจว่าฟิลด์ที่กำหนดเองที่เพิ่มในใบแจ้งหนี้การขายมีชื่อฟิลด์เดียวกันกับในใบสั่งขาย

ใบสั่งขาย (ฟิลด์มาตรฐาน)

<img class="screenshot" alt="Standard fields in Sales Order" src="{{docs_base_url}}/assets/img/customize/customize-fetch-data-1.png">

ใบแจ้งหนี้การขาย (ฟิลด์กำหนดเอง)

<img class="screenshot" alt="Custom Field in Sales Invoice" src="{{docs_base_url}}/assets/img/customize/customize-fetch-data-2.png">

เนื่องจากชื่อสำหรับฟิลด์ที่เกี่ยวข้องกับ PO ของลูกค้าจะเหมือนกันในใบสั่งขายและใบแจ้งหนี้การขาย เมื่อสร้างใบแจ้งหนี้การขายจากใบสั่งขาย ค่าในฟิลด์เหล่านี้จะถูกดึงข้อมูลโดยอัตโนมัติ

<img class="screenshot" alt="Values fetching from Sales Order to Sales Invoice" src="{{docs_base_url}}/assets/img/customize/customize-fetch-data-3.png">

<img class="screenshot" alt="Values fetching from Sales Order to Sales Invoice" src="{{docs_base_url}}/assets/img/customize/customize-fetching-data.gif">

{next}
