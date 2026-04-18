Registry  and powershell tweaks for windows to enhance performance, Responsiveness, Privacy, remove telemetry and AI, improve network performance, improve user experience and more. 

In this repo I have 2 main files. One of them is a registry file with 136 configuratinos that needs to open as administrator and also as the current user. 
The second file is a powershell for debloating 27 programs and needs to run as admin. 

I've seperated what each file does in this readme. while the first part is for the reg file, and the second part will include the script.
Disclaimer: I used Perplexity for summerize the titles or description in this readme.

----------------
REGISTRY FILE: 136 CONFIGURATIONS.
----------------
### 🚀 Performance & Responsiveness
- Launch folder windows in a separate process
- Keeps the Windows kernel and drivers loaded in RAM instead of being swapped to the page file.
- Removes the artificial startup delay that Explorer normally waits before loading.
- Optimizes CPU time-slice scheduling to favor foreground and active applications over background processes.
- Keeps the memory manager optimized for desktop app use rather than server-style file caching.
- Disables Superfetch and Prefetcher to prevent Windows from pre-loading apps into RAM in the background.
- Stops NTFS from recording the last-access timestamp on every file read to reduce disk writes.
- Disables the creation of legacy 8.3 short filenames on NTFS for a small disk I/O improvement.
- Sets the Font Cache service to start automatically so fonts load faster.
- Reduces the menu popup hover delay to 100ms.
- Increases the icon cache size so Explorer renders icons faster without re-loading them.
- Increases the service startup pipe timeout to 45 seconds to give slower services more time to initialize.
- Runs the Windows desktop and taskbar in a separate Explorer process

### 🎮 Gaming & Multimedia
- Allocates more CPU time to multimedia tasks to reduce system responsiveness overhead.
- Disables network throttling so multimedia apps get full network bandwidth.
- Sets games to high CPU scheduling priority and high storage I/O priority.

### 🛡️ Privacy, Telemetry & AI
- Disables telemetry to stop Windows from sending diagnostic and usage data to Microsoft.
- Disables the Activity Feed and Timeline feature.
- Stops user activities from being published or uploaded to Microsoft's servers.
- Suppresses Windows feedback and survey notification popups.
- Disables the advertising ID used to serve personalized ads for the system and all apps.
- Turns off the per-user advertising ID and enforces advertising ID disablement through policy.
- Disables location services system-wide and blocks individual apps from accessing location.
- Disables the Connected User Experiences and Telemetry service (DiagTrack).
- Disables the WAP Push Message Routing service used for telemetry delivery.
- Disables the Windows performance counter logging and data collection service (PLA).
- Prevents apps from running in the background.
- Turns off app launch tracking so Windows stops recording program launch activity used by UserAssist.
- Disables Windows settings sync across devices and prevents users from turning settings sync back on.
- Disables Find My Device tracking.
- Disables speech, inking, and typing personalization learning features that can store or upload data.
- Turns off clipboard sync across devices and stops clipboard items from being uploaded to the cloud.
- Disables Windows Copilot.
- Disables the Click to Do AI overlay feature globally and for the current user.
- Disables Windows AI Recall data analysis and prevents it from being available or enabled on the device.
- Disables the Windows AI Fabric service entirely.
- Disables Cortana entirely.
- Disables Windows Error Reporting so no crash reports are sent to Microsoft.

### 🔎 Search, Start & Interface
- Disables Bing-powered web results in the Start menu search.
- Removes live suggestions that appear while typing in the search box.
- Prevents Windows Search from reaching out to the web in any context, including metered connections.
- Disables the animated and expanding search box on the taskbar.
- Hides Search on the taskbar for the current user and enforces that choice through policy.
- Removes the lock screen so the system goes straight to the login prompt.
- Forces the classic Control Panel instead of the modern Settings app.
- Restores the classic right-click context menu in Windows 11 by removing the "Show more options" step.
- Removes the Chat and Teams button from the taskbar.
- Disables the acrylic blur effect on the login screen.
- Disables News and Interests or Widgets on the taskbar.
- Stops tracking recently opened programs in the Start menu.
- Enables Aero Shake to minimize windows by shaking them.
- Shows verbose status messages during Windows startup and shutdown.
- Hides the Recommended section in the Windows 11 Start menu and enforces this via device policy.
- Disables Windows Consumer Features like suggested and sponsored apps in Start.
- Disables soft landing feature highlight tips.
- Disables consumer account state content promotions.
- Disables the Suggested Settings prompts in the system.
- Disables all Windows Spotlight features, desktop backgrounds, and collections.
- Disables Windows Spotlight lock-screen tips, fun facts, and similar overlay content.
- Disables Spotlight content in the Windows welcome experience.
- Disables third-party suggestions and promotions in Windows.
- Disables multiple Windows suggested and promotional content flags associated with Start suggestions.
- Disables Spotlight suggestions in Action Center and notifications.

### 🌐 Network, Connectivity & Microsoft Features
- Enables TCP window scaling (RFC 1323) for better throughput on high-speed and high-latency connections.
- Prevents the network adapter from entering idle power-down mode.
- Sets Delivery Optimization to a specific download sharing mode.
- Turns Nearby Sharing off.
- Disables Phone-PC linking and Phone Link integration at the system policy level and for the current user.
- Disables the news and content feed on the Edge new tab page and hides top sites.
- Disables Edge startup boost and pre-launch at Windows startup.
- Puts Office into a more disconnected and privacy-restricted mode.
- Disables connected user content features in Office.
- Prevents Office from downloading online content.
- Disables Remote Desktop connections to block all incoming RDP.
- Disables Windows AutoRun for all drive types.

### 🧰 Disabled Services
- SysMain (Superfetch) RAM pre-loading service.
- Windows Search file indexing service.
- Fax service.
- Geolocation (lfsvc) service.
- Parental Controls monitor service.
- Retail Demo mode service.
- All Xbox Live services (Auth, Game Save, Networking, Accessory, Game Monitoring).
- SNMP Trap service.
- Windows Insider Service.
- Mobile Hotspot service.
- Phone Link service.
- AllJoyn Router service for IoT device communication.
- Windows Media Player Network Sharing service.
- BranchCache and Peer Distribution service.
- Smart Card Removal Policy service.
- Wallet service.
- Network Data Usage (Ndu) monitoring service.
- PIM Index Maintenance service.
---------------------
SCRIPT FOR DEBLOAT
---------------------
The script will uninstall the following apps:

* Clipchamp
* Bing News
* Bing Weather
* Xbox Gaming App
* Get Help
* Get Started / Tips
* Solitaire Collection
* People
* Power Automate Desktop
* Alarms & Clock
* Mail & Calendar
* Feedback Hub
* Maps
* Xbox overlays (3x)
* Phone Link
* Groove Music
* Movies & TV
* Family Safety
* Quick Assist
* Microsoft Teams (both versions)
* Cortana
* Copilot (app + sidebar)
* Outlook for Windows
* Internet Explorer
* Language Handwriting/OCR/Speech/TTS
* Tablet PC Math
* Steps Recorder
