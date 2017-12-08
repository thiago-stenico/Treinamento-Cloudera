enterprise/labs/3_api_hive_state.md

Check Status:


}[root@ip-172-31-23-126 ~]# curl -u admin:admin   'http://localhost:7180/api/v1/clusters/TS_Cluster/services/hive'
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-23-126.us-east-2.compute.internal:7180/cmf/serviceRedirect/hive",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD"
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD"
  } ],
  "configStale" : false
}[root@ip-172-31-23-126 ~]#



STOP: 


}[root@ip-172-31-23-126 ~]# curl -X POST -u admin:admin 'http://localhost:7180/api/v1/clusters/TS_Cluster/services/hive/commands/stop'
{
  "id" : 1535,
  "name" : "Stop",
  "startTime" : "2017-12-07T19:39:13.313Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }




START



}[root@ip-172-31-23-126 ~]# curl -X POST -u admin:admin 'http://localhost:7180/api/v1/clusters/TS_Cluster/services/hive/commands/start'
{
  "id" : 1539,
  "name" : "Start",
  "startTime" : "2017-12-07T19:40:05.783Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}[root@ip-172-31-23-126 ~]#


