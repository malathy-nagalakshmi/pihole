# pihole
# 1) INSTALLATION DETAILS - 
    Pi hole is installed by running the following command:
      curl -L https://install.pi-hole.net | bash
     Add a screen shot

# 2) SETTING UP WITH DLINK 
      Reason why it did not work with DLink ?
      Dlink routers requires dns ip and lan ip to be on different networks.Therefore dhcp is enabled in pihole
      Router is then configured to force clients to set their DNS server as your pi hole
      create a new file in the /etc/dnsmasq.d directory and call it "99-dhcp.conf"
      Edit that file so that the contents are similar to this:
      dhcp-range=192.168.0.10,192.168.0.200,72h
      dhcp-option=option:router,192.168.0.1
      dhcp-option=option:dns-server,192.168.0.2
    This will set the DHCP range from 192.168.0.10 to 192.168.0.200. The router option tells dnsmasq   what the IP address is of your router. 
      option:dns-server should be changed to the IP address of your PiHole server
      disable the DHCP service on your router, and then enable the DHCP service in dnsmasq by entering this in the command           line:
     pihole restartdns
     

# 3) DETAILS OF CONFIG FILES FOR SETTING UP DHCP
# 4) ADD SCREENSHOTS OF WORKING
# 5) ADD THE ADDITIONAL BLACKLISTED DOMAINS
