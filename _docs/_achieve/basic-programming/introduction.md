---
title: บทนำก่อนเรียน
subtitle: อ่านกันสักนิด ก่อนเริ่มต้นเขียนโปรแกรมไปกับพวกเรา
duration: 60
level: ง่าย
---

# บทนำก่อนเรียน

ก่อนเริ่มต้นการเขียนโปรแกรม เราก็อยากจะปรับพื้นฐานของทุกคนให้เข้าใจตรงกันก่อน จะได้นำความรู้พื้นฐานใช้ในบทต่อๆไปอย่างไม่มีสะดุดด้วย

## ตรรกศาสตร์

โดยเนื้อหานี้จะเป็นพื้นฐานในระดับ **ม.4** หรืออาจจะต่ำกว่านั้น ซึ่งค่อนข้างจำเป็นสูงในการเขียนโปรแกรมอย่างมาก เพราะสามารถช่วยให้มีการคิดวิเคราะห์อย่างเป็นระบบระเบียบมากขึ้น

### ตรรกศาสตร์คืออะไร

ตรรกศาสตร์หรือภาษาอังกฤศ Logic (โลจิก) คือการศึกษาเชิงปรัชญาว่าด้วยการให้เหตุผลต่างๆนาๆ โดยปกติแล้วเป็นส่วนสำคัญของคณิตศาสตร์อย่างมาก แต่ก็สำคัญในด้านคอมพิวเตอร์ในระดับทีเรียกได้ว่าขาดไม่ได้เลยทีเดียว เพราะช่วยให้ลำดับเงื่อนไขต่างๆของการทำงานระบบ

### ประพจน์

ประพจน์ คือประโยคที่มีค่าเป็น **จริงหรือเท็จ** อย่างใดอย่างหนึ่งเท่านั้น มาถึงขั้นนี้หากเคยเรียนกันแล้วก็จะเข้าใจว่ามันต้องมีเครื่องหมาย `T` กับ `F` หรือก็คือ `T ^ F = F` แต่ถ้าไม่คุ้นเคยก็มาเรียนกับเราในไม่กี่บรรทัดได้ครับ เพราะไม่ใช่เรื่องยากเลย

โดยเราจะอธิบายด้วยประโยคบอกเล่าแทนการใช้เครื่องหมายนะครับ เพื่อความเข้าใจอย่างรวดเร็ว อีกทั้งเครื่องหมายในเชิงคณิตศาสตร์ที่ต้องมาเขียนแจกแจงต่างๆ มันไม่ได้นำไปใช้กับการเขียนโปรแกรมเลย ซึ่งเราจะโฟกัสคำว่า `และ` กับ `หรือ` เป็นหลัก

ยกตัวอย่างเช่น

> วันนี้อาหารเช้ามีไก่ทอด `และ` ไข่เจียว

- ในกรณีที่อาหารเช้าเรามีทั้งไก่ทอด และ มีไข่เจียวจริงๆ ประโยคนี้ก็จะเป็น `จริง` ทันที ก็ไม่ได้โกหกนะ!
- แต่จะเกิดอะไรขึ้นหากเพื่อนพูดกับว่า "วันนี้อาหารเช้ามีไก่ทอดและไข่เจียวนะ!" ขณะที่บนโต๊ะกับข้าวของคุณที่เพื่อนเราทำให้ มันมีไข่เจียวอย่างเดียวไม่เห็นจะมีไก่สักตัวเลย? ดังนั้นก็เท่ากับว่าเขาโกหก หรือก็คือเป็นประโยค `เท็จ`
- แล้วจะเกิดอะไรขึ้นอีก หากเขาพูดเหมือนเดิม แต่คราวนี้บนโต๊ะมีเพียงข้าวสวยให้คุณ มันต้องเป็นเรื่องตลกแน่ๆ ไม่รู้เหมือนกันว่าเพื่อนคุณกำลังสนุกอะไรอยู่แต่มันเป็น `เท็จ` อย่างแน่นอน

ขณะที่อีกประโยคหนึ่ง

> วันนี้อาหารเช้ามีไก่ทอด `หรือ` ไข่เจียว

- ในกรณีที่อาหารเช้ามีทั้งไก่ทอดและไข่เจียว ประโยคก็ต้องเป็นจริงอยู่แล้วก็มันมีทั้งสองอย่าง
- แต่หากเรานั่งบนโต๊ะกำลังข้าวและเพื่อนก็ถามเราว่า "วันนี้อาหารเช้ามีไก่ทอดหรือไข่เจียวหรอ?" ขณะที่อาหารเช้าก็มีแต่ไข่เจียวอย่างเดียว แต่ถามว่าเพื่อนเรามันถามถูกหรือไม่? ก็ถูกอยู่นะ ก็อย่างน้อยๆมันมีไข่เจียว ดังนั้นแปลว่าเป็นประโยค `จริง` เพราะเพื่อนถามถูก
- แต่เกิดเรากินข้าวสวยอย่างเดียวเพราะถังแตกเงินเดือนยังไม่ออก อยู่ดีๆเพื่อนถามเหมือนเดิม แต่ไม่ดูให้ดีๆล่ะว่าโซ้ยข้าวขาวอย่างเดียวอยู่ ก็จะเป็นประโยค `เท็จ` ทันทีเพราะเพื่อนถามผิด หรือกำลังล้อเล่นคุณอยู่นั้นแหละ

