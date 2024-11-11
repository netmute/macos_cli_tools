# macOS-Only Command-Line Tools

A list of macOS-only command-line tools, including their functionalities, usage examples, and reasons you might want to use them.

## `afconvert` - Audio File Convert

**What it does:**  
`afconvert` is a command-line utility that converts audio files from one format to another. It supports various formats like AIFF, WAV, MP3, AAC, and more. It also allows you to modify audio properties such as sample rate, bit depth, and channels.

**Why use it:**  
If you need to batch-convert audio files, automate audio processing tasks, or prepare audio files for different devices and applications, `afconvert` provides a powerful way to script these conversions without using a GUI application.

**Usage example:**

- Convert an AIFF file to MP3:  
  `afconvert input.aiff -o output.mp3 -f MP3`

## `afinfo` - Audio File Info

**What it does:**  
`afinfo` displays detailed information about audio files, including format, duration, bit rate, sample rate, channels, and metadata.

**Why use it:**  
When managing audio libraries or processing audio files, you might need to verify file properties quickly. `afinfo` allows you to inspect these details directly from the terminal, which is helpful for scripting and automation.

**Usage example:**

- Display information about an audio file:  
  `afinfo song.m4a`

## `afplay` - Audio File Play

**What it does:**  
`afplay` plays audio files from the command line. It supports common audio formats and allows you to control playback options like volume and playback rate.

**Why use it:**  
If you're working in a terminal session and want to listen to audio files without opening a separate application, `afplay` lets you play sounds directly. It's also useful in scripts where you want to provide auditory feedback.

**Usage example:**

- Play an audio file:  
  `afplay notification.wav`

## `airport` - Manage Apple AirPort

**What it does:**  
`airport` is a command-line tool for managing Wi-Fi connections. It allows you to scan for wireless networks, connect to networks, display the status of the Wi-Fi interface, and adjust wireless settings.

**Why use it:**  
For troubleshooting Wi-Fi issues, automating network connections, or collecting Wi-Fi diagnostics, `airport` offers control over wireless interfaces without needing to navigate through system preferences.

**Usage example:**

- Scan for available Wi-Fi networks:  
  `airport -s`

## `asr` - Apple Software Restore

**What it does:**  
`asr` is used to clone disks and restore disk images to volumes. It performs block-level copying, which can be faster than file-level copying, and supports features like encryption and compression.

**Why use it:**  
When you need to deploy a standard system image across multiple Macs, backup a disk, or restore a system from a disk image, `asr` provides an efficient way to perform these tasks via scripting.

**Usage example:**

- Restore a disk image to a volume:  
  `sudo asr restore --source image.dmg --target /Volumes/TargetDrive --erase`

## `atsutil` - Font Registration System Utility

**What it does:**  
`atsutil` manages the Apple Type Services (ATS), including font caches. It can be used to reset font caches, verify font registrations, and troubleshoot font-related issues.

**Why use it:**  
If you're experiencing problems with fonts not displaying correctly, corrupted fonts, or system slowdowns due to font issues, `atsutil` can help resolve these by clearing and rebuilding font caches.

**Usage example:**

- Reset font caches:  
  `atsutil databases -remove`

## `automator` - Run an Automator Workflow

**What it does:**  
`automator` executes Automator workflows from the command line. Automator allows users to create custom workflows to automate repetitive tasks using a visual interface.

**Why use it:**  
Integrating `automator` into scripts enables you to automate complex tasks that involve GUI interactions, such as batch image processing or file organization, without manual intervention.

**Usage example:**

- Run an Automator workflow:  
  `automator /path/to/workflow.workflow`

## `bless` - Set Volume Bootability and Startup Disk Options

**What it does:**  
`bless` configures boot settings on macOS systems. It can set the startup disk, create bootable volumes, and modify boot configurations.

**Why use it:**  
When setting up dual-boot systems, creating bootable external drives, or managing startup configurations remotely, `bless` provides the necessary control over boot settings.

**Usage example:**

- Set the startup disk to a specific volume:  
  `sudo bless --mount /Volumes/BootVolume --setBoot`

## `caffeinate` - Prevent the System from Sleeping

**What it does:**  
`caffeinate` prevents your Mac from going to sleep. It can inhibit sleep indefinitely or for a specified duration, and it can target specific sleep behaviors like display sleep.

**Why use it:**  
Useful for ensuring long-running tasks, such as downloads, backups, or presentations, are not interrupted by the system entering sleep mode.

**Usage example:**

- Prevent sleep for 2 hours:  
  `caffeinate -t 7200`

## `chflags` - Change a File or Folder's Flags

**What it does:**  
`chflags` modifies special flags on files and directories, such as making them immutable (`uchg`), hidden, or append-only.

