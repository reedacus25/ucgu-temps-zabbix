# ucgu-temps-zabbix

This is a very basic Zabbix template (v5.2+) to discover and collect temperature values for temperature sensors on Unifi Cloud Gateway Ultra (UCGU).
Based on a very cursory test, I believe this will work with other Unifi Gateways like the UDM-Pro running OS3+

While outside the scope of this template, this requires the zabbix-agent or zabbix-agent2 to be installed on the UCGU.

There are two macros that can be set to tune this template to match your requirements.

|   **Macro**   |   **Default Value**   |   **Description**   |
| --- | --- | --- |
|   {$TEMP\_SENSOR\_DIR}   |   /sys/class/thermal/   |   Directory to read temperature sensors from   |
|   {$TEMP\_WARN}   |   50   |   Temperature value to warn at   |

Warning temperature of 50ºC is not based on a specific value, it was just higher than my normal temperatures, and seemed like an easy starting threshold.

Hopefully this will be useful to others.
