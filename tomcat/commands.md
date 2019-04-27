#### Tomcat Service File for CentOS 7

Name With Location :  /etc/systemd/system/tomcat.service
```bash
[Unit]
Description=Tomcat Container
After=network.target

[Service]
Type=forking


User=root
Group=root


Environment='UMASK=0022'
#Environment=CATALINA_PID=/opt/tomcat-latest/tomcat8.pid
#Environment=TOMCAT_JAVA_HOME=/usr/java/default
#Environment=CATALINA_HOME=/opt/tomcat-latest
#Environment=CATALINA_BASE=/opt/tomcat-latest
#Environment=CATALINA_OPTS=
#Environment="JAVA_OPTS=-Dfile.encoding=UTF-8 -Dnet.sf.ehcache.skipUpdateCheck=true -XX:+UseConcMarkSweepGC -XX:+CMSClassUnloadingEnabled -XX:+UseParNewGC -Xms256m -Xmx256m"

ExecStart=/location/tomcat/bin/startup.sh
ExecStop=/bin/kill -15 $MAINPID

[Install]
WantedBy=multi-user.target
```