**Why use it:**  
To protect critical files from accidental modification or deletion, or to hide files from standard directory listings without changing permissions.

**Usage example:**

- Make a file immutable:  
  `chflags uchg important.doc`

- Remove the immutable flag:  
  `chflags nouchg important.doc`

## `codesign` - Create and Manipulate Code Signatures

**What it does:**  
`codesign` applies, verifies, and manages code signatures for applications and other code objects. Code signing is required for apps to pass macOS security checks like Gatekeeper.

**Why use it:**  
If you're a developer distributing software on macOS, `codesign` ensures your apps are properly signed, which is essential for user trust and compliance with macOS security policies.

**Usage example:**

- Sign an application with a development certificate:  
  `codesign -s "Developer ID Application: Your Name" /path/to/App.app`

## `createhomedir` - Create and Populate Home Directories

**What it does:**  
`createhomedir` generates home directories for user accounts that lack them, especially in networked or directory service environments.

**Why use it:**  
Administrators can automate the creation of home directories for new users, ensuring they have the necessary environment when they first log in.

**Usage example:**

- Create home directories for all users:  
  `sudo createhomedir -c`

## `csrutil` - Configure System Integrity Protection (SIP)

**What it does:**  
`csrutil` enables or disables System Integrity Protection, a security feature that restricts root-level access to critical system files.

**Why use it:**  
Developers or advanced users may need to disable SIP temporarily to install certain system-level software or perform troubleshooting tasks that require modifying protected areas.

**Usage example:**

- Disable SIP (requires recovery mode):  
  `csrutil disable`

- Enable SIP:  
  `csrutil enable`

## `cupsfilter` - Convert Files Using CUPS Filters

**What it does:**  
`cupsfilter` processes files using the CUPS (Common UNIX Printing System) filters, converting them into printer-ready formats.

**Why use it:**  
To convert documents to formats compatible with specific printers, or to process print jobs programmatically in custom printing workflows.

**Usage example:**

- Convert a PDF to a printer-specific format:  
  `cupsfilter -m printer/foo input.pdf > output.pcl`

## `diskutil` - Disk Utilities

**What it does:**  
`diskutil` manages disks and volumes on macOS. It can format, partition, verify, repair, mount, unmount, and erase disks.

**Why use it:**  
For tasks like preparing new disks, repairing disk errors, managing disk partitions, or scripting disk operations without using Disk Utility's GUI.

**Usage example:**

- List all disks and partitions:  
  `diskutil list`

- Erase a disk and format it as HFS+:  
  `diskutil eraseDisk HFS+ NewDiskName /dev/disk2`

## `ditto` - Copy Files and Folders

**What it does:**  
`ditto` copies files and directories, preserving metadata, resource forks, and extended attributes. It can also create archives and perform incremental backups.

**Why use it:**  
When `cp` isn't sufficient because it doesn't preserve all macOS-specific metadata, `ditto` ensures a faithful copy, making it ideal for backups and system migrations.

**Usage example:**

- Copy a folder and preserve metadata:  
  `ditto /source/folder /destination/folder`

## `dot_clean` - Remove Dot-Underscore Files

**What it does:**  
`dot_clean` merges or removes `.DS_Store` and `._` files, which store metadata on non-HFS+ file systems.

**Why use it:**  
To clean up unnecessary files that can cause clutter or compatibility issues when transferring files to other operating systems or devices.

**Usage example:**

- Clean up a USB drive:  
  `dot_clean /Volumes/USBDrive`

## `drutil` - Interact with CD/DVD Burners

**What it does:**  
`drutil` controls optical disc drives, allowing you to burn discs, erase rewritable media, eject or close the tray, and get drive status.

**Why use it:**  
For automating disc burning processes, managing discs in servers or kiosks, or controlling the drive without a GUI.

**Usage example:**

- Eject the disc tray:  
  `drutil tray eject`

- Burn an ISO image to disc:  
  `drutil burn image.iso`

## `dscacheutil` - Directory Service Cache Utility

**What it does:**  
`dscacheutil` interacts with the directory service cache, allowing you to query, flush, and monitor the cache.

**Why use it:**  
When experiencing issues with user authentication, DNS resolution, or directory services, flushing the cache can resolve outdated or corrupt data problems.

**Usage example:**

- Flush DNS cache:  
  `sudo dscacheutil -flushcache; sudo killall -HUP mDNSResponder`

## `dseditgroup` - Edit Groups

**What it does:**  
`dseditgroup` manages user groups in the directory services, enabling you to create, delete, and modify group memberships.

**Why use it:**  
Administrators can script group management tasks, such as adding users to groups or setting up permissions, essential for managing multi-user systems.

**Usage example:**

- Add a user to the admin group:  
  `sudo dseditgroup -o edit -a username -t user admin`

## `dsenableroot` - Enable Root Access

