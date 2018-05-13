---
title: Conditional
subtitle: การทำงานของโปรแกรมตาม <strong>เงื่อนไข</strong>
icon: fas fa-exchange-alt
difficulty: 4
duration: 4
useful: 5
---

## if()

การใช้ `if()` จะเป็นการตรวจสอบเงื่อนไขภายในวงเล็บ `()` โดยจะมีเงื่อนไขดังต่อไปนี้

- ข้อมูลที่เป็น `true` `ค่าที่มากกว่า 1` `มีข้อความใดๆก็ได้` จะถือว่าเป็น **จริง** และทำเงื่อนไขดังกล่าว
- แต่หากมีค่าเป็น `false` `0` `null` `undefined` หรือที่บอกได้ว่าไม่มีค่ากับเป็นค่าเท็จ จะถือว่าเป็น **เท็จ** และทำให้ข้ามเงื่อนไขดังกล่าว

```javascript
let money = true;
let girlFriend = false;
if (money) {
  alert('You have a money'); // คุณมีเงิน?
}
if (girlFriend) {
  alert('You have a girl friend'); // คุณมีแฟน?
}

// ลองกด </> แล้วแก้ให้ girlFriend เป็น true ดูสิ 👏🤣
```

หรือทดลองจากตัวอย่างด้านล่างสำหรับในการเปรียบเทียบข้อมูลหลายๆประเภท

```javascript
let number = 1
  , bool = true
  , string = 'foobar';
if (number) {
  alert('Number is true!');
}
if (bool) {
  alert('Boolean is true!');
}
if (string) {
  alert('String is true!');
}
alert('All tests are done');
```

```javascript
let number = 0
  , bool = false
  , string = '';
if (number) {
  alert('Number is true!');
}
if (bool) {
  alert('Boolean is true!');
}
if (string) {
  alert('String is true!');
}
alert('All tests are done');
```

หรืออาจจะยกตัวอย่างพร้อมการใช้ `confirm()` เพื่อช่วยให้เข้าใจมากขึ้น

```javascript
let isProgrammer = confirm('Are you programmer?');
alert(`Your answer is ${isProgrammer}; Type is ${typeof(isProgrammer)}`);
if (isProgrammer) { // เมื่อเงื่อนไข isProgrammer เป็นจริง โปรแกรมจะทำงานภายใน { ... }
  alert('Hello world!'); // แสดงข้อความหากเข้าเงื่อนไข
}
// กรณีตอบ Cancel หรือเท็จ จะทำให้ข้ามโปรแกรมด้านบน และจบการทำงานของโปรแกรม
```

## else

การใช้ `else` จะเป็นการเข้าเงื่อนไข **อื่นๆ** ที่เหลือทั้งหมดของเงื่อนไข `if()` ต่างๆ โดยจะมี Statement ที่ถูกทำงานภายในเครื่องหมายปีกกา `{}` ของ `if()` เท่านั้น

```javascript
let answer = prompt('1 + 3 = ?');
if (answer == 4) { // หากตอบว่า 4 จะเข้าเงื่อนไขนี้
  alert('Correct!');
}
else { // หากตอบ "อื่นๆ" ที่ไม่ใช่ 4 จะเข้าเงื่อนไขนี้
  alert('Wrong!!');
}
```

```javascript
let genderMale = confirm('Are you male?');
if (genderMale) { // เมื่อตอบตกลง
  alert('Male');
}
else { // เมื่อตอบยกเลิก
  alert('Female...or shemale? 🤔');
}
```

> **หมายเหตุ:** การใช้ `prompt()` จะได้ค่า String กลับมา ดังนั้นไม่สามารถใช้การเทียบของ `===` ได้หากต้องการเทียบกับ Number เช่น
>
> ```javascript
> let answer = prompt('1 + 3 = ?');
> alert(`answer is ${answer}; type is ${typeof(answer)}`);
> if (answer === 4) { // String === Number ไม่ได้ เพราะข้อมูลประเภทไม่ตรงกัน
>   alert('Correct!');
> }
> else {
>   alert('Wrong!!');
> }
> ```

> **คำเตือน:** การใช้ `else` จะไม่มีเครื่องหมาย `()` เนื่องจากเป็นเงื่อนไขอื่นๆที่เหลือทั้งหมดจึงไม่ต้องการใส่ค่าใดๆลงใน Arguments เพิ่มเติม
{:.is-warning}

## else if()

