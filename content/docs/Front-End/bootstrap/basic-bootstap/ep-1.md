---
weight: 1
bookFlatSection: true
title: Bootstrap 4 แบบพื้นฐาน ตอนที่ 1
bookToc: false
---

# สรุปการใช้งาน Bootstrap 4 แบบพื้นฐาน ตอนที่ 1

![enter image description here](https://benzneststudios.com/blog/wp-content/uploads/2018/11/cove.png)

บทความนี้เป็นบทความสอนการใช้ Bootstrap เรื่องมีอยู่ว่าที่ทำงานของผมส่งผมไปเรียนคอส Web Design สอนโดย อ.กษิติ พันธุ์ถนอม คอสนี้เกี่ยวกับการใช้งาน Bootstrap4 ซึ่งผมก็พอจะรู้อยู่บ้างแล้ว การเรียนครั้งนี้เลยเหมือนการทบทวนและเพิ่มเติมเทคนิคต่างๆ ผมก็เลยได้โอกาสเขียนเป็นบล็อกนี้ขึ้นครับ

โดยเป้าหมายคือ การใช้งาน Bootstrap ทำให้เว็บ responsive แล้วก็ใช้งาน component ของ Bootstrap ต่างๆ รวมถึงคลาสที่ใช้งานบ่อยๆ นอกจากนี้ก็มีแนะนำเทค และการใช้เครื่องมือช่วยต่างๆด้วย

## ติดตั้ง VS code

เครื่องมือสำหรับเขียน แนะนำ VS Code ใครไม่มีก็ติดตั้งเลย

ดาวน์โหลดได้ที่  
[https://code.visualstudio.com/](https://code.visualstudio.com/)

## เริ่มต้น

เริ่มจากการพิมพ์คำสั่งลัด _html:5_ เพื่อให้ VS Code generate code ให้อัตโนมัติ

![g2](https://benzneststudios.com/blog/wp-content/uploads/2018/11/g2.gif)

คำสั่ง meta UTF-8 และ viewport สำคัญสำหรับ Bootstrap ต้องใส่ทุกครั้ง ซึ่งมันก็สร้างมาให้แล้ว

```html
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

อีกอันคือพิมพ์ว่า lorem มันจะ generate ประโยคที่เรียกว่า lorem ให้ มันคือคำที่ไม่มีความหมาย เอามาวางไว้เฉยๆว่านี่คือตัวอักษรจะเห็นในงานพวก design หรือตัวอย่างโค้ดบ่อยๆ

![g3](https://benzneststudios.com/blog/wp-content/uploads/2018/11/g3.gif)

### Deprecate tag

ใน HTML5 มียกเลิก tag บางอย่างไปแล้ว เปลี่ยนมาใช้อันใหม่ เช่น

```html
<b>เปลี่ยนเป็น <strong> <i> ไม่ใช่ตัวเอียง แต่เป็น icons</i></strong></b>
```

## ทบทวน CSS

ก่อนอื่นทบทวน css นิดนึง css คือภาษาสำหรับจัดแต่งหน้า HTML ในบทความนี้ การเขียน style ไม่แนะนำให้ใช้แบบ inline Style เพราะไม่ทำงานในบาง device , Framework แนะนำ external style sheet คือ เขียนแยกจาก HTML tag

### เพิ่ม css ใน html

เพิ่มให้ html ขอเราใช้ไฟล์ .css ได้

```html
<link rel="stylesheet" href="css/custom.css" />
```

### Selector

สมมุติเราจะกำหนดให้ h1 เป็นสี #dd1144

```css
h1 {
  color: #d14;
}
```

ต้องการให้ h1 ที่อยู่ใน div เป็นสีแดง เขียนแบบนี้ได้

```css
div h1 {
  color: red;
}
```

### การใช้ !important

ปกติการทำงานจะทำแบบบนลงล่าง ทำให้คำสั่งมันทับกันได้ แต่ถ้าไม่อยากให้มันอานทับ ให้เพิ่ม `important`

```css
h1 {
  color: #d14 !important;
}
h1 {
  color: green;
}
```

### การใช้ id

กำหนด id ให้ tag

```css
<div id="first">
```

ใน CSS จะใช้สัญลักษณ์ #

```css
#first {
  background: lightblue;
}
```

### การใช้ class

กำหนด class ให้ tag ได้ ซึ่งใน Bootstrap จะใช้บ่อย

```html
<div class="second">
  <h1>Outside</h1>
</div>
```

ใน CSS จะใช้สัญลักษณ์ .

```css
.second {
  background: indianred;
}
```

### id vs class

id มีได้ element เดียว แต่ class มีได้หลาย element การใช้ id ส่วนใหญ่จะใช้เชื่อมกับ js ส่วน class จะมักเชื่อมกับ css และใน bootstrap จะเน้นใช้ class ส่วน id จะใช้เชื่อมกับของ bootstrap เอง

## รู้จัก Bootstrap

Bootstrap คือ UI Framework พูดง่ายๆคือเขาเขียน CSS , JS สวยๆ มาให้แล้ว เรามีหน้าที่เรียกใช้ ซึ่งส่วนใหญ่ Bootstrap จะใช้ การเรียก class เป็นหลัก เรามาลองใช้งานกันนะ ตอนนี้ Bootstrap เวอชัน 4

### ดาวน์โหลด Bootstrap

ไปที่เว็บ [https://getbootstrap.com/](https://getbootstrap.com/)

[![2](https://benzneststudios.com/blog/wp-content/uploads/2018/11/2.png)](https://benzneststudios.com/blog/wp-content/uploads/2018/11/2.png "2")

พอโหลด Bootstrap มาให้ copy มาไว้ในโปรเจค จะได้โฟลเดอร์ css กับ js มีไฟล์ด้านในประมาณนี้

bootstarp grid จะมีเฉาะเรื่อง grid และ layout  
bootstrap reboot จะมีฟังชันก์ใหม่ ตัวที่ยังไม่ใช่ production จริง  
bootstarp.css จะเป็นแบบโค้ดสวยๆ อ่านได้  
bootstarp.min.css จะทำ minify มาแล้ว ตัด space และ ขึ้นบรรทัดใหม่ ทำให้ไฟล์เล็กลง

[![1a](https://benzneststudios.com/blog/wp-content/uploads/2018/11/1a.png)

เวลาจะใช้งานจริง เราจะใช้ bootstrap.min.css ในการทำงาน

```html
<link rel="stylesheet" href="css/bootstrap.min.css" />
```

## MaxCDN:

```html
<!-- Latest compiled and minified CSS -->
<link
  rel="stylesheet"
  href="https://maxcdn.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css"/>

<!-- jQuery library -->
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>

<!-- Popper JS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.16.0/umd/popper.min.js"></script>

<!-- Latest compiled JavaScript -->
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.4.1/js/bootstrap.min.js"></script>
```

### การจัด Layout แบบ GRID

ใน bootstrap จะใช้ระบบ GRID ในการวาง layout ต่างๆ  
เริ่มจากใช้ div ที่มี class ชื่อว่า container

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Hello</title>
    <link rel="stylesheet" href="css/bootstrap.min.css" />
  </head>
  <body>
    <div class="container"></div>
  </body>
</html>
```

ด้านในจะมี div ย่อย แบ่งเป็น row col คล้ายกับตาราง  
_แนะนำเขียน comment เอาไว้ ซึ่งใน HTML จะใช้ <!– –>_

```html
<body>
  <div class="container">
    <div class="row">
      <div class="col"></div>
      <!--  Close col  1.1  -->
    </div>
    <!--  Close row  1  -->
  </div>
  <!--  Close container  -->
</body>
```

class container จะทำให้มีพื้นที่ว่างด้านข้าง และเปลี่ยน Font เป็น **Helvetica Neue**

[![3](https://benzneststudios.com/blog/wp-content/uploads/2018/11/3.png)](https://benzneststudios.com/blog/wp-content/uploads/2018/11/3.png "3")

เพื่อนของมันอีกตัวคือ container-fluid มันจะขายเต็มจอ

```html
<div class="container-fluid"></div>
```

![4](https://benzneststudios.com/blog/wp-content/uploads/2018/11/4.png)

มาลองเล่นเรื่องรูปภาพกันบ้าง

[ดาวน์โหลดรูปภาพ](https://benzneststudios.com/blog/wp-content/uploads/2018/11/img.rar)

เพิ่มรูปภาพใน grid col คือใช้ <img>

```html
    <body>
    <div class="container">
    <div class="row">
    <h1>Hello World</h1>
    </div>
    <div class="row">
    <div class="col>
    <img src="img/banner/banner2.jpg">
    </div>
    </div>
    </div>
    </body>
```

ลองเลือกรูปภาพใหญ่ๆ เมื่อเปิดดูจะเห็นว่ารูปภาพมีขนาดใหญ่จนล้นจอ ยิ่งเปิดในมือถือก็ยิ่งล้น มันไม่ responsive

วิธีแก้คือ เพิ่ม class ชื่อว่า img-fluid

```html
<img src="img/banner/banner2.jpg" class="img-fluid" />
```

รูปภาพจะปรับ scale อัตโนมัติ

![7](https://benzneststudios.com/blog/wp-content/uploads/2018/11/7.png)

ลองเพิ่ม col 3 อัน มันจะแบ่งหน้าจอให้เท่ากัน เป็น 3 ส่วน

```html
<body>
  <div class="container">
    <div class="row">
      <h1>Hello World</h1>
    </div>
    <!--  Close Row  1  -->
    <div class="row">
      <div class="col">
        <img src="img/banner/banner2.jpg" class="img-fluid" />
      </div>
    </div>
    <!--  Close Row  2  -->
    <div class="row">
      <div class="col">
        <img src="img/staffs/staff1.jpg" class="img-fluid" />
        <h1>CEO</h1>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio odit
          illum autem porro! Quisquam voluptatibus nesciunt impedit, suscipit
          corporis, minus culpa molestiae necessitatibus blanditiis, repellat
          mollitia beatae hic voluptatum deleniti.
        </p>
      </div>
      <div class="col">
        <img src="img/staffs/staff2.jpg" class="img-fluid" />
        <h1>CTO</h1>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio odit
          illum autem porro! Quisquam voluptatibus nesciunt impedit, suscipit
          corporis, minus culpa molestiae necessitatibus blanditiis, repellat
          mollitia beatae hic voluptatum deleniti.
        </p>
      </div>
      <div class="col">
        <img src="img/staffs/staff3.jpg" class="img-fluid" />
        <h1>CFO</h1>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio odit
          illum autem porro! Quisquam voluptatibus nesciunt impedit, suscipit
          corporis, minus culpa molestiae necessitatibus blanditiis, repellat
          mollitia beatae hic voluptatum deleniti.
        </p>
      </div>
    </div>
    <!--  Close Row  3  -->
  </div>
  <!--  Close container  -->
</body>
```

![8](https://benzneststudios.com/blog/wp-content/uploads/2018/11/8.png)](https://benzneststudios.com/blog/wp-content/uploads/2018/11/8.png "8")

1 แถวของ Bootstrap มี 12 หน่วย ถ้าเกินมันจะล่วงลงมาแถวใหม่ ถ้าใส่ไม่ถึง 12 มันจะมีช่องว่างที่เหลืออยู่  
วิธีการคือ ใช้คลาส col- ตามด้วยหน่วย เช่น ต้องการให้คอลัมภ์แรก 50% ของแถว อีกสองอันก็แบ่งอันละ 25%

```html
<div class="row">
  <div class="col-6">
    <img src="img/staffs/staff1.jpg" class="img-fluid" />
    <h1>CEO</h1>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio odit illum
      autem porro! Quisquam voluptatibus nesciunt impedit, suscipit corporis,
      minus culpa molestiae necessitatibus blanditiis, repellat mollitia beatae
      hic voluptatum deleniti.
    </p>
  </div>
  <div class="col-3">
    <img src="img/staffs/staff2.jpg" class="img-fluid" />
    <h1>CTO</h1>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio odit illum
      autem porro! Quisquam voluptatibus nesciunt impedit, suscipit corporis,
      minus culpa molestiae necessitatibus blanditiis, repellat mollitia beatae
      hic voluptatum deleniti.
    </p>
  </div>
  <div class="col-3">
    <img src="img/staffs/staff3.jpg" class="img-fluid" />
    <h1>CFO</h1>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio odit illum
      autem porro! Quisquam voluptatibus nesciunt impedit, suscipit corporis,
      minus culpa molestiae necessitatibus blanditiis, repellat mollitia beatae
      hic voluptatum deleniti.
    </p>
  </div>
</div>
```

![10](https://benzneststudios.com/blog/wp-content/uploads/2018/11/10.png)

ทีนี้ลองมาดูปัญหาเมื่อเปิดในจอของโทรศัพท์ คอลัมภ์สามอันมันดูอึดอัด การดูในมือถือมันควรจะแสดงทีละอัน มันยังไม่ responsive

![9](https://benzneststudios.com/blog/wp-content/uploads/2018/11/9.png)

วิธีการคือใช้ Grid option เช่น col-md-4 หมายถึง ถ้าหน้าจอมีขนาดมากกว่า Medium มันจะใช้หน่วยขนาด 4 แต่ถ้าไม่ใช่ มันจะใช้ 1 เป็นค่าเดิม ซึ่ง Medium มีหน้าจอขนาด >= 768px ซึ่งคือหน้าจอคอมนั่นเอง ดังนั้น ถ้าหน้าจอเล็กมันก็จะใช้ col-1 แทนนั่นเอง หน้าจอมือถือเลยแสดง col-1 ซึ่งคืออันเดียวเต็มจอ

```html
<div class="row">
  <div class="col-md-4">
    <img src="img/staffs/staff1.jpg" class="img-fluid" />
    <h1>CEO</h1>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio odit illum
      autem porro! Quisquam voluptatibus nesciunt impedit, suscipit corporis,
      minus culpa molestiae necessitatibus blanditiis, repellat mollitia beatae
      hic voluptatum deleniti.
    </p>
  </div>

  <div class="col-md-4">
    <img src="img/staffs/staff2.jpg" class="img-fluid" />
    <h1>CTO</h1>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio odit illum
      autem porro! Quisquam voluptatibus nesciunt impedit, suscipit corporis,
      minus culpa molestiae necessitatibus blanditiis, repellat mollitia beatae
      hic voluptatum deleniti.
    </p>
  </div>

  <div class="col-md-4">
    <img src="img/staffs/staff3.jpg" class="img-fluid" />
    <h1>CFO</h1>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio odit illum
      autem porro! Quisquam voluptatibus nesciunt impedit, suscipit corporis,
      minus culpa molestiae necessitatibus blanditiis, repellat mollitia beatae
      hic voluptatum deleniti.
    </p>
  </div>
</div>
<!--  Close Row  3  -->
```

พอเปิดในจอเล็กมันก็แสดงเต็มจอแล้ว

![11](https://benzneststudios.com/blog/wp-content/uploads/2018/11/11.png)

ดูรายละเอียดเรื่อง Grid Option ได้ที่

[https://getbootstrap.com/docs/4.0/layout/grid/](https://getbootstrap.com/docs/4.0/layout/grid/)

ซึ่งนอกจาก md แล้วก็มี sm , lg , xl ด้วย

[![12](https://benzneststudios.com/blog/wp-content/uploads/2018/11/12.png)
จะได้ประมาณนี้

[![14](https://benzneststudios.com/blog/wp-content/uploads/2018/11/14.png)

### Source code

[https://gist.github.com/benznest/f365a2de60451b6696c78d5ce642e293](https://gist.github.com/benznest/f365a2de60451b6696c78d5ce642e293)

### การจัด Format

ตอนนี้ เราจะเริ่มใช้ <div> ซับซ้อนขึ้น โค้ดมันอาจจะไม่เป็นระเบียบ  
วิธีการให้มันจัดระเบียบ คือ คลิกขวาเลือก Format document หรือกด Shift + Alt + F

[![g4](https://benzneststudios.com/blog/wp-content/uploads/2018/11/g4.gif)

### การซ้อน Grid

เราสามารถนำ Grid มาซ้อนอีกชั้นได้ โดยมันจะยังใช้หน่วย 12 เหมือนเดิม

```html
<!--  Start Row  4  -->

<div class="row">
  <div class="col-md-6 col-12">
    <div class="row">
      <div class="col-4">
        <img src="img/life/life2.jpg" class="img-fluid" />
      </div>

      <div class="col-8">
        <h3>Service</h3>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio odit
          illum autem porro! Quisquam voluptatibus nesciunt impedit
        </p>
      </div>
    </div>

    <div class="row">
      <div class="col-4">
        <img src="img/life/life3.jpg" class="img-fluid" />
      </div>

      <div class="col-8">
        <h3>Subscription</h3>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio odit
          illum autem porro! Quisquam voluptatibus nesciunt impedit
        </p>
      </div>
    </div>

    <div class="row">
      <div class="col-4">
        <img src="img/life/life4.jpg" class="img-fluid" />
      </div>

      <div class="col-8">
        <h3>More</h3>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio odit
          illum autem porro! Quisquam voluptatibus nesciunt impedit
        </p>
      </div>
    </div>
  </div>

  <div class="col-md-6 col-12">
    <img src="img/content/office12.jpg" class="img-fluid" />
    <h1>About</h1>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio odit illum
      autem porro! Quisquam voluptatibus nesciunt impedit, suscipit corporis,
      minus culpa molestiae necessitatibus blanditiis, repellat mollitia beatae
      hic voluptatum deleniti.
    </p>
  </div>
</div>

<!--  Close Row  4  -->
```

![16](https://benzneststudios.com/blog/wp-content/uploads/2018/11/16.png)

### Source code

[https://gist.github.com/benznest/5c13cf8292c68a89183103233f53f7bd](https://gist.github.com/benznest/5c13cf8292c68a89183103233f53f7bd)

### Class ของรูปภาพ

เพิ่มความสวยงามให้กับรูปภาพ ด้วย class ชื่อว่า rounded รุปภาพจะมีขอบมน

```html
<img src="img/life/life4.jpg" class="img-fluid rounded" />
```

![17](https://benzneststudios.com/blog/wp-content/uploads/2018/11/17.png)

หรือจะใช้ class ชื่อว่า rounded-circle ทำให้รูปเป็นวงกลม

```html
<img src="img/life/life4.jpg" class="img-fluid rounded-circle" />
```

![18](https://benzneststudios.com/blog/wp-content/uploads/2018/11/18.png)

อีกอัน คือ class ชื่อว่า img-thumbnail ทำให้รูปมีขอบเป็นเส้นด้านนอก

```html
<img src="img/life/life4.jpg" class="img-fluid img-thumbnail" />
```

![19](https://benzneststudios.com/blog/wp-content/uploads/2018/11/19.png)

## Class ของ Width

มี class ของ bootstrap ที่ใช้บ่อย เช่น การกำหนด width %  
เช่น w-50 คือกำหนด ให้มีขนาด 50% และการกำหนด mx-auto d-block คือการกำหนดตรงกลาง

```html
<img src="img/staffs/staff1.jpg" class="w-50 mx-auto d-block" />
<h1 class="text-center">CEO</h1>
```

![21](https://benzneststudios.com/blog/wp-content/uploads/2018/11/21.png)

class เพื่อนๆในแก็งนี้ก็มี w-25 , w-50 , w-75 , w-100

```html
<img src="img/staffs/staff1.jpg" class="w-50" />
<img src="img/staffs/staff2.jpg" class="w-75" />
<img src="img/staffs/staff3.jpg" class="w-100" />
```

![20](https://benzneststudios.com/blog/wp-content/uploads/2018/11/20.png)

## การ Custom Bootstrap

เวลาเราจะเพิ่ม css ของเราและต้องการทับกับ bootstrap ให้ไปเขียนที่ custom.css  
เช่น ต้องเปลี่ยนสีพื้นหลัง ของ class container ซึ่ง container เป็นของ bootstrap

```css
body {
  background: #dcebfc;
}
.container {
  background: #fff;
}
```

แล้วก็เวลาเรียกใน HTML ให้ใส่ทีหลัง bootstrap.css นะ เพราะมันจะได้อ่านทับ bootstrap แล้วนั่นเอง

```html
<head>
  
  <link rel="stylesheet" href="css/bootstrap.min.css" />
  <link rel="stylesheet" href="css/custom.css" />
</head>
```

![23](https://benzneststudios.com/blog/wp-content/uploads/2018/11/23.png)

## หน่วย rem

rem คือ root element มันคือการกำหนด font-size ที่ root แล้วเอามาคูณ เช่น ถ้ากำหนด font-size 10 px  
2 rem = 16×2 = 32 px นั่นเอง

ใน Bootstrap จะใช้ font-size = 16 px ดังนั้น 1 rem = 16 px  
ลองกำหนด padding ของ container 4.5rem = 16×4.5 = 72px

```css
body {
  background: #dcebfc;
}
.container {
  background: #fff;
  padding: 4.5rem;
}
```

![24](https://benzneststudios.com/blog/wp-content/uploads/2018/11/24.png)

การ custom ค่า font-size ไม่ใช้ของ bootstrap ต้องไปเซ็ตใน html ที่เป็น root element

```css
html {
  font-size: 8px;
}
```

ค่า rem ก็จะเปลี่ยนมาใช้ font-size ของเราแทน

```css
body {
  background: #dcebfc;
}
.container {
  background: #fff;
  padding: 10rem;
}
h1,
h2,
h3 {
  color: #4f85d7;
}
```

![25](https://benzneststudios.com/blog/wp-content/uploads/2018/11/25.png)

### Class สำหรับ Margin – Padding – Border

เราสามารถใช้ rem มาใช้กับ class Margin Padding ได้  
margin คือระยะห่างจาก element นี้กับอันอื่น  
padding คือระยะห่างจากเนื้อหาถึงขอบ  
border คือ ขนาดขอบ

วิธีการคือ {boxmodel}{position}-{rem}

```css

margin-top 3 rem = mt-3
padding 5 rem = p-5
margin 2 rem = m-2
padding-bottom 3 rem= pd-3
```

ลองกำหนด padding-top 4 rem ซึ่งมีขนาด 16×4 = 64 px

```html
<div class="row pt-4">
  ...
</div>
```

![26](https://benzneststudios.com/blog/wp-content/uploads/2018/11/26.png)
ซึ่ง class margin padding ใช้บ่อยมากๆ

```html
<div class="row">
  <div class="col-3 mt-2">
    <img src="img/life/life.jpg" class="img-fluid rounded" />
  </div>

  <div class="col-3 mt-2">
    <img src="img/life/life2.jpg" class="img-fluid rounded" />
  </div>

  <div class="col-3 mt-2">
    <img src="img/life/life3.jpg" class="img-fluid rounded" />
  </div>

  <div class="col-3 mt-2">
    <img src="img/life/life4.jpg" class="img-fluid rounded" />
  </div>

  <div class="col-3 mt-2">
    <img src="img/life/life5.jpg" class="img-fluid rounded" />
  </div>

  <div class="col-3 mt-2">
    <img src="img/life/life6.jpg" class="img-fluid rounded" />
  </div>

  <div class="col-3 mt-2">
    <img src="img/life/life7.jpg" class="img-fluid rounded" />
  </div>

  <div class="col-3 mt-2">
    <img src="img/life/life8.jpg" class="img-fluid rounded" />
  </div>
</div>
<!--  Close Row  5  -->
```

![28](https://benzneststudios.com/blog/wp-content/uploads/2018/11/28.png)

## Custom font

มาลองเปลี่ยน font ให้กับเว็บกัน  
เข้าไปดาวน์โหลด font ที่ Google Font

[https://fonts.google.com/](https://fonts.google.com/)

เลือกอันที่ชอบ กด +

[![29](https://benzneststudios.com/blog/wp-content/uploads/2018/11/29.png)

มันจะมีแถบด้านล่าง กดขึ้นมาเลือกแท็บ IMPORT แล้ว copy โค้ด @import

[![30](https://benzneststudios.com/blog/wp-content/uploads/2018/11/30.png)

เอาไปวางใน custom.css ของเรา  
จากนั้นอยากใช้ font ตรงไหนก็เอา font-family ไปวางไว้ เช่นใส่ทั้งหน้าเลยก็ใส่ที่ body

```css
@import url("https://fonts.googleapis.com/css?family=Indie+Flower");
body {
  background: #dcebfc;
  font-family: "Indie Flower", cursive;
}
.container {
  background: #fff;
  padding: 1.5rem;
}
h1,
h2,
h3 {
  color: #4f85d7;
}
```

![31](https://benzneststudios.com/blog/wp-content/uploads/2018/11/31.png)

### ทำ Footer

ลองเพิ่ม class ของเราเองชื่อ footer  
เนื้อหาใส่เป็นคำคม เพื่อลองใช้ font อีกตัว

```html
<div class="row footer p-5">
  <div class="col-12">
    <h2 class="text-center">
      Nothing in life is to be feared, it is only to be understood. Now is the
      time to understand more, so that we may fear less.
    </h2>
  </div>
</div>
```

ก็ทำเหมือนเดิม คือเพิ่มตรง @import  
แล้วก็ใส่ font-family ที่ footer

```css
@import url("https://fonts.googleapis.com/css?family=Dancing+Script|Indie+Flower");
body {
  background: #dcebfc;
  font-family: "Indie Flower", cursive;
}
.container {
  background: #fff;
  padding: 1.5rem;
}

h1,
h2,
h3 {
  color: #4f85d7;
}
.footer {
  font-family: "Dancing Script", cursive;
}
```

![33](https://benzneststudios.com/blog/wp-content/uploads/2018/11/33.png)

### Source code

[https://gist.github.com/benznest/21a5a7f2acbce4815433cd77f91c0b8e](https://gist.github.com/benznest/21a5a7f2acbce4815433cd77f91c0b8e)

## Fontawesome

fontawesome คือ ไลบรารี่เกี่ยวกับ icon ซึ่ง Bootstrap 4 ไม่มี fontawesome ติดมาอีกแล้ว เนื่องจาก fontawesome ไม่มีฟรี

[https://fontawesome.com/how-to-use/on-the-web/setup/getting-started?using=web-fonts-with-css](https://fontawesome.com/how-to-use/on-the-web/setup/getting-started?using=web-fonts-with-css)

copy link CDN ของ Fontawesome เข้ามา

```html
<link rel="stylesheet" href="css/bootstrap.min.css" />
<link
  rel="stylesheet"
  href="https://use.fontawesome.com/releases/v5.5.0/css/all.css"
  integrity="sha384-B4dIYHKNBt8Bc12p+WXckhzcICo0wtJAoU8YZTY5qE0Id1GSseTk6S+L3BlXeVIU"
  crossorigin="anonymous"
/>
<link rel="stylesheet" href="css/custom.css" />
```

ในเว็บ Fontawesome ก็เลือก icon ที่ชอบ พอกดเข้าไปมันจะมีโค้ดอยู่

[![34a](https://benzneststudios.com/blog/wp-content/uploads/2018/11/34a.png)

ให้นำโค้ด มาใช้ โดย <i> คือ icon มันต้องอยู่ภายใต้แท็กอื่นๆ

```html
<h2 class="text-center">
  <i class="far fa-kiss-wink-heart"></i>
  Nothing in life is to be feared, it is only to be understood. Now is the time
  to understand more, so that we may fear less.
</h2>
```

![35](https://benzneststudios.com/blog/wp-content/uploads/2018/11/35.png)

เราสามารถนำ <span> มาใช้ได้เพื่อกำหนดขนาดของมัน  
เช่น custom.css กำหนดขนาดของ icon ที่ 10rem

```css
.front-icon {
  display: block;
}
.front-icon i {
  font-size: 10rem;
}
```

ใน html ก็เอา span มาครอบ

```html
<div class="row">
  <div class="col-12">
    <span class="front-icon text-center">
      <i class="far fa-kiss-wink-heart"></i>
    </span>
  </div>
</div>
<!--  Close Row  7  -->
```

icon จะมีขนาด 10rem แล้ว

[![36](https://benzneststudios.com/blog/wp-content/uploads/2018/11/36.png)

หรือจะใช้พื้นหลังสีอื่น ไอคอนสีขาว

```css
.front-icon {
  display: block;
  color: #ffffff;
  padding: 3rem;
  background: #4f85d7;
}
.front-icon i {
  font-size: 10rem;
}
```

![37](https://benzneststudios.com/blog/wp-content/uploads/2018/11/37.png)

## Class ของสี

class utilities ที่ใช้บ่อยอีกตัวคือ เกี่ยวกับสี

อ่านได้ที่ [https://getbootstrap.com/docs/4.0/utilities/colors/](https://getbootstrap.com/docs/4.0/utilities/colors/)

หลักๆคือ มีให้เลือกใช้ดังนี้

```css

_primary
**danger
**success
**info
**dark
\_\_light_
```

ใช้กับ class พวก bg- , text-  
เช่น

```html
<h3 class="bg-primary p-2 text-white">Service</h3>
```

![38](https://benzneststudios.com/blog/wp-content/uploads/2018/11/38.png)

### วิธี Custom

เช่นอยากเปลี่ยนสีให้ต่างจาก bootstrap ให้ใส่ !important ด้วย

```css
.bg-primary {
  background: #4f85d7 !important;
}
```

## การใช้ Animate.css

เข้าไปดาวน์โหลด css ได้ที่  
[https://daneden.github.io/animate.css/](https://daneden.github.io/animate.css/)

แล้วเพิ่มเข้ามาใน HTML ของเรา

```html
<link rel="stylesheet" href="css/animate.css" />
```

วิธีการเรียกใช้ ก็แค่ใช้ class  
animated = เรียกใช้ animated  
infinite = ทำไปเรื่อยๆ  
pulse = Animation แบบ pulse  
delay-1s = delay 1 วินาที

```html
<h2 class="text-center animated infinite pulse delay-1s">
  <i class="far fa-kiss-wink-heart"></i>

  Nothing in life is to be feared, it is only to be understood. Now is the time
  to understand more, so that we may fear less.
</h2>
```

![g1](https://benzneststudios.com/blog/wp-content/uploads/2018/11/g1.gif)

### Source code

[https://gist.github.com/benznest/ad45fd26b773e1ff47bb9727a4702494](https://gist.github.com/benznest/ad45fd26b773e1ff47bb9727a4702494)

## สรุป

บทความนี้ก็สรุปคร่าวๆเกี่ยวกับการใช้ bootstrap ที่เป็นเรื่องสำคัญๆ เช่นการใช้ grid จัดวาง layout การทำให้รองรับ responsive การใช้ utility class เช่น margin padding รวมถึงพวกสี เช่น primary danger ที่เจอบ่อยมาก แล้วก็แนะนำเกี่ยวกับหน่วย rem ด้วย แถมด้วยเปลี่ยน Font กับใส่ Icon

ตอนหน้าจะเป็นเรื่องของการใช้ component อื่นๆที่ใช้งานบ่อยๆ รวมถึงเทคนิคเกี่ยวกับ bootstrap เพิ่มเติมด้วย

> Source : [benzneststudios.com](https://benzneststudios.com/blog/web/bootstrap-4-basic-part-1/).