**What it does:**  
`dsenableroot` activates or deactivates the root user account on macOS.

**Why use it:**  
In situations where `sudo` is insufficient, enabling the root account allows for direct root login, though it should be used cautiously due to security risks.

**Usage example:**

- Enable the root user:  
  `sudo dsenableroot`

- Disable the root user:  
  `sudo dsenableroot -d`

## `dsmemberutil` - View User and Group Rights

**What it does:**  
`dsmemberutil` provides information about user and group memberships, UUIDs, and other directory service data.

**Why use it:**  
To verify group memberships, troubleshoot permission issues, or script checks on user access rights.

**Usage example:**

- Check if a user is in a group:  
  `dsmemberutil checkmembership -U username -G groupname`

## `dscl` - Directory Service Command Line

**What it does:**  
`dscl` is a powerful tool for interacting with directory services. It can read and modify directory data, manage users and groups, and perform advanced queries.

**Why use it:**  
For automating user and group management, scripting directory service interactions, and performing bulk operations in enterprise environments.

**Usage example:**

- List all local users:  
  `dscl . list /Users`

- Create a new user:  
  `sudo dscl . -create /Users/newuser`

## `execsnoop` - Snoop New Process Execution

**What it does:**  
`execsnoop` monitors and displays new processes as they are executed on the system, using DTrace.

**Why use it:**  
Useful for real-time monitoring of process execution, debugging, performance analysis, or security auditing to detect unexpected or malicious processes.

**Usage example:**

- Start monitoring process execution (requires sudo):  
  `sudo execsnoop`

## `fdesetup` - FileVault Setup Utility

**What it does:**  
`fdesetup` configures FileVault 2 encryption. It can enable or disable encryption, manage recovery keys, and add or remove authorized users.

**Why use it:**  
To automate the deployment of full-disk encryption across multiple systems, ensuring data security compliance in organizational environments.

**Usage example:**

- Enable FileVault:  
  `sudo fdesetup enable`

- Add a user to FileVault:  
  `sudo fdesetup add -usertoadd username`

## `fs_usage` - Filesystem Activity Monitor

**What it does:**  
`fs_usage` displays file system activity in real-time, showing system calls and page faults related to file operations.

**Why use it:**  
For diagnosing performance issues, monitoring application file usage, or identifying processes causing high disk activity.

**Usage example:**

- Monitor filesystem activity:  
  `sudo fs_usage`

## `GetFileInfo` - Get HFS+ File Attributes

**What it does:**  
`GetFileInfo` retrieves metadata and attributes of files on HFS+ file systems, such as file type, creator code, and flags.

**Why use it:**  
To inspect file properties that are not visible through standard commands, particularly when dealing with legacy Mac files.

**Usage example:**

- Get information about a file:  
  `GetFileInfo myfile.txt`

## `hdiutil` - Manipulate Disk Images

**What it does:**  
`hdiutil` creates, mounts, unmounts, and manipulates disk images (.dmg files). It supports encryption, compression, and segmentation.

**Why use it:**  
For creating custom disk images for software distribution, backups, encrypted volumes, or automating disk image tasks in scripts.

**Usage example:**

- Create a disk image from a folder:  
  `hdiutil create -volname MyDisk -srcfolder /path/to/folder -ov -format UDZO mydisk.dmg`

## `installer` - Install macOS Packages

**What it does:**  
`installer` installs macOS installer packages (.pkg files) from the command line.

**Why use it:**  
To automate software installations, especially in deployment scripts or when setting up multiple systems without user interaction.

**Usage example:**

- Install a package:  
  `sudo installer -pkg package.pkg -target /`

## `iosnoop` - Monitor I/O Events

**What it does:**  
`iosnoop` tracks I/O events as they occur, showing which processes are performing read/write operations.

**Why use it:**  
For performance tuning, identifying I/O bottlenecks, or monitoring disk activity for specific applications.

**Usage example:**

- Start monitoring I/O events (requires sudo):  
  `sudo iosnoop`

## `kextfind` - Find Kernel Extensions

**What it does:**  
`kextfind` searches for kernel extensions (kexts) based on criteria like bundle identifiers, version numbers, or dependencies.

**Why use it:**  
To locate specific kernel extensions when troubleshooting system issues or verifying driver installations.

**Usage example:**

- Find all kexts with a specific bundle identifier:  
  `kextfind -b com.example.driver`

## `kextstat` - Kernel Extension Status

**What it does:**  
`kextstat` lists currently loaded kernel extensions, showing their load addresses, dependencies, and identifiers.

**Why use it:**  
For diagnosing kernel-related problems, ensuring necessary drivers are loaded, or checking for conflicting extensions.

**Usage example:**

- List all loaded kernel extensions:  
  `kextstat`

