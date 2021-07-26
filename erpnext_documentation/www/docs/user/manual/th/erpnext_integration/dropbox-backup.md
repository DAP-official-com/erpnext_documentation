
<!-- add-breadcrumbs -->
#การตั้งค่าการสำรองข้อมูล Dropbox

เราแนะนำให้ลูกค้าสำรองข้อมูลใน ERPNext เสมอ การสำรองข้อมูลฐานข้อมูลจะถูกดาวน์โหลดในรูปแบบของไฟล์ SQL หากจำเป็น ไฟล์ SQL ของการสำรองข้อมูลนี้สามารถกู้คืนได้ในบัญชี ERPNext อื่นเช่นกัน

คุณสามารถทำการดาวน์โหลดสำรองฐานข้อมูลของบัญชี ERPNext ลงในบัญชี Dropbox ของคุณโดยอัตโนมัติ

ในการตั้งค่าการสำรองข้อมูล Dropbox
> หน้าแรก > การผสานการทำงาน > การตั้งค่า Dropbox

##ขั้นตอนต่างกันสำหรับ ERP เวอร์ชันที่มีการจัดการถัดไปและเวอร์ชันโอเพ่นซอร์ส

###ERPnext Managed Version คำแนะนำ

####ขั้นตอนที่ 1: ตั้งค่าความถี่

ตั้งค่าความถี่เพื่อดาวน์โหลดข้อมูลสำรองในบัญชี Dropbox ของคุณ

<img class="screenshot" alt="set frequency" src="{{docs_base_url}}/assets/img/setup/integrations/setup-backup-frequency.png">

####ขั้นตอนที่ 2: อนุญาตการเข้าถึง Dropbox

หลังจากตั้งค่าความถี่และอัปเดตรายละเอียดอื่นๆ แล้ว ให้คลิกที่ 'อนุญาตการเข้าถึง Dropbox' เมื่อคลิกปุ่มนี้ หน้าเข้าสู่ระบบ Dropbox จะเปิดขึ้นในแท็บใหม่ ซึ่งอาจต้องการให้คุณอนุญาตป๊อปอัปสำหรับบัญชี ERPNext ของคุณ

####ขั้นตอนที่ 3: เข้าสู่ระบบ Dropbox

เข้าสู่ระบบบัญชี Dropbox ของคุณโดยป้อนข้อมูลรับรองการเข้าสู่ระบบ

<img class="screenshot" alt="Login" src="{{docs_base_url}}/assets/img/setup/integrations/dropbox-2.png">

####ขั้นตอนที่ 4: อนุญาต

เมื่อเข้าสู่ระบบสำเร็จ คุณจะพบข้อความยืนยันดังต่อไปนี้ คลิกที่ "อนุญาต" เพื่อให้บัญชี ERPNext ของคุณสามารถเข้าถึงบัญชี Dropbox ของคุณได้

<img class="screenshot" alt="Allow" src="{{docs_base_url}}/assets/img/setup/integrations/dropbox-3.png">

ด้วยวิธีนี้ โฟลเดอร์ชื่อ "ERPNext" จะถูกสร้างขึ้นในบัญชี Dropbox ของคุณ และการสำรองฐานข้อมูลจะเริ่มดาวน์โหลดอัตโนมัติในนั้น


## คำแนะนำเวอร์ชันโอเพ่นซอร์ส

####ขั้นตอนที่ 1: ลงชื่อเข้าใช้พื้นที่นักพัฒนา Dropbox

<a href="https://www.dropbox.com/developers/apps" target="_blank" style="line-height: 1.42857143;">https://www.dropbox.com/developers/apps</a>
####ขั้นตอนที่ 2: สร้างแอป Dropbox ใหม่
<img class="screenshot" alt="Create new" src="{{docs_base_url}}/assets/img/setup/integrations/dropbox-open-3.png">
####ขั้นตอนที่ 3: กรอกรายละเอียดสำหรับแอปใหม่ของคุณ
<img class="screenshot" alt="Choose Dropbox API and type as APP Folder" src="{{docs_base_url}}/assets/img/setup/integrations/dropbox-open-1.png">
-
<img class="screenshot" alt="Setup APP Name" src="{{docs_base_url}}/assets/img/setup/integrations/dropbox-open-2.png">
####ขั้นตอนที่ 4: แทรก URI การเปลี่ยนเส้นทางโดเมนที่กำหนดเองของคุณ
`https://{yourwebsite.com}/api/method/frappe.integrations.doctype.dropbox_settings.dropbox_settings.dropbox_auth_finish`
<img class="screenshot" alt="Set Redirect URL" src="{{docs_base_url}}/assets/img/setup/integrations/dropbox_redirect_uri.png">

