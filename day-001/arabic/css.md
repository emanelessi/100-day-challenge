<style>
  body {
    direction: rtl;
    text-align: right;
  }
</style>

### CSS (Cascading Style Sheets)

هي لغة تستخدم لتنسيق وتجميل صفحات الويب. تهدف إلى فصل المحتوى (الذي يتم إنشاؤه باستخدام HTML) عن العرض أو المظهر البصري.
يمكن تطبيق CSS مباشرة داخل ملف HTML أو بشكل خارجي عبر ملف CSS منفصل.

### الأساسيات في CSS

#### 1. **التحديدات (Selectors)**

التحديدات تُستخدم لاختيار العناصر في صفحة الويب لتطبيق الأنماط عليها.

- **التحديد بالعناصر (Type Selector):**
  يستخدم لتطبيق الأنماط على نوع معين من العناصر.

  ```css
  p {
      color: blue;
  }
  ```
  هذا الكود يغير لون جميع الفقرات `<p>` إلى اللون الأزرق.

- **التحديد بالصفوف (Class Selector):**  
  يتم استخدام الكلاس لتطبيق الأنماط على العناصر التي تحتوي على اسم كلاس معين.

  ```css
  .myClass {
      font-size: 18px;
  }
  ```

- **التحديد بالهوية (ID Selector):**  
  يحدد عنصرًا باستخدام معرف (`id`)، ويجب أن يكون فريدًا في الصفحة.

  ```css
  #header {
      background-color: #f0f0f0;
  }
  ```

#### 2. **الألوان والخلفيات (Colors and Backgrounds)**

- **تغيير لون النص:**

  ```css
  h1 {
      color: #333;
  }
  ```

- **تغيير لون الخلفية:**

  ```css
  body {
      background-color: #f4f4f4;
  }
  ```

- **إضافة صورة خلفية:**

  ```css
  div {
      background-image: url('image.jpg');
      background-size: cover;
  }
  ```

#### 3. **الأبعاد (Dimensions)**

CSS يُمكّن من تحديد العرض والارتفاع للعناصر.

- **عرض العنصر:**

  ```css
  div {
      width: 200px;
  }
  ```

- **ارتفاع العنصر:**

  ```css
  div {
      height: 300px;
  }
  ```

#### 4. **الهامش والحشو (Margin and Padding)**

- **الهامش (Margin):**  
  المسافة الخارجية بين العنصر والعناصر الأخرى.

  ```css
  div {
      margin: 20px;
  }
  ```

- **الحشو (Padding):**  
  المسافة الداخلية بين حدود العنصر والمحتوى الداخلي.

  ```css
  div {
      padding: 10px;
  }
  ```

#### 5. **التنسيق النصي (Text Styling)**

CSS يُستخدم لتنسيق النصوص بطرق مختلفة.

- **تغيير حجم الخط:**

  ```css
  p {
      font-size: 16px;
  }
  ```

- **جعل النص عريضًا:**

  ```css
  p {
      font-weight: bold;
  }
  ```

- **محاذاة النص:**

  ```css
  p {
      text-align: center;
  }
  ```

#### 6. **النماذج (Forms)**

CSS يساهم في تحسين مظهر عناصر النماذج مثل الحقول وأزرار الإرسال.

- **تنسيق حقول الإدخال:**

  ```css
  input[type="text"] {
      border: 1px solid #ccc;
      padding: 10px;
      width: 100%;
  }
  ```

- **تنسيق أزرار الإرسال:**

  ```css
  input[type="submit"] {
      background-color: green;
      color: white;
      padding: 10px 20px;
      border: none;
      cursor: pointer;
  }
  ```

#### 7. **النماذج الشبكية (CSS Grid)**

النماذج الشبكية تتيح تقسيم الصفحة إلى شبكة مرنة.

- **إنشاء شبكة بسيطة:**

  ```css
  .container {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      gap: 10px;
  }
  ```

- **دمج الأعمدة أو الصفوف:**

  يمكنك دمج الأعمدة أو الصفوف لجعل عنصر واحد يمتد عبر أكثر من عمود أو صف.

  ```css
  .item1 {
      grid-column: 1 / span 2; /* يمتد على عمودين */
  }
  ```

#### 8. **التخطيطات باستخدام Flexbox**

Flexbox يُمكّن من إنشاء تصاميم مرنة وسهلة.

