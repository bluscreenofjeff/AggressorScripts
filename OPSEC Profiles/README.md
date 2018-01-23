# Opsec Aggressor Profiles

The profiles in this folder overwrite the built-in Cobalt Strike commands to prevent certain commands from being run altogether. For example, if you are operating in an environment where process injections is very closely monitored, load the *process-injection.cna* to prevent any Beacon commands that rely on process injection from running. 

Demo:
![OPSEC Profile Demo](https://bluescreenofjeff.com/assets/cobalt-strike-opsec-profiles/cobalt-strike-powershell-opsec-profile-demo.gif)

The profiles allow an operator to `enable` or `block` commands. *Block* is used to prevent a command from running, while *enable* allows the command to run. To modify the state of a given command on-the-fly, you will need to unload the script, modify the source, and reload the script.

The following profiles are available:

* **cmd-execution.cna** - Prevents commands that rely on cmd.exe
* **powershell.cna** - Prevents commands that rely on powershell.exe
* **process-execution.cna** - Prevents commands that spawn a new process
* **process-injection.cna** - Prevents commands that use process injection
* **service-creation.cna** - Prevents commands that create new services
* **template.cna** - Includes all commands with an on/off variable for each command at the top of the script. Edit as needed for your specific use-case.

Note: if you wish to remove the OPSEC profile and restore default functionality, you can either unload the script and restart the Cobalt Strike client or unload the script and load the [default.cna](https://www.cobaltstrike.com/aggressor-script/default.cna) script.

The profiles also add the `opsec` command, which can be used to list all commands with their current block/enable setting.

```
beacon> opsec
[+] The current opsec profile has the following commands set to enable/block: 
[*] browserpivot - enable
[*] bypassuac - block
[*] cancel - enable
[*] cd - enable
[*] checkin - enable
[*] clear - enable
[*] covertvpn - block
[*] cp - enable
```


The profiles limit command functionality in both the Beacon console and popup (right-click) menu. The profiles do NOT limit additional functionality provided in the GUI, such as the ability to inject from the Process Pane. Be wary of these limitations!

*If you run into any operational issues while using this profiles, please open a GitHub issue!*

For more information about OPSEC Profiles, please see my blog post [Cobalt Strike OPSEC Profiles](https://bluescreenofjeff.com/2018-01-23-cobalt-strike-opsec-profiles/)