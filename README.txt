TRAINING TIMER APP - SETUP STEPS
================================
Files in this package (keep them together, all in the top level of your GitHub repo):
  index.html, manifest.webmanifest, sw.js, icon-192.png, icon-512.png, icon-maskable-512.png, .nojekyll

PART A - PUT IT ON GITHUB PAGES (free hosting)
1. Make a free account at github.com (or sign in).
2. Tap + (top right) > New repository.
   Name it EXACTLY:  yourusername.github.io   (your GitHub username, all lowercase)
   Set it to Public. Leave the other boxes unchecked. Tap Create repository.
3. On the empty repo page tap "uploading an existing file". Unzip this package first, then
   select every file in it (index.html, manifest.webmanifest, sw.js and the three icon PNGs).
   Tap Commit changes.
4. Add the hidden file: Add file > Create new file. Name it  .nojekyll  , type a single space
   in the editor, and Commit changes.
5. Open Settings > Pages. Under "Build and deployment" choose Source: Deploy from a branch,
   Branch: main, Folder: / (root). Tap Save.
6. Wait 1 to 2 minutes, refresh Settings > Pages. Your app address appears at the top:
   https://yourusername.github.io/
   Open it in Chrome on your phone to make sure the timer loads.

PART B - INSTALL IT STRAIGHT FROM CHROME (quickest, no APK)
7. In Chrome on the phone open your address, tap the 3-dot menu, then Install app
   (or Add to Home screen > Install).
8. Open it from the new icon. It runs in its own window with no address bar, shows up
   in the recent-apps screen, and works in split-screen.

PART C - MAKE AN APK WITH PWABUILDER (free)
9. Go to pwabuilder.com, paste https://yourusername.github.io/ and tap Start. Wait for the report.
10. Tap Package for stores > Android. Fill in:
      App name: Training Timer      Package ID: io.github.yourusername.timer
      Version: 1                    Signing key: New (let it generate one)
    Tap Generate / Download. You get a ZIP.
11. Unzip it. Keep the whole ZIP somewhere safe (it holds your signing key, needed for updates).
    Find the .apk file and the assetlinks.json file.
12. FULL SCREEN STEP - without this the app shows a browser bar at the top:
    In your GitHub repo choose Add file > Create new file. In the name box type
    .well-known/assetlinks.json   (typing the slash makes the folder).
    Paste the contents of the assetlinks.json from the ZIP and Commit changes.
13. Copy the .apk to your phone (Drive, USB or email it to yourself). Tap it. If Android asks,
    allow "Install unknown apps" for the app you opened it from. Install.
14. Open the app. It should fill the window with no browser bar. Try it in split-screen.

UPDATING LATER
Replace index.html in your repo (Add file > Upload files, same name). Close and reopen the app
twice and it picks up the new version. The APK itself never needs reinstalling.

NOTES
- Your shuffle and length choices are saved on the device only.
- The page is public on the web, but it holds no personal data.
- Screens on GitHub and PWABuilder change now and then, so button names may differ a little.
