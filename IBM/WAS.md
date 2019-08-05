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

# SyncNode
./syncNode.sh

# Start Web Console
# from AppSvr/bin
./startManager.sh
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

### Check JVM version running on Websphere Application Server

Go to your server logs folder, as example below:

```sh
cd opt/IBM/WebSphere/AppServer/profiles/AppSrv01/logs/server1
```

Execute head command on native_stdout.log or systemOut.log file:

```sh
head native_stdout.log
```

You will see message as below where you can check the Java version:

```sh
************ Start Display Current Environment ************
WebSphere Platform 9.0.5.0 [BASE 9.0.5.0 f5001923.01] [JAVA8 8.0.5.37 pxa6480sr5fp37-20190618_01] running with process name DefaultCell01\DefaultNode01\server1 and process id 660
Full server name is DefaultCell01\DefaultNode01\server1-660
Host Operating System is Linux, version 4.9.125-linuxkit
Java version = 1.8.0_211, Java Runtime Version = 8.0.5.37 - pxa6480sr5fp37-20190618_01(SR5 FP37), Java Compiler = j9jit29, Java VM name = IBM J9 VM
was.install.root = /opt/IBM/WebSphere/AppServer
user.install.root = /opt/IBM/WebSphere/AppServer/profiles/AppSrv01
Java Home = /opt/IBM/WebSphere/AppServer/java/8.0/jre
ws.ext.dirs = /opt/IBM/WebSphere/AppServer/java/8.0/lib:/opt/IBM/WebSphere/AppServer/profiles/AppSrv01/classes:/opt/IBM/WebSphere/AppServer/classes:/opt/IBM/WebSphere/AppServer/lib:/opt/IBM/WebSphere/AppServer/installedChannels:/opt/IBM/WebSphere/AppServer/lib/ext:/opt/IBM/WebSphere/AppServer/web/help:/opt/IBM/WebSphere/AppServer/deploytool/itp/plugins/com.ibm.etools.ejbdeploy/runtime
Classpath = /opt/IBM/WebSphere/AppServer/profiles/AppSrv01/properties:/opt/IBM/WebSphere/AppServer/properties:/opt/IBM/WebSphere/AppServer/lib/startup.jar:/opt/IBM/WebSphere/AppServer/lib/bootstrap.jar:/opt/IBM/WebSphere/AppServer/lib/jsf-nls.jar:/opt/IBM/WebSphere/AppServer/lib/lmproxy.jar:/opt/IBM/WebSphere/AppServer/lib/urlprotocols.jar:/opt/IBM/WebSphere/AppServer/deploytool/itp/batchboot.jar:/opt/IBM/WebSphere/AppServer/deploytool/itp/batch2.jar:/opt/IBM/WebSphere/AppServer/java/8.0/lib/tools.jar
```

### server.xml and other config files location

```sh
/opt/IBM/WebSphere/AppServer/profiles/AppSrv01/config/cells/DefaultCell01/nodes/DefaultNode01/servers/server1
```

### References

(https://www.mkyong.com/websphere/remote-debugging-with-eclipse-websphere-7/)
