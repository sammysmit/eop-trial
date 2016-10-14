# eop-trial

Gradle based Spring Cloud (Zuul, Spring Boot) project to deploy in Google AppEngine Standard Environment (Java 7, Servlet 2.5).

Project created by following these instructions: https://cloud.google.com/appengine/docs/java/tools/gradle 

Can't consider the alternative Google AppEngine Flexible Environment (Java 8, Servlet 3.x).

Command to simulate running in AppEngine locally:
```sh
./gradlew appengineRun
```

What's the reason for:
```code
java.lang.ClassNotFoundException: com.google.appengine.api.ThreadManager
        at java.net.URLClassLoader$1.run(URLClassLoader.java:366) ~[na:1.7.0_80]
        at java.net.URLClassLoader$1.run(URLClassLoader.java:355) ~[na:1.7.0_80]
        at java.security.AccessController.doPrivileged(Native Method) [na:1.7.0_80]
        at java.net.URLClassLoader.findClass(URLClassLoader.java:354) ~[na:1.7.0_80]
        at java.lang.ClassLoader.loadClass(ClassLoader.java:425) ~[na:1.7.0_80]
        at com.google.appengine.tools.development.IsolatedAppClassLoader.loadClass(IsolatedAppClassLoader.java:198) ~[appengine-local-runtime.jar:na]
        at java.lang.ClassLoader.loadClass(ClassLoader.java:358) ~[na:1.7.0_80]
        at java.lang.Class.forName0(Native Method) ~[na:1.7.0_80]
        at java.lang.Class.forName(Class.java:195) ~[na:1.7.0_80]
        at com.netflix.hystrix.util.PlatformSpecific.getAppEngineThreadFactory(PlatformSpecific.java:64) ~[hystrix-core-1.5.5.jar:1.5.5]
```

