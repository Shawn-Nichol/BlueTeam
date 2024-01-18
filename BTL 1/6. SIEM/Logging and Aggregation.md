# PRI (PRiorty Value)
THe priority value is derived form both the Facility code and severity level. We can use the simple equation to calculate PRI:

(facility code * 8) + Severity value = PRI

Header
Contains the identifyying information, such as; Timestamp, Hostname, Application name, Message ID. This is useful for understanding where the system message has come from. 

Message
This could be simple readable text or only machine-readable. The content of the message is not defined by the protocol only the format  is. 

