# Nusuk Quiz Assistant — 1.2.2

[Download APK 1.2.2](https://github.com/zeyad-ashour/1st/raw/refs/heads/apk-download/downloads/NusukQuizAssistant-1.2.2.apk)

Android 11+; ARM64/x86_64. Debug/test APK. Same signing certificate as 1.2.1; install as an update to retain the local bank and device-local encrypted API key.

## تشخيص اتصال Gemini

هذه نسخة تشخيص لخطأ 404، وليست تأكيدًا أن مشكلة الخدمة قد أُصلحت.

1. ثبّت التحديث دون حذف التطبيق السابق.
2. افتح **إعدادات الذكاء الاصطناعي** واترك الرابط والنموذج والمفتاح المحفوظ كما هي.
3. اضغط **حفظ واختبار الاتصال** مرة واحدة.
4. عند الفشل يظهر URL الفعلي وHTTP وstatus ورسالة الخطأ المنظمة من الخدمة. اضغط **نسخ تشخيص الاتصال** وأرسل النص للمراجعة.

التشخيص يظهر لاختبار الاتصال اليدوي فقط؛ لا تُعرض رؤوس الطلب أو نص السؤال أو جسم الرد الكامل. تُزال بيانات الدخول ومعاملات الاستعلام من الرابط ويُحجب المفتاح المعروف وأنماط المفاتيح من رسالة الخطأ. لا يتم إرسال التقرير تلقائيًا ولا حفظه في سجل دائم. شاشة الإعدادات تظل محمية من الالتقاط؛ استخدم زر النسخ للنص التشخيصي فقط. لم تتغير آلية اختيار الإجابات أو التكرار.

## Actual validation

75 local tests passed, including 14 native Gemini HTTPS/mock tests, three diagnostic redaction tests, 30 AI/flow tests, four UI/storage tests, and 24 core tests. Android Lint: zero issues. APK signature, matching update certificate, version metadata, and ZIP/native 16 KB alignment verified.

**No live Google API key or Android device was available. Real Gemini availability and the cause of the user's 404 still require the device-side diagnostic report.**

SHA-256 1.2.2: `edf3c8c75950113def659faf8a431cc7a84f480b6bb820879e01b7d1e78b9b06`
