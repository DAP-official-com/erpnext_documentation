<!-- add-breadcrumbs -->
# สิทธิ์ตามบทบาท

**สิทธิ์ในเอกสารต่างๆ สามารถควบคุมได้โดยใช้การอนุญาตตามบทบาท**

ERPNext มีระบบการอนุญาตตามบทบาท หมายความว่าคุณสามารถกำหนดบทบาทให้กับผู้ใช้ และสามารถตั้งค่าการอนุญาตบนบทบาทได้ Role Permissions Manager อนุญาตให้คุณกำหนดบทบาทที่สามารถเข้าถึงเอกสารใดและมีสิทธิ์ใดบ้าง (อ่าน เขียน ส่ง ฯลฯ)

เมื่อกำหนดบทบาทให้กับผู้ใช้แล้ว การเข้าถึงของพวกเขาจะถูกจำกัดไว้สำหรับเอกสารเฉพาะ โครงสร้างการอนุญาตอนุญาตให้คุณกำหนดกฎการอนุญาตที่แตกต่างกันสำหรับฟิลด์ต่างๆ โดยใช้แนวคิดที่เรียกว่า **ระดับของสิทธิ์** ของฟิลด์


## 1. วิธีใช้ตัวจัดการสิทธิ์ตามบทบาท
ในการเริ่มใช้ ตัวจัดการสิทธิ์ตามบทบาท ไปที่:
> หน้าหลัก > ผู้ใช้และการอนุญาต > ตัวจัดการสิทธิ์ตามบทบาท

<img alt="Manage Read, Write, Create, Submit, Amend access using the Role Permissions Manager" class="screenshot" src="{{docs_base_url}}/assets/img/users-and-permissions/setting-up-permissions-leave-application.png">

สิทธิ์จะใช้กับการรวมกันของ:

  * **บทบาท:** ผู้ใช้ได้รับมอบหมายบทบาท และอยู่ในบทบาทเหล่านี้ที่มีการนำกฎการอนุญาตไปใช้ ตัวอย่างเช่น ผู้ใช้ฝ่ายขายอาจได้รับบทบาทของพนักงานและผู้ใช้ฝ่ายขาย

  ตัวอย่างของบทบาท ได้แก่ ผู้จัดการบัญชี พนักงาน ผู้ใช้ทรัพยากรบุคคล ฯลฯ

  * **ประเภทเอกสาร:** เอกสารแต่ละประเภท เอกสารหลักหรือธุรกรรม มีรายการสิทธิ์ตามบทบาทที่แยกจากกันดังที่เห็นในภาพหน้าจอก่อนหน้านี้

  ตัวอย่างประเภทเอกสาร ได้แก่ ใบกำกับสินค้า ใบขอลางาน รายการสินค้า ฯลฯ

  * **ระดับการอนุญาต:** ในแต่ละเอกสาร คุณสามารถจัดกลุ่มฟิลด์ตาม "ระดับ" ฟิลด์แต่ละกลุ่มจะแสดงด้วยตัวเลขที่ไม่ซ้ำกัน (0 ถึง 9) กฎการอนุญาตชุดแยกต่างหากสามารถนำไปใช้กับกลุ่มฟิลด์แต่ละกลุ่มได้ โดยค่าเริ่มต้น ฟิลด์ทั้งหมดจะมีระดับ 0

    ได้รับอนุญาต "ระดับ" เชื่อมต่อสาขาที่มีระดับ X เพื่อกฎได้รับอนุญาตที่มีระดับเอ็กซ์หากต้องการทราบรายละเอียดเพิ่มเติมคลิก [ที่นี่](/docs/user/manual/en/setting-up/articles/managing-perm-level).

  * **ลำดับขั้นตอนของเอกสาร:** สิทธิ์จะถูกนำไปใช้กับแต่ละขั้นตอนของเอกสาร เช่น การสร้าง การบันทึก การส่ง การยกเลิก และการแก้ไข บทบาทสามารถได้รับอนุญาตให้พิมพ์ อีเมล นำเข้าหรือส่งออกข้อมูล เข้าถึงรายงาน หรือกำหนดสิทธิ์ของผู้ใช้

  * **สิทธิ์ของผู้ใช้:** การใช้สิทธิ์ของผู้ใช้ใน ERP ถัดไป ผู้ใช้สามารถถูกจำกัดให้เข้าถึงเฉพาะเอกสารเฉพาะสำหรับประเภทเอกสารนั้น เช่น มีเพียงอาณาเขตเดียวจากทุกอาณาเขต สิทธิ์ของผู้ใช้ที่กำหนดไว้สำหรับประเภทเอกสารอื่นๆ ยังถูกนำไปใช้หากเกี่ยวข้องกับประเภทเอกสารปัจจุบันผ่านช่องลิงก์

    ตัวอย่างเช่น ลูกค้าคือฟิลด์ลิงก์ในใบสั่งขายหรือใบเสนอราคา ใน Role Permissions Manager สิทธิ์ของผู้ใช้สามารถตั้งค่าได้โดยใช้ปุ่ม 'ตั้งค่าสิทธิ์ของผู้ใช้'

    ในการตั้งค่าการอนุญาตของผู้ใช้ตามเอกสาร/ฟิลด์ ให้ไปที่::
    > หน้าหลัก > ผู้ใช้และการอนุญาต > สิทธิ์  > [สิทธิ์ของผู้ใช้](/docs/user/manual/en/setting-up/users-and-permissions/user-permissions)

  * **เพิ่มกฎใหม่**: ในตัวจัดการการอนุญาตบทบาท หากต้องการเพิ่มกฎใหม่ ให้คลิกที่ปุ่มเพิ่มกฎใหม่และกล่องป๊อปอัปจะขอให้คุณเลือกบทบาทและระดับการอนุญาต เมื่อคุณเลือกตัวเลือกนี้และคลิกที่ 'เพิ่ม' จะเป็นการเพิ่มแถวใหม่ในตารางกฎของคุณ