ในการกำหนดเงื่อนไข สามารถกำหนดได้ **มากกว่า 2 เงื่อนไขขึ้นไป**

```javascript
let answer = prompt('4 * 4 = ?');
if (answer < 16) { // เมื่อ answer น้อยกว่า 16
  alert('น้อยไปหรือเปล่า?');
}
else if (answer > 16) { // เมื่อ answer มากกว่า 16
  alert('มากไปหรือเปล่า?');
}
else { // เมื่อเงื่อนไขอื่นๆ กล่าวคือต้องไม่น้อยกว่า 16 และไม่มากกว่า 16 ซึ่งหมายถึงต้องเท่ากับ 16 เท่านั้น
  alert('คุณฉลาดมาก!! 👏');
}
```

ซึ่งจะต้องใช้ `else if()` หลังจากเรียก `if()` ก่อนเท่านั้น เพื่อทำเงื่อนไขอื่นๆเพิ่มเติม ไม่เช่นนั้นจะมีปัญหาดังตัวอย่างด้านล่าง

```javascript
let answer = prompt('4 * 4 = ?');
else if (answer < 16) { // ใช้ else if() ทันที โดยยังมีมีการใช้ if() ก่อนหน้านั้น
  alert('Less?');
}
else if (answer > 16) {
  alert('Greater?');
}
else {
  alert('Correct!');
}
```
{:.is-danger}

