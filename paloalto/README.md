# How to monitor Paloalto Firewalls with Telegraf, InfluxDB and Grafana
Once you import the Paloalto Dashboard, it should look like this.
![Dashboard](/paloalto/pictures/Dashboard1.png)
![Dashboard](/paloalto/pictures/Dashboard2.png)
![Dashboard](/paloalto/pictures/Dashbaord3.png)

## Setting up the enviroment
If you don't already have a Telegraf, InfluxDB and Grafana instance u can follow these instructions: **Anleitung einfügen**

## Additional Information about the telegraf collector
The telegraf collector checks the ports from 1 - 30. If the port ist acitv it will show up in the grafana dashboard. After u found your acitv ports, it's up to you, if you wanna stop monitoring the other ports. To stop monitoring them, just remove them from the telegraf-panos.conf file.
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
