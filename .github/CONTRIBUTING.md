# การมีส่วนร่วม

สำหรับบทนี้มีไว้เพื่อรองรับการพัฒนาของ Source code นี้ รวมทั้งเนื้อหาทั้งหมดที่ใช้เพื่อเป็นบทเรียน เพื่อให้รักษารูปแบบของเนื้อหาให้ดีที่สุด

## วิธีการมีส่วนร่วม

- สามารถร่วมเขียนบทความได้โดยทำการ [Pull Request](https://github.com/anitation/nong-program/pulls) เพื่อให้ทาง Contributors สามารถรีวิวและตอบถามความเห็นได้ก่อน
- สามารถร่วมเขียนบทความอีกทางได้โดยการเข้าร่วมเป็นส่วนหนึ่งของ Contributors จาก [anitation](https://github.com/anitation) ได้โดยการส่งเมลพูดคุยกับเจ้าของโครงการนี้ได้ที่ `nakorndev@gmail.com` หรือ Facebook: [nakorndev](https://www.facebook.com/nakorndev)
- สามารถร่วมแก้ไขบทความที่มีความผิดพลาด โดยไม่ต้องทำการ Pull Request โดยการเปิด [Issues](https://github.com/anitation/nong-program/issues) ใหม่ เพื่อพูดคุยกันก่อนทำการแก้ไขปัญหาของเนื้อหา

## วิธีการใช้สำหรับผู้พัฒนา

เราใช้ [Jekyll](jekyllrb.com) และ [GitHub Pages](https://pages.github.com) ในการเขียนบล็อกขึ้นมา เพื่อให้รองรับการแก้ไขจากผู้อื่น และยังเป็นการเขียนบทความที่เหมาะแก่โปรแกรมเมอร์อย่างมากด้วยการใช้ `Markdown` หรือ `HTML` ในการเขียนเนื้อหา ดังนั้นการใช้งานจึงควรมีพื้นฐานการใช้งาน `Jekyll` ด้วย

> ศึกษาเพิ่มเติมได้ที่ [https://jekyllrb.com/docs/quickstart/](https://jekyllrb.com/docs/quickstart/)

## ความต้องการ

- [Ruby](https://rubyinstaller.org/downloads/) >= 2.2.5
- ruby2.3-dev
- [RubyGems](https://rubygems.org/pages/download) >= 2.7.6
- [Jekyll](https://jekyllrb.com/) >= 3.7.3
- [Bundler](http://bundler.io/) >= 1.16.1
- `gcc` `g++` และ `make`

> สำหรับระบบ Windows อาจจะไม่มีบางคำสั่ง แต่สามารถใช้ [http://www.mingw.org/](http://www.mingw.org/) และ [http://gnuwin32.sourceforge.net/packages/make.htm](http://gnuwin32.sourceforge.net/packages/make.htm) ร่วมกันได้
>
> **Tips:** บน Windows เวอร์ชั่นล่าสุด สามารถใช้ [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/install-win10) แทน Vitrual Machine ได้ และยังรองรับกับ Visual Studio Code ได้หลายๆส่วน (ยังไม่สมบูรณ์)

## การติดตั้ง

หลังจาก Clone เข้าสู่เครื่องแล้ว ใช้คำสั่ง `bundle` เพื่อติดตั้ง Package ที่จำเป็นของ Jekyll

```bash
bundle install
```

จากนั้นทำการ `serve` ไปยัง [http://127.0.0.1:4000/nong-program](http://127.0.0.1:4000/nong-program) โดยใช้คำสั่งนี้

```bash
jekyll serve
```

หรือ

```bash
bundle exec jekyll serve
```

> หากมีปัญหาใดๆ ลองตรวจสอบได้ที่ [https://jekyllrb.com/docs/installation/](https://jekyllrb.com/docs/installation/) หรือ [https://jekyllrb.com/docs/troubleshooting/](https://jekyllrb.com/docs/troubleshooting/)

## กฎและรูปแบบการเขียนบทความ

ในส่วนนี้จะเป็นวิธีการแก้ไขหรือเพิ่มเติมข้อมูล โดยเราจะมีส่วนที่อนุญาตหรือไม่อนุญาตในการแก้ไข ดังนั้นกรุณาอ่านให้ละเอียดก่อนทำการแก้ไขเนื้อหาและทำการ Pull Request เพื่อให้การรีวิวเนื้อหาเป็นไปได้อย่างรวดเร็ว

โดยเราจำกัดขอบเขตบางอย่างเพียงเพื่อให้มีความเรียบร้อยของ Repository แต่ส่วนของเนื้อ และวิธีการอธิบาย หรือแม้กระทั่งการใช้เชิงพานิชย์เชื่อมโยงไปยังลิงก์ที่เกี่ยวข้องที่มีประโยชน์ เราก็ยินดีมอบให้แก้ไขอย่างอิสระเสรี แต่ก็ต้องดูไม่น่าเกลียดมากเกินไป

- Read only หมายถึงอนุญาตให้เรียกใช้หรืออ่านไฟล์ได้อย่างเดียว
- Edit only หมายถึงอนุญาตให้แก้ไขได้ แต่ไม่ให้เพิ่มไฟล์ (สำหรับ Directory)
- Editable หมายถึงอนุญาตให้แก้ไขได้ (สำหรับ File)
- Full access หมายถึงอนุญาตให้แก้ไข เพิ่มเติม และลบไฟล์ได้

### Markdown

ทุกๆไฟล์ `.md` ที่แก้ไขจะต้องมีโค้ดดังต่อไปนี้อยู่บนส่วนหัวสุด ตามตัวอย่างไฟล์อื่นๆ เพื่อให้ Jekyll ทำการ Build เอกสารออกมาอย่างถูกต้อง โดยไม่จำเป็นต้องเพิ่ม Variable ใดๆ เนื่องจากเราได้ตั้งไว้บน `_config.yml` ไว้เรียบร้อยแล้ว

```markdown
---
---
```

### Editor

กรุณาเลือกใช้ Text Editor ที่รองรับ [EditorConfig](http://editorconfig.org/) โดยทางเราแนะนำให้เลือกใช้ [Visual Studio Code](https://code.visualstudio.com/) ร่วมกับ Extension: [EditorConfig for VS Code](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig) เพื่อให้ทุกส่วนของเนื้อหามีโครงสร้างและรูปแบบการเขียนที่ตรงกันกับทุกคน

### Directory

| Directory | Meaning | Usage | Permit |
| --- | --- | --- | --- |
| `/_awesome/` | Awesome Pages | สำหรับเก็บ Awesome Lists โดย ramut และบุคคลที่สนใจลงลิงก์ที่มีประโยชน์ | Edit only |
| `/_data/` | Global YAML data | สำหรับเก็บข้อมูลและตัวแปร ที่จำเป็นนำมาใช้กับบล็อก | Read only |
| `/_docs/` | Documentation Pages | สำหรับเก็บ Documentation หลักโดย URL จะถูกเรียกเป็น `/docs/:path/` และบังคับให้ `.md` เป็นหลัก โดยใช้ชื่อไฟล์เป็นภาษาอังกฤษเท่านั้น และต้องมีความหมายตรงกับเนื้อหา | Full access |
| `/_includes/` | Components | สำหรับใช้งานเป็น Components ที่ถูกเรียกใช้งานในหน้าอื่นๆผ่าน `{% include filename.html %}` | Read only |
| `/_layouts/` | Layout, Template | สำหรับเรียกใช้งาน Layouts ผ่านตัวแปล `layout` ใน `YAML` | Read only |
| `/_news/` | News Pages | สำหรับเขียนข่าวสารในรูปแบบ Posts โดยต้องมีไฟล์ชื่อ `YYYY-MM-DD-TITLE.md` ที่ถูกต้อง และมี `date` ภายใน `YAML` ถูกกำกับตาม Timezone ที่ถูกต้องเป็น `YYYY-MM-DD HH:MM:SS +0700` | Read only |

### File

| File | Meaning | Usage | Permit |
| --- | --- | --- | --- |
| `/_awesome/*.md` | Awesome file | สำหรับเนื้อหาลิงก์ที่มีประโยชน์ทั้งหมด โดยจะถูกแบ่งหัวข้อไว้ตาม Filename | Editable |
| `/_data/contributors.yml` | Contributors list | สำหรับเก็บข้อมูลผู้เขียน เพื่อเก็บไว้เป็น Credit บนหน้าแรก | Editable |
| `/_data/docs.yml` | Documents list | สำหรับเก็บข้อมูล และ URL ที่เข้าถึง Documentation กับการจัดลำดับของเนื้อหา | Editable |
| `/_docs/*/*.md` | Document file | สำหรับเนื้อหาเอกสารทั้งหมด โดยจะถูกเรียงหัวข้อใหญ่ไว้ตาม Directory และหัวข้อรองเป็น Filename | Editable |

> ทุกๆไฟล์ที่ไม่ได้อยู่ในรายการ จะไม่อนุญาตให้แก้ไขได้

#### `data/contributors.yml`

เป็นไฟล์ที่มีเพื่อบันทึกข้อมูลผู้มีส่วนร่วม ในฐานนักพัฒนาบทความและโครงการนี้

```yml
- realname_th: # ชื่อจริง เป็นภาษาไทย ไม่ต้องมีคำนำหน้า
  realname_en: # ชื่อจริง เป็นภาษาอังกฤษ ไม่ต้องมีคำนำหน้า
  penname: # ชื่อเล่นของคุณหรือนามปากกา โดยเราแนะนำให้ใช้คำว่า "พี"่ นำหน้าด้วย และไม่ควรซ้ำกับผู้อื่น
  title: # งานหรืออะไรบางอย่างที่บ่งบอก
  quote: # พื้นที่สำหรับอธิบายความรู้สึกที่มีต่อโครงการน้องโปรแกรม
  image: # ที่อยู่รูปภาพของ Avatar เป็นรูปแบบพร้อม http:// หรือ https:// ที่ถูกต้อง (แนะนำให้ใช้ Gravatar ตามตัวอย่างบนไฟล์)
  github: # ID GitHub (ไม่จำเป็น)
  facebook: # ID Facebook (ไม่จำเป็น)
  twitter: # ID Twitter (ไม่จำเป็น)
```

> Gravatar จะต้องใช้ Email ที่ได้รับการ Hash MD5 สามารถใช้ [http://www.md5online.org/md5-encrypt.html](http://www.md5online.org/md5-encrypt.html) และใช้ URL เป็น `https://www.gravatar.com/avatar/yourMD5Hashed`

#### `data/docs.yml`

เป็นไฟล์จัดเรียงเนื้อหาที่จะแสดงบนหน้า Documentation และสามารถกด Next หรือ Previous ตามลำดับได้

```yml
- title: # ชื่อหัวข้อ
  url: # URL of directory name (อนุญาตเฉพาะ a-z, 0-9 และ - เท่านั้น)
  docs:
  - title: # ชื่อหัวข้อรอง 1
    url: # URL of Filename (อนุญาตเฉพาะ a-z, 0-9 และ - เท่านั้น และไม่ต้องมี .md หรือ .html)
  - title: # ชื่อหัวข้อรอง 2
    url: # URL of Filename (อนุญาตเฉพาะ a-z, 0-9 และ - เท่านั้น และไม่ต้องมี .md หรือ .html)
    # ...
```

> การจัดเรียงจะมีผลต่อลำดับเนื้อหาเอกสาร ดังนั้นจำเป็นต้องใช้เนื้อหาที่เหมาะแก่ผู้เรียนรู้ตามลำดับ

### Emoji

เราใช้ [Emojione](https://www.emojione.com/) เพื่อรองรับการใช้งาน Emoji ให้เข้ากับทุก Device ที่แตกต่างกัน โดยสามารถใช้ได้ทั้ง Unicode `😄` หรือ Shortname `:smile:` เพื่อแสดงภาพยิ้มเป็นต้น โดยทางเราแนะนำให้ใช้ Unicode เพื่อง่ายต่อการดูแบบไม่ต้อง Preview

- บน Windows อัปเดตเวอร์ชั่นล่าสุดสามารถกดปุ่ม `Win + ;` หรือ `Win + .` เพื่อแสดงแถบเลือก Emoji (Layout ต้องเป็นภาษา EN ก่อนด้วย)
- บน Windows สามารถเลือก Emoji ผ่านบน Touch Keyboard ได้
- สามารถดูรายการที่รองรับทั้งหมดได้ที่ [https://www.emojicopy.com/](https://www.emojicopy.com/)

## การจัดเนื้อหา

เนื้อหาทั้งหมดนั้นสามารถลงได้อย่างอิสระ โดยทางเราขอให้ใช้คำสุภาพเรียบร้อย ที่เหมือนพี่ๆกำลังดูแลและช่วยสอนรุ่นน้อง โดยเนื้อหาที่ลงเราอนุญาตให้ใช้เพื่อโฆษณาหรือโปรโมทต่างๆได้ เพียงแต่เราอยากให้โฆษณานั้นมีความเกี่ยวข้องกับการพัฒนาโปรแกรมโดยตรง และควรมอบสิทธิ์พิเศษให้รุ่นน้องได้ด้วย

โดยเนื้อหาทั้งหมดจะอยู่บน `_docs` เป็นหลัก ซึ่งดูตัวอย่างไฟล์ที่มีอยู่แล้วได้ จะได้เขียนได้ตรงรูปแบบกัน

### ชื่อ File

กรุณาตั้งชื่อไฟล์และโฟลเดอร์ที่สอดคล้องกับหัวข้อของคุณ ซึ่งเมื่อตั้งเสร็จให้กรุณาทำการตั้งค่าบน `data/docs.yml` เพื่อเลือกตำแหน่งของเอกสารที่ถูกต้องด้วย

### การใช้ Heading

กรุณาดูตามตัวอย่างไฟล์ คือต้องมีส่วนที่จะทำให้ Jekyll compile ทำงานของ `.md` ด้วย

```markdown
---
---
```

จากนั้นให้ใช้ `#` ในการทำ Heading 1 สำหรับหัวข้อหลัก ซึ่งจะต้องตรงกับ title attribute บน `data/docs.yml` ด้วย จากนั้นให้ใช้ Heading 2, 3, 4 ตามลำดับของหัวข้อย่อยที่ถูกต้อง โดยขอให้แบ่ง Heading โดยละเอียดและทำโดยบ่อยครั้ง เพื่อกำจัดขอบเขตของเนื้อหาภายในนั้นว่าเกี่ยวกับอะไรอย่างสั้นๆ

### การใช้รูปภาพ

การใช้รูปภาพที่จะใส่ลงบน Markdown กรุณาเก็บไว้บน Directory `assets` และอนุญาตทุก Format ที่เป็นรูปภาพ เพื่อให้ง่ายต่อการจัดการ โดยแบ่งเป็น Sub-directory ไว้ตามชื่อของ Documents ที่เกี่ยวข้องด้วย หากไม่ทราบว่าควรไว้อย่างไรสามารถเก็บไว้บน Root directory ก่อนได้ แล้วทางเราจะมาจัดเก็บให้เป็นระเบียบอีกที

### การใช้วิดีโอ

สำหรับการใช้วิดีโอ ขอให้ทำการ Embed code จากภายนอกมาโดยทางเราแนะนำให้เป็น YouTube เป็นหลัก และสามารถใช้ HTML ลงบน Markdown ได้เลย

### การใช้ HTML

HTML นั้นเราไม่ได้ห้ามใช้บน Markdown แต่เราก็จะอนุญาตพอดีงาม เช่นการใส่วิดีโอ หรือต้องการจัดเรียงเนื้อหาบางอย่างด้วย JavaScript ก็สามารถทำได้ แต่กรุณาเขียนความเห็นไว้บน Pull Request ด้วยว่ามีเหตุผลอย่างไรถึงจำเป็นต้องใช้ HTML ที่นอกเหนือจากการใส่วิดีโอ

### การเชื่อมโยง URL

เนื่องจาก Jekyll ไม่ได้ฉลาดเหมือน GitHub ทำให้ Markdown ไม่ได้เปลี่ยนให้ [https://www.google.com](https://www.google.com) เป็นลิงก์โดยอัตโนมัติ ดังนั้นรบกวนใส่เพิ่มเป็น `[https://www.google.com](https://www.google.com)`

### Markdown Lint

กรุณาใช้ [DavidAnson/vscode-markdownlint](https://github.com/DavidAnson/vscode-markdownlint) สำหรับบน Visual Studio Code เพื่อให้สามารถเปิดใช้งาน Lint และตรวจสอบปัญหาของ Syntax ได้
