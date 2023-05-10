

You might wanna create a different workspace for different targets:
```
man recon-ng
https://github.com/lanmaster53/recon-ng
[recon-ng][default] >  workspaces create example_name 
```

Recon-ng:
```
Install all the plugins:
marketplace info all
marketplace install all
```
You might wanna check what modules are installed:
modules load <tab>

Choose a module:
```
modules load recon/domains-hosts/bing_domain_web 
```
See options for the module u need to provide:
```
info
```

set the SOURCE to georgiancollege.ca:
```
options set SOURCE georgiancollege.ca
run
```

Now type show to see the domains:

    show hosts
[-] Quert the database to get the hosts stored in db: 
    
    db query SELECT * from Hosts

    db delete hosts <enter>
    1-10
    db insert hosts <enter>
Reporting and Export:

    modules load reporting/csv
    info
IF To set the filename to something else:

    options FILENAME set /home/kali/.recon-ng/workspaces/default/results.csv
then type:

    run
To see what was recovered type:
    
    show <tab>

Search for plugins for different domain:
    modules search domains

try running brute-hosts

recon-web to rung the web api interface and see the files.

----
### ihavebeenpwnd api access using recon-ng.
https://github.com/paralax/Recon-ng/blob/master/modules/recon/contacts-credentials/hibp_paste.py


---
### Google Dorking:
https://www.exploit-db.com/google-hacking-database

----
### Shodan with recon:
How to add shodan API key
Create or login to your Shodan account, Go to 'Account" in top right corner. The API Key is listed here on the Account Overview page.

Recon-ng shows the syntax to add an API key is below

    [recon-ng][default] > keys add 
Adds/Updates a third party resource credential

Usage: keys add name value

    [recon-ng][default] keys add shodan_api bbexampleapikey33 

More on:
https://hackertarget.com/recon-ng-tutorial/

---
### theHarvester:
```
theHarvester -d microsoft.com -l 200 -b bing
```

### Sublist3r
    git clone https://github.com/aboul3la/Sublist3r.git
    - OR 
    gh repo clone aboul3la/Sublist3r
    
    pip install -r requirements.txt

    sublist3r -d georgiancollege.ca 

    - Or try 
    python3 /usr/lib/python3/dist-packages/sublist3r.py -v -d example.com

    You may link the installation dir with [optional]
        ln -sf /opt/Sublist3r/sublist3r.py /usr/bin/sublist3r
        cd ~
        if you go to home dir now or any dir you may be able to run the tool.

Errors found: If you get this error: 
    [!] Error: Virustotal probably now is blocking our requests #346

Then do this:

    https://github.com/aboul3la/Sublist3r/issues/346

    This has been the case since April or something. Row 940 in sublist3r.py:
    Change:
            NetcraftEnum, DNSdumpster, Virustotal, ThreatCrowd,
    To:
            NetcraftEnum, DNSdumpster, ThreatCrowd,

    python3 /usr/lib/python3/dist-packages/sublist3r.py -v -d google.com

### Metasploit:
To check the open port for metasploit/ postgresql:

    sudo netstat -plunt |grep postgres 
    service <srv> status
    systemctl status <srv>
https://www.hackers-arise.com/post/2017/03/29/metasploit-basics-part-4-connecting-and-using-the-postgresql-database-with-metasploit

    Step #1: Start the postgresql Database
    msfdb status
    msfdb init 
    msfconsole
    Step #3: Working with Workspaces
    workspace 
    workspace -a hackersarise
    Step #6 Database Commands
    help
