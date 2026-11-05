# Nusuk Quiz Assistant — 1.3.2 (Android 11+)

[Download APK 1.3.2](https://github.com/zeyad-ashour/1st/raw/refs/heads/apk-download/downloads/NusukQuizAssistant-1.3.2.apk)

Based on the full Android 11+ 1.3.1 feature set, including Arabic OCR, direct AI, local bank, import and export. This is not the Android 7 compatibility variant. Same signing certificate and higher versionCode=12 permit updating earlier builds without uninstalling or clearing data.

## خطأ الدخول إلى الأبواب

- يبدأ من باب السيرة النبوية، أو آخر باب عمل في الجلسات السابقة.
- عند قراءة رسالة **حدث خطأ / حدث خطأ ما** مع **يرجى إعادة المحاولة لاحقًا** وزر **إغلاق**، يغلق الرسالة في الوضع التلقائي. لا تُعامل رسائل AI أو الإجابة الخاطئة أو مجرد وجود زر إغلاق كخطأ أبواب.
- لا يُغيّر الباب حتى تختفي رسالة الخطأ فعليًا. بعدها ينتقل بالترتيب: السيرة النبوية → القرآن الكريم → مكة المكرمة والمسجد الحرام → المدينة المنورة والمسجد النبوي.
- إذا كانت صفحة الأبواب غير ظاهرة بعد الإغلاق، يجرب الرجوع ضمن تطبيق نسك، بحد محاولتين؛ إذا لم يصل لصفحة الأبواب يطلب فتحها يدويًا ويتابع عند ظهورها.
- يستمر على الباب الحالي بعد نجاح فتح السؤال، بما في ذلك الجولات التالية. لا يبدله إلا عند ظهور رسالة الخطأ المحددة.
- إذا فشلت الأبواب الأربعة قبل ظهور سؤال، ينتظر 30 ثانية ثم يعيد المحاولة. إغلاق الرسالة له محاولات محدودة وفاصل بين المحاولات؛ لا يعيد صرف مفتاح بسبب تكرار نفس الشاشة.
- المساعدة تعرض الحالة دون ضغط إذا كان الوضع التلقائي مقفولًا. لا تتغير إعدادات AI أو إجابات البنك.

## الاستخدام

ثبّت التحديث دون حذف التطبيق السابق، فعّل خدمة إمكانية الوصول والمساعدة العائمة والوضع التلقائي من الزر 3. افتح نسك وراقب أول استرداد للخطأ. قراءة OCR وصلاحيات Android 11+ كما في 1.3.1. عند نجاح قراءة السؤال، يراجع البنك المعتمد قبل طلب AI.

[Prepared bank ZIP](https://github.com/zeyad-ashour/1st/raw/refs/heads/apk-download/downloads/nusuk-question-bank.zip)

الاستيراد والتصدير يحتفظان بنفس السلوك السابق؛ لا تُرفع مفاتيح أو بيانات المستخدم تلقائيًا.

## Actual validation

100 local tests passed (89 regression tests plus 11 door-recovery tests). Includes the screenshot's error wording, combined OCR text, missing/ambiguous close targets, switching across four doors, sticky working-door selection, backoff, restored selection, manual navigation, and preventing duplicate open attempts. Android Lint: no errors, one harmless obsolete-version-guard warning. APK signature, update certificate, minSdk=30, version metadata and ZIP/native alignment verified. Full Arabic OCR assets and ARM64/x86_64 Tesseract libraries are present.

**No live Nusuk UI/device was available. Actual modal closing, Back behavior, category labels and service availability must be checked on the user's device.**

SHA-256: `99d87de00fea8ed1af95dd4c661324ef332d903c424d4e44a515607c247f4627`
