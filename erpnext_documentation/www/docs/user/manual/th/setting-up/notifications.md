<!-- add-breadcrumbs -->
# การแจ้งเตือน

**คุณสามารถกำหนดค่าการแจ้งเตือนต่างๆ ในระบบของคุณเพื่อเตือนกิจกรรมที่สำคัญ**

1. วันที่เสร็จสิ้น
2. วันที่จัดส่งที่คาดไว้ของคำสั่งขาย
3. วันที่จะชำระเงิน
4. แจ้งเตือนในการติดตาม
5. หากได้รับหรือส่งคำสั่งซื้อที่มากกว่ามูลค่าเฉพาะ
6. การแจ้งเตือนการหมดอายุของสัญญา
7. เสร็จสิ้น/การเปลี่ยนแปลงสถานะของงาน

ในการเข้าถึงการตั้งค่าการแจ้งเตือน ไปที่:

> หน้าหลัก > การตั้งค่า > การแจ้งเตือน

## 1. การตั้งค่าการแจ้งเตือน

การตั้งค่าการแจ้งเตือน:

1. เลือกประเภทเอกสารที่คุณต้องการดูการเปลี่ยนแปลง
2. กำหนดกิจกรรมที่คุณต้องการรับชมภายใต้ส่งการแจ้งเตือน เหตุการณ์คือ
    1. ใหม่: เมื่อมีการสร้างเอกสารประเภทที่เลือกใหม่
    2. บันทึก/ส่ง/ยกเลิก: เมื่อมีการบันทึก ส่ง หรือยกเลิกเอกสารประเภทที่เลือก
    4. วันก่อน/วันหลัง: เรียกใช้การแจ้งเตือนนี้สองสามวันก่อนหรือหลัง **วันที่อ้างอิง** ในการตั้งวันชุดวันก่อนหรือหลัง สิ่งนี้มีประโยชน์ในการเตือนคุณถึงวันครบกำหนดที่จะมาถึง หรือเตือนให้คุณติดตามโอกาสในการขายบางรายการ
    3. การเปลี่ยนแปลงค่า: เมื่อค่าเฉพาะในประเภทที่เลือกเปลี่ยนแปลง.
    1. วิธีการ: ส่งการแจ้งเตือนเมื่อมีการทริกเกอร์วิธีการเฉพาะ เช่น before_insert
    1. กำหนดเอง: ส่งการแจ้งเตือนไปยัง [บัญชีอีเมล](/docs/user/manual/th/setting-up/email/email-account) ที่เลือก
3. กำหนดเงื่อนไขเพิ่มเติมหากต้องการ
4. ตั้งค่าผู้รับการแจ้งเตือนนี้ ผู้รับอาจเป็นฟิลด์ของเอกสารหรือรายการที่อยู่อีเมลที่กำหนด
5. เขียนข้อความ
1. บันทึก


