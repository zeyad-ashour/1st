# Nusuk Quiz Assistant — 1.3.1

[Download APK 1.3.1](https://github.com/zeyad-ashour/1st/raw/refs/heads/apk-download/downloads/NusukQuizAssistant-1.3.1.apk)

Android 11+; ARM64/x86_64. Debug/test APK. Same signing certificate as 1.3.0; install as an update without uninstalling to preserve the current bank and device-local encrypted API key.

## تصدير البنك الحالي

1. اضغط **تصدير بنك الأسئلة الحالي** من الرئيسية أو إدارة البنك.
2. اختر مكان الحفظ واضغط حفظ. الاسم المقترح: nusuk-bank-export.json.
3. الملف يشمل جميع الأسئلة والإجابات الحالية، المعتمدة وغير المعتمدة، وحالة الاعتماد والمصدر والثقة. لا يشمل إعدادات AI أو المفتاح. لا يتم رفعه تلقائيًا.
4. يمكن نقله لجهاز آخر واستيراده عبر زر الاستيراد. عند الاستيراد تظل مراجعة الاعتماد مطلوبة؛ لا تُوثق حقول verified الواردة من ملف خارجي تلقائيًا.

## استيراد بنك أسئلة

[Prepared bank ZIP download](https://github.com/zeyad-ashour/1st/raw/refs/heads/apk-download/downloads/nusuk-question-bank.zip)

استخرج ملف JSON من ZIP ثم اختر **استيراد بنك أسئلة من ملف**. راجع الجديد والمكرر والمتعارض، ثم احفظ. يمكن اعتماد الدفعات المعروضة حتى 150 سؤالًا بعد مراجعتها؛ وإلا تحفظ كاقتراحات. الصيغة قائمة JSON من عناصر question/answer أو q/a، UTF-8، بحد 2 ميجابايت و10000 سجل. المكرر لا ينشئ نسخًا إضافية والمتعارض لا يستبدل الإجابات الحالية. الإجابات المعتمدة المطابقة تستخدم البنك قبل AI.

## Actual validation

89 local tests passed, including five export tests covering current trusted/untrusted/rejected records, Arabic and quoted-text UTF-8 round trip, re-import trust handling, non-mutation, empty banks and Android Create Document intent; nine import/preview tests remain passing. Android Lint: zero issues. APK signature, matching update certificate, version metadata, and ZIP/native 16 KB alignment verified. No real Android device/file-provider or live Gemini key was used for these checks.

SHA-256 1.3.1: `1b29a4fe61852f48d0145d4b75f49a727367df98aa415e4da2e5080a72c0fd64`