> **หมายเหตุ:** คือเราอาจจะเริ่มเข้าใจกันมากขึ้น ว่าภาษาโปรแกรมจะเหมือนการคุยกับคอมพิวเตอร์ด้วยภาษาเฉพาะ ที่มีสัญลักษณ์ต่างๆบอกถึงความหมายอย่างชัดเจน 
>
> และการใช้ศัพท์ก็เช่นกันที่สามารถบอกความหมายได้เข้าใจง่ายมาก ดังตัวอย่างคำว่า `if` หมายถึง **ถ้าหาก** ดังนั้นหากเขียนเป็น `if (answer > 16)` โปรแกรมจะแปลได้ว่า **ถ้าหาก answer มากกว่า 16** และการใช้ `else if (answer < 16)` โปรแกรมก็จะแปลความหมายตรงๆว่า **หรือว่าถ้าหาก answer น้อยกว่า 16** ขณะที่จบด้วย `else` ก็คือ **และหากเป็นอย่างอื่นนอกเหนือจากนั้น** โดยบางคำหากไม่เก่งภาษาอังกฤษอ่านหรือแปลไม่ออก ให้ลองใช้ [Google Translate](http://translate.google.com) จะช่วยเหลือการเรียนรู้ควบคู่ไปด้วยได้อย่างดี 👍

> **เพิ่มเติม:** ในการใช้เครื่องหมาย `{}` ค่อนข้างมีวิธีการจัดระเบียบหลายวิธี แล้วแต่สไตล์ของแต่ล่ะคนและความถนัด เพราะจะช่วยให้การอ่านโปรแกรมได้ง่ายขึ้น ซึ่งโดยส่วนมากเราจะเลือกใช้แบบที่ 2 เพราะทำให้ประหยัดบรรทัดมากกว่าแบบอื่น เช่น
>
> ```js
> if (...) {
>   //
> }
> else if (...) {
>   //
> }
> else {
>   //
> }
> ```
>
> ```js
> if (...) {
>   //
> } else if (...) {
>   //
> } else {
>   //
> }
> ```
>
> ```js
> if (...)
> {
>   //
> }
> else if (...)
> {
>   //
> }
> else
> {
>   //
> }
> ```

## Code block

ภายในเครื่องหมาย `{}` จะเรียกว่า **Code block** คือช่วงของการทำงานใน **Statement แต่ล่ะช่วง** เพื่อให้ทราบว่าการทำงานของส่วนนั้นๆจะเริ่มที่จุดใดและสิ้นสุดที่ไหน ดังนั้นในกรณีที่โปรแกรมของเราต้องการเพียง Statement เดียวสามารถนำเครื่องหมายออกได้ดังตัวอย่าง

```javascript
let age = 19;
if (age >= 18) {
  alert('Adult');
} else {
  alert('Younger');
}
```

```javascript
let age = 19;
if (age >= 18) alert('Adult');
else alert('Younger');
```

แต่หากเรามีมากกว่า **2 Statements ขึ้นไป** จำเป็นต้องใช้ `{}` เพื่อให้โปรแกรมทราบว่า ช่วงการทำงานของ `if()` Statement ถึงที่ไหน

```javascript
let age = 19;
if (age >= 18) {
  alert('Adult');
  alert('Welcome back');
} else {
  alert('Younger');
  alert('You are not allow');
}
```

```javascript
let age = 19;
if (age >= 18) alert('Adult'); alert('Welcome back');
else alert('Younger'); alert('You are not allow');
```
{:.is-danger}

> **เพิ่มเติม:** เราอยากจะให้ใช้เครื่องหมาย `{}` ไว้ตลอดสำหรับการทำเงื่อนไขและอื่นๆ ถึงแม้มันจะมีเพียง Statement เดียวก็ตาม เพื่อป้องกันความสับสนในการจำ **Syntax (สัญลักษณ์)** ต่างๆ ซึ่งหลังจากนี้ในบทเรียนเราจะแทรก `{}` ไว้ตลอด แต่ในการเขียนโปรแกรมขั้นสูงขึ้นไปเราก็ควรจะต้องทราบวิธีลัดเช่นนี้ด้วย เพราะบางครั้งอาจจะมีการตอบถามปัญหาโปรแกรมที่ใช้ภาษาขั้นสูงมากหรือใช้วิธีลัดขึ้น

## Shorthand

เนื่องจากการใช้ if else โดยทั่วไปแล้วจะมีปัญหาการเขียนที่ **ยาวเกินไป** กับเงื่อนไขเล็กๆน้อยๆ จึงมีการใช้ **Shorthand** ที่จะทำให้สามารถเรียกใช้ Statement บางส่วนโดยใช้สัญลักษณ์โดยย่อได้ อาจจะคล้ายๆกับการนำ `{}` ออก แต่จะใช้งานง่ายกว่าและจบในบรรทัดเดียว

โดยการใช้ If Shorthand จะสามารถทำได้เพียง 2 เงื่อนไขหลักๆเท่านั้น คือจริงและเท็จ โดยเราจะใช้เครื่องหมาย `?` ในการทำงานข้อมูลของจริง จากนั้นใช้ `:` ในการทำงานข้อมูลของเท็จ

```js
conditional ? 'if true' : 'if false';
```

โดยจะมีความหมายเหมือนกับ

```js
if (conditional) {
  'if true';
} else {
  'if false';
}
```

ซึ่งจากตัวอย่างจะเห็นว่าใช้ได้เพียง 2 เงื่อนไขเท่านั้น เช่นดังตัวอย่าง

```javascript
let age = prompt('Your age?');
let message;
if (age >= 18) {
  message = 'Adult';
} else {
  message = 'Younger';
}
alert(message);
```

```javascript
let age = prompt('Your age?');
let message = (age >= 18) ? 'Adult' : 'Younger'; // หากจริงจะได้หลัง ? หากเท็จจะได้หลัง :
alert(message);

/* ลำดับการทำงานโปรแกรมจะประมาณว่า... */

// message = อะไรดี
  // ก็มาดูเงื่อนไขกันที่ว่า (age >= 18) จริงหรือไม่
    // ? ถ้า age มากกว่าหรือเท่ากับ 18 จริงๆ ให้เก็บค่าเป็น 'Adult'
    // : แต่หากน้อยกว่า 18 ให้เก็บค่าเป็น `Younger`
// จากนั้นโปรแกรมแสดงผล alert(message); อีกที
```

หรืออาจจะเขียนให้สั้นกว่าเดิมได้ดังตัวอย่างเหลือเพียงบรรทัดเดียวได้

```javascript
alert(prompt('Your age?') >= 18 ? 'Adult' : 'Younger');

/* อธิบายการทำงานในบรรทัดเดียว */

// ถ้ายังจำกันได้ของลำดับการทำงานคณิตศาสตร์ โปรแกรมจะเริ่มทำงานใน () ข้างในสุดก่อน
// คือแสดง prompt('Your age?') จากนั้นโปรแกรมจะหยุดรอรับค่า
  // เมื่อรับค่าได้แล้ว ทำการเทียบค่าที่ได้ >= 18 หรือไม่
    // ? หากจริง 'Adult'
    // : หากเท็จ 'Younger'
      // สุดท้าย แสดงค่าที่ได้บน alert()
```

และสามารถใช้เทคนิค ที่จากเดิมใช้ได้เพียง 2 เงื่อนไข สามารถใช้ได้มากขึ้นไปได้ด้วยการซ้อน `?:` อีกครั้งหนึ่ง หรือสามารถจัดเรียงให้อ่านได้ง่ายขึ้นอีกดังตัวอย่างด้านล่าง

```javascript
alert(
  confirm('Your are programmer?') // คุณเป็นโปรแกรมเมอร์หรือไม่?
    ? confirm('Do you like JavaScript?') // คุณชอบ JavaScript หรือไม่?
      ? confirm('Will you need to develop a front-end website?') // คุณต้องการจะพัฒนาด้านออกแบบหน้าเว็บไซต์หรือไม่?
        ? 'Try learn HTML and CSS' // สายออกแบบหน้าเว็บต้องลองเรียน HTML และ CSS ดู
        : 'Try learn Node.js' // ถ้าไม่ชอบออกแบบเว็บลองเรียน Node.js ดู
      : 'Try to learn Python language then' // ไปลองเรียนภาษาไพทอนล่ะกันนะ (เป็นอีกภาษาที่น่าสนใจสำหรับกลุ่มชอบวิเคราะห์ข้อมูล)
    : 'Oh no!' // ม้ายยย! 😭
);
```

> **หมายเหตุ:** ถึงอย่างไรการใช้ Shorthand ก็ไม่ได้จำเป็นเสมอไป วิธีการใช้ if else หลายๆครั้งอาจจะช่วยให้อ่านลำดับขั้นตอนการทำงานโปรแกรมได้ง่ายกว่า เพียงแต่เราอยากจะสอนให้ทราบกันก่อนว่าสามารถใช้วิธีเหล่านี้ได้ เพราะการเขียนโปรแกรมที่มีเงื่อนไขเล็กๆน้อยๆบ่อยครั้งจะทำให้มีความน่ารำคาญต่อการเรียก if else ทำให้การใช้ `?:` อาจจะสะดวกกว่าในหลายๆสถานการณ์

## switch

การใช้ `switch()` จะเป็นการเรียก Statement ที่ต้องการเงื่อนไขเช่นเดียวกับ `if()` แต่จะสามารถนำตัวแปรใดตัวแปรหนึ่งมาเปรียบเทียบได้หลายครั้ง

```javascript
let input = prompt(`
  Input only A-D to answer (Uppercase)

  What is 4 + 4 = ?
  A) 1
  B) 9
  C) 8
  D) 10