##2. การอนุญาตตามบทบาททำงานอย่างไร

การลาเป็นตัวอย่างที่ดีที่ครอบคลุมทุกด้านของระบบการอนุญาต

* จะถูกสร้างขึ้นโดยพนักงาน สำหรับสิ่งนี้ บทบาทพนักงานควรได้รับสิทธิ์ในการอ่าน เขียน สร้าง แก้ไข

  <img class="screenshot" alt="Giving Read, Write and Create Permissions to Employee for Leave Application"  src="{{docs_base_url}}/assets/img/users-and-permissions/setting-up-permissions-employee-role.png">

* **พนักงาน** ควรจะสามารถเข้าถึง / แอพลิเคชันของเขาทิ้งเธอ ดังนั้น ควรสร้างเรกคอร์ดสิทธิ์ของผู้ใช้ สำหรับ ผู้ใช้-พนักงาน แต่ละชุด

  <img class="screenshot" alt="Limiting access to Leave Applications for a user with Employee Role via User Permissions Manager" src="/docs/assets/img/users-and-permissions/setting-up-permissions-employee-user-permissions.png">

* ถ้าคุณต้องการให้**พนักงาน**เลือกเฉพาะเอกสารในเอกสารอื่นและไม่มีสิทธิ์อ่านเอกสารนั้นทั้งหมด ให้อนุญาตเฉพาะสิทธิ์การเลือก (Select) ให้กับบทบาท พนักงาน

  <img class="screenshot" alt="Limiting access to Leave Applications for a user with Employee Role via User Permissions Manager" src="/docs/assets/img/users-and-permissions/setting-up-select-permissions-employee.png">

