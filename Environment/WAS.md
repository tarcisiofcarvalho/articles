# WebSphere Application Server

### Commands

```sh
# From a command prompt, go to the [appserver root]/bin directory

# Start Server
./startServer.sh

# Stop Server
./stopServer.sh

# Status Server
./statusServer.sh
```
### Enable Deployment Monitoring Folder

You can setup Websphere Applicaton Server to automatically deploy WAR/EAR/JAR/SAR products when you move one of them to a monitored folder. Take a look:

* Go to WAS Admin Console
* Applications > Global deployment settings
* Enable the "Monitor directory to automatically deploy applications"
* On Monitoring Directory set your owned path or keep the default
* Save

After this step, every 5 minutes the WAS will check the following folder

```sh
<path you provided>/servers/<your server name>/
```

### Enable WebSphere in Debug Mode

On WebSphere Application Server Console go to:

* Servers > Server Types > WebSphere application servers
* Under Server Infrastructure section > expand Java and Process Management > Process definition
* Under Additional Properties section > click Java Virtual Machine
* Checked the Debug Mode
* In Debug arguments set: -Xdebug -Xnoagent -Xrunjdwp:transport=dt_socket,server=y,suspend=n,address=8888

### Eclipse Enable Java Remote Debug

On your Eclipse go to project properties:

* Click on “Run”, “Debug Configurations…”
* Select “Remote Java Application”, right click and select “New”
* Renamed a new name , e.g “WebSphere 7 Instance”
* In “Connection Type”, select default, “Standard (Socket Attached)”
* Host, put your WebSphere host IP
* Port, put 8888.

### References

(https://www.mkyong.com/websphere/remote-debugging-with-eclipse-websphere-7/)