### 1.1 การตั้งหัวเรื่อง
คุณสามารถดึงข้อมูลสำหรับสาขาเฉพาะโดยใช้  `doc.[field_name]`. หากต้องการใช้ในหัวเรื่อง/ข้อความ คุณต้องล้อมรอบด้วย `{% raw %}{{ }}{% endraw %}`. สิ่งเหล่านี้เรียกว่าแท็ก [Jinja](http://jinja.pocoo.org/). ตัวอย่างเช่น ในการรับชื่อเอกสาร คุณใช้ `{% raw %}{{ doc.name }}{% endraw %}`. ตัวอย่างต่อไปนี้จะส่งอีเมลเกี่ยวกับการบันทึกงานที่มีหัวเรื่อง "TASK#### ถูกสร้างขึ้นแล้ว"

<img class="screenshot" alt="Setting Subject" src="{{docs_base_url}}/assets/img/setup/notifications/email-alert-subject.png">

### 1.2 Sเงื่อนไขการตั้งค่า

การแจ้งเตือนช่วยให้คุณกำหนดเงื่อนไขตามข้อมูลภาคสนามในเอกสารของคุณได้ ตัวอย่างเช่น หากคุณต้องการรับอีเมลหากลูกค้าเป้าหมายได้รับการบันทึกเป็น "สนใจ" ตามสถานะ คุณจะต้องใส่ `doc.status == "Interested"` ในกล่องข้อความเงื่อนไข  คุณยังสามารถกำหนดเงื่อนไขที่ซับซ้อนมากขึ้นได้โดยการรวมเงื่อนไขเหล่านั้นเข้าด้วยกัน

<img class="screenshot" alt="Setting Condition" src="{{docs_base_url}}/assets/img/setup/notifications/email-alert-condition.png">

ตัวอย่างข้างต้นจะส่งการแจ้งเตือนเมื่อมีการบันทึกงานโดยมีสถานะเป็น "เปิด" และ "วันที่สิ้นสุดที่คาดไว้" สำหรับงานคือวันที่ในหรือก่อนวันที่ที่บันทึกงานนั้น


### 1.3 การตั้งค่าข้อความ

คุณสามารถใช้ทั้งแท็ก Jinja (`{% raw %}{{ doc.[field_name] }}{% endraw %}`) และแท็ก HTML ในกล่องข้อความ

    {% raw %}<h3>Order Overdue</h3>

    <p>Transaction {{ doc.name }} has exceeded Due Date. Please take necessary action.</p>

    <!-- show last comment -->
    {% if comments %}
    Last comment: {{ comments[-1].comment }} by {{ comments[-1].by }}
    {% endif %}

    <h4>Details</h4>

    <ul>
    <li>Customer: {{ doc.customer }}
    <li>Amount: {{ doc.total_amount }}
    </ul>{% endraw %}


### 1.4 การตั้งค่าหลังจากตั้งค่าการแจ้งเตือนแล้ว

บางครั้งเพื่อให้แน่ใจว่าไม่มีการส่งการแจ้งเตือนหลายครั้ง คุณสามารถกำหนดคุณสมบัติที่กำหนดเอง (ผ่านแบบฟอร์มปรับแต่ง) เช่น "ส่งการแจ้งเตือน" แล้วตั้งค่าคุณสมบัตินี้หลังจากส่งการแจ้งเตือนโดยการ **ตั้งค่า** ฟิลด์ **ตั้งค่าคุณสมบัติหลังการแจ้งเตือน**

Then you can use that as a condition in the **Condition** rules to ensure emails are not sent multiple times

<img class="screenshot" alt="Setting Property in Notification" src="{{docs_base_url}}/assets/img/setup/notifications/email-alert-subject.png">

### 1.5 ตัวอย่าง

1. การกำหนดเกณฑ์
    <img class="screenshot" alt="Defining Criteria" src="{{docs_base_url}}/assets/img/setup/notifications/email-alert-1.png">

1. การตั้งค่าผู้รับและข้อความ
    <img class="screenshot" alt="Set Message" src="{{docs_base_url}}/assets/img/setup/notifications/email-alert-2.png">


---

## 2. Slack Notification

หากคุณต้องการให้ส่งการแจ้งเตือนไปยังแชนเนล Slack โดยเฉพาะ คุณยังสามารถเลือกตัวเลือก "Slack" ในตัวเลือกช่องและเลือก Slack Webhook URL ที่เหมาะสม

### 2.1 Slack Webhook URL

Slack webhook URL คือ URL ที่ชี้ไปยังแชนเนล Slack โดยตรง

ในการสร้าง URL ของเว็บฮุค คุณต้องสร้างแอป Slack ใหม่:

1. ไปที่ https://api.slack.com/slack-apps.
2. คลิกที่"Create a Slack App".
    <img class="screenshot" alt="Set Message" src="{{docs_base_url}}/assets/img/setup/notifications/slack_notification_1.png">

3. ตั้งชื่อแอปและเลือกพื้นที่ทำงานที่เหมาะสม เมื่อสร้างแอปแล้ว ให้ไปที่ส่วน "Incoming Webhooks" และเพิ่ม Webhook ใหม่ลงใน Workspace
    Once your app is created, go to the "Incoming Webhooks" section and add a new Webhook to Workspace.
    <img class="screenshot" alt="Set Message" src="{{docs_base_url}}/assets/img/setup/notifications/slack_notification_2.png">

4. คัดลอกลิงก์ที่สร้าง กลับไปที่ ERPNext และใช้เพื่อสร้าง Slack Webhook URL ใหม่ใน Integrations > Slack Webhook URL
    <img class="screenshot" alt="Set Message" src="{{docs_base_url}}/assets/img/setup/notifications/slack_notification_3.png">

5. เลือก Slack และช่อง Slack ของคุณในฟิลด์ช่องและช่อง Slack ภายในการแจ้งเตือนของคุณ


### 2.2 รูปแบบข้อความ

ต่างจากข้อความอีเมล Slack ไม่อนุญาตให้จัดรูปแบบ HTML

คุณสามารถใช้การจัดรูปแบบมาร์กดาวน์แทนซ [Slack Documentation](https://get.slack.help/hc/en-us/articles/202288908-Format-your-messages)

ตัวอย่าง:
    {% raw %}
    *Order Overdue*

    Transaction {{ doc.name }} has exceeded Due Date. Please take the necessary action.


    {% if comments %}
    Last comment: {{ comments[-1].comment }} by {{ comments[-1].by }}
    {% endif %}

    *Details*

    • Customer: {{ doc.customer }}
    • Amount: {{ doc.grand_total }}
    {% endraw %}

<img class="screenshot" alt="Set Message" src="{{docs_base_url}}/assets/img/setup/notifications/slack_notification_4.png">


---

## 3. การแจ้งเตือนระบบ

ใน **Version 12** ใช้การแจ้งเตือนของระบบสำหรับ **การกำหนด** , **กล่าว** , **เอกสารที่ใช้ร่วมกัน** และค่าพลังงาน (Energy Point) การแจ้งเตือนเหล่านี้จะแสดงในรายการแบบเลื่อนลงการแจ้งเตือนที่มุมบนขวาของแถบนำทาง

ใน **Version 13** ด้แนะนำช่องทางเพิ่มเติมในการส่งการแจ้งเตือน - **การแจ้งเตือนระบบ** :

<img class="screenshot" alt="Notifications Dropdown" src="{{docs_base_url}}/assets/img/setup/notifications/system-notifications-channel.png">

การเลือกช่องนี้จะส่งการแจ้งเตือนของระบบเมื่อมีการเรียกใช้การแจ้งเตือน แทนที่จะเป็นอีเมลหรือการแจ้งเตือน Slack

<img class="screenshot" height=400 alt="Notifications Dropdown" src="{{docs_base_url}}/assets/img/setup/notifications/system-notification.png">

การคลิกที่เส้นทางการแจ้งเตือนไปยังเอกสารบันทึกการแจ้งเตือนซึ่งมีหัวเรื่อง ข้อความ และไฟล์แนบที่กำหนดค่าไว้ หากมีการตั้งค่า Attach Print:

<img class="screenshot" alt="Notifications Dropdown" src="{{docs_base_url}}/assets/img/setup/notifications/notification-log.png">

หากจำเป็นต้องมีการแจ้งเตือน Email/Slack และ System Notifications ช่องทางหลักสามารถตั้งค่าเป็น Email หรือ Slack และตัวเลือกนี้สามารถตรวจสอบได้:

<img class="screenshot" alt="Notifications Dropdown" src="{{docs_base_url}}/assets/img/setup/notifications/send-system-notification.png">

## 4. WhatsApp
ใน **Version 13** ได้แนะนำช่องทางเพิ่มเติมในการส่งการแจ้งเตือน - **WhatsApp**:
<img class="screenshot" alt="Notifications WhatsApp Channel" src="{{docs_base_url}}/assets/img/setup/notifications/twilio-channel.png">

หากคุณต้องการให้ส่งการแจ้งเตือนไปยังหมายเลข WhatsApp คุณยังสามารถเลือกตัวเลือก "WhatsApp" ในตัวเลือกช่องและเลือกหมายเลข Twilio ที่เหมาะสมได้ คุณสามารถเพิ่ม Twilio Numbers ในการตั้งค่า Twilio ใน Frappe ข้อความ WhatsApp สามารถส่งไปยังหมายเลขที่มีรหัสประเทศเท่านั้น

<img class="screenshot" alt="Twilio Settings" src="{{docs_base_url}}/assets/img/setup/notifications/twilio-settings.png">

### 4.1 การตั้งค่า Twilio

ในการกำหนดค่าการตั้งค่า Twilio คุณต้องรับข้อมูลรับรอง Twilio จากการตั้งค่าบัญชี Twilio ของคุณก่อน คุณสามารถเพิ่มหมายเลขโทรศัพท์ที่เปิดใช้งานในบัญชี Twilio ของคุณด้วยการเข้าถึง WhatsApp เท่านั้น
<img class="screenshot" alt="Twilio Credentials" src="{{docs_base_url}}/assets/img/setup/notifications/twilio-credentials.png">

### 4.2 รูปแบบข้อความ

WhatsApp อนุญาตให้ผู้ใช้ส่งเฉพาะเทมเพลตข้อความที่ได้รับการอนุมัติล่วงหน้าจากพวกเขาไปยังลูกค้าของคุณ การไม่ทำเช่นนั้นอาจส่งผลให้เกิดการจำกัดบัญชี Twilio ของคุณ
<img class="screenshot" alt="Pre Approved Message Template" src="{{docs_base_url}}/assets/img/setup/notifications/twilio-pre-approved-message.png">


## 5. SMS

ใน **Version 13** ได้แนะนำช่องทางเพิ่มเติมในการส่งการแจ้งเตือน - **SMS**:
<img class="screenshot" alt="SMS Channel" src="{{docs_base_url}}/assets/img/setup/notifications/sms-notification-channel.png">

เพื่อที่จะใช้ช่องทางนี้คุณจะต้องดำเนินการกำหนดค่าของ SMS อ่านเพิ่มเติมได้ที่ [การตั้งค่า SMS](/docs/user/manual/th/setting-up/sms-setting).


### 6. หัวข้อที่เกี่ยวข้อง
1. [การตั้งค่า SMS](/docs/user/manual/th/setting-up/sms-setting)
1. [ติดตามเอกสาร](/docs/user/manual/th/setting-up/email/document-follow)
