# TODO - إصلاحات و إعادة بناء المشروع

## خطوة 1: إعداد خطة التعديل
- [x] اختيار: الاثنين (الجذر + deploy)
- [x] تثبيت/تطابق أسماء الملفات (app.html vs deploy/index.html)


## خطوة 2: إصلاح Tailwind config في app.html و deploy/index.html
- [ ] تصحيح الأقواس/الـscript tag لتفادي كسر JS


## خطوة 3: إصلاح Service Worker
- [ ] توحيد CACHE_NAME
- [ ] تعديل ASSETS بحيث تشير لمسارات صحيحة داخل الجذر والـdeploy
- [ ] تحسين fallback لمسار document الصحيح

## خطوة 4: إزالة الاعتماد على global event
- [ ] استبدال `onclick="if(event.target===this)"` بـ handler يمرر event

## خطوة 5: تقليل مخاطر XSS
- [ ] إضافة دالة escape للحقول النصية قبل وضعها داخل HTML
- [ ] استخدام escape في مواضع: أسماء/عناوين/رسائل/notes

## خطوة 6: تحسين منطق Leave
- [ ] عند رفض leave: إعادة حالة الموظف active إذا لا يوجد approved آخر يثبت على on_leave
- [ ] عند تغيير الحالة من approved إلى rejected/أو رفض طلبات أخرى

## خطوة 7: تحديث Calendar UI
- [ ] عرض description/type
- [ ] إضافة Delete/Edit للـevents (اختياري حسب الطلب)

## خطوة 8: اختبارات يدوية
- [ ] فتح التطبيق على الجذر و deploy
- [ ] اختبار offline/service worker
- [ ] اختبار سيناريو leave approval/rejection

