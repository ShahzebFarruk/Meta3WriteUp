### Installing Metasploit3 to build Win2k8 box using/on Windows.
## Installing Vagrant
Download the [Vagrnat Software for Windows!https://developer.hashicorp.com/vagrant/downloads] and install it. Then Restart your PC.

Then disable Windows Firewall Defender.
Now we have to install vargant plugins. So test if vagrant is installed? Open cmd and type ```vagrant --version```
If no output shows up then vagrant is not installed. If you see output like Vagrant 2.3.4(latest version in April 2023) then proceed.

Open cmd & Type ```vagrant plugin install vagrant-vbguest```. Note this can take sometime so wait don't hurry and stop the cmd prompt(took me 4 mins). Output will look something like this:
OUTPUT:
``` 
C:\Users\Parzival>vagrant plugin install vagrant-vbguest
Installing the 'vagrant-vbguest' plugin. This can take a few minutes...
Fetching micromachine-3.0.0.gem
Fetching vagrant-vbguest-0.31.0.gem
Installed the plugin 'vagrant-vbguest (0.31.0)'!
```
Now install Plugin-2: Type ``` vagrant plugin install vagrant-reload ```. This will also take somtime(took me 5 mins). Output looks like this.
```
C:\Users\Sfarruk>vagrant plugin install vagrant-reload
Installing the 'vagrant-reload' plugin. This can take a few minutes...
Fetching vagrant-reload-0.0.1.gem
Installed the plugin 'vagrant-reload (0.0.1)'!
```

Open PowerShell in Administrator mode. Got to the Working Directory of Metasploit3.
``` 
cd C:\Users\Parzival\Desktop\NETS1034\metasploitable3-master\metasploitable3-master
./build.ps1 windows2008 
```
This will build a windows2008 server version of Metaspolit3.(took me 5 mins) This will setup the box and once this is done type ```vagrant up``` to setup the box.
