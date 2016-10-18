# AggressorScripts
Aggressor scripts for use with [Cobalt Strike](https://cobaltstrike.com) 3.0+

**beacon_to_empire.cna** - a script that leverages [Powershell Empire's](http://www.powershellempire.com/) RESTful API to migrate sessions from a Beacon session on Cobalt Strike

**CCDC** - a collection of scripts designed for use at CCDC
* **lulz.cna** - includes some Blue Team annoyance functions: IE Popup (kiosk mode), Windows Alert (7+), Host Shutdown, Boo.exe (uploads/executes Boo), and Clippy popup (requires setup and Windows 7).
* **misc.cna** - includes functions to stomp the host file with a chosen text file or add an entry to the existing host file.

**forcecheckin.cna** - forces an SMB Beacon to checkin after a specified frequency

**mimikatz-every-30m.cna** - runs mimikatz's "logonpasswords" alias every thirty minutes

**powershell.cna** - adds context items for some common Powerup and Powerview functions. For this to work, you must put the PowerUp.ps1 and powerview.ps1 files in the same directory as this script

**ping_aliases.cna** - creates an alias for quick ping (one ping packet w/ shell) and smbping (to portscan smb w/o ping)

**sleeptimer.cna** - automatically sets sleep intervals based on time. (ie from 10p to 6a, sleep for 60s). Resets to 60s sleeps when the sleep interval ends.

**timestamped_activitylog_export.cna** - Outputs all event and activity logs with human-readable timestamp to activitylog.txt in your working directory (runs on script load)