# How to monitor Paloalto Firewalls with Telegraf, InfluxDB and Grafana
Once you import the Paloalto Dashboard, it should look like this (some data has been blacked in the images for privacy reasons):
![Dashboard](/paloalto/pictures/FirewallPaloAlto1.png)
![Dashboard](/paloalto/pictures/FirewallPaloAlto2.png)

# Additional Information about the Telegraf Collector
The Telegraf collector checks ports from 1 to 30. If the port is active, it will appear on the Grafana dashboard. After you identify your active ports, it's up to you whether you want to stop monitoring the other ports. To stop monitoring them, simply remove them from the telegraf-panos.conf file. We also recommend editing the overrides used in the "Active Session", "Traffic In" and "Traffic Out" panels because the installed overrides were created for our specific ports.
```
[[inputs.snmp.field]]
  name = "ifHCOutOctets.1"
  oid = ".1.3.6.1.2.1.31.1.1.1.10.1"
[[inputs.snmp.field]]
  name = "ifHCOutOctets.2"
  oid = ".1.3.6.1.2.1.31.1.1.1.10.2"
[[inputs.snmp.field]]
  name = "ifHCOutOctets.3"
  oid = ".1.3.6.1.2.1.31.1.1.1.10.3"
[[inputs.snmp.field]]
  name = "ifHCOutOctets.4"
  oid = ".1.3.6.1.2.1.31.1.1.1.10.4"
```
