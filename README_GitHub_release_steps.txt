SCALefy GitHub Release Steps

1) Create repository on GitHub:
   Scalefy

2) Upload these files to the repository main branch:
   - Scalefy_GitHub_Update.py
   - update.json
   - build_exe_scalefy.bat
   - Scalefy_installer.iss
   - icon.ico

3) IMPORTANT: replace YOUR_GITHUB_USERNAME in both files:
   - Scalefy_GitHub_Update.py
   - update.json

Example:
   https://raw.githubusercontent.com/stanislav/Scalefy/main/update.json
   https://github.com/stanislav/Scalefy/releases/latest

4) Build EXE:
   Put icon.ico in the same folder.
   Double click build_exe_scalefy.bat
   Result:
   dist\Scalefy.exe

5) Build installer:
   Open Scalefy_installer.iss in Inno Setup.
   Press Compile.
   Result:
   installer\Scalefy_Setup_v1.0.0.exe

6) Create GitHub Release:
   Tag: v1.0.0
   Upload:
   - Scalefy_Setup_v1.0.0.exe
   - Scalefy.exe optional

7) For next update 1.0.1:
   In Scalefy_GitHub_Update.py change:
   CURRENT_VERSION = "1.0.1"

   In Scalefy_installer.iss change:
   #define MyAppVersion "1.0.1"

   Build new installer and upload release v1.0.1.

   Then update update.json:
   {
     "version": "1.0.1",
     "url": "https://github.com/YOUR_GITHUB_USERNAME/Scalefy/releases/latest",
     "notes": "Describe what changed here."
   }

Users with old version will see DOWNLOAD UPDATE button.
