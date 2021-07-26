<!-- add-breadcrumbs -->
# การส่งหลักฐานการยกเว้นภาษีพนักงาน

**พนักงานต้องแสดงหลักฐานการใช้จ่ายทั้งหมดที่ได้รับยกเว้นภาษี สามารถทำได้ผ่านเอกสารยื่นหลักฐานการยกเว้นภาษีพนักงาน**

 โดยปกติจะทำเมื่อสิ้นสุดระยะเวลาการจ่ายเงินเดือน แต่พนักงานสามารถส่งหลักฐานจำนวนเท่าใดก็ได้ ซึ่งแตกต่างจากใบประกาศการยกเว้นภาษีของพนักงาน

> **หมายเหตุ:** สร้างใบประกาศการยกเว้นภาษีพนักงานก่อนสร้างการส่งหลักฐานการยกเว้นภาษีพนักงาน

ในการเข้าถึงการส่งหลักฐานการยกเว้นภาษีของพนักงาน ไปที่:

> หน้าแรก > ทรัพยากรบุคคล > ยื่นหลักฐานการยกเว้นภาษีพนักงาน

## 1. วิธีสร้างการส่งหลักฐานการยกเว้นภาษีของพนักงาน

รายละเอียดจะถูกดึงออกมาแล้วหากคุณคลิกที่ 'ส่งหลักฐาน' จาก [ยกเว้นภาษีพนักงาน](/docs/user/manual/th/human-resources/employee-tax-exemption-declaration) อย่างไรก็ตาม หากคุณต้องการสร้าง 'การส่งหลักฐานการยกเว้นภาษีของพนักงาน' ด้วยตนเอง ให้ทำตามขั้นตอนเหล่านี้

1. ไปที่รายการยื่นหลักฐานการยกเว้นภาษีพนักงาน คลิกที่ใหม่
1. กรอกรายละเอียดตามต้องการ
1. นอกจากนี้ ให้ป้อน 'ประเภทหลักฐาน' (เอกสาร ใบเสร็จ ฯลฯ)
1. แนบหลักฐานโดยคลิกที่ปุ่ม **แนบ** ที่ด้านล่าง
1. ป้อนจำนวนเงินที่ชำระค่าเช่าบ้านเช่าจากวันที่และเช่าถึงวันที่
1. บันทึกและส่ง

    <img class="screenshot" alt="Employee Tax Exemption Proof Submission" src="{{docs_base_url}}/assets/img/human-resources/employee-tax-exemption-proof-submission.png">

 

The _Total Exemption Amount_ will be exempted from annual taxable earnings of the employee while calculating the tax deductions in the last payroll.

> Note: Even if employees submit exemption proofs anytime during the payroll period, ERPNext will only consider this in the last payroll of the Payroll Period for adjusting the final taxes based on the proof submitted. If you need to adjust any additional tax collected or consider proof submission of employees anytime before the last payroll, while processing Payroll Entry (or in the Salary Slip of the employee) check the _Deduct Tax For Unsubmitted Tax Exemption Proof_ option.

<!--### Regional - India
For the current fiscal year, in India, House Rent Allowance (HRA) exemption from taxable earnings is the minimum of:

* The actual amount allotted by the employer as the HRA.
* Actual rent paid less 10% of the basic salary.
* 50% of the basic salary, if the employee is staying in a metro city (40% for a non-metro city).

As part of the Employee Tax Exemption Proof Submission, employees shall also submit proof for HRA Exemption. ERPNext will calculate the exemption eligible for HRA and exempt it while calculating the taxable earnings in the last payroll of the Payroll Period.

> Note: HRA component shall be configured in Company for HRA exemption to work-->

{next}
