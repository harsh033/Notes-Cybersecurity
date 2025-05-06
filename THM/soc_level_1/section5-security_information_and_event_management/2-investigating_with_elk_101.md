## ElasticStack overview
Elastic stack - Elastic stack is the collection of different open source components linked together to help users take the data from any source and in any format and perform a search, analyze and visualize the data in real-time.

* components
    * Elastic Search - index and store data
    * Logstash - data input/filter/process & output
    * Beats - Data collection agent.
    * Kibana - Analysis & visualization

* Elasticsearch - Elasticsearch is a full-text search and analytics engine used to store JSON-formated documents. supports restful API to interact with the data.

* Logstash - is a data processing engine used to take the data from different sources, apply the filter on it or normalize it, and then send it to the destination which could be kibana or listening port.

* Beats - is a host-based agent known as data-shippers that is used to ship/transfer data from the endpoints to elasticsearch. each beat is a single purpose agent that sends specific data. (eg - filebeat, packetbeat, winlogbeat etc)

* Kibana - is a web based data visualization that works with elasticsearch to analyze, investigate and visualize the data stream in real-time.

## Discover Tab (Kibana)
Discover tab within the Kibana interface contains the logs being ingested manually or in real-time, the time-chart, normalized fields, etc.

## KQL overview

KQL (Kibana Query Language) is a search query language used to search the ingested logs/documents in the elasticsearch. 

* With KQL, we can search for the logs in two different ways.
    - Free text search 
        * eg:- "United States" AND NOT("Florida") 
    - Field text search
        * we can use `FIELD:VALUE` Syntax

## Creating visualizations
The visualization tab allows us to visualize the data in different forms like Table, Pie charts, Bar charts, etc.

