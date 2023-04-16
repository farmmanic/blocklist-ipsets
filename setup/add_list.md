###
##https://wazuh.com/blog/using-osint-to-create-cdb-lists/

##get files alienvault list
sudo wget https://raw.githubusercontent.com/firehol/blocklist-ipsets/master/alienvault_reputation.ipset -O /var/ossec/etc/lists/alienvault_reputation.ipset
sudo wget https://wazuh.com/resources/iplist-to-cdblist.py -O /var/ossec/etc/lists/iplist-to-cdblist.py
sudo chmod +x /var/ossec/etc/lists/iplist-to-cdblist.py
sudo /var/ossec/etc/lists/iplist-to-cdblist.py /var/ossec/etc/lists/alienvault_reputation.ipset /var/ossec/etc/lists/blacklist-alienvault
sudo rm -f /var/ossec/etc/lists/alienvault_reputation.ipset

