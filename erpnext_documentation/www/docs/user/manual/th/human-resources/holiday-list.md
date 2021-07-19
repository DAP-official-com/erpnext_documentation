<!-- add-breadcrumbs -->
#รายการวันหยุด

**รายการวันหยุดเป็นรายการที่มีวันที่ของวันหยุด**

องค์กรส่วนใหญ่มี Holiday List มาตรฐานสำหรับพนักงานของตน อย่างไรก็ตาม บางแห่งอาจมีรายการวันหยุดที่แตกต่างกันตามสถานที่หรือแผนกต่างๆ ใน ERPNext คุณสามารถกำหนดค่ารายการวันหยุดหลายรายการและกำหนดให้กับพนักงานของคุณตามความต้องการของคุณ

หากต้องการเข้าถึงรายการวันหยุด ให้ไปที่:

> หน้าหลัก > ทรัพยากรบุคคล > ระบบการลา > รายการวันหยุด



## 1. วิธีสร้างรายการวันหยุด

1. ไปที่รายการวันหยุด คลิกที่ใหม่
2. ป้อนชื่อรายการวันหยุด โดยสามารถอ้างอิงตามปีงบประมาณหรือสถานที่ตั้งหรือแผนกได้ตามต้องการ
3. เลือกจากวันที่และวันที่สำหรับรายการวันหยุด


    <img class="screenshot" alt="Holiday List" src="{{docs_base_url}}/assets/img/human-resources/holiday-list-1.png">

## 2. Features 

Some of the additional features in the Holiday List are as follows:

### 2.1 Adding Weekly Holidays 

You can quickly add Weekly Offs in the Holiday List as follows:

1. In the 'Add Weekly Holidays' section, select the day in the Weekly Off field.
2. Click on the 'Add to Holidays' button.
3. Save.

Once the Weekly Offs are added, it is reflected in the Holidays table.

> **Note:** You can add multiple days in the Weekly Offs.

<img class="screenshot" alt="Holiday List" src="{{docs_base_url}}/assets/img/human-resources/holiday-list-2.gif">


You can also add specific days (like festival holidays) manually by clicking on the 'Add row' option in the Holidays table.

<img class="screenshot" alt="Holiday List" src="{{docs_base_url}}/assets/img/human-resources/holiday-list-3.png">

> **Note:** Each time a new holiday is updated in the Holidays table, the Total Holidays field gets updated.

### 2.2 Holiday List in Company

You can set a default Holiday List at the company-level in the Company master in the 'Default Holiday List' field.


<img class="screenshot" alt="Holiday List" src="{{docs_base_url}}/assets/img/human-resources/default-holiday-list-company.png">


### 2.3 Holiday List in Employee 

If you have created multiple Holiday List, select a specific Holiday List for an Employee in the respective master.

When an Employee applies for Leave, the days mentioned in the Holiday List will not be counted, as they are holidays already. 

> **Note:** If you have specified a Holiday List in the Employee master, then that Holiday List will be given priority as compared to the default Holiday List of the Company.
You can form as many holiday lists as you wish. For example, if you have a factory, you can have one list for the factory workers and another list for office staff. You can manage between many lists by linking a Holiday List to the respective Employee.

### 2.4 Holiday List in Workstation

You can also set a Holiday List at workstation-level as shown in the screenshot below. 

<img class="screenshot" alt="Holiday List" src="{{docs_base_url}}/assets/img/human-resources/holiday-list-workstation.png">

The dates in the Holiday List tagged in the [Workstation](/docs/user/manual/th/manufacturing/workstation) master will be considered as the days the Workstation will remain closed.


## 3. Related Topics

1. [Leave Allocation](/docs/user/manual/th/human-resources/leave-allocation)
1. [Leave Period](/docs/user/manual/th/human-resources/leave-period)
1. [Leave Policy](/docs/user/manual/th/human-resources/leave-policy)
1. [HR Settings](/docs/user/manual/th/human-resources/hr-settings)


