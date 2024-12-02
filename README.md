# How to fix broken internet after using EZFN Hybrid mode

**Explanation:**  
EZFN installs a certificate that can break your internet. I have no idea what causes this to break, but here's a fix:

1. **Step 1:** Press `Win + R` to open the run dialog and type `certmgr.msc`, then press Enter. This will open the certificate manager for Windows, allowing us to remove the installed certificate.
2. **Step 2:** In the sidebar, find `Trusted Root Certification Authorities`, open it, then open the subfolder `Certificates`.
3. **Step 3:** In the main window, find `EZFN - Hybrid (###)` (`###` will be some random numbers). You can make this easier by just pressing `E` after clicking in the main window until it highlights the right one.
4. **Step 4:** Right-click on the certificate and press delete. Just to be sure, restart your PC, though sometimes it's not required.

---

## Additional Note:

This should fix it but may break EZFN for future use. I personally have never had this problem, so I'm not sure if EZFN will ask you to reinstall the certificate if you want to use Hybrid again. If it doesn't, and you want to use it again, reinstall EZFN. Otherwise (again, untested if this works; the previously mentioned fix does, and that's all I tested), instead of deleting the certificate, you can try:

- Right-click on the certificate, press **Properties**, and then press **Disable all purposes for this certificate**.
- If you want to use EZFN Hybrid again later, press **Enable all purposes for this certificate**, and press **Apply** when done.
