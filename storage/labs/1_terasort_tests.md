
[hdfs@ip-172-31-22-225 hadoop-mapreduce]$ time hadoop jar hadoop-mapreduce-examples.jar teragen -D dfs.blocksize=33554432 -Dmapred.map.tasks=4 350000 /tmp/hdfs/3
17/12/06 20:09:30 WARN ipc.Client: Failed to connect to server: ip-172-31-23-126.us-east-2.compute.internal/172.31.23.126:8032: retries get failed due to exceeded maximum allowed retries number: 0
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
        at org.apache.hadoop.mapreduce.Job.waitForCompletion(Job.java:1325)
        at org.apache.hadoop.examples.terasort.TeraGen.run(TeraGen.java:305)
        at org.apache.hadoop.util.ToolRunner.run(ToolRunner.java:70)
        at org.apache.hadoop.examples.terasort.TeraGen.main(TeraGen.java:309)
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
        at java.lang.reflect.Method.invoke(Method.java:498)
        at org.apache.hadoop.util.ProgramDriver$ProgramDescription.invoke(ProgramDriver.java:71)
        at org.apache.hadoop.util.ProgramDriver.run(ProgramDriver.java:144)
        at org.apache.hadoop.examples.ExampleDriver.main(ExampleDriver.java:74)
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
        at java.lang.reflect.Method.invoke(Method.java:498)
        at org.apache.hadoop.util.RunJar.run(RunJar.java:221)
        at org.apache.hadoop.util.RunJar.main(RunJar.java:136)
17/12/06 20:09:30 INFO client.ConfiguredRMFailoverProxyProvider: Failing over to rm156
17/12/06 20:09:30 INFO terasort.TeraGen: Generating 350000 using 4
17/12/06 20:09:31 INFO mapreduce.JobSubmitter: number of splits:4
17/12/06 20:09:31 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
17/12/06 20:09:31 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1512585104579_0011
17/12/06 20:09:31 INFO impl.YarnClientImpl: Submitted application application_1512585104579_0011
17/12/06 20:09:31 INFO mapreduce.Job: The url to track the job: http://ip-172-31-26-157.us-east-2.compute.internal:8088/proxy/application_1512585104579_0011/
17/12/06 20:09:31 INFO mapreduce.Job: Running job: job_1512585104579_0011
17/12/06 20:09:35 INFO mapreduce.Job: Job job_1512585104579_0011 running in uber mode : false
17/12/06 20:09:35 INFO mapreduce.Job:  map 0% reduce 0%
17/12/06 20:09:40 INFO mapreduce.Job:  map 100% reduce 0%
17/12/06 20:09:41 INFO mapreduce.Job: Job job_1512585104579_0011 completed successfully
17/12/06 20:09:41 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=603792
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=337
                HDFS: Number of bytes written=35000000
                HDFS: Number of read operations=16
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=4
                Other local map tasks=4
                Total time spent by all maps in occupied slots (ms)=11433
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=11433
                Total vcore-milliseconds taken by all map tasks=11433
                Total megabyte-milliseconds taken by all map tasks=11707392
        Map-Reduce Framework
                Map input records=350000
                Map output records=350000
                Input split bytes=337
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=209
                CPU time spent (ms)=3840
                Physical memory (bytes) snapshot=744886272
                Virtual memory (bytes) snapshot=11158401024
                Total committed heap usage (bytes)=838336512
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=751290264957846
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=35000000

real    0m13.101s
user    0m5.637s
sys     0m0.254s
[hdfs@ip-172-31-22-225 hadoop-mapreduce]$





TERASORT



