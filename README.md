# MinerWatch

MinerWatch makes it possible to monitor asic miners running cgminer (e.g. all Bitmain products) in a single window. You need java version 1.8 or higher to run the tool on your machine, to verify java on your computer type java.exe from the command line or use "search programs and files" option in the start-up menu in Windows, to download java follow this link : http://www.oracle.com/technetwork/java/javase/downloads/jre9-downloads-3848532.html   
MinerWatch displays main parameters enabling you to track the state of all devices in your subnet:
1. URL - IP address
2. Type - device type (e.g. Antminer S9)
3. Status - miner current status, may take several values:  
3.1. Alive - a device can be reached(you ping it) and connected to pool
3.2. Offline - a device can't be reached(you don't ping it). Re-configure your network and make sure that you can ping miner from your PC. See below how to verify all your devices.
3.3. Dead - your device isn't mining, one of the possible reasons - your pool is dead.
4. Pool - shows your mining pool
5. User - your username that you used to setup your miner
6. Elapased - the period of time (hours:minutes:seconds) the miners has been working after the last reboot.
(G)MH/S (RT) - hash rate taken over the last 5 secs.
(G)MH/S (AVG) - avreage hash rate. 
Chip temp. in Celsius on each of your hash plates. Note that different miners have different amount of hash plates.


How to set up
Create manually the folder in your file system, extract minerwatch.zip into the folder. Find minerwattch.config. Add IP address(es) in the following format [{ip:xxx.xxx.xxx.xxx,port:xxxx}]. Each ip address should be surrounded by brackets and separated from each other with comma.
E.g. : [{ip:192.168.0.0,port:4028}, {ip:192.168.0.1,port:4028}, {ip:192.168.0.2,port:4028}]

Use port number 4028 by default, if it doesn't work try to identify the port of your device.

Once you have set up the configuration file run the program in the test mode to verify that all IP addresses are valid. 
Run minerwatchtest.bat from the command line and make sure that all urls are 'Active'.

Log file. 
Log file is created in the same folder and shows all issues with your devices. It detects changes in the connection status. E.g. 
2018-01-19 13:28:32    Total: active ip - 10, offline ip - 0, alive pool - 10, dead pool - 0  
indicates that all your asics are up and mining. 

2018-01-19 13:57:52    Total: active ip - 9, offline ip - 1, alive pool - 9, dead pool - 0
2018-01-19 13:57:52    Offline IPs: 192.168.0.xxx;
indicates that one of your asics lost ip connection.

2018-01-19 14:48:51    Total: active ip - 10, offline ip - 0, alive pool - 7, dead pool - 3
2018-01-19 14:48:51    Dead pools: 192.168.0.xxx;192.168.0.xxx;192.168.0.xxx;
indicates dead pools.

Each log record is accompanied by a summary.
  
It's absolutely for free but if you think it's usefull small donations are welcome :)
here are wallets:
BTC : 35NWrbHU7RRcSHc67NAkQMjFP8faqqCKNT
BCH : 1As5HRERfLxoBrhZEKuqJTVNnWeQKzU27G
LTC : MRKA1if9Em8mkxKhVWEUuuQXpuukgEMtr8
DASH : Xby7kVF6RpTQK2g6mrrSMANu7J5je4AvvV

telegram ID: @hesaid.












  
  
