### Installing Metasploitable3 to build Win2k8 box using/on Windows.
If you want to get direct VMs that I'm using for Metasploitable3. Use this [Google Drive link](https://drive.google.com/drive/folders/1gMVka_GJBoK83rqmh53brZ97ukTtUJQZ?usp=sharing) to download and directly import the .0va files into VirtualBox to use start hacking....! Hurray you can now skip and the below process..!


## Step1: Install VirtualBox
Download and install VirtualBox. Go to [Oracle VirtualBox](https://www.virtualbox.org/wiki/Downloads).

## Step2: Install Packer
The process is straighforward. Go to [Packer](https://developer.hashicorp.com/packer/downloads). Download and install packer. I used ```AMD64 Version: 1.9.4```

## Step3: Installing Vagrant
Download the [Vagrant Software for Windows](https://developer.hashicorp.com/vagrant/downloads) and install it. Then Restart your PC.

Then disable Windows Firewall Defender.
Now we have to install vargant plugins. So test if vagrant is installed? 
* Open cmd and type ```vagrant --version```
* If no output shows up then vagrant is not installed. If you see output like Vagrant 2.3.4(latest version in April 2023) then proceed.

Open cmd & Type ```vagrant plugin install vagrant-vbguest```. 
* Note this can take sometime so wait don't hurry and stop the cmd prompt(took me 4 mins). Output will look something like this:
OUTPUT:
``` 
C:\Users\user1>vagrant plugin install vagrant-vbguest
Installing the 'vagrant-vbguest' plugin. This can take a few minutes...
Fetching micromachine-3.0.0.gem
Fetching vagrant-vbguest-0.31.0.gem
Installed the plugin 'vagrant-vbguest (0.31.0)'!
```
Now install Plugin-2: 
* Type ``` vagrant plugin install vagrant-reload ```. This will also take somtime(took me 5 mins). Output looks like this.
```
C:\Users\user1>vagrant plugin install vagrant-reload
Installing the 'vagrant-reload' plugin. This can take a few minutes...
Fetching vagrant-reload-0.0.1.gem
Installed the plugin 'vagrant-reload (0.0.1)'!
```
## Step4: Clone the Metasploitable3 Repo:
Download or Clone [this](https://github.com/rapid7/metasploitable3) repository and build your own box.
```
git clone https://github.com/rapid7/metasploitable3.git
```
After you clone or download this link it will give you the ```metasploitable3-master``` folder

## Step5: Installing Metasploitable3 through script:
Open PowerShell in Administrator mode.    

&nbsp; Got to the Working Directory of Metasploit3 & install ./build.ps1 (This is the script that will install Metasploitable3):   

``` 
cd C:\Users\user1\Desktop/<your_dir_where_metasploitable3-master_is>\metasploitable3-master\metasploitable3-master
./build.ps1 windows2008 
```
This will build a windows2008 server version of Metaspolit3.(took me 5 mins) This will setup the box and once this is done type ```vagrant up``` to setup the box.
