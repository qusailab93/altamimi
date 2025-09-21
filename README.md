# تطبيق التميمي - Altamimi App

موقع إلكتروني متجاوب باللغة العربية مصمم للنشر على Firebase Hosting.

## المحتويات

- صفحة رئيسية ترحيبية
- قسم "من نحن"
- قسم الخدمات
- نموذج اتصال تفاعلي
- تصميم متجاوب يدعم الهواتف والأجهزة اللوحية

## التقنيات المستخدمة

- HTML5
- CSS3 (مع دعم RTL للعربية)
- JavaScript (ES6+)
- Firebase Hosting

## التثبيت والتشغيل

### متطلبات النظام

- Node.js (الإصدار 14 أو أحدث)
- npm أو yarn
- Firebase CLI

### تثبيت Firebase CLI

```bash
npm install -g firebase-tools
```

### تسجيل الدخول إلى Firebase

```bash
firebase login
```

### تشغيل المشروع محلياً

```bash
# تثبيت المتطلبات
npm install

# تشغيل الخادم المحلي
firebase serve
```

سيكون الموقع متاحاً على `http://localhost:5000`

## النشر على Firebase

### إعداد مشروع Firebase

1. اذهب إلى [Firebase Console](https://console.firebase.google.com/)
2. أنشئ مشروعاً جديداً أو استخدم مشروعاً موجوداً
3. فعّل Firebase Hosting

### تحديث معرف المشروع

قم بتعديل الملف `.firebaserc` وضع معرف مشروعك:

```json
{
  "projects": {
    "default": "your-project-id"
  }
}
```

### النشر

```bash
# النشر لأول مرة
firebase init hosting

# النشر
npm run deploy
```

أو

```bash
firebase deploy --only hosting
```

## هيكل الملفات

```
├── public/
│   ├── index.html      # الصفحة الرئيسية
│   ├── style.css       # ملف التنسيقات
│   └── script.js       # ملف JavaScript
├── firebase.json       # إعدادات Firebase
├── .firebaserc        # معرف مشروع Firebase
├── package.json       # إعدادات المشروع ومتطلباته
└── README.md          # هذا الملف
```

## الميزات

- **تصميم متجاوب**: يعمل بشكل مثالي على جميع الأجهزة
- **دعم كامل للعربية**: اتجاه RTL وخطوط مناسبة
- **تفاعلي**: نموذج اتصال وتأثيرات انيميشن
- **سريع التحميل**: ملفات محسنة وmضغوطة
- **SEO محسن**: بنية HTML صحيحة ومحسنة لمحركات البحث

## التخصيص

يمكنك تخصيص الموقع من خلال:

1. تعديل المحتوى في `public/index.html`
2. تغيير الألوان والتنسيقات في `public/style.css`
3. إضافة وظائف جديدة في `public/script.js`

## الدعم

إذا واجهت أي مشاكل، يرجى:

1. التأكد من تثبيت Firebase CLI بشكل صحيح
2. التأكد من تسجيل الدخول إلى Firebase
3. التأكد من صحة معرف المشروع في `.firebaserc`

## الترخيص

هذا المشروع مرخص تحت رخصة MIT.