####ขั้นตอนที่ 5: ในหน้าต่างใหม่ เปิดหน้าการตั้งค่า Dropbox ในการติดตั้ง ERPnext ของคุณ
####ขั้นตอนที่ 6: ตั้งค่าความถี่ในการสำรองข้อมูลและอีเมล
กำหนดความถี่ในการดาวน์โหลดข้อมูลสำรองไซต์ของคุณไปยังบัญชี Dropbox ของคุณ
<img class="screenshot" alt="set frequency" src="/docs/assets/img/setup/integrations/setup-backup-frequency.png">

####ขั้นตอนที่ 7: ปุ่มป้อนข้อมูลจากหน้าต่างแอป Dropbox ของคุณ
จากหน้าแอพ Dropbox ของคุณ ให้ป้อนรหัสแอพและ (ไม่ได้ซ่อน) ความลับของแอพลงในหน้าการตั้งค่า ERP ถัดไป Dropbox

หรือคุณสามารถป้อนด้วยตนเองใน `sites/{sitename}/site_config.json` ดังนี้
<div>
	<pre>
		<code>{ 
 "db_name": "demo", 
 "db_password": "DZ1Idd55xJ9qvkHvUH", 
 "dropbox_access_key": "ACCESSKEY", 
 "dropbox_secret_key": "SECRECTKEY" 
} 		
		</code>
	</pre>
</div>

####ขั้นตอนที่ 8: คลิกบันทึกก่อนดำเนินการต่อ
####ขั้นตอนที่ 9: หลังจากบันทึกแล้ว ให้คลิก "อนุญาตการเข้าถึง Dropbox"
หน้าเข้าสู่ระบบ Dropbox จะเปิดขึ้นในแท็บใหม่ ซึ่งอาจต้องการให้คุณอนุญาตป๊อปอัปสำหรับบัญชี ERPNext ของคุณ
####ขั้นตอนที่ 11: อนุญาตการเข้าถึง Dropbox
เมื่อเข้าสู่ระบบสำเร็จ คุณจะพบข้อความยืนยันดังต่อไปนี้ คลิกที่ "อนุญาต" เพื่อให้บัญชี ERPNext ของคุณสามารถเข้าถึงบัญชี Dropbox ของคุณได้
<img class="screenshot" alt="Allow" src="/docs/assets/img/setup/integrations/dropbox-3.png">
####ขั้นตอนที่ 12: ยืนยันการทำงานของการสำรองข้อมูล
จากหน้า ERPnext Dropbox ให้คลิก 'Take Backup Now' จากนั้นไปที่มุมมองไฟล์ Dropbox คุณควรเห็นโฟลเดอร์ใหม่ใน Dropbox ชื่อ 'Apps' และภายในโฟลเดอร์ {New App} ของคุณ ข้างในควรเป็นโฟลเดอร์สำรองสำหรับทั้งไฟล์และฐานข้อมูล
ดังนั้นสำหรับแอปชื่อ `erpnext' ต่อไปนี้เป็นตำแหน่งของโฟลเดอร์:
```
Database files: /Apps/erpnext/database
Public files: /Apps/erpnext/files
Private files: /Apps/erpnext/private/files
```

> **หมายเหตุ**: หากขนาดการสำรองข้อมูลที่บีบอัดเกิน 1GB (กิกะไบต์) ระบบจะอัปโหลดข้อมูลสำรองล่าสุดที่มีไปยัง Dropbox แทนที่จะสร้างไฟล์สำรองใหม่