* **ผู้จัดการด้านทรัพยาการบุลคคล** ควรจะสามารถดูระบบการลาทั้งหมดได้ สร้างกฎการอนุญาตสำหรับ ผู้จัดการด้านทรัพยาการบุลคคล ที่ระดับ 0 พร้อมสิทธิ์ในการอ่าน ใช้สิทธิ์ผู้ใช้ควรปิดการใช้งาน

  <img class="screenshot" alt="Giving Submit and Cancel permissions to HR Manager for Leave Applications. 'Apply User Permissions' is unchecked to give full access." src="{{docs_base_url}}/assets/img/users-and-permissions/setting-up-permissions-hr-manager-role.png">

* **ผู้อนุญาตการลา** ควรสามารถดูและปรับปรุงระบบการลาของพนักงานภายใต้เขา/เธอ ผู้อนุมัติการลาจะได้รับสิทธิ์อ่านและเขียนที่ระดับ 0 เอกสารพนักงานที่เกี่ยวข้องควรถูกเกณฑ์ในสิทธิ์ของผู้ใช้ของผู้อนุมัติการลา (ความพยายามนี้จะลดลงสำหรับผู้อนุมัติการลาที่กล่าวถึงในเอกสารพนักงาน โดยการสร้างเรกคอร์ดการอนุญาตของผู้ใช้โดยทางโปรแกรม)

  <img class="screenshot" alt="Giving Read, Write and Submit permissions to Leave Approver for Leave Applications.'Apply User Permissions' is checked to limit access based on Employee." src="{{docs_base_url}}/assets/img/users-and-permissions/setting-up-permissions-leave-approver-role.png">

* ควรได้รับการอนุมัติ/ปฏิเสธโดยผู้ใช้ระบบทรัพยากรบุคคลหรือระบบการลาเท่านั้น ฟิลด์สถานะของระบบการลาถูกตั้งค่าไว้ที่ระดับ 1 ผู้ใช้ระบบทรัพยากรบุคคล และผู้อนุญาตการลา จะได้รับสิทธิ์ในการอ่านและเขียนสำหรับระดับ 0 ในขณะที่คนอื่นๆ (ทั้งหมด) จะได้รับสิทธิ์ในการอ่านสำหรับระดับ 1

  <img class="screenshot" alt="Limiting read access for a set of fields to certain Roles" src="/docs/assets/img/users-and-permissions/setting-up-permissions-level-1.png">

* **ผู้ใช้ระบบทรัพยากรบุคคล** ควรสามารถมอบหมายระบบการลาห้กับผู้ใต้บังคับบัญชาของตนได้ผู้ใช้ระบบทรัพยากรบุคคล*ได้รับสิทธิ์ในการตั้งค่าการอนุญาตของผู้ใช้ ผู้ใช้ที่มีบทบาทผู้ใช้ระบบทรัพยากรบุคคล*จะสามารถกำหนดสิทธิ์ผู้ใช้ในการออกจากแอปพลิเคชันสำหรับผู้ใช้รายอื่น

  <img class="screenshot" alt="Let HR User delegate access to Leave Applications by checking 'Set User Permissions'. This will allow HR User to access User Permissions Manager for 'Leave Application'" src="{{docs_base_url}}/assets/img/users-and-permissions/setting-up-permissions-hr-user-role.png">

ในกรณีที่คุณกำหนดบทบาทอย่างถูกต้อง แต่ยังได้รับข้อผิดพลาดเมื่อเข้าถึงเอกสาร โปรดดู[หน้านี้](/docs/user/manual/en/setting-up/articles/report-permission-error).

### 3. หัวข้อที่เกี่ยวข้อง
1. [สิทธิ์ตามบทบาท](/docs/user/manual/en/setting-up/users-and-permissions/role-based-permissions)
1. [สิทธิ์ของผู้ใช้](/docs/user/manual/en/setting-up/users-and-permissions/user-permissions)
1. [การอนุญาตบทบาทสำหรับเพจและรายงาน](/docs/user/manual/en/setting-up/users-and-permissions/role-permission-for-page-and-report)