> ดังนั้นสรุปง่ายๆของ **จริงและเท็จ** ได้ว่า
> - คำว่า **และ** จะเป็นจริงก็ต่อเมื่อจริงทั้งสองอย่างถูกทั้งคู่ แต่ถ้าอย่างใดอย่างหนึ่งผิดจะถือว่าเป็นเท็จทันที
> - คำว่า **หรือ** จะเป็นเท็จก็ต่อเมื่อเท็จทั้งสองอย่าง แต่ถ้าอย่างใดอย่างหนึ่งเป็นจริง ก็จะถือว่าเป็นจริงทันที
>
> เจ้าก็จงเอาเทคนิคนี้ไปหลอกแฟนว่า "วันนี้เรากลับบ้านดึกเพราะเราไปเที่ยวกับเพื่อนหรือไปทำงานมา" มันจะเป็นจริงทันทีไม่ได้พูดโกหกเลย แต่จริงข้อไหนกันนะ? หรืออาจจะจริงทั้งคู่ก็ได้นะ สับสนไปอีก 🤣

และนอกจากนี้ยังมี **นิเสธ** หรือ **การเชื่อมประพจน์** อีกด้วย ซึ่งเนื้อหาที่ลึกไปมากกว่านี้เราสามารถนำเสนอในรูปแบบของโปรแกรมได้ ดังนั้นเราจะไปสอนต่อกันในบทเขียนโปรแกรมจริง

## นามธรรม

นามธรรมมาจากคำว่า **Abstract** (แอ็ปสแต็ก) ซึ่งมีความหมายตรงกันข้ามกับรูปธรรม กล่าวคือรูปธรรมเป็นสิ่งหนึ่งที่เป็นวัตถุ แสดงให้เห็นได้ และบอกได้ว่ามันคืออะไร ขณะที่นามธรรมเป็นเพียงความคิดที่อยู่ในหัว ไม่ได้ออกมาเป็นรูปร่างแต่อย่างใด ซึ่งโปรแกรมเมอร์ก็จะมีหน้าที่ทำให้นามธรรมทั้งหมด ก่อร่างสร้างตัวจนกลายเป็นรูปธรรมขึ้นมาได้

ยกตัวอย่างเช่น คุณต้องการบอกเพื่อนให้ไปซื้อพิซซ่า มันคงจะเป็นเรื่องที่ดีหากเพื่อนคุณรู้ทันทีว่าควรจะไปซื้อพิซซ่าที่ไหน ร้านอะไร เอาเงินที่ใคร เพราะอะไรถึงโดนฝากซื้อ แล้วจะเอาพิซซ่าหน้าไหน หรือคิดเล็กคิดน้อยได้มากกว่านั้น เช่น จะเดินทางไปนานขนาดไหน โทรสั่งเองจะนานกว่าหรือเปล่า เหล่านี้จัดว่าเป็นนามธรรมทั้งหมด ซึ่งการที่คนมีความคิดที่ดี สามารถคิดเผื่อคนอื่นได้ หรือเข้าใจสถานการณ์เร็ว ก็อาจจะมีความคิดด้านการพัฒนาโปรแกรมที่ได้เปรียบกว่าคนอื่นๆได้

> **เพิ่มเติม:** อาจจะงงๆกับความหมาย เอาให้เข้าใจง่ายๆคือเราจะเปลี่ยนจากความคิดที่อยู่ในหัวที่อยากได้อย่างนู้นอย่างนี้ (นามธรรม) กลายเป็นโปรแกรมอะไรสักอย่างที่คนใช้งานได้จริงๆ (รูปธรรม)

### Pseudocode

Pseudocode อ่านได้ว่า "ซูโดโค้ด" *(ไม่ได้อ่านว่า เพรซูโดโค้ด)* หรือภาษาไทยอาจจะเรียกกันว่า **รหัสเทียม** เป็นการเขียนโปรแกรมในรูปภาษาคนแทน ถือว่าเป็นขั้นตอนหนึ่งของการฝึกนำความคิดแบบนามธรรมได้ดีสำหรับผู้ที่ยังเขียนโปรแกรมไม่เป็น และยังมีบทบาทหลายๆด้านที่ทำให้การสื่อสารระหว่างคนที่เป็นโปรแกรมเมอร์ สามารถเข้าใจนามธรรมจากลูกค้าที่ต้องการได้ด้วย

ยกตัวอย่างการอธิบายขั้นตอนของภายในร้านพิซซ่าแบบซูโดโค้ด โดยใช้ **Application** บนมือถือ

