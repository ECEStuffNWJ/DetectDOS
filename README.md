# DetectDOS
 Quick DOS detection for Linux Server. Makes a snapshot so the Report will be indicative, and aid your early Incident Response.  
 Use cron to run dosde.h regularly. <br/>

# Mitigate a DOS attack
From dosde.sh, identify the IPs attacking you. Block using the following manual commands  
<br/>
**route add "ipaddress" reject**  
**route -n |grep "ipaddress"  to check if blocked**  
<br/>
Also, you can block an IP address using iptables
<br/>
**iptables -A INPUT 1 -s IPADDRESS -j DROP/REJECT**  
**service iptables restart**  
**service iptables save**  
<br/>
Now kill all httpd connections and restart httpd services
<br/>
**killall -KILL httpd**  
**service httpd startssl**  
<br/>
Repeat for all malicious IPs.
<br/>

# Install
git clone https://github.com/ECEStuffNWJ/DetectDOS.git

# Run
cd DetectDOS  
chmod +x *.sh
./install.sh and follow onscreen prompts to install SMTP outgoing only mail server
reboot
./detectdos.sh
Add detectdos.sh to cronjob if needed.

# Results
PLCE OF RESULT ???????????

# License
MIT License

# Author
Nathan W Jones ducatinat@gmail.com

# CPD
Part of EC-Council ECE/CPD Credits
