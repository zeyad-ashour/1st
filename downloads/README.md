# Nusuk Quiz Assistant — 1.2.1

[Download APK 1.2.1](https://github.com/zeyad-ashour/1st/raw/refs/heads/apk-download/downloads/NusukQuizAssistant-1.2.1.apk)

Android 11+; ARM64/x86_64. Debug/test APK. Same signing certificate as 1.2.0/1.1.1; update without uninstalling to retain the bank and encrypted device-local key.

## إصلاح Gemini

1. حدّث التطبيق دون حذفه.
2. افتح إعدادات الذكاء الاصطناعي واضغط **ضبط Gemini تلقائيًا**.
3. إذا كان مفتاح Gemini محفوظًا، اترك خانة المفتاح فارغة ولا تحدد حذف المفتاح. لا ترسل المفتاح في المحادثة.
4. اضغط **تحميل نماذج Gemini المتاحة** واختر نموذج Flash نصيًا من القائمة التي ترجعها Google لمفتاحك. النموذج الافتراضي gemini-flash-latest؛ لا تعتمد على أسماء قديمة يدويًا.
5. اضغط **حفظ واختبار الاتصال**. إذا فشل، الرسالة الجديدة توضح HTTP/status وفئة السبب دون طباعة المفتاح أو جسم خطأ الخادم.

التطبيق يتعرف أيضًا على روابط Google القديمة من نوع generateContent أو openai/chat/completions ويستخدم Gemini الأصلي حسب اسم النموذج المضبوط. يرسل المفتاح في x-goog-api-key وليس الرابط، ويستخدم GenerateContent JSON وJSON responseSchema. يوجد تمييز بين مفتاح غير صالح، وقيود المفتاح/المشروع، ونموذج غير متاح، وحصة مستنفدة أو خطأ صيغة. لا يوجد مفتاح مشترك أو خدمة مجانية مضمونة داخل APK.

## Automation

Verified local answers work offline. Optional AI sends only the question and four choices to the configured service. Enable accessibility, floating assistance and auto mode. Automatic AI answers require a separate opt-in; unverified guesses are not trusted offline until explicit correct-result evidence or manual approval. Fresh-screen option matching, request budgets/backoff, select-confirm-next/replay and duplicate-submit guards are retained. A model confidence estimate is not a correctness guarantee.

## Actual validation

69 local tests passed; Android Lint zero issues. Includes 11 native Gemini HTTPS/mock tests, 30 AI/flow tests, four UI/storage tests and 24 core tests. APK signature and ZIP/native 16 KB alignment verified. **No live Google account/key was available in this environment; your real key and model availability must be tested on your device.** Six device tests were compiled only; real Nusuk OCR/gestures/Keystore behavior is not certified.

SHA-256 1.2.1: `66beb946e5d1473ff54bfb98116cb5e92886993dea4ac09487ca6e97a2b7b33a`
