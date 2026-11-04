# Nusuk Quiz Assistant — 1.2.0

[Download APK 1.2.0](https://github.com/zeyad-ashour/1st/raw/refs/heads/apk-download/downloads/NusukQuizAssistant-1.2.0.apk)

Android 11+; ARM64 and x86_64. Test/debug APK signed with the same certificate as 1.1.1, so normal upgrade retains the local answer bank.

## الاستخدام

1. فعّل خدمة إمكانية الوصول والمساعدة العائمة من التطبيق.
2. فعّل الوضع التلقائي لاختيار الإجابة المحلية ثم «تحقق» و«السؤال التالي» أو إعادة اللعب عندما تظهر بوضوح.
3. جرّب السؤال المحلي أولًا. الضغط على النافذة العائمة يوقف الوضع التلقائي.
4. لإجابات AI الجديدة افتح «إعدادات الذكاء الاصطناعي». أدخل مفتاح OpenAI الخاص بك على الجهاز، أو رابط خادم HTTPS متوافق تملكه ويمكنه العمل بدون مفتاح. **بدون خدمة مضبوطة، لن يعمل AI على الأسئلة الجديدة؛ البنك المحلي يظل متاحًا.** لا يوجد مفتاح مشترك داخل APK.
5. فعّل اقتراحات AI، ثم السماح بإجابات AI التلقائية، واحفظ واختبر الاتصال. اختر حد الطلبات وتقدير الثقة المناسبين لك.
6. يُرسل نص السؤال والاختيارات الأربعة فقط، وليس الصور. API قد يستهلك رصيدًا. مفتاحك يُحفظ مشفرًا باستخدام Android Keystore، ولا يُرسل إلى GitHub.
7. اقتراحات AI تُحفظ غير مؤكدة. تُعتمد بعد نتيجة صحيحة واضحة أو مراجعتك اليدوية. ظهور نتيجة خاطئة لإجابة AI يوقف الوضع التلقائي للمراجعة. تقدير الثقة ليس ضمانًا للصحة.

## Validation

57 local tests passed (24 core, 30 AI/flow/network, 3 UI/storage). HTTPS integration used an isolated mock server, not a live AI provider. Android Lint: zero issues. APK v2 signature, ZIP/native 16 KB alignment and OCR assets verified.

Actual Android device OCR, accessibility gestures, overlay, Keystore execution and real Nusuk compatibility remain unverified for this release. The six device tests were compiled only. No live AI provider/key was available. The app recognizes specific Arabic control labels and pauses on unclear layouts; alternate/inline result UIs may need adaptation.

Previous offline-only build: [1.1.1](https://github.com/zeyad-ashour/1st/raw/refs/heads/apk-download/downloads/NusukQuizAssistant-1.1.1.apk).

SHA-256 for 1.2.0: `09eb2f6d8fbe4161ef3530db4f47d07ffd147aa39f51b749256ced819f941e7d`
