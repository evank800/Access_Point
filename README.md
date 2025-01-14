# Access_Point

<h2>Objectives</h2>

This project includes creating a legitimate/fake access point via **hostapd** on a Linux machine and using **dnsmasq**, in order to serve it as the DHCP server. In addition to that, **iptables** is used to enable NAT(Network Address Translation). 

Upon successfully connecting to the access point, the device will be able to access the internet and all the traffics from the device can be monitored(ex. **Wireshark**) and potentially be manipulated(ex. **Burp Suite**), although its practicality should be questioned due to many security features present in modern networking sysytems.  


<h2>What I have learned:</h2>

<h3>-Practical insight to the general functions of a router/hotspot</h3>

<h3>-Importance of different security features such as:</h3>

<h4>-WPA</h4>Encryption on Layer 2, protection against attacks such as deauthentication attack
    
<h4>-https</h4> Encryption on the application layer => even when the traffic is captured at the AP, the encryption makes it infeasible to read the data.

<h4>-CA Certificate</h4> I have created my own CA Certificate using openssl, sent this to iphone. Although getting the device to download the .crt file is (theoretically) easy enough(ex. by using phishing captive portals), getting the device to trust the certificate is highly infeasible, as it requires the user to take suspiciously many steps to achieve this. 

<h3>-Practical insight to a DHCP server</h3>

<h3>-Deeper understanding of NAT</h3>
<h4>Configuring NAT can almost completely manipulate the incoming packets. </h4>

<h3>-The usage of a network interface</h3>
<h4>I have used an external network interface capable of monitor mode for this project.</h4>





<h2>DEMO</h2>
<h3>Connect the Interface</h3>
<img src="https://github.com/evank800/Access_Point/blob/main/Dropbox/IMG_4489.jpeg"></img>

<h3>hostapd configuration</h3>
<img src="https://github.com/evank800/Access_Point/blob/main/Dropbox/IMG_4497.jpeg"></img>

<h3>dnsmasq configuration</h3>
<img src="https://github.com/evank800/Access_Point/blob/main/Dropbox/IMG_4498.jpeg"></img>

<h3>start both hostapd and dnsmasq</h3>
<img src="https://github.com/evank800/Access_Point/blob/main/Dropbox/IMG_4490.jpeg"></img>

<h3>Check the interface</h3>
<img src="https://github.com/evank800/Access_Point/blob/main/Dropbox/IMG_4495.jpeg"></img>

<h3>NAT Table</h3>
<img src="https://github.com/evank800/Access_Point/blob/main/Dropbox/IMG_4494.jpeg"></img>

<h3>Look for AP on Phone</h3>
<img src="https://github.com/evank800/Access_Point/blob/main/Dropbox/IMG_4491.png"></img>

<h3>Check configurations</h3>
<img src="https://github.com/evank800/Access_Point/blob/main/Dropbox/IMG_4492.png"></img>

<h3>Access captive portal associated with the static ip(of the AP) </h3>
<img src="https://github.com/evank800/Access_Point/blob/main/Dropbox/IMG_4493.png"></img>

<h3>Custom .crt file(here named Ghost)</h3>
<img src="https://github.com/evank800/Access_Point/blob/main/Dropbox/IMG_4496.png"></img>
