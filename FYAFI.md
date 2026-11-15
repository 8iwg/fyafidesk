# FyafiDesk — نسخة فيافي من RustDesk

نسخة معدّلة من [RustDesk](https://github.com/rustdesk/rustdesk) ، وسم 1.4.9 (رخصة AGPL-3.0، انظر LICENCE).

التعديلات:
- `fyafi.json` + `src/common.rs`: إعداد مدمج (خادم 95.111.244.218 ومفتاحه، اسم FyafiDesk، إخفاء الحساب ودفتر العناوين، إيقاف التحديث التلقائي).
- أيقونات وشعار فيافي (`res/`, `flutter/assets/`, `flutter/macos/Runner/AppIcon.icns`, `flutter/windows/runner/resources/app_icon.ico`).
- لون الثيم الطيني `#AD6237` في `flutter/lib/common.dart`.
- `.github/workflows/fyafi-build.yml`: بناء Windows x64 (MSI) وmacOS arm64 (DMG).

البناء: Actions ← "Build FyafiDesk" ← Run workflow.

لماذا 1.4.9 مو 1.5.x؟ عملاء 1.5.x يطلبون مصافحة تشفير جديدة (KeyExchange/WebRTC) مع hbbs/hbbr، وسيرفر OSS 1.1.16 ما يدعمها، فالـrelay يفشل بـ«deadline has elapsed».
التعديلات تنطبق بـ tools/apply_fyafi.py على أي شجرة RustDesk.
