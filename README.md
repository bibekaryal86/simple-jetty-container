# simple-jetty-container

This app creates a simple jetty container to load war files and run the web application (locally).

The app is pretty simple to run with java -jar command, with arguments:
java -jar -Dport=8004 -Dcontextpath=/some-context-path -Dsizeinbytes=20000000 JAR_NAME.jar

As a result the web application whose war file is loaded will run on localhost port 8004 with context
path `some-context-path`

If the web application whose war file will be deployed by this container also requires system variables, provide them
when running as well. For eg:
java -jar -DSPRING_PROFILES_ACTIVE=development -Dport=8004 -Dcontextpath=/some-context-path -Dsizeinbytes=20000000
JAR_NAME.jar
