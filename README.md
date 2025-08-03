# 🎨 مدخل إلى CSS

CSS هي اختصار لـ Cascading Style Sheets، وهي اللغة المسؤولة عن تنسيق شكل صفحات الويب، من ألوان وخطوط وتوزيع ومسافات وغير ذلك، وهي تعمل مكملة للغة HTML.

## 📑 الفهرس

- [🎨 مدخل إلى CSS](#-مدخل-إلى-css)
  - [📑 الفهرس](#-الفهرس)
  - [ما هي CSS؟](#ما-هي-css)
  - [ربط ملف CSS بـ HTML](#ربط-ملف-css-بـ-html)
  - [طرق كتابة CSS](#طرق-كتابة-css)
  - [الخصائص الأساسية لتنسيق العناصر](#الخصائص-الأساسية-لتنسيق-العناصر)
    - [اللون](#اللون)
    - [حجم الخط](#حجم-الخط)
    - [الخلفية](#الخلفية)
    - [الأبعاد](#الأبعاد)
    - [الحدود](#الحدود)
    - [الزوايا](#الزوايا)
    - [التباعد الداخلي والخارجي](#التباعد-الداخلي-والخارجي)
    - [ملاحظة هامة عن الـ Box Model](#ملاحظة-هامة-عن-الـ-box-model)
    - [الخطوط](#الخطوط)
  - [أنواع المحددات (Selectors)](#أنواع-المحددات-selectors)
    - [المحددات البسيطة](#المحددات-البسيطة)
      - [ملاحظات](#ملاحظات)
    - [محددات أكثر تعقيدًا](#محددات-أكثر-تعقيدًا)
    - [محددات السمات](#محددات-السمات)
  - [الوحدات المستخدمة في CSS](#الوحدات-المستخدمة-في-css)
    - [استخدام الأمثلة](#استخدام-الأمثلة)
    - [مقدار الوحدة](#مقدار-الوحدة)
    - [ملاحظـات](#ملاحظـات)
    - [مشكلة النسبة المئوية](#مشكلة-النسبة-المئوية)
  - [التعامل مع الألوان](#التعامل-مع-الألوان)
  - [الخلفيات](#الخلفيات)
    - [ملاحظـات](#ملاحظـات-1)
    - [ملاحظــات](#ملاحظــات)
    - [خصائص الخلفية](#خصائص-الخلفية)
      - [الفرق بين background-clip و background-origin](#الفرق-بين-background-clip-و-background-origin)
    - [اختصار الخلفية](#اختصار-الخلفية)
      - [ملاحظات مهمة](#ملاحظات-مهمة)
  - [أمثلة عملية](#أمثلة-عملية)
  - [الخطوط والنصوص](#الخطوط-والنصوص)
    - [اختصار الخصائص الخمسة لسطر واحد](#اختصار-الخصائص-الخمسة-لسطر-واحد)
  - [الصندوق (Box Model)](#الصندوق-box-model)
    - [padding](#padding)
    - [margin](#margin)
    - [border](#border)
    - [box-sizing](#box-sizing)
  - [العناصر Block وInline](#العناصر-block-وinline)
    - [التحكم في النوع](#التحكم-في-النوع)
    - [visibility](#visibility)
  - [خاصية overflow](#خاصية-overflow)
  - [z-index](#z-index)
  - [Float](#float)
    - [ملاحظـــات](#ملاحظـــات)
    - [حل مشكلة انهيار العنصر الأب دون تعديل HTML بإضافة محتوى وهمي](#حل-مشكلة-انهيار-العنصر-الأب-دون-تعديل-html-بإضافة-محتوى-وهمي)
  - [القوائم (List Styles)](#القوائم-list-styles)
    - [موقع النقطة](#موقع-النقطة)
    - [صورة بدلاً من النقاط](#صورة-بدلاً-من-النقاط)
    - [اختصار](#اختصار)
  - [Table style](#table-style)
  - [التأثيرات البصرية (Hover, Focus, Checked)](#التأثيرات-البصرية-hover-focus-checked)
    - [Hover](#hover)
    - [Active](#active)
    - [Empty](#empty)
    - [Visited](#visited)
    - [Link](#link)
    - [Focus](#focus)
    - [Disabled](#disabled)
    - [حالات `<input>` المدعومة في CSS](#حالات-input-المدعومة-في-css)
    - [ملاحظات مهمـة](#ملاحظات-مهمـة)
    - [المراجع المفيدة](#المراجع-المفيدة)
    - [Checked](#checked)
    - [Opacity](#opacity)
  - [الأمثلة العملية](#الأمثلة-العملية)
    - [الفرق بين النقطتين `:` والأقواس المربعة `[]`](#الفرق-بين-النقطتين--والأقواس-المربعة-)
  - [العناصر الزائفة (Pseudo-elements)](#العناصر-الزائفة-pseudo-elements)
    - [::first-letter](#first-letter)
    - [::first-line](#first-line)
    - [::selection](#selection)
  - [تخطيط الصفحة (Flexbox, Grid)](#تخطيط-الصفحة-flexbox-grid)
    - [Flexbox](#flexbox)
      - [عناصر الأب](#عناصر-الأب)
        - [الفرق بين `align-items`, `align-content`](#الفرق-بين-align-items-align-content)
      - [عناصر الابن](#عناصر-الابن)
    - [Grid](#grid)
      - [عنـاصر الأب](#عنـاصر-الأب)
  - [الاستجابة للشاشات (Media Queries)](#الاستجابة-للشاشات-media-queries)
  - [مفاهيم متقدمة](#مفاهيم-متقدمة)
    - [التغليف (Wrapping)](#التغليف-wrapping)
      - [التحكم في التغليف](#التحكم-في-التغليف)
    - [التحويلات (Transforms)](#التحويلات-transforms)
      - [الفرق بين `position` (مع `top` / `bottom` / `left` / `right`) وبين `transform: translate()`](#الفرق-بين-position-مع-top--bottom--left--right-وبين-transform-translate)
    - [التحريكات (Translates)](#التحريكات-translates)
    - [الأحجام (Scales)](#الأحجام-scales)
    - [الدوران (Rotate)](#الدوران-rotate)
    - [الانتقالات (Transitions)](#الانتقالات-transitions)
    - [التحريكات (Animations)](#التحريكات-animations)
    - [الوراثة (Inheritance)](#الوراثة-inheritance)
    - [all: inherit](#all-inherit)
  - [تعليقات في CSS](#تعليقات-في-css)
  - [تحديد الكل](#تحديد-الكل)
  - [وضع النص في الوسـط](#وضع-النص-في-الوسـط)
    - [أفقياً](#أفقياً)
    - [عموديًا (Flex)](#عموديًا-flex)
    - [ملاحظات هامـة](#ملاحظات-هامـة)
    - [أمثلة توضيحية](#أمثلة-توضيحية)
      - [1. محاذاة أفقيـة](#1-محاذاة-أفقيـة)
      - [2. محاذاة عموديـة](#2-محاذاة-عموديـة)
      - [3. محاذاة مركزية شاملة (أفقي + عمودي)](#3-محاذاة-مركزية-شاملة-أفقي--عمودي)
    - [التحذيرات الشائعة](#التحذيرات-الشائعة)
  - [ملاحظات هامة](#ملاحظات-هامة)

## ما هي CSS؟

CSS هي لغة تنسيق تستخدم مع HTML لإضفاء الشكل الجميل والمنظم على صفحات الويب. فبينما HTML تهتم ببناء المحتوى مثل العناوين والفقرات والصور، تتولى CSS تنسيق هذا المحتوى من حيث الألوان، الأحجام، المواقع، الخطوط، الخلفيات، وغيرها.

## ربط ملف CSS بـ HTML

لربط CSS خارجي بملف HTML، نضع الوسم التالي داخل رأس الصفحة:

```html
<link rel="stylesheet" href="style.css">
```

هنا `style.css` هو اسم الملف الموجود في نفس المجلد مع ملف HTML. الامتداد `.css` ضروري.

## طرق كتابة CSS

هناك ثلاث طرق رئيسية لاستخدام CSS:

1. **الربط الخارجي (External CSS):**
   أفضل الطرق، حيث يكون التنسيق محفوظًا في ملف منفصل.
   يتم ربطه كما في المثال السابق.

2. **داخل وسم `<style>` في `<head>`:**

   ```html
   <style>
     p {
       color: blue;
       font-size: 18px;
     }
   </style>
   ```

- `p`: هو وسم `HTML` الذي نريد تنسيق محتواه
- `color`: أحد التنسيقات (خاصية اللون)
- `:`: هو الذي يعطي قيمة للخاصية
- `;`: يسمح بالإنتقال لسطر جديد

3. **داخل الوسم نفسه (Inline CSS):**

   ```html
   <p style="color: red; font-size: 20px;">نص داخل الفقرة</p>
   ```

⚠️ الأولوية عند التطبيق:

- التنسيق الأقرب للعنصر يطغى
- Inline > داخل `<style>` > خارجي (ملف CSS)

من الأفضل دائمًا الاعتماد على الملفات الخارجية لتنظيم الكود وتسهيل التعديل عليه.

---

## الخصائص الأساسية لتنسيق العناصر

الخصائص الأساسية في CSS تسمح لك بتحديد شكل العناصر مثل الألوان والأحجام والخلفيات والحدود. إليك أهمها:

### اللون

لتغيير لون النص داخل عنصر:

```css
p {
  color: red;
}
```

يمكن اختيار اللون بالاسم، أو بنظام RGB:

```css
color: rgb(255, 0, 0);
```

أو RGBA مع شفافية:

```css
color: rgba(230, 22, 0, 0.7);
```

أو بالهيكساديسيمال:

```css
color: #ff0000;
```

أو بنظام HSL وHSLA:

```css
color: hsl(0, 100%, 50%);
color: hsla(0, 100%, 50%, 0.5);
```

### حجم الخط

```css
font-size: 16px;
```

يمكن استخدام وحدات أخرى مثل:

- px: بكسل
- em: نسبة لحجم الخط الأب
- rem: نسبة للجذر
- %: نسبة مئوية
- vw/vh: نسبة لحجم الشاشة

### الخلفية

لتلوين الخلفية:

```css
background-color: yellow;
```

لإضافة صورة خلفية:

```css
background-image: url("image.jpg");
```

خصائص أخرى:

- background-repeat: no-repeat, repeat-x, repeat-y
- background-size: cover, contain, 100px 200px
- background-position: center, top left
- background-attachment: fixed, scroll

يمكن اختصار الكل:

```css
background: url("image.jpg") no-repeat center / cover;
```

---

### الأبعاد

لتحديد العرض والارتفاع:

```css
width: 200px;
height: 100px;
```

تحديد أقصى عرض:

```css
max-width: 200px
```

عرض متغير حسب حجم النافذة ينتهي عند `200px`

تحديد أدنى عرض:

```css
min-width: 200px
```

عرض متغير حسب حجم النافذة يبدأ من `200px`

تحديد أقصى ارتفاع:

```css
max-height: 200px
```

ارتفاع متغير حسب حجم المحتوى ينتهي عند `200px`

تحديد أدنى ارتفاع:

```css
min-height: 200px
```

ارتفاع متغير حسب حجم المحتوى يبدأ من `200px`

وحدات مقبولة:

- px, em, rem, %, vw, vh

---

### الحدود

تتكون من:

- border-width
- border-style
  - soild
  - dotted
  - dashed
  - .etc
- border-color

مثال:

```css
border: 2px solid black;
```

الترتيب غير إجباري

- يمكن التحكم بكل خاصية:

```css
border-width: 3px
border-style: solid
border-color: red
```

يمكن التحكم بكل جانب:

- الأعلى:

```css
border-top: 1px dashed red;
```

- الأسفل:

```css
border-bottom: 5px red dashed;
```

- اليسار:

```css
border-left: red dashed 2px;
```

- اليمين:

```css
border-right: dashed blue 2px;
```

---

### الزوايا

```css
border-redius: 50px 20px 50px 20px
```

- قيمة واحدة: تحدد كل الزوايا

- قيمتين: كل قيمة تحدد زاويتين:
  - أول قيمة:
    - top left
    - bottom right
  - ثاني قيمة:
    - top right
    - bottom left

- أربع قيم: كل قيمة تحدد زاوية:
  - الأولى: top left
  - الثانية: top right
  - الثالثة: bottom right
  - الرابعة: bottom left

- يمكن تحديد قيمة لكل زاوية:

```css
border-top-left-radius: 50px
```

- يمكن تحديد قيمتين لكل زاوية

```css
border-bottom-right-radius: 40px 60px;
```

كل قيمة تأخذ زاوية الاتجاه على الترتيب

يمكن إنشاء دائرة إذا كان العرض يساوي الطول و قيمة `border-radius` نصف قيمة إحداهما مثل:

```css
width: 490px;
height: 490px;
border-radius: 245px;
background-color: red;
```

يمكن جعل `border-radius: 505%;`

---

### التباعد الداخلي والخارجي

- **padding**: المسافة داخل العنصر بين المحتوى والحدود
- **margin**: المسافة خارج العنصر

```css
padding: 10px 20px 10px 20px;
margin: 5px 10px 15px 20px;
```

الترتيب: top, right, bottom, left.

لو قيمة واحدة: كل الاتجاهات

لو قيمتين: أول قيمة للأعلى والأسفل وثاني قيمة لليمين واليسار

- يمكن التحكم بكل اتجاه:

```css
padding-top: 100px;
padding-right: 100px;
padding-bottom: 100px;
padding-left: 100px;

margin-top: 100px;
margin-right: 100px;
margin-bottom: 100px;
margin-left: 100px;
```

⚠️ يمكن استخدام قيم سالبة في margin فقط لعكس الاتجاه.

- ضبط العنصر في المنتصف أفقيًا:

```css
margin: 0 auto;
```

- `auto`: تُحسب المسافة تلقائيًا لتوسيط العنصر
- القيمة 0 للهامش العلوي والسفلي (يمكن تعديلها حسب الحاجة)
- عند ضبط العنصر بالمنتصف باستخدام `margin-right` و`margin-left` بنفس القيمة (مثل margin: 0 200px;) فعند تصغير النافذة:
- `margin-left` يظل ثابتًا
- `margin-right` لا يتكيف مع المساحة المتبقية
- مما يسبب مساحة غير مرغوب فيها على اليمين
- لذا فالطريقة الأمثل هي استخدام `auto`
- `auto` غير مخصصة للضبط الرأسي

---

### ملاحظة هامة عن الـ Box Model

العناصر لها:

- Content
- Padding
- Border
- Margin

وخاصية:

```css
box-sizing: border-box;
```

تجعل padding وborder محسوبة ضمن width/height.

---

### الخطوط

- font-family: تحديد نوع الخط

```css
font-family: Arial, sans-serif;
```

- font-weight: سمك الخط (normal, bold, أو أرقام مثل 100, 400, 700)
- line-height: المسافة بين الأسطر
- letter-spacing: المسافة بين الحروف
- text-align: left, right, center, justify (يوسع المسافات بين الكلمات لتنتهي عند نفس المحاذاة)
- direction: rtl (للعربية), ltr (للانجليزية)

---

## أنواع المحددات (Selectors)

CSS يستخدم محددات لاستهداف العناصر التي تريد تنسيقها.

### المحددات البسيطة

- بالاسم:

```css
p { color: blue; }
```

ينطبق على كل الوسوم `<p>`.

- بالكلاس:

```html
<div class="highlight">...</div>
```

يختصر إلى:

```html
.highlight
```

```css
.highlight { color: red; }
```

استدعاء الكلاس بنقطة `.`.

- بالمعرف (ID):

```html
<p id="unique">...</p>
```

يختصر إلى:

```html
#unique
```

```css
#unique { color: green; }
```

استدعاء الـ ID بالرمز `#`.

#### ملاحظات

لا يصلح أن تضع أرقاما ببداية الكلاس أو المعرف

يمكن كتابة أكثر من قيمة واستدعاء كل قيمة على حدة مثال:

```html
<div class="green">
    <h1 class="red float"></h1>
    <h1 class="blue float"></h1>
    <h1 class="yellow float"></h1>
</div>
```

```css
.green {
    background: green;
}
.red {
    height: 50px;
    width: 100px;
    background: red;
}
.blue {
    height: 50px;
    width: 100px;
    background: blue;
}
.yellow {
    height: 50px;
    width: 100px;
    background: yellow;
}
.float {
    float: right;
}
```

---

### محددات أكثر تعقيدًا

- تحديد أكثر من عنصر

```css
p , h1 { color: red; }
```

`,` يسمح بإضافة أكثر من عنصر

- تحديد الجسم كله

```css
body { color: red; }
```

يحدث التنسيق على كل العناصر الوارثة من body في معظم المتصفحات وهي العناصر النصية مثل:

`<p>`

`<h1>`

`<span>`

`<a>`

هناك بعض العناصر لها بعض الأنماط الافتراضية بإمكانها تجاوز التوريث كاللون مثلا عند `<a>`

- تحديد الجسم على العناصر ذو الأنماط الافتراضية

```css
body { color: red; }
input, a { color: inherit; }
```

أي تغيير في اللون سيرثه أيضا `input`, `a`

- تحديد الصفحة كلها

```css
* { color: red; }
```

يحدث التنسيق على كل العناصر مباشرة بما في ذلك العناصر الغير قابلة للتوريث من body وهي العناصر التفاعلية التي لها أنماط افتراضية مثل:

`<input>`

`<button>`

`<textarea>`

`<select>`

`<progress>`

بعض تلك العناصر لها خصائص تنسيق خاصة بها مثل `<progress>`, `<input type="checkbox">` يتم تحديد لونهما من خلال `accent-color`

- تحديد كلاس داخل عنصر

```css
div.p { color: orange; }
```

أي كلاس له نفس الاسم `p` خارج `div` لن يضيفه

- تحديد معرف داخل عنصر

```css
div#p { color: orange; }
```

أي معرف له نفس الاسم `p` خارج `div` لن يضيفه

- تحديد عنصر داخل عنصر:

```css
div p { color: orange; }
```

ينطبق على كل p داخل div.

- تحديد عنصر داخل عنصر داخل عنصر:

```css
div p strong { color: orange; }
```

ينطبق على كل strong داخل p داخل div وهكذا.

- تحديد العنصر مباشرة داخل عنصر:

```css
div > p { color: purple; }
```

ينطبق فقط على الأبناء المباشرين وليس الأحفاد.

- تحديد العنصر مباشرة داخل عنصر داخل عنصر:

```css
div > p > strong { color: purple; }
```

ينطبق فقط على الأحفاد المباشرين وليس أبناء الأحفاد وهكذا.

لتحديد ابن أو حفيد أو أي سلالة بعينها نميزه من خلال `class` أو `id` مثلا:

```html
<div class="parent">
  <p class="child">
    هذا النص يحتوي على <strong id="grandchild">عنصر قوي</strong>
  </p>
  <p>
    هذا <strong>لن يتأثر</strong> لأنه ليس ابنًا مباشرًا للـ div
  </p>
</div>
```

```css
.parent .child { 
  background-color: lightyellow;
}
#grandchild {
  border: 2px dashed green;
}
```

سينسق `background-color` جملة `هذا النص يحتوي على عنصر قوي`
سينسق `border` جملة `عنصر قوي`

- تحديد أخ شقيق لاحق:

تستخدم اعتمادا على تأثير يطرق على الأخ السابق

```css
h2 + p { margin-top: 0; }
```

ينطبق على أول p بعد h2 مباشرة (ليس بينهم وسم إخر) في نفس النطاق.

- تحديد كل الأشقاء اللاحقين:

```css
h2 ~ p { color: gray; }
```

ينطبق على كل p بعد h2 في نفس المستوى حنى لو يفصل بينهم عناصر أخرى بشرط أن تكون بنفس النطاق.

---

### محددات السمات

لتحديد عنصر بصفة خاصة:

```html
<input type="text">
```

```css
input[type="text"] {
  background-color: lightyellow;
}
```

يمكن استخدام سمات أخرى مثل placeholder.

⚠️ يفضل عدم استهداف value لأنها متغيرة.

طرق التحديد:

- [attr]
  - `[type] { background: green; }`
- element[attr]
  - `input[type] { background: green; }`
- [attr="value"]
  - `[type="text"] { background: green; }`
- element[attr="value]
  - `input[type="text"] { background: green; }`
- [attr ^="value"] start with
  - تطبيق التنسيق على ما يبدأ بما هو محدد
  - `[href ^="www"] { color: red; }`
- [attr $="value"] end with
  - تطبيق التنسيق على ما ينتهي بما هو محدد
  - `[href $="com"] { color: red; }`
- [attr *="value"] containing a spacefied value
  - تطبيق التنسيق على ما يحتوي بما هو محدد
  - `[href *="/"] { color: red; }`
- [attr ~="value"] containing a spacefied word
  - تطبيق التنسيق على ما يحتوي على كلمة محددة
  - `[class ~="red"] { border: 2px solid red; }`
- [attr ="value" i] case sensitive
  - إلغاء حالة الحروف (مع كل المحددات)
  - `[class ~="RED" i] { border: 2px solid red; }`
  - `[type="TEXT" i] { background: green; }`

---

## الوحدات المستخدمة في CSS

الوحدات تسمح لك بقياس المسافات والأحجام:

- **px**: بكسل – وحدة ثابتة.
- **em**: نسبة لحجم خط الأب.
- **rem**: نسبة لحجم الخط الجذر (`root`).
- **%**: نسبة مئوية لحاوية العنصر الأب.
- **vw / vh**: نسبة من عرض أو ارتفاع الشاشة وليس الأب.
- **fr**: في Grid لتقسيم المساحات.
- **auto**: يعتمد على المحتوى.
- **calc**(): للعمليات الحسابية مثلا: (100% - 50px)

---

### استخدام الأمثلة

```css
width: 80%;
font-size: 1.2em;
margin: auto;
height: 50vh;
```

---

### مقدار الوحدة

- Normal text = `<p>` = 16px = 1em = 100%
- `<h1>` = 32px = 2em = 200%
- `root` = 16px = 1rem

### ملاحظـات

✅ يفضل استخدام وحدات مرنة مثل em, rem, % للواجهات المتجاوبة.  
✅ px ثابتة لكنها دقيقة للتصميم الثابت.  
✅ vh وvw ممتازة لتصميمات الشاشة الكاملة.

### مشكلة النسبة المئوية

- النسبة المئوية تحدد قيمة العرض بالنسبة للأب
- القيمة الإفتراضية للنسبة المئوية للعرض هي `100%` من عرض الأب ويمكن تغييرها
- الأب هو العنصر الخارجي فلو العنصر واحد فيكون الأب هو جسم الموقع (المتصفح)
- النسبة المئؤية لا تحدد على عناصر الـ `inline` بل يعمل على العناصر الكتلية (block/inline-block)
- الارتفاع يتغير بالنسبة المئوية فقط إذا كان العنصر الأب مُحدد الارتفاع بوحدة مطلقة
- القيمة الإفتراضية للنسبة المئوية للطول هي `auto` بالنسبة لطول المحتوى (تصبح 0 إذا كان العنصر فارغًا)، ولا يمكن تغييرها (فقظ نغير طول الأب بوحدة أخرى مطلقة كالبكسل والابن يتبعه حسب النسبة)
- أما قيمة العرض تكون متغيرة حسب حجم المتصفح

---

## التعامل مع الألوان

يمكنك كتابة الألوان بعدة طرق:

- بالاسم:

```css
color: red;
```

- بنظام RGB:

```css
color: rgb(255, 0, 0);
```

- بنظام RGBA (مع الشفافية):

```css
color: rgba(230, 22, 0, 0.7);
```

القيمة الأخيرة بين 0 و1 للتحكم في الشفافية.

- بالنظام الست عشري (Hex):

```css
color: #ff0000;
```

اختصارات ممكنة:

```css
color: #f00;
```

- بنظام HSL / HSLA:

```css
color: hsl(0, 100%, 50%);
color: hsla(0, 100%, 50%, 0.5);
```

---

## الخلفيات

لإضافة لون خلفية:

```css
background-color: lightblue;
```

لإضافة صورة خلفية:

```css
background-image: url("image.jpg");
```

لدمج ألوان الخلفية خطيا:

```css
background-image: linear-gradient(to right, red 60%, blue 40%);
```

linear-gradient: تأخذ تلاث قيم:

  1. اتجاه التدرج مثل:
     1. to bottom (الافتراضية)
     2. to right bottom, to bottom right ...etc
     3. 90deg, 360deg ...etc
  2. من اللون
  3. ألى اللون

### ملاحظـات

النسبة المئوية هنا هي نسبة اللون، لو اللونين لهما نفس النسبة يتوقف التدرج

يمكن ضم أكثر من لون

أول لون نسبته تبدأ من `0%`وآخر لون نسبته تنتهي عند `100%`

يمكن تحدبد درجة الشفافية من خلال `transparent`

مثال:

```css
background-image: linear-gradient(185deg, red 0% 30%, blue 50% 60%, green 70% 80%, transparent);
```

لدمج ألوان الخلفية داخليا:

```css
background-image: radial-gradient(circle, yellow, blue, red);
```

القيم:

1. الأشكال:
   1. ellipse: بيضاوي (افتراضي)
      1. الأبعاد: قيمتين (لو متساويتين تشكل دائرة)
   2. circle: دائري
      1. الأبعاد: قيمة واحدة

### ملاحظــات

 يمكن تحديد موقع ثاني قيمة للشكل البيضاوي مثل:

 ```css
 background-image: radial-gradient(ellipse 200px 100px at top left, yellow, blue, red);
 ```

### خصائص الخلفية

- تكرار الخلفية:

```css
background-repeat: no-repeat;
background-repeat: repeat-x;
background-repeat: repeat-y;
```

القيم:

1. `background-repeat`:
   1. `repeat`: تكرار (افتراضيا)
   2. `no-repeat`: بدون تكرار
2. `background-repeat`:
   1. `repeat-x`: تكرار أفقي
   2. `repeat-y`: تكرار عمودي

- حجم الخلفية:

```css
background-size: cover;
background-size: 100%;
background-size: contain;
background-size: 100px 200px;
```

القيم:

1. `width` `height`
2. `cover`: تملأ كل أبعاد الخلفية على حساب كمال الصورة
3. `contain`: تحافظ على أبعاد الصورة

- موقع الخلفية:

```css
background-position: center;
background-position: center top;
background-position: top left;
background-position: 50% 50%;
background-position: 30px 10px;
```

- ثبات الخلفية أثناء التمرير:

```css
background-attachment: fixed;
background-attachment: scroll;
```

القيم:

`fixed`: متنقل مع التمرير
`scroll`: يتم تمريره (افتراضيا)

- بداية الخلفية:

```css
background-origin: border-box;
background-origin: padding-box;
background-origin: content-box;
```

1. `border-box`: (الافتراضي)
   1. تبدأ الخلفية من حافة الإطار (border)
   2. الخلفية تمتد تحت الإطار إذا كان شفافًا أو متقطعًا
2. `padding-box`:
   1. تبدأ الخلفية من حافة الحشو الداخلي (padding)
   2. لا تمتد الخلفية تحت الإطار
3. `content-box`:
   1. تبدأ الخلفية من حافة المحتوى
   2. لا تمتد تحت الحشو الداخلي أو الإطار

- نقطة اقتصاص الخلفية للعنصر:

```css
background-clip: border-box;
background-clip: padding-box;
background-clip: content-box;
```

القيم:

1. `border-box` (القيمة الافتراضية)
   1. الخلفية تمتد خلف الإطار (border)
   2. إذا كان الإطار شفافًا أو متقطعًا، ستبدو الخلفية تحته
2. `padding-box`
   1. الخلفية تقتصر على منطقة الحشو (padding) ولا تمتد تحت الإطار
   2. الإطار سيكون فوق الخلفية (إذا كان مرئيًا)
3. `content-box`
   1. الخلفية تقتصر على منطقة المحتوى فقط
   2. لا تظهر تحت الحشو (padding) ولا تحت الإطار
4. `text` (تجريبي، يحتاج prefix في بعض المتصفحات)
   1. الخلفية تقتصر على نص العنصر فقط
   2. يحتاج إلى -webkit-background-clip: text في بعض المتصفحات
   3. يجب أن يكون لون النص شفافًا (color: transparent) لرؤية التأثير

#### الفرق بين background-clip و background-origin

`background-clip`: يحدد أين تنتهي الخلفية (منطقة الاقتصاص)

`background-origin`: يحدد من أين تبدأ الخلفية (نقطة الأصل)

### اختصار الخلفية

يمكن دمج كل الخصائص في خاصية واحدة:

```css
background: red url("image.jpg") no-repeat center / cover padding-box fixed;
```

#### ملاحظات مهمة

لا يوجد قيم إجبارية يجب كتابتها

إذا استخدمت `background-size` يجب أن تأتي بعد `background-position` مفصولة بشرطة مائلة (`/`)

لا يوجد ترتيب إجباري، لكن هناك ترتيب موصى به:

1. `background-color`
2. `background-image`
3. `background-repeat`
4. `background-attachment`
5. `background-position` / `background-size`

تأتي `background-origin` بعد `background-size` لذا يمكن للمتصفح أن يفرق بين قيمتها وقيمة `background-clip`

القيم غير المحددة ستحصل على قيمها الافتراضية

يمكنك استخدام none لإلغاء أي خاصية

القيم الافتراضية إذا لم تحددها:

```css
.element {
  background: transparent none repeat scroll 0% 0%/auto padding-box padding-box;
}
```

التركيبة الخاصة بها:

```css
.element {
  background: [color] [image] [repeat] [attachment] [position] / [size] [origin] [clip];
}
```

يمكن معاينة الألوان بسهولة في أغلب المحررات بوجود معاين تلقائي، كما تدعم بعض المتصفحات اختيار الألوان مباشرة من أدوات المطور.

---

## أمثلة عملية

تلوين النص:

```css
h1 {
  color: #3498db;
}
```

خلفية صورة بحجم الغلاف:

```css
header {
  background: url("header.jpg") no-repeat center / cover;
}
```

خلفية ثابتة:

```css
body {
  background-attachment: fixed;
}
```

---

## الخطوط والنصوص

لإضفاء طابع جمالي على النصوص، تستخدم عدة خصائص:

- **font-style**: أسلوب الخط

```css
font-style: italic;
```

القيم:

`normal`: طبيعي (الافتراضي)

`italic`: مائل = `oblique` (أقل دعما) = `<i>` في html

- **font-variant**: نوع الخط

```css
font-variant: small-caps;
```

القيم:

`normal`: طبيعي (الافتراضي)

`small-caps`: حرف كبير بحجم صغير

- **font-weight**: سمك الخط

```css
strong {
  font-weight: bold;
}
.light {
  font-weight: 300;
}
```

القيم:

`bold`: غامق = `<b>`, `<strong>`, `<h1>` في html

`bolder`: أغمق من باقي النصوص

`lighter`: أفتح من باقي النصوص

`inherit`: وراثة السمك من الأب

`أرقام`: (100 إلى 900) (الافتراضي: 400)

`normal`: طبيعي بدون السمك المحدد أو الموروث من الأب (غير افتراضي في حالة تغيير السمك)

`initial`: يُعيد السمك إلى قيمته الافتراضية الأولية حسب المواصفات CSS (وهي normal في معظم العناصر مثل `<p>`، لكنها قد تكون bold في عناصر مثل `<th>` أو `<h1>` إلى `<h6>`).

يلغي أي تأثير للوراثة (Inheritance) ويعود إلى الإعداد الافتراضي للمتصفح.

الفرق بين `font-weight: normal` و `font-weight: initial` في CSS كالتالي:

1- **`font-weight: normal`**

- يعطي النص **سمكًا عاديًا** (عادةً ما يعادل `400` في القيم الرقمية).
- يتجاهل أي سمك موروث من العنصر الأب.  
- مثال:

```css
p {
  font-weight: normal; /* يجعل النص عاديًا بغض النظر عن الإعدادات الموروثة */
}
 ```

2- **`font-weight: initial`**

- يُعيد السمك إلى **قيمته الافتراضية الأولية** حسب المواصفات CSS (وهي `normal` في معظم العناصر مثل `<p>`، لكنها قد تكون `bold` في عناصر مثل `<th>` أو `<h1>` إلى `<h6>`).  
- يلغي أي تأثير للوراثة (Inheritance) ويعود إلى الإعداد الافتراضي للمتصفح.  
- مثال:

```css
p {
       font-weight: initial; /* يعيد السمك إلى القيمة الافتراضية للعنصر (عادةً normal) */
}
```

الفرق العملي:

- إذا كان العنصر الأب لديه `font-weight: bold`، فإن:  
  - `normal` سيتجاهل التوريث ويجعل النص عاديًا.  
  - `initial` سيعيده إلى القيمة الافتراضية (التي قد تكون `normal` أو `bold` حسب العنصر).  

مثال توضيحي:

```html
<style>
  body { font-weight: bold; } /* كل النصوص ستكون غامقة بالتوريث */
  p.normal { font-weight: normal; } /* يتجاهل التوريث ويصبح عاديًا */
  p.initial { font-weight: initial; } /* يعود إلى القيمة الافتراضية (normal هنا) */
  th.initial { font-weight: initial; } /* يعود إلى القيمة الافتراضية (bold في العنصر <th>) */
</style>

<body>
  <p>نص عادي (bold بالتوريث)</p>
  <p class="normal">نص بـ normal (يصبح عاديًا)</p>
  <p class="initial">نص بـ initial (يعود إلى normal)</p>
  <table>
    <tr>
      <th class="initial">عنوان الجدول بـ initial (يبقى bold)</th>
    </tr>
  </table>
</body>
```

---

متى نستخدم كل منهما؟

- استخدم `normal` عندما تريد **إجبار النص على أن يكون عاديًا** بغض النظر عن التوريث أو الإعدادات الأخرى.  
- استخدم `initial` عندما تريد **إعادة السمك إلى القيمة الافتراضية الأصلية** للعنصر (مثلاً لإلغاء تأثير التوريث).  

ملاحظة: في معظم الحالات، النتيجة ستكون متشابهة (`normal` = `initial`)، إلا في عناصر مثل العناوين (`<h1>`) أو `<th>` حيث قد يكون `initial` = `bold`.

---

`شــــــــرح أدق`

---

1- **لو كان العنصر له قيمة افتراضية مختلفة عن `normal`**

- بعض العناصر مثل `<th>` أو العناوين (`<h1>` إلى `<h6>`) لها قيمة `font-weight` الافتراضية `bold` (وليست `normal`).  
- هنا يظهر الفرق:
  - `normal` → **يُجبر** النص على أن يكون عاديًا (مهما كانت القيمة الافتراضية).  
  - `initial` → **يعود** إلى القيمة الافتراضية الأصلية للعنصر (مثلاً `bold` للعناوين).  

مثال:

```html
<h1 style="font-weight: normal">عنوان بـ normal (يصبح عاديًا)</h1>
<h1 style="font-weight: initial">عنوان بـ initial (يبقى غامقًا، لأنه القيمة الافتراضية)</h1>
```

- النتيجة:  
  - الأول: نص عادي (على الرغم أن `<h1>` غامق افتراضيًا).  
  - الثاني: نص غامق (لأن `initial` أعادته للقيمة الأصلية `bold`).

---

2- **لو كان هناك توريث (Inheritance) من العنصر الأب**

- لو كان العنصر الأب لديه `font-weight: bold`، فكل العناصر الفرعية ترث هذا السمك.  
- هنا:  
  - `normal` → يتجاهل التوريث ويجعل النص عاديًا.  
  - `initial` → يتجاهل التوريث **ويُعيد القيمة الافتراضية للعنصر نفسه** (ليست بالضرورة `normal`).  

مثـال:

```html
<div style="font-weight: bold;">
  <p style="font-weight: normal;">هذا النص سيكون عاديًا (تجاهل التوريث).</p>
  <p style="font-weight: initial;">هذا النص سيعود إلى القيمة الافتراضية لـ <p> (وهي normal).</p>
  <h1 style="font-weight: initial;">هذا النص سيعود إلى القيمة الافتراضية لـ <h1> (وهي bold).</h1>
</div>
```

---

الخلاصة:

| الحالة               | `font-weight: normal`               | `font-weight: initial`              |
|----------------------|-------------------------------------|--------------------------------------|
| عنصر عادي (`<p>`)    | يصبح عاديًا (400)                   | يصبح عاديًا (مثل القيمة الافتراضية) |
| عنصر غامق افتراضيًا (`<h1>`) | يُجبره على أن يصبح عاديًا           | يبقى غامقًا (القيمة الأصلية)        |
| مع توريث من الأب     | يتجاهل التوريث ويُجبر النص على `normal` | يتجاهل التوريث ويعود للقيمة الافتراضية للعنصر |

---

متى تستخدم كل منهما؟

- استخدم `normal` عندما تريد **إجبار** النص على أن يكون عاديًا بغض النظر عن أي شيء (توريث أو قيم افتراضية).  
- استخدم `initial` عندما تريد **إعادة الضبط** للقيمة الأصلية للعنصر (مثلاً لإلغاء توريث السمك من الأب).  

هل هناك فرق في العناصر العادية مثل `<p>`؟

- **لا**، لأن قيمتها الافتراضية أصلًا `normal`، لذا كلتا القاعدتين ستعطيان نفس النتيجة.  
- الفرق يظهر فقط في العناصر التي لها قيمة افتراضية مختلفة (مثل العناوين أو `<th>`).  

باختصار:

`normal`: قيمتها 400 كقيمة رقمية افتراضية

`initial`: القيمة الافتراضية للمتصفح نفسه (غالبا normal)

- **font-size**: حجم الخط

```css
h1 {
  font-size: 32px;
}
p {
  font-size: 16px;
}
```

القيم: `large`, `larger`, `medium`, `small`, `smaller`, `x-large`, `xx-large`, `x-small`, `xx-small`, `inherit`, `أرقام`

- **font-family**: تحديد الخط

```css
p {
  font-family: Arial, Helvetica, sans-serif;
}
```

يمكن كتابة عدة خطوط بالترتيب، لو لم يتوفر الأول ينتقل للثاني.

لمعرفة الخطوط المتوفرة بأغلب الأجهزة اضغط [هنا](https://www.w3schools.com/cssref/css_websafe_fonts.php)

لجعل الخط آمنا اضغط [هنا](https://fonts.google.com/?preview.layout=grid)

خطوات اختياره:

1. البحث عن اسم الخط
2. الضغط عليه ثم `Get font`ثم `Get embed code`
3. يوجد طريقتين لاستخدامه من خلال قسم Web
   1. طريقة `<link>`: نسخ كود html الخاص بالروابط ووضعه بقسم html head ونسخ اسم الخط وضعه بتنسيق css
   2. طريقة `import`: نسخ وسم `<style>` بمحتواه ووضعه في html head أو نسخ المحتوى نفسه ووضعه في css

### اختصار الخصائص الخمسة لسطر واحد

يجب أن يكون بهذا الترتيب:

`font-style`

`font-variant`

`font-weight`

`font-size`

`font-family`

```html
<h1>Welcome!</h1>
```

```css
h1 {
    font-style: italic;
    font-variant: small-caps;
    font-weight: bold;
    font-size:x-large;
    font-family:'Courier New', Courier, monospace;
    font: italic small-caps bold x-large 'Courier New', Courier, monospace;
  }
```

كل قيم `font` اختيارية ما عدا آخر قيمتين: `font-size`, `font-family`

ليست كل القيم صالحة لكل أنواع الحروف

- **line-height**: المسافة بين السطور

```css
p {
  line-height: 1.5;
}
```

يمكن كتابتها مع `font-size` (فقط مع قيم `font`):

```css
h1 {
    font: 30px/90px Arial, sans-serif;
  }
```

- **letter-spacing**: المسافة بين الكلمات

```css
h2 {
  word-spacing: 2px;
}
```

- **letter-spacing**: المسافة بين الحروف

```css
h2 {
  letter-spacing: 2px;
}
```

- **text-align**: محاذاة النص

```css
p {
  text-align: center;
}
```

القيم: left, right, center, justify.

- **text-decoration-line**: خط زخرفة النص

`underline`: خط تحت النص

`overline`: خط فوق النص

`line-through`: خط وسط الكلمة

`none`: إزالة الخط (مثل الموجود عند `<a>`)

يمكن تحديد الثلاثة معًا:

```css
text-decoration-line: underline overline line-through;
```

يمكن تحديد لون الخط:

```css
text-decoration-color: red;
```

يمكن تحديد شكل الخط:

```css
text-decoration-style: wavy;
```

يمكن اختصار الثلاثة:

```css
text-decoration: solid black underline
```

الترتيب غير إجباري

- **text-shadow**: ظل النص

  - يأخذ أربع قيم:
    - `H-shadow`: ظل أفقي
      - قيمة موجبة: يمين
      - قيمة سالبة: يسار
    - `V-shadow`: ظل عمودي
      - قيمة موجبة: أسفل
      - قيمة سالبة: أعلى
    - `Blur`: الضبابية
    - `color`: اللون

يمكن إضافة أكثر من ظل

```css
text-shadow:
-50px -60px 1px red,
20px 40px 2px blue;
```

- **box-shadow**: ظل الصندوق

  - يأخذ ست قيم:
    - `H-shadow`: ظل أفقي
      - قيمة موجبة: يمين
      - قيمة سالبة: يسار
    - `V-shadow`: ظل عمودي
      - قيمة موجبة: أسفل
      - قيمة سالبة: أعلى
    - `Blur`: الضبابية
    - `spread`: الانتشار
    - `color`: اللون
    - `inset`: الإدراج (الانتشار داخل الصندوق)

يمكن إضافة أكثر من ظل

```css
div {
  width: 200px;
  height: 200px;
  background: #eee;
  box-shadow: inset 5px 5px 10px 10px rgba(0,0,0,0.5),
  10px 10px 10px 10px blue;
}
```

- **direction**: اتجاه النص

```css
body {
  direction: rtl;
}
```

مثالية لدعم اللغات من اليمين لليسار.

- **text-transform**: صفة الخط

```css
text-transform: uppercase; /* حروف كبيرة */
text-transform: lowercase; /* حروف صغيرة */
text-transform: capitalize; /* أول حرف من كل كلمة كبير دون تغيير باقي الحروف */

```

---

## الصندوق (Box Model)

كل عنصر في HTML يعتبر "صندوقًا" في CSS. الصندوق يتكون من:

- **Content**: المحتوى نفسه (نص، صورة...)
- **Padding**: المسافة بين المحتوى والحدود الداخلية
- **Border**: حدود العنصر
- **Margin**: المسافة خارج العنصر

مثال:

```css
.box {
  width: 200px;
  padding: 20px;
  border: 2px solid black;
  margin: 10px;
}
```

---

### padding

إزاحة داخلية:

```css
padding: 10px;
padding: 10px 20px;
padding: 10px 15px 20px 25px;
```

الترتيب: top, right, bottom, left.

---

### margin

إزاحة خارجية:

```css
margin: 10px;
margin: 10px 20px;
```

يمكن أن تكون سالبة.

---

### border

إطار يحيط بالصندوق:

```css
border-width: 2px;
border-style: solid;
border-color: blue;
```

أو اختصارًا:

```css
border: 2px solid blue;
```

---

### box-sizing

افتراضيًا، width/height لا يشمل padding وborder. لجعلها داخلهما:

```css
box-sizing: border-box;
```

---

✅ هذه القاعدة تجعل التصميم أسهل وتقلل من أخطاء القياسات.

---

## العناصر Block وInline

عناصر HTML تنقسم إلى نوعين رئيسيين:

- **Block**: تأخذ عرض السطر كاملًا (100% من عرض الأب) وتبدأ في سطر جديد حتى لو كان العنصر الذي يسبقه `inline`.
  - أمثلة: div, p, h1-h6, section
  - يمكن تحديد عرض وطول، خلفية تغطي كل السطر وينشيء سطر جديد حتى لو العرض ليس 100% من الأب.

- **Inline**: تأخذ عرض محتواه فقط وتبقى في نفس السطر مع العناصر المجاورة (إلا لو كان عرض المحتوى أكبر من الأب ينتقل لسطر جديد).
  - أمثلة: span, a, strong, em
  - لا يمكن تحديد عرض وطول، الخلفية تغطي المحتوى فقط.
  - الأبعاد الممكن تحديدها:
    - `border`
    - `padding`:
      - يأخذ مساحة للعرض فيزيح العناصر المجاورة
      - لا يأخذ مساحة للطول فلا يزيح عناصر الأسطر المحيطة
    - `margin`:
      - يأخذ مساحة للعرض فيزيح العناصر المجاورة
      - لا يمكن تحديد قيمة الطول (`top`, `bottom`)
  - عناصر `inline` تنقسم لقسمين:
    - عناصر نصية لا يمكن تحديد أبعادها
    - عناصر مرئية تعامل على أنها `inline-block` مثل:
      - `img`
      - `iframe`
      - `canvas`
      - `video`: له أبعاد افتراضية
      - `audio`: لو كان له واجهة مرئية
      - `object`
      - عناصر متصفحيا `inline-block`
        - `input`
        - `textarea`
        - `select`
        - `button`

- يمكن معرفة نوع العنصر من خلال `background-color` أو `Inspect`

---

### التحكم في النوع

يمكنك تغيير نوع العنصر:

```css
span {
  display: block;
}

div {
  display: inline;
}

img {
  display: inline-block;
}
```

- **inline-block**: يجمع خصائص inline وblock معًا (يسمح بتحديد العرض والطول ويبقى في السطر).

- **contents**: يزيل صندوق العنصر (box) ويجعل أطفاله جزءًا من تدفق الأب. مفيد في التنسيق المتقدم (مثل `grid`/`flex`).

- **none**: يخفي العنصر تمامًا ويزيله من التخطيط ويهمل مكانه.

```css
.hidden {
  display: none;
}
```

- ماذا تقبل `inline-block` من خواص العناصر `block`؟
  - تقبل:
    - الأبعاد: `width`, `height`
    - المسافات: `padding`, `margin`, `border`
    - تنسيقات الخلفية والظلّ والتدرجات مثل `background`, `box-shadow`, `outline`
    - `vertical-align` (ميزة إضافية عن block!)
    - `text-align` يعمل داخليًا
  - لا تقبل:
    - الامتداد التلقائي لكامل عرض الأب (`width: auto` في `inline-block` لا يعني 100%)
    - كسر السطر تلقائيًا (unless تستخدم `br` أو `flex-wrap`)
    - لا تُوسَّط تلقائيًا بـ `margin: auto` إلا إن وضعتها داخل `block` محدد العرض

---

### visibility

- يتحكم في الظهور مع بقاء المساحة.

```css
.visible {
  visibility: visible; /* Default */
}

.invisible {
  visibility: hidden;
}
```

- `visibility: visible`: ظهور (افتراضي)
- `visibility: hidden`: اخفاء
- `opacity: 0`: يخفي العنصر مع بقاءه مؤثرًا في التخطيط (يحتفظ بالمساحة ويبقى قابلًا للنقر إذا لم تُعطِ `pointer-events: none`)، يمكن مراجعة التنسيق من [هنا](#opacity)
  - الفرق الرئيسي هو أن `opacity` يمكن استخدامه لتحويلات الحركة (animations) بسلاسة، بينما `visibility` لا يدعم التدرج.
- `display: none`: حذف

---

## خاصية overflow

عند صغر حجم العنصر مقارنة بمحتواه:

```css
overflow: visible; /* الافتراضي */
overflow: hidden;
overflow: scroll;
overflow: auto;
```

- **hidden**: يخفي المحتوى الزائد.
- **scroll**: دائما يظهر شريط التمرير.
- **auto**: يظهر شريط التمرير عند الحاجة.

يمكن تحديد محور معين:

```css
overflow-x: scroll;
overflow-y: hidden;
---

## الموقع والإزاحة

---

## Position

خاصية position تتحكم في مكان العنصر في الصفحة:

- **static** (افتراضي): موقع طبيعي في التدفق.
- **relative**:
  - يسمح بتحريك العنصر من مكانه الأصلي
  - يحافظ على حجز مكانه

```css
.relative {
  position: relative;
  top: 10px;
  left: 20px;
}
```

- **absolute**:
  - يخرج من التدفق العادي ويتموضع نسبة لأقرب أب به خاصية `position` إلا لو القيمة `static`
  - يهمل حجز مكانه
  - يخرج من أبعاد الأب ويحدد المحتوى أبعاده (ما لم يحدد له أبعاد)

يملك position غير static.

```css
.absolute {
  position: absolute;
  bottom: 0;
  right: 0;
}
```

- **fixed**: ثابت في مكانه بالنسبة للنافذة حتى مع التمرير.

```css
.fixed {
  position: fixed;
  top: 0;
}
```

- **sticky**: مزيج من relative وfixed.

```css
.sticky {
  position: sticky;
  top: 0;
}
```

يبقى في مكانه عند التمرير حتى حد معين. (ينتهي عند أقصى حد للأب)

---

## z-index

تتحكم بمكان الطبقات (القيمة الأعلى تأخذ الطبقة الأعلى)

```css
.test1 {
  z-index: 1
}
```

```css
.test2 {
  z-index: 2
}
```

```css
.test3 {
  z-index: 3
}
```

```css
.test4 {
  z-index: -1
}
```

أعلى طبقة هي `.test3`

أسفل طبقة هي `.test4` (أسفل من الأب: لن تظهر لو للأب لون خلفية)

---

## Float

لجعل العناصر بمحاذاة اليسار أو اليمين داخل حاوية:

```css
.left {
  float: left;
}

.right {
  float: right;
}
```

- القيمة الافتراضية: `none`
- يسمح بوضع عناصر بجانب بعضها.
- يخرجها من التدفق العادي مما قد يجعل الخلفية أو الحدود لا تحتويها (يعني لو العنصر داخل حاوية مثل `div` يقوم بالخروج منها) مثال:

```html
<div class="green">
    <div class="red float"></div>
    <div class="blue float"></div>
    <div class="yellow float"></div>
</div>
```

```css
.green {
    background: green;
}
.red {
    height: 50px;
    width: 100px;
    background: red;
}
.blue {
    height: 50px;
    width: 100px;
    background: blue;
}
.yellow {
    height: 50px;
    width: 100px;
    background: yellow;
}
.float {
    float: right;
}
```

لحل مشكلة "الخروج" من الحاوية:

```html
<div class="green">
  ...
</div>
<div class="clearfix"></div>
```

```css
.clearfix{
  clear: both;
}
```

- `clear`:
  - `right`: -> `float: right;`
  - `left`: -> `float: left;`
  - `both`: الاثنين

---

### ملاحظـــات

- هذه الطريقة لا تحل مشكلة انهيار العنصر الأب:
  - يعمل فقط على منع العناصر الطافية من التأثير على العناصر التالية
  - لا يجبر العنصر الأب على احتواء العناصر الطافية داخله
- يحتاج إلى عنصر إضافي في HTML

- بعد استخدام float، يجب عادةً "تصفية" التدفق بـ clear.

### حل مشكلة انهيار العنصر الأب دون تعديل HTML بإضافة محتوى وهمي

```html
<div class="green clearfix">
  ...
</div>
```

```css
.clearfix::after {
    content: "";
    display: table;
    clear: both;
}
```

- `::after`: هو عنصر زائف (pseudo-element) يُنشئ عنصرًا افتراضيًا بعد محتوى العنصر المحدد.
- `content`: "": ينشئ محتوى فارغًا لهذا العنصر الافتراضي.
- `display: table (أو block)`: يجعل العنصر الافتراضي يأخذ مساحة كاملة.
- `clear: both`: يمنع هذا العنصر من أن يتأثر بالعناصر الطافية من أي جهة (يمين أو يسار).

---

## القوائم (List Styles)

لعناصر القوائم مثل ul وol يمكنك التحكم في شكل النقاط أو الأرقام:

```css
ul {
  list-style-type: disc; /* الافتراضي */
}

ol {
  list-style-type: decimal;
}
```

أنواع أخرى:

- circle
- square
- none (لإزالة النقاط)
  
---

### موقع النقطة

```css
ul {
  list-style-position: inside;
}
```

- **outside** (افتراضي): النقاط خارج المحتوى.
- **inside**: النقاط داخل المساحة المخصصة للنص.

---

### صورة بدلاً من النقاط

```css
ul {
  list-style-image: url("bullet.png");
}
```

يفضل أن تكون صغيرة الحجم.

---

### اختصار

```css
ul {
  list-style: square inside;
}
```

يمكن دمج النوع والموقع والصورة.

---

## Table style

يمكن عمل تنسيقات للجداول مثلا:

```html
<table>
  <caption>جدول توضيحي</caption>
  <thead>
      <tr>
          <th>الاسم</th>
          <th>العمر</th>
          <th>المدينة</th>
      </tr>
  </thead>
  <tbody>
      <tr>
          <td>أحمد</td>
          <td>25</td>
          <td>القاهرة</td>
      </tr>
      <tr>
          <td>محمد</td>
          <td>30</td>
          <td>الرياض</td>
      </tr>
      <tr>
          <td>فاطمة</td>
          <td>22</td>
          <td>دبي</td>
      </tr>
  </tbody>
</table>
```

```css
table {
    width: 80%;
    margin: 20px auto;
    border-collapse: collapse;
    font-family: Arial, sans-serif;
    box-shadow: 0 0 20px rgba(0,0,0,0.1);
}

th, td {
    padding: 12px 15px;
    text-align: left;
    border-bottom: 1px solid #ddd;
}

th {
    background-color: #4CAF50;
    color: white;
    text-transform: : uppercase;
    font-size: 14px;
}

tr:nth-child(even) {
    background-color: #f2f2f2;
}

tr:hover {
    background-color: #ddd;
}

caption {
    font-size: 1.5em;
    margin-bottom: 10px;
    font-weight: bold;
}
```

تنسيق الجدول الرئيسي (table):

- `background-color`: لون خلفية الجدول
- `border`: حد الجدول
- `width`: عرض الجدول (100% لعرض كامل)
- `border-spacing`: المسافة بين الخلايا
- `border-collapse`: (`collapse` | `separate`) - يتحكم في دمج حدود الخلايا
  - `collapse`: يدمج الحدود بين الخلايا
  - `separate`: يفصل الحدود (الافتراضي)

تنسيق عناوين الجدول (th):

- `background-color`: لون خلفية العناوين
- `color`: لون النص
- `height`: ارتفاع الخلية
- `font-weight`: سمك الخط (غالبًا bold للعناوين)
- `text-align`: محاذاة النص (left, center, right)
- `padding`: المساحة الداخلية حول النص

تنسيق خلايا البيانات (td):

- `text-align`: محاذاة النص أفقياً
- `height`: ارتفاع الخلية
- `vertical-align`: محاذاة النص عمودياً
  - `top`: أعلى الخلية
  - `middle`: منتصف الخلية (الافتراضي)
  - `bottom`: أسفل الخلية

تنسيق الصفوف (tr):

```css
tr {
  background-color: #f2f2f2; /* لون خلفية الصف */
}

tr:nth-child(even) {
  background-color: #ddd; /* تلوين متبادل للصفوف */
}

tr:hover {
  background-color: #ccc; /* تأثير عند المرور */
}
```

تنسيق القوائم داخل الجدول:

```css
ul, ol {
  background-color: blueviolet;
  list-style-type: armenian;
  list-style-position: inside;
}

li {
  background-color: blanchedalmond;
}
```

تنسيق حدود متقدم:

```css
table {
  border-collapse: collapse;
}

th, td {
  border: 1px solid #ddd;
  padding: 8px;
}
```

تأثيرات مرئية:

```css
td {
  transition: background-color 0.3s;
}

td:hover {
  background-color: #f5f5f5;
}
```

نصائح مهمة لتنسيق الجداول:

- استخدم `border-collapse: collapse` للحصول على حدود أنظف
- استخدم `padding` لخلق مساحة داخل الخلايا
- استخدم `text-align` و `vertical-align` لمحاذاة المحتوى
- استخدم ألوان خلفية مختلفة للعناوين والبيانات
- جرب `:hover` لإضافة تفاعل مع المستخدم
- استخدم `nth-child` للتلوين المتناوب للصفوف

## التأثيرات البصرية (Hover, Focus, Checked)

### Hover

تطبيق تنسيق عند مرور المؤشر:

```css
a:hover {
  color: red;
  text-decoration: none;
  cursor: pointer; /* شكل المؤشر */
}
```

---

### Active

تطبيق تنسيق عند الضغط

```css
div:active {
  background: green
}
```

---

### Empty

تطبيق التنسيق على  أبناء ليس لها محتوى

```html
<div><p></p></div>
```

```css
p:empty {
  background: green
}
```

---

### Visited

تطبيق تنسيق على الروابط التي تمت زيارتها:

```css
a:visited {
  color: purple;
}
```

يجب أن يكون الرابط صالح

---

### Link

تطبيق تنسيق على الروابط التي لم تتم زيارتها:

```css
a:link {
  color: red;
}
```

---

### Focus

تطبيق تنسيق عند تركيز المستخدم على عنصر (مثل input):

```css
input:focus {
  outline: 2px solid red;
  border: 2px solid blue;
}
```

- `outline`: حدود الملربع
  - none
  - 2px solid red
- `outline-offset`: أزاحة الحدود

---

### Disabled

تطبيق تنسيق في حالة `disabled`:

```html
<input disabled/>
```

```css
input:disabled {
  background: blue;
}
```

يمكنك تطبيق تنسيقات على عنصر `<input>` في جميع حالاته باستخدام `pseudo-classes` المخصصة لكل حالة.

إليك التفاصيل:

---

### حالات `<input>` المدعومة في CSS

يمكنك تنسيق `<input>` في الحالات التالية (وأكثر):

- الحالات الأساسية:

| Pseudo-Class       | الوصف                                  | مثال CSS                     |
|--------------------|---------------------------------------|-----------------------------|
| `:enabled`         | عندما يكون `input` نشطًا (غير معطل). | `input:enabled { ... }`     |
| `:disabled`        | عندما يكون `input` معطلًا.           | `input:disabled { ... }`    |
| `:read-only`       | عندما يكون `input` للقراءة فقط.      | `input:read-only { ... }`   |
| `:read-write`      | عندما يكون `input` قابلًا للكتابة.   | `input:read-write { ... }`  |

- حالات التركيز (Focus) والتحديد:
| Pseudo-Class       | الوصف                                  | مثال CSS                     |
|--------------------|---------------------------------------|-----------------------------|
| `:focus`           | عند التركيز على `input`.             | `input:focus { ... }`       |
| `:checked`         | عند تحديد `radio` أو `checkbox`.     | `input:checked { ... }`     |
| `:indeterminate`   | عندما يكون `checkbox` غير محدد.      | `input:indeterminate { ... }` |

- حالات الصحة (Validation):

| Pseudo-Class       | الوصف                                  | مثال CSS                     |
|--------------------|---------------------------------------|-----------------------------|
| `:valid`           | عندما تكون القيمة صالحة.             | `input:valid { ... }`       |
| `:invalid`         | عندما تكون القيمة غير صالحة.         | `input:invalid { ... }`     |
| `:required`        | عندما يكون `input` مطلوبًا.          | `input:required { ... }`    |
| `:optional`        | عندما يكون `input` اختياريًا.        | `input:optional { ... }`    |

- حالات خاصة:

| Pseudo-Class       | الوصف                                  | مثال CSS                     |
|--------------------|---------------------------------------|-----------------------------|
| `:placeholder-shown` | عند عرض النص البديل (placeholder).  | `input:placeholder-shown { ... }` |
| `:out-of-range`    | عندما تكون القيمة خارج النطاق.       | `input:out-of-range { ... }` |
| `:in-range`        | عندما تكون القيمة ضمن النطاق.        | `input:in-range { ... }`    |

---

- مثال شامل لتنسيق `<input>` في حالات مختلفة:

```html
<!DOCTYPE html>
<html>
<head>
    <style>
        /* الحالة الأساسية */
        input {
            padding: 10px;
            margin: 5px;
        }

        /* عند التركيز */
        input:focus {
            border: 2px solid blue;
            background-color: #f0f8ff;
        }

        /* عند التعطيل */
        input:disabled {
            background-color: #eee;
            cursor: not-allowed;
        }

        /* عند التحديد (لـ checkbox/radio) */
        input:checked {
            width: 20px;
            height: 20px;
        }

        /* عندما تكون القيمة غير صالحة */
        input:invalid {
            border: 2px solid red;
        }

        /* عند عرض النص البديل */
        input:placeholder-shown {
            font-style: italic;
        }
    </style>
</head>
<body>
    <input type="text" placeholder="اكتب شيئًا...">
    <input type="text" disabled value="معطل">
    <input type="checkbox" id="check">
    <label for="check">موافق</label>
    <input type="email" required placeholder="البريد الإلكتروني">
</body>
</html>
```

---

هل يمكن تطبيق تنسيق في أي حالة؟

- نعم! يمكنك تنسيق `<input>` في أي حالة من الحالات المذكورة أعلاه.  
- بعض الحالات تتطلب نوعًا محددًا من `<input>`، مثل:
  - `:checked` → يعمل فقط مع `radio` أو `checkbox`.
  - `:in-range` → يعمل مع `number`, `date`, etc.

---

### ملاحظات مهمـة

1. المتصفحات القديمة (مثل IE) قد لا تدعم بعض الحالات مثل `:placeholder-shown`.  
2. الحالات الديناميكية (مثل `:valid`/`:invalid`) تتغير تلقائيًا بناءً على قيمة `input`.  
3. يمكنك دمج الحالات باستخدام CSS:

```css
input:enabled:focus {
    /* تنسيق عند التركيز على input نشط */
}
```

---

### المراجع المفيدة

- [MDN: Pseudo-classes](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)  
- [w3schools: Input Pseudo-classes](https://www.w3schools.com/css/css_pseudo_classes.asp)

---

### Checked

تنسيق عند تحديد عناصر مثل checkbox:

```css
input:checked {
  background-color: green;
}
```

---

### Opacity

للتحكم في شفافية العناصر:

```css
.transparent {
  opacity: 0.5;
}
```

القيمة بين 0 (شفاف تمامًا) و1 (غير شفاف).

---

## الأمثلة العملية

رابط بتأثير عند المرور:

```css
a {
  color: blue;
  text-decoration: underline;
}
a:hover {
  color: darkblue;
  text-decoration: none;
}
```

عنصر إدخال يبرز عند الضغط:

```css
input:focus {
  border-color: green;
}
```

Checkbox يتغير عند تحديده:

```css
input:checked {
  outline: 2px solid red;
}
```

---

### الفرق بين النقطتين `:` والأقواس المربعة `[]`

- النقطتان `:` (Pseudo-class) → تختار حالات/ظروف العنصر
- ما تفعله:
  تختار العنصر بناءً على حالته الديناميكية أو وظيفته (مثل التفعيل، التركيز، الزيارة).  
- خصائصها:  
  - تعتمد على تفاعل المستخدم أو حالة المتصفح (مثل `:hover` عند تمرير المؤشر).  
  - بعضها يتغير تلقائيًا (مثل `:valid` عند إدخال بيانات صحيحة).  
- أمثلة شائعة:  

  ```css
  a:hover      /* عند تمرير المؤشر */
  input:focus  /* عند النقر على حقل إدخال */
  li:first-child /* أول عنصر في قائمة */
  ```

---

- الأقواس المربعة `[]` (Attribute Selector) → تختار سمات/خصائص العنصر
- ما تفعله:  
  تختار العنصر بناءً على سماته (attributes) الثابتة في HTML (مثل `type`، `class`، `id`).  
- خصائصها:  
  - تعتمد على القيم المكتوبة في الكود (لا تتغير مع التفاعل).  
  - يمكن استخدامها مع أي سمة (حتى المخصصة مثل `data-*`).  
- أمثلة شائعة:

```css
input[type="text"]  /* جميع حقول النصوص */
a[target="_blank"]  /* جميع الروابط التي تفتح في نافذة جديدة */
[data-color="red"]  /* العناصر ذات السمة data-color="red" */
```

---

- مقارنة عملية بين `:` و `[]`:

| الميزة                  | النقطتان `:` (Pseudo-class) | الأقواس `[]` (Attribute Selector) |
|-------------------------|----------------------------|-----------------------------------|
| **التحديد**             | الحالات الديناميكية        | السمات الثابتة                   |
| **مثال**               | `button:disabled`          | `button[disabled]`               |
| **هل يتغير أثناء التشغيل؟** | نعم (مثل `:hover`)         | لا (ثابت除非 تعديل الـ HTML)     |
| **يدعم التخصيص؟**       | محدود (لديه قائمة معينة)  | نعم (أي سمة في HTML)             |

---

متى تستخدم كلًا منهما؟

- استخدم `:` عندما تريد:
  - تنسيق عنصر عند التفاعل معه (مثل تغيير لون الزر عند الضغط).  
  - التحديد بناءً على ترتيب أو علاقة العناصر (مثل `:nth-child(2)`).  

- استخدم `[]` عندما تريد:  
  - تنسيق عناصر **لها سمة محددة** (مثل كل حقول كلمات المرور `[type="password"]`).  
  - التحديد بناءً على **قيمة مخصصة** (مثل `[lang="ar"]` للنصوص العربية).  

---

- مثال يوضح الفرق بوضوح:

```html
<style>
  /* باستخدام : (حالة) */
  input:focus {
    border: 2px solid blue; /* عندما ينقر المستخدم على الحقل */
  }

  /* باستخدام [] (سمة) */
  input[required] {
    background: lightyellow; /* جميع الحقول المطلوبة */
  }
</style>

<input type="text" required placeholder="حقل مطلوب">
<input type="email" placeholder="حقل عادي">
```

---

- تحذير مهم:
  - يمكنك دمج الاثنين لتحقيق تنسيق دقيق جدًا:

```css
input[type="text"]:hover {
  /* يؤثر فقط على حقول النصوص عند تمرير المؤشر! */
  background: lightgreen;
}
```

---

الخلاصة:

- `:` → للتفاعلات والحالات (مثل `:hover`, `:checked`).
- `[]` → للسمات الثابتة (مثل `[type]`, `[href]`).

---

## العناصر الزائفة (Pseudo-elements)

العناصر الزائفة تسمح بتحديد أجزاء من المحتوى لتطبيق تنسيق خاص

نضع `::` بدلا من `:` للتفريق بينها وبين `Pseudo-Class`

### ::first-letter

لتنسيق أول حرف:

```css
p::first-letter {
  font-size: 2em;
  color: red;
}
```

---

### ::first-line

لتنسيق أول سطر:

```css
p::first-line {
  font-weight: bold;
}
```

---

### ::selection

لتنسيق النص المحدد بالمؤشر:

```css
::selection {
  background: yellow;
  color: black;
}
```

يمكن تطبيقها على عنصر معين مثلا:

```css
p::selection {
  background: yellow;
}

---

### ::before و::after

لإضافة محتوى قبل أو بعد العنصر:

```css
h2::before {
  content: "★ ";
  color: gold;
}

h2::after {
  content: " ✔";
  color: green;
}
```

- `conten`: يجب كتابتها حتى لو بدون محتوى
- يمكن استخدامها لإنشاء أشكال مثل الخطوط داخل الحاويات:

```css
.card {
  position: relative;
  padding-left: 10px;
}
.card::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 5px;
  height: 100%;
  background: blue;
}
```

- لو المحتوى فارغ فيجب تحديد أبعاده ومكانه
- `.card`: نستخدم معها `relative` حتى يتمكن العنصلر الزائف من وراثتها
- لا نضع `position: relative` مباشرة على `::before` لأن:
  - `::before` هو عنصر زائف (pseudo-element) ليس له وجود مستقل في DOM - إنه مجرد وهمي مرتبط بالعنصر الأصلي (.card في هذه الحالة).
  - `position: relative` تحتاج إلى عنصر حقيقي في شجرة المستند لتؤثر عليه، بينما `::before`:
    - لا يمكن أن يكون "أبًا" لعناصر أخرى
    - لا يمكن أن يكون مرجعًا لعناصر أخرى
    - وجوده مشروط بالعنصر الأصلي

---

## تخطيط الصفحة (Flexbox, Grid)

### Flexbox

طريقة حديثة لتنظيم العناصر في اتجاه واحد (صف أو عمود):

```css
.father {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
```

يمكن معرفة كل شيء عن من [هنا](https://nouvil.net/flex-box-game/)

#### عناصر الأب

خصائص رئيسية:

- **`display`**:
  - `flex`: عناصر أفقية وعرض الخلفية `100%` من عرض الأب
  - `inline-flex`: عناصر أفقية وعرض الخلفية `100%` من عرض المحتوى

- **`flex-direction`**: اتجاه
  - `row`: صف (افتراضي: اتجاه قيمة `dir`: ltr (افتراضي)، rtl)
  - `row-reverse`: عرض معكوس
  - `column`: عمود
  - `column-reverse`: عمود معكوس

- **`flex-wrap`**: التفاف رأسي (في حالة `flex-direction: row`)
  - `nowrap`: لا التفاف (افتراضي)
  - `wrap`: التفاف للأسفل إن تجاوز المحتوى عرض الأب
  - `wrap-reverse`: التفاف للأعلى إن تجاوز المحتوى عرض الأب

- **`flex-flow`**: تجمع خاصية `flex-direction` وخاصية `flex-wrap`
  - `flex-flow: row nowrap`

- **`justify-content`**: توزيع العناصر
  - `flex-start`: بداية الاتجاه (افتراضي)
  - `flex-end`: نهاية الاتجاه
  - كلاهما يختلف تأثيرهما حسب قيمة `flex-direction`
    - `row`: حسب قيمة `dir`:
      - `ltr` (افتراضي):
        - `flex-start`: يسار
        - `flex-end`: يمين
      - `rtl`:
        - `flex-start`: يمين
        - `flex-end`: يسار
    - `column`:
      - `flex-start`: أعلى
      - `flex-end`: أسفل
  - `left`, `right`: `flex-direction: row`
  - `center`: `flex-direction: row`, `flex-direction: column`
  - `space-between`: مسافات بين العناصر (لا يشمل الأطراف)
  - `space-around`: مسافات حول كل عنصر(يشمل الأطراف)
  - `space-evenly`: مسافات مشتركة حول العناصر (يشمل الأطراف)

- **`gap`**: مسافة بين العناصر
  - `gap: 200px`
  - تختلف قيمتها حسب `flex-direction`:
    - `row`: مسافة طولية
    - `column`: مسافة عرضية

- **`align-items`, `align-content`**: محاذاة (عكس `justify-content`)
  - `stretch`: تمدد (افتراضي)
    - تختلف تأثيرها حسب قيمة `flex-direction`:
      - `row`: تمدد طولي مساوي للأب
      - `column`: تمدد عرضي مساوي للأب
        - حسب قيمة `dir`
          - `rtl`: من اليمين
          - `ltr`: من اليسار
  - `flex-start`, `flex-end`:
    - كلاهما يختلف تأثيرهما حسب قيمة `flex-direction`:
      - `row`: `flex-start`: أعلى، `flex-end`: أسفل
      - `column`: `flex-start`: يسار ، `flex-end`: يمين
    - ملحوظة: `flex-wrap: wrap-reverse` تقوم بعكس اتجاهات  `flex-start`, `flex-end`مع `column`, `row`
  - `center`: `flex-direction: row`, `flex-direction: column`

##### الفرق بين `align-items`, `align-content`

- `align-content`:
  - تعمل فقط بحالة الالتفاف: `wrap, wrap-reserve`
  - لا تحدث مسافات بينها وبين العناصر الملتفة
  - إضافة `space-between`, `space-align`: تأثيرها يكون بينها وبين العناصر الملتفة

#### عناصر الابن

الخصائص:

- **`align-self`**: محاذاة
  - مثل `align-items` في الأب

- **`order`**: ترتيب
  - `0`: افتراضي
  - القيم المتساوية ترتيبها افتراضي
  - كلما زادت القيمة ابتعد العنصر
  - كلما قلت القيمة (حتى تحت الصفر) سبق العنصر

- **`flex-grow`**: تمدد
  - تتوسع للمساحة المتبقية من أبعاد الأب
  - `0`: افتراضي
  - أكبر قيمة يأخذ أكبر مساحة مثلا:
    - المساحة المتبقية -> `160px`
    - `item1`:
      - `flex-grow: 1` -> `20px`
    - `item2`:
      - `flex-grow: 2` -> `40px`
    - `item3`:
      - `flex-grow: 2` -> `40px`
    - `item4`:
      - `flex-grow: 3` -> `60px`
  - القيم السالبة غير صالحة

- **`flex-shrink`**: انكماش
  - `1`: افتراضي
  - `0`: تعطيل
  - كلما زادت القيمة كانت لعنصره الأولوية للانكماش
  - القيم السالبة غير صالحة

- **`flex-basis`**: التحكم بالأبعاد
  - حسب قيمة `flex-direction`:
    - `row`: `width`
    - `column`: `height`

- **`flex`**: اختصار الثلاث قيم:
  - `flex-grow`, `flex-shrink`, `flex-basis`:
    - `flex: 0 1 100px`

---

### Grid

شبكة ثنائية الأبعاد:

```css
.grid-container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 10px;
}
```

#### عنـاصر الأب

خصائص:

- **`display`**:
  - `grid`: تفعيل

- **`grid-template-columns` / `rows`**: تقسيم الشبكة (لا يتجاوز عدد الأبناء).
  - `fr`: تقسيم بالتساوي
  - يمكن استخدام أي وحدة قياس مثل (`%` `px` `auto`...) كما يمكن دمجها

الفرق بين `fr`, `auto`

| المعيار | `fr` | `auto` |
|---------|------|--------|
| **التوزيع** | حسب النسبة المحددة | حسب المحتوى أو المساحة |
| **المرونة** | أكثر مرونة في التوزيع | أقل مرونة |
| **حجم المحتوى** | يتجاهل حجم المحتوى | يحترم حجم المحتوى |
| **أفضل استخدام** | توزيع المساحات | العناصر ذات المحتوى المتغير |

- **`gap`**: المسافة بين العناصر.





`hhh`

``hhh``

```hhh```

````hhh````












---

✅ Flexbox مثالي لترتيب العناصر في صف أو عمود.
✅ Grid أفضل للتقسيمات المعقدة.

---

## الاستجابة للشاشات (Media Queries)

تسمح لك بتغيير التصميم حسب حجم الشاشة:

```css
@media screen and (max-width: 600px) {
  .container {
    flex-direction: column;
    width: 100%;
  }
}
```

✅ يمكن تحديد حد أدنى وأقصى:

```css
@media screen and (min-width: 400px) and (max-width: 800px) {
  .box {
    width: 80%;
  }
}
```

---

✅ ملاحظة:

- **min-width** يجب أن تكون أولاً.
- Media Queries مهمة لجعل المواقع متجاوبة على الهواتف والأجهزة اللوحية.

---

## مفاهيم متقدمة

### التغليف (Wrapping)

لا يمكن للمحتوى الانتقال لسطر جديد إن كان كلمة واحدة (بدون مسافات)

```html
<div>
    WOW!!!!!!!!!!!!!!
</div>
```

```css
div {
    width: 50px;
    background-color: red;
}
```

النص سيتجاوز العرض

#### التحكم في التغليف

```css
white-space: normal

```

الخصائص والقيم:

- white-space:
  - normal: الوضع الطبيعي (الوضع الافتراضي)
  - nowrap: عدم الالتزام بالأبعاد (كحالة الكلمة الواحدة)
  - pre: الالتزام بالمسافات والأسطر الفارغة كما هي (بدون الالتزام بالأبعاد)
  - pre-wrap:
    - الالتزام بالمسافات والأسطر الفارغة كما هي (مع الالتزام بالعرض)
    - لا يمنع النص من تجاوز الارتفاع المحدد للعنصر.
    - يمكن قص النص الزائد من خلال خاصية `overflow: hidden`
  - pre-line: مثل `pre-wrap` مع عدم الالتزام بالمسافات المتتالية
- word-wrap:
  - break-word: الالتزام بالعرض (حتى لو كلمة واحدة) (بدون الالتزام بالمسافات والأسطر)

### التحويلات (Transforms)

تحوبل العنصر من مكان لإخر

```css
transform: translate(100px, -200px)
```

- `translate`: move(x, y)
- لو أخذ قيمة واحدة ستكون قيمة `x`
  - `transform: translate(100px)` = `transform: translate(100px, 0)`
- `translateX`: قيمة `x`
- `translateY`: قيمة `y`
- `scale`: الحجم (الخلفية والمحتوى)
  - تكبير (أكبر من 1)
  - تصغير (بين 0 و 1)
  - نكبير مع تقليب عمودي (أصغر من -1)
  - تصغير مع تقليب عمودي (بين 0 و -1)
  - لو أخذ قيمة واحدة ستكون قيمة `x`, `y`
    - `transform: scale(5)` = `transform: scale(5, 5)`
- `scaleX`, `scaleY`: حجم كل تتجاه
  - لهم نفس الخواص
  - القيمة السالبة مع `scaleX`: تقليب أفقي
- `rotate`: الدوران
  - `transform: rotate(80deg)`
  - `transform: rotate(-60deg)` = `300deg`
  - يأخذ قيمة واحدة فقط
- `roteX`: دوران رأسي، `roteY`: دوران أفقي
  - تختفي الخلفية عند (90deg, 270deg)
  - القيم السالبة غير مؤثرة
- `skew`: الانحراف
  - `transform: skew(30deg, -310deg)` = `(-330deg, 50deg)`
  - لو أخذ قيمة واحدة ستكون قيمة `x`
  - `transform: skew(70deg)` = `transform: skew(70deg, 0deg)`
- `skewX`: انحراف أفقي، `skewY`: انحراف رأسي
  - تختفي الخلفية عند (90deg, 270deg)
- `matrix`: إضافة 6 قيم في سطر واحد بدون وحدات وهي:
  - `scaleX`
  - `skewY`
  - `skewX`
  - `scaleY`
  - `translateX`
  - `translateY`
  - القيم الافتراضية: `transform: matrix(1, 0, 0, 1, 0, 0)`
  - `transform: matrix(1, 0, 0, 1, 100, 0)` = `transform: translate(100px)`

#### الفرق بين `position` (مع `top` / `bottom` / `left` / `right`) وبين `transform: translate()`

هو فرق **كبير** من حيث التأثير والسياق والنتائج. لنشرح كل واحدة، ثم نوضح الفرق بينهما بمثال واضح.

---

- أولًا: `position` + `bottom` / `right`

تُستخدم مع أنواع التموضع مثل:

- `relative`
- `absolute`
- `fixed`
- `sticky`

مثال:

```css
position: relative;
bottom: 200px;
right: 100px;
```

- **`relative`**: العنصر يتحرك **نسبة إلى موضعه الأصلي في التدفق العادي للصفحة**، ولكنه **ما يزال يحتفظ بمكانه** الأصلي من حيث حجز المساحة.
- عند كتابة `bottom: 200px;` و `right: 100px;` فهذا يعني:

  > "حرك العنصر لأعلى بمقدار 200px، ولليسار بمقدار 100px"

لاحظ أن:

- `bottom` يدفع العنصر **لأعلى**
- `right` يدفع العنصر **لليسار**

> لأن الاتجاه هو عكس الخاصية، وليس معها.

---

- ثانيًا: `transform: translate(x, y)`

مثال:

```css
transform: translate(200px, 100px);
```

هذا يُحرك العنصر **بصريًا فقط** دون أن يُغيّر من تدفق العنصر أو من موضعه في تدفق الصفحة.

- `translate(200px, 100px)` يعني:

  > "انقل العنصر بصريًا **200px يمينًا** و**100px للأسفل**".

- أهم الفروقات:

| الخاصية                   | position + bottom/right      | transform: translate()       |
| ------------------------- | ---------------------------- | ---------------------------- |
| يؤثر على تدفق العنصر؟     | نعم (في حالات معينة)         | لا                           |
| يحتفظ بمكانه الأصلي؟      | نعم (مع `relative`)          | نعم                          |
| الاتجاه                   | عكس الخاصية (`bottom` يرفعه) | مع الاتجاه (y موجب = للأسفل) |
| قابل للتأنيم (animation)? | أقل سلاسة                    | أكثر سلاسة وأداء أفضل        |
| يتفاعل مع position الأب؟  | نعم                          | لا                           |

---

- مثال عملي لفهم الفرق:

- HTML:

```html
<div class="box1">Position</div>
<div class="box2">Transform</div>
```

- CSS:

```css
.box1, .box2 {
  width: 100px;
  height: 100px;
  background: tomato;
  margin: 20px;
  color: white;
  display: inline-block;
  text-align: center;
  line-height: 100px;
}

.box1 {
  position: relative;
  bottom: 50px;
  right: 50px;
}

.box2 {
  transform: translate(50px, -50px);
}
```

- الملاحظة

- `box1` ستتحرك لأعلى ويسار الصفحة، لكن المساحة التي كانت تشغلها ستبقى فارغة.
- `box2` ستتحرك بنفس الاتجاه، لكن بدون التأثير على المساحة الأصلية أو العناصر المجاورة.

---

- متى أستخدم كل واحدة؟

- استخدم **`transform: translate()`** عندما تريد تحريك العنصر **بدون التأثير على التخطيط** أو عند عمل **أنيميشن** سلس.
- استخدم **`position`** عندما تحتاج إلى **تحديد مكان العنصر بدقة** بالنسبة للأب أو تريد عنصرًا يخرج عن تدفق الصفحة (مثلاً dropdown أو modal).

### التحريكات (Translates)

هو تطور لـ `transform: translate`

```css
translate: 200px 100px;
```

`transform: translate(200px)` = `translate: 200px 0px`

### الأحجام (Scales)

هو تطور لـ `transform: scale`

```css
scale: 2; /* x = 2, y = 2 */
scale: -0.5 3; /* x = -0.5, y = 3 */
```

`transform: scale(2)` = `scale: 2 2`

### الدوران (Rotate)

هو تطور لـ `transform: rotate`

```css
rotate: 20deg;
```

`transform: rotate(70deg)` = `rotate: -290deg`

### الانتقالات (Transitions)

تسمح بإنشاء حركة سلسة عند تغيير الخصائص (التي نكتبها بعد `:`):

```css
button {
  background-color: blue;
  color: blanchedalmond;
  transition: 1s;
}

button:hover {
  background-color: darkblue;
  color: red
}
```

يتغير لون الخلفية والمحتوى بعد ثانية من وضع المؤشر عليه

`1s` = `1000ms`

- `transition` تأخذ أربع خصائص:
  - `property`: تحديد الخاصية (Default: `all`) (يمكن تحديد أكثر من خاصية بعد `,`)
    - `transition: background-color 3000ms, color 1s`
  - `duration`: المدة (Default: `0s`)
  - `timing-function`: شكل الحركة
    - `ease`: slow → fast → slow (Default)
    - `ease-in`: slow → normal speed
    - `ease-out`: normal speed → slow
    - `ease-in-out`: slow → normal speed → slow
    - `linear`: normal speed
    - `steps(n, direction)`: تتحرك خلال عدد خطوات
      - `number_of_steps`: عدد القفزات أو الإطارات.
      - `irection`: إما `start` أو `end` (Default)، وتحدد متى تحدث القفزة.
      - `sters(1)` = `sters(1, end)` = `step-end`
      - `sters(1, start)` = `step-start`
  - `delay`: تأخير التحريك (Default: 0s)
    - `background-color 5s steps(1, start) 8s`
      - يبدأ التغيير بعد 8 ثواني
      - يظل العنصر في وضع الانتقال لمدة 5 ثواني دون تغيير لأنه قفز بالبداية

يمكن تحديد كل خاصية:

```css
transition-property: width, hight;
transition-duration: 3s, 1s;
transition-timing-function: ease;
transition-delay: 2s;
```

---

### التحريكات (Animations)

للحركات المعقدة والمستمرة:

```css
@keyframes slide {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(100px);
  }
}

.box {
  animation: slide 2s infinite alternate;
}
```

`animation`: هي اختصار لخصائصها

- `from`: نقطة البداية
- `to`: نقطة النهاية

يمكن تحديد النقاط من خلال النسبة المئوية مثلا:

```css
0% {
  width: 200px
}
50% {
  width: 250px
}
100% {
  width: 300px
}
```

خصائص:

- **name**: اسم الحركة.
- **duration**: مدتها.
- **timing-function**: منحنى الحركة.
  - `ease`: الافتراضية
  - `linear`: ثابتة
  - نفيس القيم الخاصة بـ `transition-timing-function`
- **delay**: تأخير
- **iteration-count**: عدد التكرارات.
  - `infinite`: لانهائي
- **direction**: اتجاهها
  - `alternate`: ارتداد
  - `reverse`: عكس
  - `normal`: طبيعي (افتراضي)
  - `alternate-reverse`: عكس مع ارتداد
- **fill-mode**: شكل الحركة بالبداية والنهاية
  - `none`: يبدأ وينتهي عند الوضع الأصلي (الافتراضي)
  - `forwards`: ينتهي عند آخر وضع `100%`
  - `backwards`: يبدأ عند أول وضع
  - `both`: يبدأ عند أول وضع وينتهي عند آخر وضع
- **play-state**: حالة التشغيل
  - `runnig`: تشغل (افتراضي)
  - `paused`: إيقاف (يمكن استخدامها مع `hover`)

يمكن استخدام كل خاصية لوحدها:

```css
animation-name: slide;
animation-duration: 4s;
animation-timing-function: linear;
animation-delay: 2s;
animation-iteration-count: infinite;
animation-direction: reverse;
animation-fill-mode: forwards;
animation-play-state: paused;
```

---

### الوراثة (Inheritance)

بعض الخصائص تنتقل تلقائيًا إلى الأبناء:

- color
- font-family
- line-height

خصائص أخرى لا تورث:

- margin
- padding
- background

---

### all: inherit

لجعل كل الخصائص تورث من العنصر الأب:

```css
.child {
  all: inherit;
}
```

---

## تعليقات في CSS

- تعليق أحادي السطر/متعدد:

```css
/* هذا تعليق */
```

---

## تحديد الكل

لتطبيق قاعدة على كل العناصر:

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

✔️ يساعد على إزالة الفروقات بين المتصفحات.

---

## وضع النص في الوسـط

### أفقياً

```css
.text-center {
  text-align: center; /* يعمل على محتويات العناصر الكتلية والسطرية */
}
```

- `text-align`: `left` (افتراضي)، `right`، `center`، `justify`.

### عموديًا (Flex)

```css
.center {
  display: flex;
  justify-content: center; /* محاذاة المحور الرئيسي (أفقي افتراضيًا) */
  align-items: center;     /* محاذاة المحور المعامد (عمودي افتراضيًا) */
}
```

### ملاحظات هامـة

- **الأب (الحاوية)**:
  - في الجسم (المتصفح) أو أي وسـم حاوي:
    - إذا لم تحدد أبعاده: يتكيف مع المحتوى (غير ثابت).
    - إذا حددت أبعاده (`width`/`height`): يصبح ثابتًا.

- **نطاق التطبيق**:
  - `text-align`: يعمل على **محتويات** العناصر الكتلية (`<div>`, `<p>`) والسطرية (`<span>`, `<a>`).
  - `flexbox`: يعمل على العناصر الكتلية ويحول السطرية إلى `inline-block` تلقائيًا.

- **العناصر السطرية (`inline`)**:
  - لها أبعاد (تتسع لمحتواها) ويمكن محاذاتها:
    - أفقيًا: عبر `text-align` في الأب.
    - عموديًا: عبر `line-height` أو `flexbox/grid`.
  - لا يمكن تطبيق `text-align` عليها مباشرة (لأنها لا تحتوي محتوى آخر).

---

### أمثلة توضيحية

#### 1. محاذاة أفقيـة

```html
<div style="text-align: center;">
  <span>نص يتمحور أفقيًا</span>
</div>
```

#### 2. محاذاة عموديـة

```html
<div style="display: flex; height: 100px; align-items: center;">
  <span>نص يتمحور عموديًا</span>
</div>
```

#### 3. محاذاة مركزية شاملة (أفقي + عمودي)

```html
<div style="display: flex; height: 200px; justify-content: center; align-items: center;">
  <span>نص في المنتصف تمامًا</span>
</div>
```

---

### التحذيرات الشائعة

- `text-align: center` لا يمركز العنصر نفسه بل **محتوياته**.
- العناصر السطرية تحتاج إلى تحويلها لـ `inline-block` أو استخدام `flexbox` لمحاذاتها عموديًا.
- المحاذاة العمودية تتطلب تحديد ارتفاع (`height`) للحاوية.

---

## ملاحظات هامة

✅ استعمل وحدات مرنة لتصميم متجاوب.  
✅ نظّم ملفات CSS في أقسام (عناصر أساسية، مكونات، تخطيطات، إعدادات عامة).  
✅ استخدم Media Queries لتلائم كل الشاشات.  
✅ جرب أدوات مثل Flexbox وGrid لتسهيل التخطيط.

---
