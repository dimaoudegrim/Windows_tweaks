Disclaimer: I used Perplexity for summerize the titles or description in this readme.
In this repo I have 2 main files. One of them is a registry file that needs to open as administrator and also as the current user. the second file is a powershell for debloating some programs and needs to run as admin. 

I've seperated what each file does in this readme. while the first part is for the reg file, and the second part will include the script.

----------------
REGISTRY FILE:
----------------
Performance and Memory
Tweaking how Windows handles system memory and processor scheduling can make older hardware feel much faster. These changes prioritize the active applications you are using while stopping Windows from aggressively caching files or artificially delaying startup sequences.
*	Increases the icon cache size so Explorer renders icons faster without re-loading them.
*	Keeps the Windows kernel and drivers loaded in RAM instead of being swapped to the page file.
*	Removes the artificial startup delay that Explorer normally waits before loading.
*	Optimizes CPU time-slice scheduling to favor foreground and active applications over background processes.
*	Allocates more CPU time to multimedia tasks to reduce system responsiveness overhead.
*	Disables network throttling so multimedia apps get full network bandwidth.
*	Keeps the memory manager optimized for desktop app use rather than server-style file caching.
*	Disables Superfetch and Prefetcher to prevent Windows from pre-loading apps into RAM in the background.
*	Stops NTFS from recording the last-access timestamp on every file read to reduce disk writes.
*	Disables the creation of legacy 8.3 short filenames on NTFS for a small disk I/O improvement.
*	Sets the Font Cache service to start automatically so fonts load faster.
*	Reduces the menu popup hover delay to 100ms.
*	Sets games to high CPU scheduling priority and high storage I/O priority.
*	Increases the service startup pipe timeout to 30 seconds to give slower services more time to initialize.
Privacy and Telemetry
Telemetry refers to the background usage data Windows constantly sends back to Microsoft. Disabling these trackers and sync features helps protect your personal information, saves bandwidth, and stops your clipboard or typing habits from being uploaded to the cloud.
*	Disables telemetry to stop Windows from sending diagnostic and usage data to Microsoft.
*	Disables the Activity Feed and Timeline feature.
*	Stops user activities from being published or uploaded to Microsoft's servers.
*	Suppresses Windows feedback and survey notification popups.
*	Disables the advertising ID used to serve personalized ads for the system and all apps.
*	Turns off the per-user advertising ID and enforces advertising ID disablement through policy.
*	Disables location services system-wide and blocks individual apps from accessing location.
*	Disables the Connected User Experiences and Telemetry service (DiagTrack).
*	Disables the WAP Push Message Routing service used for telemetry delivery.
*	Disables the Windows performance counter logging and data collection service (PLA).
*	Prevents apps from running in the background.
*	Turns off app launch tracking so Windows stops recording program launch activity used by UserAssist.
*	Disables Windows settings sync across devices and prevents users from turning settings sync back on.
*	Disables Find My Device tracking.
*	Disables speech, inking, and typing personalization learning features that can store or upload data.
*	Turns off clipboard sync across devices and stops clipboard items from being uploaded to the cloud.
AI and Copilot Features
Microsoft has deeply integrated generative AI into recent Windows updates. These tweaks remove these AI overlays, background analysis services, and recall features to reclaim processing power and maintain complete control over your local data.
*	Disables Windows Copilot.
*	Disables the Click to Do AI overlay feature globally and for the current user.
*	Disables Windows AI Recall data analysis and prevents it from being available or enabled on the device.
*	Disables the Windows AI Fabric service entirely.
Search and Cortana
The default Windows search box often searches the internet via Bing, slowing down results when you just want to find a local file. These modifications force the search bar to stick to your local hard drive and turn off resource-heavy digital assistants.
*	Disables Cortana entirely.
*	Disables Bing-powered web results in the Start menu search.
*	Removes live suggestions that appear while typing in the search box.
*	Prevents Windows Search from reaching out to the web in any context, including metered connections.
*	Disables the animated and expanding search box on the taskbar.
*	Hides Search on the taskbar for the current user and enforces that choice through policy.
User Interface Experience
Modern Windows includes heavy visual effects and forced layouts that can slow down navigation. These registry edits restore classic, snappy menus, disable unnecessary widgets, and remove promotional clutter from your Start menu.
*	Removes the lock screen so the system goes straight to the login prompt.
*	Disables Windows AutoRun for all drive types.
*	Forces the classic Control Panel instead of the modern Settings app.
*	Restores the classic right-click context menu in Windows 11 by removing the "Show more options" step.
*	Removes the Chat and Teams button from the taskbar.
*	Disables the acrylic blur effect on the login screen.
*	Disables News and Interests or Widgets on the taskbar.
*	Stops tracking recently opened programs in the Start menu.
*	Enables Aero Shake to minimize windows by shaking them.
*	Shows verbose status messages during Windows startup and shutdown.
*	Hides the Recommended section in the Windows 11 Start menu and enforces this via device policy.
Consumer Cloud Promotions
Windows often treats the lock screen, Action Center, and Start menu as billboards for suggested apps and "fun facts." Disabling these Spotlight and consumer features provides a much cleaner, distraction-free desktop environment.
*	Disables Windows Consumer Features like suggested and sponsored apps in Start.
*	Disables soft landing feature highlight tips.
*	Disables consumer account state content promotions.
*	Disables the Suggested Settings prompts in the system.
*	Disables all Windows Spotlight features, desktop backgrounds, and collections.
*	Disables Windows Spotlight lock-screen tips, fun facts, and similar overlay content.
*	Disables Spotlight content in the Windows welcome experience.
*	Disables third-party suggestions and promotions in Windows.
*	Disables multiple Windows suggested and promotional content flags associated with Start suggestions.
*	Disables Spotlight suggestions in Action Center and notifications.
Network and Connectivity
These tweaks manage how your computer talks to other devices and handles network states. By limiting idle power-downs and background sharing services, you ensure your active network connection remains stable and private.
*	Enables TCP window scaling (RFC 1323) for better throughput on high-speed and high-latency connections.
*	Prevents the network adapter from entering idle power-down mode.
*	Sets Delivery Optimization to a specific download sharing mode.
*	Turns Nearby Sharing off.
*	Disables Phone-PC linking and Phone Link integration at the system policy level and for the current user.
App Specific Tweaks
Web browsers and office suites come with their own background startup routines and telemetry. These modifications stop Microsoft Edge and Office from connecting to external servers or launching before you actually need them.
*	Disables the news and content feed on the Edge new tab page and hides top sites.
*	Disables Edge startup boost and pre-launch at Windows startup.
*	Puts Office into a more disconnected and privacy-restricted mode.
*	Disables connected user content features in Office.
*	Prevents Office from downloading online content.
Security and Remote Access
By turning off remote connection protocols and automated error reporting, you close off potential entry points for attackers and stop crash dumps (which can sometimes contain sensitive memory contents) from leaving your machine.
*	Disables Remote Desktop connections to block all incoming RDP.
*	Disables Windows Error Reporting so no crash reports are sent to Microsoft.
Background Services Disabled
Windows runs dozens of hidden services meant to support everything from fax machines to smart cards. Turning off these niche services frees up valuable system resources for users who only need a standard gaming or workstation environment.
*	SysMain (Superfetch) RAM pre-loading service.
*	Windows Search file indexing service.
*	Fax service.
*	Geolocation (lfsvc) service.
*	Parental Controls monitor service.
*	Retail Demo mode service.
*	All Xbox Live services (Auth, Game Save, Networking, Accessory, Game Monitoring).
*	SNMP Trap service.
*	Windows Insider Service.
*	Mobile Hotspot service.
*	Phone Link service.
*	AllJoyn Router service for IoT device communication.
*	Windows Media Player Network Sharing service.
*	BranchCache and Peer Distribution service.
*	Smart Card Removal Policy service.
*	Wallet service.
*	Network Data Usage (Ndu) monitoring service.
*	PIM Index Maintenance service.


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