## `kextunload` - Unload Kernel Extensions

**What it does:**  
`kextunload` unloads a kernel extension from the running system.

**Why use it:**  
To remove problematic drivers without rebooting, update extensions, or temporarily disable functionality for testing.

**Usage example:**

- Unload a kernel extension:  
  `sudo kextunload /System/Library/Extensions/Example.kext`

## `kickstart` - Configure Apple Remote Desktop

**What it does:**  
`kickstart` configures the Apple Remote Desktop (ARD) service, allowing you to enable remote management and set access permissions.

**Why use it:**  
For setting up remote administration capabilities on multiple Macs, automating ARD configurations, or deploying settings in managed environments.

**Usage example:**

- Enable ARD and allow access for all users:  
  `sudo /System/Library/CoreServices/RemoteManagement/ARDAgent.app/Contents/Resources/kickstart -activate`

## `launchctl` - Manage Daemons and Agents

**What it does:**  
`launchctl` interacts with `launchd`, the service management framework for starting, stopping, and managing daemons and agents.

**Why use it:**  
To control background services, schedule tasks, or manage startup items, essential for system administration and automation.

**Usage example:**

- Load a launch agent:  
  `launchctl load ~/Library/LaunchAgents/com.example.agent.plist`

- List all loaded services:  
  `launchctl list`

## `lsregister` - Launch Services Database Management

**What it does:**  
`lsregister` rebuilds or resets the Launch Services database, which maps file types to applications.

**Why use it:**  
When experiencing issues like incorrect file associations, applications not appearing in "Open With" menus, or other anomalies, `lsregister` can help fix them.

**Usage example:**

- Rebuild the Launch Services database:  
  `/System/Library/Frameworks/CoreServices.framework/Frameworks/LaunchServices.framework/Support/lsregister -kill -r -domain local -domain system -domain user`

## `lsbom` - List Bill of Materials

**What it does:**  
`lsbom` lists the contents of a Bill of Materials (BOM) file, which records files installed by a package.

**Why use it:**  
To audit installed files, verify package installations, or understand what files are associated with a specific package.

**Usage example:**

- List files in a BOM file:  
  `lsbom /var/db/receipts/com.example.pkg.bom`

## `mdfind` - Spotlight Search from the Command Line

**What it does:**  
`mdfind` performs searches using Spotlight's index, allowing you to find files based on metadata and content.

**Why use it:**  
To locate files quickly without scanning the entire filesystem, useful in scripts or when the GUI is unavailable.

**Usage example:**

- Find files with "report" in the name:  
  `mdfind "kMDItemFSName == '*report*'"`

## `mdimport` - Import Files into Spotlight Index

**What it does:**  
`mdimport` forces Spotlight to index specified files or directories.

**Why use it:**  
To manually update the Spotlight index after adding or modifying files, ensuring they appear in search results promptly.

**Usage example:**

- Index a folder:  
  `mdimport /path/to/folder`

## `mdls` - Display Metadata Attributes

**What it does:**  
`mdls` lists the metadata attributes of a file as indexed by Spotlight, such as creation date, keywords, and content type.

**Why use it:**  
To inspect file metadata for debugging, data analysis, or to use in scripts that process files based on attributes.

**Usage example:**

- Show metadata of a file:  
  `mdls document.pdf`

## `mdutil` - Manage Spotlight Indexing

**What it does:**  
`mdutil` enables or disables Spotlight indexing on volumes and manages the index store.

**Why use it:**  
To prevent indexing on volumes where it's unnecessary (like backup drives), or to rebuild the index when it's corrupted.

**Usage example:**

- Disable indexing on a volume:  
  `sudo mdutil -i off /Volumes/ExternalDrive`

- Rebuild the index:  
  `sudo mdutil -E /`

## `mkfile` - Create a File with a Specific Size

**What it does:**  
`mkfile` creates a file of a specified size, filled with null bytes.

**Why use it:**  
For testing disk space usage, simulating large files, benchmarking, or creating placeholder files.

**Usage example:**

- Create a 100 MB file:  
  `mkfile 100m largefile.dat`

## `networkQuality` - Network Performance Testing

**What it does:**  
`networkQuality` measures network performance metrics like upload/download capacity and responsiveness.

**Why use it:**  
To diagnose internet connection issues, test network speed, or monitor network quality over time.

**Usage example:**

- Run a network quality test:  
  `networkQuality`

## `networksetup` - Configure Network Settings

**What it does:**  
`networksetup` manages network configurations, including interfaces, locations, proxies, and DNS settings.

**Why use it:**  
To automate network setup, switch configurations when moving between locations, or manage settings on headless systems.

**Usage example:**

- Set DNS servers for Wi-Fi:  
  `networksetup -setdnsservers Wi-Fi 8.8.8.8 8.8.4.4`

