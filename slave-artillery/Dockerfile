FROM openshift/jenkins-slave-base-centos7

LABEL org.centos.component="jenkins-slave-artillery" \
      name="jenkins-slave-artillery" \
      architecture="x86_64" \
      io.k8s.display-name="Jenkins Slave artillery" \
      io.k8s.description="Artillery tools on top of the jenkins slave base image" \
      io.openshift.tags="openshift,jenkins,slave,load"
USER root

RUN yum install epel-release -y
RUN yum install jq -y
RUN yum install -y git bzip2 npm

RUN npm install -g artillery

RUN yum clean all

USER 1001
