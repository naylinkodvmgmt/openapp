# How to Decode APK

1. Install APK in Android Emulator
2. Check APK Path
3. Pull APK
4. Decode APK

### 1. Install APK in Android Emulator

1. Need to install Android Studio
2. Install Emulator

### 2. Check APK Path

#### 1. First, need to chek package Name

eg.

```bash
adb shell pm list packages | grep uab
# package:com.uab.uabbankpay
```

```bash
adb shell pm path com.uab.uabbankpay
# package:/data/app/.../com.uab.uabbankpay-XYZ==/base.apk
```

### 3. Pull APK

Afater pull, check base.apk file

```bash
adb pull /data/app/.../com.uab.uabbankpay-XYZ==/base.apk

```

### 4. Decode APK

First, already install apktool

```bash
apktool d base.apk -o uabbankpay_decoded
```
