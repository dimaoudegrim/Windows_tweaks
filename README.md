Disclaimer: I used Perplexity for summerize the titles or description in this readme.
In this repo I have 2 main files. One of them is a registry file that needs to open as administrator and also as the current user. the second file is a powershell for debloating some programs and needs to run as admin. 

I've seperated what each file does in this readme. while the first part is for the reg file, and the second part will include the script.

----------------
-REGISTRY FILE:-
----------------

-----Performance & Memory-----
*	Increases the icon cache size so Explorer renders icons faster without re-loading them
*	Keeps the Windows kernel and drivers loaded in RAM instead of being swapped to the page file
*	Removes the artificial startup delay that Explorer normally waits before loading
*	Optimizes CPU time-slice scheduling to favor foreground/active applications over background processes
*	Allocates more CPU time to multimedia tasks (reduces system responsiveness overhead)
*	Disables network throttling so multimedia apps get full network bandwidth
*	Keeps the memory manager optimized for desktop app use rather than server-style file caching
*	Disables Superfetch and Prefetcher, preventing Windows from pre-loading apps into RAM in the background
*	Stops NTFS from recording the last-access timestamp on every file read — reduces disk writes
*	Disables creation of legacy 8.3 short filenames on NTFS — small disk I/O improvement
*	Sets the Font Cache service to start automatically, so fonts load faster
*	Reduces the menu popup hover delay to 100ms
*	Sets games to high CPU scheduling priority and high storage I/O priority

-----Search & Cortana-----
*	Disables Cortana entirely
*	Disables Bing-powered web results in the Start menu search
*	Removes live suggestions that appear while typing in the search box
*	Prevents Windows Search from reaching out to the web in any context, including metered connections
*	Disables the animated/expanding search box on the taskbar

-----Privacy & Telemetry-----
*	Disables telemetry — stops Windows from sending diagnostic/usage data to Microsoft
*	Disables the Activity Feed and Timeline feature
*	Stops user activities from being published or uploaded to Microsoft's servers
*	Suppresses Windows feedback/survey notification popups
*	Disables the advertising ID used to serve personalized ads, both for the system and all apps
*	Disables location services system-wide and blocks individual apps from accessing location
*	Disables the Connected User Experiences and Telemetry service (DiagTrack)
*	Disables the WAP Push Message Routing service used for telemetry delivery
*	Disables Windows performance counter logging and data collection service (PLA)
*	Prevents apps from running in the background

-----AI & Copilot-----
*	Disables Windows Copilot
*	Disables the "Click to Do" AI overlay feature
*	Disables Windows AI (Recall) data analysis
*	Disables the Windows AI Fabric service entirely

-----Windows Services (Disabled)-----
*	SysMain (Superfetch) — RAM pre-loading service
*	Windows Search — file indexing service
*	Fax service
*	Geolocation (lfsvc) service
*	Parental Controls monitor service
*	Retail Demo mode service
*	All Xbox Live services (Auth, Game Save, Networking, Accessory, Game Monitoring)
*	SNMP Trap service
*	Windows Insider Service
*	Mobile Hotspot service
*	Phone Link service
*	AllJoyn Router service (IoT device communication)
*	Windows Media Player Network Sharing service
*	BranchCache / Peer Distribution service
*	Smart Card Removal Policy service
*	Wallet service
*	Network Data Usage (Ndu) monitoring service

-----UI & Shell-----
*	Removes the lock screen — goes straight to the login prompt
*	Disables Windows AutoRun for all drive types
*	Forces the classic Control Panel instead of the modern Settings app
*	Restores the classic right-click context menu in Windows 11 (removes the "Show more options" step)
*	Removes the Chat/Teams button from the taskbar
*	Disables the acrylic/blur effect on the login screen
*	Disables "News and Interests" / Widgets on the taskbar
*	Stops tracking recently opened programs in the Start menu
*	Enables Aero Shake (window minimize by shaking)
*	Shows verbose status messages during Windows startup and shutdown

-----Privacy — Windows Cloud & Consumer Features-----
*	Disables Windows Consumer Features (suggested/sponsored apps in Start)
*	Disables "soft landing" feature highlight tips
*	Disables consumer account state content promotions
*	Disables the "Suggested Settings" prompts in the system

-----Remote Desktop & Security-----
*	Disables Remote Desktop connections (blocks all incoming RDP)
*	Disables Windows Error Reporting — no crash reports sent to Microsoft

-----Edge Browser-----
*	Disables news/content feed on Edge's new tab page and hides top sites
*	Disables Edge's startup boost and pre-launch at Windows startup

-----Network-----
*	Enables TCP window scaling (RFC 1323) for better throughput on high-speed/high-latency connections
*	Prevents the network adapter from entering idle power-down mode
*	Sets Delivery Optimization to a specific download sharing mode
*	Increases the service startup pipe timeout to 30 seconds, giving slower services more time to initialize


---------------------
-SCRIPT FOR DEBLOAT--
---------------------
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
