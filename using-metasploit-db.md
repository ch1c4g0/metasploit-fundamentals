

<h1>How to start the Database<h1>

><h5><p>Metasploit uses PostgreSQL</p><h5>
<h5></h5>
<p>You can start PostgreSQL with</p>

```$ systemctl start postgresql```

![start-postgresql](https://github.com/ch1c4g0/metasploit-fundamentals/blob/37d0813fbe41be5e85f1dcab2faebc3784da0df8/using-metasploit-screenshots/Screenshot%202026-03-10%20at%2020-31-54%20TryHackMe%20Metasploit%20Meterpreter.png)
><p>You then need to intialize the Database<p>

```$ msfdb init```

![init-db](https://github.com/ch1c4g0/metasploit-fundamentals/blob/9f03c3391efcf6f5bf9ca32fa0c76891919d2434/using-metasploit-screenshots/Screenshot%202026-03-10%20at%2020-38-37%20TryHackMe%20Metasploit%20Meterpreter.png)

><p>Please note,running this as root will throw an error, if you are using root in kali use,</p> 

```$ sudo -u postgres msfdb init```

><p>You can also delete databases with,</p>

```$ delete databases with sudo -u postgres msfdb delete```

<p><h1>Check the status of your DB</h1></p>

<p>NOTE: msfconsole must be running before running this command</p>

![start-msf-console](https://github.com/ch1c4g0/metasploit-fundamentals/blob/29231ab389c9ab64a8e73d72c5d9de26f5862daf/using-metasploit-screenshots/Screenshot%202026-03-10%20at%2020-41-27%20TryHackMe%20Metasploit%20Meterpreter.png)

```$ msf6 db_status```

![db-status](https://github.com/ch1c4g0/metasploit-fundamentals/blob/4496d03902c0ced65aad6d4470c3f2595753b968/using-metasploit-screenshots/Screenshot%202026-03-10%20at%2020-43-36%20TryHackMe%20Metasploit%20Meterpreter.png)

<p><h1>Checking, Creating, and Adding workspaces</h1></p>

><p><h2>What are workspaces in Metasploit?</h2></p>
>
> - <p>Workspaces allow you to segment your pentration tests into easily accessible containers.</p>
> - <p>hosts, vulnerabilites, and loot are stored here.</p>

<p>NOTE: you can check your workspaces with,</p>

```$ msf6 workspace```

[check-workspace](https://github.com/ch1c4g0/metasploit-fundamentals/blob/c86910561a53dc513d548d679e345fd80db60cf8/using-metasploit-screenshots/Screenshot%202026-03-10%20at%2020-46-33%20TryHackMe%20Metasploit%20Meterpreter.png)

<p>Your current work space will be highlighted with "*".</p>

><p><h1>How to add / delete workspace</h1></p>
>
><p>You can use the -a and -d options to achieve creation and deletion.</p>

```$ workspace -a testworkspace```

![add-workspace](https://github.com/ch1c4g0/metasploit-fundamentals/blob/ff76dd2f20aad3ea21be00433260748e58bbd103/using-metasploit-screenshots/Screenshot%202026-03-10%20at%2020-51-39%20TryHackMe%20Metasploit%20Meterpreter.png)

```$ workspace -d testworkspace```

![delete-workspace](https://github.com/ch1c4g0/metasploit-fundamentals/blob/0fed3a1bf091742d9965add7f58bcfa38f886c30/using-metasploit-screenshots/Screenshot%202026-03-10%20at%2020-54-46%20TryHackMe%20Metasploit%20Meterpreter.png)

<p>NOTE: Removing a workspace will put you back to the default workspace</p>

<p><h1>Changing workspaces</h1></p>

<p>You can change workspaces by using workspace then specifying the workspace name</p>

<p>Creating the workspace again,</p>

```$ workspace -a tryhackme```

![add-thm-workspace](https://github.com/ch1c4g0/metasploit-fundamentals/blob/66be766561a32ae489ca12b3e4b236dda45417b7/using-metasploit-screenshots/Screenshot%202026-03-10%20at%2020-57-13%20TryHackMe%20Metasploit%20Meterpreter.png)

<p>Changing to the tryhackme workspace,</p>

```$ workspace tryhackme```

[change-to-thm-workspace](https://github.com/ch1c4g0/metasploit-fundamentals/blob/ee1bc115486832184ffe9ea64de9fa2b0803d9b3/using-metasploit-screenshots/Screenshot%202026-03-10%20at%2020-59-41%20TryHackMe%20Metasploit%20Meterpreter.png)

<p>Check to see if your workspace switched,</p>

```$ workspace```

![confirm-workspace-change](https://github.com/ch1c4g0/metasploit-fundamentals/blob/8222e0823543a3f10a3ba766768000168149cf59/using-metasploit-screenshots/Screenshot%202026-03-10%20at%2021-01-24%20TryHackMe%20Metasploit%20Meterpreter.png)

<p>Again, your current workspace will be highlighted with " * "</p>

><p><h1>Running an NMAP scan within your workspace</h1></p>
>
><p>You can run nmap scans directly from your db / workspace,</p>

```$ db_nmap -sV -p- 000.000.000.000```

![db-in-nmap](https://github.com/ch1c4g0/metasploit-fundamentals/blob/be3da027abb097f2ae9183f37afacb5fe783c5b2/using-metasploit-screenshots/Screenshot%202026-03-10%20at%2021-09-13%20TryHackMe%20Metasploit%20Exploitation.png)

<p>This data will now be stored within your workspace, it can be accessed by using the following,</p>

```$ hosts``` 

![running-hosts-after-nmap](https://github.com/ch1c4g0/metasploit-fundamentals/blob/3d2bdb5fcaf4138f240a77758eab80193fb605fb/using-metasploit-screenshots/Screenshot%202026-03-10%20at%2021-11-18%20TryHackMe%20Metasploit%20Exploitation.png)

```$ services```

![list-ports-in-db](https://github.com/ch1c4g0/metasploit-fundamentals/blob/b3cfa0395cafc476c934e20c46dd21a78f0cf4a3/using-metasploit-screenshots/Screenshot%202026-03-10%20at%2021-13-26%20TryHackMe%20Metasploit%20Exploitation.png)

<p>NOTE: you can use the services -h or hosts -h for help with that specific prompt.<br>
using "help" will provide you help with database syntax</p>

#### Workflow when scanning for vulnerabilities ####

- When you produce a host entry, it will set a global host address within the workspace.
    - You can check this with
        - hosts -R

msf6 auxiliary(scanner/smb/smb_ms17_010) > hosts -R

Hosts
=====

address      mac  name               os_name  os_flavor  os_sp  purpose  info  comments
-------      ---  ----               -------  ---------  -----  -------  ----  --------
10.66.138.1       ip-10-66-138-107.  Unknown                    device
07                ec2.internal

RHOSTS => 10.66.138.107

- Make sure your parameters are assigned properly.

#### Searching for services / hosts within your environment ####

    - services -S

msf6 auxiliary(scanner/smb/smb_ms17_010) > services -S netbios
Services
========

host           port  proto  name         state  info
----           ----  -----  ----         -----  ----
10.66.138.107  139   tcp    netbios-ssn  open   Samba smbd 4.6.2
10.66.138.107  445   tcp    netbios-ssn  open   Samba smbd 4.6.2

#### Things to look for ####

You may want to look for low-hanging fruits such as:

    HTTP: Could potentially host a web application where you can find vulnerabilities like SQL injection or Remote Code Execution (RCE).
    FTP: Could allow anonymous login and provide access to interesting files.
    SMB: Could be vulnerable to SMB exploits like MS17-010
    SSH: Could have default or easy to guess credentials
    RDP: Could be vulnerable to Bluekeep or allow desktop access if weak credentials were used. 



