AUTHOR: CH1C4G0
DATE: 03/06/2026

<p><h1>How to use exploits</h1></p>

``
the "use" command
``

<p><h1>You can search for exploits</h1></p>

```
search apache
```

<p>or</p>

```
search type:auxiliary (keyword here)
```

<p><h1>You can gather info on an exploit with the following</h1></p>

<P>Select the exploit you want information on, once seletected type info.</P>

```
use (exploit type) path/to/exploit
- info
```

<p><h1>You can show options for an exploit with the following</h1></p>

```
use (exploit type) path/to/exploit
    - show options
```

<p><h1>Exploits Rankings</h1></p>

```
=======================================================================================================================================================================================================================================================================
Ranking	                Description

ExcellentRanking        The exploit will never crash the service. This is the case for SQL Injection, CMD execution, RFI, LFI, etc. No typical memory corruption exploits should be given this ranking unless there are extraordinary circumstances (WMF Escape()).

GreatRanking	        The exploit has a default target AND either auto-detects the appropriate target or uses an application-specific return address AFTER a version check.

GoodRanking	        The exploit has a default target and it is the “common case” for this type of software (English, Windows 7 for a desktop app, 2012 for server, etc). Exploit does not auto-detect the target.

NormalRanking	        The exploit is otherwise reliable, but depends on a specific version that is not the “common case” for this type of software and can’t (or doesn’t) reliably autodetect.

AverageRanking	        The exploit is generally unreliable or difficult to exploit, but has a success rate of 50% or more for common platforms.

LowRanking	        The exploit is nearly impossible to exploit (under 50% success rate) for common platforms.

ManualRanking	        The exploit is unstable or difficult to exploit and is basically a DoS (15% success rate or lower). This ranking is also used when the module has no use unless specifically configured by the user (e.g.: exploit/unix/webapp/php_eval).
======================================================================================================================================================================================================================================================================
```

<p><h1>SHOW OPTIONS IS CRUCIAL</h1></p>

```
show options
```

<p>This allows you to see the parameters you must satisy for the module to work</p>

<p><h1>How to Set Parameters</h1></p>

```
- set PARAMETER_NAME VALUE
```

<p><h1>Unsetting Parameter Values</h1></p>

```
- unset param value

        or
        
- unset all
    - unsets all parameters
```

<p><h1>How to set parameters accross modules</h1></p>

<p>You can set values that will stay even when you switch modules by using</p>

```
"setg"

You can also remove these global parameters by using.

"unsetg"

```
    
<p><h1>Common Parameters</h1></p>

```
==========================================================================================================================================
RHOSTS: “Remote host”, the IP address of the target system. A single IP address or a network range can be set. This will support the CIDR (Classless Inter-Domain Routing) notation (/24, /16, etc.) or a network range (10.10.10.x – 10.10.10.y). You can also use a file where targets are listed, one target per line using file:/path/of/the/target_file.txt, as you can see below.
==========================================================================================================================================
RPORT: “Remote port”, the port on the target system the vulnerable application is running on.
==========================================================================================================================================
PAYLOAD: The payload you will use with the exploit.
==========================================================================================================================================
LHOST: “Localhost”, the attacking machine (your AttackBox or Kali Linux) IP address.
==========================================================================================================================================
LPORT: “Local port”, the port you will use for the reverse shell to connect back to. This is a port on your attacking machine, and you can set it to any port not used by any other application.
==========================================================================================================================================
SESSION: Each connection established to the target system using Metasploit will have a session ID. You will use this with post-exploitation modules that will connect to the target system using an existing connection.
==========================================================================================================================================
```
<p><h1>Executing the payload</h1></p>

<p>Once all parameters are set you can execute your payload with "exploit" or "run"</p>

```
exploit
```
```
run
```
<p><h1>How to clear the payload</h1></p>

```
unset "PAYLOAD"
```

<p><h1>Running successfully exploited machines in background mode.</h1></p>

<p>simply type "background" after successful execution</p>

```
background
```

<p>You can view your open sessions / background sessions with the "sessions" command.</p>

<p>You can interact with the open sessions by using,</p>
```
sessions -i (session # )
```

<p><h1>Meterpreter</h1></p>

<p>An important payload. This means the merterpreter payload was loaded into the target system and connected back to you.<br>
This will allow you to get a shell, ect.</p>



