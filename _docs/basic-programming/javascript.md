---
title: JavaScript
subtitle: ทำความรู้จักกับภาษา <strong>JavaScript</strong> ก่อนการเรียนรู้การเขียนโปรแกรมเบื้องต้น
icon: fab fa-js-square
difficulty: 1
duration: 1
---

## JavaScript คืออะไร

**JavaScript** (ชื่อย่อ: JS) เป็นภาษาโปรแกรมที่ถูกออกแบบให้ใช้งานบน [Web browser](https://th.wikipedia.org/wiki/เว็บเบราว์เซอร์) เป็นหลัก ที่มีความสำคัญเป็นลำดับต้นๆ เดิมสามารถทำงานได้เพียงบน [Client](https://th.wikipedia.org/wiki/เครื่องลูกข่าย) เท่านั้น และไม่สามารถทำงานบน [Server](https://th.wikipedia.org/wiki/เซิร์ฟเวอร์) ได้ 

### คุณสมบัติ

โดยหลักแล้ว JavaScript มีคุณสมบัติดังนี้

- Web browser ในยุคปัจจุบันมีการรองรับการทำงาน JavaScript ทั้งหมด
- ทำให้เว็บไซต์ที่เคยได้เพียงแสดงผล สามารถทำงาน **เป็นโปรแกรม** ได้

> **หมายเหตุ:** เปรียบเสมือน **รถยนต์** ที่เคยขับได้อย่างเดียว แต่พอมี JavaScript เข้ามาอาจจะช่วยให้รถมีระบบเพิ่มความสะดวก เช่น ดูทีวีได้ มีกล้องท้ายรถ ระบบกันขโมย ดังนั้น JavaScript ไม่ได้จำเป็นในการเขียนเว็บไซต์ แต่จะทำให้เว็บไซต์มีลูกเล่นมากขึ้น

## ทำไมต้อง JavaScript

สาเหตุที่เราเลือกใช้ JavaScript ในการสอนการเขียนโปรแกรมพื้นฐาน เพราะเป็นภาษาที่ **วงการ Startup** ทั้งไทยและต่างประเทศเริ่มนำมาใช้งานมากขึ้น ทั้งการทำเว็บไซต์, [IoT](https://th.wikipedia.org/wiki/อินเทอร์เน็ตของสรรพสิ่ง), [RESTful](https://en.wikipedia.org/wiki/Representational_state_transfer), [ปัญญาประดิษฐ์](https://th.wikipedia.org/wiki/ปัญญาประดิษฐ์) และอื่นๆอีกมากมาย

ซึ่งก็เป็นช่วงที่ [Node.js](https://nodejs.org/) ถูกพัฒนาอย่างก้าวกระโดด โดย Node.js เป็น Engine หนึ่งที่ช่วยให้ JavaScript มีคุณสมบัติพิเศษมากขึ้น และยังมีจุดน่าสนใจดังต่อไปนี้

- ทำให้ JavaScript สามารถทำงานบน Server ได้ จึงทำให้ผู้คนสนใจมากขึ้นเพราะเดิมการจะทำโปรแกรมฝั่ง Client และ Server มักต้องมีการเรียนรู้หลายภาษา แต่การใช้ Node.js จะช่วยให้เหลือเพียงการเรียนรู้ด้วยภาษาเดียวเป็นหลัก
- รองรับการเชื่อมต่อกับ Database ทั้ง [SQL](https://th.wikipedia.org/wiki/ภาษาสอบถามเชิงโครงสร้าง) และ [NoSQL](https://en.wikipedia.org/wiki/NoSQL) เป็นอย่างดี
- ใช้ข้อมูลประเภท [JSON](https://developer.mozilla.org/en-US/docs/Glossary/JSON) เป็นหลัก ทำให้ง่ายต่อการเขียนโปรแกรมในการจัดการข้อมูล
- เบาและเรียบง่าย และมีการใช้ [Non-blocking I/O](https://en.wikipedia.org/wiki/Asynchronous_I/O) ในการทำงาน ทำให้เร็วกว่า มีการใช้ทรัพยากรที่น้อยกว่า
- มีการรองรับบนโปรแกรม IDE และ Editor มากมาย
- มี [Package manager](https://en.wikipedia.org/wiki/Package_manager) ในชื่อ [npm](https://en.wikipedia.org/wiki/Npm_(software)) ที่สามารถจัดการข้อมูลได้อย่างดี

> **หมายเหตุ:** ในบทแรกเราจะสอนใช้งานเฉพาะ JavaScript เป็นพื้นฐานก่อนที่เริ่มใช้งาน Node.js ในภายหลัง

## ทดลองใช้งานบนหน้าเว็บไซต์นี้

การใช้ JavaScript สามารถสั่งทำงานผ่าน Web Browser ได้ทันที ผ่านการใช้ Developer Tools โดยการกดปุ่ม `F12` และเลือก `Console` เพื่อใช้คำสั่งต่างๆของ JavaScript ได้ทันที

> **หมายเหตุ:** ในการใช้งาน Console บน Developer Tools สามารถกด `ESC` เพื่อเปิดใช้งานได้

โดยในส่วนของ Console จะบอกถึงการมีปัญหาของหน้าเว็บไซต์ได้เช่นกัน ซึ่งหากทุกคนที่เปิด Console ดูจะพบว่ามีข้อความสีแดงดังต่อไปนี้

- สำหรับ Google Chrome

{% message danger | Uncaught ReferenceError: Hello is not defined %}

- สำหรับ Mozilla Firefox

{% message danger | ReferenceError: Hello is not defined[Learn More] %}

<script>
  console.log(Hello);
</script>

นั้นเป็นเพราะว่าเราพยายามทำให้หน้าเว็บนี้มี Error อยู่จุดหนึ่งเพื่อทดสอบว่าทุกคนได้เข้าถึงหน้า Console ที่ถูกต้องกันแล้ว แต่หากพบ Error อื่นๆอันนี้ก็จะเกิดความผิดพลาดของในหน้าเว็บที่เราไม่ได้ตั้งใจกันล่ะ 🤐