## `ntfs.util` - NTFS Filesystem Utility

**What it does:**  
`ntfs.util` assists in mounting NTFS volumes and handling NTFS-specific tasks.

**Why use it:**  
To access NTFS-formatted drives on macOS, particularly for reading data from Windows-formatted disks.

**Usage example:**

- Mount an NTFS volume (usually handled automatically):  
  `ntfs.util -m disk2s1`

## `nvram` - Manipulate Firmware Variables

**What it does:**  
`nvram` reads and writes variables stored in non-volatile memory, such as boot arguments and system settings.

**Why use it:**  
For configuring low-level system settings, troubleshooting boot issues, or setting hardware preferences.

**Usage example:**

- Reset NVRAM:  
  `sudo nvram -c`

- Set a boot argument:  
  `sudo nvram boot-args="-v"`

## `open` - Open Files and Applications

**What it does:**  
`open` opens files, directories, or URLs in the default or specified application. It can also open applications directly.

**Why use it:**  
To launch applications or files from the command line, integrate with scripts, or automate workflows that require opening GUI elements.

**Usage example:**

- Open a file with the default application:  
  `open report.pdf`

- Open a URL in the default browser:  
  `open https://www.example.com`

- Open a file with a specific application:  
  `open -a TextEdit notes.txt`

## `opensnoop` - Monitor File Opens

**What it does:**  
`opensnoop` tracks and displays files as they are opened by processes in real-time.

**Why use it:**  
For security auditing, troubleshooting file access issues, or monitoring application behavior regarding file usage.

**Usage example:**

- Start monitoring file opens (requires sudo):  
  `sudo opensnoop`

## `osacompile` - Compile AppleScript Scripts

**What it does:**  
`osacompile` compiles AppleScript files into compiled scripts or applications.

**Why use it:**  
To automate the compilation of scripts for distribution, integrate scripting into build processes, or protect source code.

**Usage example:**

- Compile an AppleScript into an application:  
  `osacompile -o MyApp.app myscript.scpt`

## `osascript` - Execute AppleScript and Other OSA Scripts

**What it does:**  
`osascript` runs AppleScript or other Open Scripting Architecture (OSA) scripts from the command line.

**Why use it:**  
To automate tasks that require interaction with GUI applications or system services that are scriptable via AppleScript.

**Usage example:**

- Run an AppleScript file:  
  `osascript myscript.scpt`

- Execute an inline AppleScript:  
  `osascript -e 'display dialog "Hello, world!"'`

## `pbcopy` - Copy Data to the Clipboard

**What it does:**  
`pbcopy` takes standard input and places it into the clipboard (pasteboard).

**Why use it:**  
To programmatically copy text or data into the clipboard from scripts or command output.

**Usage example:**

- Copy the contents of a file to the clipboard:  
  `cat file.txt | pbcopy`

## `pbpaste` - Paste Data from the Clipboard

**What it does:**  
`pbpaste` outputs the contents of the clipboard to standard output.

**Why use it:**  
To retrieve data from the clipboard for use in scripts or to process clipboard contents via command-line tools.

**Usage example:**

- Save the clipboard contents to a file:  
  `pbpaste > clipboard.txt`

## `pbs` - Pasteboard Server Helper Tool

**What it does:**  
`pbs` is a background service that manages the clipboard (pasteboard) on macOS.

**Why use it:**  
While not typically used directly, understanding `pbs` can help in troubleshooting clipboard issues or when needing to restart the service.

**Usage example:**

- Restart the pasteboard server:  
  `killall pbs`

## `pdisk` - Apple Partition Table Editor

**What it does:**  
`pdisk` edits partition maps on disks, particularly those using the Apple Partition Map (APM) scheme.

**Why use it:**  
For managing partitions on legacy systems or disks that require APM, which is necessary for older Mac hardware or specific compatibility scenarios.

**Usage example:**

- List partitions on a disk:  
  `pdisk /dev/disk0 -dump`

## `pfctl` - Packet Filter Control

**What it does:**  
`pfctl` manages the PF firewall, allowing you to configure firewall rules, NAT, and traffic filtering.

**Why use it:**  
To enhance network security by controlling inbound and outbound traffic, set up complex firewall rules, or manage network address translation.

**Usage example:**

- Load a PF configuration file:  
  `sudo pfctl -f /etc/pf.conf`

- Enable the PF firewall:  
  `sudo pfctl -e`

## `pkgbuild` - Build Installer Packages

**What it does:**  
`pkgbuild` creates macOS installer packages from a payload and scripts, used for software distribution.

**Why use it:**  
Developers and system administrators can package applications, scripts, or settings for deployment across multiple systems.

**Usage example:**

- Build a package from a component:  
  `pkgbuild --root /path/to/root --identifier com.example.pkg --version 1.0 example.pkg`

