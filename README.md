# pihole
# 1) INSTALLATION DETAILS - 
    Pi hole is installed by running the following command:
      curl -L https://install.pi-hole.net | bash
     Add a screen shot

# 2) SETTING UP WITH DLINK 
      Reason why it did not work with DLink ?
      Router is then configured to force clients to set their DNS server as your pi hole
      create a new file in the /etc/dnsmasq.d directory and call it "99-dhcp.conf"
      Edit that file so that the contents are similar to this:
      dhcp-range=192.168.0.10,192.168.0.200,72h
      dhcp-option=option:router,192.168.0.1
      dhcp-option=option:dns-server,192.168.0.2
      disable the DHCP service on your router, and then enable the DHCP service in dnsmasq by entering this in the command           line:
     pihole restartdns
     Why do you do all these lines? 

# 3) DETAILS OF CONFIG FILES FOR SETTING UP DHCP
# 4) ADD SCREENSHOTS OF WORKING
# 5) ADD THE ADDITIONAL BLACKLISTED DOMAINS
