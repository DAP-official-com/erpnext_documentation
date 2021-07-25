<!-- add-breadcrumbs -->
# แบบการพิมพ์แบบกำหนดเอง

**รูปแบบการพิมพ์คือรูปแบบที่สร้างขึ้นเมื่อคุณต้องการพิมพ์หรือส่งอีเมลธุรกรรม**

ฟีเจอร์นี้มีประโยชน์สำหรับธุรกรรมทั้งหมดใน ERPNext เช่น ธุรกรรมการขายและการซื้อ เอกสาร HR และอื่นๆ อีกมากมาย

ใน ERPNext มีรูปแบบการพิมพ์สามประเภท ได้แก่ รูปแบบการพิมพ์มาตรฐาน รูปแบบการพิมพ์แบบกำหนดเอง และรูปแบบการพิมพ์ HTML

## รูปแบบการพิมพ์มาตรฐาน

เอกสารที่พิมพ์ได้ทุกประเภทใน ERPNext จะมีรูปแบบการพิมพ์มาตรฐานของตัวเองซึ่งสร้างโดย Frappe Framework ตำแหน่งฟิลด์ในรูปแบบการพิมพ์มาตรฐานจะขึ้นอยู่กับตำแหน่งของฟิลด์ที่เกี่ยวข้องในเอกสาร

<img alt="Print Format" class="screenshot" src="{{docs_base_url}}/assets/img/customize/customize-standard-print-format.png">

การเปลี่ยนแปลงใดๆ ที่เกิดขึ้นกับรูปแบบการพิมพ์มาตรฐานจะต้องดำเนินการโดยใช้แบบฟอร์มปรับแต่งเอง คุณยังสามารถชำระเงิน [การเพิ่มฟิลด์ในรูปแบบการพิมพ์](/docs/user/manual/th/customize-erpnext/articles/making-fields-visible-in-print-format)

## รูปแบบการพิมพ์ที่กำหนดเอง

คุณยังสามารถสร้างรูปแบบการพิมพ์แบบกำหนดเองได้โดยใช้เครื่องมือชื่อ [ตัวสร้างรูปแบบการพิมพ์](/docs/user/manual/th/setting-up/print/print-format-builder) เครื่องมือนี้จะช่วยคุณในการสร้างรูปแบบการพิมพ์ที่กำหนดเองอย่างง่ายโดยการลากและวางฟิลด์ในรูปแบบตามที่คุณต้องการ

<img alt="Print Format" class="screenshot" src="{{docs_base_url}}/assets/img/customize/customize-cutom-print-format-builder2.gif">

เมื่อสร้างรูปแบบการพิมพ์โดยใช้ตัวสร้างรูปแบบการพิมพ์ จะสามารถเลือกได้ในรายการรูปแบบการพิมพ์ หลังจากมาตรฐาน

<img alt="Print Format" class="screenshot" src="{{docs_base_url}}/assets/img/customize/customize-custom-print-format-4.png">

สำหรับการสร้างรูปแบบการพิมพ์แบบกำหนดเอง ERPNext มาพร้อมกับเทมเพลตที่กำหนดไว้ล่วงหน้าหลายแบบในสามสไตล์ ได้แก่ โมเดิร์น โมโนโครม และคลาสสิก

หากต้องการสร้างเวอร์ชันของคุณ ให้เปิดเทมเพลตที่มีอยู่จาก:

> ตั้งค่า > การพิมพ์ > รูปแบบการพิมพ์

## รูปแบบการพิมพ์ HTML

สำหรับการสร้างรูปแบบการพิมพ์ HTML คุณจะต้องมีความรู้เกี่ยวกับ HTML, CSS และ Python นี่คือตัวอย่างวิธีการออกแบบรูปแบบการพิมพ์ที่มีรูปแบบเฉพาะเจาะจงมาก

<img alt="Print Format" class="screenshot" src="{{docs_base_url}}/assets/img/customize/customize-custom-print-format-1.png">

รูปแบบการพิมพ์มีให้ที่ฝั่งเซิร์ฟเวอร์โดยใช้ [Jinja Templating Language] (http://jinja.pocoo.org/docs/templates/) แบบฟอร์มทั้งหมดมีสิทธิ์เข้าถึงวัตถุ doc ซึ่งมีข้อมูลเกี่ยวกับเอกสารที่กำลังจัดรูปแบบ คุณยังสามารถเข้าถึงยูทิลิตีทั่วไปผ่านโมดูล frappe หากต้องการความช่วยเหลือในการสร้างรูปแบบการพิมพ์ที่ใช้ HTML โปรดดูที่ [ฟอรัมชุมชน ERPNext](https://discuss.erpnext.com/) หรือเริ่มโพสต์ใหม่สำหรับคำถามของคุณ

สำหรับการจัดสไตล์ มี [Bootstrap CSS Framework](http://getbootstrap.com/) ให้และคุณสามารถเพลิดเพลินกับคลาสต่างๆ ได้อย่างเต็มที่

#### อ้างอิง

1. [ภาษาแม่แบบ Jinja: อ้างอิง](http://jinja.pocoo.org/docs/templates/)
2. [เฟรมเวิร์ก CSS ของ Bootstrap] (http://getbootstrap.com/)

#### การตั้งค่าการพิมพ์

หากต้องการแก้ไข/อัปเดตการตั้งค่าการพิมพ์และ PDF ของคุณ ให้ไปที่:

> ตั้งค่า > การพิมพ์และการสร้างแบรนด์ > การตั้งค่าการพิมพ์

<img alt="Print Format" class="screenshot" src="{{docs_base_url}}/assets/img/customize/customize-print-format-1.png">

<img alt="Print Format" class="screenshot" src="{{docs_base_url}}/assets/img/customize/customize-print-format-2.png">

#### ตัวอย่าง

        {% raw %}<h3>{{ doc.select_print_heading or "Invoice" }}</h3>
        <div class="row">
            <div class="col-md-3 text-right">Customer Name</div>
            <div class="col-md-9">{{ doc.customer_name }}</div>
        </div>
        <div class="row">
            <div class="col-md-3 text-right">Date</div>
            <div class="col-md-9">{{ doc.get_formatted("invoice_date") }}</div>
        </div>
        <table class="table table-bordered">
            <tbody>
                <tr>
                    <th>Sr</th>
                    <th>Item Name</th>
                    <th>Description</th>
                    <th class="text-right">Qty</th>
                    <th class="text-right">Rate</th>
                    <th class="text-right">Amount</th>
                </tr>
                {%- for row in doc.items -%}
                <tr>
                    <td style="width: 3%;">{{ row.idx }}</td>
                    <td style="width: 20%;">
                        {{ row.item_name }}
                        {% if row.item_code != row.item_name -%}
                        <br>Item Code: {{ row.item_code}}
                        {%- endif %}
                    </td>
                    <td style="width: 37%;">
                        <div style="border: 0px;">{{ row.description }}</div></td>
                    <td style="width: 10%; text-align: right;">{{ row.qty }} {{ row.uom or row.stock_uom }}</td>
                    <td style="width: 15%; text-align: right;">{{
                        row.get_formatted("rate", doc) }}</td>
                    <td style="width: 15%; text-align: right;">{{
                        row.get_formatted("amount", doc) }}</td>
                </tr>
                {%- endfor -%}
            </tbody>
        </table>{% endraw %}

## หมายเหตุ

1. ในการรับค่ารูปแบบวันที่และสกุลเงิน ให้ใช้ `doc.get_formatted("fieldname")`
1. สำหรับสตริงที่แปลได้ ให้ใช้ `{{ '{{ _("This string is translated") }}' }}`

{next}
