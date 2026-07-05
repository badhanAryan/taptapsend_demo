# Tap Tap Send — prototype

A UI prototype of a Germany → Bangladesh remittance app (no real payments).
Includes a PIN lock screen, home dashboard, the signature tap-tap send flow,
a full scrollable Activity history (your real 69 transfers), a Referrals
screen, and a Lock configuration in Settings.

Files (keep them all in the SAME folder):
- index.html — the whole app
- manifest.webmanifest — makes it installable
- icon-180.png, icon-192.png, icon-512.png, icon-maskable-512.png — icons

Demo passcode: 1234 (or tap the Face ID button on the lock screen).

--------------------------------------------------------------------
INSTALL ON IPHONE 14 PRO — STEP BY STEP
--------------------------------------------------------------------
Opening the files straight from the Files app will NOT give the full app
feel — they must be served over https. GitHub Pages is the easiest free
way, and you have used it before.

A) Publish with GitHub Pages
 1. On a computer, go to github.com and create a new PUBLIC repository,
    e.g. taptap-send.
 2. Click "Add file -> Upload files". Drag in ALL of these:
    index.html, manifest.webmanifest, and the four icon-*.png files.
    index.html must be at the top level (not inside a subfolder).
 3. Click "Commit changes".
 4. Go to the repo's Settings -> Pages.
 5. Source = Deploy from a branch, Branch = main, Folder = / (root), Save.
 6. Wait ~1 minute. A live URL appears, like
    https://<your-username>.github.io/taptap-send/

B) Add it to the iPhone home screen
 7. On the iPhone 14 Pro, open that URL in SAFARI (only Safari works here).
 8. Tap the Share button (square with an up arrow, bottom center).
 9. Scroll down and tap "Add to Home Screen".
10. Keep the name "Tap Tap Send" and tap Add (top right).
11. Close Safari and open the new Tap Tap Send icon. It launches full-screen
    with no browser bars — like a native app.

C) Test before you submit
 - Unlock with passcode 1234 (or the Face ID button).
 - Home: check the balance and "Send again" recipients.
 - Activity: scroll the full history; try the search box (type "wasif").
 - Tap any transfer to open its receipt.
 - Send flow: center button -> enter amount -> pick recipient -> Review ->
   double-tap the big green "tap . tap" button -> success. The new transfer
   appears at the top of Activity as "Today".
 - Settings (gear icon, top-right of Home): try Lock configuration — change
   passcode, Face ID toggle, require-passcode-to-send, auto-lock timing.
   To wipe changes before your demo: Settings -> Reset demo data.
 - Referrals tab: Copy code / Share invite.

--------------------------------------------------------------------
EDIT THE DATA LATER
--------------------------------------------------------------------
Open index.html and find the block marked "DEMO DATA". Edit RAW_TX
(each row is [name, amount, "ok"/"fail"/"pend", "YYYY-MM-DD"]) and
RECIP_META for recipient cities/methods. The home total and transfer count
recompute automatically. Save and re-upload to GitHub.