- **استخدام Flexbox لتوزيع العناصر:**

  ```css
  .container {
      display: flex;
      justify-content: space-between;
  }
  ```

- **التحكم في الاتجاه (Flex Direction):**

  يمكن التحكم في اتجاه العناصر إما أفقيًا أو عموديًا:

  ```css
  .container {
      display: flex;
      flex-direction: column;
  }
  ```

  هذا الكود يجعل العناصر تظهر في عمود بدلاً من صف.

- **التحكم في المرونة (Flex Grow):**

  يمكنك جعل عنصر معين يأخذ حيزًا أكبر أو أصغر بناءً على مرونته:

  ```css
  .item {
      flex-grow: 2;
  }
  ```

  هذا يعني أن العنصر الذي يحتوي على `flex-grow: 2` سيأخذ ضعف المساحة مقارنة بالعناصر الأخرى.

### 9. **CSS Grid vs Flexbox**

**Flexbox:**

- **تصميم بسيط باستخدام Flexbox:**

  ```css
  .flex-container {
      display: flex;
      justify-content: space-between;
  }

  .flex-item {
      width: 30%;
  }
  ```

**CSS Grid:**

- **تصميم شبكة باستخدام CSS Grid:**

  ```css
  .grid-container {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 10px;
  }

  .grid-item {
      background: #4CAF50;
      height: 100px;
  }
  ```

**مقارنة:**

- **Flexbox** يناسب توزيع العناصر في صف أو عمود واحد.
- **Grid** مثالي لإنشاء تخطيطات متعددة الأبعاد.

#### 10. **التأثيرات (Transitions and Animations)**

- **الانتقالات (Transitions):**

  ```css
  button {
      transition: background-color 0.3s ease;
  }

  button:hover {
      background-color: blue;
  }
  ```

#### 11. **المتغيرات (CSS Variables)**

المتغيرات في CSS تسهل إعادة استخدام القيم في الأنماط المختلفة.

- **تعريف متغير:**

  ```css
  :root {
      --main-color: #4CAF50;
      --padding-size: 10px;
  }
  ```

- **استخدام المتغيرات:**

  ```css
  .box {
      background-color: var(--main-color);
      padding: var(--padding-size);
  }
  ```

المتغيرات تجعل الأكواد أكثر نظافة وقابلة لإعادة الاستخدام.

### 12. **الوحدات النسبية (Relative Units)**

الوحدات مثل `em` و `rem` تتيح مرونة أكبر في تصميماتك.

- **وحدة `em`:**

  تعتمد على حجم الخط الحالي للعنصر الأب.

  ```css
  p {
      font-size: 1.5em; /* 1.5 ضعف حجم الخط الأساسي */
  }
  ```

- **وحدة `rem`:**

  تعتمد على حجم الخط الجذري (`root`).

  ```css
  body {
      font-size: 16px;
  }

  h1 {
      font-size: 2rem; /* 2 ضعف حجم الخط الجذري */
  }
  ```

### 13.  **الاستفسارات الإعلامية (Media Queries)**

الاستفسارات الإعلامية تساعد في جعل الموقع متجاوبًا مع الشاشات المختلفة.

- **تغيير التصميم بناءً على عرض الشاشة:**

  ```css
  @media (max-width: 768px) {
      .container {
          flex-direction: column;
      }
  }
  ```

  هذا الكود يجعل العناصر تتحول إلى عمود بدلاً من صف عند عرض الصفحة على شاشة أصغر.

### 14.  **التحكم في التكديس (Z-Index)**

`z-index` يحدد ترتيب العناصر على المحور العمودي (الأمام والخلف).

- **زيادة ترتيب العنصر للأمام:**

  ```css
  .box {
      position: relative;
      z-index: 10;
  }
  ```

### 15.  **التظليل (Box Shadows & Text Shadows)**

- **ظل الصندوق (Box Shadow):**

  يمكن إضافة ظلال للعناصر لإضفاء تأثير ثلاثي الأبعاد.

  ```css
  .box {
      box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.3);
  }
  ```

- **ظل النص (Text Shadow):**

  يمكن إضافة تأثير الظل للنصوص.

  ```css
  h1 {
      text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3);
  }
  ```

### **CSS Pseudo-Classes and Pseudo-Elements** .16

- **Pseudo-Classes:**

  تُستخدم لتطبيق الأنماط على العناصر بناءً على حالة معينة.

  ```css
  a:hover {
      color: red;
  }
  ```