## `pkgutil` - Package Manager Utility

**What it does:**  
`pkgutil` examines and manipulates installed package receipts, allowing you to query, verify, and forget packages.

**Why use it:**  
To troubleshoot installation issues, verify what files were installed by a package, or clean up package receipts.

**Usage example:**

- List all installed packages:  
  `pkgutil --pkgs`

- Forget a package (remove its receipt):  
  `sudo pkgutil --forget com.example.pkg`

## `plutil` - Property List Utility

**What it does:**  
`plutil` checks, converts, and manipulates property list (plist) files, which are used for storing configuration data.

**Why use it:**  
To validate plist files, convert between binary and XML formats, or automate changes to configuration files.

**Usage example:**

- Convert a binary plist to XML:  
  `plutil -convert xml1 settings.plist`

- Validate a plist file:  
  `plutil settings.plist`

## `pmset` - Power Management Settings

**What it does:**  
`pmset` adjusts power management settings like sleep timers, hibernation modes, and wake-on-LAN.

**Why use it:**  
To optimize power usage, extend battery life, or configure systems for specific operational needs, such as servers or kiosks.

**Usage example:**

- Set the display sleep timer to 15 minutes:  
  `sudo pmset displaysleep 15`

- Disable sleep mode:  
  `sudo pmset sleep 0`

## `powermetrics` - Power and Performance Statistics

**What it does:**  
`powermetrics` provides detailed statistics on power usage, CPU activity, thermal conditions, and more.

**Why use it:**  
For performance analysis, diagnosing battery drain issues, or monitoring system health under different workloads.

**Usage example:**

- Monitor CPU power usage:  
  `sudo powermetrics --samplers cpu_power`

## `profiles` - Configuration Profiles Management

**What it does:**  
`profiles` manages user and device configuration profiles, which enforce settings and restrictions on macOS.

**Why use it:**  
To deploy settings across multiple machines, enforce security policies, or manage devices in an enterprise environment.

**Usage example:**

- List installed profiles:  
  `profiles -P`

- Install a profile:  
  `sudo profiles -I -F /path/to/profile.mobileconfig`

## `purge` - Clear Disk Cache

**What it does:**  
`purge` forces the system to clear disk caches, freeing up memory.

**Why use it:**  
For testing applications under low-memory conditions, clearing inactive memory, or troubleshooting memory-related performance issues.

**Usage example:**

- Clear disk caches:  
  `sudo purge`

## `qlmanage` - Quick Look Management Tool

**What it does:**  
`qlmanage` tests and manages Quick Look generators, which create file previews in Finder.

**Why use it:**  
To troubleshoot preview issues, test custom Quick Look plugins, or force the generation of new previews.

**Usage example:**

- Preview a file using Quick Look:  
  `qlmanage -p document.pdf`

- Reset the Quick Look server:  
  `qlmanage -r`

## `ReportCrash` - Crash Reporting

**What it does:**  
`ReportCrash` handles the logging and reporting of application crashes to Apple.

**Why use it:**  
Developers might disable `ReportCrash` during testing to prevent interference, or re-enable it to capture crash logs for troubleshooting.

**Usage example:**

- Disable crash reporting:  
  `launchctl unload -w /System/Library/LaunchAgents/com.apple.ReportCrash.plist`

- Enable crash reporting:  
  `launchctl load -w /System/Library/LaunchAgents/com.apple.ReportCrash.plist`

## `say` - Text-to-Speech Utility

**What it does:**  
`say` converts text to speech, outputting audio through the speakers or saving to an audio file.

**Why use it:**  
For accessibility purposes, creating spoken alerts in scripts, generating audio versions of text, or just for fun.

**Usage example:**

- Speak a phrase:  
  `say "Hello, world!"`

- Save speech to an audio file:  
  `say -o greeting.aiff "Welcome to the system"`

## `screencapture` - Capture Screenshots

**What it does:**  
`screencapture` takes screenshots of the screen, windows, or selected areas, saving them as image files.

**Why use it:**  
To automate screenshot capture in scripts, document processes, or capture images in remote sessions.

**Usage example:**

- Capture the entire screen:  
  `screencapture screen.jpg`

- Capture a selected window after a delay:  
  `screencapture -w -T5 window.png`

## `scselect` - Switch Network Locations

**What it does:**  
`scselect` changes the active network location, which is a set of network configurations.

**Why use it:**  
To quickly switch between different network setups, such as home and office networks, without manual reconfiguration.

**Usage example:**

- List available network locations:  
  `scselect`

- Switch to a network location named "Office":  
  `scselect "Office"`

## `scutil` - System Configuration Utility

**What it does:**  
`scutil` interacts with the system configuration database, allowing you to query and change network settings.

