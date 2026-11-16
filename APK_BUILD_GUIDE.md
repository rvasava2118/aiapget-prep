# Guide: Packaging the AIAPGET Ayurveda App into an Android APK

Since you requested an APK file to test the application on your Android device, follow this step-by-step guide using **Capacitor** (the industry-standard tool by Ionic to turn web/PWA apps into native Android APKs).

---

### Prerequisites (Run in Termux or your PC terminal)
1. **Node.js & npm** installed.
2. **Android Studio** (if building locally on PC) or use free cloud builders like **Capacitor CLI**.

---

### Step 1: Initialize Project & Install Capacitor

Run these commands in your project directory (`/data/data/com.termux/files/home/ram-sita-hanuman`):

```bash
npm init -y
npm install @capacitor/core @capacitor/cli
npx cap init "AIAPGET Prep" "com.ayurveda.aiapget" --web-dir "."
```

---

### Step 2: Add Android Platform

```bash
npm install @capacitor/android
npx cap add android
```

---

### Step 3: Configure Anti-Screenshot & Security (Native Android)

To enforce strict screenshot prevention on Android (`FLAG_SECURE`), open `android/app/src/main/java/com/ayurveda/aiapget/MainActivity.java` and add the security flag in `onCreate`:

```java
package com.ayurveda.aiapget;

import android.os.Bundle;
import android.view.WindowManager;
import com.getcapacitor.BridgeActivity;

public class MainActivity extends BridgeActivity {
    @Override
    public void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        // Prevent screenshots and screen recording across the entire app
        getWindow().setFlags(WindowManager.LayoutParams.FLAG_SECURE, WindowManager.LayoutParams.FLAG_SECURE);
    }
}
```

---

### Step 4: Build & Generate APK

```bash
npx cap sync
cd android
./gradlew assembleDebug
```

Your debug APK will be generated at:
`android/app/build/outputs/apk/debug/app-debug.apk`

---

### Alternative: Instant PWA Installation (No APK needed)
You can open `aipget-prep.html` in Chrome on your Android phone, tap the menu (3 dots), and select **"Add to Home Screen"** or **"Install App"**. It will install just like a native app with full offline support and Google/WhatsApp login options.
