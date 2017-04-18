# basicMobat

This is a cross-platform Python 2.x Remote Access Trojan (RAT), builded from the project BasicRat. Currently work in progress by the Mob's Team

**Disclaimer: This RAT is for research and educational purposes only, and should only be used on authorized systems. Accessing a computer system or network without authorization or explicit permission is illegal.**

## Features
* Cross-platform (Windows, Linux, and macOS)
* AES GCM encrypted C2 with D-H exchange
* Accepts connection from multiple clients
* Command execution
* File upload/download (a bit buggy since crypto change)
* Standard utilities (wget, unzip)
* System survey
* keylogger
* Network traffic sniffing
* Browser history dump (currently work in progress)

## Usage
```
----------------------------------------------------------------------------------------
    __  ___      __   _          ___                               ______            __
   /  |/  /___  / /_ ( )_____   /   | _____________  __________   /_  __/___  ____  / /
  / /|_/ / __ \/ __ \|// ___/  / /| |/ ___/ ___/ _ \/ ___/ ___/    / / / __ \/ __ \/ / 
 / /  / / /_/ / /_/ / (__  )  / ___ / /__/ /__/  __(__  |__  )    / / / /_/ / /_/ / /  
/_/  /_/\____/_.___/ /____/  /_/  |_\___/\___/\___/____/____/    /_/  \____/\____/_/   
----------------------------------------------------------------------------------------
                               _________-----_____
                     ____------           __      ----_
               ___----             ___------              \
                  ----________        ----                 \
                             -----__    ^|             _____)
                                  __-                /     \
                      _______-----    ___--          \    /)\
                ------_______      ---____            \__/  /
                             -----__    \ --    _          /\
                                    --__--__     \_____/   \_/\
                                            ---^|   /          ^|
                                               ^| ^|___________^|
                                               ^| ^| ((_(_)^| )_)
                                               ^|  \_((_(_)^|/(_)
                                                \             (
                                                 \_____________)
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

basicMOBAT server listening for connections on port 1337.

client <id>         - Connect to a client.
clients             - List connected clients.
download <files>    - Download file(s).
execute <command>   - Execute a command on the target.
help                - Show this help menu.
kill                - Kill the client connection.
persistence         - Apply persistence mechanism.
quit                - Exit the server and end all client connections.
scan <ip>           - Scan top 25 TCP ports on a single host.
selfdestruct        - Remove all traces of the RAT from the target system.
survey              - Run a system survey.
unzip <file>        - Unzip a file.
upload <files>      - Upload files(s).
wget <url>          - Download a file from the web.
keylogger <action>  - Active keylogger on the target.                                                                
netcapture <action> - Launch a capture on the target. 
browser_history     - Dump browser history from the target
```

## Todo
* Interactive shell
* Client periodic connection attempt
* Client binary generation tool (cross-platform)
  * Pyinstaller
  * Switch options for remote IP, port, etc
* Persistence (cross-platform)
  * Windows: Registry keys, WMIC, Startup Dir
  * Linux: cron jobs, services, modprobe
  * macOS: LaunchAgent, LaunchDaemons
* Self-destruct (remove the RAT entirely)
* Privilege Escalation (getsystem-esque, dirty cow)
* Common C2 Protocols (HTTP, DNS)
* Clean log files
    * Linux: bash history, var logs, audit logs, etc
    * Windows: Event logs, prefetch, etc
* Screenshot
* Expand toolkit (unrar, sysinfo)
* Scanning utilities (probe scan / ping sweep, scanning subnet)
* Password dumping (mimikatz / gsecdump)
* Tunneling / Pivoting (ssh)
* Anti-virus detection and evasion
* VM and Sandbox detection
* Search file system for sensitive information using regex
    * addresses, credit cards numbers, socials, PII, etc
* Detect web cameras and take snapshots
* Steal wifi passwords

## Workers
* Alexandre Minaret
* Gwendal Orinel
* Gary Bernard

## Author
https://github.com/vesche/basicRAT
