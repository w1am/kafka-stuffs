# Commands

## Security

Get the password hash for a user by using the org.eclipse.jetty.util.security.Password utility:
```psh
Invoke-WebRequest -Uri "https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-util/9.4.43.v20210629/jetty-util-9.4.43.v20210629.jar" -OutFile "$env:TEMP\jetty-util.jar"
java -cp "$env:TEMP\jetty-util.jar" org.eclipse.jetty.util.security.Password letmein
Remove-Item "$env:TEMP\jetty-util.jar"
```
