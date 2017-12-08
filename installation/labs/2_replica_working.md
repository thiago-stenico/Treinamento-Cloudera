# 2_replica_working.md
```
[hdfs@ip-172-31-22-225 ~]$ hadoop distcp hdfs://13.59.26.82:8020/input/* hdfs://18.217.157.71:8020/tmp/input
17/12/07 20:42:03 INFO tools.OptionsParser: parseChunkSize: blocksperchunk false
17/12/07 20:42:04 INFO tools.DistCp: Input Options: DistCpOptions{atomicCommit=false, syncFolder=false, deleteMissing=false, ignoreFailures=false, overwrite=false, append=false, useDiff=false, useRdiff=false, fromSnapshot=null, toSnapshot=null, skipCRC=false, blocking=true, numListstatusThreads=0, maxMaps=20, mapBandwidth=100, sslConfigurationFile='null', copyStrategy='uniformsize', preserveStatus=[], preserveRawXattrs=false, atomicWorkPath=null, logPath=null, sourceFileListing=null, sourcePaths=[hdfs://13.59.26.82:8020/input/*], targetPath=hdfs://18.217.157.71:8020/tmp/input, targetPathExists=false, filtersFile='null', blocksPerChunk=0}
17/12/07 20:42:04 INFO tools.SimpleCopyListing: Paths (files+dirs) cnt = 3; dirCnt = 0
17/12/07 20:42:04 INFO tools.SimpleCopyListing: Build file listing completed.
17/12/07 20:42:04 INFO Configuration.deprecation: io.sort.mb is deprecated. Instead, use mapreduce.task.io.sort.mb
17/12/07 20:42:04 INFO Configuration.deprecation: io.sort.factor is deprecated. Instead, use mapreduce.task.io.sort.factor
17/12/07 20:42:05 INFO tools.DistCp: Number of paths in the copy list: 3
17/12/07 20:42:05 INFO tools.DistCp: Number of paths in the copy list: 3
17/12/07 20:42:05 WARN ipc.Client: Failed to connect to server: ip-172-31-23-126.us-east-2.compute.internal/172.31.23.126:8032: retries get failed due to exceeded maximum allowed retries number: 0
java.net.ConnectException: Connection refused
        at sun.nio.ch.SocketChannelImpl.checkConnect(Native Method)
        at sun.nio.ch.SocketChannelImpl.finishConnect(SocketChannelImpl.java:717)
        at org.apache.hadoop.net.SocketIOWithTimeout.connect(SocketIOWithTimeout.java:206)
        at org.apache.hadoop.net.NetUtils.connect(NetUtils.java:530)
        at org.apache.hadoop.net.NetUtils.connect(NetUtils.java:494)
        at org.apache.hadoop.ipc.Client$Connection.setupConnection(Client.java:648)
        at org.apache.hadoop.ipc.Client$Connection.setupIOstreams(Client.java:744)
        at org.apache.hadoop.ipc.Client$Connection.access$3000(Client.java:396)
        at org.apache.hadoop.ipc.Client.getConnection(Client.java:1557)
        at org.apache.hadoop.ipc.Client.call(Client.java:1480)
        at org.apache.hadoop.ipc.Client.call(Client.java:1441)
        at org.apache.hadoop.ipc.ProtobufRpcEngine$Invoker.invoke(ProtobufRpcEngine.java:230)
        at com.sun.proxy.$Proxy13.getNewApplication(Unknown Source)
        at org.apache.hadoop.yarn.api.impl.pb.client.ApplicationClientProtocolPBClientImpl.getNewApplication(ApplicationClientProtocolPBClientImpl.java:217)
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
        at java.lang.reflect.Method.invoke(Method.java:498)
        at org.apache.hadoop.io.retry.RetryInvocationHandler.invokeMethod(RetryInvocationHandler.java:260)
        at org.apache.hadoop.io.retry.RetryInvocationHandler.invoke(RetryInvocationHandler.java:104)
        at com.sun.proxy.$Proxy14.getNewApplication(Unknown Source)
        at org.apache.hadoop.yarn.client.api.impl.YarnClientImpl.getNewApplication(YarnClientImpl.java:206)
        at org.apache.hadoop.yarn.client.api.impl.YarnClientImpl.createApplication(YarnClientImpl.java:214)
        at org.apache.hadoop.mapred.ResourceMgrDelegate.getNewJobID(ResourceMgrDelegate.java:187)
        at org.apache.hadoop.mapred.YARNRunner.getNewJobID(YARNRunner.java:262)
        at org.apache.hadoop.mapreduce.JobSubmitter.submitJobInternal(JobSubmitter.java:157)
        at org.apache.hadoop.mapreduce.Job$10.run(Job.java:1307)
        at org.apache.hadoop.mapreduce.Job$10.run(Job.java:1304)
        at java.security.AccessController.doPrivileged(Native Method)
        at javax.security.auth.Subject.doAs(Subject.java:422)
        at org.apache.hadoop.security.UserGroupInformation.doAs(UserGroupInformation.java:1917)
        at org.apache.hadoop.mapreduce.Job.submit(Job.java:1304)
        at org.apache.hadoop.tools.DistCp.execute(DistCp.java:182)
        at org.apache.hadoop.tools.DistCp.run(DistCp.java:143)
        at org.apache.hadoop.util.ToolRunner.run(ToolRunner.java:70)
        at org.apache.hadoop.tools.DistCp.main(DistCp.java:493)
17/12/07 20:42:05 INFO client.ConfiguredRMFailoverProxyProvider: Failing over to rm156
17/12/07 20:42:05 INFO mapreduce.JobSubmitter: number of splits:3
17/12/07 20:42:05 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1512671246213_0005
17/12/07 20:42:05 INFO impl.YarnClientImpl: Submitted application application_1512671246213_0005
17/12/07 20:42:05 INFO mapreduce.Job: The url to track the job: http://ip-172-31-26-157.us-east-2.compute.internal:8088/proxy/application_1512671246213_0005/
17/12/07 20:42:05 INFO tools.DistCp: DistCp job-id: job_1512671246213_0005
17/12/07 20:42:05 INFO mapreduce.Job: Running job: job_1512671246213_0005
17/12/07 20:42:12 INFO mapreduce.Job: Job job_1512671246213_0005 running in uber mode : false
17/12/07 20:42:12 INFO mapreduce.Job:  map 0% reduce 0%
17/12/07 20:42:19 INFO mapreduce.Job:  map 67% reduce 0%
17/12/07 20:42:22 INFO mapreduce.Job:  map 100% reduce 0%
17/12/07 20:42:22 INFO mapreduce.Job: Job job_1512671246213_0005 completed successfully
17/12/07 20:42:22 INFO mapreduce.Job: Counters: 33
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=463728
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=102401450
                HDFS: Number of bytes written=102400000
                HDFS: Number of read operations=47
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=12
        Job Counters
                Launched map tasks=3
                Other local map tasks=3
                Total time spent by all maps in occupied slots (ms)=23646
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=11823
                Total vcore-milliseconds taken by all map tasks=11823
                Total megabyte-milliseconds taken by all map tasks=18160128
        Map-Reduce Framework
                Map input records=3
                Map output records=0
                Input split bytes=345
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=122
                CPU time spent (ms)=3670
                Physical memory (bytes) snapshot=650145792
                Virtual memory (bytes) snapshot=10728980480
                Total committed heap usage (bytes)=626524160
        File Input Format Counters
                Bytes Read=1105
        File Output Format Counters
                Bytes Written=0
        DistCp Counters
                Bytes Copied=102400000
                Bytes Expected=102400000
                Files Copied=3
```