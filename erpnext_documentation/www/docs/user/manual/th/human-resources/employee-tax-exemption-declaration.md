<!-- add-breadcrumbs -->
# ใบแจ้งการยกเว้นภาษีพนักงาน

**การยกเว้นภาษีคือการยกเว้นรายได้ ทรัพย์สิน หรือธุรกรรมจากภาษีที่อาจเรียกเก็บจากพนักงาน**

ในช่วงเริ่มต้นของรอบระยะเวลาบัญชีเงินเดือน พนักงานสามารถแจ้งจำนวนการยกเว้นที่พวกเขาจะได้รับจากเงินเดือนที่ต้องเสียภาษี ERPNext อนุญาตให้คุณระบุประเภทการยกเว้นภาษี/ประเภทย่อย จำนวนการยกเว้นภาษี และข้อมูลที่เกี่ยวข้องอื่นๆ ในแบบฟอร์มใบแจ้งการยกเว้นภาษีพนักงาน
 

ในการเข้าถึงใบแจ้งการยกเว้นภาษีพนักงาน ไปที่:

> หน้าแรก > ทรัพยากรบุคคล > ภาษีและสวัสดิการพนักงาน > แจ้งยกเว้นภาษีพนักงาน


## 1. ข้อกำหนดเบื้องต้น

ก่อนสร้างใบแจ้งการยกเว้นภาษีพนักงาน ขอแนะนำให้คุณสร้างสิ่งต่อไปนี้:

* [ลูกจ้าง](/docs/user/manual/th/human-resources/employee)
* [หมวดหมู่การยกเว้นภาษีพนักงาน](#31-employee-tax-exemption-category)
* [หมวดย่อยการยกเว้นภาษีของพนักงาน](#32-employee-tax-exemption-category)


## 2. วิธีสร้างใบแจ้งการยกเว้นภาษีพนักงาน

ในการสร้างใบแจ้งการยกเว้นภาษีพนักงานใหม่:

1. ไปที่: การยกเว้นภาษีพนักงาน > ใหม่
1. เลือกหมวดย่อยการยกเว้นและหมวดการยกเว้น
1. ป้อนจำนวนเงินยกเว้นสูงสุดและจำนวนเงินที่แจ้ง
1. บันทึกและส่ง

    <img class="screenshot" alt="Employee Tax Exemption Declaration" src="{{docs_base_url}}/assets/img/human-resources/employee-tax-exemption-declaration.png">

จำนวนเงินที่ได้รับยกเว้นทั้งหมดจะได้รับการยกเว้นจากรายได้ที่ต้องเสียภาษีประจำปีของพนักงานในขณะที่คำนวณการหักภาษีในบัญชีเงินเดือน

> **หมายเหตุ:** พนักงานสามารถส่งใบแจ้งการยกเว้นภาษีของพนักงานได้เพียงฉบับเดียวเท่านั้นสำหรับระยะเวลาการจ่ายเงินเดือน

## 3. คุณสมบัติ

###3.1 ประเภทการยกเว้นภาษีพนักงาน

การยกเว้นจากเงินเดือนที่ต้องเสียภาษีมักจะจำกัดเฉพาะการใช้จ่ายในหมวดหมู่เฉพาะที่ตัดสินใจโดยรัฐบาลหรือหน่วยงานกำกับดูแล ERPNext ช่วยให้คุณกำหนดค่าหมวดหมู่ต่างๆ ที่อนุญาตให้ยกเว้นได้ ตัวอย่างเหล่านี้ (สำหรับอินเดีย) อาจเป็น 80G, 80C, B0CC เป็นต้น

คุณสามารถกำหนดค่าประเภทการยกเว้นภาษีของพนักงานได้โดยไปที่ **ภาษีและสวัสดิการของพนักงาน > หมวดหมู่การยกเว้นภาษีพนักงาน**

 <img class="screenshot" alt="Employee Tax Exemption Category" src="{{docs_base_url}}/assets/img/human-resources/employee-tax-exemption-sub-category1.png">


### 3.2 หมวดหมู่ย่อยยกเว้นภาษีพนักงาน

ภายใต้แต่ละประเภท อาจมีหลายหัวที่อนุญาตให้ยกเว้นได้ ตัวอย่างเช่น ในอินเดีย หมวดหมู่ย่อยภายใต้ 80C อาจเป็นประกันชีวิตแบบพรีเมียม

คุณสามารถกำหนดค่าประเภทการยกเว้นภาษีพนักงานได้โดยไปที่ **ภาษีและสวัสดิการของพนักงาน > หมวดหมู่ย่อยยกเว้นภาษีพนักงาน**

 <img class="screenshot" alt="Employee Tax Exemption Category" src="{{docs_base_url}}/assets/img/human-resources/employee-tax-exemption-category1.png">


<!--### 3.3 HRA Exemption (Regional - India)

For the current fiscal year, in India, House Rent Allowance (HRA) exemption from taxable earnings is the minimum of:

* The actual amount allotted by the employer as the HRA.
* Actual rent paid less 10% of the basic salary.
* 50% of the basic salary, if the employee is staying in a metro city (40% for a non-metro city).

As part of the Employee Tax Exemption Declaration, employees can also fill out the HRA Exemption. ERPNext calculates the exemption eligible for HRA and exempts it while calculating the taxable earnings. 

Enter the Monthly House Rent and check the 'Rented in Metro City' checkbox if applicable and submit the form. The Annual and Monthly HRA Exemption will be automatically calculated.

Once the declaration is submitted, you can submit the proof of your tax exemption by clicking on the _Submit Proof_ button.


<img class="screenshot" alt="Employee Tax Exemption Declaration" src="{{docs_base_url}}/assets/img/human-resources/hra-exemption.png">

> Note: HRA component needs to be configured in Company master under HRA Settings sections for the HRA exemption to work-->


## 4. หัวข้อที่เกี่ยวข้อง

1. [การยื่นหลักฐานการยกเว้นภาษีของพนักงาน](/docs/user/manual/th/human-resources/employee-tax-exemption-proof-submission)
1. [ใบสมัครสวัสดิการพนักงาน](/docs/user/manual/th/human-resources/employee-benefit-application)
1. [ผลประโยชน์พนักงาน](/docs/user/manual/th/human-resources/employee-benefit-claim)

{next}
