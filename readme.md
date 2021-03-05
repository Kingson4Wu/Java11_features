<pre>
/usr/local/gradle-6.8.3/bin/gradle idea  -Dorg.gradle.java.home=/usr/local/jdk11/jdk-11.0.10.jdk/Contents/Home

https://segmentfault.com/a/1190000016527932

328: Flight Recorder
相关解读Java 11 Features: Java Flight Recorder
Flight Recorder以前是商业版的特性，在java11当中开源出来，它可以导出事件到文件中，之后可以用Java Mission Control来分析。可以在应用启动时配置java -XX:StartFlightRecording，或者在应用启动之后，使用jcmd来录制，比如
$ jcmd <pid> JFR.start
$ jcmd <pid> JFR.dump filename=recording.jfr
$ jcmd <pid> JFR.stop

废除Nashorn javascript引擎，在后续版本准备移除掉，有需要的可以考虑使用GraalVM

java11是java改为6个月发布一版的策略之后的第一个LTS(Long-Term Support)版本(oracle版本才有LTS)，这个版本最主要的特性是：在模块方面移除Java EE以及CORBA模块，在JVM方面引入了实验性的ZGC，在API方面正式提供了HttpClient类。
从java11版本开始，不再单独发布JRE或者Server JRE版本了，有需要的可以自己通过jlink去定制runtime image

</pre>