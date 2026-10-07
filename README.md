# ORIFA — Website

إعادة بناء موقع Orifa (النسخة الأصلية على Canva) كموقع ثابت بـ HTML5 / CSS3 / Vanilla JS،
جاهز للرفع مباشرة على GitHub Pages.

## البنية

```
index.html
course-brand.html / course-ai.html / course-fashion.html / course-illustrator.html   صفحات تفاصيل الدورات
style.css
script.js
assets/
  logo-orifa.png     شعار Orifa الذهبي (خلفية شفافة)
  ornament.png       الزخرفة الذهبية أعلى بطاقات الدورات
  hero-banner.jpg    بانر الهيرو العاجي
```

## الرفع على GitHub Pages

1. أنشئي repository جديد باسم `orifa` (أو أي اسم).
2. ارفعي محتويات هذا المجلد كما هي في الجذر (وليس داخل مجلد فرعي).
3. Settings → Pages → Source: `Deploy from a branch` → Branch: `main` / `(root)` → Save.
4. الرابط سيكون: `https://<username>.github.io/orifa/`

لا يحتاج الموقع أي backend ولا build step ولا سيرفر محلي.

## ملاحظات

- الخطوط الحالية من Google Fonts كبدائل مؤقتة (Cormorant Garamond / Playfair Display / Almarai / Changa).
  عند توفر ملفات MediaPro و Stazin: ضعيها في `assets/fonts/` وأضيفي `@font-face` في أعلى `style.css`،
  ثم بدّلي قيم `--font-*`.
- أيقونات الخدمات مرسومة SVG داخل `index.html` ويمكن استبدالها بملفات مُصدّرة من Canva.
- الألوان معرّفة كمتغيّرات CSS في `:root` أعلى `style.css`.

## خلفية الموقع (نمط شعار Orifa)

الخلفية الموحدة معرّفة في `style.css` تحت عنوان `SITE BACKGROUND` (رمز الشعار كـ SVG داخل الـ CSS، بدون ملف صورة).
التحكم بسهولة من `:root` في أعلى الملف:

- `--bg` لون البيج (#eee7dc)
- `--pattern-ink` درجة لون الرمز (أغمق من البيج بقليل) — اجعليه أقرب لـ `--bg` ليصبح أخفى
- `--pattern-size` حجم المربع المتكرر (كل مربع فيه 16 رمزًا): قيمة أكبر = رموز أكبر وأقل كثافة

## رابط التسجيل

زر "سجّل الآن" في صفحات الدورات الأربع يفتح رابط الاستبيان (Google Forms). لتغييره ابحثي عن `docs.google.com/forms` في ملفات `course-*.html`.