[hdfs@ip-172-31-22-225 hadoop-mapreduce]$ time hadoop jar hadoop-mapreduce-examples.jar terasort /tmp/hdfs/3 /tmp/hdfs/terasort
17/12/06 20:15:59 INFO terasort.TeraSort: starting
17/12/06 20:15:59 INFO input.FileInputFormat: Total input paths to process : 4
Spent 102ms computing base-splits.
Spent 2ms computing TeraScheduler splits.
Computing input splits took 105ms
Sampling 4 splits of 4
Making 6 from 100000 sampled records
Computing parititions took 420ms
Spent 527ms computing partitions.
17/12/06 20:16:00 WARN ipc.Client: Failed to connect to server: ip-172-31-23-126.us-east-2.compute.internal/172.31.23.126:8032: retries get failed due to exceeded maximum allowed retries number: 0
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
        at org.apache.hadoop.mapreduce.Job.waitForCompletion(Job.java:1325)
        at org.apache.hadoop.examples.terasort.TeraSort.run(TeraSort.java:316)
        at org.apache.hadoop.util.ToolRunner.run(ToolRunner.java:70)
        at org.apache.hadoop.examples.terasort.TeraSort.main(TeraSort.java:325)
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
        at java.lang.reflect.Method.invoke(Method.java:498)
        at org.apache.hadoop.util.ProgramDriver$ProgramDescription.invoke(ProgramDriver.java:71)
        at org.apache.hadoop.util.ProgramDriver.run(ProgramDriver.java:144)
        at org.apache.hadoop.examples.ExampleDriver.main(ExampleDriver.java:74)
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
        at java.lang.reflect.Method.invoke(Method.java:498)
        at org.apache.hadoop.util.RunJar.run(RunJar.java:221)
        at org.apache.hadoop.util.RunJar.main(RunJar.java:136)
17/12/06 20:16:00 INFO client.ConfiguredRMFailoverProxyProvider: Failing over to rm156
17/12/06 20:16:00 INFO mapreduce.JobSubmitter: number of splits:4
17/12/06 20:16:00 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1512585104579_0012
17/12/06 20:16:01 INFO impl.YarnClientImpl: Submitted application application_1512585104579_0012
17/12/06 20:16:01 INFO mapreduce.Job: The url to track the job: http://ip-172-31-26-157.us-east-2.compute.internal:8088/proxy/application_1512585104579_0012/
17/12/06 20:16:01 INFO mapreduce.Job: Running job: job_1512585104579_0012
17/12/06 20:16:06 INFO mapreduce.Job: Job job_1512585104579_0012 running in uber mode : false
17/12/06 20:16:06 INFO mapreduce.Job:  map 0% reduce 0%
17/12/06 20:16:11 INFO mapreduce.Job:  map 25% reduce 0%
17/12/06 20:16:12 INFO mapreduce.Job:  map 100% reduce 0%
17/12/06 20:16:18 INFO mapreduce.Job:  map 100% reduce 33%
17/12/06 20:16:19 INFO mapreduce.Job:  map 100% reduce 83%
17/12/06 20:16:20 INFO mapreduce.Job:  map 100% reduce 100%
17/12/06 20:16:20 INFO mapreduce.Job: Job job_1512585104579_0012 completed successfully
17/12/06 20:16:20 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=15165457
                FILE: Number of bytes written=31831969
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=35000400
                HDFS: Number of bytes written=35000000
                HDFS: Number of read operations=30
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=12
        Job Counters
                Launched map tasks=4
                Launched reduce tasks=6
                Data-local map tasks=2
                Rack-local map tasks=2
                Total time spent by all maps in occupied slots (ms)=15618
                Total time spent by all reduces in occupied slots (ms)=22386
                Total time spent by all map tasks (ms)=15618
                Total time spent by all reduce tasks (ms)=22386
                Total vcore-milliseconds taken by all map tasks=15618
                Total vcore-milliseconds taken by all reduce tasks=22386
                Total megabyte-milliseconds taken by all map tasks=15992832
                Total megabyte-milliseconds taken by all reduce tasks=22923264
        Map-Reduce Framework
                Map input records=350000
                Map output records=350000
                Map output bytes=35700000
                Map output materialized bytes=15141772
                Input split bytes=400
                Combine input records=0
                Combine output records=0
                Reduce input groups=350000
                Reduce shuffle bytes=15141772
                Reduce input records=350000
                Reduce output records=350000
                Spilled Records=700000
                Shuffled Maps =24
                Failed Shuffles=0
                Merged Map outputs=24
                GC time elapsed (ms)=956
                CPU time spent (ms)=16360
                Physical memory (bytes) snapshot=3190259712
                Virtual memory (bytes) snapshot=28014415872
                Total committed heap usage (bytes)=3469213696
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=35000000
        File Output Format Counters
                Bytes Written=35000000
17/12/06 20:16:20 INFO terasort.TeraSort: done

real    0m22.173s
user    0m6.443s
sys     0m0.317s
[hdfs@ip-172-31-22-225 hadoop-mapreduce]$
