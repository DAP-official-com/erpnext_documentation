<!-- add-breadcrumbs -->
#โฮมเพจ

**หน้าแรกคือหน้า Landing Page เริ่มต้นของเว็บไซต์ของคุณ**

โมดูลเว็บไซต์ของ ERPNext สร้างหน้า Landing Page เริ่มต้นสำหรับเว็บไซต์ของคุณ คุณ
ปรับแต่งได้ในหน้าแรก

ในการเข้าถึงโฮมเพจใน ERPNext ให้ไปที่:

> หน้าแรก > เว็บไซต์ > พอร์ทัล > หน้าแรก

## 1. วิธีตั้งค่าโฮมเพจ
1. เลือกบริษัท
1. ตั้งชื่อ ซึ่งจะแสดงในแท็บเบราว์เซอร์
1. กำหนดค่าส่วนฮีโร่ตามที่อธิบายไว้ในส่วนถัดไป

![Homepage](/docs/assets/img/website/homepage.png)
*โฮมเพจ*

> ตรวจสอบให้แน่ใจว่า 'หน้าแรก' เริ่มต้นของคุณถูกตั้งค่าเป็น 'หน้าแรก' ในการตั้งค่าเว็บไซต์สำหรับ

## 2. หมวดฮีโร่

มีสามวิธีที่คุณสามารถปรับแต่งลักษณะของส่วนฮีโร่ได้:

1. Tag Line และ คำอธิบาย (ค่าเริ่มต้น)
1. สไลด์โชว์หน้าแรก
1. ส่วนฮีโร่ที่กำหนดเอง

### 2.1 แท็กไลน์และคำอธิบาย

หลังจากที่คุณตั้งค่า Tag Line, Description และ Hero Image แล้ว คุณจะมีดี
มองไปข้างหน้า คุณยังสามารถเปลี่ยน URL สำหรับปุ่มสำรวจภายใต้ **URL สำหรับ "ผลิตภัณฑ์ทั้งหมด"**

![Website Homepage](/docs/assets/img/website/website-homepage.png)
*หน้าแรกของเว็บไซต์*


### 2.2 สไลด์โชว์หน้าแรก

ตั้งค่า **ส่วนฮีโร่ตาม** เป็น **สไลด์โชว์** และ **สไลด์โชว์หน้าแรก**
ฟิลด์จะปรากฏขึ้น

![Homepage Slideshow Setting](/docs/assets/img/website/homepage-slideshow-setting.png)
*การตั้งค่าสไลด์โชว์หน้าแรก*

ตอนนี้ เลือกสไลด์โชว์ที่มีอยู่หรือสร้างใหม่ที่แสดงดังนี้:

![Website Slideshow](/docs/assets/img/website/website-slideshow.png)
*สไลด์โชว์เว็บไซต์*

> เพื่อผลลัพธ์ที่ดีที่สุด ตรวจสอบให้แน่ใจว่ารูปภาพสไลด์โชว์ทั้งหมดของคุณมีความสูงเท่ากันและ
> ความกว้างมากกว่าความสูง

![Website Homepage with Slideshow](/docs/assets/img/website/website-homepage-slideshow.gif)

### 2.3 Hero Section ที่กำหนดเอง

ส่วนฮีโร่ประเภทที่สามช่วยให้คุณเขียน HTML ของคุณเองได้

ตั้งค่า **Hero Section Based On** เป็น **Hero Section**

ตอนนี้สร้าง Hero Section ใหม่ ตั้งค่า **ตามส่วน** เป็น **HTML ที่กำหนดเอง**
เขียน HTML ที่กำหนดเองของคุณในฟิลด์ HTML ของส่วน

![Homepage Settings](/docs/assets/img/website/homepage-hero-custom.png)
*การตั้งค่า โฮมเพจ*

คุณสามารถเขียนมาร์กอัป [Bootstrap 4](https://getbootstrap.com/docs/4.3/getting-started/introduction/) ที่ถูกต้องได้ที่นี่

![New Hero Section](/docs/assets/img/website/hero-custom.png)
*Hero Section ใหม่*

มันจะมีลักษณะดังนี้:
![Homepage Hero Custom](/docs/assets/img/website/website-homepage-custom.png)
*Homepage Hero ที่กำหนดเอง*

## 3. สินค้าแนะนำ

คุณยังสามารถแสดงสินค้าเด่นบนโฮมเพจของคุณโดยเพิ่มลงในตารางสินค้า

![Homepage Products Table](/docs/assets/img/website/homepage-featured-products.png)
*โฮมเพจตารางสินค้า*

มันจะมีลักษณะดังนี้:
![Featured Products on Homepage](/docs/assets/img/website/website-featured-products.png)
*สินค้าแนะนำในโฮมเพจ*

## 4. ส่วนของหน้าแรก (โฮมเพจ)

คุณสามารถเพิ่มส่วนที่กำหนดเองบนโฮมเพจของคุณโดยการสร้างส่วนโฮมเพจใหม่

> ไปที่เว็บไซต์ > พอร์ทัล > ส่วนโฮมเพจ

ส่วนของหน้าแรกอาจประกอบด้วยการ์ดหรือ HTML ที่กำหนดเอง กำหนด **ส่วนตาม**
ถึง **การ์ด**

![New Homepage Section](/docs/assets/img/website/new-homepage-section.png)
*ส่วนโฮมเพจใหม่*

เพิ่มรายละเอียดของการ์ดแต่ละใบ เช่น ชื่อเรื่อง คำบรรยาย รูปภาพ เนื้อหา และเส้นทางใน
ตารางบัตรมาตรา.

มันจะมีลักษณะดังนี้:
![Homepage Section](/docs/assets/img/website/homepage-section.png)
*ส่วนโฮมเพจ*

คุณยังสามารถควบคุมลำดับที่ส่วนเหล่านี้ปรากฏโดยการตั้งค่า
**ลำดับมาตรา**. 0 จะแสดงก่อน ตามด้วย 1 และอื่นๆ

> หากต้องการเพิ่มส่วนด้วย HTML ที่กำหนดเอง โปรดดู [ส่วนฮีโร่ที่กำหนดเอง](#23-ส่วนฮีโร่ที่กำหนดเอง)

## 5. หน้าแรกที่กำหนดเอง

ERPNext ช่วยให้คุณมีโฮมเพจที่แตกต่างไปจากเดิมอย่างสิ้นเชิงหากคุณไม่ต้องการ
ใช้ค่าเริ่มต้นที่อธิบายไว้ข้างต้น

ในการตั้งค่าโฮมเพจที่กำหนดเอง:

1. สร้าง [เว็บเพจ](/docs/user/manual/th/website/web-page)
1. ไปที่เว็บไซต์ > ตั้งค่า > การตั้งค่าเว็บไซต์
1. ตั้งค่าโฮมเพจเป็น "เส้นทาง" ของหน้าเว็บของคุณ
   ![](/docs/assets/img/website/custom-homepage.png)

{next}