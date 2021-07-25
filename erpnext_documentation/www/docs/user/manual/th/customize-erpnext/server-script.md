<!-- add-breadcrumbs -->
# สคริปต์เซิร์ฟเวอร์

**สคริปต์เซิร์ฟเวอร์ช่วยให้คุณกำหนดสคริปต์ Python แบบไดนามิกที่ดำเนินการบนเซิร์ฟเวอร์ในเหตุการณ์ของเอกสารหรือ API**

> เปิดตัวในเวอร์ชัน 12

## 1. วิธีสร้างสคริปต์เซิร์ฟเวอร์

เพื่อสร้าง Server Script

1. หากไซต์ของคุณถูกโฮสต์บน [erpnext.com](https://erpnext.com/) ให้ติดต่อฝ่ายสนับสนุนเพื่อเปิดใช้งานเซิร์ฟเวอร์สคริปต์
ในกรณีของบัญชีที่โฮสต์เอง ให้ตั้งค่า `server_script_enabled` เป็นจริงใน site_config.json ของไซต์ของคุณ
2. ในการเพิ่ม/แก้ไข Server Script ให้ตรวจสอบว่าบทบาทของคุณคือ System Manager
3. สร้างสคริปต์เซิร์ฟเวอร์ใหม่ผ่าน "สคริปต์เซิร์ฟเวอร์ใหม่" ในแถบเครื่องมือ
4. เลือกประเภทของสคริปต์เซิร์ฟเวอร์: Document Event, API, Permission Query
5. ตั้งค่าประเภทเอกสารและชื่อเหตุการณ์ หรือชื่อเมธอด สคริปต์ และบันทึก

## 2. คุณสมบัติ

### 2.1 การเปิดใช้งานสคริปต์เซิร์ฟเวอร์

ต้องเปิดใช้งานสคริปต์เซิร์ฟเวอร์ผ่าน site_config.json

```
bench --site site1.local set-config server_script_enabled true
```

### 2.2 กิจกรรมเอกสาร

สำหรับสคริปต์ที่จะเรียกผ่านเหตุการณ์เอกสาร คุณต้องตั้งค่าประเภทเอกสารอ้างอิงและชื่อเหตุการณ์เพื่อกำหนดทริกเกอร์

- ก่อนแทรก
- ก่อนบันทึก
- หลังจากบันทึก
- ก่อนส่ง
- หลังจากส่ง
- ก่อนยกเลิก
- หลังจากยกเลิก
- ก่อนลบ
- หลังจากลบ
- ก่อนบันทึก (ส่งเอกสาร)
- หลังจากบันทึก (ส่งเอกสาร)

### 2.3 สคริปต์ API

คุณสามารถสร้าง API ใหม่ที่สามารถเข้าถึงได้ผ่าน `api/method/[methodname]` ตามประเภทสคริปต์ "API"

หากคุณต้องการให้ผู้ใช้ทั่วไปเข้าถึง API คุณต้องทำเครื่องหมายที่ "อนุญาตผู้เยี่ยมชม"

การตอบสนองสามารถตั้งค่าได้ผ่าน `frappe.response["message"]` object

### 2.4 แบบสอบถามการอนุญาต

สคริปต์ประเภทนี้ช่วยให้คุณเพิ่มเงื่อนไขที่กำหนดเองในส่วนคำสั่งย่อยสำหรับการค้นหารายการ DocType

ตัวอย่างเช่น สมมติว่าคุณต้องการแสดงรายการของระเบียน ToDo ให้กับผู้ใช้เท่านั้น
ถ้าพวกเขากำหนดเรกคอร์ดหรือถูกกำหนดให้กับพวกเขา สามารถดำเนินการได้โดย
สคริปต์ต่อไปนี้:

```py
conditions = 'owner = {user} or assigned_by = {user}'.format(user=frappe.db.escape(user))
```

The resulting `select` query will look something like this:
```sql
select * from `tabToDo` where owner = 'faris@erpnext.com' or assigned_by = 'faris@erpnext.com'
```

ตอนนี้ มุมมองรายการของ ToDo จะแสดงระเบียนที่จำกัด สิ่งนี้จะ จำกัด also
ผลลัพธ์ที่แสดงในช่องลิงก์

### 2.5 ความปลอดภัย

Frappe Framework ใช้ไลบรารี RestrictedPython เพื่อจำกัดการเข้าถึงวิธีการที่พร้อมใช้งานสำหรับสคริปต์เซิร์ฟเวอร์ เฉพาะวิธีการที่ปลอดภัยตามรายการด้านล่างเท่านั้นที่มีให้ในสคริปต์เซิร์ฟเวอร์

```py
json # json module
dict # internal dict
_ # translator method
_dict # frappe._dict internal method
frappe.flags # global flags

# FORMATTING
frappe.format # frappe.format_value(value, dict(fieldtype='Currency'))
frappe.format_value # frappe.format_value(value, dict(fieldtype='Currency'))
frappe.date_format # default date format
frappe.format_date # returns date as "1st September 2019"

# SESSION
frappe.form_dict # form / request parameters
frappe.request # request object
frappe.response # response object
frappe.session.user # current user
frappe.session.csrf_token # CSRF token of the current session
frappe.user  # current user
frappe.get_fullname # fullname of the current user
frappe.get_gravatar # frappe.utils.get_gravatar_url
frappe.full_name = # fullname of the current user

# ORM
frappe.get_meta # get metadata object
frappe.get_doc
frappe.get_cached_doc
frappe.get_list
frappe.get_all
frappe.get_system_settings

# DB
frappe.db.get_list
frappe.db.get_all
frappe.db.get_value
frappe.db.get_single_value
frappe.db.get_default
frappe.db.escape

# UTILITIES
frappe.msgprint # msgprint
frappe.get_hooks # app hooks
frappe.utils # methods in frappe.utils
frappe.render_template # frappe.render_template,
frappe.get_url # frappe.utils.get_url
frappe.sendmail # send email via server script
frappe.get_print # get pdf for a doc
frappe.attach_print # attach PDF to an email
socketio_port # port for socketio
style.border_color # '#d1d8dd'
guess_mimetype = mimetypes.guess_type,
html2text = html2text,
dev_server # True if in developer mode
```

## 3. ตัวอย่าง

### 3.1 เปลี่ยนค่าของคุณสมบัติก่อนการเปลี่ยนแปลง

ประเภทสคริปต์: ก่อนบันทึก

```py
if "test" in doc.description:
	doc.status = 'Closed'
```

### 3.2 การตรวจสอบแบบกำหนดเอง

ประเภทสคริปต์: "ก่อนบันทึก"

```py
if "validate" in doc.description:
	raise frappe.ValidationError
```

### 3.3. สร้างสิ่งที่ต้องทำโดยอัตโนมัติ

ประเภทสคริปต์: "หลังจากบันทึก"

```py
if doc.allocated_to:
    frappe.get_doc(dict(
        doctype = 'ToDo'
        owner = doc.allocated_to,
        description = doc.subject
    )).insert()
```

### 3.4 API

- ประเภทสคริปต์: API
- ชื่อวิธีการ: `test_method`

```py
frappe.response['message'] = "hello"
```

เรียก: `/api/method/test_method`
