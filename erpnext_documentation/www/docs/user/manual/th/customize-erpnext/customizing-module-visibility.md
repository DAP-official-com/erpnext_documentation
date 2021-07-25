<!-- add-breadcrumbs -->
# การปรับแต่งการมองเห็นโมดูล

**ERPNext เป็นระบบสามารถใช้ได้กับหลายธุรกิจในทุกขนาด การผลิต การศึกษา การค้าปลีก เป็นธุรกิจบางส่วนที่ได้รับประโยชน์สูงสุดจากความสามารถในการใช้งานของระบบ**

โปรดทราบว่า ความสนใจของเจ้าของธุรกิจทุกประเภท ความสามารถในการใช้งานระบบสำหรับธุรกิจต่างๆ ได้รับการแมปเป็น 'โมดูล' ต่างๆ ซึ่งแสดงเป็น 'การ์ด' ในระบบ ในทำนองเดียวกัน โมดูลหลักในระบบ เช่น ทรัพยากรบุคคล การบัญชี CRM เป็นต้น จะแสดงด้วยการ์ดต่างๆ บนแดชบอร์ด

เจ้าของบัญชี ERPNext ทุกคนมีตัวเลือกในการปรับแต่งการมองเห็นโมดูลต่างๆ ตามกรณีธุรกิจของตน

*ในเวอร์ชัน 12 คุณสามารถไปที่ แสดง / ซ่อน โมดูล ที่มุมบนขวาของหน้าจอหลักเพื่อตรวจสอบการมองเห็นของโมดูล**

<img alt="Module Visibility" class="screenshot" src="{{docs_base_url}}/assets/img/customize/customize-module-visibility-2.png">

<img alt="Module Visibility" class="screenshot" src="{{docs_base_url}}/assets/img/customize/customize-module-visibility.gif">

> Note: Modules are automatically hidden for users that have no permissions on the documents within that module. For example, if a User has no permissions on Purchase Order, Purchase Request, Supplier, the “Buying” module will automatically hidden for that User.

หากคุณมีสิทธิ์ในโมดูลใดโมดูลหนึ่ง แต่ยังมองไม่เห็น สาเหตุต่อไปนี้อาจเป็นสาเหตุที่เป็นไปได้

ลองพิจารณาสถานการณ์สมมติที่ผู้ใช้มีสิทธิ์สำหรับโมดูลเว็บไซต์ แต่ไม่สามารถเข้าถึงได้

ตามข้อกำหนดพื้นฐาน ตรวจสอบให้แน่ใจว่าบทบาท "ผู้จัดการเว็บไซต์" ถูกกำหนดให้กับผู้ใช้นั้น เป็นบทบาทมาตรฐานที่อนุญาตบนโมดูลเว็บไซต์ หากมีการกำหนดสิทธิ์ในบัญชีของคุณ ให้ตรวจสอบ บทบาทผู้จัดการการอนุญาต เพื่อทราบว่า หน้าที่ ใดที่มีสิทธิ์บนเว็บไซต์ จากนั้นตรวจสอบว่า หน้าที่ เดียวกันถูกกำหนดให้กับผู้ใช้หรือไม่

<img alt="Module Visibility" class="screenshot" src="{{docs_base_url}}/assets/img/customize/customize-module-visibility-4.png">

นอกจากนี้ คุณควรตรวจสอบด้วยว่าภายใต้การตั้งค่า 'อนุญาตโมดูล' มีการเปิดใช้งานโมดูลที่จำเป็นสำหรับผู้ใช้หรือไม่

<img alt="Module Visibility" class="screenshot" src="{{docs_base_url}}/assets/img/customize/customize-module-visibility-1.png">

โหลดซ้ำอีกครั้งใน ERPNext ของคุณและการเปลี่ยนแปลงที่ทำขึ้นจะถูกนำไปใช้และจะมองเห็นได้ในระบบ

{next}
