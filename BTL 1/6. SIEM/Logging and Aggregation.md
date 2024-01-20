# PRI (PRiorty Value)
The priority value is derived from both the Facility code and severity level. We can use the simple equation to calculate PRI:

(facility code * 8) + Severity value = PRI

Header
It contains the identifying information, such as Timestamp, Hostname, Application name, and Message ID. This is useful for understanding where the system message has come from. 

Message
This could be simple, readable text or only machine-readable. The content of the message is not defined by the protocol. Only the format  is. 

# Sysmon
IS a windows system service and device driver that, once installe
