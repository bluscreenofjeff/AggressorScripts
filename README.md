# AggressorScripts
Aggressor scripts for use with [Cobalt Strike](https://cobaltstrike.com) 3.0+

**apache-style-weblog-output.cna** - outputs weblog hits to an Apache-like access log file named weblog.log in Cobalt Strike's working directory 

**beacon_to_empire.cna** - a script that leverages [Powershell Empire's](http://www.powershellempire.com/) RESTful API to migrate sessions from a Beacon session on Cobalt Strike

**beaconid_note.cna** - set Beacon note to its ID on load and initial checkin (primarily useful when coding Aggressor scripts)

**beaconestablishednote.cna** - set Beacon note to the time it was established on initial checkin

**Beaconpire** - send Beacons to Empire and pull Empire Agents into Cobalt Strike

**CCDC** - a collection of scripts designed for use at CCDC
* **lulz.cna** - includes some Blue Team annoyance functions: IE Popup (kiosk mode), Windows Alert (7+), Host Shutdown, Boo.exe (uploads/executes Boo), and Clippy popup (requires setup and Windows 7).
* **misc.cna** - includes functions to stomp the host file with a chosen text file or add an entry to the existing host file.
* **sysinternals-killer.cna** - Automatically kill common Blue Team processes, such as the Sysinternals tools, on launch

**checkin_jobs_context.cna** - adds context menu options to run "checkin" or "jobs" on Beacon session to help detect stale beacons in bulk

**eventlog-to-slack.cna** - script to send event log events to Slack. NOTE: Review code before deploying in production. Sensitive information (usernames, hostnames, teamserver IPs) will be sent to Slack.

**forcecheckin.cna** - forces an SMB Beacon to checkin after a specified frequency

**mass-dcsync.cna** - DCSync a line-separated list of users from a DC

**mimikatz-every-30m.cna** - runs mimikatz's "logonpasswords" alias every thirty minutes

**mimikatz-timestamp-note-BETA.cna** - POC script that adds a timestamp to the source column in new credentials. The script is considered BETA - it has not been field tested and has bugs.

**OPSEC Profiles** - limits the commands Cobalt Strike can execute while loaded. Used to reduce the chance of performing high-risk actions in mature target environments.

**powershell.cna** - adds context items for some common Powerup and Powerview functions. For this to work, you must put the PowerUp.ps1 and powerview.ps1 files in the same directory as this script

**ping_aliases.cna** - creates an alias for quick ping (one ping packet w/ shell) and smbscan (to portscan smb w/o ping)

**ps-window-alias.cna** - creates an alias to open the process browser pane for the current Beacon

**silver-tickets.cna** - monitors Beacon output for machine hashes and stores them in the cred store. Also adds a dialog box for generating a [Silver Ticket](https://adsecurity.org/?p=2753) from a gathered machine hash

**slack-notify-beacon.cna** - sends a generic alert to a chosen Slack channel via incoming webhook when a new Beacon is established(requires curl on team server)

**slack-notify-webhit.cna** - sends a generic alert to a chosen Slack channel via incoming webhook when a specific URI or URIs are requested (requires curl on team server)

**sleep-down-when-no-operators.cna** - increases the sleep interval on all Beacons when there are no operators logged in

**sleeptimer.cna** - automatically sets sleep intervals based on time (i.e. from 10p to 6a, sleep for 60s). Resets to 60s sleeps when the sleep interval ends.

**stale-beacon-notifier.cna** - sends a generic alert to a chosen Slack channel via incoming webhook when a Beacon's last checkin exceeds a specified time (requires curl on team server).

**timestamped_activitylog_export.cna** - Outputs all event and activity logs with human-readable timestamp to activitylog.txt in your working directory (runs on script load)

# Other Aggressor Repos

* [https://github.com/Und3rf10w/Aggressor-scripts](https://github.com/Und3rf10w/Aggressor-scripts)
* [https://github.com/001SPARTaN/aggressor_scripts](https://github.com/001SPARTaN/aggressor_scripts)
* [https://github.com/vysec/Aggressor-VYSEC](https://github.com/vysec/Aggressor-VYSEC)
* [https://github.com/harleyQu1nn/AggressorScripts](https://github.com/harleyQu1nn/AggressorScripts)
* [https://github.com/rasta-mouse/Aggressor-Script](https://github.com/rasta-mouse/Aggressor-Script)
* [https://github.com/ramen0x3f/AggressorScripts](https://github.com/ramen0x3f/AggressorScripts)
* [https://github.com/invokethreatguy/CSASC](https://github.com/invokethreatguy/CSASC)

# Submissions
Please feel free to submit a Pull Request with fixes or improvements to any of the existing scripts; however, my intention is to only keep Aggressor scripts that I've written in this repo.

If you have an idea for a script and would like to submit it somewhere, consider adding it to Lee Kagan's [Aggressor Scripts Collection](https://github.com/invokethreatguy/CSASC) repo.
