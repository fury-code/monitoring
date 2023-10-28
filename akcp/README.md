# How to Monitor AKCP Sensor with Telegraf, InfluxDB, and Grafana
Once you import the AKCP Dashboard, it should appear as shown below (Some data has been blacked in the images for privacy reasons):
![Dashboard](/akcp/pictures/AKCPDashboard1.jpeg)
![Dashboard](/akcp/pictures/AKCPDashboard2.jpeg)


# Setting Up the Environment
If you don't already have a Telegraf, InfluxDB, and Grafana instance, you can follow these instructions: Insert Instructions Here

# Additional Information about the Telegraf Collector
The Telegraf Collector collects the following OIDs for Temperature Metrics:
```
sensorProbeTempDegree = 1.3.6.1.4.1.3854.1.2.2.1.16.1.3.X
sensorProbeTempStatus = 1.3.6.1.4.1.3854.1.2.2.1.16.1.4.X
```

The Collector also gathers OIDs for the water sensor, dry contact, security, motion sensor, AC Voltage Detector, relay, and siren & strobe light. In the Grafana Dashboard, it's displayed as the Liquid Sensor:
```
sensorProbeSwitchStatus = 1.3.6.1.4.1.3854.1.2.2.1.18.1.3.X
```

You can find more information about the OIDs here: [Documentation](https://www.akcp.com/wp-content/uploads/2012/02/AKCP_OID_SNMP%20manual.pdf)