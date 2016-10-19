Base on https://github.com/patric-r/jvmtop/blob/master/README.md

Show the thread trace on the monitor, u can use tracedeep argument to control how deep the trace should be print.
```
./jvmtop.sh pid --threadlimit 5 --threadnamewidth 500 --tracedeep 15
```

```
PID 25445: com.intellij.rt.execution.application.AppMain 
 ARGS: com.yhd.arch.akka.SimpleServer
 VMARGS: -Xms1024m -Xmx2048m -XX:MaxPermSize=64m -XX:+UseConcMarkSweepGC -[...]
 VM: Oracle Corporation Java HotSpot(TM) 64-Bit Server VM 1.8.0_40
 UP:  0: 0m  #THR: 55   #THRPEAK: 55   #THRCREATED: 56   USER: archer      
 GC-Time:  0: 0m   #GC-Runs: 15        #TotalLoadedClasses: 4214    
 CPU: 38.90% GC:  0.00% HEAP: 299m /1920m NONHEAP:  35m /  n/a

    TID NAME                                    STATE      CPU    TOTALCPU BLOCKEDBY 
     42 New I/O worker #4                    RUNNABLE 15.80%    10.15%       
		sun.nio.ch.NativeThread.current(Native Method)
		sun.nio.ch.SocketChannelImpl.write(SocketChannelImpl.java:468)
		org.jboss.netty.channel.socket.nio.SocketSendBufferPool$UnpooledSendBuffer.transferTo(SocketSendBufferPool.java:203)
		org.jboss.netty.channel.socket.nio.AbstractNioWorker.write0(AbstractNioWorker.java:202)
		org.jboss.netty.channel.socket.nio.AbstractNioWorker.writeFromTaskLoop(AbstractNioWorker.java:152)
		org.jboss.netty.channel.socket.nio.AbstractNioChannel$WriteTask.run(AbstractNioChannel.java:335)
		org.jboss.netty.channel.socket.nio.AbstractNioSelector.processTaskQueue(AbstractNioSelector.java:366)
		org.jboss.netty.channel.socket.nio.AbstractNioSelector.run(AbstractNioSelector.java:290)
		org.jboss.netty.channel.socket.nio.AbstractNioWorker.run(AbstractNioWorker.java:90)
		org.jboss.netty.channel.socket.nio.NioWorker.run(NioWorker.java:178)
		org.jboss.netty.util.ThreadRenamingRunnable.run(ThreadRenamingRunnable.java:108)
		org.jboss.netty.util.internal.DeadLockProofWorker$1.run(DeadLockProofWorker.java:42)
		java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1142)
		java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:617)
		java.lang.Thread.run(Thread.java:745)

```


