# MinerWatch
1. Overview
MinerWatch makes it possible to monitor ASIC miners running cgminer (e.g. all Bitmain production) in a single window.

You need java version 1.8 or higher to run the MinerWath on you machine. 
MinerWatch displays main paramters enabling you to track the state of all devices in your subnet:
URL - IP address
Type - device type (e.g. Antminer S9)
Status - miner current status. It may take several values:  
  1)Alive - a device can be reached(ping) and connected to pool
  2)Offline - a device can't be reached(ping). Re-configure your network and make sure that you can ping miner from your PC. See below how   to verify all your devices.
  3)Dead - your device isn't mining, one of the possible reasons is that your pool is dead.
Pool - shows your mining pool
User - your username that you used to setup your miner
Elapased - the period of time (hours:minutes:seconds) the miners has been working after the last restart.
(G)MH/S (RT) - hash rate taken over the last 5 sec
(G)MH/S (AVG) - avreage hash rate. Refer to miner documentation to figure out period of time taken to calculate average.
Chip temp in Celsius on each of your hash plates. Note that different miners have different amount of hash plates.

At the bottom, below the list there total values focusing your attention on the most important values.

2. How to set up
Create manually the folder in your file system, extract minerwatch.zip into the folder. Find minerwattch.config. Add IP address(es) in the following format [{ip:xxx.xxx.xxx.xxx,port:xxxx}]. Each ip address should be surrounded by brackets and separated from each other with comma.
E.g. : [{ip:192.168.0.0,port:4028}, {ip:192.168.0.1,port:4028}, {ip:192.168.0.2,port:4028}]

Use port number 4028 by default, if it doesn't work try to identify the port of you device.

Once you have set up the configuration file. Run the program in the test mode to verify that all IP addresses are valid. 
Run minerwatchtest.bat from command line and make sure that all urls are 'Active'.

3. Log file. 
log file created in the same folder shows all issues with your devices. It detects changes in the connection status. E.g. 
2018-01-19 13:28:32    Total: active ip - 10, offline ip - 0, alive pool - 10, dead pool - 0  
indicates that all your asics are up and mining. 

2018-01-19 13:57:52    Total: active ip - 9, offline ip - 1, alive pool - 9, dead pool - 0
2018-01-19 13:57:52    Offline IPs: 192.168.0.xxx;
indicates that one of your asics lost ip connection.

2018-01-19 14:48:51    Total: active ip - 10, offline ip - 0, alive pool - 7, dead pool - 3
2018-01-19 14:48:51    Dead pools: 192.168.0.xxx;192.168.0.xxx;192.168.0.xxx;
indicates dead pools.

Each log record is accompanied by summary.

4. Limitations.

Version 'L'supports 'home' miners - up to 3 miners for free.
Version 'F' supports unlimited amount of miners for a symbolic amount of money - 20 USD.  I accept equivalent in BTC, BCH, LTC, DASH.
Once your decide to get the full version, please send email to minerwatch@gmail.com I'll reply you with the address of the wallet and once accepted I'll send the full version.  
You can also reach me in telegram  - @hesaid.












  
  