- **Pseudo-Elements:**

  تستخدم لتنسيق جزء معين من العنصر مثل الحرف الأول.

  ```css
  p::first-letter {
      font-size: 2em;
      color: red;
  }
  ```

### 16. **التصميم المتجاوب (Responsive Design)**

**استخدام الاستفسارات الإعلامية:**

- **تصميم متجاوب للعرض الصغير:**

  ```css
  @media (max-width: 768px) {
      .container {
          flex-direction: column;
      }
  }

  @media (min-width: 769px) {
      .container {
          flex-direction: row;
      }
  }
  ```

يغير هذا التصميم اتجاه العناصر بناءً على عرض الشاشة.

### 18. **التحسينات في الأداء (Performance Optimization)**

**تحسينات CSS:**

- **تقليل حجم الملفات:**

  استخدم أدوات مثل [CSSNano](https://cssnano.co/) لضغط ملفات CSS وتقليل حجمها.

- **تحميل الكسل (Lazy Loading):**

  استخدم خاصية `media` لتحميل CSS فقط عند الحاجة:

  ```html
  <link rel="stylesheet" href="styles.css" media="(min-width: 600px)">
  ```

### 19. **أدوات CSS**

**Preprocessors (مثل Sass):**

- **استخدام Sass لتحسين تنظيم CSS:**

  ```scss
  $primary-color: #4CAF50;

  body {
      background-color: $primary-color;
  }
  ```

**PostCSS:**

- **استخدام PostCSS مع Autoprefixer:**

  استخدم [Autoprefixer](https://autoprefixer.github.io/) لإضافة بادئات المتصفح تلقائيًا:

  ```css
  .box {
      display: flex;
      display: -webkit-flex; /* Safari */
  }
  ```

### 20. **التأثيرات المتقدمة في CSS**

**CSS Filters:**

- **إضافة تأثيرات فلتر على الصور:**

  ```css
  img {
      filter: grayscale(100%) blur(5px);
  }
  ```

**Clip-path:**

- **قص العناصر باستخدام `clip-path`:**

  ```css
  .clip-box {
      clip-path: circle(50%);
      background: #4CAF50;
      width: 100px;
      height: 100px;
  }
  ```

### 21. **التجربة العملية**

**مشروع عملي:**

يمكنك إنشاء مشروع ويب يعرض كيفية استخدام Flexbox وGrid بشكل متزامن، مثل تصميم لوحة تحكم تحتوي على أقسام متعددة باستخدام
Grid، وداخل كل قسم، استخدام Flexbox لتوزيع العناصر بشكل مرن.

**مثال:**

```html
<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>مشروع CSS</title>
    <style>
        :root {
            --main-bg-color: #f0f0f0;
            --primary-color: #4CAF50;
            --font-size: 16px;
        }

        body {
            background-color: var(--main-bg-color);
            font-size: var(--font-size);
            margin: 0;
            padding: 0;
        }

        .container {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 10px;
            padding: 20px;
        }

        .box {
            background: var(--primary-color);
            height: 100px;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            font-size: 1.2em;
            transition: transform 0.3s ease;
        }

        .box:hover {
            transform: scale(1.1);
        }

        @media (max-width: 768px) {
            .container {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

<div class="container">
    <div class="box">مربع 1</div>
    <div class="box">مربع 2</div>
    <div class="box">مربع 3</div>
</div>

</body>
</html>
```

هذا المثال يدمج CSS Grid و Flexbox ويوضح كيفية استخدام المتغيرات والفلاتر في تصميم بسيط.

### خاتمة

CSS لغة قوية يمكن استخدامها لبناء تخطيطات معقدة، تطبيق تأثيرات متقدمة، وإنشاء مواقع متجاوبة وحديثة. في درسك، يمكنك
التركيز على هذه المفاهيم المتقدمة لتقديم تصميمات احترافية تواكب التحديات الحديثة في تطوير الويب.


---
### تواصل معي

يمكنك متابعتي على وسائل التواصل الاجتماعي التالية:

- **Instagram:** [emanelessi](https://www.instagram.com/emanelessi/)
- **LinkedIn:** [emanelessi](https://www.linkedin.com/in/emanelessi/)

أنا متاح لأي استفسار أو تعاون في المشاريع المستقبلية. لا تتردد في التواصل معي!

