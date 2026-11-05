# Nusuk Quiz Assistant — 1.3.3 (Android 11+)

[Download APK 1.3.3](https://github.com/zeyad-ashour/1st/raw/refs/heads/apk-download/downloads/NusukQuizAssistant-1.3.3.apk)

Based on the full 1.3.1/1.3.2 Android 11+ app, with Arabic OCR, direct AI, verified local bank, import/export, and door-error recovery. Same signing certificate; versionCode=13. Install over the earlier full build without uninstalling or clearing its bank/settings.

## تشغيل حسابين جنب بعض

1. ثبّت التحديث، وتأكد أن خدمة إمكانية الوصول والمساعدة مفعّلتان.
2. فعّل **تشغيل الحسابين بتقسيم الشاشة** من الصفحة الرئيسية للمساعد؛ الوضع مقفول افتراضيًا للحفاظ على التشغيل بحساب واحد.
3. افتح نسك الأصلي ونسخته داخل Parallel Space جنب بعض، وكلاهما على صفحة الأبواب أول مرة.
4. فعّل الاختيار والتكرار التلقائيين من الزر 3. إذا كنت تعتمد على AI، فعّل AI والسماح بإجاباته التلقائية في إعداداته كما في النسخة السابقة.
5. راقب أول جولة في النافذتين. الشريط يعرض حالة منفصلة لكل جانب؛ الضغط عليه يوقف الوضع التلقائي للحسابين. لاستئناف حساب توقف للمراجعة، أوقف التلقائي ثم فعّله مجددًا.

لكل نافذة سؤال، وطلب AI، واختيار، وتأكيد، وباب حالي مستقل. طلبا AI يمكنهما العمل بالتوازي، أما الضغطات فتتم بالتبادل لأن لمس الجهاز مشترك. حد طلبات جلسة AI مشترك بين الحسابين، والبنك المحلي المعتمد مشترك لتقليل الطلبات المتكررة في الجولات التالية.

تُقرأ نوافذ التطبيق المسموح بها فقط. عند الحاجة إلى OCR تُلتقط صورة واحدة، ثم تُقص كل نافذة منفردة قبل القراءة، وتُترجم مواقع الاختيارات إلى إحداثيات الشاشة. لا تُخلط اختيارات النافذتين، ولا تُرسل صور الشاشة إلى AI. الرد المتأخر لا ينفذ ضغطة في نافذة أخرى أو على سؤال مختلف.

الحزمة الافتراضية لنسك `com.moh.nusukapp`، ولـParallel Space `com.lbe.parallel.intl`. قد تختلف حزمة النسخة المثبتة على جهازك: استخدم **نسخ تشخيص نوافذ الحسابين** بعد فتحهما إذا لم تظهر حالتا اليمين والشمال. التشخيص يتضمن أسماء الحزم وأرقام وحدود النوافذ فقط؛ لا يحتوي على أسئلة أو مفتاح API. يمكن تعديل حزمة Parallel Space من الصفحة الرئيسية. فتح صفحة أبواب نسك أولًا مطلوب للتعرف عليه داخل حزمة Parallel Space.

## خطأ الأبواب

عند قراءة «حدث خطأ ما، يرجى إعادة المحاولة لاحقًا» وزر «إغلاق»، يغلق الخطأ ثم يغيّر باب هذا الحساب وحده، بعد اختفاء الرسالة. الترتيب: السيرة → القرآن → مكة → المدينة. يستمر على الباب الذي يعمل، ولا يتوقف الحساب الآخر بسبب رسالة الخطأ أو نفاد المفاتيح في حساب واحد.

الرجوع في وضع الحسابين يستهدف سهم نسك داخل النافذة المعنية، ولا يستخدم زر رجوع Android العام. إذا تعذر الرجوع بعد محاولتين، افتح الأبواب يدويًا وسيكمل. بعد أخطاء الأبواب الأربعة توجد مهلة 30 ثانية. عدد محاولات الإغلاق محدود، ولا تُكرر ضغطة صرف مفتاح على نفس الشاشة.

## البنك والبيانات

[Prepared bank ZIP](https://github.com/zeyad-ashour/1st/raw/refs/heads/apk-download/downloads/nusuk-question-bank.zip)

الاستيراد والتصدير كما في الإصدار السابق. مفاتيح AI وبنك المستخدم تبقى على جهازه. عند تشغيل AI يُرسل نص السؤال واختياراته فقط إلى الخدمة المضبوطة. لا يتطلب Root.

## Validation

110 local tests passed, including 10 new dual-account tests. Covers same-package window isolation, shared gesture serialization, clone recognition, independent selection and confirmation, per-account error/door recovery, continuing after one account exhausts keys, parallel AI replies, shared request limit, stale callbacks, unrelated app rejection, and OCR coordinate clipping/translation. Android Lint: 0 errors; one existing obsolete API guard warning. APK signature, update certificate, version/minSdk, and ZIP/native alignment verified. Arabic OCR assets and ARM64/x86_64 libraries remain included.

**No live Nusuk / Parallel Space device was available. The split-screen workflow, host package identity, screenshot permissions and actual taps still need verification on the user's device. Android 11+ is required; some clone apps may prevent accessibility or screenshots.**

SHA-256: `479c7d0ab9cd474ea22d59c887e4fd1fa781c34f121e79267e209f666661f89d`
