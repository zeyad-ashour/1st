# Nusuk Quiz Assistant — 1.3.4 (Android 11+)

[Download APK 1.3.4](https://github.com/zeyad-ashour/1st/raw/refs/heads/apk-download/downloads/NusukQuizAssistant-1.3.4.apk)

Based on the full 1.3.1/1.3.2 Android 11+ app, with Arabic OCR, direct AI, verified local bank, import/export, and door-error recovery. Same signing certificate; versionCode=14. Install over the earlier full build without uninstalling or clearing its bank/settings.

## تحسين السرعة والأسئلة التي لا تصل إلى AI

- الفاصل الداخلي الأدنى بين الضغطات 350ms بدلًا من 2500ms، والمتابعة الدورية 400ms بدلًا من 1800ms. أحداث نسك تعجّل المتابعة دون إلغاء موعد أقرب كان مجدولًا؛ انتهاء الضغط أو رد AI يعجّل الخطوة التالية.
- تستمر حماية منع تكرار فتح الباب أو التأكيد على نفس الجولة؛ تقليل الانتظار لا يسمح بصرف مفتاحين على نفس الشاشة.
- لا يعيد التحقق من حساب واحد مسح نصوص الحساب الآخر. تظل القراءة البصرية مقصورة على نافذة الحساب المطلوب، وبفاصل لا يقل عن 600ms بين محاولات الالتقاط. لم تُلغَ ضوابط صلاحية الصورة أو فصل الحسابين.
- تُحلّل صيغة بنك الأسئلة المحفوظة مرة واحدة حتى يتغير محتواها؛ مطابقة السؤال الكامل واختياراته تستبدل البحث في كل تجميعات أسطر الشاشة عندما تكون قراءته كاملة.
- إصلاح تجاهل الاختيارات الرقمية، بما فيها الأرقام العربية والفارسية، ودعم صيغ مثل «بماذا»، «بمن»، «لمن»، «على يد من»، والأسئلة الواضحة المنتهية بعلامة استفهام.
- وجود إجابة قديمة للبنك خارج الاختيارات الحالية لا يحجب طلب AI. لا تُعتمد إجابة غير مؤكدة أو مطابقة ملتبسة تلقائيًا.
- الانتقال اليدوي لسؤال مختلف يلغي انتظار طلب السؤال القديم ويسمح بطلب السؤال الحالي دون تصفير عداد الطلبات أو استخدام الرد المتأخر.
- عند عدم اكتمال قراءة السؤال وأربعة اختيارات تظهر رسالة توضح ذلك. أخطاء AI وانخفاض الثقة وغياب السماح بالإجابة التلقائية تظل ظاهرة؛ سرعة خدمة AI وتحميل نسك لا يمكن ضمانها.

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

124 local tests passed (110 existing plus 14 new parser, fast-flow and AI recovery cases). Covers numeric choices in native/OCR text, Arabic/Persian numbers, previously unrecognized question forms, inherited clickable question nodes, incomplete/duplicate choice rejection, unusable bank answers falling back to AI, manual question changes while an old request is pending, budget preservation, bank cache invalidation, short tap debounce, and duplicate-submit protection after partial frames. A local 2,001-entry bank scenario completed ten question matches successfully; this is not a device speed benchmark. All existing two-account isolation and door-recovery tests also passed. Android Lint: 0 errors, one existing obsolete API guard warning. APK signature/update certificate, version metadata, minSdk=30 and ZIP/native alignment verified.

**No live Nusuk / Parallel Space device was available. The split-screen workflow, host package identity, screenshot permissions and actual taps still need verification on the user's device. Android 11+ is required; some clone apps may prevent accessibility or screenshots.**

SHA-256: `38a2acb71aaa26102fb6df8e0f3b063999c751705065ab62eb7a7357ce22020e`
