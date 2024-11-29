# Access_Point

This project includes creating a legitimate/fake access point via **hostapd** on a Linux machine and using **dnsmasq** in order to serve it as a DHCP, in addition to that **iptables** is used to enable NAT(Network Address Translation). Upon successfully connecting to the access point, the device will be able to access the internet and all the traffics from the device can be monitored(ex. **Wireshark**) and potentially be manipulated(ex. **Burp Suite**), although its practicality should be questioned due to many security features present in modern networking sysytems.  
