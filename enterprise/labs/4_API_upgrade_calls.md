enterprise/labs/4_API_upgrade_calls.md


[root@ip-172-31-23-126 ~]# curl -u admin:admin   'http://localhost:7180/api/v1/cm/version'
{
  "version" : "5.12.1",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20170818-0807",
  "gitHash" : "9bdee611802535491d400e03c98ef694a2c77d0a",
  "snapshot" : false
}[root@ip-172-31-23-126 ~]#

___________________



[root@ip-172-31-23-126 ~]# curl -u admin:admin   'http://localhost:7180/api/v1/users'
{
  "items" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "tarkin",
    "roles" : [ "ROLE_ADMIN" ]
  } ]
}[root@ip-172-31-23-126 ~]#


________________

