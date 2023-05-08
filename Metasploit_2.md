

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
