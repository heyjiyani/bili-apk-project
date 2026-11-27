BILI – build your own APK for free (works fully offline, including label reading)
==============================================================================
You do not need Android Studio or a computer program. GitHub builds it for you, free.

1. Make a free account at github.com and click "New repository" (name it bili, keep it Public).
2. Click "uploading an existing file" and drag in EVERYTHING from this folder
   (package.json, capacitor.config.json, build-apk.yml, README.txt, the www folder and the assets folder). Click "Commit changes".
3. Because phones/computers hide folders that start with a dot, create the build file by hand:
   Add file > Create new file. In the name box type:  .github/workflows/build-apk.yml
   Open the file build-apk.yml from this folder, copy all of it, paste it in, then click "Commit changes".
4. Click the "Actions" tab. Open "Build APK" > "Run workflow" > "Run workflow". Wait about 5-10 minutes for the green tick.
5. Open the finished run, scroll to "Artifacts", download "bili-apk", unzip it, and you get app-debug.apk.
6. Copy the APK to your phone, tap it, allow "Install unknown apps" when asked, and install.

Notes
- Label reading and everything else run on the phone with no internet.
- Lists are stored only on the phone. Use Overview > Save backup (copies text you can paste into Notes).
- To update later: change files in the repository, then run the workflow again and install the new APK over the old one.
- If the build shows a red cross, open the failed step, copy the error text and send it to Claude.
