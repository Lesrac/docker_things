##Do:

`useradd jenkins`
got to /etc/passwd and look for UID and GID of jenkins
use found IDs for docker-compose up command bellow

`docker volume create jenkins_jenkins-data`

do run command below once first and then do the following before doing the run command below again

`sudo chown -R jenkins:jenkins /var/lib/docker/volumes/jenkins_jenkins-data/_data`


##RUN:
`UID_J=1001 GID_J=1001 docker-compose up -d`
