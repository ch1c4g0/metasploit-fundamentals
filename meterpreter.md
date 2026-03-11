

<p><h1>What is Meterpreter?</h1></p>

<p>Meterpreter is a payload that runs on target machines and acts as a<br>
command and control agent.</p>

<p><h1>How does Meterpreter work?</h1></p>

><p>Meterpreter runs on the host but is not installed. It operates in memory<br>
>so it does not have to write itself to the disk, this evades Anti-Virus Detection.</p>
>
><p>Meterpreter also aims to avoid detection by IDS/IPS systems.<br>
>It uses encrypted communication with your attacking machine.<br>
If the IDS/IPS does not decrypt and inspect traffic before hitting hosts, it can evade detection.</p>

><p><h1>Meterpreter is available for the following platforms;</h1></p>
>
> - Android
> - Apple IOS
> - Java
> - Linux
> - OSX
> - PHP
> - Python
> - Windows

><p><h1>How do you chose your payload?</h1></p>
>
> - What is the target operating system?
> - What components are available on the target system (Python installed, PHP Website, ect)
> - What kind of network connections are allowed? (TCP, HTTP, HTTPs)?

<p><h1>Meterpreter commands</h1></p>

<p>Core commands will be helpful to navigate and interact with the target system. Below are some of the most commonly used.<br>
Remember to check all available commands running the help command once a Meterpreter session has started.</p>

><p><h2>Core commands</h2></p>
>
> - background: Backgrounds the current session
> - exit: Terminate the Meterpreter session
> - guid: Get the session GUID (Globally Unique Identifier)
> - help: Displays the help menu
> - info: Displays information about a Post module
> - irb: Opens an interactive Ruby shell on the current session
> - load: Loads one or more Meterpreter extensions
> - migrate: Allows you to migrate Meterpreter to another process
> - run: Executes a Meterpreter script or Post module
> - sessions: Quickly switch to another session

><p><h2>File system commands</h2></p>
>
> - cd: Will change directory
> - ls: Will list files in the current directory (dir will also work)
> - pwd: Prints the current working directory
> - edit: will allow you to edit a file
> - cat: Will show the contents of a file to the screen
> - rm: Will delete the specified file
> - search: Will search for files
> - upload: Will upload a file or directory
> - download: Will download a file or directory

><p><h2>Networking commands</h2></p>
>
> - arp: Displays the host ARP (Address Resolution Protocol) cache
> - ifconfig: Displays network interfaces available on the target system
> - netstat: Displays the network connections
> - portfwd: Forwards a local port to a remote service
> - route: Allows you to view and modify the routing table

><p><h2>System commands</h2></p>
>
> - clearev: Clears the event logs
> - execute: Executes a command
> - getpid: Shows the current process identifier
> - getuid: Shows the user that Meterpreter is running as
> - kill: Terminates a process
> - pkill: Terminates processes by name
> - ps: Lists running processes
> - reboot: Reboots the remote computer
> - shell: Drops into a system command shell
> - shutdown: Shuts down the remote computer
> - sysinfo: Gets information about the remote system, such as OS

><p><h2>Others Commands (these will be listed under different menu categories in the help menu)</h2></p>
>
> - idletime: Returns the number of seconds the remote user has been idle
> - keyscan_dump: Dumps the keystroke buffer
> - keyscan_start: Starts capturing keystrokes
> - keyscan_stop: Stops capturing keystrokes
> - screenshare: Allows you to watch the remote user's desktop in real time
> - screenshot: Grabs a screenshot of the interactive desktop
> - record_mic: Records audio from the default microphone for X seconds
> - webcam_chat: Starts a video chat
> - webcam_list: Lists webcams
> - webcam_snap: Takes a snapshot from the specified webcam
> - webcam_stream: Plays a video stream from the specified webcam
> - getsystem: Attempts to elevate your privilege to that of local system
> - hashdump: Dumps the contents of the SAM database
