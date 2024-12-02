## Simple fix to broken internet after using EZFN
**Explanation:**
EZFN creates a proxy for your computer that may not disable if the launcher crashes. This tutorial will help you fix your internet by disabling the proxy.

**Step 1:** Win + R and paste the following command: 
```batch
REG ADD "HKCU\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v ProxyEnable /t REG_DWORD /d 0 /f
```
Press Enter, and that’s literally it! This should disable the proxy that EZFN creates and will not prevent you from using EZFN in the future. The command also works in CMD.
