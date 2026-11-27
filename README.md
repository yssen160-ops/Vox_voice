# Voxa Gateway Test

واجهة عربية ثابتة لاختبار Voxa حصراً عبر Cloudflare Worker.

## النشر

ينشر ملف `index.html` تلقائياً إلى GitHub Pages عند الدفع إلى فرع `main`
باستخدام سير العمل `.github/workflows/pages.yml`. يجب أن يكون مصدر GitHub
Pages مضبوطاً على **GitHub Actions** من إعدادات المستودع (Settings → Pages).

## الأمان وحدود التشغيل

- أدخل مفتاح المشروع في الواجهة عند الاستخدام؛ لا يُحفظ في التخزين المحلي أو
  ضمن ملفات الموقع، ويُرسل كـ `Authorization: Bearer <key>`.
- نقطة `/api/play` تعيد رابط `player_url` للمشغل، ولا تعيد ملفاً صوتياً جاهزاً.
- لا تنفذ الواجهة توليداً صوتياً محلياً ولا تضيف مزوداً آخر.
