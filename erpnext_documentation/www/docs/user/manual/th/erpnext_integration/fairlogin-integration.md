<!-- add-breadcrumbs -->
# การตั้งค่า fairlogin

fairlogin เป็นผู้ให้บริการ oAuth ที่รับรู้ GDPR โดย fairkom.eu

ในการตั้งค่า fairlogin เป็นผู้ให้บริการ oAuth ให้ไปที่:
> หน้าแรก > การรวมระบบ > รหัสเข้าสู่ระบบโซเชียล

## ตั้งค่า keycloak

fairlogin อิงตาม keycloak ดังนั้นพารามิเตอร์อาจคล้ายกันสำหรับการตั้งค่า oAuth ที่กำหนดเองซึ่งอำนวยความสะดวกให้ keycloak

จากที่นั่น คุณเพิ่มไคลเอนต์ใหม่ เลือก open-id เป็นโปรโตคอลไคลเอนต์ และป้อนที่อยู่ของอินสแตนซ์ ERPnext ของคุณเป็น Root, Redirect และ Base URL

กำลังเพิ่มบริการ ERNext ของคุณในฐานะลูกค้า [เสนอเป็นบริการโดย fairkom](https://erp.fairkom.net/cloud/fairlogin-client)

![ERPnext keycloak Settings](/docs/assets/img/erpnext_integrations/fairloginKeycloakERPnext.png)

## ตั้งค่า fairlogin

ในการเปิดใช้งาน fairlogin เป็นตัวเลือกการเข้าสู่ระบบ ERPNext คุณต้องกำหนดค่าพารามิเตอร์ต่อไปนี้:

- URL พื้นฐาน https://id.fairkom.net/auth/realms/fairlogin/
- อนุญาต URL https://id.fairkom.net/auth/realms/fairlogin/protocol/openid-connect/auth
- เปลี่ยนเส้นทาง URL /api/method/frappe.integrations.oauth2_logins.login_via_fairlogin
- เข้าถึง Token URL https://id.fairkom.net/auth/realms/fairlogin/protocol/openid-connect/token
- ปลายทาง API https://id.fairkom.net/auth/realms/fairlogin/protocol/openid-connect/userinfo

![ERPnext fairlogin Settings](/docs/assets/img/erpnext_integrations/fairloginERPnextSettings.png)

ในการเปิดใช้บริการ ระบบจะอนุญาตให้เข้าสู่ระบบด้วยบัญชี fairlogin ใดก็ได้

บทบาทเริ่มต้นของผู้ใช้ใหม่คือ Blogger (ปัจจุบันเป็นแบบฮาร์ดโค้ด)