> - ให้ลูกค้าดาวน์โหลด Application จากนั้นเข้าที่โปรแกรม
>   - หากไม่เคยสมัคร ต้องทำการสมัครผ่าน Facebook
>   - หากเป็นลูกค้าเก่า ให้ใช้ Facebook เดิมเข้าระบบได้ทันที
>     - ทำการเลือกพิซซ่าที่ต้องการ และเลือกวิธีการสั่งซื้อว่าต้องการรับที่ร้านหรือจัดส่ง
>       - ในกรณีที่ลูกค้าเลือกรับที่ร้านเอง ให้ออกบิลบนมือถือและใช้ Application ในการยืนยัน
>       - ในกรณีที่ลูกค้าเลือกจัดส่ง ให้ทำการพิกัดบน **GPS** ตำแหน่งจัดส่ง และมีการเพิ่มราคาหลังออกบิล
>         - กรอกรหัสรับส่วนลด หากลูกค้ามีคูปอง
>           - ให้ลูกค้าทำการชำระผ่านบัตร หรือช่องทางอื่นๆ
>             - ออกใบเสร็จ และเสร็จขั้นตอน
>             - ในกรณีที่จัดส่ง ลูกค้าสามารถติดตามเวลาที่คาดว่าจะจัดส่งถึงบ้านได้ ตั้งแต่เวลาการปรุง และการจัดส่ง

อ่านๆไปเราอาจจะรู้สึกว่า มันก็แค่ข้อความอธิบายปกติไม่ใช่หรอ? จริงๆแล้วสิ่งนี้ก็ถือว่าเป็นซูโดโค้ดได้ เพราะมันไม่ได้มีรูปแบบที่ชัดเจนในการเขียนเลย โดยเป้าหมายหลักของการเขียนซูโดโค้ดคือต้องการสื่ออะไรบางอย่างผ่านข้อความให้โปรแกรมเมอร์สามารถเข้าใจขั้นตอนต่างๆได้ในย่อหน้าเดียวได้

และหากจะเขียนให้ดูเป็นโปรแกรมเมอร์มากกว่าเดิม อาจจะเขียนได้ดังนี้

```markdown
Open application
  If customer has user
    Then login
    Else register
      User select order <- need user authentication
        If customer use method: retail
          Then billing <- complete for application
        Else if customer use method: shipping
          Then billing with prepare shipping method <- complete for application
          Additional:
            Customer can select location from GPS
```

> **หมายเหตุ:** โดยส่วนมากซูโดโค้ดมักนิยมเขียนเป็นภาษาอังกฤษ เพราะเป็นภาษากลาง และสามารถใช้ศัพท์สั้นๆให้เข้าใจได้ดีกว่าภาษาไทย หรือบางครั้งอาจจะเขียนคล้ายๆกับการเขียนโปรแกรมจริงๆเพียงแต่ไม่มีสัญลักษณ์ที่ถูกต้อง
>
> - **Application** หรือแอปพริเคชั่น โดยศัพท์ทั่วไปอาจจะแปลได้ว่า "ใบสมัคร" แต่ในของโลกโปรแกรมคือ "โปรแกรมประยุกต์"
> - **GPS** มาจากคำว่า Global Positioning System แปลได้ตรงๆว่า "ระบบระบุตำแหน่งทั่วโลก" หรือก็คือระบบที่สามารถระบุได้ว่าอุปกรณ์นี้อยู่ในตำแหน่งใด มักไว้ใช้เพื่อการนำทางหรือติดตามอุปกรณ์

## ตัวแปร

ตัวแปรเรียกในภาษาอังกฤษว่า Variable (แวรี่เอเบอร์) ถ้าเราเรียนคณิตศาสตร์มาได้สักระดับ ม.4 ก็คงจะทราบกันดีกว่า **ตัวแปร** คือการแทนค่าอย่างหนึ่ง หรือถ้าหากเราเขียนรายงานการใช้ตัวแปรของการวิจัย ก็คือคุณลักษณะหรือคุณสมบัติของบางสิ่งที่สามารถแปรค่าเป็นอย่างอื่นได้

> **ยกตัวอย่าง:**
> - ตัวแปร "A" มีค่าเท่ากับ 5 ดังนั้นโจทย์ของ `A + 5 = ?` จะเท่ากับ `10`
> - ตัวแปร "น้ำ" จะมีคุณสมบัติ `ของเหลว` หากนำไปแช่แข็งก็จะกลางเป็น `ของแข็ง`

อย่างตัวอย่างด้านบนเพียงแค่มองตัวอักษร `A` ให้เท่ากับ `5` เข้าไว้ ดังนั้นพอบวกกันจึงได้ `10` (5 + 5 = 10) แต่ในกรณีที่ตัวแปรอาจจะมีการเปลี่ยนแปลง เช่น...

```markdown
กำหนด A มีค่าเท่ากับ 5
A + 10 = 15

กำหนด A มีค่าเท่ากับ 7
A + 10 = 17

กำหนดให้ B มีค่าเท่ากับ 10
A + B = 17
```

ถ้าดูจากตัวอย่างจะเห็นได้ว่าเดิม `A` เคยมีค่าเท่ากับ `5` ก่อนจะถูกเปลี่ยนค่าในภายหลัง

### การเขียนตัวแปรในภาษาโปรแกรม

สำหรับภาษาโปรแกรมอาจจะ