**Why use it:**  
For advanced network configuration, scripting network setups, or troubleshooting connectivity issues.

**Usage example:**

- Display the current hostname:  
  `scutil --get HostName`

- Set a new hostname:  
  `sudo scutil --set HostName newhostname`

## `security` - Manage Keychains and Certificates

**What it does:**  
`security` handles tasks related to keychains, certificates, and secure storage, such as adding certificates or querying keychain items.

**Why use it:**  
To automate certificate deployment, manage authentication credentials, or script secure interactions in applications.

**Usage example:**

- List all keychains:  
  `security list-keychains`

- Import a certificate:  
  `security import cert.pem -k ~/Library/Keychains/login.keychain-db`

## `serverinfo` - macOS Server Information

**What it does:**  
`serverinfo` provides information about the macOS Server installation, including version and services.

**Why use it:**  
To verify server configurations, check for installed services, or script server management tasks.

**Usage example:**

- Display server version:  
  `serverinfo --version`

## `setfile` - Set File Attributes

**What it does:**  
`setfile` changes file attributes like creation date, visibility, or file type and creator codes.

**Why use it:**  
To adjust file properties not accessible through standard tools, useful in batch operations or when preparing files for specific applications.

**Usage example:**

- Set the creation date of a file:  
  `SetFile -d "09/30/2023 12:00:00" document.txt`

- Make a file invisible:  
  `SetFile -a V hiddenfile.txt`

## `sharing` - Configure File Sharing

**What it does:**  
`sharing` sets up shared folders and manages sharing services like AFP, FTP, and SMB.

**Why use it:**  
To automate the setup of shared resources, manage access permissions, or configure sharing services without using the GUI.

**Usage example:**

- List all shared folders:  
  `sharing -l`

- Add a shared folder:  
  `sudo sharing -a /path/to/folder -s "SharedFolder"`

## `shortcuts` - Manage macOS Shortcuts

**What it does:**  
`shortcuts` allows you to run, list, and manage Shortcuts workflows from the command line.

**Why use it:**  
To integrate Shortcuts into automation scripts, trigger workflows programmatically, or manage shortcuts in bulk.

**Usage example:**

- List all available shortcuts:  
  `shortcuts list`

- Run a shortcut named "Resize Images":  
  `shortcuts run "Resize Images"`

## `shutdown` - Shutdown or Restart the System

**What it does:**  
`shutdown` powers off, restarts, or puts the system to sleep after a specified delay.

**Why use it:**  
For scheduling system maintenance, ensuring clean shutdowns in scripts, or remotely controlling system power states.

**Usage example:**

- Shut down immediately:  
  `sudo shutdown -h now`

- Restart after 1 minute:  
  `sudo shutdown -r +1`

## `sips` - Scriptable Image Processing System

**What it does:**  
`sips` performs basic image manipulations, including resizing, cropping, rotating, and format conversion.

**Why use it:**  
To batch process images, automate repetitive image editing tasks, or integrate image manipulation into larger scripts.

**Usage example:**

- Resize an image to 800x600 pixels:  
  `sips -z 600 800 input.jpg --out output.jpg`

- Convert an image to PNG format:  
  `sips -s format png input.jpg --out output.png`

## `softwareupdate` - Manage Software Updates

**What it does:**  
`softwareupdate` checks for, downloads, and installs macOS updates and upgrades.

**Why use it:**  
To automate system updates, manage updates across multiple machines, or integrate updates into maintenance scripts.

**Usage example:**

- List available updates:  
  `softwareupdate -l`

- Install all recommended updates:  
  `sudo softwareupdate -i -r`

## `spctl` - Security Policy Control

**What it does:**  
`spctl` manages Gatekeeper policies, controlling which applications are allowed to run based on their code signatures.

**Why use it:**  
To adjust security settings for app execution, whitelist specific applications, or troubleshoot Gatekeeper-related issues.

**Usage example:**

- Add an application to the whitelist:  
  `spctl --add /Applications/Example.app`

- Check the status of an application:  
  `spctl --assess --verbose=4 /Applications/Example.app`

## `sw_vers` - Show macOS Version

**What it does:**  
`sw_vers` displays the macOS version, build number, and product name.

**Why use it:**  
To check system version information in scripts, ensure compatibility, or log system details.

**Usage example:**

- Display macOS version information:  
  `sw_vers`

## `system_profiler` - System Configuration Report

**What it does:**  
`system_profiler` generates detailed reports of the system's hardware and software configuration.

**Why use it:**  
For inventory management, diagnostics, or collecting system information for support purposes.

**Usage example:**

- Generate a full system report:  
  `system_profiler`

- Save the report to a file:  
  `system_profiler -detailLevel full > system_report.txt`

## `systemsetup` - Configure System Settings

