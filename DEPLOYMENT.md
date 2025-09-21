# دليل النشر على Firebase - Firebase Deployment Guide

## الخطوات المطلوبة للنشر:

### 1. إنشاء مشروع Firebase جديد

1. اذهب إلى [Firebase Console](https://console.firebase.google.com/)
2. انقر على "إضافة مشروع" / "Add project"
3. اختر اسماً للمشروع (مثل: `altamimi-app`)
4. اختر إعدادات المشروع حسب تفضيلاتك
5. انقر على "إنشاء مشروع" / "Create project"

### 2. تفعيل Firebase Hosting

1. في وحة تحكم Firebase، اذهب إلى قسم "Hosting"
2. انقر على "البدء" / "Get started"
3. اتبع التعليمات المعروضة

### 3. تحديث إعدادات المشروع

قم بتعديل الملف `.firebaserc` ليحتوي على معرف مشروعك:

```json
{
  "projects": {
    "default": "your-project-id-here"
  }
}
```

استبدل `your-project-id-here` بمعرف مشروعك الفعلي.

### 4. تثبيت Firebase CLI وتسجيل الدخول

```bash
# تثبيت Firebase CLI عالمياً
npm install -g firebase-tools

# تسجيل الدخول
firebase login

# التأكد من الاتصال بالمشروع الصحيح
firebase use --add
```

### 5. النشر

```bash
# نشر الموقع
firebase deploy --only hosting
```

### 6. الوصول إلى الموقع

بعد النشر بنجاح، ستحصل على رابط الموقع مثل:
`https://your-project-id.web.app`

## ملاحظات مهمة:

- تأكد من أن جميع الملفات في مجلد `public/` صحيحة
- يمكنك اختبار الموقع محلياً قبل النشر باستخدام `firebase serve`
- يمكنك ربط دومين مخصص من خلال إعدادات Firebase Hosting

## استكشاف الأخطاء:

### خطأ في المصادقة:
```bash
firebase login --reauth
```

### خطأ في الصلاحيات:
تأكد من أن حسابك له صلاحيات التعديل على المشروع

### مشاكل في النشر:
```bash
firebase deploy --debug
```