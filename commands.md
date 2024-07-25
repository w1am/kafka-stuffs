# Commands

## Security

Ref: [Configuring the REST API for Basic HTTP Authentication
](https://docs.confluent.io/platform/current/schema-registry/security/index.html#configuring-the-rest-api-for-basic-http-authentication)

Get the password hash for a user by using the org.eclipse.jetty.util.security.Password utility:

**Powershell**
```psh
Invoke-WebRequest -Uri "https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-util/9.4.43.v20210629/jetty-util-9.4.43.v20210629.jar" -OutFile "$env:TEMP\jetty-util.jar"
java -cp "$env:TEMP\jetty-util.jar" org.eclipse.jetty.util.security.Password letmein
Remove-Item "$env:TEMP\jetty-util.jar"
```

**Curl and WGET**
```bash
curl -s https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-util/9.4.43.v20210629/jetty-util-9.4.43.v20210629.jar -o /tmp/jetty-util.jar && \
java -cp /tmp/jetty-util.jar org.eclipse.jetty.util.security.Password letmein && \
rm /tmp/jetty-util.jar

wget -q https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-util/9.4.43.v20210629/jetty-util-9.4.43.v20210629.jar -O /tmp/jetty-util.jar && \
java -cp /tmp/jetty-util.jar org.eclipse.jetty.util.security.Password letmein && \
rm /tmp/jetty-util.jar
```
