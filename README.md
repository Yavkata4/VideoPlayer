# VideoPlayer

RTSP Video Player (Kotlin, Jetpack Compose + ExoPlayer)

Lightweight RTSP player app built with Kotlin, Jetpack Compose, and AndroidX Media3 (ExoPlayer).
It provides fullscreen live video playback with rotation support, volume control, and a minimal overlay UI.

Features

✅ Plays RTSP stream (video + audio) using ExoPlayer Media3 RTSP.

✅ Fullscreen immersive mode (system bars hidden, swipe to show).

✅ Rotation preserves aspect ratio — no stretching.

✅ Overlay controls: Play / Pause and Volume slider (auto-hides after 3s, reappears on tap).

✅ Volume synced with hardware buttons and ExoPlayer volume.

✅ Simple splash screen before video loads.

✅ Works on Android 8.0 (API 26) and above.

How to run

Clone this repository.

Open in Android Studio (recommended) or build via command line:

./gradlew :app:assembleDebug


Install to your device:

adb install -r app/build/outputs/apk/debug/app-debug.apk

Usage / Testing

Open the app — splash screen appears briefly.

The player connects to the RTSP URL defined in MainActivity.

Tap screen to toggle the overlay.

Use the slider or hardware buttons to control volume.

Rotate device — video maintains correct aspect ratio.


<pre> \\\Project structure app/ ├── java/com/example/videoplayer/ │ ├── MainActivity.kt │ ├── SplashActivity.kt │ └── ui/theme/ ├── res/values/themes.xml └── AndroidManifest.xml \\\ </pre>
 


Screenshots-


<div style="display: flex; justify-content: space-between;">
  <img src="https://github.com/user-attachments/assets/44d006dc-1f4e-4bd6-8951-cf6f7e9f6a6a" width="49%" alt="Left image" />
  <img src="https://github.com/user-attachments/assets/7ffe091f-a138-479d-a5f5-077f30462b7b" width="49%" alt="Right image" />
</div>


<div style="display: flex; justify-content: space-between;">
  <img src="https://github.com/user-attachments/assets/427d8afa-d2b5-4e4d-9af4-0ce79262a8e1" width="49%" alt="Left image" />
  <img src="https://github.com/user-attachments/assets/60cb8530-07bc-41d8-a2dd-bc1ba5034687" width="49%" alt="Right image" />
</div>


<img width="2772" height="1280" alt="image" src="https://github.com/user-attachments/assets/82cc7c15-57a0-4000-bbb9-5d7ed18f36b7" />
<img width="2772" height="1280" alt="image" src="https://github.com/user-attachments/assets/40c6d5b3-049b-4bde-944a-5c6784e37348" />

-------------------------------------------------------
<img width="1661" height="577" alt="image" src="https://github.com/user-attachments/assets/0238e494-a4c9-4945-bc85-37dd4b8a49c0" />





AI tools used

ChatGPT (conversation exported as AI chat history.txt)

GitHub Copilot for small code suggestions

Notes

Min SDK: 26 (Android 8.0)

Target SDK: 34

Media3 (ExoPlayer) version: 1.4.1

Language: Kotlin + Jetpack Compose

Some Xiaomi / MIUI devices may log “no permission” messages for volume changes — this is a system quirk, not an app error.
