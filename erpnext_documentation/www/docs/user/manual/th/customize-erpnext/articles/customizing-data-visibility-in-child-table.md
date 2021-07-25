<!-- add-breadcrumbs -->
# การปรับแต่งการเปิดเผยข้อมูลในตารางย่อย

ใน ERPNext มีคุณลักษณะที่เรียกว่ากริดที่แก้ไขได้ ซึ่งช่วยให้ผู้ใช้สามารถเพิ่มค่าในตารางย่อยโดยไม่ต้องเปิดกล่องโต้ตอบ/แบบฟอร์มสำหรับแต่ละแถว

นี่คือวิธีที่ตารางรายการใบเสนอราคาแสดงค่าเมื่อเปิดใช้งานกริดที่แก้ไขได้ มันจะมีสูงสุดสี่คอลัมน์ในตาราง

<img alt="Child Table" class="screenshot" src="{{docs_base_url}}/assets/img/customize/customize-child-table-5.png">

ตามการตั้งค่าเริ่มต้น มีเพียงสี่คอลัมน์ที่แสดงในตารางย่อย ต่อไปนี้เป็นวิธีที่คุณสามารถเพิ่มคอลัมน์ใน Editable Grid ได้

สำหรับฟิลด์ที่จะเพิ่มเป็นคอลัมน์ในตาราง ให้ป้อนค่าในช่องคอลัมน์ นอกจากนี้ ตรวจสอบให้แน่ใจว่าได้ตรวจสอบคุณสมบัติ "เป็นมุมมองรายการ" สำหรับฟิลด์นั้น

<img alt="Child Table" class="screenshot" src="{{docs_base_url}}/assets/img/customize/customize-child-table-2.png">

ตามค่าในฟิลด์คอลัมน์ คอลัมน์จะถูกเพิ่มลงในตารางย่อย ตรวจสอบให้แน่ใจว่ามูลค่ารวมที่เพิ่มในช่องคอลัมน์ไม่เกิน 10 ตามค่าคอลัมน์ ความกว้างของคอลัมน์นั้นจะถูกตั้งค่า

<img alt="Child Table" class="screenshot" src="{{docs_base_url}}/assets/img/customize/customize-child-table-3.png">

**เปลี่ยนเป็นกริดที่ไม่สามารถแก้ไขได้**

หากต้องการให้แสดงค่าเพิ่มเติมในการแสดงตัวอย่างตารางรายการใบเสนอราคา คุณสามารถปิดใช้งานตารางที่แก้ไขได้สำหรับประเภทรายการใบเสนอราคา ขั้นตอนด้านล่าง

<img alt="Child Table" class="screenshot" src="{{docs_base_url}}/assets/img/customize/customize-child-table.gif">

เมื่อปิดการใช้งานกริดที่แก้ไขได้สำหรับรายการใบเสนอราคา ค่าจะแสดงในตัวอย่างตารางรายการใบเสนอราคาด้วยวิธีต่อไปนี้:

<img alt="Child Table" class="screenshot" src="{{docs_base_url}}/assets/img/customize/customize-child-table-4.png">

หากต้องการให้ค่าของฟิลด์เฉพาะแสดงในการแสดงตัวอย่าง ตรวจสอบให้แน่ใจว่าสำหรับฟิลด์นั้น ในเครื่องมือกำหนดแบบฟอร์มเอง จะมีการเลือกคุณสมบัติ "ในมุมมองรายการ"

<img alt="Child Table" class="screenshot" src="{{docs_base_url}}/assets/img/customize/customize-child-table-1.png">

{next}
