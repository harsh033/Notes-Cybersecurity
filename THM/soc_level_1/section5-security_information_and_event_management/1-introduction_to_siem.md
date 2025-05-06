It is a tool that collects data from various endpoints/network devices across the network, stores them at a centralized place, and performs correlation on them.

* We can divide our network log sources into two logical parts:
    * Host-Centric Log Sources
    * Network-Centric Log Sources

###  Some key features provided by SIEM are:
 
* Real-time log Ingestion
* Alerting against abnormal activities
* 24/7 Monitoring and visibility
* Protection against the latest threats through early detection
* Data Insights and visualization
* Ability to investigate past incidents.

## Log Sources and Log Ingestion

**log sources**
* for window listed in event viewer
* for linux in `/var/log/` diretory.

### Log Ingestion
some common method used by SIEM for log ingestion:

* 1) Agent/Forwarder - These SIEM solution provides a lightweight tool called an agent(forwarder by splunk) that gets installed in the endpoint. it is configured to capture all the important logs and send them to the SIEM server.

* 2) Syslog - Widely used protocol to collect data from various system.

* 3) Manual Upload - Splunk, ELK etc. allow users to ingest offline data for quick analysis.

* 4) Port-Forwarding - SIEM can be configured to listen on a certain port.

### SOC Analyst Responsibilities

* Monitoring and Investigating
* Identifying False positives
* Tuning Rules which are causing the noise or false positives
* Reporting and Compliance
* Identifying blind spotss in the network visibility and covering them

## Analysing Logs and Alerts

### Dashboard
Each SIEM solution comes with some default dashboards and provides an option for custom Dashboard creation. Some of the information that can be found in a dashboard are:
* Alert highlight
* System Notification
* Health Alert
* List of Failed Login Attempts
* Events Ingested Count 
* Rules triggered 
* Top Domains Visited

### Correlation Rules

Correlation rules are pretty much logical expressions set to be triggered.
* if a user gets 5 login attempts in 10 sec - raise an alert
* if outbound traffic is > 25 MB - raise an alert to potential data exfiltration.
eg - `Alert "Potential CryptoMiner Activity" If EventID = 4688 AND Log_Source = WindowsEventLogs AND ProcessName = (*miner* OR *crypt*)`

### Alert Investigation


