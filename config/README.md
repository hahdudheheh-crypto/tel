# Noor App - Remote Configuration

هذا المجلد يحتوي على ملفات الإعدادات البعيدة (Remote Config) لتطبيق نور.

## الملفات:

### 1. app_config.json
إعدادات التطبيق الأساسية:
- `share_link`: رابط مشاركة التطبيق (Google Play)
- `share_text`: نص المشاركة
- `latest_version`: آخر إصدار متاح
- `force_update`: إجبار المستخدم على التحديث
- `update_message`: رسالة التحديث
- `min_supported_version`: أقل إصدار مدعوم

### 2. announcements.json
الإعلانات والرسائل:
- `enabled`: تفعيل/تعطيل الإعلان
- `title`: عنوان الإعلان
- `message`: نص الإعلان
- `action_url`: رابط الإجراء (اختياري)
- `show_once`: عرض مرة واحدة فقط

## كيفية الاستخدام:

1. ارفع هذا المجلد على GitHub repository
2. اجعل الـ repository عام (public)
3. عدّل الرابط في `lib/services/remote_config_service.dart`:
   ```dart
   static const String _baseUrl = 'https://raw.githubusercontent.com/YOUR_USERNAME/noor-app-config/main/config';
   ```
4. استبدل `YOUR_USERNAME` باسم المستخدم الخاص بك

## ملاحظات:

- التطبيق يحفظ cache للإعدادات لمدة 24 ساعة
- يمكن تحديث الإعدادات في أي وقت بدون تحديث التطبيق
- التغييرات تظهر للمستخدمين خلال 24 ساعة كحد أقصى
