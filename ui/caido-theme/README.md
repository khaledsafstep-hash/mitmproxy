# 🎨 Caido UI Theme for mitmproxy

> تصميم واجهة مستخدم حديثة وجميلة بألوان مستوحاة من تطبيق Caido

## 📋 نظرة عامة

هذا المشروع يتضمن نظام تصميم شامل (Design System) لواجهة مستخدم mitmproxy مستوحى من تطبيق Caido الشهير. يتميز بألوان داكنة احترافية مع لمسات برتقالية حية.

## 🎯 الخصائص الرئيسية

- **نظام ألوان مظلم**: خلفيات داكنة مع نصوص فاتحة للراحة البصرية
- **لون أساسي برتقالي**: #ff6b35 لجميع العناصر التفاعلية
- **مكونات منظمة**: أزرار، نماذج، جداول، قوائم جانبية
- **سهولة التخصيص**: متغيرات LESS قابلة للتعديل بسهولة
- **استجابة كاملة**: تدعم جميع أحجام الشاشات

## 📁 هيكل الملفات

```
ui/caido-theme/
├── variables.less      # متغيرات الألوان والتباعد
├── base.less          # الأساليس الأساسية
├── buttons.less       # أنماط الأزرار
├── forms.less         # عناصر النماذج
├── sidebar.less       # القائمة الجانبية
├── topbar.less        # شريط العنوان
├── table.less         # جداول البيانات
├── split-view.less    # عرض Request/Response المقسم
├── statusbar.less     # شريط الحالة
└── main.less          # التخطيط الرئيسي
```

## 🎨 نظام الألوان

### الألوان الأساسية

| اللون | الكود | الاستخدام |
|------|------|----------|
| أسود عميق | `#0f0f0f` | الخلفية الدقيقة جداً |
| داكن | `#1a1a1a` | الخلفية الأساسية |
| متوسط | `#2a2a2a` | الخلفية الثانوية |
| فاتح | `#3a3a3a` | الخلفية الثالثة |
| برتقالي | `#ff6b35` | لون التركيز والأزرار الرئيسية |

### الألوان الدلالية

- **الأخضر**: `#4ade80` - نجاح (HTTP 200)
- **الأحمر**: `#f87171` - خطأ
- **الأصفر**: `#facc15` - تحذير
- **الأزرق**: `#38bdf8` - معلومات

## 🚀 البدء السريع

### 1. استيراد المكتبة

```less
@import 'ui/caido-theme/main.less';
```

### 2. استخدام المتغيرات

```less
.my-component {
  background-color: @bg-primary;
  color: @text-primary;
  border: 1px solid @border-color;
}
```

### 3. استخدام المكونات

```html
<!-- زر أساسي -->
<button class="btn btn-primary">اضغط هنا</button>

<!-- زر ثانوي -->
<button class="btn btn-secondary">إلغاء</button>

<!-- حقل إدخال -->
<input type="text" class="form-input" placeholder="أدخل البيانات">

<!-- جدول -->
<table class="data-table">
  <thead>
    <tr>
      <th>العنوان</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>البيانات</td>
    </tr>
  </tbody>
</table>
```

## 📐 وحدات التباعد

```less
@spacing-xs:  4px;   // Extra Small
@spacing-sm:  8px;   // Small
@spacing-md:  12px;  // Medium
@spacing-lg:  16px;  // Large
@spacing-xl:  24px;  // Extra Large
@spacing-2xl: 32px;  // 2X Extra Large
```

## 🔧 تخصيص الألوان

عدّل المتغيرات في `variables.less`:

```less
// تغيير اللون الأساسي
@primary-accent: #ff6b35;  // غيّر هنا

// تغيير لون النص
@text-primary: #ffffff;

// تغيير لون الخلفية
@bg-primary: #1a1a1a;
```

## 📦 المكونات المتوفرة

### الأزرار

```html
<!-- أنواع مختلفة من الأزرار -->
<button class="btn btn-primary">أساسي</button>
<button class="btn btn-secondary">ثانوي</button>
<button class="btn btn-ghost">شفاف</button>
<button class="btn btn-success">نجاح</button>
<button class="btn btn-error">خطأ</button>
<button class="btn btn-warning">تحذير</button>

<!-- أحجام مختلفة -->
<button class="btn btn-sm">صغير</button>
<button class="btn">عادي</button>
<button class="btn btn-lg">كبير</button>
```

### النماذج

```html
<!-- حقل بسيط -->
<div class="form-group">
  <label>البريد الإلكتروني</label>
  <input type="email" class="form-input" placeholder="example@test.com">
  <p class="form-hint">أدخل بريدك الإلكتروني الصحيح</p>
</div>

<!-- Checkbox -->
<div class="checkbox-item">
  <input type="checkbox" id="agree">
  <label for="agree">أوافق على الشروط</label>
</div>

<!-- Radio -->
<div class="radio-item">
  <input type="radio" name="option" id="option1">
  <label for="option1">الخيار الأول</label>
</div>

<!-- Toggle Switch -->
<div class="switch">
  <input type="checkbox" id="toggle">
  <label for="toggle">تفعيل الميزة</label>
</div>
```

