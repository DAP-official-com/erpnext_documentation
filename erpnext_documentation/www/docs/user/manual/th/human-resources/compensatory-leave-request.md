<!-- add-breadcrumbs -->
# ลางานเพิ่มเติมหรือชดเชย


**วันลาชดเชย คือ วันลาที่มอบให้แก่ลูกจ้างเป็นการชดเชยการทำงานล่วงเวลาหรือในวันหยุด**

 ERPNext ช่วยให้พนักงานสามารถขอการลาเพื่อชดเชยผ่านเอกสารคำร้องขอการลาเพื่อชดเชยได้ จำเป็นวันที่ที่ระบุไว้ในคำขอการลาเพื่อชดเชยควรอยู่ในรายการวันหยุดโดยปริยาย และพนักงานควรทำเครื่องหมายว่ามาทำงานปกติ
 
 > **หมายเหตุ:** เฉพาะประเภทการลาที่ทำเครื่องหมายว่า 'เป็นการชดเชย' เท่านั้นที่สามารถเลือกได้ในคำขอการลาเพื่อชดเชย

ในการเข้าถึงคำขอการลาเพื่อชดเชย ไปที่:

> หน้าหลัก > ทรัพยากรบุคคล > การลางาน > คำขอลาเพื่อชดเชย


## 1. ข้อกำหนดเบื้องต้น

ก่อนสร้างคำขอลาเพื่อชดเชย จำเป็นต้องสร้างเอกสารดังต่อไปนี้:

* [ลูกจ้าง](/docs/user/manual/th/human-resources/employee)
* [ระยะเวลาการลา](/docs/user/manual/th/human-resources/leave-period)
* [ประเภทการลา](/docs/user/manual/th/human-resources/leave-type)
* [นโยบายการลา](/docs/user/manual/th/human-resources/leave-policy)
* [การจัดสรรการลา](/docs/user/manual/th/human-resources/leave-allocation)
* [รายการวันหยุด](/docs/user/manual/th/human-resources/holiday-list)
* [การเข้างาน](/docs/user/manual/th/human-resources/attendance)


## 2. วิธีสร้างคำขอลางานชดเชย

1. ไปที่รายการคำขอลาเพื่อชดเชย คลิกที่ใหม่
1. เลือกรหัสพนักงาน เมื่อเลือกแล้ว ชื่อพนักงานและแผนกจะถูกดึงออกมาโดยอัตโนมัติ
1. เลือกประเภทการลา
1. เลือกงานจากวันที่และวันที่สิ้นสุดการทำงาน นี่คือวันที่ของวันที่พนักงานทำงานในช่วงวันหยุด
1. ใส่เหตุผล
1. บันทึกและส่ง

    <img class="screenshot" alt="Compensatory Leave Request"
    src="{{docs_base_url}}/assets/img/human-resources/compensatory-leave.png">



ในการส่งคำขอลาเพื่อชดเชย ERPNext จะอัปเดตเรกคอร์ดการจัดสรรการลาสำหรับประเภทการลาเพื่อชดเชย ซึ่งช่วยให้พนักงานสามารถยื่นขอลางานประเภทนี้ได้ในภายหลัง ขึ้นอยู่กับจำนวนใบที่เหลือ


## 3. หัวข้อที่เกี่ยวข้อง

1. [ใบขอลางาน](/docs/user/manual/th/human-resources/leave-application)
1. [Leave Encashment](/docs/user/manual/th/human-resources/leave-encashment)
1. [Leave Block List](/docs/user/manual/th/human-resources/leave-block-list)

