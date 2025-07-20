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
    - [التباعد الداخلي والخارجي](#التباعد-الداخلي-والخارجي)
    - [ملاحظة هامة عن الـ Box Model](#ملاحظة-هامة-عن-الـ-box-model)
    - [الخطوط](#الخطوط)
  - [أنواع المحددات (Selectors)](#أنواع-المحددات-selectors)
    - [المحددات البسيطة](#المحددات-البسيطة)
    - [محددات أكثر تعقيدًا](#محددات-أكثر-تعقيدًا)
    - [محددات السمات](#محددات-السمات)
  - [الوحدات المستخدمة في CSS](#الوحدات-المستخدمة-في-css)
    - [استخدام الأمثلة](#استخدام-الأمثلة)
    - [ملاحظات](#ملاحظات)
    - [مشكلة النسبة المئوية](#مشكلة-النسبة-المئوية)
  - [التعامل مع الألوان](#التعامل-مع-الألوان)
  - [الخلفيات](#الخلفيات)
    - [خصائص الخلفية](#خصائص-الخلفية)
    - [اختصار الخلفية](#اختصار-الخلفية)
  - [أمثلة عملية](#أمثلة-عملية)
  - [الخطوط والنصوص](#الخطوط-والنصوص)
  - [الصندوق (Box Model)](#الصندوق-box-model)
    - [padding](#padding)
    - [margin](#margin)
    - [border](#border)
    - [box-sizing](#box-sizing)
  - [العناصر Block وInline](#العناصر-block-وinline)
    - [التحكم في النوع](#التحكم-في-النوع)
    - [visibility](#visibility)
  - [خاصية overflow](#خاصية-overflow)
  - [الموقع والإزاحة](#الموقع-والإزاحة)
  - [Position](#position)
  - [Float](#float)
  - [القوائم (List Styles)](#القوائم-list-styles)
    - [موقع النقطة](#موقع-النقطة)
    - [صورة بدلاً من النقاط](#صورة-بدلاً-من-النقاط)
    - [اختصار](#اختصار)
  - [التأثيرات البصرية (Hover, Focus, Checked)](#التأثيرات-البصرية-hover-focus-checked)
    - [Hover](#hover)
    - [Visited](#visited)
    - [Focus](#focus)
    - [Checked](#checked)
    - [Opacity](#opacity)
  - [الأمثلة العملية](#الأمثلة-العملية)
  - [العناصر الزائفة (Pseudo-elements)](#العناصر-الزائفة-pseudo-elements)
    - [::first-letter](#first-letter)
    - [::first-line](#first-line)
    - [::selection](#selection)
    - [::before و::after](#before-وafter)
  - [تخطيط الصفحة (Flexbox, Grid)](#تخطيط-الصفحة-flexbox-grid)
    - [Flexbox](#flexbox)
    - [Grid](#grid)
  - [الاستجابة للشاشات (Media Queries)](#الاستجابة-للشاشات-media-queries)
  - [مفاهيم متقدمة](#مفاهيم-متقدمة)
    - [الانتقالات (Transitions)](#الانتقالات-transitions)
    - [التحريكات (Animations)](#التحريكات-animations)
    - [الوراثة (Inheritance)](#الوراثة-inheritance)
    - [all: inherit](#all-inherit)
  - [تعليقات في CSS](#تعليقات-في-css)
  - [تحديد الكل](#تحديد-الكل)
  - [وضع النص في الوسط](#وضع-النص-في-الوسط)
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
- text-align: left, right, center, justify
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
<p class="highlight">...</p>
```

```css
.highlight { color: red; }
```

استدعاء الكلاس بنقطة `.`.

- بالمعرف (ID):

```html
<p id="unique">...</p>
```

```css
#unique { color: green; }
```

استدعاء الـ ID بالرمز `#`.

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

```css
h2 + p { margin-top: 0; }
```

ينطبق على أول p بعد h2 مباشرة.

- تحديد كل الأشقاء اللاحقين:

```css
h2 ~ p { color: gray; }
```

ينطبق على كل p بعد h2 في نفس المستوى.

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

---

## الوحدات المستخدمة في CSS

الوحدات تسمح لك بقياس المسافات والأحجام:

- **px**: بكسل – وحدة ثابتة.
- **em**: نسبة لحجم خط الأب.
- **rem**: نسبة لحجم الخط الجذر.
- **%**: نسبة مئوية لحاوية العنصر.
- **vw / vh**: نسبة من عرض أو ارتفاع الشاشة.
- **fr**: في Grid لتقسيم المساحات.
- **auto**: يعتمد على المحتوى.

---

### استخدام الأمثلة

```css
width: 80%;
font-size: 1.2em;
margin: auto;
height: 50vh;
```

---

### ملاحظات

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

### خصائص الخلفية

- تكرار الخلفية:

```css
background-repeat: no-repeat;
background-repeat: repeat-x;
background-repeat: repeat-y;
```

- حجم الخلفية:

```css
background-size: cover;
background-size: contain;
background-size: 100px 200px;
```

- موقع الخلفية:

```css
background-position: center;
background-position: top left;
background-position: 50% 50%;
```

- ثبات الخلفية أثناء التمرير:

```css
background-attachment: fixed;
background-attachment: scroll;
```

### اختصار الخلفية

يمكن دمج كل الخصائص في خاصية واحدة:

```css
background: url("image.jpg") no-repeat center / cover;
```

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

✅ ملاحظة: يمكن معاينة الألوان بسهولة في أغلب المحررات بوجود معاين تلقائي، كما تدعم بعض المتصفحات اختيار الألوان مباشرة من أدوات المطور.

---

## الخطوط والنصوص

لإضفاء طابع جمالي على النصوص، تستخدم عدة خصائص:

- **font-family**: تحديد الخط

```css
p {
  font-family: Arial, Helvetica, sans-serif;
}
```

يمكن كتابة عدة خطوط بالترتيب، لو لم يتوفر الأول ينتقل للثاني.

- **font-size**: حجم الخط

```css
h1 {
  font-size: 32px;
}
p {
  font-size: 16px;
}
```

- **font-weight**: سمك الخط

```css
strong {
  font-weight: bold;
}
.light {
  font-weight: 300;
}
```

القيم الممكنة: normal, bold أو أرقام (100 إلى 900).

- **line-height**: المسافة بين السطور

```css
p {
  line-height: 1.5;
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

- **direction**: اتجاه النص

```css
body {
  direction: rtl;
}
```

مثالية لدعم اللغات من اليمين لليسار.

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

- **Block**: تأخذ عرض السطر كاملًا وتبدأ في سطر جديد.
  - أمثلة: div, p, h1-h6, section
  - يمكن تحديد عرض وطول، خلفية تغطي كل السطر.

- **Inline**: تبقى في نفس السطر مع العناصر المجاورة.
  - أمثلة: span, a, strong, em
  - لا يمكن تحديد عرض وطول، الخلفية تغطي المحتوى فقط.

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

- **none**: يخفي العنصر تمامًا ويزيله من التخطيط.

```css
.hidden {
  display: none;
}
```

---

### visibility

- يتحكم في الظهور مع بقاء المساحة.

```css
.visible {
  visibility: visible;
}

.invisible {
  visibility: hidden;
}
```

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

---

## الموقع والإزاحة

---

## Position  

خاصية position تتحكم في مكان العنصر في الصفحة:

- **static** (افتراضي): موقع طبيعي في التدفق.
- **relative**: يسمح بتحريك العنصر من مكانه الأصلي.

```css
.relative {
  position: relative;
  top: 10px;
  left: 20px;
}
```

- **absolute**: يخرج من التدفق العادي ويتموضع نسبة لأقرب أب

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

يبقى في مكانه عند التمرير حتى حد معين.

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

- يسمح بوضع عناصر بجانب بعضها.
- يخرجها من التدفق العادي مما قد يجعل الخلفية أو الحدود لا تحتويها.

لحل مشكلة "الخروج" من الحاوية:

```css
.clearfix::after {
  content: "";
  display: table;
  clear: both;
}
```

---

✅ ملاحظة:

- بعد استخدام float، يجب عادةً "تصفية" التدفق بـ clear.

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

يفضل أن تكون الصورة صغيرة الحجم.

---

### اختصار

```css
ul {
  list-style: square inside;
}
```

يمكن دمج النوع والموقع.

---

## التأثيرات البصرية (Hover, Focus, Checked)

### Hover

تطبيق تنسيق عند مرور المؤشر:

```css
a:hover {
  color: red;
  text-decoration: none;
}
```

### Visited

تطبيق تنسيق على الروابط التي تمت زيارتها:

```css
a:visited {
  color: purple;
}
```

---

### Focus

تطبيق تنسيق عند تركيز المستخدم على عنصر (مثل input):

```css
input:focus {
  outline: none;
  border: 2px solid blue;
}
```

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

## العناصر الزائفة (Pseudo-elements)

العناصر الزائفة تسمح بتحديد أجزاء من المحتوى لتطبيق تنسيق خاص:

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

يمكن استخدامها لإنشاء أشكال مثل الخطوط داخل الحاويات:

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

---

## تخطيط الصفحة (Flexbox, Grid)

### Flexbox

طريقة حديثة لتنظيم العناصر في اتجاه واحد (صف أو عمود):

```css
.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
```

خصائص رئيسية:

- **justify-content**: توزيع العناصر أفقياً.
- **align-items**: محاذاة عمودية.
- **flex-direction**: row (افتراضي), column.

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

خصائص:

- **grid-template-columns / rows**: تقسيم الشبكة.
- **gap**: المسافة بين العناصر.

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

### الانتقالات (Transitions)

تسمح بإنشاء حركة سلسة عند تغيير الخصائص:

```css
button {
  background-color: blue;
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: darkblue;
}
```

خصائص الانتقال:

- **property**: الخاصية المراد تحريكها.
- **duration**: مدة الحركة.
- **timing-function**: نوع المنحنى (ease, linear, ease-in-out).
- **delay**: تأخير.

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

خصائص:

- **name**: اسم الحركة.
- **duration**: مدتها.
- **iteration-count**: عدد التكرارات.
- **direction**: عكس/بدون عكس (alternate).
- **timing-function**: منحنى الحركة.

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

## وضع النص في الوسط

- أفقياً:

```css
.text-center {
  text-align: center;
}
```

- عموديًا (Flex):

```css
.center {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

---

## ملاحظات هامة

✅ استعمل وحدات مرنة لتصميم متجاوب.  
✅ نظّم ملفات CSS في أقسام (عناصر أساسية، مكونات، تخطيطات، إعدادات عامة).  
✅ استخدم Media Queries لتلائم كل الشاشات.  
✅ جرب أدوات مثل Flexbox وGrid لتسهيل التخطيط.

---