### الجداول

```html
<div class="table-container">
  <table class="data-table">
    <thead>
      <tr>
        <th class="sortable">الطريقة</th>
        <th class="sortable">الـ URL</th>
        <th>الحالة</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><span class="method-badge">GET</span></td>
        <td><span class="url">https://example.com/api</span></td>
        <td><span class="status-badge status-200">200</span></td>
      </tr>
    </tbody>
  </table>
</div>
```

## 📱 الاستجابة

جميع المكونات مصممة لتكون متجاوبة:

```less
@media (max-width: 1024px) {
  // تعديلات للأجهزة المتوسطة
}

@media (max-width: 768px) {
  // تعديلات للأجهزة الصغيرة
}
```

## 🎭 الحالات الخاصة

### الزر في حالة التحميل

```html
<button class="btn btn-loading loading">
  <span class="spinner"></span>
</button>
```

### الإدخال مع الأيقونة

```html
<div class="input-with-icon">
  <span class="icon">🔍</span>
  <input type="text" placeholder="ابحث...">
</div>
```

### النافذة المنبثقة (Modal)

```html
<div class="modal active">
  <div class="modal-header">
    <h2 class="modal-title">العنوان</h2>
    <button class="modal-close">&times;</button>
  </div>
  <div class="modal-body">
    المحتوى هنا
  </div>
  <div class="modal-footer">
    <button class="btn btn-secondary">إلغاء</button>
    <button class="btn btn-primary">حفظ</button>
  </div>
</div>
```

## 📊 شاشات العرض

### القائمة الجانبية
- عرض عادي: 200px
- عرض مطوي: 60px
- قائمة نشطة مع شريط برتقالي

### شريط العنوان
- ارتفاع: 60px
- منطقة بحث في المنتصف
- أزرار على اليمين

### شريط الحالة
- ارتفاع: 40px
- معلومات الحالة على اليسار
- أزرار الإجراءات السريعة على اليمين

## 🌙 الوضع الليلي

المقالة مصممة بالكامل للوضع الليلي (Dark Mode) بشكل افتراضي.

للتبديل إلى وضع مشابه للنهار:

```less
// استبدل المتغيرات في variables.less
@bg-primary: #ffffff;
@text-primary: #000000;
// إلخ...
```

## 💡 نصائح التطوير

1. **استخدم المتغيرات**: لا تكتب الألوان مباشرة، استخدم المتغيرات
2. **اتبع نمط الفئات**: استخدم بادئات واضحة (`.btn-`, `.form-`, إلخ)
3. **اختبر على أحجام مختلفة**: تأكد من استجابة المكونات
4. **اعتمد على Transitions**: استخدم `@transition-base` للانتقالات السلسة

## 🔄 الانتقالات والرسوم المتحركة

```less
// سرعات الانتقال
@transition-fast: 150ms ease-in-out;
@transition-base: 250ms ease-in-out;
@transition-slow: 350ms ease-in-out;
```

## 🎬 الرسوم المتحركة المتوفرة

- `spin`: دوران محمل
- `slideIn`: انزلاق للداخل
- `fadeIn`: تلاشي للداخل

## 📝 أمثلة الاستخدام

### مثال كامل

```html
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet/less" href="ui/caido-theme/main.less">
  <script src="less.js"></script>
</head>
<body>
  <div class="app-container">
    <!-- القائمة الجانبية -->
    <aside class="sidebar">
      <div class="sidebar-header">
        <div class="logo">🔍 mitmproxy</div>
      </div>
      <div class="sidebar-menu">
        <div class="menu-section">
          <div class="section-title">أدوات</div>
          <div class="menu-item active">
            <span class="icon">📡</span>
            <span class="label">الطلبات</span>
          </div>
        </div>
      </div>
    </aside>

    <!-- المحتوى الرئيسي -->
    <div class="main-layout">
      <div class="topbar">
        <div class="topbar-center">
          <input type="text" class="search-input" placeholder="ابحث...">
        </div>
      </div>

      <div class="workspace-content">
        <!-- محتوى البيانات -->
      </div>

      <div class="status-bar">
        <div class="status-info">
          <span class="status-item">
            <span class="status-label">الحالة:</span>
            <span class="status-value">جاهز</span>
          </span>
        </div>
      </div>
    </div>
  </div>
</body>
</html>
```

## 🤝 المساهمة

لإضافة مكونات جديدة:

1. أضف الأنماط في الملف المناسب
2. استخدم المتغيرات المعرفة
3. اتبع نمط التسمية
4. أضف مثال في README

## 📄 الترخيص

MIT License - انظر LICENSE للتفاصيل

## 👥 الدعم

للمساعدة والأسئلة:
- قم بفتح Issue
- راجع التوثيق
- تحقق من الأمثلة

---

**تم الإنشاء بواسطة**: Khaled SafStep  
**التاريخ**: 2026-08-14  
**الإصدار**: 1.0.0
