### Nessus
Download the install or directly export the .ova file into Virtual box from [here](https://www.tenable.com/downloads/tenable-appliance?loginAttempted=true#tenablecore-nessus). 
Initial username and passwd are wizard and admin, respectively.

Go to instance: 192.168.0.127:8000

After you login change the username & passwd to:
username:admin passwd:TenableNessus!123

Click on Nessus on the interface; go to the link 10.0.2.5:8834

Go thorough the activation process: (Perform Offline Activation) ### "But activation doesn't work for me"
  In activation process get the activation code by logging in to the Nessuscli server.
  ```
  sudo su
  sudo /opt/nessus/sbin/nessuscli fetch --challenge.
  ```
