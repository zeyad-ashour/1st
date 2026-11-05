# Nusuk Quiz Assistant — 1.3.0

[Download APK 1.3.0](https://github.com/zeyad-ashour/1st/raw/refs/heads/apk-download/downloads/NusukQuizAssistant-1.3.0.apk)

Android 11+; ARM64/x86_64. Debug/test APK. Same signing certificate as 1.2.2; install as an update without uninstalling to preserve local answers and the encrypted device-local API key.

## استيراد بنك أسئلة

1. نزّل ملف البنك JSON على جهازك.
2. افتح التطبيق ثم **استيراد بنك أسئلة من ملف** من الرئيسية أو إدارة البنك.
3. اختر الملف؛ راجع عدد الجديد والمكرر والمتعارض والسجلات غير الصالحة، ثم الأسئلة والإجابات.
4. اضغط **حفظ الأسئلة الجديدة** لاستيرادها كاقتراحات غير معتمدة. إذا راجعت كامل الدفعة المعروضة، يمكنك تحديد **راجعت إجابات الدفعة وأعتمد استخدامها محليًا** قبل الحفظ.
5. الإجابات المعتمدة تستخدم البنك المحلي قبل AI. المقترحات غير المعتمدة لا تُستخدم تلقائيًا دون مراجعة.

الصيغة قائمة JSON من عناصر question/answer (أو q/a). الحد 2 ميجابايت و10000 سجل، UTF-8. لا حاجة لصلاحية الوصول لكل الملفات؛ يتم اختيار ملف واحد عبر مدير الملفات. لا تُرسل بيانات الملف إلى AI. التكرار لا ينشئ نسخًا إضافية، والتعارض لا يستبدل إجابة موجودة. تُتجاهل علامات verified الواردة من الملف؛ الاعتماد قرار صريح داخل التطبيق. المعاينة لا تحفظ شيئًا قبل تأكيدك. الدفعات الأكبر من 150 سؤالًا تُستورد كاقتراحات للمراجعة.

The user's conversation files, extracted bank, and review report are not published in this repository or embedded in the APK. They are provided separately in the task conversation.

## Actual validation

84 local tests passed, including nine importer/preview tests covering the prepared 56-question fixture, malformed files, trust flags, duplicates, conflicts, preserving existing answers, idempotent imports, and explicit approval. Android Lint: zero issues. APK signature, matching update certificate, version metadata, and ZIP/native 16 KB alignment verified. No real Android device or live Gemini key was used for these checks.

SHA-256 1.3.0: `394944e0e338171c631638248358b0f87a93e0ff3c40eabe12d2a3dfe6c53d37`
