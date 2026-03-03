# XH505 Assistant — AI Dev System

نظام تطوير ذاتي مدعوم بالذكاء الاصطناعي يراقب المستودع، يحلل الكود، يولد توثيقًا تلقائيًا، ويحدّث README تلقائيًا عبر GitHub App.

## المزايا الرئيسية
- **Dashboard** لعرض حالة التطبيق وتحليلات AI.  
- **تحليل جودة الكود** مع درجة Static وAI.  
- **Call Graph** لعرض علاقات الاستدعاء بين الدوال.  
- **AI Auto Documentation** لتوليد توثيق دوال تلقائيًا.  
- **Security Scan** لفحص مشكلات الأمان الشائعة.  
- **Performance Analysis** لاكتشاف نقاط الاختناق.  
- **Design Patterns Detection** لاكتشاف الأنماط والتضادات.  
- رفع تلقائي إلى GitHub عبر GitHub App وWebhooks.

## المتطلبات
- Python 3.9+  
- مكتبات: `flask`, `pyjwt`, `requests`, `ast`, `psutil` (اختياري للأداء)  
- GitHub App مُعدّ ومفاتيح خاصة (Private Key) مضافة  
- مفتاح Gemini أو أي مزود AI محفوظ في متغير بيئة `GEMINI_KEY`  
- تشغيل على سيرفر عام (Replit / Render / Railway)

## كيفية التشغيل محليًا أو على Replit
1. أنشئ ملف `app.py` والصق كود الخادم.  
2. خزّن المفتاح الخاص داخل متغير بيئة أو ملف `secrets.py` غير مُضمَّن في الريبو.  
3. ضع `GEMINI_KEY` في متغير بيئة.  
4. شغّل: `python app.py` أو اضغط Run في Replit.  
5. ضع رابط السيرفر في إعدادات GitHub App → Webhook URL: `https://<your-host>/webhook`

## ملفات مهمة
- `app.py` — خادم Flask الرئيسي.  
- `README.md` — هذا الملف.  
- `quality_history.json` — (اختياري) سجل درجات الجودة عبر الزمن.

## ملاحظات أمان
- **لا تضع** أي توكن أو مفتاح داخل الكود في الريبو العام. استخدم متغيرات بيئة.  
- اسحب أي توكن تم تسريبه فورًا وأنشئ واحدًا جديدًا.

## سجل التغييرات
- الإصدار 1.0 — واجهة Dashboard، تحليلات AI، رفع تلقائي، صفحات Security/Performance/Patterns.
