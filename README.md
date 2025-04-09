# 📥 SharePoint Video Downloader & Transcriber (Windows)

This guide helps you **download a video from SharePoint** and **transcribe it** using Whisper AI on Windows.

---

## 🔧 Step 1: Install yt-dlp

1. Open **Command Prompt as Administrator**.
2. Run the following command:

   ```bash
   winget install --id yt-dlp.yt-dlp
  >  This will install both ***yt-dlp*** and ***ffmpeg***.
3. Close and reopen the terminal once the installation is complete.

## 🌐 Step 2: Get the Video URL from SharePoint

1. Open the SharePoint page containing the video.
2. Press **F12** to open the Developer Tools.
3. Go to the **Network** tab.
4. Press **F5** to reload the page.
5. In the filter bar, type:
   ```nginx
    videomanifest
6. Start playing the video.
7. A new network request will appear, starting with:
   ```nginx
    videomanifest?provider...
8. **Right-click** on that request and copy the full URL.


## ✂️ Step 3: Clean the URL
1. Paste the copied URL into a text editor (e.g., Notepad).
2. Press Ctrl+F and search for:
   ```perl
    index&format=dash
3. Delete everything after ***index&format=dash*** — from ***&altManifestMetadata*** to the end of the URL.

## 📥 Step 4: Download the Video
1. Open **Command Prompt** as **Administrator**.
2. Run the following command:
   ```bash
    yt-dlp "PASTE_YOUR_CLEANED_URL_HERE" -o DesiredFileName.mp4
  >Replace ***"PASTE_YOUR_CLEANED_URL_HERE"*** with your cleaned URL, and ***DesiredFileName*** with the name you want for your downloaded video.

## 📁 Step 5: Move the File
1. Once the download is complete, go to:
   ```makefile
   C:\Windows\System32
2. Locate your downloaded file.
3. Cut and paste it into a regular user folder (e.g., ***Documents*** or ***Desktop***) for easier access.

## 📝 Step 6: Transcribe the Video
To transcribe the downloaded video, use the simple Whisper AI script available in this repository.
