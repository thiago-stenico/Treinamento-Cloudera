enterprise/labs/0_CM_treasure_hunt.md

What is ubertask optimization?

Threshold for number of maps, beyond which a job is considered too big for ubertask optimization.

Where in CM is the Kerberos Security Realm value displayed?

Cluster -> Administration -> Settings -> Kerberus = HADOOP.COM

Which CDH service(s) host a property for enabling Kerberos authentication?

 All services in the cluster.

How do you upgrade the CM agents?

You can use CM Parcels. Clicking in hosts > parcels > configuration and add the Cloudera official parcels reposiroty location.
After that click in check for new parcells and distribut and install the new agent package

Give the tsquery statement used to chart Hue's CPU utilization?
cgroup_cpu_system_rate	

Name all the roles that make up the Hive service
Gateway, WebHCat Server, Hive Metastore Server, HiveServer2

What steps must be completed before integrating Cloudera Manager with Kerberos?

Ensure you have secured communication between the Cloudera Manager Server and Agents before you enable Kerberos on your cluster. Kerberos keytabs are sent from the Cloudera Manager Server to the Agents, and must be encrypted to prevent potential misuse of leaked keytabs. For secure communication, you should have at least Level 1 TLS enabled