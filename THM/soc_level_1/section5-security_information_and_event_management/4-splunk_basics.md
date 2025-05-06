Splunk is one of the leading SIEM solutions in the market that provides the ability to collect, analyze and correlate the network and machine logs in real-time.

## Splunk components
Splunk has three main components.

### 1 Splunk Forwarder
* lightweight agent installed on the endpoint intended to be monitored, and its main task is to collect the data and send it to the Splunk instance.

### 2 Splunk Indexer
* It main role is processing the data it receives form forwarders. it takes the data, normalizes it into field-value pairs, determines the datatype of the data, and stores them as events. Processed data is easy to search and analyze.

### 3 Search Head
* Here user can search the indexed logs. user can use splunk processing language for (SPL) for search queries.

## Navigating Splunk

### Splunk bar
* In the Splunk Bar, you can see system-level messages ( Messages ), configure the Splunk instance ( Settings ), review the progress of jobs ( Activity ), miscellaneous information such as tutorials ( Help ), and a search feature ( Find ). 

### Apps Panel
* In this panel, you can see the apps installed for the splunk instance. The default app for every splunk installation is **search and reporting**.

### Explore splunk
* This panel contains quick links to **add data**(adds different types of logs) to the splunk instance, add new **splunk apps**, and access the **splunk documentation**.

### Splunk Dashboard
* You can choose from a range of dashboards readily available within your Splunk instance. You can select a dashboard from the dropdown menu or by visiting the dashboards listing page. you can also create dashboards and add them to the Home Dashboard.