`);
switch (input) { // สลับค่าของ input
  case 'A': // หาก input == 'A'
    alert('Wrong! 🐜');
    break;
  case 'B': // หาก input == 'B'
    alert('Wrong! 🐦');
    break;
  case 'C': // หาก input == 'C'
    alert('Correct! 😸');
    break;
  case 'D': // หาก input == 'D'
    alert('Wrong! 🐶');
    break;
  default: // หาก input อื่นๆมา
    alert('Please input only (A-D) with uppercase');
    break;
}
```

เราจะเห็นว่า `switch (input)` จะตรวจสอบจนกว่าภายใน `(input)` จะมีค่าเท่ากับของ `case` โดยจะอยู่ใน Statement ของ `switch() { ... }` ซึ่งจบด้วยการใช้ `default` ที่มีความหมายถึงอื่นๆที่นอกเหนือจากเคสทีมีอยู่

และการเขียนจะต้องมีการใช้ `break` เพื่อหยุด Statement ดังกล่าว โดยอธิบายได้ดังตัวอย่างโค้ดด้านล่าง

```js
switch (variable) { // ทำการตรวจสอบ variable
  case: value1: // เมื่อ variable == value1
    // code...
    break;
  case: value2: // เมื่อ variable == value2
    // code...
    break;
  default: // เมื่อ variable เป็นค่าอื่นๆ (ทำหน้าที่เหมือนกับ else)
    // code...
    break;
}
```

หากไม่มีการใช้ `break` จะข้างต้น จะทำให้โปรแกรมรันทุกๆ `case` จนกว่าจะสิ้นสุดของ Statement

```javascript
let input = prompt(`
  กรุณาใส่ C เท่านั้นเพื่อดูผลลัพธ์ที่เปลี่ยนไป

  What is 4 + 4 = ?
  A) 1
  B) 9
  C) 8
  D) 10
