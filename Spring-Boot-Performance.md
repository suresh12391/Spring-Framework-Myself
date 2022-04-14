##### Performance Statics in Spring-Boot:

```
java -version
readlink -f $(which java)

Find ProcessID: `ps -ef | grep java`
```


- htop
- jmap -histo {PID} | head
- ps -au
- pmap {PID}
- sudo -u {USER} jmap -dump:format=b,file=/tmp/heap_application-1.hprof {PID}
- jconsole
- sudo -u {USER} jcmd {PID} GC.heap_dump /tmp/heap-dump-application-1.bin


```
mvn clean spring-boot:run -Dspring-boot.run.jvmArguments=-Xdebug -Dcom.sun.management.jmxremote=true -Dcom.sun.management.jmxremote.port=7072 -Dcom.sun.management.jmxremote.rmi.port=7072 -Dcom.sun.management.jmxremote.authenticate=false -Dcom.sun.management.jmxremote.ssl=false -Dcom.sun.management.jmxremote.local.only=false -Djava.rmi.server.hostname=192.168.43.70
```



##### 3rd Party Tools:

- ELK
- https://heaphero.io/
- https://sentry.io/resources/the-sentry-live-demo/
- https://www.datadoghq.com/pricing/
- https://newrelic.com/
- https://www.ej-technologies.com/products/jprofiler/overview.html





##### Reference Links:

- https://visualvm.github.io/
- https://dzone.com/articles/memory-wasted-by-spring-boot-application
- https://blog.heaphero.io/2017/10/13/how-to-capture-java-heap-dumps-7-options/
- https://www.baeldung.com/java-heap-dump-capture
- https://medium.com/illegalarguments/debugging-spring-boot-applications-for-memory-leaks-4ba5f8bee75a
- https://www.baeldung.com/java-profilers
- https://stackoverflow.com/questions/63034581/how-to-connect-spring-boot-application-remotely-in-visual-vm
- https://stackoverflow.com/questions/35108868/how-do-i-attach-visualvm-to-a-simple-java-process-running-in-a-docker-container

