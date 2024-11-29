# Access_Point

<h2>Objectives</h2>
This project includes creating a legitimate/fake access point via **hostapd** on a Linux machine and using **dnsmasq**, in order to serve it as the DHCP server. In addition to that, **iptables** is used to enable NAT(Network Address Translation). 

Upon successfully connecting to the access point, the device will be able to access the internet and all the traffics from the device can be monitored(ex. **Wireshark**) and potentially be manipulated(ex. **Burp Suite**), although its practicality should be questioned due to many security features present in modern networking sysytems.  


<h2>What I have learned</h2>
-Practical insight to the functions of a router. 
-Importance of different security features such as:
    **WPA**: Encryption on Layer 2, protection against attacks such as Deauthentication attack
    **https**: Encryption on the application layer => even when the traffic is captured in the 