`);
switch (input) { // โปรแกรมจะเริ่มตรวจ input
  case 'A': // C ไม่ตรงกับ A
    alert('Wrong! 🐜');
  case 'B': // C ไม่ตรง B
    alert('Wrong! 🐦');
  case 'C': // C ตรงกับ C และจะเริ่มทำงานตั้งแต่ตรงนี้
    alert('Correct! 😸'); // แสดง Correct!
  case 'D':
    alert('Wrong! 🐶'); // แสดง Wrong! โดยปกติไม่น่าจะแสดง?
  default:
    alert('Please input only (A-D) with uppercase'); // และก็แสดงตรงนี้เช่นกัน
}

/* ขยายความ */

// เนื่องจากการใช้ switch() { ... } Statement จะไม่หยุดทำงาน จนกว่าจะเจอกับ break;
// ดังนั้นโปรแกรมจึงต้องการ break; ทุกๆ case ด้วย เพื่อหยุดทำงานตั้งแต่ case นั้นๆ
```

นอกจากนี้เราสามารถทำ **Group** ของ `case` ได้ ทำให้สามารถจัดรวมเงื่อนไขที่มีการทำงานซ้ำซ้อนได้

```javascript
let input = prompt(`
  Input only A-D to answer (Uppercase)

  What is 4 + 4 = ?
  A) 1
  B) 9
  C) 8
  D) 10
`);
switch (input) {
  case 'A':
  case 'B':
  case 'D':
    alert('Wrong! 🐜 🐦🐶');
    break;
  case 'C':
    alert('Correct! 😸');
    break;
  default:
    alert('Please input only (A-D) with uppercase');
    break;
}
```

และนอกจากนี้เรายังใช้เทคนิกการ `switch()` เพื่อหา `case` ที่ได้ค่าเป็น Boolean `true` ได้อีกด้วย เช่นดังตัวอย่างของ 2 โปรแกรมนี้ที่มีการทำงานเหมือนกน

```javascript
let age = prompt('Input your age');
if (age < 12) {
  alert('Child');
} else if (age < 18) {
  alert('Teen');
} else if (age < 40) {
  alert('Adult');
} else if (age < 60) {
  alert('Middle-aged');
} else {
  alert('Old');
}
```

```javascript
let age = prompt('Input your age');
switch (true) { // ให้ทำการตรวจสอบว่า case ใดๆจะ == true บ้าง
  case (age < 12): // age < 12 หากใส่ age = 13 เราจะได้ false == true
    alert('Child');
    break;
  case (age < 18): // age < 12 หากใส่ age = 13 เราจะได้ true == true
    alert('Teen');
    break; // ป้องกันข้ามไปทำงานอีก case และจบ Statement switch() นี้ทันที
  case (age < 40):
    alert('Adult');
    break;
  case (age < 60):
    alert('Middle-aged');
    break;
  default:
    alert('Old');
    break;
}
```

> **หมายเหตุ:** เนื่องจากการใช้ `switch()` อาจจะจดจำยากกว่า ดังนั้นการใช้แต่เพียง `if()` ก็สามารถทำได้หากในกรณีที่เกิดความสับสน ถึงอย่างไรก็ตาม `switch()` ก็จะมีประโยชน์ในบางครั้งที่ทำให้การอ่านโปรแกรมเข้าใจได้ง่ายกว่า

## บทสรุป

- `if()` จะทำงานเมื่อเงื่อนไขเป็นจริง
- `else if()` จะทำงานเป็นเงื่อนไขลำดับต่อมา หากเงื่อนไข `if()` และอื่นๆจากข้างบนไม่เป็นจริง
- `else` จะทำงานเป็นเงื่อนไขสุดท้าย โดยต้องใส่เป็นลำดับสุดท้าย
  - `else if()` และ `else` เป็นเพียงทางเลือกเสริม ไม่ได้จำเป็นในการเขียนเงื่อนไข อาจจะใช้ `if()` เพียงครั้งเดียวได้
- **Code block** คือการทำงานของช่วงใน Statement
- **Shorthand** กับการใช้ `?:` เพื่อให้เขียนเงื่อนไขสั้นลง
- `switch()` จะตรวจสอบเงื่อนไขภายใน `()` ว่าเท่ากับ `case` ใดๆหรือไม่ ถ้าไม่จะจบที่ `default`
  - เพื่อป้องกันโปรแกรมทำงานเกิน Statement ของแต่ล่ะ `case` จะใช้ `break;` ในการหยุด Statement ดังกล่าว
