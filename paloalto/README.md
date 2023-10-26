# How to monitor Paloalto Firewalls with Telegraf, InfluxDB and Grafana
Once you import the Paloalto Dashboard, it should look like this.
![Dashboard](/paloalto/pictures/Dashboard1.png)
![Dashboard](/paloalto/pictures/Dashboard2.png)
![Dashboard](/paloalto/pictures/Dashbaord3.png)

## Setting up the enviroment
If you don't already have a Telegraf, InfluxDB and Grafana instance u can follow these instructions: **Anleitung einfügen**
![Monitoring architecture](/paloalto/pictures/MonitoringPaloAlto.png)

## Additional Information about the telegraf collector
The telegraf collector checks the ports from 1 - 30. If the port ist acitv it will show up in the grafana dashboard. After u found your acitv ports, it's up to you, if you wanna stop monitoring the other ports. To stop monitoring them, just remove them from the telegraf-panos.conf file.
![Monitored ports](/paloalto/pictures/PortsMonitroed.png)
