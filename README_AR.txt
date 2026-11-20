ديوان عباس - مشروع Android APK
==============================

هذا مشروع Android Studio يحوّل ملف الموقع diwan_abbas.html إلى تطبيق أندرويد باسم «ديوان عباس».
الصفحة محفوظة داخل التطبيق، لذلك تعمل الواجهة والقصائد دون الحاجة إلى استضافة الموقع.
تخزين القصائد والنبذة يستخدم localStorage في WebView؛ لا تمسح بيانات التطبيق أو تحذفه قبل تصدير/نسخ قصائدك.
اتصال الإنترنت مطلوب فقط لتحميل خطوط Google Fonts الخارجية؛ سيعمل الموقع بخط بديل عند عدم توفره.

طريقة إنشاء APK:
1) نزّل Android Studio على كمبيوتر (Windows أو Mac أو Linux) من الموقع الرسمي:
   https://developer.android.com/studio
2) فك ضغط DiwanAbbasAndroid.zip.
3) افتح Android Studio ثم Open واختر مجلد DiwanAbbasAndroid.
4) انتظر اكتمال Gradle Sync وتنزيل مكونات Android SDK إذا طُلب ذلك.
5) من القائمة Build > Build Bundle(s) / APK(s) > Build APK(s).
6) بعد اكتمال البناء اضغط Locate في الإشعار. غالباً ستجد الملف هنا:
   app/build/outputs/apk/debug/app-debug.apk
7) انقل app-debug.apk إلى هاتف Android وافتحه، واسمح بالتثبيت من هذا المصدر إذا طلب الهاتف ذلك.

لإصدار APK نهائي قابل للتوزيع:
Build > Generate Signed Bundle / APK > APK، ثم أنشئ Keystore واحفظه وكلمات مروره بأمان.
لا تفقد ملف keystore؛ ستحتاجه لتحديث التطبيق بنفس هوية التوقيع.

ملاحظة:
- هذا المشروع لا يحتوي على APK جاهز؛ يجب بناؤه باستخدام Android Studio وAndroid SDK.
- القصائد محفوظة محلياً على الجهاز ولا تتم مزامنتها تلقائياً بين الأجهزة.

إنشاء APK من الهاتف فقط (باستخدام GitHub Actions):
1) أنشئ حساباً في https://github.com إن لم يكن لديك حساب.
2) أنشئ مستودعاً جديداً (New repository) باسم DiwanAbbas واجعله Public أو Private.
3) ارفع محتويات هذا المجلد إلى المستودع، مع الحفاظ على المجلدات كما هي.
4) افتح تبويب Actions في المستودع، واختر Build Diwan Abbas APK ثم Run workflow.
5) بعد نجاح البناء، افتح نتيجة التشغيل (workflow run)، وانزل إلى Artifacts، وحمّل Diwan-Abbas-APK.zip.
6) فك ضغط الملف على هاتفك، ثم افتح app-debug.apk وثبّته.
ملاحظة: هذه الطريقة تستخدم بناءً سحابياً؛ لا تحتاج Android Studio أو كمبيوتراً. قد تختلف أسماء الأزرار قليلاً حسب واجهة GitHub.
