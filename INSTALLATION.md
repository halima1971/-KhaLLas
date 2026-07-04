# 📱 KhaLLas ইনস্টলেশন গাইড

## প্রয়োজনীয় জিনিসপত্র (Prerequisites)

- Android Studio 4.2+
- Java JDK 11 or higher
- Gradle 7.0+
- Android SDK 21+
- Minimum 4GB RAM

---

## Windows এ APK তৈরি

### ধাপ 1: প্রজেক্ট সেটআপ
```bash
git clone https://github.com/your-username/khallas.git
cd khallas
```

### ধাপ 2: Gradle Sync করুন
1. Android Studio খুলুন
2. প্রজেক্ট খুলুন
3. `File` → `Sync Project with Gradle Files`
4. সাপেক্ষে অপেক্ষা করুন

### ধাপ 3: APK বিল্ড করুন
1. `Build` → `Build Bundle(s) / APK(s)` → `Build APK(s)`
2. বিল্ড সম্পন্ন হওয়ার জন্য অপেক্ষা করুন
3. APK লোকেশন: `app/build/outputs/apk/debug/app-debug.apk`

---

## Android ফোনে ইনস্টল করুন

### ধাপ 1: Developer Mode সক্রিয় করুন
1. `Settings` → `About Phone`
2. `Build Number` ৭ বার ট্যাপ করুন
3. Developer Mode সক্রিয় হয়েছে

### ধাপ 2: USB Debugging চালু করুন
1. `Settings` → `Developer Options`
2. `USB Debugging` চালু করুন
3. USB দিয়ে কম্পিউটারে সংযুক্ত করুন

### ধাপ 3: অ্যাপ ইনস্টল করুন
**Option A - Android Studio দিয়ে:**
```
Run → Run 'app' (Shift + F10)
```

**Option B - APK ফাইল দিয়ে:**
1. APK ফাইল ফোনে কপি করুন
2. Settings → Security → Unknown Sources চালু করুন
3. File Manager খুলুন
4. APK ট্যাপ করুন
5. Install করুন

---

## টেস্ট অ্যাকাউন্ট

| ক্ষেত্র | মান |
|------|------|
| **ইউজারনেম** | test1234 |
| **পাসওয়ার্ড** | password123 |

---

## সাধারণ সমস্যা এবং সমাধান

### ❌ Gradle Sync ব্যর্থ
```
সমাধান:
1. File → Sync Project with Gradle Files
2. কখনো কখনো Gradle cache clear করুন:
   - প্রজেক্ট folder এ .gradle/ delete করুন
   - Retry করুন
```

### ❌ APK বিল্ড ব্যর্থ
```
সমাধান:
1. Build → Clean Project
2. Build → Rebuild Project
3. যদি এখনও ব্যর্থ হয়:
   - Android SDK এর version চেক করুন
   - Java JDK এর version চেক করুন (11+)
```

### ❌ ইনস্টল ব্যর্থ: "Parse Error"
```
সমাধান:
1. Settings → Apps → Uninstall previous version
2. Settings → Security → Unknown Sources চালু করুন
3. পুনরায় ইনস্টল করুন
```

### ❌ ইনস্টল ব্যর্থ: "Insufficient Storage"
```
সমাধান:
1. ফোনে কিছু ফাইল delete করুন
2. কমপক্ষে 100MB ফ্রি স্পেস রাখুন
```

### ❌ অ্যাপ ক্র্যাশ হচ্ছে
```
সমাধান:
1. অ্যাপ আনইনস্টল করুন
2. ফোন রিবুট করুন
3. পুনরায় ইনস্টল করুন
```

---

## ডেভেলপমেন্ট টিপস

### সীরিয়াল মনিটর দেখুন
```bash
adb logcat
```

### ফোন থেকে ফাইল কপি করুন
```bash
adb pull /sdcard/Download/file.txt C:\Users\YourName\Desktop
```

### অ্যাপ পুনরায় চালু করুন
```bash
adb shell am force-stop com.khallas.app
adb shell am start -n com.khallas.app/.MainActivity
```

---

## সাহায্য পান

- 📧 ইমেইল: support@khallas.com
- 🐛 বাগ রিপোর্ট: [GitHub Issues](https://github.com/your-username/khallas/issues)
- 💬 আলোচনা: [GitHub Discussions](https://github.com/your-username/khallas/discussions)

---

**Madrchod Coding! 🚀**
