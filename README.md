<p align="center"><img src="https://raw.githubusercontent.com/AlZaabiXIV/sentinel-releases/main/icon.png" width="140"></p>

<h1 align="center">SENTINEL</h1>
<p align="center"><i>by Sinistero</i></p>
<p align="center"><b>Nothing moves without you knowing.</b></p>

Sentinel turns your PC's webcam (and your other cameras) into a security system. Arm it when you leave. If someone
moves in front of the PC or touches the keyboard or mouse, your phone gets an alert with a **snapshot and a
30-second clip**. Tap the alert to **watch live**, or **lock the PC** from your phone.

## ⬇️ Download

Go to **[Releases → Latest](https://github.com/AlZaabiXIV/sentinel-releases/releases/latest)**:

| | File | How |
|---|---|---|
| 🖥️ **Windows 10 / 11** | `Sentinel-Setup-X.Y.exe` | Run it. If Windows says *"Windows protected your PC"*, choose **More info → Run anyway**. |
| 📱 **Android 8+** | `Sentinel-Android-X.Y.apk` | Open it on your phone and allow **Install unknown apps** for your browser when asked. |

Both apps update themselves: when a new version comes out, they offer it when you open them.

## ✨ What it does

- 🛡️ **Arm / Disarm** from the PC, the tray icon or your phone, with a countdown so you can leave the room
- 📷 **All your cameras**: the built-in webcam, USB cameras and Wi-Fi cameras (RTSP)
- 🏃 **Motion alerts** with smart filters (ignores light flicker and tiny movements)
- 🎯 **Watch and ignore zones**: watch only your desk or the door, and ignore a monitor, TV or window (from the PC or the phone)
- ⌨️🖱️ **Touch alerts**: key presses, mouse moves and clicks (which keys were pressed is never recorded)
- 📸 **Snapshot + 30-second clips** for every alert (more clips follow while someone is still there)
- 👁 **Live view** from any camera, or all cameras at once, straight from your PC to your phone (encrypted, never saved)
- 🛡️ **Sentinel Shield**: a black screen with the Sentinel eye; keyboard and mouse blocked while your work keeps running behind it. A new PIN (or your phone's fingerprint) every time
- 🔒 **Lock / Unlock PC** from your phone: the real Windows lock screen, unlocked with your Windows password behind your fingerprint
- 🌙 **Close the screen**: screen off, PC keeps working; if anyone touches it, Sentinel locks it and alerts you
- 🖥️ **PC remote control** from the phone: volume, keyboard and mouse lock, open apps, screenshots, messages, sleep / restart
- 🔐 **App Lock** for the phone app: fingerprint or app PIN
- 🕓 **Timeline** of everything that happened
- 📹 **Video calls**: show your face full screen on the PC (it wakes up and locks), talk through the PC speakers even when muted, and hear the room
- 🕶️ **Stealth Arm** from the phone: the PC screens go black and stay black while the cameras keep watching
- 🎞️ **Recording while armed** in 1-minute clips, with your own quality, disk limit and auto-delete; play any minute on the PC or the phone
- 🤏 **Live view**: full screen, pinch-to-zoom, double-tap zoom
- 🔔 **Update notifications** on both apps

---

## 📱 Connect your phone (one-time setup)

Sentinel uses **your own free Firebase project** to reach your phone from anywhere. That way nobody else's
server ever sees your cameras. It's free (Spark plan, no card needed) and takes about 10 minutes.

### 1. Make a Firebase project
1. Open **[console.firebase.google.com](https://console.firebase.google.com)** and sign in with your Google account.
2. **Create a project** → name it, e.g. `my-sentinel` → you can turn Google Analytics **off** → **Create project**.

### 2. Turn on the Realtime Database
1. In the left menu: **Databases & Storage → Realtime Database → Create database**. (Older screens call the group *Build*.)
2. Pick a location (any is fine; *Belgium (europe-west1)* is closest to the UAE) → **Next**.
3. Choose **Start in locked mode** → **Enable**. (Sentinel installs its own security rules for you.)

### 3. Turn on anonymous sign-in (so only your paired phones can connect)
1. In the left menu: **Authentication** (inside the *Security* or *Build* group) → **Get started**.
2. **Sign-in method** tab → **Anonymous** → switch it **on** → **Save**.

### 4. Add the Android app and download `google-services.json`
1. Click the ⚙️ next to *Project Overview* → **Project settings**.
2. Under **Your apps**, click the **Android** icon.
3. **Android package name**: `com.sinistero.sentinel` (exactly like this) → **Register app**.
4. **Download google-services.json** → then just click **Next / Continue to console** (skip the SDK steps).

### 5. Download the service account key
1. Still in **Project settings** → **Service accounts** tab.
2. **Generate new private key** → **Generate key**. A `.json` file downloads.
3. ⚠️ Keep this file private: it's the key to your Firebase project.

### 6. Put the 2 files into Sentinel on your PC
1. Open Sentinel → **📱 Phone** → **📁 Add the 2 Firebase files…** → pick both downloaded files.
2. It connects by itself (or press **🔌 Connect**). You should see **✅ Connected**.

### 7. Pair your phone
1. Install the APK on your phone and open Sentinel.
2. On the PC: **📱 Phone → Show pairing code**.
3. On the phone: **Pair with my PC** → scan the code. Done ✅

Pair more phones (or your wife's 😉) the same way. Remove a phone any time in the PC's Phone page.

### Live view doesn't connect on some networks?
Most home Wi-Fi and mobile networks work straight away. If live view never connects on a very strict network
(some office Wi-Fi or mobile data), add a free TURN server in **📱 Phone → Advanced: TURN server**
(for example the free plan at metered.ca "Open Relay").

---

## ✉️ Questions, problems or ideas?

<p align="center"><a href="mailto:sinistero.digital.co@gmail.com?subject=Sentinel%20support"><b>✉️ Contact us</b></a></p>

---

## 🔐 Privacy

- Pictures, clips and settings stay **on your PC** and in **your own Firebase project**. Sinistero has no access to them.
- Live video goes **directly** from your PC to your phone, encrypted (WebRTC), and is never stored.
- Only phones you paired with the QR code can see or control your PC.
- Please only watch places you're allowed to watch, and let the people who live there know.

<p align="center">© 2026 Sinistero · Made in the UAE 🇦🇪</p>
