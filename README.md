# VMware Audio Fixes
This repo cotains modified audio drivers to reduce the chances of hearing popping/crackling on versions of Windows that use the NT 5.x kernel when installed in VMware without requiring the user to modify their host registry to enable GlobalTimerResolutionRequests. 

The mod does this by forcing the driver to use a notification timer of 20ms

## Compatible OSes

| Operating System | Compatible?
|---------|:-------:|
|Windows 2000 Service Pack 4|✅
|Windows XP RTM|❓
|Windows XP Service Pack 1|❓
|Windows XP Service Pack 2|❓
|Windows XP Service Pack 3|✅
|Windows Server 2003 Service Pack 2|✅

## Installation

### Windows 2000
1. Right click **"My Computer"** and click manage
2. Click **"Device Manager"**
3. Expand **"Sound, video and game controllers"** and double click on **"Creative AudioPCI (ES1371,ES1373) (WDM)"**
4. Click the Driver tab
5. Click **"Update Driver"**
6. Click **"Display a list of known drivers for this device"**
9. Click **"Has Disk..."**
10. Click **"Browse"**
11. Locate **"wdma_ens.inf"** and double click on the file
12. Click **"OK"**
13. Click **"Next"** 
14. Click **"Next"** again
14. Windows will say that the device does not contain a Microsoft digital signature, click **"Yes"**
15. Click finish
16. Click close
17. Reboot your machine
    
### Windows XP / Server 2003

1. Right click **"My Computer"** and click manage
2. Click **"Device Manager"**
3. Expand **"Sound, video and game controllers"** and double click on...:
    - **Windows XP:** "Creative AudioPCI (ES1371,ES1373) (WDM)"
    - **Windows Server 2003:** "VMware VMaudio (VMAUDIO) (WDM)"
5. Click the Driver tab
6. Click **"Update Driver"**
7. Click **"No, not this time"** when asked if Windows can connect to Windows Update
8. Click **"Install from a list or specific location"**
9. Click **"Don't search"**
10. Click **"Has Disk..."**
11. Click **"Browse"**
12. Locate and double click the appropriate driver INF file:
    - **Windows XP:** `wdma_ens.inf`
    - **Windows Server 2003:** `vmaudio.inf`
14. Click **"OK"**
15. Click **"Next"**
16. Windows will say that the device has not passed Windows Logo testing, click **"Continue Anyway"**
17. Click finish
18. Click close
19. Reboot your machine
