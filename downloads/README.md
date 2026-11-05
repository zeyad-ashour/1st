# Nusuk Quiz Assistant — 1.4.0

## اختر النسخة المناسبة

- [BlueStacks Nougat/Pie / Android 7+ APK](https://github.com/zeyad-ashour/1st/raw/refs/heads/apk-download/downloads/NusukQuizAssistant-1.4.0-Android7plus.apk): Android 7.0/API 24 or newer; no native ABI requirement, suitable for x86/ARM 32/64-bit environments. **Accessibility text reading, gestures, AI, local bank, import/export. No screenshot OCR in this compatibility variant.**
- [Android 11+ full OCR APK](https://github.com/zeyad-ashour/1st/raw/refs/heads/apk-download/downloads/NusukQuizAssistant-1.4.0-Android11.apk): ARM64/x86_64, includes the existing Arabic screenshot OCR.

Same package/signing certificate as earlier APKs. Debug/test builds. Install as an update to retain the bank and encrypted device-local key. For the user's P64 (Pie/Android 9) BlueStacks instance, use Android7plus rather than Android11.

## تجربة نسخة المحاكي

1. نزّل Android7plus APK واسحبه إلى نفس نافذة BlueStacks التي يعمل نسك داخلها، أو استخدم Install APK.
2. فعّل خدمة إمكانية الوصول للمساعد، ثم المساعدة العائمة. استورد البنك إن كان المحاكي جديدًا واضبط مفتاح AI محليًا.
3. جرّب السؤال المحلي أولًا، ثم افتح نسك وراقب قراءة السؤال. إذا كانت النصوص غير متاحة لإمكانية الوصول، ستوضح النسخة أن OCR غير متاح ولن تضغط على اختيار غير مقروء. لا تُضمن قراءة شاشة رسومية أو نسك نفسه داخل المحاكي دون اختبار فعلي.
4. الاختيار التلقائي يحتاج الزر 3 من الرئيسية. إجابات AI التلقائية تحتاج مفتاحًا منفصلًا في إعدادات AI.

The compatibility variant does not implement MediaProjection screenshot capture. This is an accessibility-first install/reading test, not a claim of legacy OCR support or emulator security compatibility.

## البنك المحلي

[Prepared bank ZIP](https://github.com/zeyad-ashour/1st/raw/refs/heads/apk-download/downloads/nusuk-question-bank.zip)

الاستيراد عبر JSON بعد استخراج ZIP؛ المكرر لا يُضاف والمتعارض لا يستبدل الإجابات الحالية. الاعتماد صريح بعد المراجعة. زر **تصدير بنك الأسئلة الحالي** يحفظ جميع الأسئلة والإجابات وحالة اعتمادها إلى ملف تختاره، دون مفتاح AI. إعادة الاستيراد تتطلب مراجعة الاعتماد ولا تثق تلقائيًا في حقول verified داخل الملفات.

## Actual validation

Compatibility: 95 local tests passed, including six SDK-specific test executions on Robolectric Android 7.0/API 24 and 7.1/API 25 covering Activity/insets/settings, service connection without loading native OCR libraries, gesture construction, and bank import/export. Full Android 11+ variant: 89 regression tests passed. Android Lint: no errors in either variant; compatibility has one unused-newer-attribute warning, standard has five obsolete-version-guard warnings. Both APK signatures and alignment checked; certificate matches earlier builds. Compatibility APK manifest minSdk=24 and contains no native .so libraries.

**No actual BlueStacks instance/device or live Gemini key was available. Installation and reading of Nusuk on the user's emulator remain to be tested.**

SHA-256:

- `NusukQuizAssistant-1.4.0-Android7plus.apk`: `f70e4d05c834968686305afe84a1be8063775d4695afffd675d387ec4a85f4af`
- `NusukQuizAssistant-1.4.0-Android11.apk`: `92f17fa1091da6ac08861d3b25b49a5a20a59d3c604ca3a67560baf47d78e7af`
