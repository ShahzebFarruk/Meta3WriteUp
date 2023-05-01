fdo:wq
### Installing Metasploit3 to build Win2k8 box using/on Windows.
## Installing Vagrant
Restart your PC.

Then disable Windows Firewall Defender.
Now we have to install vargant plugins. So test if vagrant is installed? Open cmd and type ```vagrant --version```
If no output shows up then vagrant is not installed. If you see output like Vagrant 2.3.4(latest version in April 2023) then proceed.

Open cmd type ```vagrant plugin install vagrant-vbguest```. Note this can take sometime so wait don't hurry and stop the cmd prompt. Output will look something like this:
OUTPUT:
``` 
C:\Users\Parzival>vagrant plugin install vagrant-vbguest
Installing the 'vagrant-vbguest' plugin. This can take a few minutes...
Fetching micromachine-3.0.0.gem
Fetching vagrant-vbguest-0.31.0.gem
Installed the plugin 'vagrant-vbguest (0.31.0)'!
```
Now install Plugin-2: Type ``` vagrant plugin install vagrant-reload ```. This will also take somtime.
```

```
