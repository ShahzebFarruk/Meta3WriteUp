### Nmap commands

Nmap Commands:
Here is the list of Nmap Commands:

1. Scan a Range of IP Address
2. Port Scanning
3. Ping Scan Using Nmap
4. Saving the Nmap Scan Output to a File
5. Most Popular Ports Scanning
6. Display Open Ports:
7. Exclude Host/ IP Addresses for the Scan
8. Service Version Detection

#### 1. Scan a Range of IP Address: To scan a range of IP addresses, the Nmap command is as follows:
     `nmap 192.168.1.1-24`

#### 2. Port Scanning: There are multiple commands in Nmap for scanning ports such as:
>   To scan TCP port 80, the following Nmap command can be used:

      `nmap -p T:80 192.168.1.1`

>   To scan UDP port 53:

     `nmap -p U:53 192.168.1.1`

 >    To scan the range of ports:

     `nmap -p 80-160 192.168.1.1`
>    We can also combine all these commands to scan multiple ports:

        `nmap -p U:53, 112, 135, T:80, 8080 192.168.1.1`
#### 3. Ping Scan Using Nmap: It can be used for host discovery and the following command can be used:
     ```nmap -sP 192.168.1.1/20```
#### 4. Saving the Nmap Scan Output to a File: The syntax for the command to save the Nmap output to a text file is as follows:
       `nmap 192.168.1.1 > op.txt`
      `nmap -oN /temp/files/output/ 192.168.1.1`
      `nmap -oN op.txt 192.168.1.1`
      
#### 5. Most Popular Ports Scanning: The most popular TCP ports can be scanned using TCP SYN scan and the following command exists for this purpose:
     `nmap -sS 192.168.1.1`
>    the above command is used for stealthy scan
>    For OS fingerprinting, the following command can be used:
     `nmap -sT 192.168.1.1`
     
#### 6. Display Open Ports: The command for displaying open ports on the network is as follows:
     `nmap –open 192.168.1.1`
     `nmap –open server2.gl.biz`
     `nmap –open 192.168.0.1`
#### 7. Exclude Host/ IP Addresses for the Scan: In order to exclude the hosts from the Nmap scan, you can use the following Nmap commands:
>    If you are scanning a number of hosts/networks, then you can exclude hosts/IPs from a scan by using:
     `nmap 192.168.1.1-24 –exclude 192.168.1.4`
     OR
     `nmap 192. 168.1.1-24 –exclude 192.168.1.3, 192.168.1.7`   for excluding more than one host.

#### 8. Service Version Detection: The service version can be detected for IPv4 script with the help of Nmap by using any of the following commands:
     `nmap -A 192.168.1.254`
     `nmap -v -A 192.168.1.1`
     `nmap -A -iL /user/temp/list.txt`