**What it does:**  
`systemsetup` changes system-level settings like time zone, wake settings, and network time servers.

**Why use it:**  
To automate configuration tasks, standardize settings across multiple machines, or adjust settings without user interaction.

**Usage example:**

- Set the time zone:  
  `sudo systemsetup -settimezone "America/New_York"`

- Enable network time synchronization:  
  `sudo systemsetup -setusingnetworktime on`

## `tab2space` - Convert Tabs to Spaces

**What it does:**  
`tab2space` replaces tabs with spaces in text files and ensures consistent line endings.

**Why use it:**  
To format code or text files according to style guidelines, or to prepare files for environments where tabs cause issues.

**Usage example:**

- Convert tabs to spaces in a file:  
  `tab2space -t 4 input.txt > output.txt`

## `taskpolicy` - Set Process Resource Policies

**What it does:**  
`taskpolicy` runs a command with modified resource policies, such as reduced CPU priority or I/O throttling.

**Why use it:**  
To limit the resource impact of a process, ensuring it doesn't interfere with other system activities.

**Usage example:**

- Run a command with low CPU priority:  
  `taskpolicy -c low command`

## `tccutil` - Privacy Database Management

**What it does:**  
`tccutil` manages the Transparency, Consent, and Control (TCC) database, which controls app access to protected resources.

**Why use it:**  
To reset permissions for apps accessing the camera, microphone, or other sensitive data, useful in troubleshooting or scripting privacy settings.

**Usage example:**

- Reset all permissions for an app:  
  `tccutil reset All com.example.app`

## `textutil` - Manipulate Text Files

**What it does:**  
`textutil` converts and manipulates text files in formats like TXT, RTF, DOC, HTML, and others.

**Why use it:**  
To batch convert documents, extract text from rich text files, or automate text processing tasks.

**Usage example:**

- Convert a Word document to plain text:  
  `textutil -convert txt document.docx`

- Combine multiple text files into one RTF:  
  `textutil -cat rtf file1.txt file2.txt -output combined.rtf`

## `tmutil` - Time Machine Utility

**What it does:**  
`tmutil` manages Time Machine backups, allowing you to start, stop, and configure backups.

**Why use it:**  
To automate backup processes, manage backup destinations, exclude items from backups, or restore data.

**Usage example:**

- Start a backup manually:  
  `tmutil startbackup`

- Set a new backup destination:  
  `sudo tmutil setdestination /Volumes/BackupDrive`

## `trimforce` - Enable TRIM for Third-Party SSDs

**What it does:**  
`trimforce` enables TRIM commands on non-Apple SSDs, which can improve performance and longevity.

**Why use it:**  
If you're using a third-party SSD, enabling TRIM helps maintain optimal performance, though it should be used with caution.

**Usage example:**

- Enable TRIM support:  
  `sudo trimforce enable`

## `ufs.util` - UFS Filesystem Utility

**What it does:**  
`ufs.util` handles mounting and unmounting of UFS file systems.

**Why use it:**  
For managing UFS volumes, though it's largely obsolete in modern macOS environments.

**Usage example:**

- Mount a UFS filesystem:  
  `ufs.util -m disk2s1`

## `wait4path` - Wait for a Path to Become Available

**What it does:**  
`wait4path` pauses execution until a specified file path appears in the filesystem.

**Why use it:**  
To ensure that a script doesn't proceed until a necessary resource is available, such as an external drive or network share.

**Usage example:**

- Wait for a volume to mount:  
  `wait4path /Volumes/ExternalDrive`

## `wdutil` - Wireless Diagnostics Utility

**What it does:**  
`wdutil` provides tools for capturing and analyzing wireless network diagnostics.

**Why use it:**  
For troubleshooting Wi-Fi connectivity issues, analyzing signal strength, or collecting data for support.

**Usage example:**

- Start a Wi-Fi diagnostics capture:  
  `sudo wdutil capture`

## `xattr` - Extended Attributes Utility

**What it does:**  
`xattr` reads and modifies extended attributes of files, which store metadata like quarantine status or custom properties.

**Why use it:**  
To remove quarantine flags from downloaded files, manage custom metadata, or fix issues caused by extended attributes.

**Usage example:**

- List extended attributes of a file:  
  `xattr -l downloaded.app`

- Remove the quarantine attribute:  
  `xattr -d com.apple.quarantine downloaded.app`

## `xcode-select` - Manage Command Line Developer Tools

**What it does:**  
`xcode-select` sets the active developer directory and installs command-line tools necessary for software development.

**Why use it:**  
To configure development environments, switch between multiple versions of Xcode, or install essential build tools.

**Usage example:**

- Install command-line developer tools:  
  `xcode-select --install`

- Switch to a different Xcode version:  
  `sudo xcode-select -s /Applications/Xcode_12.app`
